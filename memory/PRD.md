# OpenClaw Multi-Agent Business Model Pipeline

## Original Problem Statement
Автоматический поиск, фильтрация и валидация бизнес-моделей 24/7. Telegram-боты в Supergroup. `core-chief` самообучается.

## VPS: `188.214.107.181`
- AGENTS.md: `/srv/openclaw/config/workspace-branch-models-lead/AGENTS.md` (911 строк)
- Jobs: `/srv/openclaw/config/cron/jobs.json` (16 jobs, 14 enabled)
- Wordstat Service: `/srv/openclaw/wordstat_proxy.py` → systemd → port 9001
- Command Processor: `/srv/openclaw/command_processor.py` → cron */5 * * * *
- Stale Detector: `/srv/openclaw/stale_detector.py` → cron 0 5 * * *
- TG Notifier: `/srv/openclaw/tg_notifier.py` → cron */10 * * * *

## SSH Whitelist (постоянный, через iptables)
Добавлены подсети Google Cloud в `/etc/iptables/rules.v4` и hook `if-pre-up.d`:
- 34.0.0.0/8, 35.0.0.0/8, 104.0.0.0/8 (все Google Cloud IPs)
Если SSH снова блокируется: добавить IP через VPS-консоль:
`iptables -I INPUT 1 -s <IP> -j ACCEPT && iptables-save > /etc/iptables/rules.v4`

## Wordstat Setup (нужен токен!)
Сервис запущен: `http://localhost:9001/health` → ok
Для активации реального Wordstat: добавить OAuth-токен в `/srv/openclaw/config/wordstat.env`
```
YANDEX_OAUTH_TOKEN=<ваш_токен>
```
Получить токен: https://oauth.yandex.ru → создать приложение → scopes: wordstat

## Telegram Topics
| Topic | Назначение |
|-------|------------|
| 267 | Подтверждённые модели (APPROVED ≥70) |
| 270 | Отклонённые + Near-Pass (REJECTED / NEAR-PASS 65-69) |
| 8 | Дайджест + Health Dashboard |
| 76 | Обучение (feedback, команды) |

## Telegram Commands (пишутся в любом топике группы)
| Команда | Что делает |
|---------|------------|
| `/relaunch <case-slug>` | Сбросить кейс для переработки |
| `/status` | Статус пайплайна |
| `/sectors` | Статистика по секторам |
| `/help` | Справка |

## Auto-Posting (Telegram)
Система работает в двух режимах:
1. **OpenClaw agent** (Program 7: Critic): после создания 06-verdict.md агент сам отправляет сообщения в Telegram, затем создаёт маркер `.telegram-sent`
2. **tg_notifier.py** (cron */10): резервный механизм — отправляет кейсы с 06-verdict.md без маркера (failsafe на случай если агент не создал маркер)

### Маркер `.telegram-sent`
Файл в папке кейса. Формат: `sent=ВЕРДИКТ score=X/100 ts=ISO-DATE`
Предотвращает дублирование отправки.

## Devil's Advocate (Near-Pass 65-69)
Для каждого Near-Pass кейса агент отправляет **СООБЩЕНИЕ 3** в topic 270:
- 3 конкретных сценария провала за 6 месяцев (финансовый, конкурентный, операционный)
- Ранние сигналы для каждого сценария
- Итоговая рекомендация: /relaunch или отклонить окончательно

## All Cron Jobs (14 enabled)
| Job | Schedule | Назначение |
|-----|----------|------------|
| radar-b2b-ops | 12,42 * * * * | AI-автоматизация, AI-агентства |
| radar-ai-services | 17,47 * * * * | AI-услуги на заказ |
| radar-quick-ai | 22,52 * * * * | TG-боты, 1 услуга = быстрый результат |
| radar-geo-expansion | 27,57 * * * * | Западные модели без аналога в РФ |
| models-intake-triage | 25,55 * * * * | Triage + Auto-enrich 01-evidence.md |
| chief-models-review | 58 * * * * | Ревью качества |
| models-demand-validation | 30 * * * * | Demand: Wordstat + HH.ru + Avito + TG + vc.ru |
| models-economics | 5 */2 * * * | Unit economics RUB + ScoreTrajectory |
| models-finance | 35 */2 * * * | P&L 3 scenarios + Critic + ScoreTrajectory |
| models-critic | 55 */2 * * * | Verdict 0-100 + Near-Pass + Devil's Advocate + Telegram |
| models-digest | 0 9 * * * | Digest + Health Dashboard |
| chief-supervisor | 0 */6 * * * | Self-learning + Sector Analytics |
| models-feedback-loop | 30 */6 * * * | User feedback → SEARCH_PREFERENCES |
| models-market-pulse | 0 10 * * 0 | Weekly Wordstat trend check |

System crons (host VPS):
- `*/5 * * * *` → command_processor.py (Telegram /relaunch, /status, /sectors)
- `*/10 * * * *` → tg_notifier.py (авто-постинг новых вердиктов в Telegram)
- `0 5 * * *` → stale_detector.py (stale cases alert to topic 76)

## Sectors
B2B-OPS | AI-SERVICES | QUICK-AI | HEALTHCARE | FINTECH | GEO-EXPAND

## Key Rules
- LTV Gate: > 500 000 руб/мес
- Score: ≥70 APPROVED, 65-69 NEAR-PASS, <65 REJECTED
- Wordstat: via proxy localhost:9001 (requires OAuth token) + fallback multi-source
- Язык: ТОЛЬКО РУССКИЙ | Валюта: РУБЛИ

## Pipeline State (последнее обновление: 2026-04-14)
### Rejected (7 кейсов)
| Кейс | Score | Статус TG |
|------|-------|-----------|
| ai-customer-service-operations-operator | 54/100 | ✅ sent topic 270 |
| ai-finance-supply-chain-operations-operator | 55/100 | ✅ sent topic 270 |
| ai-marketing-ops-microagency | 43/100 | ✅ sent topic 270 |
| enterprise-agentic-marketing-implementation-operator | 58/100 | ✅ sent topic 270 |
| enterprise-ai-process-automation-operator | 68/100 NEAR-PASS | ✅ sent topic 270 |
| enterprise-contract-operations-agents | 54/100 | ✅ sent topic 270 |
| draft-ai-support-local-clinics | manual reject | нет verdict |

### Active cases (11 кейсов, в пайплайне)
- ai-manufacturing-quoting-operator
- ai-native-salesforce-implementation-operator
- ai-songs-on-demand-service (QUICK-AI, создан 2026-04-14, ожидает demand-validation)
- ambient-clinical-documentation-operator
- autonomous-b2c-crm-operator
- autonomous-enterprise-service-operations-operator (возвращён из rejected, нужен 05-critic.md)
- autonomous-medical-coding-operator
- enterprise-agent-control-plane-implementation-operator
- expert-human-data-ops-for-ai-models-operator
- investment-banking-ai-analyst-operator
- openclaw-contours-agency

## Backlog
### P0 (DONE в сессии 2026-04-14)
- ✅ Исправить права файлов root→1000 (EACCES в логах)
- ✅ Devil's Advocate для Near-Pass (3 сценария провала)
- ✅ Авто-постинг rejected/approved в Telegram топики
- ✅ Ретроспективная рассылка 6 существующих кейсов
- ✅ Исправить Telegram 409 конфликт в command_processor.py
- ✅ Постоянный whitelist SSH (Google Cloud подсети)

### P1
- Активировать Wordstat токен (пользователь должен получить OAuth)
- Stale case — поправить порог если нужно (сейчас 7 дней)
- Мониторинг прогрессии ai-songs-on-demand-service через пайплайн

### P2
- Конкурентный радар (мониторинг approved конкурентов)
- Webhook topic 76 → FEEDBACK_LOG.md (сейчас polling)
- radar-healthcare, radar-fintech

### P3
- Pattern learning в chief-supervisor
- Дедупликация при intake (semantic similarity)
- LTV Upside Calculator (что нужно улучшить чтобы пройти порог)
- Минимум 3 независимых источника для demand validation

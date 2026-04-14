# OpenClaw Multi-Agent Business Model Pipeline

## Original Problem Statement
Автоматический поиск, фильтрация и валидация бизнес-моделей 24/7. Telegram-боты в Supergroup. `core-chief` самообучается.

## VPS: `188.214.107.181`
- AGENTS.md: `/srv/openclaw/config/workspace-branch-models-lead/AGENTS.md` (957 строк)
- Jobs: `/srv/openclaw/config/cron/jobs.json` (16 jobs, 14 enabled)
- Wordstat Proxy: `/srv/openclaw/wordstat_proxy.py` → systemd → port 9001
- Command Processor: `/srv/openclaw/command_processor.py` → cron */5 * * * *
- Stale Detector: `/srv/openclaw/stale_detector.py` → cron 0 5 * * *
- TG Notifier: `/srv/openclaw/tg_notifier.py` → cron */10 * * * *

## SSH Whitelist (постоянный)
Добавлено в `/etc/ufw/before.rules` (переживает ufw reload и reboot):
```
-A ufw-before-input -s 34.0.0.0/8 -j ACCEPT
-A ufw-before-input -s 35.0.0.0/8 -j ACCEPT
-A ufw-before-input -s 104.0.0.0/8 -j ACCEPT
```
Также `/etc/network/if-pre-up.d/iptables-restore` → восстанавливает `/etc/iptables/rules.v4`.
Если SSH блокируется: `iptables -I INPUT 1 -s <IP> -j ACCEPT && iptables-save > /etc/iptables/rules.v4`

## Wordstat Setup (нужен токен!)
Сервис запущен: `http://localhost:9001/health` → ok
Для активации: `YANDEX_OAUTH_TOKEN=<токен>` в `/srv/openclaw/config/wordstat.env`
Получить: https://oauth.yandex.ru → создать приложение → scopes: wordstat

## Telegram Topics
| Topic | Назначение |
|-------|------------|
| 267 | Подтверждённые модели (APPROVED ≥70) |
| 270 | Отклонённые + Near-Pass (REJECTED / NEAR-PASS 65-69) |
| 8 | Дайджест + Health Dashboard |
| 76 | Обучение (feedback, команды) |

## Telegram Commands
| Команда | Что делает |
|---------|------------|
| `/relaunch <case-slug>` | Сбросить кейс для переработки |
| `/status` | Статус пайплайна |
| `/sectors` | Статистика по секторам |
| `/help` | Справка |

## Auto-Posting Architecture
1. **Program 7 (models-critic)**: после создания 06-verdict.md → отправляет в Telegram → создаёт `.telegram-sent`
2. **tg_notifier.py** (cron */10): failsafe — отправляет кейсы с 06-verdict.md без маркера

Маркер `.telegram-sent`: `sent=ВЕРДИКТ score=X/100 ts=ISO-DATE` — предотвращает дубли.

## LTV Upside Calculator
Для всех REJECTED/NEAR-PASS кейсов — в 06-verdict.md секция `## LTV Upside Calculator`:
| Критерий | Сейчас | Макс | Потенциал | Действие |
|----------|--------|------|-----------|---------|
| ... | X/20 | 20 | +Y | конкретное действие с цифрами |
Кратчайший путь до 70 + LTV цель в рублях + рычаг роста.
В Telegram NEAR-PASS сообщение: блок `📐 LTV Upside Calculator` с топ-2 критериями.

## Devil's Advocate (Near-Pass 65-69)
СООБЩЕНИЕ 3 в topic 270 для каждого Near-Pass кейса:
- 3 сценария провала за 6 месяцев (финансовый, конкурентный, операционный)
- Ранние сигналы для каждого сценария
- Итоговая рекомендация: /relaunch или отклонить окончательно

## All Cron Jobs (14 enabled, OpenClaw)
| Job | Schedule | Назначение |
|-----|----------|------------|
| radar-b2b-ops | 12,42 * * * * | AI-автоматизация |
| radar-ai-services | 17,47 * * * * | AI-услуги |
| radar-quick-ai | 22,52 * * * * | TG-боты, быстрые AI-продукты |
| radar-geo-expansion | 27,57 * * * * | Западные модели без аналога в РФ |
| models-intake-triage | 25,55 * * * * | Triage + Auto-enrich |
| chief-models-review | 58 * * * * | Ревью качества |
| models-demand-validation | 30 * * * * | Demand: Wordstat + HH.ru + Avito + TG + vc.ru |
| models-economics | 5 */2 * * * | Unit economics RUB |
| models-finance | 35 */2 * * * | P&L 3 scenarios |
| models-critic | 55 */2 * * * | Verdict + Near-Pass + Devil's Advocate + LTV Upside + Telegram |
| models-digest | 0 9 * * * | Digest + Health Dashboard |
| chief-supervisor | 0 */6 * * * | Self-learning |
| models-feedback-loop | 30 */6 * * * | Feedback → SEARCH_PREFERENCES |
| models-market-pulse | 0 10 * * 0 | Weekly trend check |

System crons (host):
- `*/5 * * * *` → command_processor.py
- `*/10 * * * *` → tg_notifier.py
- `0 5 * * *` → stale_detector.py

## Sectors
B2B-OPS | AI-SERVICES | QUICK-AI | HEALTHCARE | FINTECH | GEO-EXPAND

## Key Rules
- LTV Gate: > 500 000 руб/мес
- Score: ≥70 APPROVED, 65-69 NEAR-PASS, <65 REJECTED
- Язык: ТОЛЬКО РУССКИЙ | Валюта: РУБЛИ

## Pipeline State (2026-04-14 20:00 MSK)
### Active (9 кейсов)
| Кейс | Статус |
|------|--------|
| ai-songs-on-demand-service | 02-demand.md готов (REJECT на demand), идёт дальше |
| ai-native-salesforce-implementation-operator | 04-economics.md |
| ambient-clinical-documentation-operator | 05-critic.md |
| autonomous-medical-coding-operator | 04-economics.md |
| enterprise-agent-control-plane-implementation-operator | 02-demand.md |
| expert-human-data-ops-for-ai-models-operator | 00-brief.md |
| human-data-ai-trainers-operator | 02-demand.md |
| investment-banking-ai-analyst-operator | 02-demand.md |
| openclaw-contours-agency | 04-economics.md |

### Rejected (10 кейсов, 9 отправлены в TG topic 270)
| Кейс | Score | TG |
|------|-------|----|
| ai-customer-service-operations-operator | 54/100 | ✅ |
| ai-finance-supply-chain-operations-operator | 55/100 | ✅ |
| ai-manufacturing-quoting-operator | 62/100 | ✅ |
| ai-marketing-ops-microagency | 43/100 | ✅ |
| autonomous-b2c-crm-operator | 65/100 NEAR-PASS | ✅ |
| autonomous-enterprise-service-operations-operator | 58/100 | ✅ |
| draft-ai-support-local-clinics | manual reject | нет verdict |
| enterprise-agentic-marketing-implementation-operator | 58/100 | ✅ |
| enterprise-ai-process-automation-operator | 68/100 NEAR-PASS | ✅ |
| enterprise-contract-operations-agents | 54/100 | ✅ |

### Approved
(пока пусто)

## Backlog
### P1
- Активировать Wordstat OAuth токен
- Мониторинг ai-songs-on-demand-service до финального вердикта

### P2
- Конкурентный радар (мониторинг approved кейсов, weekly)
- radar-healthcare, radar-fintech
- Webhook topic 76 (сейчас polling)

### P3
- Pattern learning в chief-supervisor
- Дедупликация при intake (semantic similarity)
- Минимум 3 независимых источника для demand validation

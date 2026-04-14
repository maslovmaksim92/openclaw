# OpenClaw Multi-Agent Business Model Pipeline

## Original Problem Statement
Автоматический поиск, фильтрация и валидация бизнес-моделей 24/7. Telegram-боты в Supergroup. `core-chief` самообучается.

## VPS: `188.214.107.181`
- AGENTS.md: `/srv/openclaw/config/workspace-branch-models-lead/AGENTS.md` (875 строк)
- Jobs: `/srv/openclaw/config/cron/jobs.json` (16 jobs, 14 enabled)
- Wordstat Service: `/srv/openclaw/wordstat_service.py` → systemd → port 9001
- Command Processor: `/srv/openclaw/command_processor.py` → cron */5 * * * *
- Stale Detector: `/srv/openclaw/stale_detector.py` → cron 0 5 * * * (08:00 MSK)

## Wordstat Setup (нужен токен!)
Сервис запущен: `http://localhost:9001/health` → ok
Для активации реального Wordstat: добавить OAuth-токен в `/srv/openclaw/config/wordstat.env`
```
YANDEX_OAUTH_TOKEN=<ваш_токен>
```
Получить токен: https://oauth.yandex.ru → создать приложение → scopes: wordstat

## Telegram Commands (пишутся в любом топике группы)
| Команда | Что делает |
|---------|------------|
| `/relaunch <case-slug>` | Сбросить кейс для переработки (Near-Pass fix) |
| `/status` | Статус пайплайна (cases/approved/rejected) |
| `/sectors` | Статистика по секторам |
| `/help` | Справка |

## All Cron Jobs (14 enabled)
| Job | Schedule | Назначение |
|-----|----------|------------|
| radar-b2b-ops | 12,42 * * * * | AI-автоматизация, AI-агентства |
| radar-ai-services | 17,47 * * * * | AI-услуги на заказ |
| radar-quick-ai | 22,52 * * * * | TG-боты, 1 услуга = быстрый результат |
| radar-geo-expansion | 27,57 * * * * | Западные модели без аналога в РФ |
| models-intake-triage | 25,55 * * * * | Triage + Auto-enrich 01-evidence.md |
| chief-models-review | 58 * * * * | Ревью качества |
| models-demand-validation | 30 * * * * | Demand: Wordstat API + HH.ru + Avito + TG + vc.ru |
| models-economics | 5 */2 * * * | Unit economics RUB + ScoreTrajectory |
| models-finance | 35 */2 * * * | P&L 3 scenarios + Critic + ScoreTrajectory |
| models-critic | 55 */2 * * * | Verdict 0-100 + Near-Pass + Telegram |
| models-digest | 0 9 * * * | Digest + Health Dashboard |
| chief-supervisor | 0 */6 * * * | Self-learning + Sector Analytics |
| models-feedback-loop | 30 */6 * * * | User feedback → SEARCH_PREFERENCES |
| models-market-pulse | 0 10 * * 0 | Weekly Wordstat trend check |

System crons (outside OpenClaw):
- `*/5 * * * *` → command_processor.py (Telegram /relaunch, /status, /sectors)
- `0 5 * * *` → stale_detector.py (stale cases alert to topic 76)

## Sectors
B2B-OPS | AI-SERVICES | QUICK-AI | HEALTHCARE | FINTECH | GEO-EXPAND

## Key Rules
- LTV Gate: > 500 000 руб/мес
- Score: ≥70 APPROVED, 65-69 NEAR-PASS, <65 REJECTED
- Wordstat: via proxy localhost:9001 (requires OAuth token) + fallback multi-source
- Язык: ТОЛЬКО РУССКИЙ | Валюта: РУБЛИ

## Backlog
### P1
- Активировать Wordstat токен (пользователь должен получить OAuth)
- Devil's Advocate для Near-Pass (3 сценария провала)
- Stale case — поправить порог если нужно (сейчас 7 дней)
### P2
- Конкурентный радар (мониторинг approved конкурентов)
- Webhook topic 76 → FEEDBACK_LOG.md (сейчас polling)
- radar-healthcare, radar-fintech
### P3
- Pattern learning в chief-supervisor
- Дедупликация при intake (semantic similarity)

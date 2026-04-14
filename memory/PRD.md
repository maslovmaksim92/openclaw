# OpenClaw Multi-Agent Business Model Pipeline

## Original Problem Statement
Автоматический поиск, фильтрация и валидация бизнес-моделей 24/7. Telegram-боты в Supergroup. `core-chief` самообучается.

## VPS: `188.214.107.181`
- AGENTS.md: `/srv/openclaw/config/workspace-branch-models-lead/AGENTS.md` (957 строк)
- Jobs: `/srv/openclaw/config/cron/jobs.json` (18 jobs, 16 enabled)
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
Также: `/etc/network/if-pre-up.d/iptables-restore` → `/etc/iptables/rules.v4`
Экстренный whitelist: `iptables -I INPUT 1 -s <IP> -j ACCEPT && iptables-save > /etc/iptables/rules.v4`

## Wordstat (нужен токен!)
Сервис: `http://localhost:9001/health` → ok
Активация: `YANDEX_OAUTH_TOKEN=<токен>` в `/srv/openclaw/config/wordstat.env`
Получить: https://oauth.yandex.ru → создать приложение → scopes: wordstat

## Telegram Topics
| Topic | Назначение |
|-------|------------|
| 267 | Подтверждённые модели (APPROVED ≥70) |
| 270 | Отклонённые + Near-Pass |
| 8 | Дайджест + Health Dashboard |
| 76 | Обучение (feedback, команды) |

## Telegram Commands
`/relaunch <slug>` | `/status` | `/sectors` | `/help`

## Features реализованные
- **LTV Upside Calculator** (в 06-verdict.md + Telegram NEAR-PASS): таблица критериев, кратчайший путь до 70, LTV цель в рублях, рычаг роста
- **Devil's Advocate** (NEAR-PASS 65-69): 3 сценария провала за 6 мес + ранние сигналы + рекомендация /relaunch или отклонить
- **Auto-posting**: Program 7 → .telegram-sent маркер; tg_notifier.py каждые 10 мин (failsafe)
- **Стабильный SSH**: ufw before.rules + iptables-persistent

## All Radar Jobs (6 активных)
| Job | Schedule | Сектор |
|-----|----------|--------|
| radar-b2b-ops | 12,42 * * * * | AI-автоматизация B2B операций |
| radar-ai-services | 17,47 * * * * | AI-услуги на заказ |
| radar-quick-ai | 22,52 * * * * | TG-боты, быстрые AI-продукты |
| radar-geo-expansion | 27,57 * * * * | Западные модели без аналога в РФ |
| **radar-healthcare** | **7,37 * * * *** | **AI в медицине, клиниках, диагностике** |
| **radar-fintech** | **2,32 * * * *** | **AI в финансах, бухгалтерии, страховании** |

## All Pipeline Jobs (10 активных)
| Job | Schedule | Назначение |
|-----|----------|------------|
| models-intake-triage | 25,55 * * * * | Triage + Auto-enrich |
| chief-models-review | 58 * * * * | Ревью качества |
| models-demand-validation | 30 * * * * | Demand: мульти-сигнальный |
| models-economics | 5 */2 * * * | Unit economics RUB |
| models-finance | 35 */2 * * * | P&L 3 scenarios |
| models-critic | 55 */2 * * * | Verdict + Near-Pass + Devil's + LTV Upside + Telegram |
| models-digest | 0 9 * * * | Digest + Health Dashboard |
| chief-supervisor | 0 */6 * * * | Self-learning |
| models-feedback-loop | 30 */6 * * * | Feedback → SEARCH_PREFERENCES |
| models-market-pulse | 0 10 * * 0 | Weekly trend check |

System crons (host VPS):
- `*/5` → command_processor.py | `*/10` → tg_notifier.py | `0 5` → stale_detector.py

## Key Rules
- LTV Gate: > 500 000 руб/мес | Score: ≥70 APPROVED, 65-69 NEAR-PASS, <65 REJECTED
- Язык: ТОЛЬКО РУССКИЙ | Валюта: РУБЛИ

## Pipeline State (2026-04-14 20:30 MSK)
### Active (9 кейсов)
- ai-songs-on-demand-service → 02-demand.md (REJECT demand, идёт к economics)
- ai-native-salesforce-implementation-operator → 04-economics.md
- ambient-clinical-documentation-operator → 05-critic.md
- autonomous-medical-coding-operator → 04-economics.md
- enterprise-agent-control-plane-implementation-operator → 02-demand.md
- expert-human-data-ops-for-ai-models-operator → 00-brief.md
- human-data-ai-trainers-operator → 02-demand.md
- investment-banking-ai-analyst-operator → 02-demand.md
- openclaw-contours-agency → 04-economics.md

### Rejected (10 кейсов, 9 отправлены в TG topic 270)
ai-customer-service 54 ✅ | ai-finance-supply-chain 55 ✅ | ai-manufacturing-quoting 62 ✅
ai-marketing-ops 43 ✅ | autonomous-b2c-crm 65 NEAR-PASS ✅ | autonomous-enterprise-service 58 ✅
draft-ai-support-local-clinics (manual) | enterprise-agentic-marketing 58 ✅
enterprise-ai-process-automation 68 NEAR-PASS ✅ | enterprise-contract-operations 54 ✅

## Backlog
### P1
- Активировать Wordstat OAuth токен

### P2
- Конкурентный радар для approved кейсов (weekly мониторинг)
- Webhook topic 76 (сейчас polling, конфликт)

### P3
- Pattern learning в chief-supervisor
- Дедупликация при intake (semantic similarity)
- Минимум 3 независимых источника для demand validation
- LTV Upside Leaderboard в дайджест (топ-3 NEAR-PASS ближайших к 70)

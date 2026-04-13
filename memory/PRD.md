# OpenClaw Multi-Agent Business Model Pipeline

## Original Problem Statement
Настройка OpenClaw для автоматического поиска, фильтрации и валидации бизнес-моделей 24/7.
Telegram-боты в Supergroup с Topics. `core-chief` самообучается.

## Architecture

### VPS: `188.214.107.181`
- Jobs: `/srv/openclaw/config/cron/jobs.json`
- AGENTS.md: `/srv/openclaw/config/workspace-branch-models-lead/AGENTS.md` (867 строк, 11 программ)
- State: `/srv/openclaw/config/workspace-branch-models-lead/state/`

### Pipeline Flow
Radar (4 потока) → Triage (Auto-enrich) → Demand (Multi-source) → Economics → Finance+Critic → Verdict → Telegram → Digest+Health+Market Pulse

### Telegram Topics
| Топик | threadId | Кто пишет |
|-------|----------|-----------|
| Подтверждение | 267 | models-critic (≥70) + alert в topic 8 |
| Отклонённые/Near-Pass | 270 | models-critic (<70, особый формат 65-69) |
| Дайджест+Dashboard+Pulse | 8 | models-digest (09:00) + market-pulse (вс 10:00) |
| Обучение | 76 | core-chief + feedback-loop |

### Bot
- `@vd_programist_bot` = `7993830496:AAFDoTzBbWUCybkvKM-hRm1iay45CBRpXU8` (admin, pin rights)
- Chat ID: `-1003900243133`

## All Enabled Cron Jobs (14 jobs)
| Job | Schedule | Назначение |
|-----|----------|------------|
| radar-b2b-ops | 12,42 * * * * | AI-автоматизация операций, AI-агентства |
| radar-ai-services | 17,47 * * * * | Услуги на заказ автоматизированные AI |
| radar-quick-ai | 22,52 * * * * | TG-боты, 1 услуга = быстрый результат |
| radar-geo-expansion | 27,57 * * * * | Западные модели без аналога в России |
| models-intake-triage | 25,55 * * * * | Triage + Автообогащение 01-evidence.md |
| chief-models-review | 58 * * * * | Ревью качества кейсов |
| models-demand-validation | 30 * * * * | Спрос (multi-source, no Wordstat) |
| models-economics | 5 */2 * * * | Юнит-экономика в рублях + ScoreTrajectory |
| models-finance | 35 */2 * * * | Финмодель + Критика + ScoreTrajectory |
| models-critic | 55 */2 * * * | Вердикт 0-100, Near-Pass, Telegram |
| models-digest | 0 9 * * * | Дайджест + Health Dashboard |
| chief-supervisor | 0 */6 * * * | Self-learning + Sector Analytics |
| models-feedback-loop | 30 */6 * * * | Обратная связь пользователя |
| models-market-pulse | 0 10 * * 0 | Тренды спроса по всем кейсам (вс) |

Disabled: models-radar-search (заменён 4 нишевыми), models-case-validation

## Sectors
| Код | Название | Примеры |
|-----|----------|---------|
| B2B-OPS | AI-операции и агентства | AI CS operator, AI sales ops, AI process automation |
| AI-SERVICES | AI-услуги на заказ | AI сайты, AI SEO, AI контент, AI дизайн |
| QUICK-AI | Быстрые AI-сервисы | AI песни, AI фото, TG боты, AI поздравления |
| HEALTHCARE | AI в медицине | AI клиника, AI диагностика |
| FINTECH | AI в финансах | AI бухгалтерия, AI платежи |
| GEO-EXPAND | Западная модель → РФ | US/EU сервис без российского аналога |

## Key System Rules
- **LTV Gate**: > 500 000 руб/мес на всех этапах
- **Scoring**: 70+ = APPROVED, 65-69 = NEAR-PASS (особый формат), <65 = REJECTED
- **Wordstat ЗАМЕНЁН** многоисточниковым подходом: Google Trends + HH.ru + Avito + Telegram/tgstat + vc.ru/Habr
- **Язык**: ТОЛЬКО РУССКИЙ во всех файлах и Telegram
- **Валюта**: РУБЛИ

## Case Files Map
```
pipeline/cases/<slug>/
  00-brief.md          — сигнал, гипотеза, сектор
  01-evidence.md       — доказательная база (автообогащение)
  02-demand.md         — multi-source demand + сектор + geo-flag
  03-offer.md          — оффер
  04-economics.md      — CAC/LTV/GM/break-even в рублях
  05-critic.md         — P&L 3 сценария + критический анализ
  06-verdict.md        — score 0-100 + сектор + вердикт
  07-score-trajectory.md — промежуточные score по этапам
```

## State Files
```
state/
  SEARCH_PREFERENCES.md — текущие параметры поиска
  FEEDBACK_LOG.md       — обратная связь пользователя
  SECTOR_STATS.md       — статистика по секторам (обновляет chief-supervisor)
```

## Active Cases
| Кейс | Сектор | Этап |
|------|--------|------|
| ai-songs-on-demand-service | QUICK-AI | demand validation |
| openclaw-contours-agency | B2B-OPS | verdict pending (00:55) |
| enterprise-agentic-marketing-* | B2B-OPS | demand |
| 6 других кейсов | B2B-OPS | demand validation |

## Implemented (all sessions)
- 2026-04-13 S1: Строгая критичность, LTV Gate, порог 70/100
- 2026-04-13 S2: LTV 500k, Feedback Loop, Pinned messages, Alerts
- 2026-04-14 S3: Near-Pass, Автообогащение, Market Pulse, Health Dashboard, Score Trajectory
- 2026-04-14 S4: Sector Mapping, Geographic Expansion Radar, 4 нишевых радара (B2B-OPS/AI-SERVICES/QUICK-AI/GEO-EXPAND), замена Wordstat на multi-source, кейс ai-songs-on-demand-service

## Backlog
### P1
- /relaunch команда (TG → сброс Near-Pass кейса на переработку)
- Stale case detection (кейс завис >7 дней → alert)
### P2
- Конкурентный радар (мониторинг цен конкурентов approved кейсов)
- Webhook topic 76 → FEEDBACK_LOG.md
- Дедупликация при intake (semantic similarity check)
- Devil's Advocate для Near-Pass (стресс-тест провала)
### P3
- radar-healthcare, radar-fintech (отдельные нишевые потоки)
- Pattern learning: chief-supervisor выявляет что общего у approved кейсов
- Score trajectory визуализация (mini chart в Telegram)

## Notes
- GitHub auto-deploy — ОТМЕНЕНО
- SSH timeout → `iptables -I INPUT -s <IP> -j ACCEPT`
- Backups: `/srv/openclaw/config/workspace-branch-models-lead/AGENTS.md.bak.*`

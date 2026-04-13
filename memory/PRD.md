# OpenClaw Multi-Agent Business Model Pipeline

## Original Problem Statement
Настройка OpenClaw для конкретных задач и построение мультиагентной системы для автоматического поиска, фильтрации и валидации бизнес-моделей 24/7. Telegram-боты в Supergroup с Topics. Пайплайн для `branch-models-lead`. `core-chief` самообучается.

## Architecture

### VPS
- IP: `188.214.107.181`
- Docker Compose: `/opt/openclaw/docker-compose.yml`
- Jobs: `/srv/openclaw/config/cron/jobs.json`
- AGENTS.md: `/srv/openclaw/config/workspace-branch-models-lead/AGENTS.md` (796 строк, 11 программ)
- Симлинк: `/srv/openclaw/agents/branch-models-lead/workspace/` → `/srv/openclaw/config/workspace-branch-models-lead/`

### Pipeline Flow
Radar → Triage (+ Auto-enrich) → Demand (+ScoreTrajectory) → Economics (+ScoreTrajectory) → Finance+Critic (+ScoreTrajectory) → Verdict (Near-Pass/Approved/Rejected) → Telegram → Digest (+ Health Dashboard) + Market Pulse (weekly)

### Telegram Topics
| Топик | threadId | Кто пишет |
|-------|----------|-----------|
| Подтверждение модели | 267 | models-critic (score ≥ 70) — 3 сообщения |
| Отклонённые / Near-Pass | 270 | models-critic — 2 сообщения (особый формат для 65-69) |
| Дайджест + Health Dashboard | 8 | models-digest (09:00) + Market Pulse (вс 10:00) + alerts |
| Обучение | 76 | core-chief / models-feedback-loop |

### Bot Tokens
- `@vd_programist_bot` = models bot: `7993830496:AAFDoTzBbWUCybkvKM-hRm1iay45CBRpXU8` (admin, can pin)
- Chat ID: `-1003900243133`

## All Enabled Cron Jobs (11 jobs)
| Job | Schedule | Назначение |
|-----|----------|------------|
| models-radar-search | 10,40 * * * * | Поиск сигналов с LTV Gate |
| models-intake-triage | 25,55 * * * * | Тriage + Автообогащение 01-evidence.md |
| chief-models-review | 58 * * * * | Ревью качества |
| models-demand-validation | 30 * * * * | Спрос (Wordstat/Avito/HH.ru) + ScoreTrajectory |
| models-economics | 5 */2 * * * | Юнит-экономика в рублях + ScoreTrajectory |
| models-finance | 35 */2 * * * | Финмодель + Критика + ScoreTrajectory |
| models-critic | 55 */2 * * * | Вердикт 0-100, Near-Pass, Telegram |
| models-digest | 0 9 * * * | Дайджест + Health Dashboard |
| chief-supervisor | 0 */6 * * * | Самообучение + CHANGELOG |
| models-feedback-loop | 30 */6 * * * | Обратная связь пользователя |
| models-market-pulse | 0 10 * * 0 | Тренды Wordstat (воскресенье 10:00 МСК) |

## Key System Rules

### LTV Gate
- Минимум: LTV > 500 000 руб/мес
- Применяется: Radar, Triage, Demand, Economics, Critic

### Scoring (0-100)
- Спрос Wordstat/Avito/HH.ru: 20 pts | Экономика RUB: 25 pts | Масштаб: 20 pts
- Конкуренция: 15 pts | Защита: 10 pts | Данные: 10 pts

### Verdict Thresholds
- ≥ 70 → APPROVED → pipeline/approved/ → topic 267 (3 msg)
- 65-69 → NEAR-PASS → pipeline/rejected/ → topic 270 (особый формат: что улучшить)
- < 65 → REJECTED → pipeline/rejected/ → topic 270 (стандарт)

### Язык
- ВСЕ файлы, отчёты, Telegram — ТОЛЬКО НА РУССКОМ ЯЗЫКЕ

### Валюта
- Все расчёты в РУБЛЯХ

## Implemented

### Сессия 1 (2026-04-13): Базовая строгая критичность
- AGENTS.md переписан с программами 4-8
- LTV Gate, порог 70/100, запрет шаблонов

### Сессия 2 (2026-04-13): LTV 500k, Feedback Loop, закрепление
- LTV Gate 500k руб/мес во всех этапах
- Program 9 (Feedback Loop), SEARCH_PREFERENCES.md
- Pinned messages в topиках 267, 270, 8
- Alerts в topic 8 при approved

### Сессия 3 (2026-04-14): 5 новых функций
- **Near-Pass** (65-69/100): особый формат в topic 270 с конкретными рекомендациями что улучшить
- **Автообогащение** (Program 1): supporting signal → автодобавление в 01-evidence.md открытого кейса
- **Market Pulse** (Program 10, cron воскресенье 10:00): Wordstat-тренды по всем кейсам → topic 8
- **Health Dashboard** (Program 8): ежедневная статистика пайплайна в topic 8 (in-progress/approved/rejected/near-pass/top-rejection-reason)
- **Score Trajectory** (07-score-trajectory.md): каждый этап записывает свой промежуточный score в кейс

## Case Files Map
```
pipeline/cases/<slug>/
  00-brief.md          — сигнал и гипотеза
  01-evidence.md       — доказательная база (автообогащается)
  02-demand.md         — спрос Wordstat/Avito/HH.ru
  03-offer.md          — оффер
  04-economics.md      — CAC/LTV/GM/break-even в рублях
  05-critic.md         — финмодель P&L + критический анализ
  06-verdict.md        — финальный вердикт 0-100
  07-score-trajectory.md — история score по этапам
```

## Backlog

### P1
- Проверить openclaw-contours-agency вердикт (runs at 00:55 MSK)
- Убедиться что Near-Pass формат корректно отображается в Telegram

### P2
- Конкурентный радар (мониторинг цен конкурентов для approved кейсов)
- Webhook для автоматического чтения topic 76 в FEEDBACK_LOG.md
- Portfolio view (monthly report by category)

## Notes
- GitHub auto-deploy/VPS connection — ОТМЕНЕНО
- SSH timeout → `iptables -I INPUT -s <IP> -j ACCEPT`
- Все backup AGENTS.md: `/srv/openclaw/config/workspace-branch-models-lead/AGENTS.md.bak.*`

# OpenClaw Multi-Agent Business Model Pipeline

## Original Problem Statement
Настройка OpenClaw для конкретных задач и построение мультиагентной системы для автоматического поиска, фильтрации и валидации бизнес-моделей 24/7. Интеграция Telegram-ботов в Telegram Supergroup с Topics. Пайплайн для `branch-models-lead`. `core-chief` самообучается по логам.

## Architecture

### VPS
- IP: `188.214.107.181`
- Docker Compose: `/opt/openclaw/docker-compose.yml`
- Jobs (Cron): `/srv/openclaw/config/cron/jobs.json`
- Agent workspace (симлинк): `/srv/openclaw/agents/branch-models-lead/workspace/` → `/srv/openclaw/config/workspace-branch-models-lead/`

### Pipeline Flow
Radar → Triage → Demand → Economics → Finance+Critic → Verdict → Telegram → Digest

### Telegram Topics
| Топик | threadId | Кто пишет |
|-------|----------|-----------|
| Подтверждение модели | 267 | models-critic (score ≥ 70) — 3 сообщения |
| Отклонённые модели | 270 | models-critic (score < 70) — 2 сообщения |
| Дайджест | 8 | models-digest (09:00 МСК) + alert для approved |
| Обучение | 76 | core-chief / models-feedback-loop |

### Bot Tokens
- `@vd_programist_bot` = models bot: `7993830496:AAFDoTzBbWUCybkvKM-hRm1iay45CBRpXU8`
- Chat ID: `-1003900243133`

## All Enabled Cron Jobs (10 jobs)
| Job | Agent | Schedule | Назначение |
|-----|-------|----------|------------|
| models-radar-search | branch-models-lead | 10,40 * * * * | Поиск сигналов (LTV Gate) |
| models-intake-triage | branch-models-lead | 25,55 * * * * | Обработка raw сигналов |
| chief-models-review | core-chief | 58 * * * * | Ревью качества кейсов |
| models-demand-validation | branch-models-lead | 30 * * * * | Валидация спроса (Wordstat/Avito) |
| models-economics | branch-models-lead | 5 */2 * * * | Юнит-экономика в рублях |
| models-finance | branch-models-lead | 35 */2 * * * | Финмодель + критический анализ |
| models-critic | branch-models-lead | 55 */2 * * * | Вердикт 0-100 + Telegram |
| models-digest | branch-models-lead | 0 9 * * * | Ежедневный дайджест |
| chief-supervisor | core-chief | 0 */6 * * * | Самообучение + CHANGELOG |
| models-feedback-loop | branch-models-lead | 30 */6 * * * | Обратная связь пользователя |

## Key System Rules

### LTV Gate
- Минимум: LTV > 500 000 руб/мес (6 000 000 руб/год)
- Применяется на всех этапах: Radar, Demand, Economics, Critic
- LTV < 500k руб/мес → автоматический REJECT

### Scoring (0-100, порог 70)
- Спрос с Wordstat/Avito/HH.ru: 20 pts
- Юнит-экономика в рублях (CAC/LTV/GM): 25 pts
- Масштабируемость: 20 pts
- Конкурентное позиционирование: 15 pts
- Барьеры входа: 10 pts
- Качество данных: 10 pts

### Валюта
- Все расчёты в РУБЛЯХ. USD → конвертировать (~90 руб/$)

### Telegram формат
- Approved: 3 сообщения (заголовок + экономика+рынок + финмодель+обоснование) + alert в topic 8
- Rejected: 2 сообщения (причина + данные+проблемы)

## Implemented (2026-04-13 сессия 2)

### Строгие правила (сессия 1)
- AGENTS.md переписан с программами 4-8 + строгая критичность
- jobs.json обновлён (5 задач)
- Отправлены rejected кейсы в topic 270
- Очищены шаблонные файлы

### Масштабные улучшения (сессия 2, эта)
- LTV Gate > 500k руб/мес добавлен во все этапы (Radar, Demand, Economics, Critic)
- Валюта: переход на рубли как основную валюту
- Program 9 (Feedback Loop): новый cron job `models-feedback-loop` (каждые 6ч)
- state/SEARCH_PREFERENCES.md и state/FEEDBACK_LOG.md созданы
- core-chief AGENTS.md обновлён: читает FEEDBACK_LOG, обновляет SEARCH_PREFERENCES
- chief-supervisor обновлён: публикует статистику pipeline + user preferences в topic 76
- Alert для approved: brief уведомление в topic 8 при каждом одобрении
- Сообщения закреплены (pinned) в топиках 267, 270, 8 через @vd_programist_bot
- Telegram topics explain messages: 267 (правила одобрения), 270 (правила отклонения), 8 (дайджест info)
- Добавлен призыв к обратной связи (👍/👎) в каждое сообщение пайплайна

## Current Pipeline State (2026-04-13)
| Кейс | Файлы | Следующий шаг |
|------|-------|---------------|
| openclaw-contours-agency | до 05-critic.md | models-critic (20:55 МСК) |
| ai-marketing-ops-microagency | до 05-critic.md | models-critic (20:55 МСК) |
| ai-customer-service-operations-operator | до 04-economics.md | models-finance |
| 5 других кейсов | только 00-brief.md | models-demand-validation |

## Backlog
### P1
- Дождаться первого прогона models-critic (20:55 МСК) и проверить качество Telegram-сообщений
- Добавить Wordstat-данные в уже существующие 02-demand.md файлы (ai-customer-service, openclaw-contours, ai-marketing)

### P2
- Механизм прямого чтения Telegram thread 76 (через webhook или polling) для FEEDBACK_LOG.md

## Notes
- GitHub auto-deploy/VPS connection — ОТМЕНЕНО пользователем
- SSH timeout → добавить IP в iptables: `iptables -I INPUT -s <IP> -j ACCEPT`

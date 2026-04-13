# OpenClaw Multi-Agent Business Model Pipeline

## Original Problem Statement
Настройка OpenClaw для конкретных задач и построение мультиагентной системы для автоматического поиска, фильтрации и валидации бизнес-моделей 24/7. Интеграция Telegram-ботов в Telegram Supergroup с Topics для мониторинга. Построение пайплайна для `branch-models-lead`. Оркестратор (`core-chief`) должен самообучаться по логам/ошибкам.

## Architecture

### VPS
- IP: `188.214.107.181`
- Docker Compose: `/opt/openclaw/docker-compose.yml`
- Config: `/srv/openclaw/config/openclaw.json`
- Jobs (Cron): `/srv/openclaw/config/cron/jobs.json`
- Agent workspace: `/srv/openclaw/config/workspace-branch-models-lead/` (симлинк: `/srv/openclaw/agents/branch-models-lead/workspace/`)

### Pipeline flow
Radar → Triage → Demand → Economics → Finance+Critic → Verdict → Telegram → Digest

### Telegram Topics
| Топик | threadId | Кто пишет |
|-------|----------|-----------|
| Подтверждение модели | 267 | models-critic (score ≥ 70) |
| Отклонённые модели | 270 | models-critic (score < 70) |
| Дайджест | 8 | models-digest (09:00 ежедневно) |
| Обучение | 76 | core-chief (chief-supervisor) |

### Bot Tokens
- `models` bot: `7993830496:AAFDoTzBbWUCybkvKM-hRm1iay45CBRpXU8` (пишет в 267, 270)
- `chief` bot: `8221350239:AAFaAcO_u3WUGqlgrosaiz7ps6jnh1A6eWo` (пишет в 76)
- Chat ID: `-1003900243133`

## Implemented

### 2026-04-13: Строгая критичность (strict criticality)
- Обновлён AGENTS.md (577 строк): добавлены "СТРОГИЕ ПРАВИЛА КРИТИЧНОСТИ"
  - Запрет шаблонного содержимого
  - Порог: оценка ≥ 70 → APPROVED, < 70 → REJECTED (нет on-hold)
  - Экономика без реальных CAC/LTV → автоматическое REJECT
  - Формат полного Telegram-сообщения (3 msg для approved, 2 для rejected)
  - Структура 02-demand.md обязана содержать реальные цифры Wordstat/Avito/HH.ru
  - Структура 04-economics.md обязана содержать таблицу бизнес-процесса + формулы
- Обновлён jobs.json: все 5 cron-задач обновлены с явными правилами отклонения
- Отправлены в Telegram topic 270 (Отклонённые):
  - ai-finance-supply-chain-operations-operator (msg 293-294)
  - autonomous-enterprise-service-operations-operator (msg 295-296)
- Очищены шаблонные файлы из 5 активных кейсов (оставлен только 00-brief.md)
- Удалены устаревшие 06-verdict.md из openclaw-contours-agency и ai-marketing-ops-microagency

### Ранее выполнено
- Пайплайн end-to-end работает
- Self-learning core-chief запущен
- Telegram Thread IDs замаплены (Digest:8, Training:76, Approve:267, Reject:270)
- Docker DNS исправлен
- iptables: whitelisted Google Cloud ranges (34.0.0.0/8, 104.0.0.0/8)

## Current Pipeline State (2026-04-13)

### pipeline/cases/ (active)
| Кейс | Статус | Следующий шаг |
|------|--------|---------------|
| openclaw-contours-agency | 05-critic.md готов | models-critic (~20:55 МСК) |
| ai-marketing-ops-microagency | 05-critic.md готов | models-critic (~20:55 МСК) |
| ai-customer-service-operations-operator | 04-economics.md готов | models-finance |
| 5 остальных кейсов | только 00-brief.md | models-demand-validation |

### pipeline/rejected/
- ai-finance-supply-chain-operations-operator ✅ отправлен в TG
- autonomous-enterprise-service-operations-operator ✅ отправлен в TG

### pipeline/approved/
- (пусто — первые кейсы появятся после оценки models-critic)

## Prioritized Backlog

### P0 (критично)
- Дождаться первого прогона models-critic и проверить что полное сообщение отправлено в TG (20:55 МСК)

### P1
- Уточнить параметры Radar: искать только модели с LTV > 500k RUB/год
- Добавить обязательные Wordstat-числа в существующие 02-demand.md файлы

### P2
- Feedback loop из Telegram: core-chief корректирует критерии поиска на основе реакций пользователя
- Возможность закрепить объяснительные сообщения в топиках (нужны права "Pin Messages" для @vd_programist_bot)

## Notes
- GitHub auto-deploy/VPS connection — ОТМЕНЕНО пользователем
- Если SSH timeout — добавить IP в iptables через консоль провайдера

# OpenClaw Multi-Agent Business Model Pipeline

## Original Problem Statement
Автоматический поиск, фильтрация и валидация бизнес-моделей 24/7. Telegram-боты в Supergroup. `core-chief` самообучается.

## VPS: `188.214.107.181`
- AGENTS.md: `/srv/openclaw/config/workspace-branch-models-lead/AGENTS.md` (984 строк)
- Jobs: `/srv/openclaw/config/cron/jobs.json` (18 jobs, 16 enabled)
- Wordstat Service v3: `/srv/openclaw/wordstat_service.py` → systemd → port 9001
- Command Processor: `/srv/openclaw/command_processor.py` → cron */5 * * * *
- Stale Detector: `/srv/openclaw/stale_detector.py` → cron 0 5 * * *
- TG Notifier: `/srv/openclaw/tg_notifier.py` → cron */10 * * * *

## SSH Whitelist (постоянный)
В `/etc/ufw/before.rules`: `-A ufw-before-input -s 34.0.0.0/8 -j ACCEPT` + 35/104
Также: `/etc/network/if-pre-up.d/iptables-restore` → `/etc/iptables/rules.v4`

## Wordstat Service v3 (без токена!)
**Источники без авторизации:**
| Источник | Метод | Статус |
|----------|-------|--------|
| Google Trends RU | pytrends (0-100) | ✅ работает |
| Yandex Suggest | публичный API | ✅ работает |
| HH.ru API | официальный API | ✅ работает |
| Avito | scraping | ⚠️ иногда блокируется |
| Habr | scraping | ✅ работает |

**Endpoint `/multi-demand`**: сводный анализ без токена. Принимает `tg_subs=N` — агент передаёт подписчиков Telegram-бота/канала найденного вручную.
**OAuth токен** (опциональный): добавить в `/srv/openclaw/config/wordstat.env` для официального Wordstat.

## Улучшения агентов (апрель 2026)

### Program 0 (Radar)
- Обязательная проверка Telegram-ботов: `@keyword_bot`, `@keywordaibot`
- Запрос `http://172.17.0.1:9001/telegram-search?keyword=...`
- Добавление `existing_products_ru` в raw-файл

### Program 4 (Demand Validation) — полностью переписан
- Запрещено давать LOW без 4+ источников
- Обязательный первый шаг: поиск Telegram-ботов/каналов по теме
- Использует `/multi-demand?keyword=X&tg_subs=N` (Google Trends + HH + Avito + Habr)
- MEDIUM минимум если: действующий конкурент в РФ с 1k+ пользователей
- LTV gate: проверяет ВСЕ сценарии (B2C + B2B + White-label + Hybrid)

### Program 7 (Critic) — детальный scoring
- Спрос: 0-20 с бонусом +2 за product-market fit (действующий продукт в РФ 10k+)
- Экономика: 0-25 с детальными порогами по LTV/GM/CAC
- Масштабируемость: 0-20 с бонусом +2 за автоматическую доставку (бот/API)
- Полные шкалы для всех 6 критериев

## Features
- **LTV Upside Calculator**: в 06-verdict.md + Telegram NEAR-PASS
- **Devil's Advocate**: 3 сценария провала (Near-Pass 65-69)
- **Auto-posting**: Program 7 → `.telegram-sent` → topic 270/267

## Telegram Topics
| Topic | Назначение |
|-------|------------|
| 267 | Подтверждённые (APPROVED ≥70) |
| 270 | Отклонённые + Near-Pass |
| 8 | Дайджест + Health |
| 76 | Обучение |

## Radar Jobs (6)
radar-b2b-ops | radar-ai-services | radar-quick-ai | radar-geo-expansion | radar-healthcare | radar-fintech

## Pipeline State (2026-04-14 21:30 MSK)
### Active cases/: 20 кейсов
Все сброшены на demand validation с улучшенными агентами:
- ai-customer-service-operations-operator
- ai-finance-supply-chain-operations-operator
- ai-manufacturing-quoting-operator
- ai-marketing-ops-microagency
- ai-native-salesforce-implementation-operator
- **ai-songs-on-demand-service** (был REJECTED, пересматривается с @bro_hit_bot 177k)
- ambient-clinical-documentation-operator
- autonomous-b2c-crm-operator
- autonomous-enterprise-service-operations-operator
- autonomous-medical-coding-operator
- autonomous-sre-incident-response-operator
- draft-ai-support-local-clinics
- enterprise-agent-control-plane-implementation-operator
- enterprise-agentic-marketing-implementation-operator
- enterprise-ai-process-automation-operator
- enterprise-contract-operations-agents
- human-data-ai-trainers-operator
- investment-banking-ai-analyst-operator
- openclaw-contours-agency

### Rejected/: пусто (все перемещены в cases/ для пересмотра)
### Approved/: пусто

**Ожидаемое время:** demand validation 1 per :30 → 20 cases / 2 per hour = ~10 hours
После demand → economics (5 */2) → finance (35 */2) → critic (55 */2): ~3-5 дней полный цикл

## Key Rules
- LTV Gate: > 500 000 руб/мес | Score: ≥70 APPROVED, 65-69 NEAR-PASS, <65 REJECTED
- Язык: ТОЛЬКО РУССКИЙ | Валюта: РУБЛИ

## Backlog
### P1
- Секторальная оценка: отдельные scoring-веса для QUICK-AI vs B2B-OPS
- Реальные цены конкурентов (3 источника, не галлюцинации — Program 4)
- Следить за топиками 267/270 — кейсы начнут прилетать по мере прохождения пайплайна

### P2
- Минимум 3 независимых источника для demand validation (избежать vendor bias)
- Конкурентный радар для approved кейсов (weekly мониторинг)
- Активировать Wordstat OAuth токен (oauth.yandex.ru → wordstat.env)

### P3
- LTV Upside Leaderboard в дайджест (топ-3 NEAR-PASS ближайших к 70)
- Pattern learning в chief-supervisor
- Feedback loop: трекинг запущенных кейсов 30/60/90 дней

## Changelog
### 2026-04 (последние изменения)
- ✅ Anti-duplication (Program 1): DEDUP CHECK с 5 правилами (2 из 3 критериев = дубль)
- ✅ Улучшен формат REJECTED: 3 сообщения (бизнес-процесс + команда + стек + экономика + LTV Upside)
- ✅ Улучшен формат APPROVED: добавлена 👥 Команда в СООБЩЕНИЕ 2
- ✅ Улучшен формат NEAR-PASS: добавлены бизнес-процесс + команда в СООБЩЕНИЕ 2
- ✅ AGENTS.md: 984 → ~1020 строк, docker compose restarted

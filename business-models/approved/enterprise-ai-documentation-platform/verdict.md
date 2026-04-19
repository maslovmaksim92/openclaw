# enterprise-ai-documentation-platform
**Статус:** APPROVED
**Итоговый балл:** 72/100
**Дата:** 2026-04-19
**Сектор:** GEO-EXPAND

---

## Этап 1 — Описание кейса
# 00-brief

## Кейс
enterprise-ai-documentation-platform

## Статус
active

## Краткое описание
AI-native платформа для создания, поддержки и оптимизации продуктовой, developer и API-документации для B2B-команд: разработка, DevRel, product, support и solution engineering.

## Текущее состояние
На входе появился GEO-EXPAND сигнал по Mintlify. По данным входного файла, в начале 2026 года компания вышла на 8-значную годовую выручку, используется 20 000+ компаниями и обслуживает 100+ млн пользователей в год. Продукт закрывает понятную и регулярную боль: документация быстро устаревает, поиск по ней неудобен, а нагрузка на команды разработки, поддержки и product marketing растёт.

Сигнал проходит порог Program 1 по экономике. Во входном файле указан ориентир `≈ 180 000–900 000 RUB MRR` на команду документации, а потенциальный LTV в РФ оценивается в `≈ 650 000–3 000 000 RUB` на клиента при удержании 36 месяцев. Верхняя часть диапазона превышает рабочий порог `> 500 000 ₽/мес.` и допускает service-led или implementation-led модель с допродажей интеграций, миграции контента, кастомного поиска, private deployment и сопровождения.

Дополнительно важно, что во входном сигнале российский эквивалент отмечен как `none`. Это означает не просто локальный дефицит хороших AI-возможностей в docs/CMS, а вероятное отсутствие упакованного AI-first решения уровня Mintlify для русскоязычного B2B-рынка. Окно для входа может лежать на стыке SaaS, внедрения и managed service.

## Ключевая гипотеза
Можно собрать high-LTV бизнес вокруг AI-native документационной платформы для B2B-команд в РФ, если подтвердится:
- что компании готовы платить не только за хостинг документации, но и за ускорение обновлений, AI-поиск, генерацию черновиков, поддержку accuracy и снижение нагрузки на support и DevRel;
- что интеграции с GitLab, Jira, Confluence, helpdesk, SSO, внутренними knowledge base и русскоязычными workflow создают заметный внедренческий барьер;
- что buyer есть не только у developer tools компаний, но и у fintech, enterprise SaaS, интеграторов, платформенных команд и крупных внутренних IT-организаций;
- что recurring revenue можно строить на сопровождении документации, governance, quality control, AI-ассистентах по docs и enterprise-развёртывании;
- что на российском рынке нет зрелого прямого аналога уровня Mintlify, поэтому нишу можно занять через локализацию, интеграцию и сервисный слой.

---

## Этап 2 — Проверка спроса
# 02-demand

## Кейс
enterprise-ai-documentation-platform

## Дата проверки
2026-04-19, Europe/Moscow

## Сектор
B2B SaaS / Developer Tools / Knowledge Ops

## Итог
**DEMAND = MEDIUM+ / HIGH-, LTV Gate = PASS.**

Причина: в категории уже есть несколько реальных платных игроков с публичными ценами, buyer pain подтверждается наймом technical writers и инвестициями компаний в knowledge base / AI-assistant слой, а в РФ есть локальные сервисы и Telegram-first инструменты вокруг баз знаний и customer support. До чистого HIGH кейс не дотягивает потому, что обязательный local demand endpoint в этом прогоне не ответил, а прямой RU search-intent по категории слабее, чем по болям бухгалтерии, продаж или контакт-центров.

Ключевые факты:
- HH.ru по запросу `технический писатель` в Москве показывает **247 вакансий**.
- Вилки senior / lead technical writer доходят до **130 000–200 000 ₽/мес**.
- По данным Минцифры, в РФ **18 000+** аккредитованных IT-компаний.
- Есть 4 реальных платных международных якоря: Mintlify, ReadMe, GitBook, Document360.
- WTP подтверждён отдельно по platform fee и AI add-ons.

TAM / SAM / SOM:
- **TAM: 6,48 млрд ₽/год**
- **SAM: 4,05 млрд ₽/год**
- **SOM: 162 млн ₽/год**

LTV Gate:
- self-serve SaaS: условный PASS только как нижний слой;
- AI add-on: PASS;
- migration / implementation: PASS;
- managed documentation ops: PASS;
- enterprise / private deployment: PASS.

Итог спроса: **спрос подтверждён, early reject не нужен**.

---

## Этап 3 — Юнит-экономика
# 04-economics

## Кейс
enterprise-ai-documentation-platform

## Дата расчёта
2026-04-19 (Europe/Moscow)

## Итог по этапу
**PASS**

Причина: если продавать не как дешёвый docs-hosting, а как **enterprise AI documentation platform + migration + managed documentation ops**, экономика проходит fund-level пороги.

Ключевые метрики:
- Средняя выручка на клиента: **280 000 ₽/мес**
- COGS на клиента: **86 000 ₽/мес**
- Contribution profit: **194 000 ₽/мес**
- CAC: **640 000 ₽**
- LTV: **10 777 778 ₽**
- LTV/CAC: **16,8x**
- CAC Payback: **3,30 месяца**
- Contribution Margin: **69,3%**
- Fixed costs: **2 720 000 ₽/мес**
- Break-even: **15 клиентов / 8-9 месяц**

Детальный бизнес-процесс:
| Шаг | Что происходит | ROLE | TOOL | TIME | COST, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Сбор ICP-аккаунтов и enrichment по стеку docs / support / devrel | SDR / Growth | CRM, LinkedIn, Rusprofile, spreadsheets | 6 ч | 18 000 | Средняя |
| 2 | Персонализированный outbound, e-mail и Telegram outreach | SDR | Sequencer, e-mail, Telegram, CRM | 10 ч | 28 000 | Средняя |
| 3 | Qualification call | AE / Founder | CRM, discovery script, Meet | 4 ч | 24 000 | Низкая |
| 4 | Глубокий discovery | Founder + Solutions Engineer | Zoom, Notion, questionnaire | 6 ч | 42 000 | Низкая |
| 5 | Аудит текущего контента | Solutions Engineer | Connectors, crawler, sample import | 8 ч | 46 000 | Средняя |
| 6 | Демо AI-search и governance | AE + Founder | Demo workspace, slide deck | 4 ч | 26 000 | Средняя |
| 7 | Scoping пилота и расчёт ROI | Solutions Engineer + Finance | ROI sheet, pricing model | 5 ч | 31 000 | Средняя |
| 8 | Security / legal / procurement review | Founder + Ops | DPA/SLA templates, e-sign, procurement docs | 8 ч | 58 000 | Низкая |
| 9 | Коммерческое предложение | AE / Founder | CPQ, CRM, docs | 5 ч | 34 000 | Средняя |
| 10 | Onboarding kickoff и первый платёж | CSM + Finance Ops | Billing, ЭДО, банк, checklist | 4 ч | 33 000 | Высокая |

---

## Этап 4 — Финансовая модель и критика
# 05-critic

## Кейс
enterprise-ai-documentation-platform

## Итог критика
**PASS WITH RESERVATIONS**

Base scenario P&L:
- M6: **9 клиентов, MRR 2 520 000 ₽, EBITDA -1 174 000 ₽**
- M12: **23 клиента, MRR 6 440 000 ₽, EBITDA 1 322 000 ₽**
- EBITDA break-even: **M9**
- Startup capital to break-even: **≈12,1 млн ₽**
- Практически безопасный reserve: **14-15 млн ₽**

Sensitivity:
- CAC x2 -> payback **6,60 мес**
- Churn x2 -> LTV **5,39 млн ₽**
- Price -30% -> M12 EBITDA падает до **-610 000 ₽**

Главные риски:
1. Price compression из-за сравнения с wiki/help-center решениями.
2. Delivery creep и сползание в кастомную редакционную студию.
3. CAC inflation из-за длинного enterprise sales cycle.

Kill conditions:
- к M6 нет 6 активных клиентов и MRR < 1,7 млн ₽;
- realised ARPA < 220 000 ₽/мес два квартала подряд;
- gross margin < 55% три месяца подряд или CAC payback > 9 месяцев.

---

## Этап 5 — Финальный вердикт
# 06-verdict

## Сектор
GEO-EXPAND

## Финальный статус
**APPROVED С ЗАМЕЧАНИЯМИ**

## Итоговый балл
**72/100**

Разбивка:
- спрос: **16/20**
- экономика: **17/25**
- масштабируемость: **14/20**
- конкуренция: **10/15**
- барьеры входа: **6/10**
- качество данных: **9/10**

Почему approved:
- есть validated category и 4 конкурента с публичными ценами;
- unit economics сильные, GM **69,3%**, payback **3,30 мес**, LTV/CAC **16,8x**;
- компания выходит на **500k+ EBITDA** при **19 клиентах** и на **1M+ EBITDA** при **23 клиентах**.

Что доказать до запуска:
1. Минимум 3 дизайн-партнёра с чеком от **250 000 ₽/мес**.
2. Realised ARPA не ниже **220 000 ₽/мес**.
3. Gross margin на реальной delivery-базе не ниже **60%**.

---

## Этап 6 — История прохождения пайплайна
# 07-score-trajectory
## Кейс: enterprise-ai-documentation-platform
## Перепрогон начат: 2026-04-18

### 2026-04-19 — Program 4 / Demand Validation
- Статус: **PASS**
- Demand score: **16/20**
- LTV Gate: **PASS**

### 2026-04-19 — Program 5 / Unit Economics
- Статус: **PASS**
- Economics score: **21/25**
- LTV: **10,8 млн ₽**
- CAC: **640 тыс. ₽**
- LTV/CAC: **16,8x**
- CAC Payback: **3,30 месяца**

### 2026-04-19 — Program 6 / Financial Model + Critic
- Статус: **PASS WITH RESERVATIONS**
- Critic score: **18/25**
- Base scenario M12 MRR: **6,44 млн ₽**
- Base scenario M12 EBITDA: **1,322 млн ₽**
- Startup capital to EBITDA break-even: **≈12,1 млн ₽**

### 2026-04-19 — Программа 7 / Critic and verdict
- Статус: **APPROVED**
- Итоговый балл: **72/100**
- Разбивка: спрос **16/20**, экономика **17/25**, масштаб **14/20**, конкуренция **10/15**, защита **6/10**, данные **9/10**
- LTV/CAC: **16,8:1** | CAC Payback: **3,30 месяца** | Break-even: **9 месяц / 15 клиентов**
- Стартовый капитал до BEP: **12 084 000 ₽**
- Причина: кейс проходит инвестиционный порог как premium enterprise AI documentation platform с managed ops, но только при удержании ARPA около 280 тыс. ₽/мес и без ухода в low-end docs hosting.

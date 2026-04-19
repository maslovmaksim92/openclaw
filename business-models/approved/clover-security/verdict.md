# Clover Security
**Статус:** APPROVED
**Итоговый балл:** 76/100
**Дата:** 2026-04-19
**Сектор:** ENTERPRISE AI / APPSEC / DEVSECOPS

---

## Этап 1 — Описание кейса
### Что это
Clover Security позиционируется как AI product security engineer для enterprise-разработки, который автоматизирует product security review, AppSec-проверки и часть cloud security-задач внутри крупных продуктовых команд.

### Почему это может быть кейсом
Российские банки, финтех, маркетплейсы, телекомы и крупные продуктовые IT-команды регулярно упираются в дефицит AppSec-экспертизы и медленные security review. Локальный продукт с фокусом на автоматизацию security-by-design и разгрузку AppSec-команд может продаваться как инфраструктурный B2B SaaS с высоким чеком.

### Сигнал
- 13 марта 2026 Axios сообщил о Clover Security и раунде $50 млн.
- На сайте компании продукт описан как AI product security engineer для enterprise AppSec и cloud security.
- В сигнале указано коммерческое использование у десятков компаний, включая Fortune 500 и единорогов.

### Предварительная оценка LTV
Потенциал по выручке на одного крупного клиента в РФ: 3-12 млн ₽ в год, то есть примерно 250 тыс. - 1 млн ₽ в месяц. Для верхнего сегмента enterprise это проходит порог >500 тыс. ₽ в месяц.

### Источники
- https://www.axios.com/pro/enterprise-software/2026/03/13/clover-security-product-security-engineer-funding
- https://www.cloversecurity.com/

---

## Этап 2 — Проверка спроса
### Рыночное позиционирование
- Целевой покупатель: крупные продуктовые компании, банки, финтех, телеком, маркетплейсы, интеграторы и enterprise-разработчики с собственными командами AppSec / DevSecOps.
- Проблема: security review и проверка релизов тормозят SDLC, AppSec-команды перегружены, ручной triage дорогой, а требования к безопасной разработке и аудиту растут.
- Решение: AI product security engineer, который автоматизирует часть product security review, AppSec-checks, приоритизацию и remediation workflow.

### Сигналы спроса
- Mandatory demand API был недоступен в рантайме, поэтому использованы публичные коммерческие сигналы и цены конкурентов.
- Telegram-native рынка в РФ не найдено, но для enterprise AppSec это нейтральный фактор, так как покупки идут через sales-led цикл.
- Найден локальный сигнал через HScan/Krayon с on-prem и бесплатным пилотом, что подтверждает локальный enterprise-формат закупки.
- Positive Technologies сообщала, что 77% российских компаний внедряют DevSecOps, а 56% крупных компаний увеличили бюджеты на ИБ на 20-40%.

### Конкуренты с ценами
| Игрок | Что продаёт | Публичная цена | Цена в рублях | Источник |
|---|---|---:|---:|---|
| Semgrep Teams | SAST / AppSec platform | 30 $ / мес / contributor | ~2 400 ₽ / мес / contributor | https://semgrep.dev/pricing/ |
| Snyk Team | Dev-first AppSec platform | от 25 $ / мес / contributor | ~2 000 ₽ / мес / contributor | https://snyk.io/plans/ |
| Mend AppSec | AppSec platform | from 1 000 $ / year / contributing developer | ~80 000 ₽ / год / contributing developer | https://www.mend.io/pricing/ |

### WTP
WTP подтверждено: мировой рынок уже платит за AppSec workflow по recurring-модели, а в РФ заметен рост бюджетов на DevSecOps и secure SDLC.

### TAM / SAM / SOM
- TAM: 24,0 млрд ₽ / год
- SAM: 5,25 млрд ₽ / год
- SOM: 157,5 млн ₽ / год
- Зрелость рынка: GROWING / EARLY SCALE

### LTV Gate
- Seat-based SaaS: 1,2 млн ₽ / мес -> PASS
- Annual platform license / on-prem: 6,0 млн ₽ / мес run-rate -> PASS
- Managed AppSec copilot + сервис: 3,5 млн ₽ / мес -> PASS
- Scan-based / project usage: 3,2 млн ₽ / мес -> PASS
- Channel / MSSP model: 720 тыс. ₽ / мес -> PASS

### Итог этапа спроса
Demand verdict: MEDIUM-HIGH. Кейс проходит дальше, потому что категория платящая, бюджеты растут, а локальное окно для AI-native AppSec ещё открыто.

---

## Этап 3 — Юнит-экономика
### Бизнес-процесс
| № | Шаг | Кто | Инструмент | Время | Стоимость |
|---|---|---|---|---|---:|
| 1 | Формирование ICP-списка target accounts | SDR / Growth | Apollo, LinkedIn Sales Navigator, CRM | 1,5 ч | 2 500 ₽ |
| 2 | Outreach sequence, касания, follow-up | SDR | Email automation, LinkedIn, Telegram, CRM | 2,0 ч | 4 000 ₽ |
| 3 | Qualification call | AE | Zoom/Meet, CRM, call notes AI | 1,5 ч | 3 500 ₽ |
| 4 | Product demo + AppSec pain discovery | AE + Solutions Architect | Demo env, презентация, CRM | 2,5 ч | 7 000 ₽ |
| 5 | Technical scoping и pilot design | Solutions Architect + Security AI Engineer | Notion, Jira, repo access | 7,0 ч | 18 000 ₽ |
| 6 | Security / legal / procurement review | CTO + Solutions Architect + external legal | Security questionnaire, DPA/NDA, procurement docs | 6,0 ч | 34 000 ₽ |
| 7 | Пилотный запуск и интеграция | CSM + Engineer | Cloud/on-prem setup, CI/CD integration, Slack/Jira | 10,0 ч | 42 000 ₽ |
| 8 | ROI case, internal champion package, pricing | AE + Founder | ROI calculator, pricing sheet, deck | 5,0 ч | 12 000 ₽ |
| 9 | Contracting, vendor onboarding, invoice issue | AE + Finance/Ops | EDI/документооборот, billing, CRM | 3,0 ч | 19 000 ₽ |
| 10 | Go-live, first month support, payment collection | CSM + Finance/Ops | Billing, support desk, customer portal | 4,0 ч | 11 000 ₽ |

### Основные метрики
- Базовый контракт: 6 000 000 ₽ в год, или 500 000 ₽ MRR на клиента.
- COGS: 126 000 ₽ / клиент / месяц.
- Gross Margin: 74,8%.
- Contribution Margin: 70,2%.
- Blended CAC: 2 220 000 ₽.
- Churn: 1,2% / месяц.
- LTV: 31 166 667 ₽.
- LTV/CAC: 14,0x.
- CAC Payback: 6,3 месяца.
- Break-even: 13 клиентов, или 6,5 млн ₽ MRR / 78 млн ₽ ARR.

### Команда
13 ролей, 3 370 000 ₽ ФОТ в месяц и 4 044 000 ₽ fully loaded.

### Итог этапа экономики
Unit economics verdict: PASS. Модель выдерживает длинную enterprise-продажу и даёт фондово-привлекательный payback.

---

## Этап 4 — Финансовая модель и критика
### P&L, базовый сценарий
- Месяц 6: MRR 3,0 млн ₽, EBITDA -2,346 млн ₽.
- Месяц 11: первая положительная EBITDA, +196 тыс. ₽.
- Месяц 12: MRR 7,5 млн ₽, EBITDA +570 тыс. ₽.

### Альтернативные сценарии
- Optimistic: безубыточность в месяце 8, месяц 12 даёт MRR 11,5 млн ₽ и EBITDA 3,412 млн ₽.
- Pessimistic: за 12 месяцев бизнес не выходит в плюс, месяц 12 остаётся на EBITDA -1,3 млн ₽.

### Денежный поток
- Кумулятивный убыток доходит до 22,4 млн ₽ к месяцу 10.
- С буфером 15% стартовый капитал до BEP: 25,8 млн ₽.
- Burn M1-M3: 4,066 млн ₽, 3,692 млн ₽, 3,318 млн ₽.

### Sensitivity
- CAC x2 -> payback 12,6 месяца, LTV/CAC 7,0x, капитал до BEP около 39,1 млн ₽.
- Churn x2 -> LTV падает до 15,58 млн ₽, LTV/CAC до 7,0x.
- Price -30% -> payback 11,0 месяцев, break-even 23 клиента, LTV 21,82 млн ₽.

### Главные риски
| Риск | Вероятность | Влияние |
|---|---|---:|
| Цена не держится, скидки >25% | 40% | 2 250 000 ₽/мес |
| Продажи завязаны на founder | 45% | 1 800 000 ₽/мес |
| Пилоты не конвертируются в годовые контракты | 35% | 1 500 000 ₽/мес |

### Kill conditions
1. К концу месяца 9 меньше 8 платящих клиентов при burn выше 2,5 млн ₽ / месяц.
2. Median ASP падает ниже 350 тыс. ₽ MRR на двух подряд новых сделках.
3. Pilot-to-annual conversion ниже 30% на выборке минимум из 10 пилотов.

### Итог этапа критика
PASS, но с повышенным execution risk. Модель сильна экономически, но очень чувствительна к удержанию цены и repeatable enterprise conversion.

---

## Этап 5 — Финальный вердикт
### Score breakdown
| Критерий | Балл | Максимум |
|---|---:|---:|
| Реальный спрос | 16 | 20 |
| Юнит-экономика | 23 | 25 |
| Масштабируемость | 15 | 20 |
| Конкурентное позиционирование | 8 | 15 |
| Барьеры входа | 6 | 10 |
| Качество данных | 8 | 10 |
| **Итого** | **76** | **100** |

### Ключевые метрики вердикта
- CAC: 2 220 000 ₽
- LTV: 31 166 667 ₽
- LTV/CAC: 14,0x
- Payback: 6,3 месяца
- GM: 74,8%
- Break-even: 13 клиентов
- Стартовый капитал до BEP: 25 800 000 ₽

### Почему одобрено
1. Экономика уже сейчас инвестиционного уровня: LTV/CAC 14,0x и payback 6,3 месяца.
2. AppSec-категория имеет подтверждённый мировой WTP и растущий локальный бюджетный контур.
3. Порог безубыточности достижим на 13 клиентах, что реалистично для premium enterprise security vendor.

### Что доказать до запуска
1. Median ASP не ниже 450 000 ₽ MRR на серии из 5 сделок.
2. Pilot-to-annual conversion не ниже 30% на выборке от 10 пилотов.
3. Не менее 50% wins должны закрываться не через founder лично, а через воспроизводимый коммерческий playbook.

### Итог
APPROVED. Кейс проходит как controlled bet с высоким upside при сохранении enterprise pricing power.

---

## Этап 6 — История прохождения пайплайна
### 2026-04-19 — Program 4 / Demand Validation
- Статус: PASS
- Demand verdict: MEDIUM-HIGH
- TAM / SAM / SOM: 24,0 млрд ₽ / 5,25 млрд ₽ / 157,5 млн ₽ в год.
- LTV Gate: PASS во всех базовых сценариях.

### 2026-04-19 — Program 5 / Unit Economics
- Статус: PASS
- COGS: 126 000 ₽ / клиент / месяц.
- Gross Margin: 74,8%.
- Contribution Margin: 70,2%.
- CAC: 2 220 000 ₽.
- LTV: 31 166 667 ₽.
- Break-even: 13 клиентов.

### 2026-04-19 — Program 6 / Financial Model + Critic
- Статус: PASS
- Base month 12: MRR 7,5 млн ₽, EBITDA 570 тыс. ₽.
- Startup capital to BEP: 25,8 млн ₽.
- Главный fragility point: price compression и repeatable enterprise conversion.

### 2026-04-19 — Program 7 / Critic and verdict
- Статус: APPROVED
- Итоговый балл: 76/100
- Разбивка: спрос 16/20, экономика 23/25, масштаб 15/20, конкуренция 8/15, защита 6/10, данные 8/10.
- Причина: сильная enterprise AppSec-экономика и доказанный WTP перевешивают риски, но кейс остаётся зависим от удержания цены.

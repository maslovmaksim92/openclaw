# 06-verdict

## Кейс
ai-accounting-document-processing-operator

## Дата вердикта
2026-04-18, Europe/Moscow

## Статус
**APPROVED С ЗАМЕЧАНИЯМИ**

## Итоговый балл
**74/100**

Порог пройден за счёт подтверждённого спроса, сильной юнит-экономики и понятного пути к break-even, но кейс остаётся чувствительным к ценовому давлению и риску превращения в service-heavy интегратор без платформенного рычага.

## Score breakdown
| Критерий | Балл | Максимум | Обоснование |
|---|---:|---:|---|
| Реальный спрос | 16 | 20 | Есть RU-конкуренты с реальными ценами, HH proxy очень сильный, WTP подтверждён 1С и Rossum, но не удалось получить обязательный local demand feed. |
| Юнит-экономика | 22 | 25 | LTV 10.0 млн ₽, GM 55.5%, LTV/CAC 12.8x, payback 3.9 месяца, break-even 13 клиентов. |
| Масштабируемость | 12 | 20 | Delivery частично автоматизирован, но exception handling и интеграции 1С пока съедают значимую долю ручного труда. |
| Конкурентное позиционирование | 9 | 15 | Есть рабочий wedge в RU-first, on-prem и managed exceptions, но 1С и bundle-игроки способны быстро давить по цене. |
| Барьеры входа | 7 | 10 | Защита строится на интеграциях, SLA и данных по документам, однако регуляторного или патентного барьера нет. |
| Качество данных | 8 | 10 | Ключевые цифры и цены подтверждены источниками, есть WTP, но mandatory local endpoints технически не ответили. |
| **ИТОГО** | **74** | **100** | **APPROVED с замечаниями** |

## Полный бизнес-процесс из 04-economics.md
| № | Шаг | Кто | Инструмент | Время | Стоимость (руб) | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Поиск и обогащение целевых аккаунтов | BDR | HH/контур рынка, LinkedIn-аналоги, Excel/CRM | 20 мин | 900 | Средняя |
| 2 | Первый outreach / касание | BDR | e-mail, Telegram, телефония, CRM | 15 мин | 700 | Средняя |
| 3 | Квалификация лида | AE / sales lead | CRM, скрипт qualification | 30 мин | 1 800 | Низкая |
| 4 | Discovery call | AE + solutions architect | Meet, CRM, шаблон discovery | 60 мин | 4 200 | Низкая |
| 5 | Сбор 50-200 тестовых документов | Presale engineer | secure upload, S3/облако, checklist | 90 мин | 4 500 | Средняя |
| 6 | Тестовое распознавание / demo pilot | ML/integration engineer | OCR/LLM pipeline, валидация | 4 ч | 12 000 | Высокая |
| 7 | Разбор результатов и ROI-калькулятор | Solutions architect | Excel, ROI template | 2 ч | 7 000 | Средняя |
| 8 | Коммерческое предложение и scoping | AE + architect | CRM, CPQ, шаблон SoW | 2 ч | 8 500 | Средняя |
| 9 | Инфобез / legal / procurement | Founder + architect | DPA/NDA templates, e-sign | 6 ч | 18 000 | Низкая |
| 10 | Подписание договора | Founder / AE | ЭДО, e-sign | 1 ч | 2 500 | Высокая |
| 11 | Онбординг и доступы | PM / delivery lead | Jira, Notion, secure checklist | 4 ч | 10 000 | Средняя |
| 12 | Интеграция с 1С/ERP | Integration engineer | 1С, API, ETL scripts | 24 ч | 60 000 | Низкая |
| 13 | Настройка типов документов и правил | Solutions architect + ML engineer | rule engine, prompt/config layer | 20 ч | 54 000 | Средняя |
| 14 | UAT и исправления | QA + customer ops | test suite, dashboards | 12 ч | 24 000 | Средняя |
| 15 | Go-live | Delivery lead | monitoring, runbook | 4 ч | 8 000 | Средняя |
| 16 | Ежемесячная автообработка потока | AI pipeline | OCR/LLM, workflow engine | непрерывно | 50 000 | Высокая |
| 17 | Ручная обработка исключений | Customer ops specialist | queue console, 1С, QA panel | 32 ч/мес | 72 000 | Низкая |
| 18 | Ежемесячный контроль качества и SLA | CSM / QA | BI dashboard, QA checks | 8 ч/мес | 28 000 | Средняя |
| 19 | Выставление счёта | Finance ops | 1С, ЭДО | 30 мин/мес | 1 200 | Высокая |
| 20 | Получение оплаты | Finance ops | банк, 1С | 15 мин/мес | 800 | Высокая |

## Ключевые метрики
| Метрика | Значение |
|---|---:|
| CAC | 780 000 ₽ |
| ARPA | 420 000 ₽/мес |
| COGS | 187 000 ₽/мес |
| Gross Profit | 233 000 ₽/мес |
| Gross Margin | 55.5% |
| Contribution Profit | 200 000 ₽/мес |
| Contribution Margin | 47.6% |
| LTV | 9 996 000 ₽ |
| LTV/CAC | 12.8x |
| CAC Payback | 3.9 месяца |
| Break-even | месяц 8 / 13 клиентов |
| Стартовый капитал до cash BEP | ~3 900 000 ₽ |

## Команда для запуска
| Роль | Функция | Занятость | Зарплата (руб/мес) |
|---|---|---|---:|
| Founder / GM | Продажи крупных сделок, партнёрства, стратегия | full | 300 000 |
| Sales lead / AE | Discovery, pipeline, closing | full | 220 000 |
| BDR | Outbound, lead gen, qualification | full | 120 000 |
| Solutions architect | Presale, scoping, ROI model, solution design | full | 250 000 |
| ML engineer | OCR/LLM pipeline, accuracy tuning | full | 240 000 |
| 1С / ERP integration engineer | Интеграции и rollout | full | 230 000 |
| Product + QA lead | Quality control, roadmap, test cases | full | 180 000 |
| Finance / ops manager | Billing, документооборот, procurement | full | 140 000 |
| Customer ops specialist | Exception handling | part/variable | 120 000 |
| CSM / support specialist | SLA, onboarding, апсейл | part/semi-variable | 140 000 |

**Итого команда:** 10 ролей  
**Fixed payroll core:** 1 680 000 ₽/мес  
**Fixed costs total:** 2 500 000 ₽/мес

## Топ-3 риска
| Риск | Вероятность | Влияние |
|---|---|---:|
| Кастомизация под каждую конфигурацию 1С ломает масштабируемость | высокая | 900 000 ₽/мес |
| Ценовое давление со стороны 1С и bundle-игроков | средняя | 1 050 000 ₽/мес |
| Ошибки распознавания создают финансовые или налоговые инциденты | средняя | 1 500 000 ₽/мес |

## Почему модель одобрена
1. **Спрос и готовность платить уже подтверждены.** 1С продаёт решение до 3 000 000 ₽/год, Rossum держит price floor около 1.37 млн ₽/год, OnlyRead показывает 34 988 пользователей в RU low-end слое.
2. **Экономика сильная даже для service-led модели.** LTV 9 996 000 ₽, LTV/CAC 12.8x, payback 3.9 месяца, break-even на 13 клиентах.
3. **Есть понятный wedge против commodity OCR.** Локальное развёртывание, 1С/ERP-интеграции и managed exception handling позволяют продавать не распознавание страниц, а операционный SLA-слой.

## Что доказать до запуска
1. Подтвердить, что доля ручных exceptions после 90 дней удерживается **ниже 25%** потока на первых 3 клиентах.
2. Подтвердить, что средний реализованный ARPA удерживается **не ниже 350 000 ₽/мес** без скидки глубже 20%.
3. Подтвердить, что не менее **50% новых сделок** приходят через партнёров 1С, а blended CAC остаётся **ниже 900 000 ₽**.

## Замечания инвесткомитета
- Одобрение условное: нельзя идти в commodity OCR и page-based pricing.
- Масштабировать только через стандартизированные коннекторы, типовые playbook внедрения и жёсткую продуктовую дисциплину по исключениям.
- Если ARPA опустится ниже 300 000 ₽/мес или COGS уйдёт выше 240 000 ₽/клиент/мес, кейс требует немедленной переоценки.

## Финальный вывод
**APPROVED с замечаниями.**

Инвесткомитет готов пропустить кейс дальше, потому что рынок и economics выглядят достаточно сильными для high-LTV B2B-оператора. Но право на ошибку узкое: защищать нужно не OCR, а управляемый workflow-слой вокруг 1С/ERP, SLA и exception handling.
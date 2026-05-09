# Demand validation — Medsenger: AI-дистанционный мониторинг и телемедицина для клиник

## Итог
**Решение: PASS WITH RESERVATIONS.**

Почему не early reject:
- exact-category demand по broad keyword низкий: `multi-demand` вернул **LOW** и `hh_vacancies=3`;
- но willingness to pay подтверждена публичными внедрениями, ценами конкурентов и фактом, что клиники уже продают пациентам абонементы дистанционного сопровождения [T2][T3];
- Profit Gate проходит в нескольких B2B-сценариях, то есть достижение **EBITDA 500K+ ₽/мес** выглядит достижимым без фантастической доли рынка.

## Demand snapshot
- `multi-demand("дистанционный мониторинг пациентов телемедицина клиники")` → **LOW**, demand_score=0, Habr=2, HH=3, Yandex Suggest=2. Это сигнал, что рынок продаётся не по category pull, а через solution selling и ROI-selling. [T1]
- Внедрение в медцентре «XXI век» подтверждает, что клиники уже покупают такой контур как отдельный сервис, а не только как «фичу МИС». Бюджет проекта был **60M+ ₽**, в проекте участвовали **200 врачей**, **1 166 пациентов**, сервисом консультаций пользовались **500+ человек**. [T2]
- Кейс также подтверждает monetization-through-clinic: пациентам продавались **абонементы на дистанционный мониторинг и ведение лечения**. Это сильное доказательство WTP и для клиники, и для конечного пользователя. [T2]

## Конкуренты и price evidence
| Игрок | Что продаёт | Прайс / модель | Вывод |
|---|---|---:|---|
| **Medsenger** | Дистанционный мониторинг, чат с врачом, reminders, опросники | **7 000–10 000 ₽/мес за активного врача**, white-label от **500 000 ₽** [T3] | Категория уже имеет в РФ понятный B2B reference price |
| **Medesk** | МИС + телемедицина для клиник | от **5 490 ₽/мес за пользователя** на публичном pricing [T3] | Телемедицина входит в нормальный software budget клиники |
| **RWD Analytics Telemed** | Телемедицина / дистанционное наблюдение | **1 000 ₽/мес за врача**, старт внедрения от **100 000 ₽** [T3] | Есть low-end предложение, значит рынок price-discovered |
| **DocMeet** | Онлайн-запись и телемедицинный модуль | от **3 490 ₽/мес** [T3] | Низкий entry-point упрощает пилоты, но давит на SMB pricing |

**Вывод по pricing:** рыночный диапазон в РФ уже существует. Для mid-market клиник реалистичен ACV порядка **0.6–1.5M ₽/год** за 10–15 активных врачей плюс onboarding. [T3]

## Telegram в РФ
- В `multi-demand` для этого keyword Telegram-signals фактически пустые, subscribers=0. [T1]
- По manual web-check заметных standalone Telegram-first B2B-сервисов для легального дистанционного мониторинга клиник в РФ не видно; игроки продают **web/mobile platform inside protected contour**, а Telegram чаще выступает как канал уведомлений/бот-интерфейс, а не как самостоятельный продукт. [T2][T3]
- Для regulated healthcare это логично: продавать полноценный clinical workflow поверх одного Telegram-бота тяжело из-за 152-ФЗ, аудита сообщений и требований 323-ФЗ; именно поэтому Medsenger отдельно подчёркивает защищённый контур и хранение ПДн в РФ. [T2][T3]

## WTP, proof of willingness to pay
1. **Clinic-side WTP подтверждена** реальным внедрением на **60M+ ₽** в «XXI век». Это не PoC на 100–300K ₽, а крупный бюджетный проект. [T2]
2. **Patient-side WTP подтверждена** тем, что клиника через платформу продаёт **абонементы дистанционного мониторинга и ведения лечения**. [T2]
3. **Reference-price WTP подтверждена конкурентами**: на рынке уже есть публичные ставки от 1 000 ₽/врач/мес до 10 000 ₽/врач/мес и пакеты от 3 490 ₽/мес до 500K ₽ setup. [T3]
4. **Pain-side WTP умеренная, а не взрывная**: exact category search-pull слабый, значит продукт надо продавать через outcomes, например снижение no-show, рост LTV хронических пациентов, разгрузку регистратуры и врача, а не через слово «дистанционный мониторинг». [T1][T2]

## Market sizing

### Методика
Считал два пути: top-down и bottom-up. Для РФ беру не весь healthcare spend, а только адресуемую software/protocol layer в частной медицине.

### Ключевые допущения
- Объём рынка платных медуслуг в РФ в 2024 году находился около **1.5–1.6T ₽** по отраслевым публикациям со ссылками на рыночную статистику. [T2]
- В РФ действует около **8 700 частных медицинских компаний**; это база потенциальных покупателей, но не все подходят по профилю. [T2]
- Подходящий сегмент для Medsenger, это клиники с хроническим сопровождением, post-visit follow-up, реабилитацией, кардио, эндокринологией, онкологией, женским здоровьем и многопрофильные сети. Консервативно беру **12%** от базы как реально нуждающийся и готовый сегмент. [T1][T2]
- Средний контракт: **1.1M ₽/год**. Это примерно 10 активных врачей × 9 000 ₽/мес × 12 мес + небольшой onboarding / support uplift. [T3]

### Таблица reconciliation
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---|---:|---:|---|---|
| TAM (мир) | **$14.7B** рынок remote patient monitoring / telehealth wedge [T3] | — | — | top-down |
| TAM (РФ) | **1.70B ₽** = 1.55T ₽ × 0.11% software share [T2] | **1.74B ₽** = 8 700 компаний × 200K ₽ минимального annual spend [T2][T3] | diff ~2%, оценки сходятся | lower/top-down |
| SAM (РФ) | **1.19B ₽** = 1.70B ₽ × 70% segment fit [T2] | **1.15B ₽** = 8 700 × 12% × 1.1M ₽ [T1][T2][T3] | diff ~3%, оценки сходятся | lower/bottom-up |
| SOM Y1 | **24M ₽** = 2% SAM [T2] | **23M ₽** = ~21 клиника/контрактов по 1.1M ₽ [T3] | diff ~4% | **используем 23M ₽** |
| SOM Y3 | **95M ₽** = 8% SAM [T2] | **80M ₽** = 7% bottom-up SAM [T3] | diff ~19%, обе оценки реалистичны | **используем 80M ₽** |

### Комментарий к sizing
- Расхождение top-down и bottom-up меньше 3x, значит сегмент выбран адекватно.
- SOM Y1 < 10% SAM, это реалистично.
- При ARR ~1.1M ₽ SOM Y1 требует около **21 новых/активных контрактов**. При среднем deal cycle **4 месяца** это тяжёлый, но выполнимый founder-led / enterprise-sales motion.

## Bottom-up buyers, 10 реальных target accounts
1. МЕДСИ [T2]
2. Мать и дитя / MDMG [T2]
3. СМ-Клиника [T2]
4. АВА-ПЕТЕР / Скандинавия [T2]
5. EMC [T2]
6. Будь Здоров [T2]
7. АО «Медицина» [T2]
8. Семейный доктор [T2]
9. MedSwiss [T2]
10. РЖД-Медицина [T2]

**Почему именно они:** большие сети и многопрофильные игроки легче монетизируют follow-up programs, ведут chronic care pathways и могут распределить покупку на 10–50 врачей, а не на одного энтузиаста. [T2]

## Самые вероятные специализации для fast adoption
1. **Эндокринология**: диабет, ожирение, long-term adherence, повторяемый контроль показателей. [T2]
2. **Кардиология**: давление, пульс, контроль терапии, быстрое value proof для клиники и врача. [T2]
3. **Реабилитация / постоперационное ведение**: чёткий временной контур и хорошие patient-engagement сценарии. [T2]
4. **Онкология / supportive care**: высокий value per patient, но длиннее sale и выше compliance burden. [T2]
5. **Многопрофильные частные сети**: лучше всего масштабируют cross-specialty deployment. [T2]

## Profit Gate: все monetization scenarios
### 1) Лицензия за активного врача
- Допущение: **250 активных врачей** в базе, ARPU **8 000 ₽/врач/мес** → **2.0M ₽ MRR**. [T3]
- GM 80% → валовая прибыль **1.6M ₽/мес**.
- При OPEX **1.0–1.1M ₽/мес** EBITDA ≈ **0.5–0.6M ₽/мес**.
- **Вердикт: PASS.** Достижимо через ~12 средних клиник по 20–25 активных врачей.

### 2) Оплата за пациента / программу наблюдения
- Допущение: take-rate платформы **1 200 ₽/пациент/мес**, 3 000 активных пациентов → **3.6M ₽ MRR**. [T2][T3]
- При GM 65% и OPEX **1.7M ₽/мес** EBITDA ≈ **0.6M ₽/мес**.
- **Вердикт: PASS, но сложнее.** Нужна сильная клиническая методология и контроль churn на patient layer.

### 3) Enterprise setup + support
- Допущение: 4 внедрения в год по **3M ₽** = **12M ₽ ARR equivalent**, плюс recurring support **300K ₽/мес**. [T2][T3]
- В среднем это даёт **~1.3M ₽ revenue/month equivalent**; при GM 60% и OPEX **1.0M ₽/мес** EBITDA около **-0.2M до +0.1M ₽/мес** в слабые месяцы.
- **Вердикт: FAIL как standalone motion.** Слишком project-heavy и неровный cash flow.

### 4) Hybrid: setup + doctor-based recurring
- Setup **500K–1M ₽** + recurring **8–10K ₽/врач/мес**. [T3]
- Это лучший компромисс: окупает внедрение, не убивает sale длинным SI-проектом и сохраняет SaaS-like margin.
- **Вердикт: PASS, это рекомендованная monetization model.**

**Общий вывод по Profit Gate:** компания может выйти на **500K+ ₽ EBITDA/мес** в doctor-based и hybrid сценариях. Значит кейс **не подлежит early reject**.

## Главные риски спроса
- Exact category pull слабый, поэтому CAC может быть высоким: продавать придётся не «RPM-платформу», а экономику follow-up programs. [T1]
- Часть спроса будет съедаться МИС/ERP-игроками, которые добавляют телемедицину как модуль. [T3]
- В regulated healthcare длинный цикл согласований, интеграций и медико-юридической оценки. [T2]

## Что нужно доказать на следующем этапе
- CAC по founder-led и partner-led каналам.
- Конверсию пилот → платный rollout.
- Net revenue retention по клиникам и программам наблюдения.
- Насколько быстро масштабируется не только в одной сети, но и cross-clinic.

## Verdict
**PASS TO NEXT STAGE.**

Кейс не выглядит category-led, зато выглядит **ROI-led и enterprise-wedge-driven**. Для фонда это не массовый SMB SaaS, а нишевой B2B healthtech с реальным бюджетом внедрения, уже существующим reference pricing и достижимым Profit Gate.

## Sources
- [T1] multi-demand endpoint по keyword `дистанционный мониторинг пациентов телемедицина клиники` (HH/Habr/Yandex signals), проверено 2026-05-09.
- [T2] Skolkovo: https://sk.ru/news/telemedicinskaya-platforma-medsenger-pomogaet-vracham-medcentra-xxi-vek-distancionno-kontrolirovat-sostoyanie-pacientov/
- [T2] vc.ru: https://vc.ru/id996201/667835-telemedicinskaya-platforma-medsenger-pomogaet-vracham-medcentra-xxi-vek-distancionno-kontrolirovat-sostoyanie-pacientov
- [T2] Коммерсантъ / Контур.Фокус, 2025: https://www.kommersant.ru/doc/7796287
- [T3] Medsenger official site / pricing context: https://about.medsenger.ru/
- [T3] Medesk pricing: https://www.medesk.net/ru/prices/
- [T3] RWD Analytics telemed: https://rwdanalytics.ru/telemed/
- [T3] DocMeet: https://docmeet.ru/
- [T3] Global RPM market reference search: https://www.fortunebusinessinsights.com/remote-patient-monitoring-market-106265

Sources: T1=1, T2=4, T3=5. Primary evidence basis: T2.
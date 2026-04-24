---
sector: B2B-OPS
stage: demand-validation
updated: 2026-04-24T22:27:55+03:00
analyst: branch-models-lead
composite_demand: LOW
profit_gate: FAIL
---

# 02-demand — Demand Validation

## 1. Что валидируем
Проверяем, можно ли в РФ построить фондово-интересный бизнес вокруг **AI-SDR / автономного outbound для B2B**: поиск ICP, персонализация outreach, follow-up и доведение до встречи как SaaS или productized managed service.

## 2. Demand snapshot
- Multi-demand по ключу `AI SDR автономный outbound продаж для B2B` вернул **LOW / 0**: Google Trends RU = 0, Habr = 2, Yandex Suggest = 2. Это прямой сигнал, что category pull в РФ почти не сформирован. [T1]
- На hh.ru при этом есть **103 вакансии по запросу “SDR”** и **1 771 вакансия по запросу “лидогенерация”** по России. Значит, базовая задача существует и компании уже тратят деньги на неё, но покупают пока в основном людей и агентства, а не автономного AI-SDR. [T1]
- Вывод: pain реален, но **explicit demand на AI-native category пока слабый**. [T1][inference]

## 3. Конкуренты и цены
### Глобальные / category-adjacent
1. **AiSDR**: Explore **$900/mo**, Grow **$2,500/mo**, Enterprise custom. Это наиболее близкий публичный price anchor для AI-SDR-as-a-service. [T1]
2. **Regie.ai**: AI SEP **$180/user/month** при annual contract и минимум 10 seats, Force Multiplier Rep **$499/user/month** при annual contract и минимум 5 seats. Это подтверждает, что рынок готов платить за AI-prospecting layer как за отдельный revenue tool. [T1]
3. **Smartlead**: Base **$39/mo**, Pro **$94/mo**, Unlimited Smart **$174/mo**, Unlimited Prime **$379/mo**. Это уже не автономный SDR, а инфраструктура cold outreach, но она задаёт нижнюю границу WTP за стек отправки и deliverability. [T1]

### Россия / Telegram- и messaging-layer
1. **Leadhero** позиционирует ИИ-лидогенерацию в **Telegram, WhatsApp, email, Avito, LinkedIn**. На сайте опубликованы кейсы с лидами по **100-150 ₽** и примером **17 продаж** со средним чеком **120 000 ₽**. Это не чистый AI-SDR, но это proof, что в РФ покупают автоматизированную лидогенерацию через мессенджеры. [T2]
2. **BotB2B** продаёт автообработку диалогов в **Telegram / WhatsApp / сайт / Авито** по цене **от 4,5 ₽ за диалог**. Это подтверждает существование локального paid messaging supply, но не enterprise-grade autonomous outbound. [T2]
3. На hh.ru есть активные вакансии у **Telega.in** и других компаний, работающих с Telegram-каналом продаж, что подтверждает monetizable GTM вокруг Telegram, но не наличие зрелого рынка именно для autonomous AI-SDR. [T1][T2][inference]

## 4. Willingness to pay
### Что подтверждено
- Международные price anchors показывают, что buyer готов платить от **$900/mo** за AI-SDR слой и до **$499/user/month** за AI prospecting seat. [T1]
- Российский рынок уже платит за лидогенерацию и диалоги в мессенджерах, но чаще как за **agency / messaging automation / appointment setting**, а не как за полностью автономного SDR-работника. [T2]
- hh.ru показывает, что компании продолжают нанимать SDR и лидогенераторов, то есть бюджетный карман существует и берётся из sales headcount / leadgen spend. [T1]

### Что не подтверждено
- Нет сильного evidence, что средний российский mid-market buyer уже готов массово покупать **автономного AI-SDR без human-in-the-loop**. [T1][T2][inference]
- Нет явного local category leader в РФ с прозрачной repeatable enterprise-монетизацией именно в AI-SDR. [T2][inference]

**Итог по WTP:** willingness to pay есть на смежный outcome, но **WTP на чистый autonomous AI-SDR в РФ пока слабый и early-adopter-only**. [T1][T2][inference]

## 5. Market sizing
### Методика
Считаю два пути и сверяю их.

#### Top-down
- База: мировой рынок sales force automation в 2023 году оценивался в **$10,017.3 млн**. [T2]
- Для AI-SDR беру только узкий addressable slice **6%** от broader sales automation stack, потому что продукт закрывает prospecting / outreach / follow-up, а не весь CRM-контур. Это аналитическое допущение, а не прямой факт. [T2][inference]
- Для РФ беру базой рынок CRM в России **44,1 млрд ₽** в 2025 году. [T2]
- Курс ЦБ РФ на 24.04.2026: **74,8349 ₽ за $1**. [T1]

#### Bottom-up
- В реестре МСП ФНС на 10.04.2026 числится **6 947 425** субъектов, из них **21 463** средних юрлица и **198 812** малых юрлиц. [T1]
- Для ICP AI-SDR беру не весь МСП-рынок, а только outbound-heavy B2B-компании. Консервативная рабочая база: **~6 000 компаний**. Это вывод из числа средних и малых юрлиц плюс факта, что hh.ru показывает живой наём в SDR / лидогенерации. [T1][inference]
- Доля компаний с выраженной болью: **25%**, потому что не всем нужен outbound motion и не все готовы покупать automation. [T1][inference]
- Средний контракт: **720 000 ₽ ARR** или **60 000 ₽/мес**, то есть существенно ниже западного full-stack AI-SDR и ближе к entry-level hybrid offer для РФ. [T1][T2][inference]

### Обязательная таблица
| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 44,99 млрд ₽ = $601,0 млн [T2][inference] | — | — | top-down |
| TAM (РФ) | 2,65 млрд ₽ = 44,1 млрд ₽ × 6% [T2][inference] | 4,32 млрд ₽ = 6 000 × 720 000 ₽ [T1][inference] | diff=1,63x, bottom-up выше, потому что считает полный spend buyer-base, а top-down только software slice | **lower** |
| SAM (РФ) | 1,19 млрд ₽ = TAM × 45% mid-market/tech-services fit [T2][inference] | 1,08 млрд ₽ = 6 000 × 25% × 720 000 ₽ [T1][inference] | diff=1,10x, расхождение допустимо | **1,08 млрд ₽** |
| SOM Y1 | 23,8 млн ₽ = 1,19 млрд ₽ × 2% | 21,6 млн ₽ = 1,08 млрд ₽ × 2% | diff=1,10x | **используем 21,6 млн ₽** |
| SOM Y3 | 95,2 млн ₽ = 1,19 млрд ₽ × 8% | 86,4 млн ₽ = 1,08 млрд ₽ × 8% | diff=1,10x | **используем 86,4 млн ₽** |

### 10 реальных buyers для bottom-up sanity check
1. Контур
2. Первый Бит
3. КОРУС Консалтинг
4. Mindbox
5. Roistat
6. Calltouch
7. Carrot quest
8. UIS
9. eLama
10. Telega.in

Это не доказанные клиенты, а **реальные компании с sales-led B2B motion**, для которых outbound automation может быть релевантным. [T2][inference]

### Sanity check
- SOM Y1 = **21,6 млн ₽ ARR**, то есть около **30 клиентов** по 720k ₽ ARR.
- При среднем sales cycle **2 месяца** нужно закрывать примерно **2,5 новых клиента в месяц** почти с нуля. Для новой категории в РФ это уже напряжённо, но не физически невозможно. [T1][T2][inference]
- Главная проблема не в размере рынка как таковом, а в **слабом category pull и высокой необходимости education-led продаж**. [T1][T2][inference]

## 6. Profit Gate, все сценарии монетизации
Цель: проверить, можно ли собрать **EBITDA ≥ 500k ₽/мес**.

### Сценарий A, SaaS-only
- Цена: **60k ₽/мес**
- Gross margin: **85%**
- Валовая прибыль с клиента: **51k ₽/мес**
- Базовый fixed opex: **1,8 млн ₽/мес**
- Для EBITDA 500k ₽ нужно валовой прибыли **2,3 млн ₽/мес**, то есть **46 клиентов**.
- Вердикт: **FAIL**. Для low-demand новой категории 46 платящих аккаунтов в РФ слишком агрессивно. [T1][T2][inference]

### Сценарий B, Hybrid copilot + managed setup
- Цена: **120k ₽/мес**
- Gross margin: **65%**
- Валовая прибыль с клиента: **78k ₽/мес**
- Для EBITDA 500k ₽ нужно **30 клиентов**.
- Вердикт: **FAIL**. Это лучше по экономике, но всё ещё требует слишком быстрого market education. [T1][T2][inference]

### Сценарий C, Done-for-you managed outbound
- Цена: **180k ₽/мес**
- Gross margin: **45%**
- Валовая прибыль с клиента: **81k ₽/мес**
- Для EBITDA 500k ₽ нужно **29 клиентов**.
- Вердикт: **FAIL**. Чек выше, но delivery быстро уходит в service-heavy модель, а не в scalable software. [T1][T2][inference]

**Итог Profit Gate:** во всех трёх сценариях проход к **500k ₽ EBITDA/мес** выглядит **неубедительным** для текущего российского спроса. [T1][T2][inference]

## 7. Demand verdict
**DEMAND = LOW. Profit Gate = FAIL. Итог: REJECTED на demand stage.**

Почему reject:
1. Прямой category demand в РФ сейчас слабый, что подтверждено multi-demand. [T1]
2. Buyers платят за результат лидогенерации, но чаще через людей, агентства и узкие messaging-автоматизации. [T1][T2]
3. Telegram в РФ полезен как канал, но локальный рынок пока даёт скорее tooling/agency proof, чем зрелый autonomous SDR market. [T2]
4. Ни один из проверенных сценариев монетизации не даёт уверенного прохода к EBITDA ≥ 500k ₽/мес без слишком оптимистичного допущения по скорости продаж. [T1][T2][inference]

## 8. Что должно было бы измениться, чтобы кейс вернулся
- появление 2-3 локальных игроков с прозрачным AI-SDR pricing и повторяемыми кейсами в РФ;
- заметный рост hh-сигналов именно по AI outbound / AI SDR, а не просто по лидогенерации;
- доказательство, что Telegram + email hybrid motion реально сокращает CAC и не превращается в ручное агентство;
- появление ICP, где чек стабильно **150-250k ₽/мес** при margin выше 60%. [T1][T2][inference]

## Sources
- [T1] multi-demand endpoint: http://172.18.0.1:9001/multi-demand?keyword=AI%20SDR%20%D0%B0%D0%B2%D1%82%D0%BE%D0%BD%D0%BE%D0%BC%D0%BD%D1%8B%D0%B9%20outbound%20%D0%BF%D1%80%D0%BE%D0%B4%D0%B0%D0%B6%20%D0%B4%D0%BB%D1%8F%20B2B
- [T1] ФНС, реестр МСП: https://rmsp.nalog.ru/statistics.html и https://rmsp.nalog.ru/statistics-proc.json
- [T1] ЦБ РФ, курс USD на 24.04.2026: https://www.cbr.ru/scripts/XML_daily.asp?date_req=24/04/2026
- [T1] AiSDR pricing: https://aisdr.com/pricing/
- [T1] Regie.ai pricing: https://www.regie.ai/pricing
- [T1] Smartlead pricing: https://www.smartlead.ai/pricing
- [T1] hh.ru, SDR: https://hh.ru/search/vacancy?text=SDR&area=113
- [T1] hh.ru, лидогенерация: https://hh.ru/search/vacancy?text=%D0%BB%D0%B8%D0%B4%D0%BE%D0%B3%D0%B5%D0%BD%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D1%8F&area=113
- [T2] Grand View Research, Sales Force Automation market: https://www.grandviewresearch.com/industry-analysis/sales-force-automation-software-market-report
- [T2] TAdviser, CRM-системы рынок России: https://www.tadviser.ru/index.php/%D0%A1%D1%82%D0%B0%D1%82%D1%8C%D1%8F:CRM-%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%8B_(%D1%80%D1%8B%D0%BD%D0%BE%D0%BA_%D0%A0%D0%BE%D1%81%D1%81%D0%B8%D0%B8)
- [T2] Leadhero: https://leadhero.tech/
- [T2] BotB2B: https://botb2b.ru/

Sources: T1=8, T2=4, T3=0. Primary evidence basis: T1.
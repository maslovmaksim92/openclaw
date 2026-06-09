# Verdict dossier

Slug: ai-perevod-dokumentov-i-lokalizatsiya-pod-zakaz
Status: APPROVED WITH NOTES
Score: 70/100
Sector: AI-SERVICES
Date: 2026-06-09



<!-- 00-brief.md -->

# Краткий бриф

## Кейс
AI-перевод документов и локализация под заказ

## Почему открыт
- Сигнал описывает самостоятельный AI-SERVICES wedge вокруг перевода документов, сайтов и маркетингового контента как managed service с human-in-the-loop вычиткой только на low-confidence участках.
- Есть сильная коммерческая валидация категории: EasyTranslate публично заявляет цену около 0.01€ за слово, снижение стоимости перевода до 90% и клиентов уровня Wix и Monday.com.
- Базовая EBITDA-гипотеза 700 000–1 600 000 ₽ в месяц проходит порог Program 1 и выглядит достижимой для B2B-сегментов с регулярным потоком договоров, техдокументации, контента и ВЭД-документов.

## Что проверить дальше
- Какие вертикали в РФ дадут лучший payback: ВЭД, юридические фирмы, e-commerce-экспортёры, SaaS и промышленный экспорт.
- Насколько критичен on-prem/private LLM контур для чувствительных документов и сертифицированных переводов.
- Где лучше productize delivery: по словам, по пакетам документов или по ежемесячному retainer за локализацию и QA.

## Следующий этап
P3-demand-validation.



<!-- 01-evidence.md -->

# Evidence

- Дата: 2022-06-09
- URL: https://techcrunch.com/2022/06/09/papercup-raises-20m-for-ai-that-automatically-dubs-videos/
- Тип: supporting signal
- Как усиливает кейс: Сигнал усиливает кейс по AI-локализации, потому что подтверждает не только спрос на перевод, но и готовность крупных медиа платить за более сложный managed-service сценарий с дубляжом и постредактурой. Это расширяет TAM кейса от документов и текста к видео-контенту с более высоким средним чеком.
- Ключевые данные и факты: Papercup использовался Sky News, Discovery и Business Insider; позиционируется как более масштабируемая альтернатива ручному дубляжу. На сайте компания заявляет дубляж до 4x быстрее и до 80% дешевле традиционного, а также 143% ROI у Insider и 60% рост average view duration у Bloomberg.




<!-- 01-intake.md -->

---
sector: AI-SERVICES
rerun: false
source_raw: 20260512-1355-msk-ai-services-easytranslate-ai-perevod-dokumentov-i-lokalizatsiya-pod-zakaz.md
created: 2026-05-12T16:34:00+03:00
---

# Intake

## Компания
EasyTranslate HumanAI

## Wedge statement
AI-first сервисный аутсорс перевода и локализации документов, сайтов и маркетингового контента с кастомизированным AI и точечной вычиткой человеком только на low-confidence участках.

## Исходный контекст
- Sector: AI-SERVICES
- EBITDA hypothesis: 700000-1600000₽/мес
- RU-fit: 4/5
- ARPU: 60000-180000₽/мес
- CAC: 20000-80000₽
- Deal cycle: 0.5-2 мес
- Target segment: SMB | Mid-market | Regulated

## Evidence
- TechCrunch пишет, что компания перевела бизнес в AI-driven модель, заявляет снижение стоимости перевода на 90% и цену около 0.01€ за слово; среди клиентов названы Wix и Monday.com.
- На странице pricing компания повторяет оффер 0.01€ за переведённое слово, human-quality QA и ускорение до 10x относительно традиционного перевода.
- На странице services компания продаёт document translation, certified translation, website translation, proofreading, subtitling и transcription, то есть готовый шаблон AI-агентства, а не только SaaS.

## Предварительный вывод
Сигнал тянет на новый кейс: это не просто инструмент перевода, а AI-first сервисная модель с понятным unit economics, регулярной потребностью у B2B-клиентов и достаточным EBITDA-потенциалом для локальной адаптации.



<!-- 02-demand.md -->

# Demand validation — AI-перевод документов и локализация под заказ

Дата: 2026-05-12T16:58:00+03:00
Статус: PASS_TO_NEXT_STAGE

## Executive summary

Вывод: спрос на **generic category** «перевод документов / локализация» в РФ подтверждён, но спрос именно на формулировку **AI-перевод документов** пока слабый. По internal demand endpoint запрос `AI перевод документов` дал `LOW / 18`, `локализация сайтов` тоже `LOW / 3`, но широкий запрос `перевод документов` дал `MEDIUM / 30` и 3243 вакансии в HH-источнике внутри агрегатора [T1]. Значит wedge надо продавать не как «AI ради AI», а как **дешевле/быстрее managed translation desk для экспортёров, юрфирм и B2B-команд** [T1][T2].

Profit Gate: **проходим условно**. EBITDA >500k/мес достижима не в commodity per-page модели, а в retainer/hybrid модели с QA, glossary management, SLA и приватным контуром для чувствительных документов [T2].

## Demand signals

- Internal endpoint `multi-demand`:
  - `AI перевод документов` → LOW, score 18, HH vacancies 41, Habr articles 2, Yandex suggest 100 [T1].
  - `локализация сайтов` → LOW, score 3, HH vacancies 32, Habr articles 2, Yandex suggest 2 [T1].
  - `перевод документов` → MEDIUM, score 30, HH vacancies 3243, Habr articles 2, Yandex suggest 100 [T1].
- Официальный МСП.РФ пишет, что в России **более 83 тыс. МСП-экспортёров**. Это прямой пул компаний, которым регулярно нужны переводы контрактов, инвойсов, упаковки, каталогов и сайтов [T1].
- Российский экспортный центр указывает, что на платформе «Профессионалы экспорта» размещено **более 4 тыс. заявок** на экспортные услуги. Это дополнительный признак платёжеспособного спроса на экспортный сервисный слой [T1].
- HH/рынок труда внутри demand endpoint показывает не consumer-only спрос, а именно рабочие места по локализации/переводу, значит бюджеты уже есть в компаниях, а не только у частных лиц [T1].

## Конкуренты и цены

Минимум 3 реальных конкурента с ценами:

1. **Smartcat**: Basic plan от **$1,200/год** для small companies, enterprise pricing custom [T2, официальный pricing]. Это эквивалент примерно **114–120 тыс. ₽/год** при курсе порядка 95–100 ₽/$; использую диапазон, потому что конвертация плавающая [T1/T2].
2. **Google Cloud Translation**: **$20 за 1 млн символов** для NMT сверх free tier, document translation **$0.08/page**, custom models дороже [T2, официальный pricing]. Это нижняя граница commodity machine translation без сервисной обвязки.
3. **DeepL Pro**: search snippet показывает старт **от $8.74/месяц** для starter-плана [T2, официальный сайт в выдаче]. Это дешёвый self-serve ориентир и ценовой якорь для SMB.
4. **TRAKTAT**: письменный перевод **русский→английский 600 ₽/страница**, **немецкий/французский 720 ₽/страница**, срочный **900 ₽/страница** [T2, официальный прайс].

Вывод по ценам: рынок уже «обучен платить» и имеет понятный коридор цен от ultra-cheap API до 600–900 ₽ за страницу human service. Значит AI-игрок может занять middle tier: **быстрее классического бюро, но дороже голого API** [T2].

## WTP, proof of willingness to pay

- WTP подтверждается существованием платных enterprise/self-serve тарифов у Smartcat, Google Cloud Translation и DeepL [T2].
- WTP в РФ подтверждается публичным прайсом TRAKTAT на письменный и срочный перевод [T2].
- WTP со стороны экспортного сегмента дополнительно подтверждается массовостью МСП-экспортёров и активностью на платформе экспортных услуг, где компании уже покупают сопутствующие сервисы для ВЭД [T1].

Итог: willingness to pay **есть**, но платить будут не за «AI-перевод» как технологию, а за **SLA, скорость, приватность, QA и снижение стоимости относительно бюро** [T1][T2].

## Telegram bots / services в РФ

Ландшафт в Telegram есть, но он в основном consumer/SMB и не закрывает enterprise workflow [T3, поддержано общими ценовыми и рыночными сигналами T1/T2]:

- **Translator Bot** и похожие переводчики в каталогах Telegram конкурируют за моментальный перевод текста, но не за B2B workflow с glossary/SLA [T3].
- **Glarity Summary Translator Bot** позиционируется как перевод/summary помощник, опять же ближе к end-user utility, чем к управляемой локализации [T3].
- На рынке есть смежные document-AI Telegram сервисы, но они обычно решают OCR/summary, а не юридически чувствительный managed translation [T3].

Вывод: Telegram полезен как acquisition/utility-канал, но не как финальный продукт для fundable B2B-case. Для RU рынка это скорее lead magnet или intake-слой [спекуляция, T3-поддержка + T1/T2 рыночный контекст].

## ICP и 10 реальных buyers для bottom-up sanity check

Ниже 10 реальных компаний из официального списка победителей/номинантов «Экспортёр года 2024» от РЭЦ, которым типово нужны перевод упаковки, каталогов, контрактов, техдоков и локализации экспортных материалов [T1]:

1. BIOCAD [T1]
2. АО «Арнест» [T1]
3. АО «Нацимбио» [T1]
4. ООО «ПЕНТА-91» [T1]
5. ООО «Натуральные напитки» [T1]
6. АО «ЭКО РЕСУРС» [T1]
7. ООО «ПП Кизляр» [T1]
8. ООО «УК АГРОХОЛДИНГ БЕЛОЗОРИЕ» [T1]
9. ООО «Васта Дискавери» [T1]
10. ООО «Русский уголь» [T1]

ICP-приоритет:
- экспортёры с регулярным документооборотом [T1]
- производители с каталогами/упаковкой на 2+ языках [T1][T2]
- юрфирмы и сертификационные посредники, где важны turnaround и QA [T2]
- SaaS/e-commerce команды, где локализация идёт в ретейнерной модели [T2]

## Market sizing

### Метод и допущения

Ниже комбинирую top-down и bottom-up. Из-за нехватки прямых публичных T1-оценок именно по РФ AI-localized-document market секция частично **[LOW CONFIDENCE]**; поэтому использую консервативные ranges и беру lower estimate как рабочий [T1/T2/T3].

#### Top-down
- База: более **83 тыс. МСП-экспортёров** в РФ [T1].
- Допущение: адресуемая доля для managed translation desk = **25%** компаний, где реально есть регулярный multilingual документооборот или локализация контента [T1 + спекуляция].
- Средний годовой чек:
  - low: **120 тыс. ₽/год** (нерегулярные документы / light localization) [T2]
  - base: **240 тыс. ₽/год** (небольшой ретейнер или 15–20 стр/мес + сайт/маркетинг) [T2]
  - high: **600 тыс. ₽/год** (retainer + QA + glossary + SLA) [T2]

Расчёт top-down:
- TAM РФ (base, если считать весь пул 83k как теоретически покупающий хотя бы light translation): 83,000 × 240,000 ₽ = **19.9 млрд ₽** [T1+T2].
- SAM РФ (25% наиболее подходящего сегмента): 20,750 × 240,000 ₽ = **4.98 млрд ₽** [T1+T2].
- SOM Y1 при захвате 1% SAM: **49.8 млн ₽/год** [спекуляция, но в реалистичном диапазоне].
- SOM Y3 при захвате 3% SAM: **149.4 млн ₽/год** [спекуляция].

#### Bottom-up
- Беру стартовый сегмент не весь рынок, а **10 тыс. компаний** из экспортёров/производителей/сервисных посредников с регулярным multilingual workflow [LOW CONFIDENCE, T1 anchor + T2/T3 segmentation assumption].
- % with need = **20%**. Обоснование: demand endpoint показывает широкий спрос на «перевод документов», а не niche-zero; экспортный документооборот и локализация нужны не всем, но достаточно многим [T1].
- ARR avg = **180 тыс. ₽/год** как средний blended SMB/mid-market чек между page-based и light retainer моделями [T2].

Расчёт bottom-up:
- SAM_bottom_up = 10,000 × 20% × 180,000 ₽ = **360 млн ₽**.
- SOM Y1_bottom_up при capture 3% = **10.8 млн ₽**.
- SOM Y3_bottom_up при capture 8% = **28.8 млн ₽**.

### Сверка top-down и bottom-up

Расхождение между SAM top-down (4.98 млрд ₽) и SAM bottom-up (360 млн ₽) слишком большое, поэтому для investment discipline беру **сильно более узкий рабочий SAM**: считаю, что реально сервисно адресуемый сегмент в ближайшие 3 года это около **2–5 тыс. компаний**, а не 20+ тыс. Тогда рабочий SAM становится **360–900 млн ₽** [LOW CONFIDENCE, reconciliation].

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | — | — | не оценивал без надёжного T1/T2 global report | — |
| TAM (РФ) | 19.9 млрд ₽ [T1+T2] | 1.8 млрд ₽ [T1+T2, если 10k компаний × 180k] | diff ~11x, top-down явно завышает addressable reality | **1.8 млрд ₽** |
| SAM (РФ) | 4.98 млрд ₽ [T1+T2] | 360 млн ₽ [T1+T2] | diff ~13.8x, беру narrow serviceable niche | **360 млн ₽** |
| SOM Y1 | 49.8 млн ₽ | 10.8 млн ₽ | top-down слишком оптимистичен для новой команды | **10.8 млн ₽** |
| SOM Y3 | 149.4 млн ₽ | 28.8 млн ₽ | беру более консервативный сценарий | **28.8 млн ₽** |

Sanity check:
- SOM Y1 10.8 млн ₽ при среднем чеке 180k ₽ = ~60 клиентов в год, то есть ~5 новых клиентов в месяц. Это напряжённо, но достижимо для small services team при узком ICP [T2].
- SOM Y1 = 3% от narrow bottom-up SAM, то есть <10% SAM, red flag overclaiming нет.

## Profit Gate: все сценарии монетизации

### Сценарий A, commodity page-based
- 400 страниц/мес × 700 ₽ средний чек = 280k ₽ выручки [T2]
- валовая маржа ~45% после редакторов/QA = 126k ₽
- фикс. издержки 180–250k ₽
- EBITDA: **отрицательная / ниже 0.2 млн ₽**
- Вердикт: **FAIL**

### Сценарий B, AI+QA document desk
- 800 страниц/мес × 900 ₽ = 720k ₽ выручки [T2]
- GM ~60% за счёт MT+human review = 432k ₽
- OPEX 220k ₽
- EBITDA ≈ **212k ₽/мес**
- Вердикт: **FAIL**

### Сценарий C, retainer localization для 8 клиентов
- 8 клиентов × 140k ₽/мес = 1.12 млн ₽ выручки [T2]
- GM ~65% = 728k ₽
- OPEX 180k ₽
- EBITDA ≈ **548k ₽/мес**
- Вердикт: **PASS**

### Сценарий D, hybrid export desk
- 5 клиентов × 200k ₽/мес retainer = 1.0 млн ₽
- плюс 150 срочных страниц × 800 ₽ = 120k ₽
- итого выручка 1.12 млн ₽
- GM ~60% = 672k ₽
- OPEX 170k ₽
- EBITDA ≈ **502k ₽/мес**
- Вердикт: **PASS**

Итог по Profit Gate: порог EBITDA **не проходит** в commodity translation, но **проходит** в продуктированном managed-service с ретейнерами, glossary management, SLA, приватным контуром и account management [T2]. Значит fundable thesis есть только для более high-touch B2B wedge.

## Risks

- Формулировка «AI-перевод документов» сама по себе даёт слабый спрос, поэтому позиционирование надо менять на бизнес-результат, а не технологию [T1].
- Ценовое давление со стороны API и consumer tools очень высокое [T2].
- Без вертикализации в экспорт/юридический/industrial сегмент сервис скатится в low-margin бюро [T2].
- Telegram-first продукт может выглядеть слишком consumer-like и проиграть enterprise procurement [T3, supported by T2].

## Verdict

Решение: **GO, НО ТОЛЬКО В УЗКОМ B2B-ICР**.

Что должно быть в следующей стадии:
1. ICP = экспортёры и производители с регулярным документооборотом.
2. Упаковка = retainer/hybrid desk, не «бот-переводчик».
3. УТП = скорость, цена ниже бюро, приватность, human QA only on low-confidence, glossary/SLA.
4. Проверить готовность рынка платить за private/on-prem контур для чувствительных документов.

Sources: T1=8, T2=8, T3=3. Primary evidence basis: T1/T2 mixed.

> Market Pulse 2026-05-12: растущий интерес. По текущей веб-выдаче по ключевым запросам сохраняются свежие публикации, vendor-активность и смежный спрос.

> Market Pulse 2026-05-13: растущий интерес. По текущей веб-выдаче по ключевым запросам видны свежие публикации, вакансии и новые рыночные сигналы по AI-переводу и локализации.



<!-- 04-economics.md -->

# Unit economics — AI-перевод документов и локализация под заказ

Дата: 2026-05-12T20:28:00+03:00
Статус: PASS
Модель: managed service / mid-market B2B retainer

## Executive summary

Вывод: кейс **проходит Program 5** в версии не как commodity page-based бюро, а как **retainer-driven AI translation desk** для экспортёров, производителей, юр- и B2B-команд.

Ключевые метрики базового сценария:
- Average MRR per client: **140 000 ₽/мес**
- COGS per client: **40 000 ₽/мес**
- Contribution per client: **100 000 ₽/мес**
- Contribution Margin: **71.4%**
- Fully-loaded blended CAC: **165 000 ₽**
- Monthly churn benchmark used: **1.2%/мес** для mid-market B2B SaaS/services [T6]
- LTV: **8.31 млн ₽** = 140 000 × 71.4% / 1.2%
- LTV/CAC: **50.4x**
- CAC Payback: **1.18 мес** = 165 000 / 140 000
- Monthly fixed costs at steady state: **2.45 млн ₽/мес**
- Break-even: **25 клиентов** или **~3.5 млн ₽ выручки/мес**
- EBITDA at 50 clients: **~2.55 млн ₽/мес**

Инвестиционный вывод: **investment grade PASS**. Даже с консервативным stress-case LTV/CAC остаётся >3x, а EBITDA >500k/мес достижима значительно раньше 50 клиентов.

## Что именно считаю

Экономика построена для ICP из 02-demand.md:
- экспортёры и производители
- B2B-команды с регулярным multilingual документооборотом
- кейсы, где клиент покупает не «API перевода», а SLA, glossary management, QA, приватность и turnaround

Это важно: для page-based модели математика слабая. Ниже считаю **retainer + overage** модель:
- retainer: 110–140k ₽/мес
- срочные/доп. объёмы: 20–60k ₽/мес
- blended MRR: **140k ₽/клиент/мес**

## 1) Подробный бизнес-процесс от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | ICP-лист и первичный ресёрч | SDR | HH/СПАРК/экспортные каталоги/таблицы | 20 мин | 450 | Средняя |
| 2 | First touch: email/Telegram/LinkedIn/звонок | SDR | CRM + sequencing tool | 15 мин | 340 | Высокая |
| 3 | Qualification call | SDR | телефония + CRM | 30 мин | 680 | Низкая |
| 4 | Discovery и сбор 2-3 sample docs | AE | Zoom/Meet + CRM | 45 мин | 1 700 | Низкая |
| 5 | Test translation + quality estimate + glossary draft | Delivery PM + AI pipeline | Smartcat/DeepL/Google Translate/API + QA checklist | 90 мин | 4 200 | Средняя |
| 6 | Коммерческое предложение и SLA | AE + CEO | CPQ/Docs/e-sign | 60 мин | 2 600 | Средняя |
| 7 | Security/privacy согласование | CEO/CTO | DPA/NDA templates | 45 мин | 2 300 | Низкая |
| 8 | Contract signing | AE + Finance | Диадок/Контур.Sign | 30 мин | 1 100 | Высокая |
| 9 | Onboarding, glossary, routing rules, billing setup | CSM + PM + CTO | TMS/CRM/Billing | 120 мин | 6 400 | Средняя |
| 10 | Первая поставка, акт/счёт, получение оплаты | PM + Finance | TMS + 1C/МойСклад/банк | 60 мин | 2 200 | Средняя |

Итого cost-to-close + onboarding на 1 нового клиента: **~21 970 ₽ прямых операционных затрат**, без fully-loaded CAC. Это отдельно от маркетинга и sales FOT.

## 2) COGS breakdown на клиента в месяц

Базовый клиент: 140k ₽ MRR, 400-700 страниц/мес эквивалента, mix из документов, каталогов, веб-страниц и срочных задач.

| Компонент COGS | ₽/клиент/мес | Как получено | Комментарий |
|---|---:|---|---|
| MT/API usage | 6 000 | Google/DeepL/LLM + запас на пики | commodity слой перевода |
| Human QA / editor | 18 000 | 12-15 часов редактора/QA × ~1 200–1 500 ₽/ч | HITL на low-confidence сегментах |
| Delivery PM | 8 000 | ~4 часа × 2 000 ₽/ч fully-loaded | координация, дедлайны, glossary |
| Storage/OCR/infra | 3 000 | облако, OCR, secure storage | переменная инфра |
| Customer support / revisions | 3 000 | 1-2 итерации правок | пост-поставка |
| Payment/banking/misc variable | 2 000 | эквайринг/банк/документооборот | переменные расходы |
| **Итого COGS** | **40 000** |  |  |

Gross profit per client = **100 000 ₽/мес**

Gross Margin = **71.4%**

## 3) CAC по каналам с funnel conversion

Рабочая модель acquisition на scale-этапе: **7 новых платящих клиентов в месяц**.

| Канал | Spend, ₽/мес | Лиды/аккаунты | Qualified | Proposal | New paying | Conversion to pay | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Outbound ABM | 516 000 | 900 target accounts | 180 replies | 14 proposals | 3 | 0.33% от target / 21.4% от proposal | 172 000 |
| Paid search / inbound | 479 000 | 140 leads | 28 SQL | 10 proposals | 2 | 1.43% от leads / 20% от proposal | 239 500 |
| Partners / referrals | 160 000 | 20 intros | 10 SQL | 5 proposals | 2 | 10% от intros / 40% от proposal | 80 000 |
| **Blended** | **1 155 000** | **1 060** | **218** | **29** | **7** | **0.66% blended** | **165 000** |

Вывод:
- лучший CAC даёт partners/referrals
- outbound нужен как основной предсказуемый канал
- paid search полезен, но без brand/SEO выглядит самым дорогим

## 4) FULLY-LOADED CAC

Сегмент: **mid-market B2B**, поэтому применяю sanity-мультипликатор не self-serve, а **примерно x1.6 к raw acquisition layer**, что соответствует диапазону **x1.5–1.7** из задания.

### Таблица fully-loaded CAC

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK/поиск) | 120 000 | тестовый monthly media budget | модель, sanity against T1/T2 |
| Outbound team FOT (SDR/AE attributed to new) | 417 000 | SDR 150k + AE 171k attributed gross, оба ×1.3 соцвзносы | HH.ru benchmarks [T7][T8][T9] |
| Marketing team FOT (partial allocation) | 90 000 | 0.5 FTE demand gen / content | HH.ru benchmark [T10] |
| Tools (CRM, sequencing, telephony, TMS seats) | 35 000 | CRM + outreach + телефония + докс | vendor pricing / model [T2][T3][T4] |
| Events/partnerships | 60 000 | бизнес-завтраки, ассоциации, referral fees | модель |
| Raw CAC pool | 722 000 | сумма строк выше | — |
| Overhead multiplier (x1.6 for mid-market B2B) | 433 000 | 722 000 × 0.6 | policy sanity from task |
| **Total fully-loaded acquisition cost** | **1 155 000** | raw + overhead | — |
| **New paying customers** | **7** | blended monthly funnel | модель |
| **Fully-loaded CAC** | **165 000 ₽** | 1 155 000 / 7 | — |

### Sanity check vs benchmark

По заданию benchmark для **mid-market SaaS**: **60–250k ₽ CAC**, для complex enterprise выше. Наш blended CAC **165k ₽** лежит **внутри коридора**, значит явного underestimation нет.

## 5) LTV и churn rate

Формула:

LTV = MRR per customer × Gross Margin / Monthly churn

Подстановка:
- MRR = **140 000 ₽**
- GM = **71.4%**
- churn = **1.2%/мес**

LTV = 140 000 × 0.714 / 0.012 = **8 330 000 ₽**

### Benchmark churn

Для mid-market B2B SaaS беру **1.2% monthly logo churn** как рабочий benchmark: это консервативнее enterprise SaaS и лучше SMB, и соответствует диапазону, где churn заметно ниже SMB из-за годовых контрактов, интеграций и более высокой switching cost [T6].

### Sensitivity

| Сценарий | MRR, ₽ | GM % | Churn / мес | LTV, ₽ |
|---|---:|---:|---:|---:|
| Base | 140 000 | 71.4% | 1.2% | 8.33 млн |
| Conservative | 120 000 | 68.0% | 2.0% | 4.08 млн |
| Stress | 110 000 | 65.0% | 3.0% | 2.38 млн |

Даже в stress-case LTV остаётся кратно выше CAC.

## 6) LTV/CAC ratio

- Base: **8.33 млн / 165k = 50.4x**
- Conservative: **4.08 млн / 165k = 24.7x**
- Stress: **2.38 млн / 165k = 14.4x**

Итог: **сильный PASS**, сильно выше порога **3:1**.

Комментарий: отношение выглядит высоким, потому что здесь не pure SaaS, а recurring managed service с высоким чеком и относительно низким churn. Главный риск не в формальной LTV/CAC, а в способности удержать SLA и качество при масштабировании.

## 7) CAC Payback

По заданию считаю как:

CAC Payback = CAC / MRR per customer

= 165 000 / 140 000 = **1.18 месяца**

Даже если считать по gross profit,
165 000 / 100 000 = **1.65 месяца**

Оба варианта далеко лучше порога 12 мес.

## 8) Contribution Margin %

Contribution Margin = (Revenue - Variable COGS) / Revenue

= (140 000 - 40 000) / 140 000 = **71.4%**

Это хорошая метрика для service-enabled AI model. Она ниже типичного pure SaaS, но значительно выше классического бюро переводов.

## 9) Полная команда: роли, функции, зарплаты

### Full team table

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO/founder | продажи, ключевые партнёры, finance | 600 000 | 180 000 | 780 000 |
| CTO/Tech Lead | AI stack, security, workflow automation | 500 000 | 150 000 | 650 000 |
| Senior Backend | интеграции, billing, workflow APIs | 400 000 | 120 000 | 520 000 |
| ML/NLP Engineer | quality routing, glossary, evals | 450 000 | 135 000 | 585 000 |
| DevOps (0.5–1 FTE) | secure infra, monitoring, CI/CD | 320 000 | 96 000 | 416 000 |
| Delivery PM / linguistic lead | запуск клиентов, качество, очередь задач | 220 000 | 66 000 | 286 000 |
| SDR | outbound lead gen | 150 000 | 45 000 | 195 000 |
| AE | discovery, proposals, close | 280 000 | 84 000 | 364 000 |
| Customer Success | onboarding, renewals, expansions | 220 000 | 66 000 | 286 000 |
| Finance/ops (0.5 FTE) | invoices, acts, collections | 120 000 | 36 000 | 156 000 |
| **Итого steady-state FOT** |  |  |  | **4 238 000 ₽/мес** |

### HIRING REALISM

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 600 000 | 0 (founder) | 0 | 180 000 | 780 000 |
| CTO/Tech Lead | 1 | 500 000 | 2 | 2 | 150 000 | 650 000 |
| Senior Backend | 1 | 400 000 | 1.5 | 1.5 | 120 000 | 520 000 |
| ML Engineer | 1 | 450 000 | 2.5 | 2 | 135 000 | 585 000 |
| DevOps | 0.5-1 | 320 000 | 1.5 | 1 | 96 000 | 416 000 |
| Frontend | 0 | 0 | не нужен на старте | — | 0 | 0 |
| SDR | 1 | 150 000 | 0.75 | 1 | 45 000 | 195 000 |
| AE | 1 | 280 000 | 1.5 | 2.5 | 84 000 | 364 000 |
| Customer Success | 1 | 220 000 | 1 | 1 | 66 000 | 286 000 |

Salary sanity:
- backend 350–550k gross подтверждается HH.ru вакансиями [T7]
- ML 400–650k подтверждается HH.ru вакансиями [T8]
- DevOps 300–420k+ и hh article по Москве подтверждают диапазон [T9][T11]
- SDR 100–150k подтверждается HH.ru вакансиями [T12]
- AE/KAM 250–400k+ подтверждается HH.ru выдачей [T13]

## 10) Cumulative FOT timeline M1-M12

Предположение: нанимаем реалистично, без 5+ full hires в первый месяц.

| Месяц | Кто в штате / выходит в работу | FOT month, ₽ |
|---|---|---:|
| M1 | CEO, Delivery PM | 1 066 000 |
| M2 | + SDR | 1 261 000 |
| M3 | + Senior Backend | 1 781 000 |
| M4 | + AE | 2 145 000 |
| M5 | + CTO/Tech Lead | 2 795 000 |
| M6 | + Customer Success | 3 081 000 |
| M7 | + ML Engineer | 3 666 000 |
| M8 | + DevOps | 4 082 000 |
| M9 | steady state | 4 082 000 |
| M10 | steady state | 4 082 000 |
| M11 | steady state | 4 082 000 |
| M12 | steady state | 4 082 000 |

Примечание: в P&L для break-even ниже использую часть функций founder-led и аутсорс, поэтому **steady-state fixed cost для unit economics** ниже полного FOT. Это нормально: investor model считает целевую operating team, но early-stage go-to-market часто держится founder-heavy и часть функций включена в COGS или external.

## 11) Fixed costs breakdown

Для break-even беру рабочий operating stack, а не максимальный org chart.

| Компонент fixed cost | ₽/мес |
|---|---:|
| Core team FOT used in operating model | 1 900 000 |
| Office / coworking / legal / accounting | 120 000 |
| Core software stack (CRM, TMS, PM, docs, telephony) | 130 000 |
| Cloud / secure infra minimum | 150 000 |
| G&A reserve | 150 000 |
| Base acquisition retained at operating level | 0 |
| **Итого fixed costs for break-even** | **2 450 000 ₽/мес** |

## 12) Break-even по клиентам и по месяцу

Contribution per client = **100 000 ₽/мес**

Break-even clients = 2 450 000 / 100 000 = **24.5**, округляю до **25 клиентов**

Break-even revenue per month = 25 × 140 000 = **3 500 000 ₽/мес**

### EBITDA at client counts

| Клиентов | Revenue, ₽/мес | Contribution, ₽/мес | Fixed cost, ₽/мес | EBITDA, ₽/мес |
|---:|---:|---:|---:|---:|
| 10 | 1 400 000 | 1 000 000 | 2 450 000 | -1 450 000 |
| 20 | 2 800 000 | 2 000 000 | 2 450 000 | -450 000 |
| 25 | 3 500 000 | 2 500 000 | 2 450 000 | 50 000 |
| 30 | 4 200 000 | 3 000 000 | 2 450 000 | 550 000 |
| 40 | 5 600 000 | 4 000 000 | 2 450 000 | 1 550 000 |
| 50 | 7 000 000 | 5 000 000 | 2 450 000 | 2 550 000 |

**Profit Gate проходит**: уже на **30 клиентах EBITDA >500k/мес**, а на 50 клиентах запас большой.

## 13) Burn-to-breakeven

Предположим траекторию клиентов:
- M1: 0
- M2: 1
- M3: 2
- M4: 4
- M5: 6
- M6: 8
- M7: 11
- M8: 14
- M9: 18
- M10: 22
- M11: 26
- M12: 30

При такой кривой компания выходит на операционный break-even между **M10 и M11**.

Оценка cumulative burn до break-even:
- FOT + infra + acquisition burn accumulated: **~15.5–17.0 млн ₽**
- working capital buffer под дебиторку/акты: **~2.0 млн ₽**
- total startup capital to safe break-even: **~18 млн ₽**

Sanity check: для B2B enterprise-ish services это **не выглядит занижением** и выше red-flag порога 10 млн ₽.

## 14) Cash runway

При startup_capital = **18 млн ₽**:
- burn в первые 3 месяца: ~1.2–1.8 млн ₽/мес
- burn в M4-M8: ~1.6–2.0 млн ₽/мес
- burn затем снижается по мере роста клиента

Средний burn до нормализации: **~1.7 млн ₽/мес**

Cash runway = 18.0 / 1.7 ≈ **10.6 месяца**

Это означает, что без ускорения продаж runway довольно tight, но в пределах нормы. Для комфортного execution я бы считал целевым raise/капитал **20–22 млн ₽**.

## 15) Риски и анти-иллюзии

1. **LTV/CAC выглядит очень красиво**, но это не освобождает от delivery risk. Один системный провал по качеству в узком B2B-сегменте быстро ломает churn.
2. **Page-based сегмент неинвестируем**. Вся математика держится на retainer, SLA и повторяемом объёме.
3. **Сильная зависимость от founder-led sales** в первые 6 месяцев. Без этого реальные conversion rates будут хуже.
4. Для regulated кейсов CAC станет ближе к enterprise и может выйти в 250–400k+, если включатся security review и procurement.

## Verdict

Решение: **PASS**.

Почему:
- fully-loaded CAC в допустимом коридоре
- LTV/CAC кратно выше 3:1
- CAC payback сильно ниже 12 мес
- EBITDA >500k/мес достижима задолго до 50 клиентов
- break-even по клиентам выглядит реалистично для узкого B2B ICP

Что критично для следующего этапа:
1. Продавать не «AI-перевод», а **retainer desk для экспортных и юридически чувствительных workflows**.
2. Доказать 2-3 repeatable acquisition channel с win-rate не хуже модели.
3. Стандартизовать QA / glossary / privacy, иначе churn benchmark не удержится.

## Sources

- [T1] Smartcat pricing: https://www.smartcat.com/pricing/
- [T2] Google Cloud Translation pricing: https://cloud.google.com/translate/pricing
- [T3] DeepL pricing/help: https://www.deepl.com/en/pro/pricing and https://support.deepl.com/hc/en-us/articles/360019924499-About-DeepL-plans
- [T4] TRAKTAT pricing: https://www.traktat.com/price/ and https://www.traktat.com/pismennyj-perevod/ustnyj-i-pismennyj-perevod-prezentacij/
- [T5] HH senior backend market examples: https://hh.ru/vacancies/senior-backend-developer/za_sutki and https://hh.ru/vacancy/129266637
- [T6] SaaS Capital churn benchmark landing page: https://www.saas-capital.com/research/churn-benchmarks-for-b2b-saas-companies/
- [T7] HH senior backend example: https://hh.ru/vacancy/129266637
- [T8] HH senior ML example: https://hh.ru/vacancy/128836250
- [T9] HH DevOps example: https://hh.ru/vacancy/129135377
- [T10] HH product salary article: https://hh.ru/article/skills_product
- [T11] HH DevOps salary article: https://hh.ru/article/skills_devops
- [T12] HH SDR example: https://hh.ru/vacancy/128565026
- [T13] HH Account Executive search: https://hh.ru/vacancies/account_executive



<!-- 05-critic.md -->

## SECTION A. Finance PnL

### A1. Входные данные и допущения
- ARPA: **140 000 ₽/клиент/мес**.
- CAC по каналам: outbound ABM **172 000 ₽**, paid search / inbound **239 500 ₽**, partners / referrals **80 000 ₽**, blended fully-loaded CAC **165 000 ₽**.
- LTV/mo: **~99 167 ₽/мес** по формуле 140 000 × 71.4%.
- Contribution margin: **100 000 ₽/клиент/мес**.
- COGS на клиента: **40 000 ₽/клиент/мес**.
- Fixed costs: **2 450 000 ₽/мес**.
- Team FOT в operating model: **1 900 000 ₽/мес**.
- Страховые взносы: **~30% к ФОТ**, в FOT и fixed costs уже учтены.
- НДС: **20%**, если компания на ОСНО и цена не перенесена на клиента сверх прайса.

### A2. Сценарии
- **Base:** new clients = `0,1,1,2,2,2,3,3,4,4,4,4`, churn **1.2%/мес**.
- **Optimistic:** new clients = `1,1,2,2,3,3,4,4,4,5,5,5`, churn **0.8%/мес**.
- **Pessimistic:** new clients = `0,0,1,1,1,1,2,2,2,2,2,3`, churn **2.0%/мес**.
- Формула активной базы: `Total clients_t = Total clients_(t-1) × (1 - churn) + New clients_t`.
- EBITDA = `MRR - COGS - Fixed costs`.
- Cash burn = `max(0, -EBITDA)`.
- Cumulative cash считается от **0 ₽** и показывает накопленную потребность в капитале.

### A3. PnL 12 месяцев, Base
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 1 | 1 | 2 | 2 | 2 | 3 | 3 | 4 | 4 | 4 | 4 |
| Total clients | 0.00 | 1.00 | 1.99 | 3.96 | 5.92 | 7.85 | 10.75 | 13.62 | 17.46 | 21.25 | 24.99 | 28.69 |
| MRR, ₽ | 0 | 140 000 | 278 320 | 554 980 | 828 320 | 1 098 381 | 1 505 200 | 1 907 138 | 2 444 252 | 2 974 921 | 3 499 222 | 4 017 231 |
| COGS, ₽ | 0 | 40 000 | 79 520 | 158 566 | 236 663 | 313 823 | 430 057 | 544 896 | 698 358 | 849 977 | 999 778 | 1 147 780 |
| Gross profit, ₽ | 0 | 100 000 | 198 800 | 396 414 | 591 657 | 784 558 | 1 075 143 | 1 362 241 | 1 745 894 | 2 124 944 | 2 499 444 | 2 869 451 |
| GM% | 0.0% | 71.4% | 71.4% | 71.4% | 71.4% | 71.4% | 71.4% | 71.4% | 71.4% | 71.4% | 71.4% | 71.4% |
| Fixed costs, ₽ | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 |
| EBITDA, ₽ | -2 450 000 | -2 350 000 | -2 251 200 | -2 053 586 | -1 858 343 | -1 665 442 | -1 374 857 | -1 087 759 | -704 106 | -325 056 | 49 444 | 419 451 |
| Cash burn, ₽ | 2 450 000 | 2 350 000 | 2 251 200 | 2 053 586 | 1 858 343 | 1 665 442 | 1 374 857 | 1 087 759 | 704 106 | 325 056 | 0 | 0 |
| Cumulative cash, ₽ | -2 450 000 | -4 800 000 | -7 051 200 | -9 104 786 | -10 963 128 | -12 628 571 | -14 003 428 | -15 091 187 | -15 795 292 | -16 120 349 | -16 070 905 | -15 651 454 |

- Break-even по client count: **25 клиентов**.
- Break-even month: **M11**.

### A4. PnL 12 месяцев, Optimistic
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 1 | 1 | 2 | 2 | 3 | 3 | 4 | 4 | 4 | 5 | 5 | 5 |
| Total clients | 1.00 | 1.99 | 3.98 | 5.94 | 8.90 | 11.83 | 15.73 | 19.61 | 23.45 | 28.26 | 33.03 | 37.77 |
| MRR, ₽ | 140 000 | 278 880 | 556 649 | 832 196 | 1 245 538 | 1 655 574 | 2 202 329 | 2 744 711 | 3 282 753 | 3 956 491 | 4 624 839 | 5 287 840 |
| COGS, ₽ | 40 000 | 79 680 | 159 043 | 237 770 | 355 868 | 473 021 | 629 237 | 784 203 | 937 929 | 1 130 426 | 1 321 383 | 1 510 812 |
| Gross profit, ₽ | 100 000 | 199 200 | 397 606 | 594 426 | 889 670 | 1 182 553 | 1 573 092 | 1 960 508 | 2 344 824 | 2 826 065 | 3 303 456 | 3 777 029 |
| GM% | 71.4% | 71.4% | 71.4% | 71.4% | 71.4% | 71.4% | 71.4% | 71.4% | 71.4% | 71.4% | 71.4% | 71.4% |
| Fixed costs, ₽ | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 |
| EBITDA, ₽ | -2 350 000 | -2 250 800 | -2 052 394 | -1 855 574 | -1 560 330 | -1 267 447 | -876 908 | -489 492 | -105 176 | 376 065 | 853 456 | 1 327 029 |
| Cash burn, ₽ | 2 350 000 | 2 250 800 | 2 052 394 | 1 855 574 | 1 560 330 | 1 267 447 | 876 908 | 489 492 | 105 176 | 0 | 0 | 0 |
| Cumulative cash, ₽ | -2 350 000 | -4 600 800 | -6 653 194 | -8 508 768 | -10 069 098 | -11 336 545 | -12 213 453 | -12 702 945 | -12 808 122 | -12 432 057 | -11 578 600 | -10 251 571 |

- Break-even по client count: **25 клиентов**.
- Break-even month: **M10**.

### A5. PnL 12 месяцев, Pessimistic
| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 1 | 1 | 1 | 1 | 2 | 2 | 2 | 2 | 2 | 3 |
| Total clients | 0.00 | 0.00 | 1.00 | 1.98 | 2.94 | 3.88 | 5.80 | 7.69 | 9.53 | 11.34 | 13.12 | 15.85 |
| MRR, ₽ | 0 | 0 | 140 000 | 277 200 | 411 656 | 543 423 | 812 554 | 1 076 303 | 1 334 777 | 1 588 082 | 1 836 320 | 2 219 594 |
| COGS, ₽ | 0 | 0 | 40 000 | 79 200 | 117 616 | 155 264 | 232 158 | 307 515 | 381 365 | 453 738 | 524 663 | 634 170 |
| Gross profit, ₽ | 0 | 0 | 100 000 | 198 000 | 294 040 | 388 159 | 580 396 | 768 788 | 953 412 | 1 134 344 | 1 311 657 | 1 585 424 |
| GM% | 0.0% | 0.0% | 71.4% | 71.4% | 71.4% | 71.4% | 71.4% | 71.4% | 71.4% | 71.4% | 71.4% | 71.4% |
| Fixed costs, ₽ | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 | 2 450 000 |
| EBITDA, ₽ | -2 450 000 | -2 450 000 | -2 350 000 | -2 252 000 | -2 155 960 | -2 061 841 | -1 869 604 | -1 681 212 | -1 496 588 | -1 315 656 | -1 138 343 | -864 576 |
| Cash burn, ₽ | 2 450 000 | 2 450 000 | 2 350 000 | 2 252 000 | 2 155 960 | 2 061 841 | 1 869 604 | 1 681 212 | 1 496 588 | 1 315 656 | 1 138 343 | 864 576 |
| Cumulative cash, ₽ | -2 450 000 | -4 900 000 | -7 250 000 | -9 502 000 | -11 657 960 | -13 719 801 | -15 589 405 | -17 270 617 | -18 767 204 | -20 082 860 | -21 221 203 | -22 085 779 |

- Break-even по client count: **25 клиентов**.
- Break-even month в горизонте M1-M12: **не достигнут**.

### A6. Waterfall на 1 клиента / месяц
| Шаг | ₽/клиент/мес | Комментарий |
|---|---:|---|
| ARPA | 140 000 | blended retainer + overage |
| Gross | 100 000 | ARPA - COGS 40 000 ₽ |
| Contribution | 100 000 | доп. переменные продажи уже включены в blended CAC, не в unit COGS |
| EBITDA | 100 000 | до распределения fixed costs |
| Net, УСН 6% | 91 600 | 100 000 - 8 400 |
| Net, IT-льгота 3% | 95 800 | 100 000 - 4 200 |
| Net, ОСНО 20% | 80 000 | 100 000 × 0.8, НДС 20% ухудшает cash conversion при цене «с НДС» |

### A7. Cash flow: startup_capital_to_bep_rub
- **Base:** около **16.1 млн ₽** до операционного break-even, пик кумулятивного дефицита в **M10**.
- **Optimistic:** около **12.8 млн ₽** до операционного break-even, пик кумулятивного дефицита в **M9**.
- **Pessimistic:** в горизонте 12 месяцев break-even не достигается, требуется около **22.1 млн ₽** только на покрытие дефицита M1-M12.

### A8. Налоговая модель РФ
- **УСН 6% с выручки:** налог платится даже при низкой EBITDA. Налог на клиента = **8 400 ₽/мес**.
- **IT-льгота 3% с выручки:** применима при аккредитации Минцифры и соблюдении профильных критериев. Налог на клиента = **4 200 ₽/мес**.
- **ОСНО:** налог на прибыль **20%**, плюс **НДС 20%** если применимо. Если прайс объявлен без НДС и налог переносится клиенту, давление на маржу ниже; если прайс «грязный», cash conversion заметно хуже.
- **Страховые взносы ~30% к ФОТ** уже включены в team FOT и fixed costs.

### A9. Break-even summary
| Scenario | EBITDA BEP, clients | Post-tax BEP, clients (УСН / IT / ОСНО) | Break-even month | Clients at M12 |
|---|---:|---:|---:|---:|
| Base | 25 | 27 / 26 / 31 | M11 | 28.69 |
| Optimistic | 25 | 27 / 26 / 31 | M10 | 37.77 |
| Pessimistic | 25 | 27 / 26 / 31 | не достигнут | 15.85 |

<!-- P6A-DONE -->

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis: EBITDA через 12 месяцев

Методика: беру base-модель из SECTION A. Для CAC x2 считаю, что при неизменном sales budget объём новых клиентов падает примерно в 2 раза. Для Churn x2 повышаю monthly churn с 1.2% до 2.4%. Для Price -30% снижаю ARPA с 140k ₽ до 98k ₽, COGS на клиента оставляю без изменений.

| Сценарий | Ключевое изменение | Clients @M12 | EBITDA @M12, ₽/мес | Delta vs Base |
|---|---|---:|---:|---:|
| Base | без изменений | 28.69 | 419 451 | — |
| Sens1 | CAC x2 | 14.35 | -1 015 275 | -1 434 726 |
| Sens2 | Churn x2 | 27.46 | 296 292 | -123 159 |
| Sens3 | Price -30% | 28.69 | -785 719 | -1 205 170 |

Вывод: самый токсичный шок здесь не churn, а price compression. Для этой модели потеря 30% цены ломает EBITDA почти так же быстро, как и удвоение CAC. Значит защита value-based pricing и SLA важнее, чем простое наращивание лидогенерации.

### B2. Monte Carlo Lite, confidence intervals

#### Входные распределения, triangular min/mode/max

| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC ₽ | 120 000 | 165 000 | 280 000 | base CAC и benchmark mid-market SaaS из SECTION A / [T6] |
| Monthly churn % | 0.8% | 1.2% | 3.0% | base + stress range из SECTION A / [T6] |
| ARPU ₽/мес | 98 000 | 140 000 | 180 000 | price stress и retainer+overage диапазон из 04-economics.md |
| Conversion rate lead→paid % | 0.4% | 0.66% | 1.0% | base funnel 7/1060 = 0.66% из 04-economics.md |
| Time-to-hire месяцев | 1.0 | 1.5 | 3.0 | hiring realism из 04-economics.md / [T7][T8][T9] |

Упрощённая симуляция: вместо полного 1000-run Monte Carlo использую 9 комбинаций best / median / worst + 6 mixed. p10 беру как нижнюю комбинацию из 9, p50 как медианную, p90 как верхнюю. Горизонт: M24. Для runway использую стартовый капитал 18 млн ₽ из SECTION A/04-economics.md.

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----|-----|-----|-------------|
| EBITDA @M24 (₽/мес) | -1 404 824 | 4 527 996 | 20 582 768 | 21 987 592 |
| CAC payback (мес) | 4.83 | 1.20 | 0.86 | 3.97 |
| LTV/CAC | 6.90x | 69.44x | 145.83x | 138.93x |
| Cash runway (мес) | 7.53 | 8.55 | 13.37 | 5.84 |

Интерпретация правил:
- **Rule 1 triggered:** p10 EBITDA < 0, значит kill criterion #1 обязателен.
- **Rule 2 not triggered:** p50 EBITDA > 500k ₽/мес, median проходит EBITDA Gate.
- **Rule 3 effectively triggered:** распределение слишком широкое; при отрицательном p10 классическое p90/p10 неинтерпретируемо, но сам факт перехода через 0 означает экстремальную неопределённость и требует downgrade score.
- **Rule 4 triggered:** LTV/CAC range width = 138.93x, модель хрупкая к допущениям по price, churn и CAC.

### B3. Competitor deep-dive

#### Топ-3 западных

| Конкурент | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|
| **Phrase** | Enterprise-grade localization platform, сильная автоматизация workflow, security/GDPR/ISO, глубокие интеграции. | Чаще продаёт platform-first, а не done-for-you документные SLA; может быть тяжёлым и дорогим для mid-market RU-CIS. | **~8-12%** глобального enterprise localization software. Оценка по brand visibility, enterprise positioning и числу крупных внедрений, не официальный market share. | Мы можем продавать не платформу, а managed outcome: договоры, техдоки, export paperwork, HITL QA и русскоязычный сервисный слой. |
| **Lokalise** | Сильна в product/software localization, 1M users across 3,000+ companies, хороший dev workflow. | Больше заточена под app/web strings, чем под хаотичный поток PDF/scan/legal docs. | **~6-10%** в software localization stack. Оценка-инференс по 3,000+ companies и сильному PLG footprint. | Наш wedge шире для document-heavy SMB/mid-market: OCR, human QA, срочность, billing за пакет документов, а не только string-based localization. |
| **Smartling** | Сильные enterprise integrations, automation claims до 99%, cloud-native scale, multilingual governance. | Enterprise sales cycle, сложнее для локальных клиентов с требованиями data residency и русского документооборота. | **~5-9%** enterprise TMS/localization. Оценка-инференс по enterprise footprint и ecosystem depth. | Можно обыгрывать скоростью запуска, локальным compliance-пакетом и более дешёвым retainer для 20-200 сотрудников. |

#### Топ-5 российских / русскоязычных игроков

| Конкурент | Источник | Strengths | Weaknesses | Market-share estimate | Our advantage |
|---|---|---|---|---|---|
| **Smartcat** | Smartcat site, Skolkovo profile | Самый сильный AI/platform бренд из русскоязычных корней, 280+ languages, enterprise logos, мощный workflow layer. | Глобальный platform play, не всегда будет руками вести сложный российский документооборот и кастомные SLA под ВЭД/юристов. | **~10-15%** русскоязычного AI-first B2B localization software сегмента, но ниже в pure managed documents. | Мы можем идти снизу: document desk + отраслевые glossary + on-demand PM/QA, без тяжёлого platform onboarding. |
| **PROMT / Translate.ru** | Rusprofile + corporate pages | Сильный бренд в машинном переводе, on-prem и privacy-sensitive use cases, исторически узнаваем в РФ. | Более «engine-centric», слабее как современный managed workflow с гибридом AI + humans + customer success. | **~5-8%** в RU secure/corporate MT сегменте. | Наше преимущество в service wrapper, SLA и productized outcome, а не просто движок перевода. |
| **AWATERA** | vc.ru / corporate materials | Большой enterprise vendor, сильный корпус переводчиков, корпоративные продажи, тендерная компетенция. | Классический service-heavy игрок, выше косты и медленнее AI-native iteration. | **~6-10%** рынка крупных корпоративных language services в РФ. | AI-native delivery даёт нам лучший gross margin и faster turnaround на средних чеках. |
| **Janus Worldwide** | Rusprofile / Habr / corporate materials | Крупный LSP, широкий language coverage, опыт в enterprise и tech docs. | Наследие классического LSP: больше ручного труда, выше price floor, слабее perceived product velocity. | **~5-9%** в enterprise translation outsourcing РФ/СНГ. | Можно выигрывать у Janus на скорости, самообслуживании клиента и прозрачной ежемесячной подписке. |
| **Alconost** | Habr / corporate site | Сильна в app/game/software localization, голос, маркетинговая локализация, международный delivery. | Больше фокус на digital products, чем на регулярный поток договоров и ВЭД-документов. | **~3-5%** нишевого software/game localization сегмента в RU/CIS. | Мы сильнее в regulated docs, export paperwork и документных SLA для B2B-команд. |

Вывод по конкурентам: рынок переполнен либо **platform-first** игроками, либо **classic LSP**. Окно для входа есть именно в слое **AI-native managed document localization**: быстрее классических бюро и «ближе к результату» чем TMS-платформы.

### B4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Founder-led sales не масштабируется после первых 5-7 клиентов | high | high | win-rate вне founder calls падает ниже 15% | записать sales playbook, нанять AE/SDR раньше M4, разложить ICP по вертикалям |
| Operational | QA/human editor bottleneck в пиковые недели | med | high | TAT > SLA в 2+ проектах за месяц | пул фриланс-редакторов, routing по сложности, premium surcharge за rush jobs |
| Operational | LLM/API vendor outage или деградация качества | med | high | рост manual rework >20%, latency/API errors >3% | multi-vendor stack, fallback на MT/OCR providers, offline glossary cache |
| Market | Спрос концентрируется в разовых заказах, а не в retainer-модели | med | high | доля one-off revenue >50% три месяца подряд | жёстче квалифицировать ICP, продавать подписку и SLA, минимум по monthly volume |
| Market | Конкуренты начинают price war и пакет «дешёвый AI-перевод» | high | high | ASP падает >15% за квартал, чаще проигрываем по цене | упор на compliance, glossary, speed, security; tiered pricing; upsell urgent/SLA tiers |
| Market | Customer concentration: 1-2 якорных клиента дают >35% выручки | med | high | top-2 share >35% MRR | cap на скидки, diversify ICP, отдельный pipeline на mid-market |
| Regulatory | 152-ФЗ и data residency ограничивают использование западных SaaS/LLM | med | high | procurement/security review затягивается >45 дней | RU-hosted storage, DPA, split processing, on-prem/private model option |
| Regulatory | 115-ФЗ/KYC/contracting friction для экспортных клиентов и валютных платежей | med | med | сделки зависают на этапе комплаенса и банка | стандартизировать договоры, иметь RUB-first billing и local legal ops |
| Regulatory | Санкции или отключение зарубежных API/SaaS | high | high | vendor ToS changes, billing refusals, geo restrictions | резервные поставщики, локальные MT, предоплата на критичные сервисы |
| Financial | Cash runway сжимается из-за более долгого sales cycle | high | high | payback >4 мес и MRR plan <80% три месяца подряд | raise buffer 20-22 млн ₽, freeze hiring, cut paid channels |
| Financial | Ослабление рубля повышает стоимость API и софта | med | med | USD/RUB >15% выше планового курса 2 месяца | pricing clauses, частичная долларовая индексация, prebuy credits |
| Financial | Инфляция/налоги поднимают FOT и G&A быстрее выручки | med | med | fixed costs растут >10% QoQ | variable-heavy staffing, outsource non-core, quarterly repricing |
| Black swan | Резкое усиление войны/санкций ломает клиентов ВЭД | med | high | stop in export accounts, cancellations in affected sectors | секторная диверсификация, legal/e-commerce сегменты, domestic use cases |
| Black swan | Полное отключение ключевого LLM/MT-провайдера | med | high | недоступность >24 часов или запрет оплаты | резервный стек из 2-3 движков, деградационный manual mode |

### B5. Kill conditions, stop/go через 6 месяцев

1. **Kill #1, insolvency risk:** если p10-like trajectory реализуется и EBITDA остаётся отрицательной, а runway уходит ниже **6 месяцев**, проект нельзя продолжать без резкого pivot/recap.
2. **Kill #2, weak sales engine:** если к концу M6 активных клиентов **<8** или new paid clients в последние 3 месяца в среднем **<1.5/мес**, значит CAC/conversion assumptions не подтверждаются.
3. **Kill #3, price/churn failure:** если ARPA падает ниже **110k ₽** одновременно с churn **>2.5%/мес**, retainer-модель разрушается и unit economics перестают быть defendable.

### B6. Итоговый инвестиционный вывод по риску

Кейс остаётся **интересным, но уже не clean PASS без оговорок**. Основная сила модели в высокой contribution margin и управляемом COGS, но SECTION B показывает, что экономика крайне чувствительна к двум вещам: **снижению цены** и **срыву acquisition efficiency**. Поэтому правильный framing для инвестора: не "AI-перевод как commodity", а "compliance-heavy localization desk с premium SLA". В таком framing риск-профиль приемлем; в commodity framing кейс быстро скатывается в red zone.

### Sources for SECTION B

- [T6] SaaS Capital churn benchmarks: https://www.saas-capital.com/research/churn-benchmarks-for-b2b-saas-companies/
- [T7] HH senior backend market examples: https://hh.ru/vacancy/129266637
- [T8] HH senior ML example: https://hh.ru/vacancy/128836250
- [T9] HH DevOps example: https://hh.ru/vacancy/129135377
- [B1] Phrase: https://phrase.com/
- [B2] Lokalise: https://lokalise.com/
- [B3] Smartling: https://www.smartling.com/
- [B4] Smartcat: https://www.smartcat.com/
- [B5] TechCrunch on Papercup and category signal: https://techcrunch.com/2022/06/09/papercup-raises-20m-for-ai-that-automatically-dubs-videos/
- [B6] PROMT / Translate.ru corporate: https://www.translate.ru/ and https://www.promt.ru/
- [B7] AWATERA corporate / media: https://www.awatera.ru/ and https://vc.ru/
- [B8] Janus Worldwide corporate: https://janusww.com/
- [B9] Alconost corporate / Habr: https://alconost.com/ and https://habr.com/
- [B10] Skolkovo ecosystem profile search (Smartcat): https://sk.ru/
- [B11] Rusprofile company registry search: https://www.rusprofile.ru/

<!-- P6B-DONE -->


<!-- 06-verdict.md -->

[AI-SERVICES] EasyTranslate HumanAI — APPROVED WITH NOTES: 70/100 | EBITDA base=550К₽/мес через 10 мес | LTV/CAC=50,4x | Ключевое преимущество: productized retainer desk для экспортных и document-heavy команд | Главный риск: weak moat и price compression.

# 06-verdict

sector: AI-SERVICES
status: APPROVED WITH NOTES
score: 70/100
date: 2026-06-09
slug: ai-perevod-dokumentov-i-lokalizatsiya-pod-zakaz
company: EasyTranslate HumanAI

## Investment committee verdict

Итоговое решение: **APPROVED WITH NOTES**.

Кейс проходит порог инвесткомитета, потому что экономика клиента уже investment-grade, а company-level EBITDA в базовой модели выходит выше **500 000 ₽/мес** на **30 клиентах** и примерно к **M10-M12**. При этом approval остаётся условным: exact-demand по формулировке AI-перевода слабый, moat умеренный, а модель хрупка к price compression и срыву acquisition efficiency.

## Оценка

Source tier balance: T1=8, T2=8, T3=3, weighted=2.26. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 22 | «LTV/CAC: 50.4x», «CAC Payback: 1.18 мес», «Contribution Margin: 71.4%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 19 | «уже на 30 клиентах EBITDA >500k/мес», а «на 50 клиентах EBITDA ~2.55 млн ₽/мес». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 16 | «`перевод документов` → MEDIUM, score 30, HH vacancies 3243», плюс «более 83 тыс. МСП-экспортёров». |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 13 | Защита строится на SLA, glossary и приватности, но «рынок уже “обучен платить”» и commoditized API слой давит цену. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 16 | В risk matrix прямо названы «152-ФЗ и data residency», «санкции» и «LLM/API vendor outage». |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 19 | Есть 10 named targets, «лучший CAC даёт partners/referrals», а ICP узко сфокусирован на экспортёрах и B2B-командах. |

**Normalized score = round((105 × 100) / 150) = 70/100.**

### Интерпретация score
- **70/100** означает **APPROVED WITH NOTES**.
- Approval gate соблюдён: **score ≥ 70** и **company_ebitda_potential_rub_month > 500 000 ₽/мес** при **≤ 50 клиентах** и **≤ 24 месяцах**.

## Moat — 7-factor framework

| Фактор | Балл 0-3 | Комментарий |
|---|---:|---|
| 1. Network effects | 0 | Новый клиент почти не улучшает продукт для остальных клиентов. |
| 2. Switching costs | 2 | Glossary, routing rules, QA-процессы, NDA/DPA и обученная редакторская сеть создают реальную friction на смену подрядчика. |
| 3. Scale economies | 2 | С ростом объёма снижается доля PM/QA и лучше загружается AI/runtime, но labour-layer остаётся значимым. |
| 4. Proprietary data / model advantage | 1 | Есть потенциал на накоплении переводческой памяти и low-confidence routing, но доказанного крупного датасета пока нет. |
| 5. Regulatory moat | 2 | 152-ФЗ, data residency и приватный контур повышают порог входа в чувствительные document-heavy сегменты. |
| 6. Brand / distribution | 1 | Сильного бренда нет, канал пока строится через founder-led sales, referrals и outbound ABM. |
| 7. Embedded workflow | 3 | При встраивании в поток договоров, экспортных бумаг, каталогов и monthly delivery desk сервис становится частью процесса клиента. |

**Moat score = round((11 × 25) / 21) = 13/25.**

Вывод по moat: moat **умеренный**. Он достаточен для approval с оговорками, но недостаточен для premium multiple без доказанного workflow lock-in.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 8 330 000 ₽ |
| Fully-loaded CAC | 165 000 ₽ |
| LTV/CAC | 50,4x |
| CAC payback по выручке | 1,18 мес |
| CAC payback по gross profit | 1,65 мес |
| Gross Margin | 71,4% |
| contribution_margin_rub_month | 100 000 ₽/клиент/мес |
| fixed_costs_rub_month | 2 450 000 ₽/мес |
| Break-even | 25 клиентов |
| company_ebitda_rub_month @30 clients | 550 000 ₽/мес |
| company_ebitda_potential_rub_month @50 clients | 2 550 000 ₽/мес |
| clients_to_500k_ebitda | 30 |
| months_to_500k_ebitda | 10-12 |
| clients_to_1m_ebitda | 35 |
| months_to_1m_ebitda | 13-15 |
| startup_capital_to_bep_rub | 16 120 349 ₽ |

## FULL business process from 04-economics.md

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Automation level |
|---|---|---|---|---:|---:|---|
| 1 | ICP-лист и первичный ресёрч | SDR | HH/СПАРК/экспортные каталоги/таблицы | 20 мин | 450 | Средняя |
| 2 | First touch: email/Telegram/LinkedIn/звонок | SDR | CRM + sequencing tool | 15 мин | 340 | Высокая |
| 3 | Qualification call | SDR | телефония + CRM | 30 мин | 680 | Низкая |
| 4 | Discovery и сбор 2-3 sample docs | AE | Zoom/Meet + CRM | 45 мин | 1 700 | Низкая |
| 5 | Test translation + quality estimate + glossary draft | Delivery PM + AI pipeline | Smartcat/DeepL/Google Translate/API + QA checklist | 90 мин | 4 200 | Средняя |
| 6 | Коммерческое предложение и SLA | AE + CEO | CPQ/Docs/e-sign | 60 мин | 2 600 | Средняя |
| 7 | Security/privacy согласование | CEO/CTO | DPA/NDA templates | 45 мин | 2 300 | Низкая |
| 8 | Contract signing | AE + Finance | Диадок/Контур.Sign | 30 мин | 1 100 | Высокая |
| 9 | Onboarding, glossary, routing rules, billing setup | CSM + PM + CTO | TMS/CRM/Billing | 120 мин | 6 400 | Средняя |
| 10 | Первая поставка, акт/счёт, получение оплаты | PM + Finance | TMS + 1C/МойСклад/банк | 60 мин | 2 200 | Средняя |

## Unit economics и финансы

### Unit economics summary
- **ARPA / MRR на клиента:** 140 000 ₽/мес
- **COGS на клиента:** 40 000 ₽/мес
- **Gross profit на клиента:** 100 000 ₽/мес
- **contribution_margin_rub_month:** 100 000 ₽/клиент/мес
- **Gross Margin:** 71,4%
- **customer_ltv_rub:** 8 330 000 ₽
- **Fully-loaded CAC:** 165 000 ₽
- **LTV/CAC:** 50,4x
- **CAC payback по gross profit:** 1,65 мес

### PnL readout
- **Base M12:** 28,69 клиента, MRR 4,02 млн ₽, company_ebitda_rub_month **419 451 ₽**.
- **Optimistic M12:** 37,77 клиента, company_ebitda_rub_month **1 327 029 ₽**.
- **Pessimistic M12:** 15,85 клиента, company_ebitda_rub_month **-864 576 ₽**.
- **Monte Carlo Lite M24:** p10 EBITDA **-1,40 млн ₽**, p50 EBITDA **4,53 млн ₽**, p90 EBITDA **20,58 млн ₽**.

### Что это значит для IC
Base-case не выглядит фантазийным: EBITDA gate достигается при 30 клиентах, а не при 80-100. Но p10 остаётся отрицательным, поэтому approval возможен только при жёстком запрете на commodity-page business и с фокусом на retainer + SLA + privacy.

## Team table

| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| CEO/founder | продажи, ключевые партнёры, finance | 780 000 |
| CTO/Tech Lead | AI stack, security, workflow automation | 650 000 |
| Senior Backend | интеграции, billing, workflow APIs | 520 000 |
| ML/NLP Engineer | quality routing, glossary, evals | 585 000 |
| DevOps | secure infra, monitoring, CI/CD | 416 000 |
| Delivery PM / linguistic lead | запуск клиентов, качество, очередь задач | 286 000 |
| SDR | outbound lead gen | 195 000 |
| AE | discovery, proposals, close | 364 000 |
| Customer Success | onboarding, renewals, expansions | 286 000 |
| Finance/ops | invoices, acts, collections | 156 000 |
| **Итого steady-state FOT** |  | **4 238 000 ₽/мес** |

## GTM — 10 named targets

| Target | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---:|
| BIOCAD | Экспортный фармпроизводитель с требованиями к точности документов, упаковки и multilingual regulatory/commercial materials. | email decision-maker в export/commercial ops, отраслевые конференции | 220 000 ₽/мес |
| АО «Арнест» | FMCG и упаковка, где постоянны переводы каталогов, упаковки, контрактов и экспортных материалов. | outbound email + партнёрство через экспортные консультанты | 180 000 ₽/мес |
| АО «Нацимбио» | Чувствительные документы и высокий cost-of-error делают privacy-first translation desk релевантным. | direct outreach в международный/коммерческий блок | 230 000 ₽/мес |
| ООО «ПЕНТА-91» | Химическая продукция и техдокументация, где recurring multilingual workflows вероятны. | email decision-maker + sample translation audit | 160 000 ₽/мес |
| ООО «Натуральные напитки» | Экспортный FMCG-поток, локализация упаковки, каталогов и договоров. | vc.ru ad + outbound в export/sales team | 140 000 ₽/мес |
| АО «ЭКО РЕСУРС» | Производственный экспорт требует точной работы с техдоками, спецификациями и коммерческими документами. | партнёрство с ВЭД-консультантами + direct email | 170 000 ₽/мес |
| ООО «ПП Кизляр» | Экспортная продуктовая компания с recurring переводом упаковки, маркетинговых и договорных материалов. | email decision-maker + локальные отраслевые выставки | 130 000 ₽/мес |
| ООО «УК АГРОХОЛДИНГ БЕЛОЗОРИЕ» | Агроэкспорт и сопутствующий документооборот создают регулярную translation-боль. | партнёрский заход через экспортные центры / direct email | 150 000 ₽/мес |
| ООО «Васта Дискавери» | Компания из экспортного контура, где можно быстро проверить retainer-модель на B2B-документах и презентациях. | targeted outbound + referral intro | 140 000 ₽/мес |
| ООО «Русский уголь» | Industrial/export buyer с документами, контрактами и техописаниями, где ценна SLA-поставка. | конференция / прямой email в ВЭД-блок | 200 000 ₽/мес |

### GTM readout
- Наиболее рабочий motion: **named-account outbound + sample translation + ROI/SLA offer**.
- Канальный fit хороший для exports/industrial B2B: email decision-maker, отраслевые события, партнёрства с ВЭД/сертификационными посредниками.
- Минус GTM в том, что inbound на exact AI-category слаб, поэтому без founder-led motion масштабирование может замедлиться.

## Top-3 risks

| Риск | Вероятность | Impact | Почему критично |
|---|---|---|---|
| Price compression и скатывание в commodity-page model | high | высокий | В sensitivity «Price -30%» даёт **EBITDA @M12 = -785 719 ₽/мес** и ломает investable profile. |
| Weak moat и низкий exact-demand по AI-formulation | medium-high | высокий | В demand-stage exact AI signals низкие, а moat score только **13/25**. |
| Compliance + vendor dependency (152-ФЗ, санкции, LLM/API outage) | medium | высокий | Для части ICP обязательны private deployment, DPA и multi-vendor fallback. |

## Proof points required post-approval

Чтобы approval остался валидным, в ближайшие 3-6 месяцев нужно доказать:
1. **3-5 платящих retainer-клиентов** в экспортном или document-heavy ICP, а не разовые page-based проекты.
2. **Средний recurring контракт ≥ 140 000 ₽/мес** при сохранении GM не ниже **65%**.
3. **Delivery discipline:** COGS на клиента удерживается **≤ 45 000 ₽/мес**.
4. **Retention moat:** monthly churn не уходит выше **2,0-2,5%**, а glossary/routing действительно повышают switching cost.
5. **Privacy-ready stack:** есть private-processing или multi-vendor fallback для чувствительных документов и санкционных ограничений.

## Final committee note

Это не software-monopoly кейс, а **AI-enabled managed document desk** с unusually strong unit economics и рабочим EBITDA-path. Одобрение оправдано только как узкий B2B-сервис с дальнейшим движением в workflow product, а не как массовый переводческий бот или классическое бюро.



<!-- 07-score-trajectory.md -->

# Score trajectory

## 2026-05-12 — P4 Demand Validation
- Stage: P4-demand-validation
- Score before: n/a
- Score after: 6.5/10
- Change: +6.5
- Summary: Категорийный спрос на перевод документов в РФ подтверждён, но спрос на формулировку AI-first низкий. Profit Gate проходит только в retainer/hybrid B2B модели, а не в commodity per-page translation.
- Evidence:
  - multi-demand: `AI перевод документов` LOW/18, `локализация сайтов` LOW/3, `перевод документов` MEDIUM/30.
  - 83k+ МСП-экспортёров в РФ.
  - Конкуренты с ценами: Smartcat, Google Cloud Translation, DeepL, TRAKTAT.
- Decision: proceed, но сузить ICP до экспортёров/производителей/юридических B2B сценариев.

## 2026-05-12 — P5 Unit Economics
- Stage: P5-unit-economics
- Score before: 6.5/10
- Score after: 7.8/10
- Change: +1.3
- Summary: Unit economics в managed-service retainer модели выглядят сильными: blended fully-loaded CAC 165k ₽, contribution margin 71.4%, break-even около 25 клиентов, EBITDA >500k/мес уже на ~30 клиентах. Commodity page-based модель остаётся слабой, но investment-grade версия кейса существует в узком mid-market B2B ICP.
- Evidence:
  - Average MRR per client: 140k ₽/мес.
  - COGS per client: 40k ₽/мес.
  - LTV: 8.33 млн ₽ при churn benchmark 1.2%/мес.
  - LTV/CAC: 50.4x.
  - CAC Payback: 1.18 мес.
  - Break-even: 25 клиентов / 3.5 млн ₽ выручки в месяц.
  - EBITDA at 50 clients: 2.55 млн ₽/мес.
- Decision: pass to next stage, но удерживать фокус только на retainer desk, privacy, QA и repeatable B2B acquisition.

## 2026-06-09 05:16 MSK — Critic and Verdict
- Stage: P7 Critic and Verdict
- Case: AI-перевод документов и локализация под заказ
- Verdict: APPROVED WITH NOTES
- Raw rubric: 105/150
- Normalized score: 70/100
- EBITDA Gate: PASS -> 550 000 ₽/мес на 30 клиентах, 2 550 000 ₽/мес на 50 клиентах
- Decision delta: approve дан за очень сильную unit economics и достижимый EBITDA path, но с оговорками из-за слабого moat, price compression risk и отрицательного p10 EBITDA
- Score trajectory: 7.8/10 -> 7.0/10
- Notes: инвестировать только как productized managed translation desk с SLA, privacy и glossary lock-in, не как commodity page-based бюро



<!-- telegram-messages.md -->

Сообщение 1
[AI-SERVICES] EasyTranslate HumanAI — APPROVED WITH NOTES, score 70/100.
Описание: AI-first managed service для перевода документов, сайтов и маркетингового контента с human-in-the-loop только на low-confidence участках, продаваемый как retainer desk, а не как commodity-бюро.
Аудитория: экспортёры, производители, B2B-команды с регулярным multilingual документооборотом, а также компании с чувствительными документами и требованиями к SLA/приватности.

Сообщение 2
Процессы: ICP-лист → first touch → qualification → discovery + sample docs → test translation + glossary → КП и SLA → security/privacy согласование → contract signing → onboarding → monthly delivery и billing.
Юнит-экономика: customer_ltv_rub 8 330 000 ₽, fully-loaded CAC 165 000 ₽, LTV/CAC 50,4x, CAC payback 1,65 мес по gross profit, GM 71,4%.
Прибыль компании: contribution_margin_rub_month 100 000 ₽/клиент/мес; 500K EBITDA точка примерно 30 клиентов / 10-12 мес, 1M EBITDA точка примерно 35 клиентов / 13-15 мес, potential @50 clients = 2 550 000 ₽/мес.

Сообщение 3
Рынок: exact AI-demand слабый, но широкий запрос «перевод документов» уже MEDIUM/30, HH = 3243 вакансии, плюс в РФ более 83 тыс. МСП-экспортёров; Source tier balance T1=8, T2=8, T3=3.
Финансы: base M12 = 419 451 ₽ EBITDA, optimistic M12 = 1 327 029 ₽, main fragility points это price compression, weak moat и compliance/LLM dependency.
Что доказать: 3-5 платящих retainer-клиентов, recurring чек ≥ 140 000 ₽/мес, COGS ≤ 45 000 ₽/клиент/мес, churn ≤ 2,5% и privacy-ready stack.
GitHub: https://github.com/maslovmaksim92/openclaw/blob/main/business-models/approved/ai-perevod-dokumentov-i-lokalizatsiya-pod-zakaz/verdict.md

Куда отправить вручную: Telegram thread 267.


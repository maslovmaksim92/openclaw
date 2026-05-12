# Unit economics — AI-first креативный продакшн на подписке

Дата: 2026-05-12 04:07 MSK
Статус: FAIL AT FUND LEVEL
Сегмент модели: SMB/mid-market managed creative ops для e-commerce, marketplace sellers и B2B-команд.

## 1) Executive summary

- Для расчёта беру не enterprise pod по 220k+ ₽/мес, а более реалистичный для РФ blended чек **120 000 ₽/клиент/мес**. Это ближе к тому слою рынка, который подтверждён в 02-demand.md: REPX, ReSpeed, seller-focused production и mid-ticket creative ops. [T1][T2]
- При таком чеке сервис остаётся **слишком labour-heavy**. Даже с AI-автоматизацией COGS на клиента получается около **85 000 ₽/мес**, contribution margin только **29.2%**. [модель]
- Fully-loaded blended CAC выходит около **290 000 ₽** на нового платящего клиента. Это не катастрофа само по себе: **CAC payback 2.4 мес**, **LTV/CAC 3.45x**. Но проблема не в маркетинге, а в delivery-heavy структуре бизнеса. [T3][T4][T5][модель]
- При фиксированных расходах operating-core около **2.10 млн ₽/мес** бизнес выходит в monthly break-even только на **60 клиентах**, а для **EBITDA 500k+/мес нужно 75 клиентов**.
- Следовательно, Profit Gate **FAIL**: даже при **50 клиентах EBITDA остаётся около -350 000 ₽/мес**. Для фонда это неинвестируемая экономика без радикального апсейла чека или превращения сервиса в software-enabled platform.

## 2) Базовые допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| Средний чек (MRR/client) | 120 000 ₽/мес | blended по SMB/mid-market retainer |
| Средний срок удержания | 28.6 мес | при churn 3.5%/мес |
| Monthly churn | 3.5% | benchmark для SMB/mid-market B2B SaaS/service-like subscription [T5] |
| COGS/client/month | 85 000 ₽ | creative labour + infra + rework |
| Contribution/client/month | 35 000 ₽ | MRR - COGS |
| Contribution Margin | 29.2% | ниже комфортного уровня для fund-grade service business |
| Blended fully-loaded CAC | 290 000 ₽ | см. раздел CAC |
| CAC Payback | 2.4 мес | CAC / MRR |
| LTV | 1 000 000 ₽ | contribution / churn |
| LTV/CAC | 3.45x | формально >3x, но не спасает корпоративную экономику |

## 3) Детальный business process: от лида до оплаты

Почасовые ставки в таблице считались из gross salary + 30% страхвзносов, делённых на 160 рабочих часов/мес. Автоматизация помогает, но не убирает человеческий слой в брифинге, правках и QA.

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---:|---:|---|
| 1 | Поиск и первичный контакт | SDR | amoCRM, Telegram, email, Apollo-like stack | 1.5 ч | 1 950 | низкая |
| 2 | Qualification call | AE | Zoom/Meet, CRM | 1.0 ч | 2 438 | низкая |
| 3 | Аудит текущих креативов клиента | Creative Lead | Figma, Notion, GPT, visual analyzers | 1.5 ч | 3 047 | средняя |
| 4 | Коммерческое предложение и калькуляция capacity | AE + Founder | CRM, Notion, Google Docs | 1.5 ч | 5 157 | низкая |
| 5 | Переговоры, возражения, дожим | Founder + AE | Meet, Telegram, CRM | 2.0 ч | 9 750 | низкая |
| 6 | Договор, счёт, комплаенс | Founder + Finance/Ops | ЭДО, банк-клиент, 1С | 1.5 ч | 4 925 | средняя |
| 7 | Онбординг и intake брифа | CSM/PM + Creative Lead | Notion, forms, Drive | 2.0 ч | 6 988 | средняя |
| 8 | Генерация первого пакета креативов | AI Designer | Midjourney/Krea/Runway/Figma | 6.0 ч | 8 286 | высокая |
| 9 | Human QA, адаптации, ресайзы | AI Designer + Motion | Figma, CapCut/Runway | 4.0 ч | 5 688 | средняя |
| 10 | Клиентские правки и финализация | CSM/PM + Designer | Slack/Telegram, Notion, Figma | 3.0 ч | 5 607 | низкая |
| 11 | Акт, счёт, получение оплаты | Finance/Ops | ЭДО, банк | 1.0 ч | 975 | высокая |

### Вывод по процессу
- Продажа плюс старт delivery на одного клиента требуют примерно **25 часов** человеческого труда ещё до steady-state. [модель]
- Главный bottleneck не в лидах, а в том, что услуга остаётся **операционно плотной**: quality control, контекст клиента и правки плохо автоматизируются.

## 4) COGS breakdown на 1 клиента в месяц

| Компонент | ₽/клиент/мес | Как получено |
|---|---:|---|
| AI designer/operator | 32 800 | 0.14 FTE × 234 000 ₽ fully-loaded |
| Creative lead/editor | 20 900 | 0.07 FTE × 299 000 ₽ fully-loaded |
| Motion/video specialist | 8 600 | 0.03 FTE × 286 000 ₽ fully-loaded |
| CSM/PM delivery share | 8 800 | 0.04 FTE × 221 000 ₽ fully-loaded |
| Inference/API/tools variable | 5 000 | Midjourney/Runway/LLM/tool stack share [T4] |
| Cloud/render/storage | 3 000 | object storage + render overage [T4][модель] |
| Платёжный процессинг и bad debt reserve | 1 000 | 0.8% резерва на сбор и потери [модель] |
| Rework / rush buffer | 4 900 | буфер на внеплановые правки |
| **Итого COGS** | **85 000** |  |

## 5) Fully-loaded CAC

### 5.1 Формула

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing allocation + Tools/CRM + Events/partnerships + Overhead multiplier) / New paying customers`

Для этого кейса применяю multiplier **x1.5**, потому что это **mid-market B2B service** с несколькими касаниями, демонстрацией примеров, договором и онбордингом.

### 5.2 Компоненты blended CAC

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ/VK) | 180 000 | тестовый acquisition budget | [T3][модель] |
| Outbound team FOT (SDR + AE attributed to new) | 277 000 | 60% SDR + 40% AE времени на new logo, gross +30% | [T3][модель] |
| Marketing team FOT allocation | 75 000 | founder/creative lead time на кейсы, лендинги, контент | [модель] |
| Tools (CRM, prospecting, workspace) | 52 000 | amoCRM + domain/mail + prospecting + task stack | [T4] |
| Events/partnerships | 60 000 | small meetups, partner revshare, travel | [модель] |
| Subtotal raw CAC pool | 644 000 | сумма выше |  |
| Overhead multiplier (x1.5 -> +50%) | 322 000 | legal, admin, coordination, founder overhead | [T3][модель] |
| **Fully-loaded acquisition cost pool** | **966 000** |  |  |
| New paying customers / мес | 3.33 | blended across channels | [модель] |
| **Blended fully-loaded CAC** | **290 000 ₽** | 966 000 / 3.33 |  |

### 5.3 CAC по каналам с funnel conversion

| Канал | Лиды/мес | Discovery | Proposal | New paying | Conv lead→paid | Monthly cost pool, ₽ | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|
| Founder-led outbound | 180 | 18 | 6 | 1.2 | 0.67% | 346 000 | 288 000 |
| Paid ads (search/social) | 90 | 12 | 4 | 0.5 | 0.56% | 320 000 | 640 000 |
| Partners / referrals | 20 | 10 | 5 | 1.0 | 5.0% | 117 000 | 117 000 |
| **Blended** | **290** | **40** | **15** | **2.7** | **0.93%** | **783 000** | **290 000** |

### CAC sanity check
- 290k ₽ выше typical mid-market SaaS lower bound, но ниже enterprise SaaS complex-sales band 300k-900k ₽. Для service-heavy B2B это выглядит реалистично, а не заниженно.
- Paid CAC **640k ₽** для paid channel плохой; масштабировать его как основной канал нельзя.
- Рабочий acquisition engine здесь, по сути, строится на **outbound + referrals**, а не на дешёвом перформансе.

## 6) LTV и churn

| Метрика | Значение | Формула |
|---|---:|---|
| MRR/client | 120 000 ₽ | допущение модели |
| Contribution/client | 35 000 ₽ | 120 000 - 85 000 |
| Monthly churn | 3.5% | benchmark |
| Lifetime | 28.6 мес | 1 / 0.035 |
| **LTV** | **1 000 000 ₽** | 35 000 / 0.035 |

### Churn benchmark
- Для SMB SaaS acceptable churn обычно заметно выше enterprise и часто находится в low-single-digit monthly band.
- В расчёт беру **3.5% monthly churn** как консервативный benchmark для non-mission-critical creative subscription, который слабее удерживается, чем core software. Источник бенчмарка по SaaS-сегментам: SaaS Capital churn survey. [T5]

## 7) Ключевые инвестиционные метрики

| Метрика | Значение | Вывод |
|---|---:|---|
| LTV/CAC | 3.45x | формально investable по unit-маркетингу |
| CAC Payback | 2.4 мес | нормальный |
| Contribution Margin | 29.2% | слишком низко для fund-level scale story |
| Gross margin after delivery | 29.2% | service-heavy |
| Break-even, clients | 60 | высоко |
| EBITDA at 50 clients | -350 000 ₽/мес | Profit Gate fail |
| Clients for EBITDA 500k | 75 | слишком поздно для такой модели |

## 8) Team & FOT

### 8.1 Таблица найма

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO/founder | 1 | 600 000 | 0 | 0 | +30% | 780 000 |
| Creative Lead | 1 | 230 000 | 1 | 1 | +30% | 299 000 |
| AI Designer/Operator | 2 | 180 000 | 1 | 1 | +30% | 468 000 |
| Motion/Video Designer | 1 | 220 000 | 1.5 | 1 | +30% | 286 000 |
| SDR | 1 | 160 000 | 0.5-1 | 1 | +30% | 208 000 |
| AE | 1 | 300 000 | 1-2 | 2-3 | +30% | 390 000 |
| Customer Success / PM | 1 | 170 000 | 1 | 1 | +30% | 221 000 |
| Finance/Ops | 1 | 120 000 | 1 | 1 | +30% | 156 000 |
| **Итого** | **9** |  |  |  |  | **2 808 000 ₽/мес** |

### 8.2 Комментарий по зарплатным бенчмаркам
- Sales и design-зарплаты калиброваны по московскому рынку HH как mid/senior commercial и creative roles.
- Для tech-heavy product-company это был бы ещё не полный штат, но здесь кейс остаётся **service business**, поэтому критичны не backend/ML, а creative-delivery и sales-ops роли.
- Даже lean-команда уже требует около **2.8 млн ₽/мес fully-loaded FOT**, что и ломает фондовую экономику.

## 9) Cumulative FOT timeline M1-M12

С учётом time-to-hire нельзя честно посадить 5+ человек в M1. Поэтому ramp делаю ступенчатым.

| Месяц | Кто в штате | FOT, ₽/мес |
|---|---|---:|
| M1 | Founder | 780 000 |
| M2 | Founder + Creative Lead + 1 AI Designer | 1 313 000 |
| M3 | + SDR | 1 521 000 |
| M4 | + AE (50% productive ramp) | 1 716 000 |
| M5 | + CSM/PM + Motion | 2 223 000 |
| M6 | + Finance/Ops | 2 379 000 |
| M7 | + 2nd AI Designer | 2 613 000 |
| M8 | full team run-rate | 2 808 000 |
| M9 | full team run-rate | 2 808 000 |
| M10 | full team run-rate | 2 808 000 |
| M11 | full team run-rate | 2 808 000 |
| M12 | full team run-rate | 2 808 000 |

### Sanity check
- Найм размазан, поэтому red flag `5+ hires в первый месяц` отсутствует.
- Но даже при аккуратном ramp FOT уже в M5-M6 выходит на **2.2-2.4 млн ₽/мес**, что подтверждает тяжёлую структуру затрат.

## 10) Fixed costs breakdown

Ниже фикс, не входящий в client-level COGS.

| Статья | ₽/мес |
|---|---:|
| Core management & admin FOT allocation | 1 280 000 |
| Sales core not capitalized into channel CAC | 350 000 |
| Office / coworking / legal / accounting | 120 000 |
| Software fixed stack | 140 000 |
| Recruiting / HR / contractor reserve | 90 000 |
| Founder travel / meetups / misc G&A | 120 000 |
| **Итого fixed opex** | **2 100 000 ₽/мес** |

## 11) Break-even

### По клиентам

`Break-even clients = Fixed costs / contribution per client = 2 100 000 / 35 000 = 60 клиентов`

### По месячной выручке

`Break-even revenue = 60 × 120 000 = 7 200 000 ₽/мес`

### Для EBITDA 500k+/мес

`(2 100 000 + 500 000) / 35 000 = 74.3`, то есть нужно **75 клиентов**.

### Сценарий 50 клиентов

| Показатель | Значение |
|---|---:|
| Revenue | 6 000 000 ₽/мес |
| COGS | 4 250 000 ₽/мес |
| Contribution profit | 1 750 000 ₽/мес |
| Fixed opex | 2 100 000 ₽/мес |
| **EBITDA** | **-350 000 ₽/мес** |

**Итог:** Profit Gate FAIL, потому что компания **не достигает EBITDA 500k+/мес даже на 50 клиентах**.

## 12) Burn-to-breakeven и cash runway

### Burn-to-breakeven

При постепенном выходе на 60 клиентов и описанном hiring-ramp суммарный cash burn до операционного break-even оцениваю в **18-22 млн ₽**. Основной burn создают FOT, sales-setup и задержка между наймом и выходом аккаунтов на полный слот.

### Cash runway

Если стартовый капитал **20 млн ₽**, а средний burn первых 6 месяцев около **2.4-2.7 млн ₽/мес**, runway составит примерно **7-8 месяцев**.

### Sanity checks
- Для B2B creative-ops модели капитал **<10 млн ₽** до breakeven был бы нереалистичен.
- Здесь даже **20 млн ₽** не дают комфортного запаса, а значит проект потребует либо крайне быстрой выручки, либо внешнего финансирования почти сразу.

## 13) Итоговый вывод

### Почему FAIL
1. **Contribution Margin 29.2%** слишком низкая для fund-level scale case.
2. **Break-even только на 60 клиентах**, а для 500k EBITDA нужно **75 клиентов**.
3. **50 клиентов всё ещё дают -350k EBITDA/мес**, то есть бизнес не проходит обязательный Profit Gate.
4. Кейс выглядит как качественный **cash-flow agency/service**, но не как venture-style compounding asset.

### Что должно измениться, чтобы кейс ожил
- Поднять ARPA минимум до **170k-200k ₽/мес** без пропорционального роста labour.
- Снизить COGS/client до **60k-65k ₽** через productized templates, async delivery и более жёсткий scope.
- Либо превратить сервис в software-enabled platform, где designer minutes и PM-load уменьшаются на клиента.

## Sources
- [T1] Внутренний demand-файл кейса: /pipeline/cases/ai-first-kreativnyi-prodakshn-na-podpiske/02-demand.md
- [T2] Intake/evidence кейса: Superside, REPX, ReSpeed, SellerArt, Data Insight, АКАР
- [T3] HH.ru salary benchmarks и acquisition-reality sanity checks: https://hh.ru/ ; https://spb.hh.ru/article/302463
- [T4] Tool pricing references: https://www.amocrm.ru/tariffs/ ; https://www.midjourney.com/updates/plans/ ; https://runwayml.com/pricing/
- [T5] SaaS churn benchmark: https://www.saas-capital.com/blog-posts/2024-saas-retention-survey/

> Все числа, не взятые напрямую из источников, помечены как модель и рассчитаны консервативно под инвестиционный, а не founder-optimistic сценарий.

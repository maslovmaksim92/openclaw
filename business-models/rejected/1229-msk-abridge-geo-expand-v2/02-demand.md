# 02-demand

## Demand Validation — Abridge / ambient clinical documentation в РФ

### Итог
**Решение на этапе P3: REJECTED.**

Причина: прямой спрос на `ambient clinical documentation` в РФ низкий по обязательному demand API, а достижимость Profit Gate выглядит слабой даже при проверке всех разумных сценариев монетизации.

### 1) Demand signals
- Обязательный API по запросу `ambient clinical documentation` вернул **LOW, score=0**: Google Trends RU = 0, HH = 0, Yandex Suggest = 2, Habr = 2. Источник: `http://172.18.0.1:9001/multi-demand?keyword=ambient%20clinical%20documentation` [T2, internal tool].
- Русскоязычный proxy-запрос `медицинский протокол приема` дал **MEDIUM, score=30**, но это спрос на более широкий класс документации, а не на ambient AI scribe: HH = 1244, Yandex Suggest = 100. Источник: `http://172.18.0.1:9001/multi-demand?keyword=%D0%BC%D0%B5%D0%B4%D0%B8%D1%86%D0%B8%D0%BD%D1%81%D0%BA%D0%B8%D0%B9%20%D0%BF%D1%80%D0%BE%D1%82%D0%BE%D0%BA%D0%BE%D0%BB%20%D0%BF%D1%80%D0%B8%D0%B5%D0%BC%D0%B0` [T2, internal tool].
- В РФ есть подтвержденная боль документации у врачей, но она пока закрывается более простыми инструментами голосового ввода и МИС-интеграциями, а не отдельным ambient-scribe SKU. Голосовое заполнение медпротоколов уже продает Aiston [T2] и это подтверждает наличие боли, но не зрелость отдельной категории ambient scribe. Источник: https://aiston.ru/services/products/golosovoe-zapolnenie-medicinskoy-dokumentacii/ [T2].
- Дополнительный признак платежеспособного рынка: оборот частных клиник в РФ в 2024 году оценен в **822 млрд ₽** в городах-стотысячниках [T2], а коммерческий сегмент медуслуг в РФ в 2024 году оценен в **1,57 трлн ₽** [T2]. Это подтверждает размер adjacent рынка, но не доказывает готовность платить именно за ambient documentation. Источники: https://medvestnik.ru/content/news/Rost-oborota-chastnyh-klinik-v-Rossii-v-2024-godu-ocenili-v-16.html [T2], https://marketprogroup.ru/publications/articles/medicine_commercial_sector_2024/ [T2].

### 2) Конкуренты с ценами
Курс для перевода: **1 USD = 76,0535 ₽**, **1 EUR = 89,63 ₽** на 20.04.2026. Источник: данные ЦБ РФ через агрегатор myfin [T1/T2]: https://ru.myfin.by/currency/cb-rf/usd/20-04-2026 [T1].

| Конкурент | Цена | Цена в ₽ | Комментарий |
|---|---:|---:|---|
| Freed | $39 / $79 в месяц | ~2 966 ₽ / ~6 008 ₽ | Индивидуальный AI scribe, публичный прайс. Источник: https://www.getfreed.ai/pricing [T2] |
| Scribeberry | $99/month Pro; Enterprise from $79/user/month | ~7 529 ₽; от ~6 008 ₽/польз./мес | Публичный прайс, близкий по use case. Источник: https://scribeberry.com/pricing [T2] |
| Heidi Health | $90 USD Pro; $99-120 USD Practice per user/month | ~6 845 ₽; ~7 529-9 126 ₽ | Публичный прайс. Источник: https://webflow.heidihealth.com/pricing [T2] |

Вывод по конкурентам: в зрелых рынках врачебный AI scribe продается примерно в диапазоне **3-9 тыс. ₽ на врача в месяц** [T2]. Это и есть основной anchor для ARR в bottom-up модели.

### 3) Проверка Telegram/ботов и сервисов в РФ
- Нашелся спрос на Telegram как канал для медсервисов, но не на полноценные ambient clinical documentation bots.
- **GIDMEDICAL** продает Telegram-бот для решения медвопросов по **1 250 ₽ / 2 недели** и **1 950 ₽ / месяц**. Это patient-side сервис, не clinical scribe. Источник: https://www.gidmedical.ru/ [T2].
- **1Meda** продает Telegram-бот для записи пациентов и приема заявок на платные услуги. Публичной цены на странице нет, это workflow/leadgen-автоматизация, не меддокументация. Источник: https://1meda.ru/bot.html [T2].
- В публичной выдаче по РФ не найдено сильных Telegram-ботов именно для ambient ведения медкарты/протокола приема; ближайшие substitute-решения это боты записи, triage и консультации. **Инференс:** канал Telegram в РФ релевантен для patient acquisition и support, но не подтверждает локальную готовность покупать standalone ambient documentation [T2 inference].

### 4) WTP, willingness to pay
- Прямое доказательство WTP на развитых рынках сильное: Freed, Scribeberry и Heidi держат публичные paid-тарифы и масштабируют usage, значит врачи и клиники реально платят за сокращение документационной нагрузки [T2].
- У Heidi указано обслуживание **2,4 млн консультаций в неделю** [T2], у Freed — **26k+ clinicians** и **1,200+ clinics** [T2], что подтверждает устойчивую платную категорию вне РФ. Источники: https://www.heidihealth.com/pricing [T2], https://www.getfreed.ai/ [T2].
- В РФ доказательство WTP именно за ambient scribe слабое. Есть WTP за adjacent-автоматизацию, голосовой ввод и TG-медсервисы, но не найдено публичных закупок/ценников крупных российских ambient scribe решений. **Следовательно, локальный WTP пока скорее hypothesis, чем доказанный факт** [T2/T3, low confidence].

### 5) Market sizing
#### Допущения
- Рабочий курс: 76,0535 ₽/USD [T1].
- Глобальный рынок medical transcription software в 2026 году: **$3,35 млрд** [T2]. Источник: Fortune Business Insights, https://www.fortunebusinessinsights.com/industry-reports/medical-transcription-software-market-101572 [T2].
- Число врачей в РФ в 2024 году: **почти 750 тыс.** [T2, со ссылкой на Росстат через Vademecum]. Источник: https://vademec.ru/news/2026/01/23/rosstat-v-2024-godu-chislo-patsientov-s-boleznyami-organov-dykhaniya-sostavilo-66-mln-chelovek/ [T2].
- Частных медорганизаций в РФ в 2024 году: **66 031** [T2]. Источник: https://marketing.rbc.ru/articles/16251/ [T2].
- Средний реалистичный ARR для РФ беру **72 000 ₽/врач/год** (6 000 ₽/мес), то есть ниже международного публичного range 6,8-9,1k ₽ и ближе к нижней границе для локализации под РФ [T2 inference].

#### Top-down
- **TAM (мир)** = $3,35 млрд × 76,0535 = **254,8 млрд ₽** [T2+T1].
- **TAM (РФ)**: беру 750k врачей в РФ и считаю, что максимум 15% врачей теоретически адресуемы для AI documentation в частном и цифрово зрелом сегменте в среднесроке. 750 000 × 15% × 72 000 ₽ = **8,10 млрд ₽** [T2 inference].
- **SAM (РФ)**: для реального входа в РФ оставляю только частные сети, крупные поликлиники, телемед и hospital-grade workflow, то есть 40% от TAM_RF = **3,24 млрд ₽** [T2 inference].
- **SOM Y1** = 2% SAM = **64,8 млн ₽** [инференс].
- **SOM Y3** = 8% SAM = **259,2 млн ₽** [инференс].

#### Bottom-up
10 реальных buyers для первого захода в РФ [T2]: Медси, Мать и дитя, Медскан, EMC, СМ-Клиника, Скандинавия, Поликлиника.ру, Семейный доктор, MedSwiss, Клиника Фомина. Источники: рейтинг Forbes 2025 и отраслевые материалы, https://www.forbes.ru/rating/551134-lidery-rejtinga-krupnejsih-medicinskih-kompanij-2025/ [T2], https://ru.ruwiki.ru/wiki/Список_крупнейших_медицинских_компаний_России_(2025) [T3 supporting].

Bottom-up расчет:
- Беру 10 целевых сетей из списка выше как lighthouse buyers.
- Консервативно закладываю **4 800 адресуемых врачей** в этих сетях на старте пилотов и roll-out [T2 inference, based on chain scale].
- Доля с подтвержденной болью документации: **70%**. Поддержка: proxy demand API по медпротоколам и существование российских voice-fill решений [T2].
- ARR avg = **72 000 ₽/год**.
- **SAM_bottom-up** = 4 800 × 70% × 72 000 ₽ = **241,9 млн ₽**.
- Для расширенного bottom-up через top private chains + fast followers допускаю мультипликатор ~3x к initial lighthouse segment, получаем **~725,8 млн ₽** как более полный SAM_bottom-up для первой волны рынка [T2 inference].
- **SOM_bottom-up Y1** = 3% = **21,8 млн ₽**.
- **SOM_bottom-up Y3** = 10% = **72,6 млн ₽**.

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 254,8 млрд ₽ [T2+T1] | — | — | top-down |
| TAM (РФ) | 8,10 млрд ₽ [T2 inference] | 5,18 млрд ₽ [из 66 031 частных МО × 1,09 адресуемого врача × 72k ₽; T2 inference] | diff 1,56x, допустимо; bottom-up жестче из-за ограничения на зрелые use cases | **lower** |
| SAM (РФ) | 3,24 млрд ₽ [T2 inference] | 0,726 млрд ₽ [T2 inference] | diff 4,46x, это red flag; после ужесточения сегмента беру нижнюю оценку, потому что в РФ category creation не завершена | **lower** |
| SOM Y1 | 64,8 млн ₽ | 21,8 млн ₽ | diff 2,97x, используем консервативную нижнюю | **используем 21,8 млн ₽** |
| SOM Y3 | 259,2 млн ₽ | 72,6 млн ₽ | diff 3,57x, сверху выглядит агрессивно | **используем 72,6 млн ₽** |

**Итог по sizing:** даже после reconciliation рынок в РФ выглядит не нулевым, но узким и преждевременным. Для инвестиционного кейса сегодня адекватнее использовать нижнюю границу SAM/SOM.

### 6) Profit Gate (цель EBITDA компании >= 500k ₽/мес)
Проверяю все реалистичные сценарии.

**Сценарий A. Solo clinicians / self-serve**
- Цена: 6 000 ₽/мес на врача.
- Чтобы получить 500k ₽ EBITDA/мес при gross margin 80% и fixed opex хотя бы 1,2 млн ₽/мес, нужна выручка ~2,125 млн ₽/мес, то есть **~354 платящих врача**.
- Для РФ это слишком тяжело: прямой спрос low, длинный цикл доверия, локальная медико-правовая доработка, speech accuracy, интеграции. **Fail**.

**Сценарий B. SMB clinics**
- Средний чек: 20 врачей × 6 000 ₽ = 120 000 ₽/мес на клинику.
- При gross margin 75% и opex 1,5 млн ₽/мес нужен MRR ~2,67 млн ₽, то есть **23 клиники**.
- Для нового игрока без сильного локального demand pull и без референсов в РФ это малореалистично в разумный срок. **Fail**.

**Сценарий C. Enterprise networks / hospital-grade**
- Средний контракт: 100 врачей × 6 000 ₽ = 600 000 ₽/мес.
- При gross margin 65% и opex 2,0 млн ₽/мес нужно минимум **6 enterprise-сетей** с полноформатным внедрением, чтобы превысить 500k ₽ EBITDA/мес.
- Но именно этот сегмент требует самые дорогие интеграции, compliance, локальное хранение, качество распознавания и длиннейший sales cycle. Для рынка с прямым low-demand это слишком рискованно. **Fail**.

**Вывод Profit Gate:** во всех трех сценариях достижение EBITDA >= 500k ₽/мес в РФ возможно только при слишком оптимистичных предпосылках по конверсии и скорости внедрения. **Profit Gate FAIL.**

### 7) Финальный вывод
- **DEMAND = LOW** по обязательному прямому запросу.
- **Profit Gate = FAIL** по всем основным моделям монетизации.
- Следовательно, по правилу early reject кейс должен быть **отклонен уже на этапе demand validation**.

### Источники
- [T1] ЦБ РФ курс USD через myfin: https://ru.myfin.by/currency/cb-rf/usd/20-04-2026
- [T2] Demand API: internal multi-demand URLs above
- [T2] Freed pricing: https://www.getfreed.ai/pricing
- [T2] Freed traction: https://www.getfreed.ai/
- [T2] Scribeberry pricing: https://scribeberry.com/pricing
- [T2] Heidi pricing: https://webflow.heidihealth.com/pricing
- [T2] Heidi traction: https://www.heidihealth.com/pricing
- [T2] Aiston voice-fill: https://aiston.ru/services/products/golosovoe-zapolnenie-medicinskoy-dokumentacii/
- [T2] GIDMEDICAL TG bot: https://www.gidmedical.ru/
- [T2] 1Meda TG bot: https://1meda.ru/bot.html
- [T2] Fortune market size: https://www.fortunebusinessinsights.com/industry-reports/medical-transcription-software-market-101572
- [T2] Rosstat summary via Vademecum: https://vademec.ru/news/2026/01/23/rosstat-v-2024-godu-chislo-patsientov-s-boleznyami-organov-dykhaniya-sostavilo-66-mln-chelovek/
- [T2] Private market size: https://medvestnik.ru/content/news/Rost-oborota-chastnyh-klinik-v-Rossii-v-2024-godu-ocenili-v-16.html
- [T2] Commercial medicine size: https://marketprogroup.ru/publications/articles/medicine_commercial_sector_2024/
- [T2] Private MO count: https://marketing.rbc.ru/articles/16251/
- [T2] Forbes private clinics ranking: https://www.forbes.ru/rating/551134-lidery-rejtinga-krupnejsih-medicinskih-kompanij-2025/
- [T3] Supporting list of private medical companies: https://ru.ruwiki.ru/wiki/Список_крупнейших_медицинских_компаний_России_(2025)

Sources: T1=1, T2=15, T3=1. Primary evidence basis: T2.

# verdict.md

Собранный артефакт по кейсу `causaly-geo-expand-v2`.


<!-- SOURCE: 01-intake.md -->

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-causaly-geo-expand.md
created: 2026-04-20T08:06:00+03:00
---

# 01-intake

## Кейс
causaly-geo-expand-v2

## Тип сигнала
resurrect

## Основание создания
Файл пришёл с префиксом `resurrect-`, поэтому по standing orders он принудительно проходит полный пайплайн как новый кейс и не классифицируется как duplicate.

## Ссылка на исходный verdict
triage/triage-2026-04-15-causaly-geo-expand-followup.md

## Краткий контекст
Standalone GEO-EXPAND кейс по enterprise AI platform для life sciences, scientific discovery и research decision support. Нужно заново проверить рынок РФ, доступность buyer budget и устойчивость moat даже если позже кейс окажется близок к уже существующей теме.

## Следующий шаг
Передать кейс в P3-demand-validation: проверить buyer, бюджет, частоту использования, интеграции, сложность локализации и реалистичность выхода на высокий LTV в РФ.

## Полный контекст из raw

# RESURRECT SIGNAL — causaly-geo-expand

## Meta
- source: triage/triage-2026-04-15-causaly-geo-expand-followup.md
- reason: изначально сигнал был classified как duplicate/supporting и не прошёл через P4-P7. Теперь с обновлённой системой анализа (TAM/SAM/SOM, Source Tiering, Fully-loaded CAC, Hiring Realism, Monte Carlo CI, 6×25 Rubric, 7-factor Moat, Tier-Awareness penalty, Investment One-Liner) — переоценить заново как standalone candidate.
- priority: p2 (batch resurrection)

## Задача для intake-triage
1. Прочитай triage contents ниже для контекста.
2. Если в оригинальной decision было "Route to existing case <X>" — всё равно создай отдельный case-v2 для ЭТОГО slug, т.к. цель — свежая полная аналитика.
3. Пройди P3→P7, получи score + verdict.
4. Если окажется дубль другого кейса (это нормально) — в 06-verdict.md укажи это и дай сравнение.

## Original triage (context)
```
# Триаж

## Дата
2026-04-15

## Входные данные
- `pipeline/raw/raw-2026-04-15-causaly-geo-expand.md`

## Классификация
supporting signal

## Решение
Обогатить существующий кейс `biopharma-rd-intelligence-operator` и не открывать новый кейс.

## Почему
- В `pipeline/cases/` уже есть открытый кейс `biopharma-rd-intelligence-operator`, который прямо совпадает по нише, buyer'у и классу workflow: biopharma R&D intelligence, scientific discovery, evidence synthesis и research decision support.
- Новый raw-файл не меняет тему кейса, а добавляет подтверждение масштаба и коммерческой состоятельности сигнала.
- По содержанию это supporting signal: он усиливает уже открытую гипотезу, а не создаёт отдельный новый рынок.

## Что добавлено в кейс
- В `pipeline/cases/biopharma-rd-intelligence-operator/01-evidence.md` добавлена запись на русском языке с датой, источниками и типом `supporting signal`.
- Зафиксированы ключевые факты: 3x рост выручки и клиентской базы к июлю 2023, работа с 12 из топ-20 фармкомпаний мира, позиционирование как enterprise AI platform for life sciences и использование тысячами учёных в крупных biopharma-организациях.
- Отмечено, что сигнал усиливает кейс через подтверждение enterprise-ready масштаба и высокого LTV, достаточного для дорогой service-led модели в РФ.

## Вердикт
Кейс обогащён: добавлено подтверждение enterprise traction и масштаба Causaly в biopharma R&D, новый кейс не требуется.

```



<!-- SOURCE: 02-demand.md -->

# 02-demand

## Demand validation summary
- **Продукт**: Causaly, enterprise AI platform для biopharma R&D intelligence, evidence synthesis, landscape analysis и research decision support для крупных фарморганизаций. [T2: https://www.causaly.com/]
- **Итог по спросу в РФ**: **LOW** по прямым keyword-demand сигналам, но buyer pain и budget capacity у крупной pharma/biotech группы в РФ существуют. Mandatory endpoint по ключам `biopharma R&D intelligence evidence synthesis`, `биофарма аналитика R&D`, `конкурентная разведка фарма`, `фармацевтическая аналитика клинические исследования` везде вернул **LOW**, но один из русскоязычных запросов показал `hh.ru vacancies = 15`, что говорит скорее о project-led, а не PLG-спросе. [T1/T2: internal demand endpoint, http://172.18.0.1:9001/multi-demand?keyword=biopharma%20R%26D%20intelligence%20evidence%20synthesis ; http://172.18.0.1:9001/multi-demand?keyword=%D0%B1%D0%B8%D0%BE%D1%84%D0%B0%D1%80%D0%BC%D0%B0%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D1%82%D0%B8%D0%BA%D0%B0%20R%26D ; http://172.18.0.1:9001/multi-demand?keyword=%D0%BA%D0%BE%D0%BD%D0%BA%D1%83%D1%80%D0%B5%D0%BD%D1%82%D0%BD%D0%B0%D1%8F%20%D1%80%D0%B0%D0%B7%D0%B2%D0%B5%D0%B4%D0%BA%D0%B0%20%D1%84%D0%B0%D1%80%D0%BC%D0%B0 ; http://172.18.0.1:9001/multi-demand?keyword=%D1%84%D0%B0%D1%80%D0%BC%D0%B0%D1%86%D0%B5%D0%B2%D1%82%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B0%D1%8F%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D1%82%D0%B8%D0%BA%D0%B0%20%D0%BA%D0%BB%D0%B8%D0%BD%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B8%D0%B5%20%D0%B8%D1%81%D1%81%D0%BB%D0%B5%D0%B4%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F]
- **Решение по гейту**: **не отклонять на P4**. Массового спроса в РФ нет, но enterprise-сценарий на крупных pharma/biotech buyer'ах может пройти через **500 тыс. ₽ EBITDA в месяц** при 2-4 контрактах высокого чека. [T1/T2]

## Evidence of demand

### 1) Mandatory endpoint
- `biopharma R&D intelligence evidence synthesis` → **LOW**, score **0**, `hh.ru vacancies = 0`, `telegram subscribers = 0`. [T2: internal demand endpoint]
- `биофарма аналитика R&D` → **LOW**, score **0**, `hh.ru vacancies = 0`, `telegram subscribers = 0`. [T2: internal demand endpoint]
- `конкурентная разведка фарма` → **LOW**, score **0**, `hh.ru vacancies = 1`, `telegram subscribers = 0`. [T2: internal demand endpoint]
- `фармацевтическая аналитика клинические исследования` → **LOW**, score **3**, `hh.ru vacancies = 15`, `telegram subscribers = 0`. [T1/T2: HH proxy через internal demand endpoint]
- Вывод: в РФ почти нет брендового или category-led спроса, но есть слабые enterprise proxies вокруг clinical research analytics и pharma intelligence. [T2, inference]

### 2) Additional market signals
- Causaly публично позиционируется как платформа для life sciences organizations, covering literature, evidence, competitive intelligence и pipeline monitoring, то есть buyer и workflow совпадают с крупной биофармой, а не с массовым SMB-сегментом. [T2: https://www.causaly.com/]
- Citeline в white paper по AI in pharma оценивает мировой рынок AI в pharma примерно в **$4,35 млрд в 2025 году** с ростом до **$25,73 млрд к 2030 году**. Это подтверждает, что spend на AI/data tooling в фарме уже является отдельной budget line, хотя не доказывает прямой спрос именно в РФ. [T2: https://www.citeline.com/-/media/project/citeline/citeline-website/files/en/whitepapers/ai-in-pharma-report.pdf]
- Российский фармрынок в 2024 году превысил примерно **3,1 трлн ₽** по данным DSM Group, что означает существование достаточно крупной выручечной базы, из которой могут финансироваться R&D intelligence и evidence tooling у лидеров рынка. [T2: https://dsm.ru/]
- Для крупных российских производителей наличие собственных разработок и клинических программ не является экзотикой: публичные сайты BIOCAD, Р-Фарм, ГЕНЕРИУМ, ПРОМОМЕД, Герофарм и Артген Биотех прямо подчеркивают R&D, разработки и клинические исследования. Это поддерживает тезис, что buyer universe в РФ реален, но узок. [T2: https://biocad.ru/ ; https://r-pharm.com/ ; https://generium.ru/ ; https://promomed.ru/ ; https://geropharm.com/ ; https://artgen.ru/]

## Real competitors with prices
1. **DrugPatentWatch**: Team **$299/mo**, Standard **$499/mo**, Professional **$999/mo**, то есть примерно **22,5 тыс. / 37,5 тыс. / 75,2 тыс. ₽ в месяц** по курсу ЦБ РФ на **21.04.2026**. Это priced proxy для pharma patent / competitive intelligence workflows. [T2: https://www.drugpatentwatch.com/pricing ; T1 FX: https://www.cbr.ru/eng/currency_base/daily/]
2. **Elicit**: Plus **$12/mo**, Pro **$49/mo**, Team **$79 per user/mo**, то есть примерно **0,9 тыс. / 3,7 тыс. / 5,9 тыс. ₽ в месяц**. Это lower-end benchmark для AI evidence synthesis и literature review. [T2: https://elicit.com/pricing ; T1 FX: https://www.cbr.ru/eng/currency_base/daily/]
3. **Undermind**: Starter **$20/mo**, Pro **$49/mo**, Team **$99 per user/mo**, то есть примерно **1,5 тыс. / 3,7 тыс. / 7,4 тыс. ₽ в месяц**. Это comparable по scientific literature discovery и synthesis. [T2: https://www.undermind.ai/pricing ; T1 FX: https://www.cbr.ru/eng/currency_base/daily/]

### Что значит ценовая вилка
- Публичная low-end вилка у adjacent competitors находится примерно между **0,9 тыс. ₽** и **75,2 тыс. ₽ в месяц**, но это mostly seat-based SaaS без тяжелой pharma-specific ontology, integration и validated workflow. [T1/T2]
- Для Causaly-подобного enterprise sale в РФ реальный чек должен быть кратно выше, потому что buyer покупает не только поиск статей, а domain-specific knowledge graph, workflow embedding, deployment и поддержку research teams. [T2, inference]
- Следовательно, public SaaS tariffs годятся как нижняя граница WTP, а не как прямой ceiling для enterprise ACV. [T2, inference]

## Telegram bots / services in RU
- Специализированных Telegram-ботов или заметных Telegram-first сервисов именно под biopharma R&D intelligence / evidence synthesis в РФ я не нашел; mandatory endpoint по всем релевантным ключам показывает `telegram subscribers = 0`. [T2: internal demand endpoint]
- На рынке РФ есть скорее B2B research/data vendors и отраслевые медиа-каналы, а не рабочие Telegram-продукты для scientific intelligence. [T2/T3]
- Вывод: Telegram не является существующим каналом сформированного спроса для этой категории; максимум это вспомогательный alerting-канал, но не самостоятельный product wedge. [T2, inference]

## WTP, willingness to pay
- **Доказательство WTP №1**: наличие платных глобальных scientific intelligence и evidence tools с публичной подпиской показывает, что buyer в принципе платит за research acceleration и literature synthesis. [T2]
- **Доказательство WTP №2**: российские biopharma-лидеры публично подчеркивают собственные R&D-программы, клинические исследования и разработку новых молекул/препаратов, значит внутри организаций уже существуют команды, для которых стоимость ошибки в evidence review или landscape analysis высока. [T2: https://biocad.ru/ ; https://r-pharm.com/ ; https://generium.ru/ ; https://promomed.ru/ ; https://geropharm.com/ ; https://artgen.ru/]
- **Доказательство WTP №3**: hh-proxy по запросу `фармацевтическая аналитика клинические исследования` дал **15 вакансий**. Это не прямой purchase order, но показывает, что компании уже готовы платить за человеческий labor в этой функции, а значит automation/software budget theoretically monetizable. [T1/T2: HH proxy через internal demand endpoint]
- **Ограничение**: в РФ willingness to pay выглядит как **few-large-accounts market**, а не как массовый подписочный рынок. Без локальных pilot'ов и отрасловых референсов готовность к покупке будет низкой. [T2]

## Market sizing

### Методика и допущения
- Курс пересчета: **1 USD = 75,2370 ₽** по курсу Банка России, установленному с **21.04.2026**. [T1: https://www.cbr.ru/eng/currency_base/daily/]
- Top-down anchor: мировой рынок AI in pharma = **$4,35 млрд** в 2025 году. Для Causaly берем не весь этот рынок, а российскую долю pharma market и далее режем до сегмента R&D intelligence / evidence synthesis. [T2]
- Russia share proxy: российский фармрынок около **3,1 трлн ₽**, глобальный prescription drug market порядка **$1,6 трлн**. Это дает грубую долю РФ около **2,6%** от мирового фармрынка. [T2: https://dsm.ru/ ; https://www.evaluate.com/thought-leadership/pharma/evaluate-pharma-world-preview-report]
- Bottom-up buyer universe: около **95** адресуемых организаций в РФ, включая крупных производителей, биотех, разработчиков биосимиляров, вакцинных и инновационных игроков, а также selected CRO/clinical-heavy organizations. Это оценка, а не реестр; потому ниже используется консервативный penetration. [T2, inference]
- Средний enterprise ACV для РФ в base case: **27 млн ₽ в год**. Это эквивалент крупной multi-seat подписки плюс внедрение, фарм-онтологии, training и account support. Публичного прайса у Causaly нет, поэтому допущение выведено из enterprise positioning и ценовой вилки adjacent tools. [T2/T3, inference]

### Top-down
- **TAM (мир)** = **$4,35 млрд** ≈ **327,3 млрд ₽**. [T2 + T1 FX]
- **TAM (РФ)** = 327,3 млрд ₽ × 2,6% = **8,5 млрд ₽**. [T2 + inference]
- **SAM (РФ)** = 8,5 млрд ₽ × 18% = **1,53 млрд ₽**. Здесь segment fit = только инновационные pharma/biotech buyers и selected CRO, которым реально нужен advanced evidence synthesis, а не обычной market report subscription. [T2 + inference]
- **SOM Y1** = 1,53 млрд ₽ × 2% = **30,6 млн ₽**. [inference]
- **SOM Y3** = 1,53 млрд ₽ × 8% = **122,4 млн ₽**. [inference]

### Bottom-up
- **Total buyers** = **95**. [T2 + inference]
- **% with need** = **60%**. Это только организации с заметным R&D/clinical footprint и регулярной потребностью в evidence synthesis/competitive monitoring. [T2 + inference]
- **# active buyers** = 95 × 60% = **57**. [T2 + inference]
- **ARR avg** = **27 млн ₽/год**. [T2/T3 + inference]
- **SAM bottom-up** = 57 × 27 млн ₽ = **1,54 млрд ₽**. [T2 + inference]
- **SOM bottom-up Y1** = **1 клиент** + небольшой pilot expansion ≈ **27,0 млн ₽**. [inference]
- **SOM bottom-up Y3** = **4-5 клиентов** ≈ **121,5 млн ₽**. [inference]

| Метрика | Top-down | Bottom-up | Reconciliation | Preferred |
|---------|----------|-----------|----------------|-----------|
| TAM (мир) | 327,3 млрд ₽ [T2] | — | — | top-down |
| TAM (РФ) | 8,5 млрд ₽ [T2] | 2,57 млрд ₽* [T2] | diff=3,3x, но bottom-up excludes long tail buyers и CRO adjacency; для консервативности берем lower bound | lower |
| SAM (РФ) | 1,53 млрд ₽ [T2] | 1,54 млрд ₽ [T2] | diff < 1%, гипотезы сходятся | lower |
| SOM Y1 | 30,6 млн ₽ | 27,0 млн ₽ | diff=13%, нормально | **используем 27,0 млн ₽** |
| SOM Y3 | 122,4 млн ₽ | 121,5 млн ₽ | diff < 1%, нормально | **используем 121,5 млн ₽** |

\* Bottom-up TAM РФ = 95 buyers × 27 млн ₽ = 2,57 млрд ₽ как buyer-universe cross-check, а не full-market TAM.

### GTM 10 real buyers for bottom-up sanity check
1. **BIOCAD** [T2: https://biocad.ru/]
2. **Р-Фарм** [T2: https://r-pharm.com/]
3. **ГЕНЕРИУМ** [T2: https://generium.ru/]
4. **ПРОМОМЕД** [T2: https://promomed.ru/]
5. **Герофарм** [T2: https://geropharm.com/]
6. **Озон Фармацевтика** [T2: https://ozonpharm.ru/]
7. **Артген Биотех** [T2: https://artgen.ru/]
8. **Петровакс** [T2: https://petrovax.ru/]
9. **Биннофарм Групп** [T2: https://binnopharmgroup.ru/]
10. **Фармасинтез** [T2: https://pharmasyntez.com/]

Sanity check: при типичном цикле сделки **6-12 месяцев** модель Y1 = **27,0 млн ₽** означает фактически 1 крупного клиента или 1 крупного клиента + pilot expansion. Это реалистичнее, чем многодесятковый PLG-сценарий. SOM Y1 < 10% SAM, red flag overclaiming нет. [T2, inference]

## Profit Gate: проверка всех монетизационных сценариев

### Сценарий A. Self-serve seats для отдельных аналитиков
- Бенчмарк adjacent tools: от **0,9 тыс. ₽** до **7,4 тыс. ₽** за seat в месяц, premium patent intelligence до **75,2 тыс. ₽** в месяц. [T1/T2]
- Для РФ такой сценарий слаб, потому что buyer'ов мало, security/compliance высоки, а procurement идет сверху вниз, а не от individual scientist. [T2]
- Вывод: **FAIL**. [T2]

### Сценарий B. Team subscription для R&D / medical affairs группы
- Реалистичный чек: **6-15 млн ₽ ARR** на одну команду с 10-30 пользователями и limited services. [T2, inference]
- Чтобы получить **500 тыс. ₽ EBITDA/мес**, понадобятся минимум 3-5 активных контрактов плюс аккуратный cost control. Это сложно, но не невозможно. [T2, inference]
- Вывод: **на грани**, проходит только при хорошем локальном внедрении. [T2]

### Сценарий C. Enterprise platform для топ-biopharma
- Реалистичный чек: **18-30+ млн ₽ ARR** на одного клиента при multi-team access, pharma-specific ontology, onboarding, training, governance и support. [T2/T3, inference]
- При **2-4 клиентах** годовая выручка может составить **36-120 млн ₽**, что при gross margin порядка 60-70% и локальной команде из 3-5 человек уже позволяет выйти выше **500 тыс. ₽ EBITDA в месяц**. [T2, inference]
- Вывод: **PASS**. Это основной правдоподобный путь монетизации в РФ. [T2]

### Сценарий D. Service-led pilot + annual platform conversion
- Пилот/кастомный evidence project может служить wedge, после чего контракт переводится в платформенную подписку. [T2, inference]
- Этот путь снижает барьер входа, но увеличивает нагрузку на delivery. При 2-3 последующих annual conversion Profit Gate тоже достижим. [T2, inference]
- Вывод: **PASS WITH CAUTION**. [T2]

## Risks
- Прямой keyword demand в РФ остается **LOW**, и это главный риск рынка. [T2]
- Buyer universe узкий, локальные референсы критичны, цикл сделки будет длинным. [T2]
- На части задач buyer может довольствоваться более дешевыми literature/patent tools или ручной работой аналитиков. [T2]
- Без локального data residency, русского интерфейса и domain enablement product adoption будет тяжелым. [T2]

## Verdict for P4
- **P4 verdict**: **PASS WITH CAUTION**.
- Почему не reject: direct demand низкий, но WTP и buyer budget выглядят реальными в узком enterprise-сегменте; SAM по двум методикам сходится около **1,53-1,54 млрд ₽**, а Profit Gate проходит в сценарии **2-4 крупных контрактов**. [T1/T2]
- Почему не strong pass: рынок в РФ не сформирован как category-led, Telegram/distribution signals почти отсутствуют, а GTM будет тяжелым и account-based. [T2]
- Что проверять дальше на P5/P6: локализацию данных, доказуемость scientific moat против cheaper adjacent tools, список партнеров для pharma-enterprise sales и стоимость пилота. [T2]

Sources: T1=3, T2=18, T3=2. Primary evidence basis: T2.

> Market Pulse 2026-04-23: фиксирую растущий интерес по категории. В текущей выдаче видно больше свежих публикаций, вакансий, листингов и/или коммерческих сигналов, чем в прошлых срезах.


<!-- SOURCE: 03-solution.md -->

---
stage: solution
case: causaly-geo-expand-v2
date: 2026-04-22
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
Causaly как enterprise AI platform для biopharma R&D intelligence, evidence synthesis, competitive landscape analysis и research decision support при выходе в РФ.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. Продукт решает не абстрактную задачу «поиск научных статей», а дорогую проблему, как ускорить R&D hypothesis generation, evidence review, landscape analysis и monitoring для крупных фарморганизаций.
2. Реальный wedge в РФ выглядит не как массовый SaaS для исследователей, а как **knowledge layer для top-tier biopharma и clinical-heavy организаций**, где есть сложный research workflow, длинный цикл принятия решений и высокая цена пропущенного сигнала.
3. Самый правдоподобный вход в рынок, крупные инновационные фармкомпании, биотехи, selected CRO и организации с активным портфелем разработок, клинических программ или постоянной competitive intelligence функцией.
4. Главный риск, продукт может схлопнуться в дорогой research tooling или project-led knowledge service, если не доказать, что domain graph, workflow fit и скорость принятия решений реально лучше связки manual analyst + PubMed + cheaper evidence tools.

## 1. Какую проблему реально решает продукт

Causaly-подобный продукт продаёт не просто AI search, а устранение четырёх дорогих потерь:
- медленного evidence review и literature synthesis;
- неполного landscape visibility по таргетам, молекулам, trial activity и конкурентам;
- высокой зависимости от ручной работы исследователей, medical и strategy-команд;
- задержек в принятии R&D и portfolio decisions из-за разрозненных источников и knowledge silos.

Для ICP это painkiller только там, где already есть собственный R&D контур, pipeline review, мониторинг клинических исследований и несколько команд, которые регулярно потребляют scientific intelligence. Для обычного производителя дженериков или компании без сильной research-функции value proposition будет слабой.

## 2. Целевой ICP в РФ

### Primary ICP
- крупные инновационные фармкомпании;
- биотех-компании с активным research portfolio;
- производители с клиническими программами и собственным R&D;
- selected CRO и clinical-heavy research organizations;
- pharma groups, где есть central medical / R&D / BD intelligence функция.

### Фильтр на ICP
Клиент проходит, если одновременно есть:
1. регулярная потребность в literature review, evidence synthesis или pipeline monitoring;
2. несколько research, medical, strategy или BD-команд, которые работают с одним и тем же knowledge domain;
3. заметная цена ошибки или задержки в оценке target / trial / competitor landscape;
4. budget owner на уровне R&D, medical, strategy, innovation или digital transformation;
5. готовность покупать не только доступ к платформе, но и onboarding, ontology tuning, workflow embedding и поддержку.

### Нецелевой сегмент
- небольшие фармкомпании без research intensity;
- компании, где scientific review делается эпизодически;
- клиенты, которым достаточно PubMed, ручного поиска и дешёвых literature tools;
- организации без выделенного owner'а на R&D productivity или intelligence workflow.

## 3. Продуктовый wedge

### Core wedge
**Biopharma knowledge graph + research workflow layer**
- evidence synthesis для scientific и clinical questions;
- competitive intelligence и pipeline monitoring;
- поиск по disease, target, molecule, indication и trial activity;
- единый knowledge layer для R&D, medical и strategy-команд.

### Что делает wedge сильнее обычного AI-поиска
1. **Vertical depth**: продукт упакован под life sciences, а не под generic enterprise search.
2. **Ontology / graph advantage**: value не только в генерации ответа, а в структурировании domain knowledge.
3. **Workflow fit**: buyer покупает ускорение конкретных research decisions, а не просто доступ к LLM.
4. **Cross-team reuse**: одна knowledge база может использоваться несколькими функциями внутри фармы.
5. **Enterprise framing**: продукт можно продавать как decision-support platform, а не как дешёвую seat-based подписку.

Именно эта комбинация даёт шанс на premium enterprise cheque. Без неё кейс быстро превращается в «ещё один AI-поиск по научным статьям» с низким willingness to pay.

## 4. Как продукт должен выглядеть в РФ, чтобы пройти GTM

### Вариант, который, вероятно, не взлетит
- продажа как generic AI literature assistant;
- self-serve или bottom-up motion через отдельных исследователей;
- попытка идти в широкий фарма-рынок без фильтра на R&D maturity;
- отсутствие локальной адаптации по данным, языку, validation workflow и compliance.

### Вариант, который выглядит реалистично
- заход через enterprise pilot на одном monetizable research workflow, например competitor landscape, target scouting, clinical monitoring или evidence review;
- buyer сверху, head of R&D, chief scientific officer, medical director, strategy / BD lead;
- обязательная настройка под конкретные disease areas, pipeline questions и internal review process;
- KPI pilot: сокращение времени на evidence synthesis, скорость подготовки landscape review, покрытие источников, снижение ручного analyst effort;
- rollout как knowledge platform для нескольких research-команд после доказанного ROI.

## 5. Почему клиент будет покупать именно это, а не текущий стек

У локального клиента уже есть substitutes:
- PubMed, Google Scholar и открытые научные базы;
- ручная работа аналитиков и medical writers;
- дешёвые AI tools для literature review;
- кастомные внутренние knowledge repositories;
- внешние market research и consulting vendors.

Causaly-подобный продукт может выиграть только в трёх вещах:
1. **быстрее даёт usable scientific intelligence**, чем ручная research-команда;
2. **лучше структурирует domain knowledge**, чем generic AI search;
3. **остаётся repeatable platform layer**, а не превращается в набор ad hoc research services.

Если эти преимущества не доказаны, локальный buyer скорее оставит существующий research stack и купит дополнительный headcount или точечный консалтинг.

## 6. Delivery model

### Наиболее правдоподобная схема внедрения
1. аудит текущих research, medical и intelligence workflows;
2. выбор одного дорогого сценария для пилота;
3. настройка disease / molecule / competitor monitoring и evidence templates;
4. 6-12 недель pilot в одной research или medical команде;
5. сравнение скорости, качества и полноты анализа до и после;
6. rollout на соседние функции, например BD, portfolio strategy или clinical intelligence.

### Кто должен быть buyer'ом
- head of R&D;
- chief scientific officer;
- medical director;
- head of competitive intelligence;
- strategy / BD lead в biopharma;
- digital / innovation leader как co-buyer.

### Кто редко будет настоящим buyer'ом
- отдельный исследователь без бюджета;
- IT без научного спонсора;
- procurement без owner'а на research productivity.

## 7. Конкурентная позиция

### Против manual analyst + open sources
Преимущество возникает, если платформа действительно сокращает time-to-insight и уменьшает риск пропущенных сигналов.

### Против дешёвых literature / evidence tools
Шанс есть, если Causaly выигрывает не интерфейсом, а глубиной life sciences ontology, cross-source linking и пригодностью для enterprise R&D workflows.

### Против консультантов и research vendors
Преимущество возникает, если компания хочет internalize continuous intelligence, а не покупать разовые отчёты.

## 8. Основные риски solution-fit

1. **Narrow ICP risk**: платёжеспособный сегмент в РФ очень узкий.
2. **Localization risk**: западный продукт может плохо лечь на локальные процессы, данные и language expectations.
3. **Substitution risk**: часть value легко закрывается manual analysts, consultants или cheaper AI tools.
4. **Services risk**: внедрение может оказаться слишком кастомным и knowledge-heavy.
5. **Proof risk**: без измеримого ускорения research decisions продукт выглядит как expensive nice-to-have.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- сколько реально стоит enterprise sale в столь узкий pharma ICP;
- какой объём ontology tuning, support и services нужен на одного клиента;
- сохраняется ли software-like gross margin после локализации и внедрения;
- сколько пилотов нужно конвертировать в annual rollout для выхода на 500k+ EBITDA/мес;
- не дешевле ли target-клиенту держать manual team + точечные external vendors.

## Итог для пайплайна

**P4 пройден условно.**

Кейс имеет внятный solution thesis только как enterprise biopharma knowledge and intelligence layer для top-tier research-heavy организаций, а не как массовый AI research SaaS. Продолжать дальше имеет смысл, если на economics подтвердится, что локальное внедрение остаётся повторяемым, gross margin не разрушается кастомизацией, а buyer действительно готов платить за ускорение R&D и evidence workflows, а не просто за удобный поиск.

<!-- SOURCE: 04-economics.md -->

---
stage: economics
case: causaly-geo-expand-v2
date: 2026-04-22
analyst: branch-models-lead
verdict: PASS_WITH_CAUTION
confidence: medium
---

# 04-economics

## Кейс
Causaly-подобная enterprise AI platform для biopharma R&D intelligence, evidence synthesis и competitive monitoring на рынке РФ.

## Итог
**Статус: PASS WITH CAUTION.**

Экономика собирается только в узком enterprise motion: few-large-accounts, длинный sales cycle, высокий fully-loaded CAC и дорогая команда. При этом при базовом чеке **2,25 млн ₽ MRR на клиента** и gross margin около **62,7%** модель выходит на break-even примерно на **5 клиентах**, а при **50 клиентах** EBITDA многократно выше порога 500 тыс. ₽/мес. Profit Gate не срабатывает.

## 1. Базовые допущения модели

| Параметр | Base case | Комментарий |
|---|---:|---|
| ICP | крупные biopharma / инновационные фармкомпании РФ | few-large-accounts market |
| ACV | 27,0 млн ₽/год | из 02-demand, enterprise platform + onboarding |
| MRR на клиента | 2,25 млн ₽/мес | 27,0 / 12 |
| COGS на клиента | 0,84 млн ₽/мес | cloud + data + support + compliance |
| Gross profit на клиента | 1,41 млн ₽/мес | 2,25 - 0,84 |
| Gross margin | 62,7% | investable для enterprise software + services |
| Logo churn rate | 1,0%/мес | консервативно для enterprise B2B SaaS benchmark |
| Lifetime | 100 мес | 1 / 1,0% |
| CAC multiplier | x2,7 | regulated/healthtech B2B по policy band x2,5-x3,0 |
| New paying customers | 0,6 / мес | ~7 новых клиентов в год после разгона GTM |

## 2. Business process table, от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Target account list и enrichment | SDR + biopharma analyst | HH/отраслевые базы, CRM, LinkedIn-аналоги, ручной ресерч | 1,5 ч на аккаунт | 4 500 | средняя |
| 2 | Первичный outbound / warm intro | SDR | CRM + email sequences + Telegram/почта | 20 мин | 1 000 | высокая |
| 3 | Qualification call | AE | CRM + Zoom/Meet | 45 мин | 3 000 | средняя |
| 4 | Discovery с buyer group | AE + analyst | Zoom, шаблон discovery, CRM | 1,5 ч | 9 000 | низкая |
| 5 | Demo knowledge graph / use-case mapping | AE + solutions/CTO | demo env, slides, sandbox | 2 ч | 16 000 | низкая |
| 6 | Security/compliance review | CTO + legal | security docs, DPA, checklist | 8 ч | 42 000 | низкая |
| 7 | Pilot scoping | AE + analyst + CTO | proposal, CRM, shared docs | 4 ч | 24 000 | низкая |
| 8 | Paid pilot / procurement | AE + finance | договор, ЭДО, invoicing | 10 раб. дней cycle time | 35 000 | низкая |
| 9 | Onboarding данных и ontology tuning | analyst + backend + CSM | ETL, cloud, PM tool | 20 ч | 95 000 | средняя |
| 10 | Enablement и training | CSM + analyst | LMS, workshop, docs | 6 ч | 22 000 | средняя |
| 11 | Monthly evidence runs + support | analyst + CSM | product + ticketing + BI | ежемесячно 10-12 ч | 110 000 | средняя |
| 12 | Счёт, оплата, renewal follow-up | finance + AE + CSM | 1С/ЭДО/CRM | 2 ч | 8 000 | высокая |

**Вывод:** процесс дорогой и длинный, поэтому raw CAC нельзя считать только по рекламе. Это типичный regulated enterprise sale с множеством касаний, пилотом, security review и procurement.

## 3. COGS breakdown per client/month

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Cloud / inference / storage | 220 000 | выделенная инфраструктура, RAG, secure storage |
| Data / literature / enrichment licenses | 180 000 | внешние данные и доступы |
| Customer Success allocation | 90 000 | доля CSM на 6-8 клиентов |
| Biopharma analyst allocation | 160 000 | доля аналитика на ongoing evidence workflows |
| Support / implementation reserve | 120 000 | onboarding, bugfix, taxonomy updates |
| Security / compliance / audit reserve | 70 000 | DPA, policy, security ops |
| Payment/admin variable | 0 000 | для B2B invoice пренебрежимо |
| **Итого COGS** | **840 000** |  |

**MRR на клиента:** 2 250 000 ₽  
**Gross profit на клиента:** 1 410 000 ₽  
**Gross margin:** **62,7%**

## 4. CAC by acquisition channel с funnel conversion

### 4.1 Channel funnels

| Канал | Top-of-funnel / мес | Meeting rate | SQL rate | Pilot rate | Win rate | New paying customers / мес | Fully-loaded spend / мес, ₽ | CAC, ₽ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Outbound ABM | 180 target accounts | 7,8% | 28,6% от meetings | 25,0% от SQL | 25,0% от pilots | 0,25 | 1 890 000 | 7 560 000 |
| Events / partnerships | 40 leads | 20,0% | 37,5% | 33,3% | 20,0% | 0,20 | 810 000 | 4 050 000 |
| Inbound content / referrals | 20 inbound leads | 30,0% | 33,3% | 50,0% | 25,0% | 0,15 | 756 000 | 5 040 000 |

### 4.2 Blended fully-loaded CAC

| Показатель | Значение |
|---|---:|
| Total raw acquisition spend / мес | 1 341 000 ₽ |
| CAC multiplier | x2,7 |
| Fully-loaded acquisition spend / мес | 3 620 700 ₽ |
| New paying customers / мес | 0,6 |
| **Blended fully-loaded CAC** | **6 034 500 ₽** |

### 4.3 Компоненты fully-loaded CAC

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads / niche media | 250 000 | узкий digital + retargeting + sponsor placements | T4 |
| Outbound team FOT (SDR + AE attributed to new) | 489 000 | SDR 234 000 + 50% AE cost 255 000 | T3 |
| Marketing team FOT (partial allocation) | 182 000 | demand gen / content lead 140 000 gross × 1,3 social × 100% acquisition | T3 |
| Tools / CRM / data enrichment | 120 000 | CRM + sequencing + data providers + webinar tools | T5 |
| Events / partnerships | 300 000 | конференции, roundtables, industry associations | T6 |
| Overhead multiplier | 2 279 700 | raw 1 341 000 × (2,7 - 1,0) | T7 |
| **Итого fully-loaded spend / мес** | **3 620 700** |  |  |

**Sanity check against benchmark:** blended CAC **6,03 млн ₽** выше generic healthtech B2B benchmark из внутренней рамки, но это объяснимо, потому что здесь одновременно **enterprise + regulated + long cycle + pilot + security review**. Для такого motion заниженный CAC выглядел бы менее правдоподобно, чем высокий.

## 5. LTV с churn rate

### 5.1 Churn benchmark
- В качестве benchmark использую **SaaS Capital, 2025 B2B SaaS Retention Benchmarks**: у enterprise B2B SaaS retention заметно лучше, чем у SMB, а logo churn обычно однозначный и низкий относительно mid-market/SMB. [T2]
- Для РФ и для узкого regulated enterprise сегмента беру **консервативный monthly logo churn = 1,0%**, что эквивалентно около **11,4% annual churn**. Это не best case, а с запасом на длинный procurement cycle и ограниченный buyer universe. [T2][inference]

### 5.2 Расчёт LTV
Формула:  
**LTV = MRR × Gross Margin % / Churn rate**

Подстановка:  
2 250 000 × 62,7% / 1,0% = **141 000 000 ₽**

| Метрика | Значение |
|---|---:|
| MRR на клиента | 2 250 000 ₽ |
| Gross margin | 62,7% |
| Churn rate | 1,0% / мес |
| Lifetime | 100 мес |
| **LTV** | **141,0 млн ₽** |

## 6. LTV/CAC ratio

| Метрика | Значение |
|---|---:|
| LTV | 141,0 млн ₽ |
| Blended fully-loaded CAC | 6,03 млн ₽ |
| **LTV/CAC** | **23,4x** |

**Вывод:** существенно выше investment-grade порога **3:1**.

## 7. CAC Payback

Формула из standing order:  
**CAC Payback = CAC / MRR per customer**

6 034 500 / 2 250 000 = **2,68 месяца**

Это намного лучше базового порога **<12 месяцев** и комфортно проходит даже enterprise-threshold.

## 8. Contribution Margin %

В этой модели contribution margin считаю как вклад после прямых delivery costs, но до fixed opex.

| Метрика | ₽ | % от выручки |
|---|---:|---:|
| Revenue / client / month | 2 250 000 | 100,0% |
| COGS / client / month | 840 000 | 37,3% |
| **Contribution Margin / client / month** | **1 410 000** | **62,7%** |

## 9. Team & FOT

### 9.1 Полная команда

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO | продажи крупных аккаунтов, fundraising, partnerships | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | product architecture, security, enterprise delivery | 550 000 | 165 000 | 715 000 |
| Senior Backend 1 | ingestion, APIs, data pipelines | 420 000 | 126 000 | 546 000 |
| Senior Backend 2 | product backend, integrations | 420 000 | 126 000 | 546 000 |
| ML Engineer | retrieval, ranking, synthesis quality | 500 000 | 150 000 | 650 000 |
| DevOps | infra, observability, security hardening | 350 000 | 105 000 | 455 000 |
| Frontend | researcher workflows, dashboards | 300 000 | 90 000 | 390 000 |
| SDR | prospecting и initial qualification | 180 000 | 54 000 | 234 000 |
| AE | discovery, proposal, close | 400 000 | 120 000 | 520 000 |
| Customer Success | onboarding, adoption, renewals | 260 000 | 78 000 | 338 000 |
| Biopharma analyst | domain setup, ontology, evidence workflows | 280 000 | 84 000 | 364 000 |
| **Итого** |  |  |  | **5 603 000** |

### 9.2 Таблица найма, hiring realism

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 (founder) | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2,5 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 420 000 | 1,5 | 1,5 | 126 000 | 546 000 |
| ML Engineer | 1 | 500 000 | 2,5 | 2 | 150 000 | 650 000 |
| DevOps | 1 | 350 000 | 1,5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 180 000 | 1 | 1 | 54 000 | 234 000 |
| AE | 1 | 400 000 | 1,5 | 2,5 | 120 000 | 520 000 |
| Customer Success | 1 | 260 000 | 1 | 1 | 78 000 | 338 000 |
| Biopharma analyst | 1 | 280 000 | 1,5 | 1,5 | 84 000 | 364 000 |

### 9.3 Cumulative FOT timeline M1-M12

| Месяц | Кто подключается | FOT monthly, ₽ |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | + CTO | 1 560 000 |
| M3 | + AE, biopharma analyst | 2 444 000 |
| M4 | + Senior Backend 1 | 2 990 000 |
| M5 | + ML Engineer | 3 640 000 |
| M6 | + SDR | 3 874 000 |
| M7 | + Customer Success | 4 212 000 |
| M8 | + DevOps | 4 667 000 |
| M9 | + Senior Backend 2 | 5 213 000 |
| M10 | + Frontend | 5 603 000 |
| M11 | без новых ролей | 5 603 000 |
| M12 | без новых ролей | 5 603 000 |

**Sanity checks:**
- 5+ новых людей в первый месяц нет.
- Полный FOT команды 5,6 млн ₽/мес выглядит реалистично для enterprise AI + biotech vertical.
- План старта менее 10 млн ₽ был бы неправдоподобен; здесь только burn до break-even около 29,5 млн ₽.

## 10. Fixed costs breakdown

| Статья fixed cost | ₽/мес | Комментарий |
|---|---:|---|
| G&A / finance / legal | 300 000 | бухгалтерия, юрсопровождение, procurement support |
| Shared infra not in COGS | 650 000 | core platform, dev/test, security tooling |
| Office / travel / admin | 180 000 | поездки к клиентам, встречи, базовый офис |
| Insurance / audit / compliance reserve | 220 000 | security, due diligence, audits |
| **Итого fixed non-FOT** | **1 350 000** |  |

**Fixed costs including full team FOT:**  
5 603 000 + 1 350 000 = **6 953 000 ₽/мес**

## 11. Break-even

### 11.1 Break-even by client count

Формула:  
**Break-even clients = Fixed costs / Contribution per client**

6 953 000 / 1 410 000 = **4,93 клиента**

Округляя вверх: **5 клиентов**.

### 11.2 Break-even by month

Предполагаем revenue ramp: M7 = 1 клиент, M8 = 2, M9 = 3, M10 = 4, M11 = 5, M12 = 6.

| Месяц | Клиентов | GP, ₽ | Fixed costs, ₽ | EBITDA до налога, ₽ |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 1 395 000 | -1 395 000 |
| M2 | 0 | 0 | 2 110 000 | -2 110 000 |
| M3 | 0 | 0 | 2 994 000 | -2 994 000 |
| M4 | 0 | 0 | 3 740 000 | -3 740 000 |
| M5 | 0 | 0 | 4 390 000 | -4 390 000 |
| M6 | 0 | 0 | 4 624 000 | -4 624 000 |
| M7 | 1 | 1 410 000 | 5 212 000 | -3 802 000 |
| M8 | 2 | 2 820 000 | 5 667 000 | -2 847 000 |
| M9 | 3 | 4 230 000 | 6 563 000 | -2 333 000 |
| M10 | 4 | 5 640 000 | 6 953 000 | -1 313 000 |
| M11 | 5 | 7 050 000 | 6 953 000 | **+97 000** |
| M12 | 6 | 8 460 000 | 6 953 000 | **+1 507 000** |

**Break-even month:** **M11**

## 12. Burn-to-breakeven и cash runway

| Показатель | Значение |
|---|---:|
| Кумулятивный burn до первого положительного месяца | **29,5 млн ₽** |
| Startup capital base case | **60,0 млн ₽** |
| Средний burn до M10 | ~2,95 млн ₽/мес |
| Cash runway при таком burn | **~20 месяцев** |

**Вывод:** для такого кейса нужен не маленький seed, а нормальный runway. Capital need заметный, но не экстремальный для regulated enterprise AI.

## 13. Profit Gate

### Проверка mandatory conditions
1. **EBITDA < 500K/mo achievable even at 50 clients?**  
   Нет. При 50 клиентах contribution = 50 × 1,41 млн ₽ = **70,5 млн ₽/мес**. После fixed costs 6,95 млн ₽ остаётся порядка **63,5 млн ₽/мес EBITDA**.
2. **LTV/CAC < 1:1?**  
   Нет. **23,4x**.

**Итог:** Profit Gate **не срабатывает**, кейс **не уходит в rejected**.

## 14. Главные экономические риски
- Слишком узкий buyer universe, поэтому pipeline slippage сразу бьёт по runway.
- Если локальный чек опустится ниже **1,6-1,8 млн ₽ MRR**, break-even уйдёт с 5 клиентов к 6-7.
- Если delivery станет service-heavy и COGS поднимется выше **1,1 млн ₽/клиент/мес**, gross margin просядет ниже 52%.
- Enterprise procurement в regulated vertical может растянуть payback не по формуле, а по cash timing, даже если unit economics выглядят сильными на бумаге.

## 15. Verdict
**P5 verdict: PASS WITH CAUTION.**

Модель инвестиционно пригодна только как высокочековый enterprise product с жёсткой дисциплиной по COGS и account-based sales. Это не PLG и не широкий mid-market SaaS. Но если команда реально закрывает 5+ клиентов с ACV около 27 млн ₽, экономика выглядит сильной.

## Источники
- **T1**. `pipeline/cases/causaly-geo-expand-v2/02-demand.md`.
- **T2**. SaaS Capital, B2B SaaS retention benchmarks, доступ 2026-04-22: https://www.saascapital.com/blog-posts/retention-benchmarks-for-private-b2b-saas-companies/
- **T3**. HH.ru market scan по зарплатам и вакансиям Москвы/СПб, доступ 2026-04-22: https://hh.ru/search/vacancy?text=CTO ; https://hh.ru/search/vacancy?text=Senior+Backend ; https://hh.ru/search/vacancy?text=ML+Engineer ; https://hh.ru/search/vacancy?text=DevOps ; https://hh.ru/search/vacancy?text=SDR ; https://hh.ru/search/vacancy?text=Account+Executive ; https://hh.ru/search/vacancy?text=Customer+Success
- **T4**. Industry media / niche paid placements benchmark, доступ 2026-04-22: https://vc.ru/marketing
- **T5**. CRM/tooling benchmarks, доступ 2026-04-22: https://www.bitrix24.ru/prices/ ; https://sbercrm.com/tariffs/
- **T6**. Pharma / biotech event participation cost proxy, доступ 2026-04-22: https://pharmprosvet.ru/ ; https://pharmatechexpo.ru/
- **T7**. Internal policy benchmark for regulated CAC multiplier, current run instruction 2026-04-22.


<!-- SOURCE: 05-critic.md -->

## SECTION A. Finance PnL

### A1. Допущения модели
- ARPA / MRR на клиента: **2 250 000 ₽/мес**.
- COGS на клиента: **840 000 ₽/мес**.
- Gross profit на клиента: **1 410 000 ₽/мес**.
- Contribution margin на клиента: **1 410 000 ₽/мес**.
- Fixed costs в модели: **6 953 000 ₽/мес**, включая team FOT **5 603 000 ₽/мес** и fixed non-FOT **1 350 000 ₽/мес**.
- Налоговая логика РФ: **УСН 6% с выручки**, **IT-льгота 3% с выручки** при аккредитации Минцифры, **ОСНО 20% налога на прибыль**; при ОСНО также появляется **НДС 20%**, что ухудшает cash conversion.
- Страховые взносы **~30% к ФОТ** уже включены в FOT и fixed costs, повторно не добавляются.
- Сценарии new clients / churn:
  - **Base:** new clients = 0,0,0,0,0,0,1,1,1,1,1,1; churn **1.0%/мес**.
  - **Optimistic:** new clients = 0,0,0,0,0,1,1,1,1,1,1,1; churn **0.8%/мес**.
  - **Pessimistic:** new clients = 0,0,0,0,0,0,0,1,1,1,1,1; churn **1.5%/мес**.
- Cumulative cash показан от **0 ₽** как накопленный cash deficit, то есть потребность в стартовом капитале до безубыточности.

### A2. PnL 12 месяцев, scenario: Base
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 1 |
| Total clients | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.99 | 2.97 | 3.94 | 4.90 | 5.85 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 2 250 000 | 4 477 500 | 6 682 725 | 8 865 898 | 11 027 239 | 13 166 966 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 840 000 | 1 671 600 | 2 494 884 | 3 309 935 | 4 116 836 | 4 915 667 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 1 410 000 | 2 805 900 | 4 187 841 | 5 555 963 | 6 910 403 | 8 251 299 |
| GM% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 62.7% | 62.7% | 62.7% | 62.7% | 62.7% | 62.7% |
| Fixed costs, ₽ | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 |
| EBITDA, ₽ | -6 953 000 | -6 953 000 | -6 953 000 | -6 953 000 | -6 953 000 | -6 953 000 | -5 543 000 | -4 147 100 | -2 765 159 | -1 397 037 | -42 597 | 1 298 299 |
| Cash burn, ₽ | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 5 543 000 | 4 147 100 | 2 765 159 | 1 397 037 | 42 597 | 0 |
| Cumulative cash, ₽ | -6 953 000 | -13 906 000 | -20 859 000 | -27 812 000 | -34 765 000 | -41 718 000 | -47 261 000 | -51 408 100 | -54 173 259 | -55 570 296 | -55 612 893 | -55 612 893 |

### A3. PnL 12 месяцев, scenario: Optimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
| Total clients | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.99 | 2.98 | 3.95 | 4.92 | 5.88 | 6.83 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 2 250 000 | 4 482 000 | 6 696 144 | 8 892 575 | 11 071 434 | 13 232 863 | 15 377 000 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 840 000 | 1 673 280 | 2 499 894 | 3 319 895 | 4 133 335 | 4 940 269 | 5 740 747 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 1 410 000 | 2 808 720 | 4 196 250 | 5 572 680 | 6 938 099 | 8 292 594 | 9 636 253 |
| GM% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 62.7% | 62.7% | 62.7% | 62.7% | 62.7% | 62.7% | 62.7% |
| Fixed costs, ₽ | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 |
| EBITDA, ₽ | -6 953 000 | -6 953 000 | -6 953 000 | -6 953 000 | -6 953 000 | -5 543 000 | -4 144 280 | -2 756 750 | -1 380 320 | -14 901 | 1 339 594 | 2 683 253 |
| Cash burn, ₽ | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 5 543 000 | 4 144 280 | 2 756 750 | 1 380 320 | 14 901 | 0 | 0 |
| Cumulative cash, ₽ | -6 953 000 | -13 906 000 | -20 859 000 | -27 812 000 | -34 765 000 | -40 308 000 | -44 452 280 | -47 209 030 | -48 589 350 | -48 604 251 | -48 604 251 | -48 604 251 |

### A4. PnL 12 месяцев, scenario: Pessimistic
| Metric | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| New clients | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 |
| Total clients | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 | 1.00 | 1.98 | 2.96 | 3.91 | 4.85 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 2 250 000 | 4 466 250 | 6 649 256 | 8 799 517 | 10 917 525 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 840 000 | 1 667 400 | 2 482 389 | 3 285 153 | 4 075 876 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 410 000 | 2 798 850 | 4 166 867 | 5 514 364 | 6 841 649 |
| GM% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 0.0% | 62.7% | 62.7% | 62.7% | 62.7% | 62.7% |
| Fixed costs, ₽ | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 |
| EBITDA, ₽ | -6 953 000 | -6 953 000 | -6 953 000 | -6 953 000 | -6 953 000 | -6 953 000 | -6 953 000 | -5 543 000 | -4 154 150 | -2 786 133 | -1 438 636 | -111 351 |
| Cash burn, ₽ | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 6 953 000 | 5 543 000 | 4 154 150 | 2 786 133 | 1 438 636 | 111 351 |
| Cumulative cash, ₽ | -6 953 000 | -13 906 000 | -20 859 000 | -27 812 000 | -34 765 000 | -41 718 000 | -48 671 000 | -54 214 000 | -58 368 150 | -61 154 283 | -62 592 919 | -62 704 270 |

### A5. Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net
#### Waterfall на 1 клиента / месяц
- **ARPA:** 2 250 000 ₽
- **COGS:** 840 000 ₽
- **Gross profit:** 1 410 000 ₽
- **Contribution:** 1 410 000 ₽

#### Waterfall на EBITDA break-even уровне 5 клиентов
- **Revenue:** 11 250 000 ₽/мес
- **COGS:** 4 200 000 ₽/мес
- **Gross profit:** 7 050 000 ₽/мес
- **Contribution:** 7 050 000 ₽/мес
- **EBITDA:** **97 000 ₽/мес**

#### Net после налогов
- **УСН 6%:** EBITDA 97 000 - налог 675 000 = **-578 000 ₽/мес**
- **IT-льгота 3%:** EBITDA 97 000 - налог 337 500 = **-240 500 ₽/мес**
- **ОСНО 20%:** налог на прибыль ≈ 19 400 ₽, net ≈ **77 600 ₽/мес**, но дополнительно возникает **НДС 20%**

#### Waterfall на contribution safety уровне 5 клиентов
- **Revenue:** 11 250 000 ₽/мес
- **COGS:** 4 200 000 ₽/мес
- **Gross profit:** 7 050 000 ₽/мес
- **Contribution:** 7 050 000 ₽/мес
- **EBITDA:** **97 000 ₽/мес**
- **Net profit при УСН 6%:** **-578 000 ₽/мес**
- **Net profit при IT-льготе 3%:** **-240 500 ₽/мес**
- **Net profit при ОСНО 20%:** **77 600 ₽/мес** до учёта кассового эффекта НДС

### A6. Cash flow: startup_capital_to_bep_rub
| Scenario | EBITDA break-even month | startup_capital_to_bep_rub | Комментарий |
|---|---:|---:|---|
| Optimistic | M11 | 48 604 251 ₽ | самый сильный ramp, безубыточность достигается в горизонте первого года |
| Base | M12 | 55 612 893 ₽ | базовый сценарий требует полного enterprise execution и крупного runway |
| Pessimistic | M13 | 62 704 270 ₽ | в 12-месячном окне остаётся отрицательный EBITDA и нужен дополнительный капитал |

### A7. Налоговая модель РФ
- **УСН 6% с выручки:** самый простой режим, но для enterprise-чека в 2,25 млн ₽/мес съедает значимую часть EBITDA до масштаба 6+ клиентов.
- **IT-льгота 3%:** заметно лучше для post-tax прибыли, если есть аккредитация Минцифры и соблюдены требования к профильной выручке.
- **ОСНО 20%:** налог на прибыль может быть мягче после выхода в плюс, но добавляет **НДС 20%** и ухудшает cash flow на длинном enterprise cycle.
- **Страховые взносы ~30% к ФОТ:** уже учтены внутри team FOT **5 603 000 ₽/мес**.
- Для этого кейса базово рациональнее считать **УСН / IT-льготу**, а не ОСНО.

### A8. Break-even по client count и по месяцам
| Scenario | EBITDA break-even clients | Contribution break-even clients | Break-even month | Комментарий |
|---|---:|---:|---:|---|
| Optimistic | 5 | 5 | M11 | проходит break-even в M11 и даёт запас по EBITDA уже к M12 |
| Base | 5 | 5 | M12 | выходит в плюс только к M12, запас минимальный |
| Pessimistic | 5 | 5 | M13 | в пределах M1-M12 не выходит в плюс, break-even только после M12 |

<!-- P6A-DONE -->

## SECTION B. Finance Risk + Competitor

### B1. Sensitivity analysis, EBITDA через 12 месяцев
Допущение для stress-теста: base ramp из SECTION A сохраняется, но в сценарии **CAC x2** net-new logo intake после M6 режется с **1,0** до **0,5** клиента в месяц, в сценарии **Churn x2** churn растёт с **1,0%** до **2,0%** в месяц, в сценарии **Price -30%** ARPA падает с **2,25 млн ₽** до **1,575 млн ₽** при прежнем COGS **0,84 млн ₽**. [T1]

| Сценарий | Ключевое изменение | Клиенты @M12 | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---:|---|
| Base | без изменений | 5,85 | 1 298 299 | минимальный запас прочности |
| Sens1 | CAC x2 | 2,93 | -2 827 351 | pipeline резко не добирает до break-even |
| Sens2 | Churn x2 | 5,71 | 1 095 112 | больно, но модель ещё жива |
| Sens3 | Price -30% | 5,85 | -2 651 791 | pricing power, а не churn, главный single-point-of-failure |

**Вывод:** для этого кейса самый опасный shock не churn, а **price compression** и/или **ухудшение CAC**, потому что рынок узкий и enterprise sales cycle длинный. [T1][T2]

### B2. Monte Carlo Lite, confidence intervals @M24

#### Inputs, triangular distribution
| Переменная | min | mode | max | Источник |
|------------|-----|------|-----|----------|
| CAC, ₽ | 4 050 000 | 6 034 500 | 8 400 000 | [T1] |
| Monthly churn, % | 0,6% | 1,0% | 2,0% | [T1][T2] |
| ARPU, ₽/мес | 1 800 000 | 2 250 000 | 2 700 000 | [T1][T3] |
| Conversion rate lead→paid, % | 0,20% | 0,25% | 0,40% | [T1] |
| Time-to-hire, месяцев | 1,0 | 1,6 | 3,0 | [T1] |

#### Метод
Полную 1000-итерационную симуляцию здесь не запускал, использовал **9 комбинаций** min/mode/max + mixed cases как Monte Carlo Lite proxy. p10 = нижний хвост, p50 = median case, p90 = верхний хвост. Для runway взят стартовый капитал **60 млн ₽** из economics baseline. [T1]

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24, ₽/мес | -255 773 | 7 047 136 | 23 599 912 | 23 855 685 |
| CAC payback, мес | 1,5 | 2,68 | 4,67 | 3,17 |
| LTV/CAC | 5,71x | 23,37x | 76,54x | 70,83x |
| Cash runway, мес | 9 | 10 | 36 | 27 |

**Интерпретация правил:**
1. **p10 EBITDA < 0** → kill criterion #1 срабатывает, есть риск непрохождения liquidity stress. [T1]
2. **p50 EBITDA = 7,05 млн ₽/мес** → median-case EBITDA Gate проходит. [T1]
3. **Разброс слишком широкий**: при отрицательном p10 формальное p90/p10 неинтерпретируемо, но dispersion фактически выше допустимого и требует даунгрейда confidence. [inference]
4. **Range width по LTV/CAC = 70,83x > 8** → модель хрупкая, ключевая нестабильность сидит в pricing/CAC/churn. [T1]

### B3. Competitor deep-dive

#### Западные конкуренты
Оценка доли ниже, это **не audited market share всего фарм-IT**, а грубая доля в адресуемом сегменте scientific intelligence / evidence workflow для крупных pharma accounts, выведенная из публичных customer claims, product breadth и enterprise traction. [T4][T5][T6]

| Конкурент | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| BenchSci | сильный biomarker / preclinical workflow fit, крупные pharma logos, AI-assisted experiment intelligence [T4] | уже, чем full evidence + market landscape layer; сильнее в wet-lab use cases, чем в широком portfolio intelligence [T4] | 15-20% западного premium subsegment | Causaly шире покрывает literature, disease, target, trial и competitor intelligence в одном knowledge layer |
| SciBite (Elsevier) | мощная ontology/NLP база, интеграция в Elsevier stack, высокая enterprise credibility [T5] | тяжёлое внедрение, UX часто воспринимается как infra/data layer, а не быстрый decision tool [T5] | 10-15% | Causaly проще продаётся как outcome-oriented platform, а не как инфраструктурный semantic engine |
| PatSnap | силён в patent/innovation intelligence, широкий R&D + IP narrative, глобальная коммерческая машина [T6] | менее deep в biomedical evidence synthesis, чем vertical-first players; risk of being too broad [T6] | 8-12% | Causaly глубже в life-sciences ontology и research workflows, а не только patent/innovation monitoring |

#### Российские и российско-корневые конкуренты / substitutes
В РФ прямого 1:1 аналога Causaly почти нет, поэтому ниже не только прямые конкуренты, но и **adjacent substitutes**, на которые реально может уйти budget: drug discovery AI, clinical decision AI, biomedical analytics platforms. [T7][T8][T9][T10]

| Конкурент | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| Insilico Medicine | сильный brand в AI drug discovery, глубокий R&D narrative, узнаваемость у scientific buyers [T7][T8] | фокус больше на discovery pipeline и molecule generation, а не на enterprise evidence workspace для российских pharma teams [T7] | 5-8% узкого RU/CEE innovation-AI budget | Causaly ближе к daily intelligence workflow и быстрее monetizes как decision-support layer |
| Webiomed / К-Скай | локальная data residency, работа с РФ healthcare contour, сильнее в клинданных и decision support [T9][T10] | не core biopharma R&D intelligence platform, меньше fit для target/pipeline/competitor landscape задач [T9] | 8-10% RU medical-AI software budget, но низкая доля именно в R&D intelligence | Causaly лучше закрывает pharma research workflow, а не hospital analytics |
| Data MATRIX | локальная биомедицинская/clinical data инфраструктура, понятный Skolkovo-proofed B2B контур [T11] | ближе к data platform и trial/data operations, чем к scientific knowledge graph [T11] | 3-5% | Causaly даёт более готовый insight layer для R&D и strategy |
| OncoBox | сильная научная вертикаль, онкология, биоинформатика, персонализированная медицина [T12][T13] | очень узкий therapeutic scope; не general-purpose R&D intelligence platform [T12] | 1-3% | Causaly шире по disease coverage и buyer universe |

**Итог по конкуренции:** главная угроза в РФ, это не один сильный прямой конкурент, а комбинация **adjacent локальных платформ + manual analysts + дешёвые западные tools + внутренние BI/knowledge stacks**. Это повышает риск price compression. [T2][T7][T9]

### B4. Risk matrix
| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Не удаётся нанять сильного biopharma analyst | med | high | time-to-hire > 3 мес, срывы ontology setup | заранее building bench, fractional experts, advisor pool |
| Operational | Product quality проседает на сложных evidence queries | med | high | пилотные команды возвращаются к ручному search | golden datasets, HITL review, narrow high-value workflows first |
| Operational | Зависимость от внешних LLM/API поставщиков | high | high | рост latency/cost, недоступность API, ухудшение answer quality | multi-model routing, локальный fallback, prompt+RAG hardening |
| Market | Buyer universe в РФ слишком узкий | high | high | <10 qualified accounts в активном pipeline после 90 дней | идти через top-20 pharma list, CRO adjacency, партнёров и service-led entry |
| Market | Price compression из-за cheaper tools и manual teams | high | high | скидки >25%, частые сравнения с Elicit/Undermind/manual analyst | value-based packaging, ROI proof, bundled onboarding, multi-team contracts |
| Market | Пилоты не конвертируются в annual rollout | med | high | pilot win rate < 25%, много «интересно, но не сейчас» | жёсткие pilot KPI, paid pilot, executive sponsor до старта |
| Regulatory | Требования 152-ФЗ по ПДн и data residency блокируют deal | med | high | security/legal review > 8 недель, возражения по хранению данных | on-prem/VPC option, RU hosting, DPA + data mapping |
| Regulatory | 115-ФЗ / compliance / AML-процедуры тормозят enterprise procurement | low | med | финслужба клиента требует расширенный KYC пакет | шаблоны compliance docs, прозрачная структура платежей, local entity |
| Regulatory | Санкции/SaaS restrictions ломают доступ к западным компонентам | high | high | отказ в продлении лицензий, проблемы с оплатой зарубежным вендорам | vendor diversification, local mirrors, критичные компоненты без single vendor |
| Financial | Cash runway оказывается короче 12 мес | high | high | monthly burn > 5 млн ₽ дольше M10, нет 2 закрытий к M12 | tranche-based hiring, burn gates, stop hiring until 1st paid pilot |
| Financial | USD/RUB volatility поднимает cloud и data costs | med | med | COGS/клиент > 1,0 млн ₽ два месяца подряд | рублёвые контракты, hedge reserve, quarterly repricing |
| Financial | Инфляция и налоги съедают EBITDA | med | med | payroll inflation > 15% y/y, ухудшение post-tax margin | annual repricing clauses, льготы IT, control non-FOT |
| Black swan | Резкое усиление санкций/военный шок | med | high | freeze budgets, перенос проектов, отмена трансграничных оплат | фокус на local entity, shorten sales cycle, reserve cash buffer |
| Black swan | Отключение ключевого LLM или научного data provider | med | high | недоступность core search/generation > 72 ч | резервные провайдеры, cached corpora, graceful degradation mode |

### B5. Kill conditions через 6 месяцев
1. **Median-case insolvency signal:** если p10 EBITDA@M24 остаётся < 0 и фактический runway опускается ниже **9 месяцев**, продолжать нельзя.
2. **Commercial failure:** если к концу M6 нет минимум **1 paid pilot** или минимум **3 enterprise accounts** в formal security/procurement stage, GTM-гипотеза не подтверждена.
3. **Pricing failure:** если подтверждённый реализуемый чек оказывается **<1,6 млн ₽ MRR** или средняя скидка для win > **30%**, модель больше не проходит EBITDA safety margin.

### B6. Verdict section B
Finance risk профиль у кейса **напряжённый, но не фатальный**. Base и median-case выглядят живыми, однако pricing/CAC volatility критически высоки. Для инвестрешения это скорее **conditional pass с понижением confidence**, чем clean pass. Без локального compliance контура и без 1-2 сильных design partners в топ-фарме кейс легко сползает в service-heavy нишу с плохой предсказуемостью. [T1][T2][T7]

## Источники SECTION B
- **T1.** `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/causaly-geo-expand-v2/04-economics.md`
- **T2.** `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/causaly-geo-expand-v2/02-demand.md`
- **T3.** `/home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/causaly-geo-expand-v2/05-critic.md` SECTION A.
- **T4.** BenchSci, company / pharma positioning: https://www.benchsci.com/
- **T5.** SciBite, Elsevier semantic stack / life sciences positioning: https://scibite.com/
- **T6.** PatSnap, R&D and innovation intelligence positioning: https://www.patsnap.com/
- **T7.** Skolkovo, Insilico Medicine profile: https://sk.ru/news/m/insajty/30440/
- **T8.** Habr, Insilico Medicine background: https://habr.com/ru/companies/insilico/articles/
- **T9.** Skolkovo, Webiomed / К-Скай profile: https://sk.ru/news/m/wiki/21962/
- **T10.** Rusprofile, ООО «К-Скай»: https://www.rusprofile.ru/
- **T11.** Skolkovo, Data MATRIX profile: https://sk.ru/companies/data-matrix/
- **T12.** Habr, OncoBox background: https://habr.com/ru/companies/oncobox/
- **T13.** Rusprofile, ООО «Онкобокс»: https://www.rusprofile.ru/

<!-- P6B-DONE -->


<!-- SOURCE: 06-verdict.md -->

[GEO-EXPAND] Causaly GEO Expand v2 — NEAR-PASS: 68/100 | EBITDA base=1300К₽/мес через 12 мес | LTV/CAC=23,4x | Ключевое преимущество: high-ACV enterprise economics для top-biopharma | Главный риск: спрос в РФ узкий и moat пока средний.

# 06-verdict

sector: GEO-EXPAND
status: NEAR-PASS
normalized_score: 68/100
raw_score: 102/150
investment_committee_decision: REJECTED

## Investment one-liner
[GEO-EXPAND] Causaly GEO Expand v2 — NEAR-PASS: 68/100 | EBITDA base=1300К₽/мес через 12 мес | LTV/CAC=23,4x | Ключевое преимущество: high-ACV enterprise economics для top-biopharma | Главный риск: спрос в РФ узкий и moat пока средний.

## Итог инвесткомитета
**Вердикт: NEAR-PASS / REJECTED.**

Почему не approve:
1. Unit economics сильные, и EBITDA gate проходит.
2. Но прямой спрос в РФ остаётся LOW, buyer universe узкий, а GTM целиком опирается на 5-10 крупных фармкомпаний.
3. Moat не слабый, но пока недостаточно жёсткий для premium category creation в локальном рынке.
4. Модель слишком чувствительна к price compression и CAC inflation: при `Price -30%` EBITDA @M12 уходит в **-2 651 791 ₽/мес**.

## Оценка
Source tier balance: T1=3, T2=18, T3=2, weighted=2.04. Penalty applied: -2 баллов to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 22 | `LTV/CAC = 23,4x`, `CAC Payback = 2,68 месяца`, `gross margin 62,7%` из `04-economics.md`. |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 20 | `EBITDA @M12 = 1 298 299 ₽/мес`, `Break-even month: M11`, при `50 клиентах ... 63,5 млн ₽/мес EBITDA`. |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 14 | `Итог по спросу в РФ: LOW`, но `SAM ... 1,53-1,54 млрд ₽` и `hh.ru vacancies = 15` по pharma analytics proxy. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 14 | `biopharma knowledge graph + research workflow layer` есть, но `продукт может схлопнуться в дорогой research tooling`. |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 15 | `Buyer universe в РФ слишком узкий`, `Зависимость от внешних LLM/API поставщиков`, `152-ФЗ ... блокируют deal`. |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 17 | `few-large-accounts market`, `buyer сверху`, `cycle сделки 6-12 месяцев`, но 10 named targets прослеживаются и channel fit понятен. |

**Normalized score = round((102 × 100) / 150) = 68/100.**

## Moat, 7-factor framework

| Фактор | Score (0-3) | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент почти не улучшает продукт для остальных клиентов в РФ-настройке. |
| Switching costs | 2 | После ontology tuning, workflows и cross-team embedding смена платформы становится болезненной. |
| Scale economies | 1 | Часть COGS и delivery стандартизируется, но service layer остаётся заметным. |
| Proprietary data / model advantage | 2 | Вертикальная life-sciences ontology и graph дают преимущество, но локально размер уникального датасета не доказан. |
| Regulatory moat | 1 | Есть compliance friction и value от secure deployment, но формальный регуляторный барьер как moat слаб. |
| Brand / distribution | 2 | Глобальный enterprise brand помогает, но в РФ локальный distribution moat ещё не собран. |
| Embedded workflow | 4 | Невозможно; максимум 3 |

**Коррекция:** embedded workflow = 3, так как продукт может стать daily research layer для R&D, medical и strategy-команд.

| Фактор | Финальный score |
|---|---:|
| Network effects | 0 |
| Switching costs | 2 |
| Scale economies | 1 |
| Proprietary data / model advantage | 2 |
| Regulatory moat | 1 |
| Brand / distribution | 2 |
| Embedded workflow | 3 |

Сумма 7-factor = **11/21**.
**Moat score = round((11 × 25) / 21) = 13/25**, округлён в общей рубрике до **14/25** из-за сильного workflow fit, но всё ещё это **средний moat**, не approve-grade.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 141 000 000 ₽ |
| CAC fully-loaded | 6 034 500 ₽ |
| LTV/CAC | 23,4x |
| CAC payback | 2,68 мес |
| Gross Margin | 62,7% |
| contribution_margin_rub_month | 1 410 000 ₽ |
| company_ebitda_rub_month, base M12 | 1 298 299 ₽/мес |
| company_ebitda_potential_rub_month | 63 547 000 ₽/мес при 50 клиентах |
| Break-even clients | 5 |
| Break-even month | M11-M12 |
| startup_capital_to_bep_rub | 55 612 893 ₽ |
| clients_to_500k_ebitda | 6 |
| months_to_500k_ebitda | 12 |

## Полный business process (из 04-economics.md)

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Target account list и enrichment | SDR + biopharma analyst | HH/отраслевые базы, CRM, LinkedIn-аналоги, ручной ресерч | 1,5 ч на аккаунт | 4 500 | средняя |
| 2 | Первичный outbound / warm intro | SDR | CRM + email sequences + Telegram/почта | 20 мин | 1 000 | высокая |
| 3 | Qualification call | AE | CRM + Zoom/Meet | 45 мин | 3 000 | средняя |
| 4 | Discovery с buyer group | AE + analyst | Zoom, шаблон discovery, CRM | 1,5 ч | 9 000 | низкая |
| 5 | Demo knowledge graph / use-case mapping | AE + solutions/CTO | demo env, slides, sandbox | 2 ч | 16 000 | низкая |
| 6 | Security/compliance review | CTO + legal | security docs, DPA, checklist | 8 ч | 42 000 | низкая |
| 7 | Pilot scoping | AE + analyst + CTO | proposal, CRM, shared docs | 4 ч | 24 000 | низкая |
| 8 | Paid pilot / procurement | AE + finance | договор, ЭДО, invoicing | 10 раб. дней cycle time | 35 000 | низкая |
| 9 | Onboarding данных и ontology tuning | analyst + backend + CSM | ETL, cloud, PM tool | 20 ч | 95 000 | средняя |
| 10 | Enablement и training | CSM + analyst | LMS, workshop, docs | 6 ч | 22 000 | средняя |
| 11 | Monthly evidence runs + support | analyst + CSM | product + ticketing + BI | ежемесячно 10-12 ч | 110 000 | средняя |
| 12 | Счёт, оплата, renewal follow-up | finance + AE + CSM | 1С/ЭДО/CRM | 2 ч | 8 000 | высокая |

## Команда

| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| CEO | продажи крупных аккаунтов, fundraising, partnerships | 845 000 |
| CTO / Tech Lead | product architecture, security, enterprise delivery | 715 000 |
| Senior Backend 1 | ingestion, APIs, data pipelines | 546 000 |
| Senior Backend 2 | product backend, integrations | 546 000 |
| ML Engineer | retrieval, ranking, synthesis quality | 650 000 |
| DevOps | infra, observability, security hardening | 455 000 |
| Frontend | researcher workflows, dashboards | 390 000 |
| SDR | prospecting и initial qualification | 234 000 |
| AE | discovery, proposal, close | 520 000 |
| Customer Success | onboarding, adoption, renewals | 338 000 |
| Biopharma analyst | domain setup, ontology, evidence workflows | 364 000 |
| **Итого** |  | **5 603 000 ₽/мес** |

## GTM, 10 named targets

| # | Компания | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | BIOCAD | Публично подчёркивает R&D и разработку новых препаратов, значит pain по evidence synthesis и target landscape высок. | email decision-maker в R&D / intro через отраслевые конференции | 2 250 000 ₽/мес |
| 2 | Р-Фарм | Большой портфель разработок и клинических программ, нужен continuous competitor и trial monitoring. | партнёрство + warm intro через отраслевых консультантов | 2 250 000 ₽/мес |
| 3 | ГЕНЕРИУМ | Инновационный biotech-профиль и высокий research intensity. | email CSO / конференция / pilot workshop | 2 000 000 ₽/мес |
| 4 | ПРОМОМЕД | Публичный R&D narrative и pipeline pressure, нужен faster landscape review. | email medical/R&D leadership | 1 800 000 ₽/мес |
| 5 | Герофарм | Собственный разработческий контур и клиническая активность подтверждают buyer fit. | конференция + direct outbound | 1 800 000 ₽/мес |
| 6 | Озон Фармацевтика | Рост и расширение портфеля создают боль по monitoring и pipeline intelligence. | ABM outbound + профильные мероприятия | 1 500 000 ₽/мес |
| 7 | Артген Биотех | Биотех-фокус повышает ценность ontology-driven evidence synthesis. | founder-led intro / email decision-maker | 1 800 000 ₽/мес |
| 8 | Петровакс | Клинические и product-development сценарии создают repeatable use cases. | direct outbound + партнёрство | 1 500 000 ₽/мес |
| 9 | Биннофарм Групп | Масштаб компании и portfolio strategy делают value proposition понятным для multi-team deployment. | enterprise account mapping + email | 2 000 000 ₽/мес |
| 10 | Фармасинтез | Широкий pharma portfolio и R&D-функция дают хороший pilot wedge для intelligence layer. | email + конференция / профильное мероприятие | 1 500 000 ₽/мес |

## Top-3 risks

| Риск | Вероятность | Влияние | Почему это top risk |
|---|---|---|---|
| Узкий buyer universe и LOW direct demand в РФ | Высокая | Высокое | `Итог по спросу в РФ: LOW`, поэтому один неудачный квартал GTM ломает план. |
| Price compression / cheaper substitutes | Высокая | Высокое | `Price -30%` даёт `EBITDA @M12 = -2 651 791 ₽/мес`, а substitutes включают manual analysts и дешёвые tools. |
| Зависимость от LLM/API и compliance friction | Высокая | Высокое | `152-ФЗ ... блокируют deal`, плюс `Зависимость от внешних LLM/API поставщиков`. |

## Что нужно доказать для approve
1. Минимум 2 design partners из top-10 biopharma списка с paid pilot.
2. Реализуемый чек не ниже **1,8-2,25 млн ₽/мес** без скидок >25%.
3. Pilot-to-annual conversion не ниже 25-30%.
4. Локальный secure/VPC contour и data residency, снимающие 152-ФЗ objections.
5. Повторяемый workflow ROI: time-to-insight ниже минимум на 40-50% против manual research.

## LTV Upside Calculator
Так как кейс получает **REJECTED / NEAR-PASS**, нужен апсайд-калькулятор до approve-grade.

### Базовая формула
`customer_ltv_rub = MRR × GM% / monthly churn`

### Текущая база
- MRR = 2 250 000 ₽
- GM = 62,7%
- monthly churn = 1,0%
- customer_ltv_rub = **141,0 млн ₽**

### Upside-сценарии
| Сценарий | MRR | GM | Churn | Новый LTV | Что это даёт |
|---|---:|---:|---:|---:|---|
| Base | 2 250 000 ₽ | 62,7% | 1,0% | 141,0 млн ₽ | Текущий near-pass |
| Pricing discipline | 2 500 000 ₽ | 62,7% | 1,0% | 156,8 млн ₽ | Больше запас по EBITDA при том же CAC |
| Better retention | 2 250 000 ₽ | 62,7% | 0,8% | 176,3 млн ₽ | Сильнее premium enterprise thesis |
| Better delivery mix | 2 250 000 ₽ | 68,0% | 1,0% | 153,0 млн ₽ | Меньше service-heavy pressure |
| Approve-grade target | 2 500 000 ₽ | 68,0% | 0,8% | 212,5 млн ₽ | Даёт заметный margin of safety для approve |

## Proof points, которые уже есть
- `SAM по двум методикам сходится около 1,53-1,54 млрд ₽`.
- `Blended fully-loaded CAC = 6 034 500 ₽` выглядит высоким, но правдоподобным для regulated enterprise motion.
- `Break-even clients = 5`, `Break-even month: M11`.
- `p50 EBITDA @M24 = 7 047 136 ₽/мес`, то есть median-case economics жива.

## Delta vs previous
Это rerun-кейс. Относительно старого triage вывод стал сильнее по economics и слабее по certainty рынка: теперь видно, что проблема monetizable, но для approve всё ещё не хватает margin of safety по demand + moat.

## Финальное решение
**REJECTED с пометкой NEAR-PASS.**

Кейс стоит возвращать в approve only если появятся:
- 1-2 оплаченных design partner в российской биофарме,
- подтверждение локального compliance contour,
- отсутствие price compression ниже 1,8 млн ₽ MRR,
- и повторяемая pilot-to-rollout воронка.


<!-- SOURCE: 07-score-trajectory.md -->

## 2026-04-20 22:54 MSK — P4 Demand Validation
- Этап: P4 Demand Validation
- Итог: прямой спрос в РФ низкий, но кейс не умирает, потому что у крупных biopharma buyer'ов есть реальная R&D-боль и бюджет на дорогой enterprise intelligence stack.
- Ключевой вывод: mandatory demand endpoint стабильно дал LOW, зато SAM по top-down и bottom-up сошелся около 1,53-1,54 млрд ₽, а Profit Gate проходит в модели 2-4 крупных контрактов.
- Изменение оценки: умеренно негативное по ширине рынка, но умеренно позитивное по монетизации, если идти через few-large-accounts GTM.
- Артефакт: `pipeline/cases/causaly-geo-expand-v2/02-demand.md`

## 2026-04-22 18:52 MSK — P5 Unit Economics
- Этап: P5 Unit Economics
- Итог: экономика проходит, но только в формате high-ACV enterprise product для узкого списка biopharma accounts.
- Ключевой вывод: при MRR 2,25 млн ₽ на клиента, COGS 0,84 млн ₽ и gross margin 62,7% break-even достигается на 5 клиентах, blended fully-loaded CAC = 6,03 млн ₽, LTV/CAC = 23,4x, CAC payback = 2,68 месяца.
- Изменение оценки: позитивное по качеству юнит-экономики, нейтрально-негативное по риску узкого buyer universe и длинного procurement cycle.
- Артефакт: `pipeline/cases/causaly-geo-expand-v2/04-economics.md`

## 2026-04-23 04:59 MSK — P7 Critic and Verdict
- Этап: P7 Critic and Verdict
- Итог: NEAR-PASS 68/100, финальное решение инвесткомитета — REJECTED.
- Ключевой вывод: экономика инвестиционно сильная, но локальный спрос в РФ остаётся LOW, moat только средний, а чувствительность к price compression и CAC inflation слишком высокая для approve.
- Изменение оценки: умеренно негативное, потому что сильный P5/P6 не компенсировал слабость demand certainty и margin of safety по GTM.
- Артефакт: `pipeline/cases/causaly-geo-expand-v2/06-verdict.md`

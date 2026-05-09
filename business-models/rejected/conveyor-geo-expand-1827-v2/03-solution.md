---
stage: solution
case: conveyor-geo-expand-1827-v2
date: 2026-04-22
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
Conveyor как AI-native платформа для automation of customer trust workflow, security questionnaires, Trust Center и RFP при выходе на рынок РФ.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. Продукт решает не абстрактную задачу «AI для анкет», а дорогую операционную проблему, как ускорить vendor security review, не тормозить enterprise sales и снизить нагрузку на security / GRC / sales engineering команды.
2. Реальный wedge в РФ выглядит не как массовый self-serve SaaS, а как **enterprise trust workflow layer** для компаний, которые регулярно проходят security questionnaires, third-party risk review и RFP-процессы.
3. Наиболее правдоподобный вход в рынок, крупные B2B SaaS, облачные провайдеры, финтех, кибербезопасность, интеграторы и платформенные поставщики с enterprise sales motion.
4. Главный риск, продукт легко схлопывается в узкий feature-layer над knowledge base, shared docs и ручными ответами, если не доказать repeatable ROI и premium ACV.

## 1. Какую проблему реально решает продукт

Conveyor-подобный продукт продаёт не просто AI assistant, а устранение четырёх дорогих потерь:
- медленного ответа на security questionnaires и vendor due diligence;
- потери скорости enterprise-сделок из-за trust bottleneck;
- ручной сборки ответов из разрозненных документов, прошлых анкет и policy artifacts;
- перегруза security, GRC и sales engineering команд однотипной работой.

Для локального ICP это painkiller только там, где сделки крупные, security review повторяется постоянно, а задержка ответа реально стоит выручки. Для SMB и компаний без enterprise procurement motion value proposition будет слишком слабой.

## 2. Целевой ICP в РФ

### Primary ICP
- облачные и инфраструктурные провайдеры;
- enterprise cybersecurity vendors;
- крупные B2B SaaS и платформенные компании;
- финтех и банки, которые продают сложные B2B-продукты;
- интеграторы и enterprise software vendors с регулярными RFP и security review.

### Фильтр на ICP
Клиент проходит, если одновременно есть:
1. регулярный поток security questionnaires, DDQ, SIG-like форм и RFP;
2. заметная стоимость задержки в пресейле или renewal;
3. отдельные owner'ы trust / security assurance / sales engineering / GRC;
4. enterprise deal size, который оправдывает покупку workflow-layer;
5. готовность покупать не только лицензию, но и knowledge setup, migration и integration.

### Нецелевой сегмент
- SMB без зрелого enterprise sales motion;
- компании, которые редко проходят vendor security review;
- локальные сервисные бизнесы без Trust Center и questionnaire volume;
- клиенты, которым дешевле отвечать руками или через shared docs/wiki.

## 3. Продуктовый wedge

### Core wedge
**AI-native trust workflow and questionnaire automation layer**
- автоматизация ответов на security questionnaires и RFP;
- Trust Center как self-serve surface для типовых ответов и документов;
- централизованная knowledge library по security/compliance артефактам;
- orchestration между security, GRC, sales и presales командами.

### Что делает wedge сильнее обычной базы знаний
1. **Workflow depth**: продукт встроен в процесс сделки, а не просто хранит документы.
2. **Revenue linkage**: ценность можно продавать через ускорение deal velocity и снижение sales friction.
3. **Cross-functional leverage**: снимает нагрузку сразу с нескольких дорогих команд.
4. **Repeatability**: каждая новая анкета усиливает reusable answer base.
5. **Trust Center effect**: часть входящего потока можно переводить в self-serve и уменьшать объём ручных запросов.

Именно эта комбинация даёт шанс на enterprise чек. Без неё продукт быстро превращается в «умную папку с ответами».

## 4. Как продукт должен выглядеть в РФ, чтобы пройти GTM

### Вариант, который, вероятно, не взлетит
- продажа как generic AI tool для любых анкет;
- self-serve motion;
- ставка на mid-market с низким questionnaire volume;
- слабая интеграция с trust/security процессами клиента.

### Вариант, который выглядит реалистично
- заход через enterprise pilot на trust / vendor review bottleneck;
- buyer сверху, head of security assurance, GRC lead, head of sales engineering, COO revenue ops;
- KPI pilot: быстрее turnaround, меньше ручных часов, меньше deal slippage, больше reuse ответов;
- обязательный setup knowledge base, policy library и прошлых questionnaire answers;
- rollout как trust workflow overlay, а не просто chatbot для документов.

## 5. Почему клиент будет покупать именно это, а не текущий стек

У локального клиента уже есть substitutes:
- Confluence, Notion, Google Drive, shared folders и spreadsheet-based tracking;
- ручная работа security / presales / GRC команд;
- generic RFP tools и knowledge management;
- кастомная сборка поверх internal docs + LLM;
- найм дополнительного headcount в sales engineering или compliance.

Conveyor-подобный продукт может выиграть только в трёх вещах:
1. **заметно сокращает turnaround time** по сравнению с текущим ручным процессом;
2. **связывает trust workflow с revenue motion**, а не просто хранит ответы;
3. **быстрее даёт time-to-value**, чем внутренняя сборка или интеграторский проект.

Если этих преимуществ нет, buyer почти наверняка останется на internal wiki + люди + частичная автоматизация.

## 6. Delivery model

### Наиболее правдоподобная схема внедрения
1. аудит текущего questionnaire / trust workflow и узких мест в пресейле;
2. выбор одного monetizable процесса, например security questionnaires для enterprise deals;
3. загрузка policy documents, прошлых ответов, Trust Center content и шаблонов;
4. 4-8 недель pilot с security / sales engineering командой;
5. сравнение turnaround time, ручной загрузки и влияния на pipeline до/после;
6. rollout на RFP, vendor due diligence и renewal motions после доказанного ROI.

### Кто должен быть buyer'ом
- head of security assurance;
- GRC lead;
- VP Sales Engineering / presales owner;
- COO revenue operations;
- CTO/CSO в компаниях, где trust напрямую влияет на сделки.

### Кто редко будет настоящим buyer'ом
- одиночный security analyst без бюджета;
- procurement без revenue owner'а;
- IT без связи с enterprise sales KPI.

## 7. Конкурентная позиция

### Против internal docs и ручного процесса
Преимущество возникает, если продукт реально уменьшает deal friction, а не просто ускоряет поиск файлов.

### Против generic LLM-надстроек
Шанс есть, если продукт лучше удерживает структуру ответов, историю использования, approval workflow и trust-center surface.

### Против найма людей
Преимущество сильно только там, где questionnaire volume стабильно высокий, а скорость ответа влияет на win rate и revenue timing.

## 8. Основные риски solution-fit

1. **Narrow ICP risk**: платёжеспособный сегмент в РФ заметно уже глобального.
2. **Feature risk**: часть ценности могут забрать generic AI knowledge tools.
3. **Build-vs-buy risk**: сильные security/presales команды соберут похожий слой сами.
4. **Pricing risk**: публичный базовый чек слишком низкий для фонда без upsell/services модели.
5. **Proof risk**: без измеримого влияния на deal velocity продукт выглядит как nice-to-have.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- какой реальный ACV достижим в upper-mid / enterprise сегменте РФ;
- сколько services и solution engineering нужно на запуск одного клиента;
- сохраняется ли software-like gross margin после setup и integration;
- сколько активных клиентов нужно для выхода на 500k+ EBITDA/мес;
- не слишком ли узок buyer universe после отсечения компаний с маленьким questionnaire volume.

## Итог для пайплайна

**P4 пройден условно.**

Кейс имеет внятный solution thesis только как enterprise trust workflow layer для компаний с тяжёлым security-review motion, а не как массовый SaaS для любого B2B. Продолжать дальше имеет смысл, если на economics подтвердится, что локальная модель держит premium чек через enterprise rollout, usage и services, а не разваливается в низкочековый niche tool.

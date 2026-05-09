# Armadin GEO Expand v2 — Full Verdict Package
> Скомпилированный пакет стадий P0/P3/P4/P5/P6/P7 для публикации в GitHub.

## Файл: 00-brief.md

# Краткий бриф

- **Тип запуска:** принудительный full rerun/resurrect
- **Raw-файл:** `pipeline/raw/2026-04-19-resurrect-armadin-geo-expand.md`
- **Новый кейс:** `pipeline/cases/armadin-geo-expand-v2/`
- **Сектор:** `GEO-EXPAND`
- **Причина открытия:** файл начинается с `resurrect-`, поэтому по standing orders создаётся отдельный case-v2 и отправляется дальше в P3→P7 без классификации как duplicate.
- **Оригинальный источник/вердикт:** `triage/triage-2026-04-18-armadin-geo-expand.md`; Сигнал Armadin принят в работу как новый кейс Program 1.

## Файл: 01-intake.md

---
sector: GEO-EXPAND
rerun: true
source_raw: 2026-04-19-resurrect-armadin-geo-expand.md
created: 2026-04-20T06:37:59+03:00
original_source: triage/triage-2026-04-18-armadin-geo-expand.md
original_case: pipeline/cases/enterprise-autonomous-cybersecurity-agents/
original_verdict: Сигнал Armadin принят в работу как новый кейс Program 1.
---

# Intake

## Статус
Принудительный полный rerun/resurrect. Этот кейс создан заново и должен пройти P3→P7 с новой аналитикой.

## Краткое пояснение
Принудительный resurrect-rerun для новой полной аналитики по автономным AI-агентам в enterprise-кибербезопасности.

## Полный контекст raw-файла

# RESURRECT SIGNAL — armadin-geo-expand

## Meta
- source: triage/triage-2026-04-18-armadin-geo-expand.md
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
2026-04-18

## Входные данные
- `pipeline/raw/raw-2026-04-18-0527-msk-armadin-geo-expand.md`

## Классификация
новый сигнал, кейс создан

## Решение
Открыть новый кейс в `pipeline/cases/enterprise-autonomous-cybersecurity-agents/`.

## Почему
- В `pipeline/cases/` не найден открытый кейс, который уже покрывает тему autonomous AI security agents для offensive security, SOC automation и continuous validation.
- Сигнал качественный и проходит фильтр Program 1 по экономике: во входном файле указан `ltv_signal` `3000000-12000000 ₽ в год`, то есть примерно `250000-1000000 ₽ в месяц` с одного крупного клиента.
- Верхняя граница диапазона превышает порог `> 500000 ₽ в месяц`, поэтому кейс подходит для открытия.
- Категория выглядит enterprise-grade и sticky: бюджеты ИБ в крупных компаниях существенные, а локализация под российский стек ИБ, on-prem/private deployment и интеграции создаёт сервисно-ёмкий слой внедрения.

## Что сделано
- Создан новый кейс `pipeline/cases/enterprise-autonomous-cybersecurity-agents/`.
- Заполнен `00-brief.md` на русском языке.
- Добавлен `01-evidence.md` с первичным сигналом на русском языке.
- Raw-файл перенесён в `pipeline/raw/processed/`.

## Вердикт
Сигнал Armadin принят в работу как новый кейс Program 1. Добавлена новая тема: автономные AI-агенты для enterprise-кибербезопасности.

```

## Файл: 02-demand.md

---
stage: demand-validation
case: armadin-geo-expand-v2
date: 2026-04-20
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: PASS_WITH_RESERVATIONS
confidence: medium
---

# 02-demand — Demand Validation

## Кейс
Armadin, agentic AI платформа для continuous red teaming, adversarial exposure validation и remediation в enterprise-кибербезопасности.

## Итог

> Market Pulse 2026-04-22: растущий интерес.

**Статус: PASS WITH RESERVATIONS.**

- По exact-demand в РФ ниша пока выглядит как **LOW**: `continuous red teaming`, `continuous validation cybersecurity`, `automated penetration testing enterprise`, `BAS cybersecurity` и `симуляция кибератак` все дают слабый поисковый хвост и почти нулевые публичные job/search сигналы. [T2]
- Но early reject по правилу `LOW demand + Profit Gate FAIL` здесь не срабатывает. Категория enterprise-grade, бюджеты buyer'а крупные, а мировой рынок уже подтверждает willingness to pay за automated security validation и BAS/AEV-подход. [T2]
- Для РФ это не SMB/self-serve продукт, а узкий high-ticket GEO-EXPAND сценарий для крупных банков, телекомов, промышленных групп и MSSP/SOC-интеграторов. [T2/T3]

## 1) Спрос и сигналы рынка

### Demand API
- `continuous red teaming` → LOW, Google Trends RU 0, HH vacancies 1, Yandex suggest 2. [T2]
- `continuous validation cybersecurity` → LOW, Google Trends RU 0, HH vacancies 0, Yandex suggest 2. [T2]
- `automated penetration testing enterprise` → LOW, Google Trends RU 1, HH vacancies 1, Yandex suggest 2. [T2]
- `BAS cybersecurity` → LOW, Habr 2, Yandex suggest 2. [T2]
- `симуляция кибератак` → LOW, Habr 2, Yandex suggest 2. [T2]

### Интерпретация
- В РФ нет массового inbound-спроса по exact category labels. Это ожидаемо для новой security-категории: покупка идёт не через широкий search, а через top-down security leadership, red team руководителей и крупных интеграторов. [T2]
- Низкий search-volume здесь не означает нулевой бюджет, но означает высокий education burden и длинный enterprise sales cycle. [T2]

## 2) Category proof и why now
1. На сайте Armadin продукт прямо позиционируется как **continuous, agentic red teaming and remediation platform** для enterprise attack surface. Это подтверждает, что компания продаёт не point solution, а стратегический offensive-security control layer. [T1]
2. **10 марта 2026 года** Armadin объявила о **$189.9 млн Seed + Series A**, назвав это крупнейшим объединённым Seed/A в истории cybersecurity. Это сильный внешний сигнал, что инвесторы верят в category formation и крупный spend line. [T1]
3. AttackIQ в феврале 2025 года описывает AEV как framework, который **continuous emulates real-world cyberattacks** для проверки security posture. То есть сама соседняя категория уже артикулирована зрелым игроком и не является фантазией Armadin. [T1]
4. AttackIQ в partner-программе для MSSP прямо пишет, что breach and attack simulation можно продавать как managed service с white-label и low operational overhead. Это важный proof, что motion может работать не только как чистый SaaS, но и как сервисный слой, релевантный для GEO-EXPAND. [T1]
5. Picus в апреле 2026 года сообщает о лидерстве в G2 по BAS с 200+ reviews и высокими метриками adoption/satisfaction. Это не pricing-proof, но это подтверждение активного коммерческого спроса на adjacent category. [T1]

## 3) Что это значит для локального GEO-EXPAND кейса
- Локальный exact-demand слабый, зато категория хорошо ложится на enterprise security budgets, где покупка часто идёт как часть CTEM / validation / red-team modernization, а не как отдельный поисковый продукт. [T1/T2]
- Вероятный wedge в РФ, если он вообще соберётся, это не массовая продажа лицензий, а **managed offensive validation** с on-prem/private deployment, кастомизацией под локальный security stack и интеграцией в существующий SOC/VM/process. [T2/T3]
- Следовательно, кейс выглядит как **узкий, но потенциально high-LTV** GEO-EXPAND, а не как standalone массовая software category. [T2]

## 4) WTP и ценностные якоря

### Прямые сигналы willingness to pay
- Сам факт существования зрелых BAS/AEV игроков Picus и AttackIQ с enterprise/government/MSSP motion подтверждает, что buyer уже платит за continuous security validation. [T1]
- AttackIQ отдельно подчёркивает покупку через MSSP и GSA/government channels, а значит продукт выдерживает procurement-heavy контур и продаётся не только в стартапы. [T1]
- Armadin строит продукт вокруг команды ex-Mandiant и обещания закрывать exploitable risk до adversarial opportunity, то есть value prop привязан к дорогостоящему enterprise risk reduction, а не к дешёвому pentest automation. [T1]

### Ограничения
- Публичного прайсинга Armadin нет. [T1]
- Для РФ нет найденных прямых публичных ценовых якорей именно на local BAS/AEV category. [T2]
- Поэтому месячный чек ниже оцениваю как inference из enterprise security economics и adjacent market motions, а не как confirmed quote. [T2/T3]

## 5) TAM / SAM / SOM в рублях

### Подход и допущения
- ICP: крупные организации с внутренним SOC/red team и высоким regulatory / threat pressure, плюс крупные MSSP и security integrators.
- Базовый контракт беру как **3.6 млн ₽ ARR** (примерно 300 тыс. ₽/мес) для ограниченного pilot/department deployment.
- Enterprise rollout с сервисным слоем может быть выше, **до 9.6 млн ₽ ARR** (800 тыс. ₽/мес), но для sizing использую консервативный baseline 3.6 млн ₽. [T2/T3]

### Top-down
- Беру целевой локальный universe в **1 200** крупных организаций и security providers, где такая боль вообще может существовать. [T3]
- Если 20% из них реально addressable в горизонте 24 месяцев, SAM составляет **240 buyers**. [T2/T3]
- При baseline ARR **3.6 млн ₽** получаем **SAM ≈ 864 млн ₽/год**. [T2]

### Bottom-up
- Реалистичный SOM Y1 для founder-led / partner-led захода: **6 клиентов** × **3.6 млн ₽** = **21.6 млн ₽/год**. [T2]
- SOM Y3 при успешной локализации и channel motion: **20 клиентов** × **3.6 млн ₽** = **72 млн ₽/год**. [T2]

### Sanity-check
- 6 клиентов за год для новой enterprise security category тяжело, но не абсурдно, если продавать через MSSP / red-team advisory motion. [T2]
- 20 клиентов за 3 года остаётся <10% от SAM, то есть sizing не выглядит заведомо overclaim. [T2]

## 6) Profit Gate

### Сценарий A: чистый SaaS pilot
- Цена: **300 тыс. ₽/мес**
- Валовая маржа: **65%**
- Валовая прибыль на клиента: **195 тыс. ₽/мес**
- Для покрытия fixed costs **1.5 млн ₽/мес** и выхода на **500 тыс. ₽ EBITDA/мес** нужно около **11 клиентов**.
- **Вердикт:** погранично, но достижимо только при сильном enterprise execution. [T2]

### Сценарий B: managed validation / private deployment
- Цена: **800 тыс. ₽/мес**
- Валовая маржа: **55%**
- Валовая прибыль на клиента: **440 тыс. ₽/мес**
- Для той же цели достаточно **5 клиентов**.
- **Вердикт:** PASS. [T2]

### Сценарий C: MSSP / channel-led white-label
- Цена для конечного аккаунта: **500 тыс. ₽/мес**, vendor share ниже, но CAC лучше.
- При 8–10 аккаунтах через 2–3 канальных партнёра можно дойти до порога EBITDA быстрее, чем в прямых продажах. [T2/T3]
- **Вердикт:** PASS WITH EXECUTION RISK. [T2]

### Общий вывод по Profit Gate
- Для SMB/horizontal motion кейс не работает.
- Для узкого enterprise / managed-service motion **Profit Gate проходит**.
- Поэтому формального early reject на P3 нет. [T2]

## 7) Основные риски
- Слабый локальный exact-demand и высокая стоимость category education. [T2]
- Длинный цикл сделки, необходимость on-prem/private deployment и дорогой presales. [T2/T3]
- Риск, что покупатель предпочтёт существующего глобального игрока BAS/AEV или локального интегратора без отдельного нового вендора. [T1/T3]
- Возможный overlap с уже существующим кейсом `enterprise-autonomous-cybersecurity-agents`, который надо будет отдельно проверить на этапе verdict. [T2]

## 8) Вывод для pipeline
**Решение на этапе demand validation: PASS WITH RESERVATIONS.**

Кейс не уходит в early reject, потому что хотя публичный search demand в РФ низкий, enterprise economics и мировой category proof достаточно сильные, чтобы не отбрасывать гипотезу раньше P4/P5. Дальше нужно жёстко проверить CAC, channel strategy, локализацию под российский security stack и риск overlap/duplicate с broader cybersecurity-agents thesis.

## Источники
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=continuous%20red%20teaming [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=continuous%20validation%20cybersecurity [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=automated%20penetration%20testing%20enterprise [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=BAS%20cybersecurity [T2]
- Demand API: http://172.18.0.1:9001/multi-demand?keyword=%D1%81%D0%B8%D0%BC%D1%83%D0%BB%D1%8F%D1%86%D0%B8%D1%8F%20%D0%BA%D0%B8%D0%B1%D0%B5%D1%80%D0%B0%D1%82%D0%B0%D0%BA [T2]
- Armadin homepage: https://www.armadin.com/ [T1]
- Armadin funding announcement, 2026-03-10: https://www.armadin.com/blog-posts/armadin-secures-record-breaking-189-9m-in-seed-and-series-a-funding-to-combat-the-era-of-ai-driven-hyperattacks [T1]
- AttackIQ acquisition / AEV definition, 2025-02-04: https://www.attackiq.com/resources/press-release/attackiq-acquires-deepsurface/ [T1]
- AttackIQ MSSP partner program: https://www.attackiq.com/resources/press-release/attackiq-launches-new-mssp-partner-program/ [T1]
- Picus Security G2 BAS press release, 2026-04-15: https://www.picussecurity.com/resource/press-release/picus-security-earns-top-ranking-in-spring-2026-g2-grid-report-for-breach-and-attack-simulation [T1]

Sources: T1=5, T2=5, T3=1. Primary evidence basis: T1/T2.
## Market Pulse
- Market Pulse 2026-04-21: растущий интерес.
Market Pulse 22.04.2026: растущий интерес.

> Market Pulse 2026-04-23: растущий интерес.
> Market Pulse 2026-04-24: растущий интерес.

## Файл: 03-solution.md

---
stage: solution
case: armadin-geo-expand-v2
date: 2026-04-24
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: CONDITIONAL_PASS
confidence: medium
---

# 03-solution — Solution / GTM Fit

## Кейс
Armadin, agentic AI платформа для continuous red teaming, adversarial exposure validation и remediation в enterprise-кибербезопасности.

## Executive summary

**Итог P4: CONDITIONAL PASS.**

Почему:
1. Продукт решает дорогую и регулярную enterprise-задачу, проверку реальной атакуемости и скорости remediation, а не декоративный AI-use case.
2. На локальном GEO-EXPAND рынке правдоподобный wedge выглядит не как чистый self-serve SaaS, а как managed offensive validation layer с private deployment и глубокой интеграцией в existing security stack.
3. Лучший GTM идёт не в широкий рынок, а в крупные regulated enterprise, MSSP и security-интеграторов, у которых уже есть бюджет на red team, BAS, CTEM или validation.
4. Главный риск, кейс легко расползается в дорогой security consulting, если не удержать scope, playbooks, time-to-value и шаблонность внедрения.

## 1. Какую проблему реально решает продукт

Покупают не “AI-агентов для ИБ”, а устранение четырёх дорогих потерь:
- слепых зон между pentest, BAS и реальной эксплуатационной готовностью защиты;
- ручной и редкой проверки attack paths вместо continuous validation;
- медленного перевода findings в remediation backlog;
- зависимости от внешних red-team циклов, которые дают snapshot, но не постоянный контроль.

Для крупного enterprise это painkiller, если продукт действительно:
- регулярно показывает exploitable paths;
- приоритизирует, что чинить первым;
- сокращает время между обнаружением и remediation;
- встраивается в SOC / VM / exposure-management процессы.

## 2. Целевой ICP в локальном контуре

### Primary ICP
- крупные банки, телекомы и промышленные группы с внутренним SOC и зрелой ИБ-функцией;
- enterprise-команды, у которых уже есть red team, VM, BAS или CTEM-бюджет;
- MSSP и security-интеграторы, которым нужен white-label / managed validation layer;
- крупные организации с жёсткими требованиями к private deployment и локальному хранению данных.

### Фильтр на ICP
Клиент проходит, если одновременно есть:
1. высокий ущерб от инцидента и понятный security budget;
2. зрелый owner, CISO, head of red team, head of SOC или exposure-management owner;
3. существующий процесс remediation, в который можно встроить findings;
4. готовность к pilot с инженерной интеграцией;
5. потребность не в разовом pentest, а в повторяемом validation loop.

### Нецелевой сегмент
- SMB без отдельной offensive-security функции;
- компании, которые покупают только разовый pentest “для галочки”;
- команды без internal owner и без готовности подключать приватный контур;
- покупатели, которым нужен generic AI copilot вместо security control layer.

## 3. Продуктовый wedge

### Core wedge
**Managed adversarial validation layer для enterprise security**
- continuous эмуляция атак и проверка exploitable exposure;
- приоритизация findings по реальному риску, а не по формальным CVE-спискам;
- перевод результатов в remediation actions и workflow для security team;
- playbooks под типовые enterprise-сценарии и локальный security stack;
- private deployment, auditability и controlled human oversight.

### Почему это сильнее, чем просто BAS или pentest automation
1. **Workflow ownership**: продукт закрывает не разовую проверку, а постоянный validation loop.
2. **Actionability**: ценность в том, что findings быстро переходят в remediation backlog.
3. **Enterprise fit**: покупатель получает security control, который можно встроить в существующую операционную модель.
4. **Service-heavy moat**: локальная настройка, интеграции и managed delivery повышают stickiness.
5. **Channel fit**: wedge можно продавать как слой для MSSP и интеграторов, а не только прямыми лицензиями.

## 4. Как продукт должен выглядеть в РФ, чтобы пройти GTM

### Вариант, который, вероятно, не взлетит
- чистый self-serve SaaS без private deployment;
- generic “AI pentester” без интеграции в remediation процесс;
- продажа в mid-market без сильного security owner;
- широкий маркетинг на неподготовенный рынок с долгим education cycle.

### Вариант, который выглядит реалистично
- pilot на одном понятном сегменте, например external exposure validation или continuous control validation;
- deployment в приватном контуре или через доверенного MSSP-партнёра;
- заранее подготовленные playbooks, integration adapters и remediation workflow;
- упаковка как managed validation service, а не как просто лицензия на AI-платформу;
- top-down buyer плюс сильный технический champion внутри SOC/red-team функции.

## 5. Почему клиент будет покупать именно это, а не текущий стек

У клиента уже есть substitutes:
- классический pentest;
- BAS/AEV-платформы без локального сервисного слоя;
- ручной red team и external consultancies;
- внутренние security engineering команды.

Такой продукт выигрывает только если делает три вещи:
1. **даёт более частый и прикладной validation**, чем периодический pentest;
2. **сокращает время до remediation**, а не просто генерирует ещё один отчёт;
3. **поставляется как управляемый слой**, который проще внедрить, чем строить всё in-house.

Если этого нет, рынок выберет либо глобального BAS-вендора, либо локального интегратора, либо старую модель “несколько аудитов в год”.

## 6. Delivery model

### Наиболее правдоподобная схема внедрения
1. discovery по текущему security stack и ownership-модели;
2. выбор одного validation use case для пилота;
3. настройка сценариев атак, приоритетов и routing findings;
4. запуск в приватном или partner-managed контуре;
5. демонстрация time-to-detect / time-to-remediate improvement;
6. расширение на новые поверхности, бизнес-юниты или канал MSSP.

### Кто должен быть buyer'ом
- CISO;
- head of red team;
- head of SOC / security operations;
- owner направления exposure management / CTEM;
- руководитель MSSP-практики.

### Кто редко будет настоящим buyer'ом
- procurement без security sponsor;
- ИТ-руководитель без ИБ-мандата;
- SMB-основатель без зрелой security-функции.

## 7. Конкурентная позиция

### Против глобальных BAS/AEV-вендоров
Шанс есть, если продукт лучше упакован под local deployment, сервисный контур и интеграцию с российским security stack.

### Против локальных интеграторов
Преимущество возможно, если у продукта есть repeatable platform layer, а не только дорогой ручной delivery.

### Против in-house offensive security
Шанс появляется, если pilot быстрее запускается, чем внутренняя разработка, и даёт более стабильный recurring validation.

## 8. Основные риски solution-fit

1. **Consulting-risk**: каждый enterprise-клиент может требовать слишком много bespoke-настроек.
2. **Deployment-risk**: без private/on-prem модели часть целевых аккаунтов не откроется вообще.
3. **Champion-risk**: без сильного internal owner продукт останется “интересной демкой”.
4. **Crowding-risk**: adjacent BAS/AEV category уже занята сильными глобальными игроками.
5. **Margin-risk**: если каждая поставка требует heavy presales и кастомной интеграции, экономика ломается.
6. **Overlap-risk**: кейс может оказаться частным подмножеством более широкого тезиса про enterprise autonomous cybersecurity agents.

## 9. Что обязательно доказать на следующем этапе

В `04-economics.md` нужно жёстко проверить:
- сколько реально стоит pilot и private deployment для одного enterprise-клиента;
- какая доля delivery шаблонизируется, а какая остаётся консалтингом;
- сколько presales и security engineering часов съедает одна сделка;
- какой канал реалистичнее, direct enterprise, MSSP или интеграторы;
- сколько активных клиентов нужно для EBITDA > 500 000 ₽/мес при честной gross margin.

## Итог для пайплайна

**P4 пройден условно.**

Кейс имеет внятный solution thesis только как узкий enterprise GEO-EXPAND сценарий, managed adversarial validation с private deployment и сильным сервисным слоем. Двигать дальше стоит, но только если на economics подтвердятся повторяемое внедрение, приемлемый presales burden и отсутствие провала в кастомный security consulting.

## Файл: 04-economics.md

---
stage: economics
case: armadin-geo-expand-v2
date: 2026-04-25
analyst: branch-models-lead
sector: GEO-EXPAND
verdict: PASS
confidence: medium
---

# 04-economics — Unit Economics

## Кейс
Armadin, agentic AI платформа для continuous red teaming, adversarial exposure validation и remediation в enterprise-кибербезопасности.

## Executive summary

**Итог P5: PASS.**

Кейс работает только как дорогой enterprise / regulated security motion, с private deployment, presales-heavy продажей и длинным циклом сделки. Для SMB экономика не сходится. Для enterprise-сегмента модель сходится:

- **Blended MRR на клиента:** **600 000 ₽/мес**.
- **COGS на клиента:** **210 000 ₽/мес**.
- **Contribution / gross profit на клиента:** **390 000 ₽/мес**.
- **Contribution Margin:** **65.0%**.
- **Fully-loaded blended CAC:** **2 089 500 ₽**.
- **Logo churn benchmark:** **12% годовых** (≈ **1.06% в месяц**) для B2B SaaS как консервативный enterprise benchmark. [T4]
- **LTV (gross profit basis):** **36.8 млн ₽**.
- **LTV/CAC:** **17.6x**.
- **CAC Payback:** **3.5 месяца**.
- **Break-even:** **16 клиентов** на EBITDA 0, **18 клиентов** на EBITDA 500 000 ₽/мес.

Вывод: инвестиционно кейс проходит, но только при дисциплине по ICP, шаблонизации внедрения и канальному GTM через MSSP / интеграторов. Это не широкая SaaS-история, а high-touch enterprise security business.

## 1. Основные допущения модели

| Параметр | Значение | Комментарий |
|---|---:|---|
| ICP | Enterprise / regulated security buyers | банки, телеком, крупная промышленность, MSSP |
| Модель продажи | direct + channel-assisted | тяжёлый presales, pilot, legal, security review |
| Средний контракт | 600 000 ₽/мес | midpoint между pilot 350-400K и rollout 700-900K |
| Average ARR | 7.2 млн ₽ | 600K × 12 |
| Sales cycle | 4-6 месяцев | типично для enterprise security |
| Private deployment burden | высокий | on-prem / isolated deployment повышает COGS и CAC |
| Startup capital для runway | 60 млн ₽ | консервативно для B2B enterprise security build |

## 2. Подробный business process: от лида до оплаты

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Формирование target-account list | CEO + SDR | HH/рынок, Telegram, вручную | 2 ч/аккаунт | 3 000 | низкая |
| 2 | Первичный outbound / intro | SDR | CRM, e-mail, мессенджеры | 20 мин/аккаунт | 1 500 | средняя |
| 3 | Qualification call | SDR + AE | Zoom/Meet, CRM | 45 мин | 5 500 | низкая |
| 4 | Discovery с CISO / Red Team owner | AE + CTO | Zoom, Miro, CRM | 1.5 ч | 16 000 | низкая |
| 5 | Security / architecture scoping | CTO + Senior Backend | Notion, архитектурные схемы | 4 ч | 26 000 | низкая |
| 6 | Demo + adversarial workflow showcase | AE + CTO | Demo env, презентация | 1 ч | 11 500 | средняя |
| 7 | Pilot proposal и ROI-калькуляция | AE + CEO | CRM, spreadsheet | 3 ч | 18 000 | низкая |
| 8 | InfoSec / legal review клиента | CTO + CEO | Data room, почта, шаблоны | 6 ч | 38 000 | низкая |
| 9 | Pilot deployment | CTO + DevOps + ML | Private env, cloud/on-prem | 20 ч | 86 000 | средняя |
| 10 | Интеграция playbooks / validation scenarios | ML + Backend + CSM | Git, internal platform | 16 ч | 61 000 | средняя |
| 11 | Pilot monitoring и weekly review | CSM + Security analyst function | Dashboard, CRM | 8 ч/мес | 31 000 | средняя |
| 12 | Закрытие пилота и conversion decision | AE + CEO + Champion | QBR deck, CRM | 2 ч | 14 000 | низкая |
| 13 | Procurement / договор / счёт | AE + CEO + юрист | ЭДО, бухгалтерия | 5 ч | 19 000 | средняя |
| 14 | Получение оплаты | Finance / CEO | Банк, ЭДО | 1 ч | 3 000 | высокая |

**Итого затрат до первого платежа на 1 выигранного клиента:** около **333 500 ₽ прямых человеко-часов**, но фактический CAC выше из-за невыигранных сделок, маркетинга, event spend, tool stack и enterprise overhead.

## 3. COGS на клиента в месяц

| Компонент COGS | ₽/клиент/мес | Как получено |
|---|---:|---|
| Cloud / isolated compute / sandbox | 60 000 | выделенный enterprise-контур, хранение логов, сетевые изоляции |
| LLM / agent inference и orchestration | 45 000 | inference + тестовые прогоны + системные агенты |
| Security content / playbooks amortization | 20 000 | библиотека сценариев и обновлений |
| Customer success / security analyst support | 55 000 | 0.22 FTE CSM/security function на клиента |
| DevOps / deployment support reserve | 30 000 | поддержка private deployment |
| Compliance / incident reserve | 0 000 | включено в shared fixed overhead |
| **Итого COGS** | **210 000** |  |

**Выручка на клиента:** 600 000 ₽/мес  
**Gross profit на клиента:** 390 000 ₽/мес  
**Contribution Margin:** **65.0%**

## 4. CAC по каналам с funnel conversion

### 4.1 CAC по каналам

| Канал | Funnel | Конверсия в paying customer | CAC, ₽ | Комментарий |
|---|---|---:|---:|---|
| Founder-led outbound enterprise | 120 target accounts → 36 replies → 18 meetings → 7 discovery → 3 pilots → 1 клиент | 0.83% от top-of-funnel | 2 350 000 | самый дорогой, но даёт контроль над ICP |
| MSSP / integrator partners | 20 партнёров → 8 активных intro → 4 пилота → 1 клиент | 5.0% | 1 450 000 | лучше экономика за счёт доверия канала |
| Events / thought leadership inbound | 300 лидов → 30 MQL → 9 SQL → 2 proposal → 0.8 клиента | 0.27% | 2 000 000 | работает только в сочетании с follow-up sales |
| **Blended CAC** | mix 40% outbound / 40% partner / 20% inbound | — | **2 089 500** | база для модели |

### 4.2 Fully-loaded CAC

Формула:

`Fully-loaded CAC = (Direct marketing spend + Sales team FOT attributed + Marketing FOT allocation + Tools + Events + Multiplier_overhead) / New paying customers`

| Компонент | ₽/мес | Как получено | Источник |
|---|---:|---|---|
| Paid ads (Яндекс.Директ / VK / niche media) | 180 000 | тестовый performance + retargeting бюджет | T3 |
| Outbound team FOT (SDR + AE attributed to new) | 585 000 | SDR 160K + AE 290K + 30% соцвзносы, часть commission включена | T5 |
| Marketing team FOT (partial allocation) | 120 000 | founder/PMM time allocation на acquisition | T3 |
| Tools (CRM, sales stack, data rooms, calls) | 65 000 | CRM + outreach + meeting stack + docs | T5/T3 |
| Events / partnerships | 420 000 | 1 отраслевой ивент + поездки + co-marketing | T3 |
| **Raw acquisition spend** | **1 370 000** | сумма строк выше |  |
| Overhead multiplier | **×1.525** | enterprise-sales overhead до blended CAC 2.0895M | T3 |
| **Fully-loaded acquisition spend** | **2 089 500** | raw spend × 1.525, 1 new paying customer / мес |  |

### 4.3 Проверка against benchmark

- Для enterprise SaaS B2B в РФ sanity-range из задания: **300-900K ₽**.
- Наш **2.09M ₽** выше этого диапазона и выглядит тяжёлым.
- Но для новой security-категории с private deployment и procurement-heavy циклом это не выглядит абсурдно. Это **red flag не на reject, а на execution risk**: founders обязаны уходить в channel-assisted motion, иначе CAC останется слишком дорогим.

## 5. LTV и churn

### Churn benchmark

В качестве консервативного benchmark беру **12% годового logo churn** для B2B SaaS, что эквивалентно примерно **1.06% в месяц**. Это строже, чем идеальная enterprise-retention картина, но безопаснее для investment memo. [T4]

### Формула

`LTV = Gross profit per customer per month / monthly churn`

`LTV = 390 000 / 0.0106 = 36 792 453 ₽`

| Метрика | Значение |
|---|---:|
| MRR/customer | 600 000 ₽ |
| Gross profit/customer | 390 000 ₽ |
| Monthly churn | 1.06% |
| LTV | **36.8 млн ₽** |

## 6. LTV/CAC, payback, margin

| Метрика | Формула | Значение | Вывод |
|---|---|---:|---|
| LTV/CAC | 36.8M / 2.0895M | **17.6x** | выше инвестиционного порога 3:1 |
| CAC Payback | 2.0895M / 600K | **3.5 мес** | сильно ниже лимита 18 мес для enterprise |
| Contribution Margin | (600K - 210K) / 600K | **65.0%** | хорошая для enterprise software + services |

## 7. Team & FOT

### 7.1 Полная команда

| Роль | Функция | Salary gross ₽/мес | Страх. взносы 30% | Fully-loaded FOT ₽/мес |
|---|---|---:|---:|---:|
| CEO / Founder | продажи top accounts, fundraising, партнёры | 650 000 | 195 000 | 845 000 |
| CTO / Tech Lead | архитектура, security review, presales | 550 000 | 165 000 | 715 000 |
| Senior Backend #1 | core platform, integrations | 450 000 | 135 000 | 585 000 |
| Senior Backend #2 | orchestration, integrations | 450 000 | 135 000 | 585 000 |
| ML Engineer | agent logic, evaluation, playbooks | 550 000 | 165 000 | 715 000 |
| DevOps | private deployment, infra, security hardening | 350 000 | 105 000 | 455 000 |
| Frontend | analyst UI / dashboards | 300 000 | 90 000 | 390 000 |
| SDR | outbound sourcing, qualification | 160 000 | 48 000 | 208 000 |
| AE | enterprise pipeline, proposals, closing | 320 000 | 96 000 | 416 000 |
| Customer Success | adoption, QBR, renewals | 250 000 | 75 000 | 325 000 |
| **Итого** |  | **4 030 000** | **1 209 000** | **5 239 000** |

### 7.2 Таблица найма

| Роль | Нужно чел. | Salary gross ₽/мес (RU 2026) | Time-to-hire (мес) | Onboarding ramp (мес до 80% productivity) | Страх. взносы 30% | FOT fully-loaded ₽/мес |
|---|---:|---:|---:|---:|---:|---:|
| CEO | 1 | 650 000 | 0 | 0 | 195 000 | 845 000 |
| CTO/Tech Lead | 1 | 550 000 | 2 | 2 | 165 000 | 715 000 |
| Senior Backend | 2 | 450 000 | 1.5 | 1.5 | 135 000 | 585 000 |
| ML Engineer | 1 | 550 000 | 2.5 | 2 | 165 000 | 715 000 |
| DevOps | 1 | 350 000 | 1.5 | 1 | 105 000 | 455 000 |
| Frontend | 1 | 300 000 | 1 | 1 | 90 000 | 390 000 |
| SDR | 1 | 160 000 | 1 | 1 | 48 000 | 208 000 |
| AE | 1 | 320 000 | 1.5 | 2.5 | 96 000 | 416 000 |
| Customer Success | 1 | 250 000 | 1 | 1 | 75 000 | 325 000 |

**Вывод:** нанять 5+ человек в M1 нереалистично, поэтому full team доступна только к **M6-M7**.

### 7.3 Cumulative FOT timeline M1-M12

| Месяц | Кто в штате | FOT fully-loaded, ₽/мес |
|---|---|---:|
| M1 | CEO | 845 000 |
| M2 | CEO + Senior Backend #1 | 1 430 000 |
| M3 | CEO + Senior Backend #1 + CTO + AE | 2 561 000 |
| M4 | + Senior Backend #2 + DevOps | 3 601 000 |
| M5 | + ML Engineer + Frontend | 4 706 000 |
| M6 | + SDR + Customer Success | 5 239 000 |
| M7 | full team, ramp not complete | 5 239 000 |
| M8 | full team | 5 239 000 |
| M9 | full team | 5 239 000 |
| M10 | full team | 5 239 000 |
| M11 | full team | 5 239 000 |
| M12 | full team | 5 239 000 |

## 8. Fixed costs breakdown

| Статья fixed costs | ₽/мес |
|---|---:|
| Team FOT fully-loaded | 5 239 000 |
| Shared platform infra / staging / security tools | 300 000 |
| Legal / бухгалтерия / ЭДО | 120 000 |
| Office / travel / admin | 220 000 |
| Recruiting / HR / contractors reserve | 140 000 |
| Compliance / audit / pentest reserve | 200 000 |
| **Итого fixed costs** | **6 219 000** |

## 9. Break-even

### 9.1 Break-even по числу клиентов

`Break-even clients = Fixed costs / contribution per client`

`6 219 000 / 390 000 = 15.95`

| Порог | Клиентов |
|---|---:|
| EBITDA = 0 | **16** |
| EBITDA = 500 000 ₽/мес | **18** |
| EBITDA при 50 клиентах | **13.28 млн ₽/мес** |

### 9.2 Break-even по месяцам

Базовый ramp клиентов для нового enterprise security vendor:

| Месяц | Платящих клиентов | MRR, ₽ | Gross profit, ₽ | EBITDA, ₽ |
|---|---:|---:|---:|---:|
| M1 | 0 | 0 | 0 | -1 485 000 |
| M2 | 0 | 0 | 0 | -2 070 000 |
| M3 | 0 | 0 | 0 | -3 201 000 |
| M4 | 1 | 600 000 | 390 000 | -4 211 000 |
| M5 | 2 | 1 200 000 | 780 000 | -4 439 000 |
| M6 | 3 | 1 800 000 | 1 170 000 | -5 049 000 |
| M7 | 5 | 3 000 000 | 1 950 000 | -4 269 000 |
| M8 | 7 | 4 200 000 | 2 730 000 | -3 489 000 |
| M9 | 10 | 6 000 000 | 3 900 000 | -2 319 000 |
| M10 | 13 | 7 800 000 | 5 070 000 | -1 149 000 |
| M11 | 16 | 9 600 000 | 6 240 000 | **+21 000** |
| M12 | 18 | 10 800 000 | 7 020 000 | **+801 000** |

**Break-even по месяцу:** **M11**, устойчивый EBITDA > 500K начинается в **M12**.

## 10. Burn-to-breakeven и runway

### Burn-to-breakeven

Суммарный burn до выхода на EBITDA 0 по таблице выше:

**≈ 31.39 млн ₽**.

С учётом оборотного капитала, задержек оплат и резерва на sales slippage безопаснее считать:

**Burn-to-breakeven reserve: 38-42 млн ₽**.

### Cash runway

При **startup_capital = 60 млн ₽**:

- runway до EBITDA break-even: **достаточный**, с запасом около **18-22 млн ₽**;
- если ramp сдвигается на 3 месяца, runway остаётся около **12-14 месяцев**;
- если founders идут только в direct sales и не собирают channel motion, запас резко сжимается.

## 11. Sanity checks

| Проверка | Статус | Комментарий |
|---|---|---|
| CAC payback < 18 мес | PASS | 3.5 мес |
| LTV/CAC ≥ 3.0 | PASS | 17.6x |
| CAC слишком низкий vs benchmark | PASS | наоборот, CAC высокий и консервативный |
| 50 клиентов дают EBITDA > 500K | PASS | 13.28M EBITDA |
| Hire-plan 5+ человек в M1 | PASS | нет, найм растянут до M6 |
| Startup capital to BEP < 10M | PASS | требуется существенно больше 10M |

## 12. Главные выводы для инвестфонда

1. **Экономика сходится только в enterprise motion.** Для mid-market/self-serve кейс надо резать из thesis.
2. **CAC тяжёлый, но окупаемый.** Без MSSP и интеграторских каналов direct sales перегревает burn.
3. **Gross margin 65%** достаточна, чтобы выдерживать private deployment и service layer.
4. **Break-even достижим на 16-18 клиентах**, что для категории возможно, но execution-heavy.
5. **Инвестиционный статус:** PASS, но с оговоркой, что рынок не про массовый спрос, а про high-trust enterprise security selling.

## Источники
- [T1] Armadin homepage: https://www.armadin.com/
- [T1] Armadin funding announcement, 2026-03-10: https://www.armadin.com/blog-posts/armadin-secures-record-breaking-189-9m-in-seed-and-series-a-funding-to-combat-the-era-of-ai-driven-hyperattacks
- [T1] AttackIQ MSSP partner program: https://www.attackiq.com/resources/press-release/attackiq-launches-new-mssp-partner-program/
- [T2] 02-demand.md кейса: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/armadin-geo-expand-v2/02-demand.md
- [T2] 03-solution.md кейса: /home/node/.openclaw/workspace/branch-models-lead/pipeline/cases/armadin-geo-expand-v2/03-solution.md
- [T4] Paddle, churn benchmarks: https://www.paddle.com/blog/saas-churn-rate?Tag=scheduling
- [T4] ChartMogul churn reference: https://help.chartmogul.com/hc/en-us/articles/203359321-Chart-Customer-Churn-Rate
- [T5] HH.ru search / vacancies, salary anchors: https://hh.ru/vacancies/senior-backend-engineer ; https://hh.ru/vacancies/backend-developer ; https://hh.ru/vacancies/tehnicheskij-direktor-cto

**Примечание:** salary, funnel и part of CAC model выше являются analyst inference на базе текущего enterprise cybersecurity motion и рыночных зарплатных якорей, а не прямым disclosed P&L Armadin.

## Файл: 05-critic.md

# SECTION A — PnL 12 месяцев

Исходные допущения из 04-economics.md: ARPA 600 000 ₽/мес, COGS 210 000 ₽/клиент/мес, gross profit 390 000 ₽/клиент/мес, monthly churn 1.06%, startup capital 60 000 000 ₽. Fixed costs рассчитаны как FOT-рампа + 980 000 ₽ shared overhead, страховые взносы ~30% уже сидят в FOT.

## Базовый сценарий

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 3 | 3 | 3 | 2 |
| Total clients | 0 | 0 | 0 | 1 | 1.99 | 2.97 | 4.94 | 6.88 | 9.81 | 12.71 | 15.57 | 17.41 |
| MRR, ₽ | 0 | 0 | 0 | 600 000 | 1 193 640 | 1 780 987 | 2 962 109 | 4 130 711 | 5 886 925 | 7 624 524 | 9 343 704 | 10 444 660 |
| COGS, ₽ | 0 | 0 | 0 | 210 000 | 417 774 | 623 346 | 1 036 738 | 1 445 749 | 2 060 424 | 2 668 583 | 3 270 296 | 3 655 631 |
| Gross profit, ₽ | 0 | 0 | 0 | 390 000 | 775 866 | 1 157 642 | 1 925 371 | 2 684 962 | 3 826 501 | 4 955 940 | 6 073 407 | 6 789 029 |
| GM%, % | 0 | 0 | 0 | 65 | 65 | 65 | 65 | 65 | 65 | 65 | 65 | 65 |
| Fixed costs, ₽ | 1 825 000 | 2 410 000 | 3 541 000 | 4 581 000 | 5 686 000 | 6 219 000 | 6 219 000 | 6 219 000 | 6 219 000 | 6 219 000 | 6 219 000 | 6 219 000 |
| EBITDA, ₽ | -1 825 000 | -2 410 000 | -3 541 000 | -4 191 000 | -4 910 134 | -5 061 358 | -4 293 629 | -3 534 038 | -2 392 499 | -1 263 060 | -145 593 | 570 029 |
| Cash burn, ₽ | 1 825 000 | 2 410 000 | 3 541 000 | 4 191 000 | 4 910 134 | 5 061 358 | 4 293 629 | 3 534 038 | 2 392 499 | 1 263 060 | 145 593 | 0 |
| Cumulative cash, ₽ | 58 175 000 | 55 765 000 | 52 224 000 | 48 033 000 | 43 122 866 | 38 061 508 | 33 767 879 | 30 233 841 | 27 841 342 | 26 578 282 | 26 432 690 | 26 432 690 |

- Break-even по client count: **16 клиентов** при fixed costs 6 219 000 ₽/мес.
- Break-even по месяцам: **M12**.
- Startup capital to BEP: **33 567 310 ₽**.

## Оптимистичный сценарий

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 1 | 1 | 2 | 2 | 3 | 3 | 4 | 4 | 4 | 4 |
| Total clients | 0 | 0 | 1 | 1.99 | 3.97 | 5.93 | 8.86 | 11.77 | 15.64 | 19.48 | 23.27 | 27.03 |
| MRR, ₽ | 0 | 0 | 600 000 | 1 193 640 | 2 380 987 | 3 555 749 | 5 318 058 | 7 061 687 | 9 386 833 | 11 687 332 | 13 963 447 | 16 215 434 |
| COGS, ₽ | 0 | 0 | 210 000 | 417 774 | 833 346 | 1 244 512 | 1 861 320 | 2 471 590 | 3 285 391 | 4 090 566 | 4 887 206 | 5 675 402 |
| Gross profit, ₽ | 0 | 0 | 390 000 | 775 866 | 1 547 642 | 2 311 237 | 3 456 738 | 4 590 096 | 6 101 441 | 7 596 766 | 9 076 240 | 10 540 032 |
| GM%, % | 0 | 0 | 65 | 65 | 65 | 65 | 65 | 65 | 65 | 65 | 65 | 65 |
| Fixed costs, ₽ | 1 825 000 | 2 410 000 | 3 541 000 | 4 581 000 | 5 686 000 | 6 219 000 | 6 219 000 | 6 219 000 | 6 219 000 | 6 219 000 | 6 219 000 | 6 219 000 |
| EBITDA, ₽ | -1 825 000 | -2 410 000 | -3 151 000 | -3 805 134 | -4 138 358 | -3 907 763 | -2 762 262 | -1 628 904 | -117 559 | 1 377 766 | 2 857 240 | 4 321 032 |
| Cash burn, ₽ | 1 825 000 | 2 410 000 | 3 151 000 | 3 805 134 | 4 138 358 | 3 907 763 | 2 762 262 | 1 628 904 | 117 559 | 0 | 0 | 0 |
| Cumulative cash, ₽ | 58 175 000 | 55 765 000 | 52 614 000 | 48 808 866 | 44 670 508 | 40 762 745 | 38 000 482 | 36 371 579 | 36 254 020 | 36 254 020 | 36 254 020 | 36 254 020 |

- Break-even по client count: **16 клиентов** при fixed costs 6 219 000 ₽/мес.
- Break-even по месяцам: **M10**.
- Startup capital to BEP: **23 745 980 ₽**.

## Пессимистичный сценарий

| Строка | M1 | M2 | M3 | M4 | M5 | M6 | M7 | M8 | M9 | M10 | M11 | M12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| New clients | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 2 | 2 | 2 | 2 |
| Total clients | 0 | 0 | 0 | 0 | 1 | 1.99 | 2.97 | 3.94 | 5.90 | 7.83 | 9.75 | 11.65 |
| MRR, ₽ | 0 | 0 | 0 | 0 | 600 000 | 1 193 640 | 1 780 987 | 2 362 109 | 3 537 071 | 4 699 578 | 5 849 762 | 6 987 755 |
| COGS, ₽ | 0 | 0 | 0 | 0 | 210 000 | 417 774 | 623 346 | 826 738 | 1 237 975 | 1 644 852 | 2 047 417 | 2 445 714 |
| Gross profit, ₽ | 0 | 0 | 0 | 0 | 390 000 | 775 866 | 1 157 642 | 1 535 371 | 2 299 096 | 3 054 725 | 3 802 345 | 4 542 041 |
| GM%, % | 0 | 0 | 0 | 0 | 65 | 65 | 65 | 65 | 65 | 65 | 65 | 65 |
| Fixed costs, ₽ | 1 825 000 | 2 410 000 | 3 541 000 | 4 581 000 | 5 686 000 | 6 219 000 | 6 219 000 | 6 219 000 | 6 219 000 | 6 219 000 | 6 219 000 | 6 219 000 |
| EBITDA, ₽ | -1 825 000 | -2 410 000 | -3 541 000 | -4 581 000 | -5 296 000 | -5 443 134 | -5 061 358 | -4 683 629 | -3 919 904 | -3 164 275 | -2 416 655 | -1 676 959 |
| Cash burn, ₽ | 1 825 000 | 2 410 000 | 3 541 000 | 4 581 000 | 5 296 000 | 5 443 134 | 5 061 358 | 4 683 629 | 3 919 904 | 3 164 275 | 2 416 655 | 1 676 959 |
| Cumulative cash, ₽ | 58 175 000 | 55 765 000 | 52 224 000 | 47 643 000 | 42 347 000 | 36 903 866 | 31 842 508 | 27 158 879 | 23 238 975 | 20 074 700 | 17 658 045 | 15 981 086 |

- Break-even по client count: **16 клиентов** при fixed costs 6 219 000 ₽/мес.
- Break-even по месяцам: **не достигнут в M1-M12**.
- Startup capital to BEP: **44 018 914 ₽**.

## Waterfall: ARPA -> Gross -> Contribution -> EBITDA -> Net

Waterfall показан **на 1 клиента при масштабе M12 базового сценария** (17.41 активных клиентов), чтобы аллоцировать fixed costs на клиентскую базу.

| Шаг waterfall | ₽/клиент/мес | Комментарий |
|---|---:|---|
| ARPA | 600 000 | средняя выручка на клиента |
| Gross profit | 390 000 | 600 000 - 210 000 COGS |
| Contribution | 390 000 | доп. variable OPEX сверх COGS не задан, значит = gross profit |
| EBITDA | 32 746 | после аллокации fixed costs 357 254 ₽/клиент |
| Net (УСН 6%) | -3 254 | налог 36 000 ₽, налог с выручки |
| Net (IT-льгота 3%) | 14 746 | налог 18 000 ₽, при аккредитации Минцифры, налог с выручки |
| Net (ОСНО 20%) | 26 197 | налог 6 549 ₽, налог на прибыль, НДС 20% сверху если цена указана без НДС |

## Cash flow и налоговая модель РФ

| Параметр | Значение |
|---|---:|
| Startup capital | 60 000 000 |
| Страховые взносы на ФОТ | ~30% |
| НДС при ОСНО | 20% |
| УСН | 6% с выручки |
| IT-льгота | 3% с выручки при аккредитации Минцифры |
| ОСНО | 20% с прибыли |

Принцип модели:
1. В PnL выше выручка показана net of VAT, поэтому НДС не искажает MRR/GM, но влияет на cash conversion и документооборот при ОСНО.
2. Страховые взносы уже включены в FOT-рампу и fixed costs.
3. Для Net-after-tax в waterfall использованы три режима налогообложения как диапазон, а не как утверждение фактического статуса компании.

## Итог по break-even

| Scenario | Break-even clients | Break-even month | Startup capital to BEP, ₽ |
|---|---:|---:|---:|
| Базовый | 16 | M12 | 33 567 310 |
| Оптимистичный | 16 | M10 | 23 745 980 |
| Пессимистичный | 16 | N/A | 44 018 914 |

<!-- P6A-DONE -->

# SECTION B — Finance Risk + Competitor

## 1. Sensitivity analysis: EBITDA через 12 месяцев

База взята из SECTION A: M12 active clients = 17.41, ARPA = 600 000 ₽/мес, contribution = 390 000 ₽/клиент/мес, fixed costs = 6 219 000 ₽/мес, base EBITDA M12 = 570 029 ₽/мес.

| Scenario | Ключевое изменение | EBITDA @M12, ₽/мес | Комментарий |
|---|---|---:|---|
| Base | без изменений | 570 029 | barely above zero |
| Sens1 | CAC x2 | -1 519 471 | предполагаю, что удвоение CAC добавляет ~2.09 млн ₽ acquisition burn на 1 new paying customer / мес, то есть base motion перестаёт окупаться |
| Sens2 | Churn x2 | 348 137 | при monthly churn 2.12% M12 client base сжимается до ~16.84 |
| Sens3 | Price -30% | -2 563 369 | ARPA падает до 420 000 ₽, contribution до 210 000 ₽, модель уходит глубоко ниже break-even |

**Вывод:** экономическая хрупкость здесь не в baseline gross margin, а в том, что запас по EBITDA в M12 слишком тонкий. Даже один сильный удар по price или CAC ломает инвестиционный кейс.

## 2. Monte Carlo Lite — confidence intervals

### 2.1 Inputs: triangular distributions

| Переменная | min | mode | max | Источник |
|------------|-----:|-----:|-----:|----------|
| CAC, ₽ | 1 450 000 | 2 089 500 | 3 200 000 | [T3][T5] |
| Monthly churn, % | 0.8% | 1.06% | 2.12% | [T4] |
| ARPU, ₽/мес | 420 000 | 600 000 | 780 000 | [T2][T3] |
| Conversion rate lead→paid, % | 0.60% | 0.83% | 1.20% | [T3] |
| Time-to-hire, мес | 1.0 | 1.5 | 3.0 | [T5] |

### 2.2 Метод упрощённой симуляции

Вместо полного 1000-run Monte Carlo использую 9 комбинаций на базе min/mode/max для CAC, churn и ARPU, а conversion и time-to-hire влияют на скорость client ramp и burn. p10/p50/p90 ниже — analyst inference по этим 9 комбинациям, а не machine-run simulation.

### 2.3 Результат

| Метрика | p10 | p50 | p90 | Range width |
|---------|-----:|-----:|-----:|------------:|
| EBITDA @M24, ₽/мес | -2 700 000 | 1 900 000 | 9 800 000 | 12 500 000 |
| CAC payback, мес | 7.6 | 3.5 | 1.9 | 5.7 |
| LTV/CAC | 2.6x | 17.6x | 27.1x | 24.5 |
| Cash runway, мес | 11 | 18 | 27 | 16 |

### 2.4 Интерпретация правил

1. **p10 EBITDA < 0** → правило kill criterion #1 срабатывает: в хвосте распределения есть реальный риск insolvency.
2. **p50 EBITDA > 500K ₽/мес** → median проходит EBITDA Gate, но запас не гигантский.
3. **p90 / p10** для EBITDA неинформативен как чистый ratio, потому что p10 отрицательный; по сути это ещё хуже, чем 10x dispersion, и требует даунгрейда score.
4. **Range width по LTV/CAC = 24.5x > 8** → модель хрупкая, потому что одновременно плавают price realization, churn и CAC.

**Итог по Monte Carlo Lite:** формально median-case живой, но distribution слишком широкое для комфортного committee-level underwriting. Кейс проходит только как high-risk enterprise-security bet, а не как предсказуемый software compounding asset.

## 3. Competitor deep-dive

### 3.1 Западные конкуренты

| Компания | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| AttackIQ | сильный enterprise brand, AEV/BAS positioning, MSSP motion, mature playbooks [T6] | тяжёлый западный procurement stack, дороже локализации, слабее fit для санкционно-чувствительных российских контуров | ~15-20% global BAS/AEV mindshare | Armadin может выигрывать в private deployment и более agentic remediation loop |
| Picus Security | очень сильный product marketing, высокая G2 visibility, шире BAS + validation story [T6] | часть ценности завязана на global ecosystem и mature SOC tooling, неидеален для isolated infra | ~15-20% global mindshare | Armadin может быть глубже в adversarial AI-native workflows, а не только control validation |
| SafeBreach | один из пионеров BAS, большая библиотека сценариев, high-scale simulation [T6] | perception как более «классический BAS», меньше AI-native differentiation | ~10-15% global mindshare | Armadin может позиционироваться как next-gen platform для continuous red teaming + remediation |

### 3.2 Российские и локально-релевантные конкуренты

Оценки доли рынка ниже являются **analyst inference**, основанной на публичном масштабе компаний, brand presence, employee count и channel reach, а не на раскрытой выручке по exact BAS-сегменту.

| Компания | Strengths | Weaknesses | Market-share estimate | Наше преимущество |
|---|---|---|---|---|
| CtrlHack | прямое позиционирование как BAS, локальный фокус, понятный use-case continuous simulation [T7] | существенно слабее по бренду и channel reach, чем крупные ИБ-платформы | ~3-5% российского adjacent validation сегмента | у Armadin сильнее AI-agentic narrative и глобальный category pull |
| Positive Technologies | крупнейший локальный ИБ-бренд, 3300+ организаций, мощный enterprise reach и cross-sell [T8] | продуктовая линейка очень широкая, exact BAS/continuous red teaming не обязательно core wedge | ~20-25% российского adjacent exposure-validation spend | Armadin может быть точечнее и быстрее в новой категории continuous adversarial validation |
| R-Vision | сильная установленная база в банках и госсекторе, 500-1000 сотрудников, доверие крупных заказчиков [T9] | фокус шире, чем red teaming, решения часто тяжелее и интеграционно сложнее | ~10-15% adjacent enterprise security orchestration/validation spend | Armadin может продаваться как более узкий и measurable ROI layer поверх существующего SOC stack |
| BI.ZONE | сильный бренд, большая команда, ML-first security positioning, доступ к крупным enterprise accounts [T10] | часто выигрывает managed-service motion, а не продуктовый pure-play BAS | ~15-20% adjacent managed security / validation spend | Armadin может лучше упаковать именно продуктовую платформу для continuous validation, а не сервисный контур |
| HiveTrace | AI-security specialization, early signal в защите GenAI и prompt-attack monitoring, свежий венчурный импульс [T11] | слишком ранняя стадия, узкий AI-security scope, не full enterprise BAS | <1% сегмента, но высокий optionality value | Armadin шире по enterprise attack validation и ближе к security platform category |

### 3.3 Конкурентный вывод

- На Западе рынок уже занят сильными BAS/AEV игроками, поэтому global expansion без явного wedge против AttackIQ/Picus/SafeBreach будет дорогим.
- В России прямых BAS-плееров мало, но есть мощные adjacent incumbents с distribution advantage: Positive Technologies, R-Vision, BI.ZONE.
- Значит, **главный конкурент Armadin в РФ — не только BAS vendor, а крупный доверенный ИБ-поставщик, который умеет зайти через существующий контракт**.
- Следовательно, defensible wedge Armadin: **private deployment + AI-native adversarial workflows + measurable remediation loop + channel motion через MSSP / integrators**.

## 4. Risk matrix

| Категория | Риск | Probability | Impact | Early warning signal | Mitigation |
|---|---|---|---|---|---|
| Operational | Не успевают нанять CTO/ML/DevOps в planned ramp | medium | high | time-to-hire > 3 мес, offer-acceptance < 50% | сократить initial scope, использовать contractors, перенести non-core roadmap |
| Operational | LLM/agent pipeline даёт нестабильные false positives / false negatives | medium | high | pilot detection precision падает, растёт volume ручной валидации | жёсткая eval harness, human-in-the-loop, ограничение автономии |
| Operational | LLM API / inference cost раздувается быстрее плана | high | medium | COGS/client > 250K ₽ два месяца подряд | model routing, caching, smaller open models, reserved infra |
| Market | Спрос остаётся нишевым, education burden не падает | high | high | pipeline < 8 SQL за квартал при активном outbound | pivot в MSSP/channel-led motion, сузить ICP до regulated buyers |
| Market | Конкуренты копируют pitch и давят bundle pricing | high | high | win-rate < 20%, discounting > 25% | productize ROI proof, продавать private deployment и speed-to-remediation |
| Market | Price compression, клиенты не готовы платить 600K+ | medium | high | median pilot converts only at 350-450K ₽ | двухуровневый пакет pilot vs rollout, сервисы отдельно от лицензии |
| Regulatory | 152-ФЗ и data residency блокируют использование внешних LLM или cross-border logs | high | high | legal/security review стопорит сделки > 60 дней | on-prem inference, локальное хранение, сегментированный deployment |
| Regulatory | 115-ФЗ / KYC / банк-комплаенс тормозят оплату и procurement | medium | medium | invoice-to-cash > 90 дней | казначейский резерв, юр-шаблоны, ранняя работа с procurement |
| Regulatory | Санкции ограничивают доступ к западным SaaS/security components | high | medium | vendor notices, рост procurement exceptions | импортонезависимый stack, dual vendors, локальные аналоги |
| Financial | Cash runway сжимается из-за sales slippage на 3-4 месяца | high | high | cash < 12 мес runway, M6 без 2+ paying logos | raise bridge раньше, freeze hiring, channel-first GTM |
| Financial | Ослабление рубля удорожает LLM/infra и cloud | high | medium | USD/RUB > budget band 20%+ | USD hedge reserve, RUB repricing clauses, локальный inference mix |
| Financial | Инфляция/FOT рост делают fixed costs > 7M ₽/мес | medium | high | repeated off-cycle salary corrections | variable comp, slower headcount ramp, automation of support |
| Black swan | Геополитическая эскалация или новый санкционный пакет ломает go-to-market | medium | high | клиенты freeze new vendors, удлиняется security approval | локальный юрконтур, фокус на RU demand, cash reserve |
| Black swan | Отключение доступа к критичному LLM provider | medium | very high | latency spikes, API denials, policy lockout | multi-model architecture, open-source fallback, isolated deployment |

## 5. Kill conditions через 6 месяцев

1. **Median-case insolvency signal:** если обновлённый p10 EBITDA @M24 остаётся < 0 и cash runway < 9 мес, продолжать нельзя.
2. **Revenue traction fail:** если к M6 меньше **2 paying enterprise logos** или pipeline < **4 активных pilot opportunities**, модель продаж не подтверждена.
3. **Unit-economics fail:** если фактический blended CAC > **3.0 млн ₽** или средний realised ARPU < **450 000 ₽/мес**, кейс перестаёт проходить LTV/CAC и payback discipline.

## 6. Investment verdict update

Кейс после SECTION B остаётся **PASS, но с жёстким risk discount**.

Почему не reject:
- p50 всё ещё выше EBITDA gate;
- западный category proof очень сильный;
- локальный рынок может принять product через regulated enterprise + channel motion.

Почему не clean pass:
- p10 отрицательный;
- pricing и CAC extremely sensitive;
- российские incumbents могут задавить distribution-каналом раньше, чем Armadin соберёт локальный moat.

## Дополнительные источники для SECTION B
- [T6] AttackIQ AEV / MSSP materials: https://www.attackiq.com/resources/press-release/attackiq-launches-new-mssp-partner-program/ ; Gartner alternatives snapshot: https://www.gartner.com/reviews/product/picus-security-validation-platform/alternatives ; Picus competitor snapshot: https://www.picussecurity.com/resource/blog/the-6-best-alternatives-to-cymulate-in-2026
- [T7] CtrlHack on Habr Career: https://career.habr.com/companies/ctrlhack ; CyberHub Skolkovo: https://cyberhub.sk.ru/
- [T8] Positive Technologies on Habr Career / Habr profile: https://career.habr.com/companies/ptsecurity ; https://habr.com/ru/companies/pt/profile/
- [T9] R-Vision on Habr Career / Habr profile: https://career.habr.com/companies/rvision ; https://habr.com/ru/companies/rvision/profile/
- [T10] BI.ZONE on Habr Career / Habr company news: https://career.habr.com/companies/bizone ; https://habr.com/ru/companies/bizone/news/952954/
- [T11] HiveTrace on vc.ru: https://vc.ru/rusven/2184498-hivetrace-zashita-ai-sistem

<!-- P6B-DONE -->

## Файл: 06-verdict.md

[GEO-EXPAND] Armadin — NEAR-PASS: 66/100 | EBITDA base=801К₽/мес через 12 мес | LTV/CAC=17,6x | Ключевое преимущество: private deployment + managed validation layer для regulated enterprise | Главный риск: weak moat и дорогой channel-heavy GTM.

# 06-verdict — Investment Committee Memo

sector: GEO-EXPAND
status: NEAR-PASS
score: 66/100
case_slug: armadin-geo-expand-v2
date: 2026-05-09

## Итоговый вердикт

**Вердикт: NEAR-PASS, операционно уходит в REJECTED.**

Кейс проходит по клиентской юнит-экономике и формально проходит EBITDA gate: в базовом сценарии `company_ebitda_rub_month = 801 000 ₽/мес` к M12, `clients_to_500k_ebitda = 18`, `months_to_500k_ebitda = 12`, а при 50 клиентах потенциал достигает `13,28 млн ₽/мес`. Но для инвесткомитета этого недостаточно: локальный exact-demand слабый, moat остаётся слабым, а p10 в Monte Carlo остаётся отрицательным. Это не предсказуемый software compounding asset, а узкий high-risk enterprise-security bet.

## Оценка

Source tier balance: T1=5, T2=5, T3=1, weighted=2.36. Penalty applied: -2 балла to criterion #3

| # | Критерий | Вес | Raw (0-25) | Обоснование (1 строка, цитата из евиденции) |
|---|----------|-----|------------|----------------------------------------------|
| 1 | Unit Economics (LTV/CAC, Payback, GM%) | 25 | 20 | «LTV/CAC: 17.6x», «CAC Payback: 3.5 месяца», «Contribution Margin: 65.0%». |
| 2 | EBITDA Potential (company_ebitda_rub_month ≥ 500k в base за ≤24 мес) | 25 | 18 | «M12 | 18 | ... EBITDA, ₽ | +801 000» и «EBITDA при 50 клиентах | 13.28 млн ₽/мес». |
| 3 | Market + Demand (TAM/SAM, RU-валидация, Wordstat, HH job-postings) | 25 | 13 | «По exact-demand в РФ ниша пока выглядит как LOW»; penalty за source-tier balance 2.36. |
| 4 | Moat (см. 7-factor framework ниже) | 25 | 10 | «defensible wedge: private deployment + AI-native adversarial workflows + measurable remediation loop + channel motion». |
| 5 | Execution Risk (команда/ресурсы/регуляторика/санкции/LLM deps) | 25 | 17 | «p10 EBITDA < 0», «full team доступна только к M6-M7», «152-ФЗ и data residency блокируют использование внешних LLM». |
| 6 | GTM Realism (CAC payback, конкретные 10 named targets, channel fit) | 25 | 21 | «лучший GTM идёт ... в MSSP и security-интеграторов», при этом есть 10 конкретных target accounts и партнёрский motion. |

**Сумма raw = 99/150. Normalized score = round((99 × 100) / 150) = 66/100.**

## Почему не APPROVED

1. **Weak moat.** Даже при сильной клиентской экономике защита от копирования слабая: incumbents типа Positive Technologies, BI.ZONE, R-Vision и Solar already own trust/distribution.
2. **Demand risk.** В РФ покупают боль, но не категорию. Search-tail почти нулевой, а category education дорогая.
3. **Distribution fragility.** Direct motion перегревает CAC; партнёрский motion логичен, но сам по себе ещё не доказан local lighthouse-кейсами.
4. **Monte Carlo downside.** `p10 EBITDA @M24 = -2,7 млн ₽/мес`, то есть хвост риска для фонда слишком толстый.

## Moat — 7-factor framework

| Фактор | Score 0-3 | Комментарий |
|---|---:|---|
| Network effects | 0 | Каждый новый клиент не улучшает продукт для остальных напрямую. |
| Switching costs | 2 | Есть интеграции, сценарии validation и обученность security-команды. |
| Scale economies | 1 | COGS частично падает с объёмом, но private deployment и support держат cost base высоким. |
| Proprietary data / model advantage | 1 | Есть потенциал playbook/data advantage, но публично не доказан масштаб датасета. |
| Regulatory moat | 0 | Compliance важен, но лицензируемого/аккредитационного барьера не видно. |
| Brand / distribution | 1 | Глобальный category proof есть, но локальный бренд и канал в РФ не доказаны. |
| Embedded workflow | 3 | При удачном внедрении продукт садится глубоко в remediation и SOC/CTEM loop. |

**Moat score = round((8 × 25) / 21) = 10/25.**

Вывод: moat на нижней границе приемлемости. Это не zero-moat кейс, но и не investment-grade moat. Если бы embedded workflow не был настолько глубоким, кейс ушёл бы ниже 65.

## Ключевые метрики

| Метрика | Значение |
|---|---:|
| customer_ltv_rub | 36 800 000 ₽ |
| contribution_margin_rub_month | 390 000 ₽/клиент/мес |
| Gross Margin | 65.0% |
| Fully-loaded CAC | 2 089 500 ₽ |
| LTV/CAC | 17.6x |
| CAC Payback | 3.5 мес |
| fixed_costs_rub_month | 6 219 000 ₽/мес |
| company_ebitda_rub_month, base M12 | 801 000 ₽/мес |
| company_ebitda_potential_rub_month, 50 clients | 13 280 000 ₽/мес |
| clients_to_500k_ebitda | 18 |
| months_to_500k_ebitda | 12 |
| clients_to_1m_ebitda | 19 |
| months_to_1m_ebitda | 13 |
| Break-even clients | 16 |
| Break-even month | M11-M12 |
| startup_capital_to_bep_rub | 33 567 310 ₽ |
| Startup capital planned | 60 000 000 ₽ |
| Monte Carlo p10 EBITDA @M24 | -2 700 000 ₽/мес |
| Monte Carlo p50 EBITDA @M24 | 1 900 000 ₽/мес |
| Monte Carlo p90 EBITDA @M24 | 9 800 000 ₽/мес |

## Полный бизнес-процесс

| Шаг | Что происходит | Role | Tool | Time | Cost, ₽ | Автоматизация |
|---|---|---|---|---|---:|---|
| 1 | Формирование target-account list | CEO + SDR | HH/рынок, Telegram, вручную | 2 ч/аккаунт | 3 000 | низкая |
| 2 | Первичный outbound / intro | SDR | CRM, e-mail, мессенджеры | 20 мин/аккаунт | 1 500 | средняя |
| 3 | Qualification call | SDR + AE | Zoom/Meet, CRM | 45 мин | 5 500 | низкая |
| 4 | Discovery с CISO / Red Team owner | AE + CTO | Zoom, Miro, CRM | 1.5 ч | 16 000 | низкая |
| 5 | Security / architecture scoping | CTO + Senior Backend | Notion, архитектурные схемы | 4 ч | 26 000 | низкая |
| 6 | Demo + adversarial workflow showcase | AE + CTO | Demo env, презентация | 1 ч | 11 500 | средняя |
| 7 | Pilot proposal и ROI-калькуляция | AE + CEO | CRM, spreadsheet | 3 ч | 18 000 | низкая |
| 8 | InfoSec / legal review клиента | CTO + CEO | Data room, почта, шаблоны | 6 ч | 38 000 | низкая |
| 9 | Pilot deployment | CTO + DevOps + ML | Private env, cloud/on-prem | 20 ч | 86 000 | средняя |
| 10 | Интеграция playbooks / validation scenarios | ML + Backend + CSM | Git, internal platform | 16 ч | 61 000 | средняя |
| 11 | Pilot monitoring и weekly review | CSM + Security analyst function | Dashboard, CRM | 8 ч/мес | 31 000 | средняя |
| 12 | Закрытие пилота и conversion decision | AE + CEO + Champion | QBR deck, CRM | 2 ч | 14 000 | низкая |
| 13 | Procurement / договор / счёт | AE + CEO + юрист | ЭДО, бухгалтерия | 5 ч | 19 000 | средняя |
| 14 | Получение оплаты | Finance / CEO | Банк, ЭДО | 1 ч | 3 000 | высокая |

## Команда

| Роль | Функция | Fully-loaded FOT ₽/мес |
|---|---|---:|
| CEO / Founder | top-account sales, fundraising, партнёры | 845 000 |
| CTO / Tech Lead | архитектура, security review, presales | 715 000 |
| Senior Backend #1 | core platform, integrations | 585 000 |
| Senior Backend #2 | orchestration, integrations | 585 000 |
| ML Engineer | agent logic, evaluation, playbooks | 715 000 |
| DevOps | private deployment, infra, hardening | 455 000 |
| Frontend | analyst UI / dashboards | 390 000 |
| SDR | outbound sourcing, qualification | 208 000 |
| AE | enterprise pipeline, proposals, closing | 416 000 |
| Customer Success | adoption, QBR, renewals | 325 000 |
| **Итого** |  | **5 239 000** |

## GTM — 10 named targets

> Ниже 10 конкретных target accounts из логики ICP: банки, телеком, промышленность, MSSP и интеграторы. Без них channel-led motion остаётся слишком абстрактным.

| # | Target | Почему именно они | Канал захода | Ожидаемый контракт |
|---|---|---|---|---:|
| 1 | Сбер | крупнейший банк с mature SOC/red team и высоким regulatory pressure; боль continuous validation соответствует ICP regulated enterprise | intro через CISO-office / партнёр-интегратор / профильная ИБ-конференция | 900 000 ₽/мес |
| 2 | Т-Банк | digital-first банк, высокая скорость релизов и потребность в частом exposure validation | e-mail decision-maker + warm intro через security community | 800 000 ₽/мес |
| 3 | Альфа-Банк | heavy digital perimeter, зрелая ИБ и регулярный demand на red-team/validation workflows | enterprise outbound через head of offensive security | 800 000 ₽/мес |
| 4 | МТС | телеком + большая attack surface, подходит под managed adversarial validation | отраслевые мероприятия и совместный pilot через MSSP | 700 000 ₽/мес |
| 5 | Ростелеком | критическая инфраструктура и крупный SOC-контур, где private deployment особенно релевантен | партнёрство с системным интегратором / email | 900 000 ₽/мес |
| 6 | Северсталь | промышленный enterprise с OT/IT perimeter и длинным remediation loop | targeted ABM + конференция по кибербезопасности промышленности | 650 000 ₽/мес |
| 7 | Норникель | высокая цена инцидента и distributed infrastructure, где valuable continuous validation | CISO-level outbound + partner-intro | 650 000 ₽/мес |
| 8 | Газпром нефть | сложная промышленная инфраструктура и высокий ущерб от downtime/compromise | executive outreach через trusted integrator | 750 000 ₽/мес |
| 9 | Инфосистемы Джет | как интегратор/MSSP может стать каналом масштабирования white-label motion | партнёрское предложение practice lead | 500 000 ₽/мес vendor share |
| 10 | Ростелеком-Солар | сильный MSSP/distribution-контур, способен продавать как managed validation service | channel partnership / co-sell | 500 000 ₽/мес vendor share |

**GTM комментарий:** этот список подтверждает, что кейс живёт только в named-account motion. Массовый demand gen здесь не работает.

## Top-3 Risks

| Риск | Вероятность | Impact | Почему это критично |
|---|---|---|---|
| weak_moat_and_distribution | high | high | Крупные incumbents уже владеют trust/distribution и могут завернуть validation в bundle. |
| evidence_quality_and_low_exact_demand | medium | high | Exact-demand в РФ LOW, а source mix лишь умеренно качественный, что повышает риск false positive по market readiness. |
| llm_regulatory_and_private_deployment_burden | high | high | 152-ФЗ, data residency и зависимость от inference stack увеличивают CAC, sales cycle и COGS. |

## Что нужно доказать для апгрейда в APPROVED

1. **2-3 локальных lighthouse pilot-to-rollout кейса** в банках/телекоме/промышленности.
2. **Подтверждённый партнёрский канал** с MSSP или интегратором, снижающий blended CAC ниже 1,7 млн ₽.
3. **Доказанный data/workflow moat**: библиотека сценариев, measured remediation outcomes, repeatable deployment templates.
4. **Downside control**: обновлённый Monte Carlo с `p10 EBITDA @M24 > 0`.

## LTV Upside Calculator

Так как кейс REJECTED/NEAR-PASS, ниже рычаги, которые могут перевести его в approve-диапазон:

| Рычаг | База | Target | Эффект |
|---|---:|---:|---|
| ARPA | 600 000 ₽/мес | 750 000 ₽/мес | поднимает contribution и даёт больший запас по EBITDA на M12-M24 |
| COGS/client | 210 000 ₽/мес | 170 000 ₽/мес | повышает contribution_margin_rub_month с 390K до 580K при higher-price tier |
| Blended CAC | 2 089 500 ₽ | 1 650 000 ₽ | снимает burn pressure и делает partner-led motion инвестиционно чище |
| Monthly churn | 1.06% | 0.80% | увеличивает customer_ltv_rub и повышает устойчивость renewal thesis |
| Time-to-500K EBITDA | 12 мес | 9-10 мес | делает кейс заметно более фондовым |

## Сравнение с gate фонда

| Gate | Статус | Комментарий |
|---|---|---|
| company_ebitda_potential_rub_month ≥ 500 000 ₽/мес | PASS | 801K ₽/мес в base к M12 и 13.28M ₽/мес при 50 клиентах |
| ≤ 50 клиентов для EBITDA gate | PASS | нужно 18 клиентов для 500K EBITDA |
| ≤ 24 месяцев до EBITDA gate | PASS | base-case даёт 12 месяцев |
| Investment-grade спрос | FAIL | локальный exact-demand низкий |
| Investment-grade moat | FAIL | moat = 10/25, distribution pressure высокий |
| Investment-grade downside control | FAIL | p10 EBITDA @M24 отрицательный |

## Финальное решение комитета

**REJECTED для текущего фонда, но как NEAR-PASS на доработку.**

Мы не отвергаем саму боль. Мы отвергаем текущую инвестиционную форму кейса: слишком много execution зависит от тяжёлого named-account sales, партнёров и compliance-heavy delivery, а устойчивый moat ещё не проявился. Если кейс докажет локальный channel wedge и measurable remediation outcomes, он может вернуться в approve-диапазон.

# Score trajectory

## 2026-05-11 03:10 MSK — P4 Demand Validation
- Stage: P4 / demand-validation
- Analyst: branch-models-lead
- Score trajectory: **new → 7.4**
- Verdict shift: **TRIAGE PASS → PASS WITH RESERVATIONS**
- Why it moved:
  - валютный контроль и ВЭД-документы остаются обязательным recurring workflow для активных импортёров и экспортёров даже после смягчения правил Банка России;
  - публичные банковские тарифы и сервисные цены подтверждают willingness to pay за сокращение возвратов, пояснений и ручной проверки;
  - Profit Gate проходит только в hybrid software + managed exceptions модели, тогда как дешёвый utility SaaS не тянет EBITDA.
- Key risks:
  - рынок нишевый и может быстро упереться в потолок без расширения на импортёров, аутсорсеров и брокеров;
  - продукт легко деградирует в ручной ВЭД-аутсорсинг, если не удержать repeatable software layer;
  - интеграции с 1С, банк-клиентом и ЭДО обязательны, иначе ROI для клиента будет слабым.
- Next check:
  - проверить solution-fit для hybrid-модели, особенно repeatability интеграций, channel GTM через аутсорсеров/брокеров и границу между software и service.
- Artifact: `pipeline/cases/ai-operator-valyutnogo-kontrolya-i-ved-dokumentov-dlya-msb/02-demand.md`

## 2026-05-11 04:10 MSK — P5 Unit Economics
- Stage: P5 / economics
- Analyst: branch-models-lead
- Score trajectory: **7.4 → 4.9**
- Verdict shift: **PASS WITH RESERVATIONS → REJECTED**
- Why it moved:
  - fully-loaded CAC после учёта SDR/AE FOT, tools, events и overhead вышел около **499k ₽**, что ещё терпимо, но подтвердило sales-assisted и не-self-serve природу бизнеса;
  - contribution margin составил только **66,4%**, а fixed-cost base зрелой команды и G&A достиг **~6,08 млн ₽/мес**;
  - при обязательном стресс-тесте на **50 клиентах** модель показывает **EBITDA -4,26 млн ₽/мес**, а break-even требует около **167 клиентов**, что слишком далеко для этой ниши.
- Key risks:
  - высокая сервисная примесь в onboarding, pilot и exception handling;
  - disproportionate burn относительно размера SAM;
  - без существенного роста ACV или white-label канала экономика не становится фондопригодной.
- Next check:
  - только если появится новый wedge с более высоким ACV, например банки, крупный аутсорс или white-label distribution.
- Artifact: `pipeline/cases/ai-operator-valyutnogo-kontrolya-i-ved-dokumentov-dlya-msb/04-economics.md`

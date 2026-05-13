# Score trajectory

## 2026-05-13 — P4 Demand Validation
- Stage: P4 Demand Validation
- Score before: n/a
- Score after: 7/10
- Change: +7
- Summary: broad-demand по AI video ads в РФ пока medium-low, но wedge "видео для маркетплейсов" уже показывает живую прикладную потребность; WTP подтверждён глобальными аналогами и RU Telegram substitutes; Profit Gate проходит в self-serve, agency и hybrid сценариях.
- Evidence:
  - video ad market РФ в Q1 2026 = 67.8 млрд ₽, +53% г/г [T1]
  - demand endpoint по "видео для маркетплейсов" = MEDIUM, score 30 [T2/internal]
  - Western pricing anchors = $29-149/мес; RU low-end substitutes = 129-750 ₽+ [T2]
  - SAM preferred = 4.48 млрд ₽, SOM Y1 preferred = 89.6 млн ₽ [T1/T2 + inference]
- Decision: proceed to next stage

## 2026-05-13 — P5 Unit Economics
- Stage: P5 Unit Economics
- Score before: 7/10
- Score after: 4/10
- Change: -3
- Summary: спрос подтверждён, но fund-level экономика не проходит: fully-loaded CAC оказался заметно выше intake-оценки, LTV/CAC = 2.79x ниже порога 3:1, а при 50 клиентах EBITDA не может приблизиться к 500К ₽/мес из-за тяжёлого FOT и fixed burn.
- Evidence:
  - blended fully-loaded CAC = 43 485 ₽; paid CAC = 40 625 ₽; outbound CAC = 75 000 ₽ [model + HH/amoCRM/Unisender/Yandex docs]
  - ARPU = 7 000 ₽, GM = 72.9%, monthly churn benchmark = 4.2%, LTV = 121 500 ₽ [Topview pricing analog + Optifai churn benchmark]
  - fixed cost base after MVP ramp = 4.84 млн ₽/мес; break-even = ~950 активных клиентов [model]
  - at 50 clients revenue = 350 000 ₽/мес, gross profit = 255 000 ₽/мес, EBITDA remains deeply negative [model]
- Decision: rejected and moved to pipeline/rejected

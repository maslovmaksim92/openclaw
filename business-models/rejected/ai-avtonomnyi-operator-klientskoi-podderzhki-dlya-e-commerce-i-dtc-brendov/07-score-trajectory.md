## 2026-05-11 — P4 Demand Validation
- Stage: P4 Demand Validation
- Score before: n/a
- Score after: 6.5/10
- Direction: up from intake hypothesis, but capped by low explicit search demand
- Summary:
  - `multi-demand` по ключу кейса вернул LOW / 0, поэтому массовый inbound-спрос в РФ не подтвержден.
  - Платежеспособный рынок подтвержден через Jivo, Usedesk, Gorgias, Tidio, Telegram-слой и вакансии поддержки на HH.
  - TAM/SAM/SOM в РФ сходятся на SAM около 1.08 млрд ₽ для top/mid e-commerce.
  - Profit Gate проходит в base/premium/hybrid сценариях, не проходит только в pilot-heavy low-price сценарии.
- Decision: PROCEED to next stage as service-led B2B niche, not broad SaaS.

## 2026-05-11 — P5 Unit Economics
- Stage: P5 Unit Economics
- Score before: 6.5/10
- Score after: 7.4/10
- Direction: up, because CAC/LTV math is strong even with conservative service-heavy assumptions
- Summary:
  - Базовая модель на 220 000 ₽ MRR на клиента и fully-loaded CAC 549 250 ₽ дает LTV 6.64 млн ₽ и LTV/CAC 12.1x.
  - CAC Payback = 2.5 месяца, что сильно лучше порога 12 месяцев для mid-market B2B.
  - Contribution margin в fully-loaded variable view остается 42.7%, то есть это не pure SaaS, но экономика все еще масштабируемая.
  - Break-even достигается примерно на 51 клиентах и около M13; при 50 клиентах operating EBITDA уже выше 500 тыс. ₽/мес.
  - Главный риск не в юнитах, а в execution: integration-heavy onboarding, SLA и сервисная нагрузка могут съесть маржу.
- Decision: PASS. Кейc можно двигать дальше без reject, но только как disciplined service-led B2B model, а не как self-serve SaaS.

## 2026-05-12 — P6 Finance Risk Validation
- Stage: P6 Finance Risk Validation
- Score before: 7.4/10
- Score after: 7.0/10
- Direction: down slightly, because median economics remain strong but left-tail risk is material
- Summary:
  - p50 по модели проходит EBITDA gate, но p10 EBITDA @M24 остается отрицательным, значит у кейса есть реальный downside-рисk по runway.
  - Главные уязвимости, price compression, churn и integration-heavy delivery, а не сам базовый CAC.
  - Конкурентный wedge есть, но он не product-led, а service-led: локальный compliance, Telegram-first каналы, быстрый запуск post-purchase сценариев.
  - Итог не reject, а PASS WITH HEAVY RISK DISCOUNT, поэтому следующий reviewer должен особенно жестко проверить moat, repeatability и go-to-market realism.
- Decision: PROCEED to critic/verdict with risk discount, not as clean PASS.

## 2026-05-12 — P7 Critic and Verdict
- Stage: P7 Critic and Verdict
- Score before: 7.0/10
- Score after: 6.5/10
- Direction: down, because weak moat, LOW exact-demand и отрицательный p10 EBITDA@M24 перевешивают сильную client-level economics
- Summary:
  - Итоговый rubric-score = 65/100: сильные unit economics и достижимый EBITDA gate на operating view не компенсируют слабую защитимость.
  - Source tier balance = 2.18, к Market + Demand применён штраф -2 за преобладание T2-источников при слабом direct-demand сигнале.
  - Moat score = 8/25, это weak moat: category crowded, switching costs умеренные, уникального датасета и регуляторного преимущества пока нет.
  - Для перехода в APPROVED кейсу нужны 2-3 платных design partners, onboarding <14 дней и подтверждённый path к 500К ₽ EBITDA без price dumping.
- Decision: NEAR-PASS. Переместить в rejected как case needing proof, не как hard reject по продукту.

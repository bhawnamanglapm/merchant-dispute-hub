# Merchant Payment Operations & Dispute Hub

*⭐⭐⭐⭐⭐ Built · self-directed simulation, not client work · full Product Owner lifecycle: discovery → PRD → design → governance → business case → launch → SQL*

> Exported from the portfolio page on 2026-10-19. The live page is the canonical version: https://bhawnamanglapm.github.io/travel-tech-more.html#case-merchant-dispute-hub

- 17 real artifacts across 7 stages, discovery to post-launch
- 47-item backlog across 9 epics (252 MVP points); 24 requirements traced to 62 test cases + 9 compliance controls
- 3-scenario business case: base NPV $149k, conservative ($839k), optimistic $1.34M
- Simulation project — fictional merchants, figures and teams; not an actual client system

**Tools used:** Excel (live-formula workbooks), Word, PowerPoint, HTML (wireframes + interactive SQL lab), SQLite. Built with AI assistance for drafting, the same way I'd use it on real client work.

### The Problem (Simulated)

Merchants handle card disputes by email and spreadsheets: deadlines tracked by hand, evidence emailed to dispute operations and re-keyed, nobody able to see where a dispute actually stands. In the simulated baseline: 78% of merchant responses arrive on time, and 9% of closed disputes are lost only because the deadline passed. Dispute operations spends 42 minutes handling each dispute, with 100% of evidence arriving by email — including card numbers sitting in attachments, a PCI DSS exposure. Finance and Operations calculate win rate differently: 40% vs. 62.5% on the same disputes.

### The Solution

One portal where merchants see every dispute and its deadline, get reminders, upload evidence with card numbers auto-redacted, and understand how disputes affect their payouts. Behind it: processor integration, a prioritized ops work queue, and one agreed set of dispute numbers. Beyond the MVP, the roadmap differentiates through prevention and explainable AI — pre-dispute alerts, dispute-ratio health, an AI evidence copilot with human review, friendly-fraud evidence automation, and readiness for purchases made by AI shopping agents.

### How I Approached It — 7 Stages

| Stage | What I did |
|---|---|
| **1. Discover** | Benchmarked American Express, Adyen, Stripe and Razorpay; logged findings, gaps and decisions with sources and status. |
| **2. Define** | Wrote the PRD; built a 47-item backlog across 9 epics (252 MVP points); traced 24 requirements to 62 test cases and 9 compliance controls; defined 21 KPIs with outcome definitions. |
| **3. Design** | Created 13 annotated wireframes: 8 MVP screens and 5 concept screens, with rules, edge states and open questions. |
| **4. Plan & govern** | Outcome-based roadmap (30 initiatives), RAID log, change control with impact assessments, stakeholder map, RACI and governance calendar. |
| **5. Justify & launch** | Three-scenario business case, pilot-led go-to-market with KPI gates, launch readiness, hypercare, benefits tracking and BAU transition. |
| **6. Communicate** | 17-slide executive review ending in five explicit decisions. |
| **7. Measure** | SQL practice database with KPI, reconciliation and data-quality queries, including deliberately planted data problems. |

### Decisions Worth Discussing

- **Resolving a stakeholder conflict without escalating or giving in.** The Fraud Operations Lead wanted full fraud case management in the MVP. I proposed a read-only fraud case reference in the MVP with a Phase 2 commitment (CR-01, Option C).
- **Fixing a metric before reporting it.** Finance and Ops disagreed on win rate. The proposed definition reports Won, Partially won and Lost separately, with value recovery as the North Star (CR-05).
- **Tracing one risk end to end.** Stale deadlines (R-03) → webhook assumption (A-02) → sandbox issue (I-01) → blocked story (US-019) → mapping defect (DEF-03) → failing requirement (BR-06) → latency KPI (KPI-12) → incident playbook (PB-02).
- **Showing a business case that can lose money.** Base case NPV is $149k with a 2.3-year payback, but the conservative case is ($839k). That points leadership at the two assumptions that matter: merchant adoption and whether released ops capacity is cashable.
- **Exiting hypercare on evidence, not a date.** Twelve exit criteria, including 10 business days without a Sev 1 or Sev 2 incident.
- **Differentiating in a crowded market.** Online dispute portals are standard, including at American Express, so the roadmap competes on prevention and explainable AI rather than the portal itself.

### Business Case (Base Scenario, Illustrative)

| Measure | Value |
|---|---|
| One-time investment | $612k |
| 3-year NPV | $149k (conservative ($839k), optimistic $1.34M) |
| 3-year ROI | 26% |
| Payback after go-live | 2.3 years |
| Share of benefit from released ops capacity | ~85% |
| Merchant value at Year 3 (excluded from NPV) | ~$771k a year |

### Known Gaps & Next Steps

- The Post-Launch Plan's iteration roadmap doesn't yet include the six beyond-MVP initiatives (RM-25 to RM-30) added to the Product Roadmap.
- Concept screens S09–S13 are directional; each needs discovery, compliance review and a business case before it's real.
- Next artifacts: API specification with a Postman collection, analytics tracking plan, and a BI dashboard mockup.

Overview[full README →](https://bhawnamanglapm.github.io/projects/merchant-dispute-hub/README.md) PRD[PDF →](https://bhawnamanglapm.github.io/projects/merchant-dispute-hub/02-product-definition/PRD_Merchant_Dispute_Hub.pdf) Backlog[xlsx →](https://bhawnamanglapm.github.io/projects/merchant-dispute-hub/02-product-definition/Product_Backlog_Merchant_Dispute_Hub.xlsx) RTM[xlsx →](https://bhawnamanglapm.github.io/projects/merchant-dispute-hub/02-product-definition/RTM_Merchant_Dispute_Hub.xlsx) KPIs[xlsx →](https://bhawnamanglapm.github.io/projects/merchant-dispute-hub/02-product-definition/KPI_Definitions_Merchant_Dispute_Hub.xlsx) Wireframes[13 annotated screens →](https://bhawnamanglapm.github.io/projects/merchant-dispute-hub/03-design/Dispute_Hub_Wireframes.html) Roadmap[xlsx →](https://bhawnamanglapm.github.io/projects/merchant-dispute-hub/04-planning-and-governance/Product_Roadmap_Merchant_Dispute_Hub.xlsx) RAID[xlsx →](https://bhawnamanglapm.github.io/projects/merchant-dispute-hub/04-planning-and-governance/RAID_Log_Merchant_Dispute_Hub.xlsx) Business Case[xlsx →](https://bhawnamanglapm.github.io/projects/merchant-dispute-hub/05-business-case-and-launch/Business_Case_GTM_Merchant_Dispute_Hub.xlsx) Post-Launch[xlsx →](https://bhawnamanglapm.github.io/projects/merchant-dispute-hub/05-business-case-and-launch/Post_Launch_Plan_Merchant_Dispute_Hub.xlsx) Exec Review[17-slide PDF →](https://bhawnamanglapm.github.io/projects/merchant-dispute-hub/06-executive-communication/Dispute_Hub_Executive_Review_v2.pdf) SQL Lab[interactive, self-checking →](https://bhawnamanglapm.github.io/projects/merchant-dispute-hub/07-data-and-sql/Dispute_Hub_SQL_Lab.html) SQL Guide[54 lessons, 24 exercises →](https://bhawnamanglapm.github.io/projects/merchant-dispute-hub/07-data-and-sql/Dispute_Hub_SQL_Practice_Guide.md)

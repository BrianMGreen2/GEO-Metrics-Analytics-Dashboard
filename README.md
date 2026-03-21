# GEO Reporting System

A white-label reporting product for agencies building **Generative Engine Optimization (GEO)** client dashboards, ROI models, and prioritized action plans. Includes an executive performance dashboard, a live interactive ROI calculator, a full 8-pillar metric framework, and a recommendation engine that maps diagnostic findings to client-ready next steps.

---

## Live Demo

| Page | URL |
|---|---|
| AI Performance Dashboard | `/geo-dashboard-demo.html` |
| GEO ROI Calculator | `/geo-roi-calculator.html` |

The dashboard demo includes two clients (Acme Health and Northstar SaaS) with real seed data across four tabs:

| Tab | What it shows |
|---|---|
| **Dashboard** | KPI row, visibility gap alert, diagnostic cards, trust signals, opportunity sidebar |
| **8-Pillar Detail** | All eight pillars grouped by GEO layer with current scores and prior-week deltas |
| **Prompt Runs** | Raw prompt-by-prompt data — model, inclusion status, score, competitors, sources |
| **Action Plan** | Prioritized recommendations mapped to the three GEO layers, with ROI impact summary |

---

## Where ROI Comes From

GEO impact is structured across three compounding layers. Each layer must be stable before the next delivers its full value.

| GEO Layer | What We Improve | Business Impact |
|---|---|---|
| **Entity Hardening** | Identity clarity | Prevents misclassification — brand defense |
| **Positioning Accuracy** | Category alignment | Appears in the correct AI decision set |
| **Selection Confidence** | Signal density | Becomes the primary AI recommendation |

> "GEO ROI comes from increasing how often you are **selected** at the moment of decision — not just how often you are seen."

---

## The Eight Metric Pillars

Each pillar maps to scored columns in `prompt_runs` and rolls up into `client_metric_snapshots` for dashboard reporting. Pillars are grouped by GEO layer.

### Entity Hardening

| Pillar | What it measures | Key submetrics |
|---|---|---|
| **Identity Clarity** | Whether the AI resolves the client as a distinct, unambiguous entity | `disambiguation_score`, `entity_drift_score` |
| **Signal Cohesion** | Consistency of signals across the sources the AI reads | `signal_cohesion_score`, `cross_channel_consistency_score` |

### Positioning Accuracy

| Pillar | What it measures | Key submetrics |
|---|---|---|
| **Category Accuracy** | Whether the AI places the client in the right category | `misclassification_score`, `service_positioning_score` |
| **Visibility & Inclusion** | How often the client appears in relevant AI responses | `visibility_gap_score`, `retrieval_failure`, `comparative_absence` |
| **Source Dependence** | Whether the AI's knowledge is spread across enough sources | `source_dependence_score`, `platform_resilience_score` |

### Selection Confidence

| Pillar | What it measures | Key submetrics |
|---|---|---|
| **Authority & Trust** | How confidently the AI recommends the client | `authority_gap_score`, `selection_confidence_score` |
| **Representation Quality** | How accurately and completely the client is described | `compression_failure_score`, `hedging_score` |
| **Competitive Positioning** | How the client ranks against named competitors | `competitive_positioning_score` |

---

## Action Plan & Recommendation Engine

The Action Plan tab generates a prioritized roadmap from diagnostic findings. Each recommendation is scored across four dimensions to determine its priority band and sequencing.

### Prioritization logic

| Dimension | What it weighs |
|---|---|
| **Layer dependency** | Layer 1 issues always surface first — they block all downstream improvements |
| **ROI lever** | Fixes that lift inclusion rate rank highest, followed by CTR, then close rate |
| **Effort** | Quick wins surface before structural engagements of equal impact |
| **Severity** | Critical and high-severity findings from `metric_observations` score up |

### Priority bands

| Band | Timeframe | What it contains |
|---|---|---|
| **Immediate** | Now | Blocking issues — entity resolution, signal fragmentation, comparative absence |
| **Short-term** | 30–90 days | High-ROI content and authority fixes once the foundation is stable |
| **Strategic** | 90+ days | Structural work — source diversification, differentiation evidence, selection justification |

### Service areas

Each recommendation is tagged to one of three service areas, which maps to who does the work:

| Service Area | What we do | Typical owner |
|---|---|---|
| **Measurement** | Diagnose where the model breaks — error rates, compression failure, hedging, retrieval failure, disambiguation issues | 3WM |
| **Content Strategy** | Fix where content fails the model — unresolved attributes, buried facts, missing decision inputs, lack of comparative framing | Client / 3WM |
| **AI Enablement** | Fix where the business itself is unusable by the model — entity not resolved, no comparative structure, weak external validation, source dependence | 3WM |

### Issues mapped to pillars

**Entity Hardening** — Identity Clarity + Signal Cohesion
- Disambiguation, entity drift, inconsistent statements, unresolved attributes, entity not resolved, ambiguity under compression, signal fragmentation, lack of repeat signals, weak external validation

**Positioning Accuracy** — Category Accuracy + Visibility & Inclusion + Source Dependence
- Category misclassification, over-generalization, missing decision inputs, context gaps, error rate, retrieval failure, comparative absence, buried facts, no comparative framing, no comparative structure, source dependence

**Selection Confidence** — Authority & Trust + Representation Quality + Competitive Positioning
- Authority gap, confidence threshold, no selection justification, compression failure, hedging, buried facts (also Visibility), comparative absence (also Visibility), no comparative framing (also Visibility)

---

## ROI Calculator

The calculator models how improvements across the three GEO layers translate to revenue. Metric multipliers connect directly to the recommendation priority bands — Immediate fixes lift inclusion rate, Short-term fixes lift CTR, Strategic fixes lift close rate.

| Multiplier | GEO Layer | Rate it lifts |
|---|---|---|
| Visibility Gap fix | Positioning Accuracy | ↑ inclusion rate |
| Clarity / Compression fix | Selection Confidence | ↑ CTR |
| Misclassification fix | Positioning Accuracy | ↑ inclusion + CTR |
| Authority Gap fix | Selection Confidence | ↑ inclusion + close rate |
| Comparative Absence fix | Positioning Accuracy | ↑ inclusion |

Multipliers can be set manually via sliders, or auto-populated from live pillar scores. Scenario view (Conservative / Expected / Aggressive) shows all three outcomes simultaneously with ROI bands of 2–5x, 5–15x, and 15–30x.

---

## Stack

- **Next.js 14** (App Router)
- **TypeScript** (strict mode)
- **Tailwind CSS**
- **Supabase** (`@supabase/supabase-js`) — Postgres + RLS
- **Lucide React** icons
- **Vercel** — deployment target

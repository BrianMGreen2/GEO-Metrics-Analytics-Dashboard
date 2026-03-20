# GEO Reporting System

A white-label reporting product for agencies building **Generative Engine Optimization (GEO)** client dashboards and ROI models. Includes an executive performance dashboard, a live interactive ROI calculator, and a full 8-pillar metric framework.

---

## Live Demo

| Page | URL |
|---|---|
| AI Performance Dashboard | `/geo-dashboard-demo.html` |
| GEO ROI Calculator | `/geo-roi-calculator.html` |

The dashboard demo includes two clients (Acme Health and Northstar SaaS) with real seed data, a full 8-pillar detail view, prompt run history, and metric observations. The ROI calculator includes a base model, three scenario presets, and metric improvement multipliers tied to GEO pillar scores.

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

## ROI Calculator

The calculator models how improvements across the three GEO layers translate to revenue.

| Multiplier | GEO Layer | Rate it lifts |
|---|---|---|
| Visibility Gap fix | Positioning Accuracy | ↑ inclusion rate |
| Clarity / Compression fix | Selection Confidence | ↑ CTR |
| Misclassification fix | Positioning Accuracy | ↑ inclusion + CTR |
| Authority Gap fix | Selection Confidence | ↑ inclusion + close rate |
| Comparative Absence fix | Positioning Accuracy | ↑ inclusion |

Multipliers can be set manually via sliders, or auto-populated from live pillar scores. Scenario view (Conservative / Expected / Aggressive) shows all three outcomes simultaneously with ROI bands of 2–5x, 5–15x, and 15–30x.

---

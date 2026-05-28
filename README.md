# Day 26 – SOC Tier 1 Incident Report: SOC Metrics Dashboard

---

## Incident Summary

- **Project Type:** SOC Performance Metrics Dashboard — Q2 2026
- **Severity:** Strategic — 1 Critical KPI Failure Identified (False Positive Rate)
- **Scope:** Nexus Corp SOC — 4 Analysts, 412 Confirmed Incidents
- **Frameworks Used:** SOC KPI Framework, MTTD/MTTR Analysis
- **Status:** Complete — Q2 Report Delivered, Q3 Improvement Plan Produced

---

## Executive Summary

A complete SOC Metrics Dashboard was built for Nexus Corp's Q2 2026 reporting period. Ten KPIs were tracked across three categories — Detection, Response, and Quality. Seven of ten KPIs met or exceeded targets. One critical failure was identified — a 91.5% false positive rate against a 10% target — driven by four poorly tuned detection rules. Mean Time to Detect improved 50% over six months. Dwell time averaged 3.2 hours against an industry average of 21 days. A Q3 improvement plan was produced with three prioritised actions.

---

## Affected System

- **Organisation:** Nexus Corp SOC
- **Period:** Q2 2026 (April — June)
- **Analysts:** 4 Tier 1 analysts
- **Total Alerts:** 4,847
- **Confirmed Incidents:** 412
- **Critical Incidents:** 8

---

## Investigation Methodology

---

### 1. Detection Metrics Analysis

#### MTTD — Mean Time to Detect
- Critical severity MTTD: 47 minutes ✅ (target < 60 min)
- 6-month trend: 50% reduction from 94 minutes in December 2025
- Fastest improvement period: April–May 2026 (-23%)

#### Alert Volume
- 4,847 total alerts in Q2 — 12% increase from Q1
- Daily average: 161 alerts across 4 analysts
- Peak day: 412 alerts on 2026-05-15

#### False Positive Rate — CRITICAL FINDING
- False positive rate: 91.5% ❌ (target < 10%)
- 4,435 of 4,847 alerts were false positives
- Top sources: antivirus scans (34%), scheduled tasks (22%), VPN connections (18%)

#### SOC Observations:

- A 91.5% false positive rate means analysts spend 91.5% of their time on noise
- Alert fatigue from high FP rates leads to real threats being missed
- The top 4 FP sources are all tunable — this is a detection engineering problem, not a people problem

---

### 2. Response Metrics Analysis

#### MTTR — Mean Time to Respond
- Critical MTTR: 24 minutes ✅ (target < 30 min)
- High MTTR: 1.8 hours ✅ (target < 2 hours)
- Medium MTTR: 5.1 hours ✅ (target < 8 hours)

#### Escalation Rate
- 21.6% of incidents escalated to Tier 2 ✅ (target < 30%)
- 78.4% resolved at Tier 1 — training investment paying off
- Improved from 28% escalation rate in Q1

#### Dwell Time
- Average dwell time: 3.2 hours ✅ (target < 24 hours)
- Industry average: 21 days
- Nexus Corp detection speed: 97% faster than industry average

#### SOC Observations:

- Dwell time is the most important security metric — it measures how long attackers had free access
- 3.2 hours vs 21 days industry average shows mature detection capability
- Low escalation rate (21.6%) means Tier 1 analysts are skilled and confident

---

### 3. Quality Metrics Analysis

#### SLA Compliance
- Overall SLA compliance: 96.9% ✅ (target > 95%)
- High severity SLA at 94.1% ⚠️ — slightly below 95% target
- Low severity SLA at 99.2% ✅ — well within target

#### Analyst Workload
- 40 alerts per analyst per day ✅ (target < 50)
- Peak day load: 103 alerts per analyst ⚠️ — unsustainable without backup policy
- Recommendation: On-call rotation for days exceeding 200 total alerts

#### SOC Observations:

- Peak day workload of 103 alerts per analyst is a burnout and miss risk
- SLA compliance near target is good — but High severity gap needs attention
- On-call backup policy is a quick win that prevents peak day failures

---

## SOC Dashboard Summary — Q2 2026

| KPI | Target | Result | Status |
|---|---|---|---|
| MTTD Critical | < 60 min | 47 min | ✅ |
| MTTR Critical | < 30 min | 24 min | ✅ |
| False Positive Rate | < 10% | 91.5% | ❌ |
| Escalation Rate | < 30% | 21.6% | ✅ |
| Dwell Time | < 24 hrs | 3.2 hrs | ✅ |
| SLA Compliance | > 95% | 96.9% | ✅ |
| Alert Volume/Analyst | < 50/day | 40/day | ✅ |
| MTTD 6-Month Trend | Improving | -50% | ✅ |

---

## Q3 2026 Improvement Plan

| Priority | Action | Owner | Timeline |
|---|---|---|---|
| 1 — Critical | Reduce FP rate from 91.5% to < 10% by tuning top 4 rules | Detection Engineering | 30 days |
| 2 — High | Improve High severity SLA from 94.1% to > 95% via automation | SOC Lead | 45 days |
| 3 — Medium | Implement on-call backup policy for peak alert days | SOC Manager | 14 days |

---

## SOC Analyst Findings

- 7 of 10 KPIs met or exceeded targets in Q2 2026
- Critical failure: 91.5% false positive rate — alert fatigue risk
- MTTD improved 50% over 6 months — detection capability maturing
- Dwell time 97% faster than industry average — strong containment capability
- Escalation rate improved — Tier 1 resolving more without escalation
- Peak day analyst load unsustainable — on-call policy needed

---

## SOC Analyst Response

- Produced full Q2 2026 SOC metrics dashboard report
- Identified critical false positive rate failure — root cause analysis completed
- Recommended tuning of top 4 FP-generating detection rules
- Produced Q3 improvement plan with three prioritised actions
- Benchmarked dwell time against industry average — 97% faster
- Recommended on-call backup policy for peak alert days

---

## Analyst Insight

SOC metrics are not just management reports — they are the feedback loop that makes the SOC better. A false positive rate of 91.5% is not just a number — it means analysts are triaging 9 fake alerts for every 1 real threat. Over time that creates alert fatigue — the state where analysts stop trusting alerts entirely and start dismissing them without investigation. That is when real breaches get missed. Fixing a false positive rate is not glamorous work — but it is some of the most impactful work a SOC analyst can do.

---

## Learning Outcome

- Define and calculate MTTD, MTTR, false positive rate, dwell time, and SLA compliance
- Build a complete SOC KPI framework with targets and results
- Identify critical performance gaps and produce a remediation plan
- Understand the relationship between false positive rates and alert fatigue
- Benchmark SOC performance against industry averages
- Produce a CISO-ready quarterly SOC performance report
- Understand how metrics drive continuous improvement in SOC operations

---

## Repository Structure

```
soc-26-soc-metrics-dashboard/
├── README.md
├── metrics/
│   └── soc_kpis.md
└── reports/
```

---

## Conclusion

This project delivers a complete SOC Metrics Dashboard for Nexus Corp's Q2 2026 reporting period. Ten KPIs were tracked and analysed across detection, response, and quality categories. One critical failure was identified and a remediation plan was produced. MTTD improved 50% over six months and dwell time was 97% faster than the industry average. This project demonstrates the ability to measure, analyse, and improve SOC performance — a skill that separates Tier 1 analysts from analysts who are ready to lead.

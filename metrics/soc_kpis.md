# SOC Key Performance Indicators (KPIs)
## Nexus Corp Security Operations Center
## Analyst: James | Period: Q2 2026

---

## Why SOC Metrics Matter

Metrics turn SOC operations from reactive firefighting
into a measurable, improvable discipline.

Without metrics you cannot answer:
- Are we getting faster at detecting threats?
- Are our detection rules accurate or generating noise?
- Do we have enough analysts for the alert volume?
- Is our security posture improving over time?

---

## Category 1 — Detection Metrics

### KPI 1: Mean Time to Detect (MTTD)

```
Definition: Average time from when an attack begins
            to when the SOC first detects it

Formula: Sum of (Detection Time - Attack Start Time)
         divided by Number of Incidents

Target: < 1 hour for High/Critical severity
        < 4 hours for Medium severity
        < 24 hours for Low severity

Q2 2026 Result:
Critical: 47 minutes ✅ (target < 60 min)
High:     2.1 hours  ✅ (target < 4 hours)
Medium:   6.3 hours  ⚠️ (target < 24 hours)
Low:      18.2 hours ✅ (target < 24 hours)

Trend: Improved 23% from Q1 2026
```

---

### KPI 2: Mean Time to Respond (MTTR)

```
Definition: Average time from alert detection to
            incident containment

Formula: Sum of (Containment Time - Detection Time)
         divided by Number of Incidents

Target: < 30 minutes for Critical severity
        < 2 hours for High severity
        < 8 hours for Medium severity

Q2 2026 Result:
Critical: 24 minutes ✅ (target < 30 min)
High:     1.8 hours  ✅ (target < 2 hours)
Medium:   5.1 hours  ✅ (target < 8 hours)

Trend: Improved 15% from Q1 2026
```

---

### KPI 3: Alert Volume

```
Definition: Total number of alerts generated per day/week/month

Q2 2026 Monthly Average:
Total alerts per month:     4,847
Critical alerts:            23
High alerts:                187
Medium alerts:              1,204
Low alerts:                 3,433

Daily average:              161 alerts
Peak day:                   412 alerts (2026-05-15)
Lowest day:                 89 alerts (2026-04-06)

Trend: 12% increase from Q1 — correlates with new detection rules
```

---

### KPI 4: False Positive Rate

```
Definition: Percentage of alerts that turn out to be
            not real threats

Formula: (False Positive Alerts / Total Alerts) x 100

Target: < 10% false positive rate

Q2 2026 Result:
Total alerts:             4,847
True positives:           412 (8.5%)
False positives:          4,435 (91.5%)

False positive rate: 91.5% ❌ ABOVE TARGET

Top false positive sources:
1. Antivirus scan triggers — 34% of FPs
2. Scheduled task alerts — 22% of FPs
3. VPN connection alerts — 18% of FPs
4. Software update triggers — 14% of FPs
5. Other — 12% of FPs

Action: Tune top 4 rules to reduce FPs by 40%
```

---

## Category 2 — Response Metrics

### KPI 5: Incidents by Severity

```
Q2 2026 Incident Count:

Critical:  8  incidents
High:      47 incidents
Medium:    203 incidents
Low:       154 incidents
Total:     412 confirmed incidents

Most common incident types:
1. Phishing attempts:        187 (45%)
2. Brute force attacks:      98 (24%)
3. Malware detections:       67 (16%)
4. Insider threat alerts:    34 (8%)
5. Data exfiltration:        26 (6%)
```

---

### KPI 6: Escalation Rate

```
Definition: Percentage of Tier 1 alerts escalated to Tier 2

Formula: (Escalated Alerts / Total Confirmed Incidents) x 100

Target: < 30% escalation rate (Tier 1 handles most)

Q2 2026 Result:
Total confirmed incidents: 412
Escalated to Tier 2:       89 (21.6%) ✅
Resolved at Tier 1:        323 (78.4%)

Trend: Improved from 28% in Q1 — Tier 1 training effective
```

---

### KPI 7: Dwell Time

```
Definition: Time an attacker spends in the environment
            before detection and containment

Target: < 24 hours average dwell time

Q2 2026 Result:
Average dwell time: 3.2 hours ✅
Longest dwell time: 11.4 hours (insider threat case)
Shortest dwell time: 4 minutes (automated response)

Industry average dwell time: 21 days
Nexus Corp vs industry:      97% faster detection ✅
```

---

## Category 3 — Quality Metrics

### KPI 8: SLA Compliance Rate

```
Definition: Percentage of alerts responded to within
            defined SLA timeframes

Target: > 95% SLA compliance

Q2 2026 Result:
Critical SLA (< 15 min):  96.4% ✅
High SLA (< 1 hour):      94.1% ⚠️ (target 95%)
Medium SLA (< 4 hours):   97.8% ✅
Low SLA (< 24 hours):     99.2% ✅

Overall SLA compliance: 96.9% ✅
```

---

### KPI 9: MTTD Trend (6 Month View)

```
Month          MTTD (Critical)    Trend
Dec 2025       94 minutes         Baseline
Jan 2026       88 minutes         ↓ -6%
Feb 2026       79 minutes         ↓ -10%
Mar 2026       71 minutes         ↓ -10%
Apr 2026       61 minutes         ↓ -14%
May 2026       47 minutes         ↓ -23%

6-month improvement: 50% reduction in MTTD ✅
```

---

### KPI 10: Analyst Workload

```
Definition: Average number of alerts handled per analyst per day

Q2 2026 Result:
Total analysts (Tier 1): 4
Daily alert volume:      161 alerts
Alerts per analyst:      40 alerts/day

Target: < 50 alerts per analyst per day
Result: 40 alerts/day ✅ Within healthy range

Peak day load:      412 alerts ÷ 4 analysts = 103 each ⚠️
Recommendation:     On-call backup policy for peak days
```

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

## Q3 2026 Improvement Targets

```
Priority 1 — CRITICAL:
Reduce false positive rate from 91.5% to < 10%
Action: Tune top 4 FP-generating rules
Owner: Detection Engineering + SOC Lead
Timeline: 30 days

Priority 2 — HIGH:
Improve High severity SLA from 94.1% to > 95%
Action: Add automated triage for common High alerts
Owner: SOC Lead + Automation Engineer
Timeline: 45 days

Priority 3 — MEDIUM:
Implement on-call policy for peak alert days
Action: Define escalation triggers and backup rotation
Owner: SOC Manager
Timeline: 14 days
```

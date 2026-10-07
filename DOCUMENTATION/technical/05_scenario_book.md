# Scenario book

The Heat to Come · Application 2.5.0 · Model V2-2.3.0 · G2 dossier 2026-09-26

Audience: facilitators and technical reviewers. Language: English. Intended destination: public technical supplement, separate from the player manual. Editable master: Markdown; delivery copies: DOCX and PDF.

Source keys refer to the private V2 source root: M = `data/model/v2_3_model.json`; E = `data/events/v2_events.json`; T = `data/content/v2_3_en-GB.json`; D = `app/src/domain/engine-v2-3.mjs`. They are source identifiers, not public hyperlinks. Tables below are extracted from the current canonical data, never transcribed from the V1 workbook.

## Four different decision problems

These are fictional campus settings for examining decisions under heat risk. They are not observations or forecasts for named universities. Scenario identity and the conceptual dilemmas come from the approved original scenario document; current numbers follow the retained Alpha-5 model. All begin with acceptability and continuity 100. Budgets are relative units. Readiness scales nominal risk and resilience increments, including negative resilience; it is not a probability.

| Scenario | Risk | Resilience | Budget | Releases 1 / 2 / 3 | Risk floor | Risk k |
| --- | --- | --- | --- | --- | --- | --- |
| PC | 85 | 55 | 100 | 44 / 33 / 23 | 10 | 22 |
| FF | 90 | 30 | 70 | 32 / 23 / 15 | 15 | 27 |
| CZ | 35 | 75 | 100 | 40 / 35 / 25 | 5 | 8 |
| SR | 40 | 35 | 70 | 33 / 22 / 15 | 8 | 11 |

## The Pressure Cooker

Stable identifiers: SCN-V2-001; PC; pressure_cooker. Fictional setting: Maris Central Campus.

Maris Central enters the season with high current risk, established but incomplete resilience and a total budget of 100 released across three turns. Cooling demand, procurement delays and service continuity are already visible concerns. The campus community expects credible action, yet repeated restrictions and hurried delivery may create further strain.

Reduce immediate exposure while building capacity that can keep working as conditions and public expectations change.

Learning tension: Urgency versus durability: act at speed without confusing the most visible response with the whole strategy.

| Parameter | Value |
| --- | --- |
| Initial risk | 85 |
| Initial resilience | 55 |
| Total budget | 100 |
| Releases | 44 / 33 / 23 |
| Risk floor | 10 |
| Risk k | 22 |

### Category readiness

| Category | Multiplier |
| --- | --- |
| Infrastructure | 1.05 |
| Operations | 1.54 |
| Preparedness | 1.47 |
| Governance | 1 |
| Behavioural | 0.95 |
| Restrictive | 0.95 |

### Score priorities

| Component weight | Points |
| --- | --- |
| risk | 40 |
| resilience | 30 |
| coherence | 15 |
| acceptability | 10 |
| efficiency | 5 |

The coherence weight applies to the mean of coherence and continuity. These weights sum to 100; they do not add a starting-resilience bonus.

### Mission prompts and debrief references

**MIS-V2-PC-01: Protect essential services under compound heat.** Keep essential teaching, cooling and support functions viable as heat and delivery pressure overlap.

In the debrief, trace which decisions protected continuity and which merely displaced pressure to another service or turn. Reference: continuity score component at least 70.

**MIS-V2-PC-02: Build capacity that outlasts emergency mode.** Use the three turns to create capabilities that remain useful after the first visible response.

In the debrief, identify evidence of sustained resilience, sustained delivery or coordination rather than one-off relief. Reference: resilience score component at least 65.

**MIS-V2-PC-03: Retain legitimacy while acting at speed.** Respond decisively without allowing urgency, restrictions or funding conditions to disconnect the strategy from campus users.

In the debrief, examine where acceptability strengthened delivery and where haste created avoidable resistance. Reference: acceptability score component at least 70.

Mission references are evaluated against final score components (`ExperienceApp.tsx`, missionResults), not directly against final raw metrics. In particular, the resilience component combines normalised cumulative and final improvement. Mission labels do not replace the overall 70/85 score bands.

### Event deck

| Event ID | Title | Deck | Weight |
| --- | --- | --- | --- |
| EVT-V2-PC-01 | Early severe heatwave | intermediate | 1 |
| EVT-V2-PC-02 | Cooling-system stress | intermediate | 1 |
| EVT-V2-PC-03 | Procurement delay | intermediate | 1 |
| EVT-V2-PC-04 | Public demand for visible action | intermediate | 1 |
| EVT-V2-PC-05 | Resistance to repeated restrictions | intermediate | 1 |
| EVT-V2-PC-06 | Emergency coordination opportunity | intermediate | 1 |
| EVT-V2-PC-07 | Supplementary adaptation funding | intermediate | 1 |
| EVT-V2-PC-08 | Interdepartmental mobilisation | intermediate | 1 |
| EVT-V2-PC-09 | Compound heat and service-continuity stress | final | 1 |
| EVT-V2-PC-10 | Grid-pressure emergency | final | 1 |
| EVT-V2-PC-11 | Supply-chain disruption | final | 1 |
| EVT-V2-PC-12 | Heat-health escalation | final | 1 |

Exact effects, choices and mitigation tags appear in the event appendix. Sources: M scenarios.PC; M parameters.residualRisk.k.PC; T scenarios[runtimeId=pressure_cooker]; E events[scenarioId=PC].

## The Fragile Frontline

Stable identifiers: SCN-V2-002; FF; fragile_frontline. Fictional setting: Bahía Edge Campus.

Bahía Edge begins with the highest risk, low resilience and a total budget of 70 released across three turns. Staff capacity is stretched, basic equipment is vulnerable and some people face greater barriers to safe spaces and services. A disruption that looks modest elsewhere can cascade quickly here.

Protect essential functions and people now while creating enough adaptable capacity to recover from setbacks.

Learning tension: Immediate necessity versus future recovery: make scarce resources work across services, people and time.

| Parameter | Value |
| --- | --- |
| Initial risk | 90 |
| Initial resilience | 30 |
| Total budget | 70 |
| Releases | 32 / 23 / 15 |
| Risk floor | 15 |
| Risk k | 27 |

### Category readiness

| Category | Multiplier |
| --- | --- |
| Infrastructure | 0.85 |
| Operations | 1.76 |
| Preparedness | 1.84 |
| Governance | 1.05 |
| Behavioural | 1.76 |
| Restrictive | 1 |

### Score priorities

| Component weight | Points |
| --- | --- |
| risk | 30 |
| resilience | 35 |
| coherence | 20 |
| acceptability | 10 |
| efficiency | 5 |

The coherence weight applies to the mean of coherence and continuity. These weights sum to 100; they do not add a starting-resilience bonus.

### Mission prompts and debrief references

**MIS-V2-FF-01: Protect people and essential functions first.** Direct scarce capacity towards immediate safety and the services whose failure would cascade across the campus.

In the debrief, compare the protection achieved with the pressures that remained concentrated among vulnerable groups. Reference: continuity score component at least 65.

**MIS-V2-FF-02: Preserve room to recover from shocks.** Avoid commitments that leave no budget, staff capacity or repair route when disruption arrives.

In the debrief, identify the turning point at which flexibility was preserved or spent. Reference: efficiency score component at least 50.

**MIS-V2-FF-03: Turn local support into durable capacity.** Connect partnerships and mutual aid to safe roles, coordination and follow-through rather than relying on goodwill alone.

In the debrief, review which community capacities remained usable after the immediate event. Reference: resilience score component at least 60.

Mission references are evaluated against final score components (`ExperienceApp.tsx`, missionResults), not directly against final raw metrics. In particular, the resilience component combines normalised cumulative and final improvement. Mission labels do not replace the overall 70/85 score bands.

### Event deck

| Event ID | Title | Deck | Weight |
| --- | --- | --- | --- |
| EVT-V2-FF-01 | Staff absence surge | intermediate | 1 |
| EVT-V2-FF-02 | Vulnerable-group health incident | intermediate | 1 |
| EVT-V2-FF-03 | Basic service failure | intermediate | 1 |
| EVT-V2-FF-04 | Supplier price shock | intermediate | 1 |
| EVT-V2-FF-05 | Community mutual-aid | intermediate | 1 |
| EVT-V2-FF-06 | Health-service partnership | intermediate | 1 |
| EVT-V2-FF-07 | Targeted small grant | intermediate | 1 |
| EVT-V2-FF-08 | Emergency volunteer mobilisation | intermediate | 1 |
| EVT-V2-FF-09 | Severe heatwave under scarcity | final | 1 |
| EVT-V2-FF-10 | Equipment outage | final | 1 |
| EVT-V2-FF-11 | Water disruption | final | 1 |
| EVT-V2-FF-12 | Compound staffing stress | final | 1 |

Exact effects, choices and mitigation tags appear in the event appendix. Sources: M scenarios.FF; M parameters.residualRisk.k.FF; T scenarios[runtimeId=fragile_frontline]; E events[scenarioId=FF].

## The Comfort Zone

Stable identifiers: SCN-V2-003; CZ; comfort_zone. Fictional setting: North Sound Campus.

North Sound has low current risk, high resilience and a total budget of 100. The case for disruptive action is contested, even as longer-range signals point to changing conditions. The campus can prepare deliberately, but poorly proportioned investment may reduce trust, lock in costs or crowd out flexible learning.

Build readiness proportionate to the evidence while preserving legitimacy, learning and room to adapt.

Learning tension: Preparedness versus proportionality: use available capacity without treating expenditure itself as proof of progress.

| Parameter | Value |
| --- | --- |
| Initial risk | 35 |
| Initial resilience | 75 |
| Total budget | 100 |
| Releases | 40 / 35 / 25 |
| Risk floor | 5 |
| Risk k | 8 |

### Category readiness

| Category | Multiplier |
| --- | --- |
| Infrastructure | 0.95 |
| Operations | 0.95 |
| Preparedness | 1.595 |
| Governance | 1.6675 |
| Behavioural | 1 |
| Restrictive | 0.85 |

### Score priorities

| Component weight | Points |
| --- | --- |
| risk | 15 |
| resilience | 25 |
| coherence | 25 |
| acceptability | 15 |
| efficiency | 20 |

The coherence weight applies to the mean of coherence and continuity. These weights sum to 100; they do not add a starting-resilience bonus.

### Mission prompts and debrief references

**MIS-V2-CZ-01: Prepare in proportion to the evidence.** Use available resources without treating spending or disruption as proof of readiness.

In the debrief, distinguish commitments that generated useful capacity from those that created cost or lock-in. Reference: efficiency score component at least 55.

**MIS-V2-CZ-02: Preserve trust during low urgency.** Make the case for action legible and reversible enough to retain participation while risk remains contested.

In the debrief, examine how acceptability changed as evidence, inconvenience and commitment accumulated. Reference: acceptability score component at least 75.

**MIS-V2-CZ-03: Turn learning into staged readiness.** Use monitoring, pilots and review points to improve future choices without postponing all practical preparation.

In the debrief, identify where new evidence changed the trajectory and whether the campus kept useful options open. Reference: coherence score component at least 60.

Mission references are evaluated against final score components (`ExperienceApp.tsx`, missionResults), not directly against final raw metrics. In particular, the resilience component combines normalised cumulative and final improvement. Mission labels do not replace the overall 70/85 score bands.

### Event deck

| Event ID | Title | Deck | Weight |
| --- | --- | --- | --- |
| EVT-V2-CZ-01 | Spending scrutiny | intermediate | 1 |
| EVT-V2-CZ-02 | Resistance to disruption | intermediate | 1 |
| EVT-V2-CZ-03 | Mild season complacency | intermediate | 1 |
| EVT-V2-CZ-04 | Long-range risk forecast | intermediate | 1 |
| EVT-V2-CZ-05 | Favourable procurement window | intermediate | 1 |
| EVT-V2-CZ-06 | Monitoring partnership | intermediate | 1 |
| EVT-V2-CZ-07 | Insurance incentive | intermediate | 1 |
| EVT-V2-CZ-08 | Reversible pilot window | intermediate | 1 |
| EVT-V2-CZ-09 | Preparedness stress test | final | 1 |
| EVT-V2-CZ-10 | Budget-audit challenge | final | 1 |
| EVT-V2-CZ-11 | Heat anomaly | final | 1 |
| EVT-V2-CZ-12 | Compound confidence shock | final | 1 |

Exact effects, choices and mitigation tags appear in the event appendix. Sources: M scenarios.CZ; M parameters.residualRisk.k.CZ; T scenarios[runtimeId=comfort_zone]; E events[scenarioId=CZ].

## The Silent Risk

Stable identifiers: SCN-V2-004; SR; silent_risk. Fictional setting: Estuary Learning Campus.

Estuary Learning Campus starts with low visible risk, low resilience and a total budget of 70. Heat-related strain is unevenly detected, indoor conditions are poorly observed and decision-makers receive weak signals. Waiting for a dramatic incident could leave little time to build basic response capacity.

Make latent exposure legible and strengthen practical readiness without overbuilding ahead of the evidence.

Learning tension: Recognition versus premature certainty: act on weak signals while continuing to learn who and what is exposed.

| Parameter | Value |
| --- | --- |
| Initial risk | 40 |
| Initial resilience | 35 |
| Total budget | 70 |
| Releases | 33 / 22 / 15 |
| Risk floor | 8 |
| Risk k | 11 |

### Category readiness

| Category | Multiplier |
| --- | --- |
| Infrastructure | 0.85 |
| Operations | 1.7 |
| Preparedness | 1.955 |
| Governance | 1.87 |
| Behavioural | 1.785 |
| Restrictive | 0.95 |

### Score priorities

| Component weight | Points |
| --- | --- |
| risk | 15 |
| resilience | 40 |
| coherence | 25 |
| acceptability | 10 |
| efficiency | 10 |

The coherence weight applies to the mean of coherence and continuity. These weights sum to 100; they do not add a starting-resilience bonus.

### Mission prompts and debrief references

**MIS-V2-SR-01: Make hidden exposure visible.** Improve the chain from observation and reporting to an accountable operational response.

In the debrief, trace which signals became actionable and which people or spaces remained difficult to see. Reference: coherence score component at least 60.

**MIS-V2-SR-02: Build readiness before a visible crisis.** Create practical response capacity while preserving scarce resources for what later evidence may reveal.

In the debrief, identify whether early action reduced latent vulnerability or remained mainly symbolic. Reference: resilience score component at least 55.

**MIS-V2-SR-03: Strengthen confidence in weak signals.** Support people to report heat strain and show how uncertain evidence informs proportionate decisions.

In the debrief, review whether trust and governance improved together or whether reporting raised expectations without follow-through. Reference: acceptability score component at least 70.

Mission references are evaluated against final score components (`ExperienceApp.tsx`, missionResults), not directly against final raw metrics. In particular, the resilience component combines normalised cumulative and final improvement. Mission labels do not replace the overall 70/85 score bands.

### Event deck

| Event ID | Title | Deck | Weight |
| --- | --- | --- | --- |
| EVT-V2-SR-01 | Hidden indoor exposure | intermediate | 1 |
| EVT-V2-SR-02 | Delayed case detection | intermediate | 1 |
| EVT-V2-SR-03 | Weak warning signal | intermediate | 1 |
| EVT-V2-SR-04 | Decision-maker complacency | intermediate | 1 |
| EVT-V2-SR-05 | Reporting network | intermediate | 1 |
| EVT-V2-SR-06 | Public-health data partnership | intermediate | 1 |
| EVT-V2-SR-07 | Low-cost monitoring | intermediate | 1 |
| EVT-V2-SR-08 | Community awareness trigger | intermediate | 1 |
| EVT-V2-SR-09 | Latent-vulnerability stress | final | 1 |
| EVT-V2-SR-10 | Sensor failure | final | 1 |
| EVT-V2-SR-11 | Late heat alert | final | 1 |
| EVT-V2-SR-12 | Compound hidden-risk event | final | 1 |

Exact effects, choices and mitigation tags appear in the event appendix. Sources: M scenarios.SR; M parameters.residualRisk.k.SR; T scenarios[runtimeId=silent_risk]; E events[scenarioId=SR].

## Historical boundary and evidence

The original V1 PC/CZ budget of 120 is historical; the current value is 100. Baseline risks remain PC 85, FF 90, CZ 35 and SR 40; historical proposed moves to 30/38 were not adopted. Earlier V2 release schedules and residual-risk k values are not current. The present schedules/readiness/k values are the frozen acceptance candidate E in specification 08. The conceptual contrast remains urgency and delivery in PC, scarcity and recovery in FF, proportionality in CZ, and latent vulnerability in SR. No fixed optimal package is provided. G1 run02 verified the earlier mechanics; the corrected rules require G1 run03; historical statistical evidence is not a human learning or success-probability study.


## Coordination correction and exact rule identity

Owner decision DEC-G2-20260926-001 authorises canonical interaction lookup by the sorted intervention IDs. The earlier implementation missed 107 of 272 authored pair keys because their stored order differed from the lookup order. Both positive connectivity and conflict diagnostics now use all applicable authored records; pair payoff coefficients, model values and event data are unchanged. Multi-operation effectiveness and downstream results can change. This is not a V1 numerical model.

Current rule revision: `engine-v2.3.0-active-score-rebalance-coordination-v2`. Compatibility fingerprint: `rules-v2.3.0-coordination-pair-normalisation-2026-09-26.1`. Application version 2.5.0 and model version V2-2.3.0 alone do not identify these rules. The separate G1 run03 handoff records qualification results and the exact tested files for the corrected implementation. Earlier saves with the old rule fingerprint are rejected. No automatic migration or inherited statistical acceptance is claimed.

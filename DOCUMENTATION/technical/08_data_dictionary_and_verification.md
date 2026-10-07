# Data dictionary and verification guide

The Heat to Come · Application 2.5.0 · Model V2-2.3.0 · G2 dossier 2026-09-26

Audience: facilitators, analysts and technical reviewers. Language: English. Intended destination: public technical appendix. Editable master: Markdown, with PDF/DOCX delivery copies. Technical data extract: `technical-data-extract.json`, a parameter companion, not an importable player save or a replacement engine.

## File roles and versions

The extract has schema `g2-technical-extract-v1`, application version 2.5.0 and model version V2-2.3.0. It contains the current parameters, four scenarios, 36 interventions with 108 level rows, 272 interactions, six concentration rules and 48 events. The extract preserves English event modelling rationales. Italian internal pair/concentration notes are omitted; numeric records are unchanged. It is an audit extract created for this dossier, not a canonical runtime source. Editing it does not change the game.

Canonical sources remain `data/model/v2_3_model.json`, `data/events/v2_events.json` and `data/content/v2_3_en-GB.json`, all relative to the private V2 source root. The engine is `app/src/domain/engine-v2-3.mjs`. Event schema 2.2.0 and engine schema 2.3.0 coexist intentionally in application 2.5.0. The released application's compatibility contract requires the corresponding complete fingerprint set; matching a version string alone is insufficient.

## Model fields

| Field / selector | Type and units | Meaning |
| --- | --- | --- |
| scenarios.PC / FF / CZ / SR | Object | Four stable short scenario keys |
| scenarios.*.runtimeId | String | Stable application slug |
| riskBase / resilienceBase | Index points | Initial synthetic metrics |
| budget | Relative resource units | Nominal three-turn programme budget |
| releases | Three numbers | Exact scheduled releases; sum equals budget |
| floor | Risk index points | Scenario minimum used by risk updates |
| readiness.* | Multiplier | Category conversion of nominal risk and resilience |
| weights.* | Percentage-point weights | Five weights summing to 100 |
| interventions[].runtimeId | String | Stable INF/OPS/PRE/GOV/BEH/RES identifier |
| interventions[].id | String | Stable INT-V2 record identifier |
| levels[].level | Integer 0, 1, 2 | Not selected; limited/pilot; comprehensive |
| levels[].cost | Relative resource units | Nominal capital cost at the level |
| levels[].risk | Reduction-strength points | Input to risk asymptote, not direct risk subtraction |
| levels[].resilience | Signed contribution | Nominal positive or adverse resilience effect |
| levels[].acceptability | Index points | Input to robust package acceptability |
| lifecycle.class | Classification string | permanent / persistent / temporary; no expiry timer |
| lifecycle.activation.l1 / l2 | Turns | Activation delay from the operation |
| lifecycle.maturityCurve | Three coefficients per path | Physical benefit delivery over operation year and two following years |
| lifecycle.tags | String array | Capability tags used by events and coordination |
| lifecycle.repairCost | Relative resource units | Contextual repair price, not annual upkeep |
| falseFriend | Boolean | Authored maladaptation flag; excluded from capability contribution |
| deliveryClass | String | immediate / programme / infrastructure |
| interactions[].id1 / id2 | Stable IDs | Unordered authored pair |
| r_interaction / s_interaction | Signed points | Raw pair payoff before level intensity and caps |
| categoryMix[].ruleId | String | Stable concentration rule identity |
| dominantThreshold | Share 0–1 | Strict greater-than trigger |
| complementMinShare | Share 0–1 | Strict less-than combined-complement trigger |
| r_mix / s_mix | Signed points | Triggered concentration effect |

## Event fields

| Field | Meaning |
| --- | --- |
| id / scenarioId / deck | Stable event, scenario short ID, intermediate or final deck |
| weight | Relative draw weight within the eligible deck |
| immediateEffects | Raw signed risk, resilience, continuity, acceptability and budget vector |
| nextTurnEffects | Delayed signed vector; final-event delay is informational |
| mitigationRules[].tags | Any matching tag can activate this mitigation rule |
| riskReduction / resilienceProtection / continuityReduction | Raw mitigation magnitudes before capability scaling |
| amplificationRules[].missingTags | Amplification requires all listed tags to be absent |
| compatibilityTags | Tags for event protection and following-turn response coherence |
| exclusionTags | Retained metadata; current draw applies scenario/deck/non-repetition filtering |
| choices[] | Required revealed choice branches where present |
| choices[].titleKey / bodyKey | Keys resolved by the British-English content catalogue |
| durationTurns | Authored metadata; actual continuation is the explicit next-turn vector |
| sourceOrAssumption / auditRationale | Modelling provenance, not evidence of observed climate impacts |

## Run, snapshot and score fields

| Field | Interpretation |
| --- | --- |
| phase | planning, event-reveal, event-choice, event or complete |
| turn | 1, 2 or 3; each is an academic year |
| seed / prngState / prngVersion | Recorded deterministic draw identity and state |
| metrics | Current risk, resilience, continuity and acceptability |
| active | Lifecycle records keyed by intervention ID; includes activating/damaged items |
| effectiveLevel / targetLevel | Current physical level and pending target |
| maturitySegments | Incremental start/upgrade segments and their saved delivery factors |
| pendingActivation | Delayed segment not yet physically active |
| damage / postRepairState | Event damage and the state restored by repair |
| budget.available | Opening planning resource authority |
| budget.carryOut | Remaining resource after commitment/event; displayed outside planning |
| budget.pendingDelta / eventDelta | Delayed opening change / current event resource change |
| coordination.netLoad / capacity / excessLoad | Turn-local delivery pressure and allowance |
| coordination.effectiveness | Positive operation increment coefficient |
| effects.activeCapacity.tagCapacity | Pre-event capability map, also used for response coherence |
| event.protection | Bound protection fixed for the source event |
| metricsBeforeEvent / metricsAfterEvent | Isolate immediate event resolution |
| event.eventOnlyMetricDeltas | Realised event-only changes after metric bounds |
| event.metricDeltas | Whole-turn difference from pre-commitment metrics; not event-only |
| history | Three post-event snapshots used by final scoring |
| pendingEffects | Delayed vectors scheduled for later application |
| continuingEffects | Informational effects outside the scored horizon |
| components.resilience | Mean of normalised cumulative and final resilience improvement |
| components.cumulativeRisk | Normalised mean-risk improvement relative to initial risk and floor |
| evaluationAdjustments | Diagnostics, not additional deductions applied after the composite |

## Verification and workbook boundary

Check parameter equality before interpreting any numerical example: all four release sums, all level tuples, six concentration rows and 272 pairs should match the canonical extract. Check that authored event counts are eight intermediate plus four final per scenario and that the eight opportunity events each expose their explicit choices. Empty operations remain a legal deliberate decision when the budget is not negative; they do not bypass event resolution.

For a formula workbook, disclose exactly which equations are implemented, their inputs, rounding and limits. A parameter table and isolated risk, coordination or scoring example do not reproduce lifecycle transitions, maturity-segment history, capacity aggregation, event draws, all choices, damage or compatibility validation. Formula cells must be recalculated and independently compared with expected values. Do not import the formula reference workbook as a player result archive: the game rejects formula-bearing result imports.

G2 author examples use deterministic synthetic decisions and current engine output. They demonstrate selected arithmetic and causal records, not strategy optimality, statistical balance, complete workbook parity or learning effectiveness. The author’s source checks and examples require independent review before a G2 PASS. The final handoff records actual completed numerical and visual checks and any limitations; no check is implied merely because a document is readable.

## Source lineage and supersession

The approved original DOCX framework, scenarios, intervention catalogue, payoff manual and XLSX supplied the initial identities and payoff structure. Their originals remain unchanged. V1 app calibration, V2.2 count-based overload and lifecycle rules, and earlier release-specific documents retain historical status. Current overrides are coordination-load-v2, Alpha-4 lifecycle simplification and Alpha-5 active-score-rebalance-v1, subsequently frozen in model V2-2.3.0. The earlier G1 run02 software qualification for 2.5.0 carries an accepted loss of 226 historical files; it is not an assertion of complete historical archive integrity.

The exact editable model is private maintenance material. The public technical tables and extract support inspection without exposing the entire development history. File disposition and final hashes are controlled by the dossier inventory and G2 handoff.

## Coordination correction and exact rule identity

Owner decision DEC-G2-20260926-001 authorises canonical interaction lookup by the sorted intervention IDs. The earlier implementation missed 107 of 272 authored pair keys because their stored order differed from the lookup order. Both positive connectivity and conflict diagnostics now use all applicable authored records; pair payoff coefficients, model values and event data are unchanged. Multi-operation effectiveness and downstream results can change. This is not a V1 numerical model.

Current rule revision: `engine-v2.3.0-active-score-rebalance-coordination-v2`. Compatibility fingerprint: `rules-v2.3.0-coordination-pair-normalisation-2026-09-26.1`. Application version 2.5.0 and model version V2-2.3.0 alone do not identify these rules. The separate G1 run03 handoff records qualification results and the exact tested files for the corrected implementation. Earlier saves with the old rule fingerprint are rejected. No automatic migration or inherited statistical acceptance is claimed.

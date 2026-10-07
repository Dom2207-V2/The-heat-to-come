# Model framework

The Heat to Come · Application 2.5.0 · Model V2-2.3.0 · G2 dossier 2026-09-26

Audience: facilitators, reviewers and technically interested readers. Language: English. Intended destination: public technical documentation, separate from the player manual. Editable master: this Markdown; DOCX and PDF are generated delivery copies. This document explains a synthetic educational model, not a campus heat forecast or an engineering design tool.

## Authority and scope

The current numerical authority is `data/model/v2_3_model.json` (M), with events in `data/events/v2_events.json` (E). The implementation qualified by G1 is `app/src/domain/engine-v2-3.mjs` (D), together with `app/src/domain/coordination-load.mjs` (C). Paths in this document are relative to the private V2 source root; they identify reproducible source locations, not public download links. The private source map provides hashes. The embedded model fingerprint is `c45e7380c25783561be138d702c3be6b9d875b5fcc28927a90750c00ef5ab9f6`. The value-only digest is `b6f8bab7c225098ecce24004f9097961ae397fbe0dd40fcd77a98b7f85daeded`; these identify different projections and must not be interchanged.

Owner-approved lifecycle simplification and the frozen Alpha-5 structural rebalance are retained through the V2-2.3.0 model. Their authorities are `spec/v2_3/03_lifecycle_simplification.md` and `spec/v2_3/08_active_score_rebalance_v2_3.md`. Application 2.5.0 includes a separately identified coordination-rule correction; the model version is not 2.5.0. G1 run02 qualifies the earlier software under the accepted historical-loss exception. The current coordination correction requires G1 run03 requalification. It does not restore the 226 missing historical files or certify their original package bindings.

The approved original framework, scenarios, intervention catalogue and payoff workbook remain source-history documents. Their one-shot formulas, 120-unit high budgets, count-based overload, renewals and expiry must not be applied to the present game. The 05 scenario book and 06 intervention catalogue provide current source-extracted values. The shadow mission-attainment methods are research companions, not the score displayed in the game.

## State, units and interpretation

There are three decision turns, each representing one academic year centred on the hot season. Risk, resilience, continuity and acceptability are dimensionless synthetic indices. Risk is lower-is-better and can reach 140; its effective minimum is the scenario floor. Resilience, continuity and acceptability are clamped to 0–100. Budget uses relative resource units, not currency. All scenarios begin with continuity and acceptability 100. Resilience already present at the start is not credited as player-created improvement.

For each turn, the run stores opening metrics, available budget, operations, coordination trace, lifecycle records, pre-event metrics, the event and choice, realised event effects and post-event metrics. The random seed and PRNG state are persisted. The transition functions copy and freeze state; replay checks the causal trace. Normal numerical state operations round to three decimals. Coordination and capability traces use six decimals at their defined steps. The final score is rounded to an integer only after the weighted composite is formed.

Source: M `turnHorizon`, `metricDescriptors`, `scenarios`; D lines 19–20, 50–69, `createRun`, `validateRunState`.

## Resolution order

1. Opening planning releases the next scenario-specific budget and adds carryover. It applies queued delayed effects, matures pending activations, delivers further maturity increments, adjusts package acceptability and applies recurring active effects, in that order.
2. Commitment validates phase, intervention/action/level, one operation per intervention, realisable benefit before the end, and both individual and combined affordability. It computes coordination capacity from the pre-operation portfolio and evaluates the selected operation set.
3. Starts, upgrades and repairs are committed. The engine computes saturation for the resulting eligible active portfolio and records the operation's incremental maturity segment. It adjusts package acceptability, restores the recurring contribution of repaired items, calculates interactions and concentration, and derives current capability tags.
4. The engine draws and persists an event. Before applying its metric effects, it applies the selected operations' risk reduction and risk penalties, then resilience effects and concentration. The event reveal therefore has an immutable pre-event snapshot. Navigating or reloading does not redraw the event.
5. A revealed choice, when present, must be selected in the interface. Event effects and choice effects are applied with metric clamps. Damage is selected deterministically; budget effects adjust carryout. Delayed effects are queued and the turn snapshot is persisted.
6. Advancing opens the next turn or finalises turn 3. Queued effects marked `include` enter final metrics; `informational` effects are retained as continuing effects outside the scored horizon. Final-event delayed effects are informational. No fourth decision turn is created.

The API helper `resolveTurn` supplies the first event choice when none is passed. This convenience is for programmatic replay/test callers; the interface's persisted event-choice phase requires a choice. Sources: D `openPlanning` line 489; `prepareTurn` line 858; `resolvePendingEvent`, `resolveTurn`, `advanceTurn` line 1042.

## Budget and legal operations

For turn t, opening available budget = release[t] + carryIn + pendingDelta. After commitment and the event, carryOut = available − spent + eventDelta. Release totals are PC 44/33/23, FF 32/23/15, CZ 40/35/25 and SR 33/22/15. Event costs or benefits are additional to those scheduled totals; they can reduce carryout below zero, which constrains the following opening budget. Unspent resources carry forward rather than resetting.

Start L1 or L2 pays the listed level cost. Upgrade pays C(L2) − C(L1) and requires an active L1. Repair pays explicit `lifecycle.repairCost` (or an event override if supplied) and requires an eligible damaged item. Repair is not a recurring maintenance charge. One intervention cannot receive two operations in the same turn. A start or upgrade without a positive risk or resilience payoff that can mature within the remaining horizon is unavailable. The engine has no hard three-operation limit and no fixed three-operation effectiveness threshold.

Sources: M `scenarios.*.releases`, `interventions[].levels`, `interventions[].lifecycle`; D `releaseBudget`, `getAvailableOperations` line 560, `assertOperations`.

## Coordination load

Let K be the number of categories represented by the selected operations. Action load is 0.40 per start, 0.20 per upgrade and 0.10 per repair. Heterogeneity H(K), for K = 0…6, is [0, 0, 0, 1, 3, 6, 10]. Positive cross-category pairs are eligible only if at least one payoff interaction is positive and neither is negative. A deterministic spanning forest over categories selects at most K−1 links. Each contributes 0.50; the total credit is capped by H(K). Multiple positive links joining already connected categories do not accumulate further credit.

Gross = action load + H(K).

Net = max(0, gross − min(H(K), 0.50 × spanning links) + conflict load).

Conflict load is zero in this model: negative pairs remain visible diagnostics and already affect payoff. Capacity = 4 + built capacity. Excess = max(0, net − capacity). Effectiveness eta = 1 / (1 + 0.18 × excess^1.5).

Built capacity is capped at 1. Eligible pre-operation, undamaged Governance/Operations capability must carry coordination, planning, monitoring or continuity and have maturity at least 0.5. Each source contributes min(0.5, level/2 × maturity × 0.5). Same-turn starts cannot fund their own coordination capacity. A turn with no excess is within-capacity; a positive excess with eta ≥ 0.75 is stretched; below 0.75 it is high-pressure. Eta attenuates positive operation increments, including their later maturity delivery, but does not multiply final coherence, apply an operation-count acceptability penalty or attenuate negative increments.

Sources: M `parameters.coordinationLoad`, `parameters.activeScoreRebalance.dynamicCoordination`; D `builtCoordinationCapacity`; C `evaluateCoordinationLoad`.

## Direct effects, timing and saturation

An operation creates a segment from level a to level b. Let f be category readiness, m the relevant maturity coefficient, eta the operation effectiveness and w the saturation coefficient. Its positive risk reduction is max(0, Rb−Ra) × f × eta × m × wR. For resilience, let dS = (Sb−Sa) × f. A non-negative dS contributes dS × eta × m × wS; a negative dS contributes dS × m. Negative resilience is not softened by coordination pressure or saturation.

Saturation ranks eligible active interventions separately for risk and resilience within each category, by max(0, nominal target-level payoff) × readiness, with runtime ID breaking ties. Weights by rank are 1, 1, 0.75, 0.50, 0.25 and 0.10; the last applies to any further rank. It is not a catalogue-order penalty. An operation captures its saturation factors; later maturity increments use the captured factors. Recurring effects recompute the active portfolio's current saturation.

Physical payoff curves have three entries: the operation year, one year later and two years later. An infrastructure start has activation delay 1. L1 and upgrade curves are [0,1,1], while direct L2 is [0,0.5,1]. Programme curves are L1 [1,1,1], direct L2 [0.5,1,1] and upgrade [0,1,1]. Immediate delivery curves are [1,1,1]. The catalogue records each actual item rather than relying on this summary. Upgrade increments are L2−L1, so the old segment and new segment remain distinct.

At each opening, capable active interventions produce a recurring contribution equal to 0.16 of their realised physical payoff, with current maturity and saturation and eta = 1. Restoring a damaged item also restores its recurring contribution at commitment. The current lifecycle keeps started interventions throughout the run. There is no renewal, expiry, maintenance charge or automatic decay. The retained class name `temporary` describes inherited classification, not a current expiry timer. Damage remains until repair; its stored `durationTurns` metadata does not implement automatic recovery.

Sources: D `payoffDelta` line 134; `saturationByIntervention`; `activeEffects` line 261; `matureActivations`, `deliverMaturityIncrements`, `settleLifecycle`; M `interventions[].lifecycle.maturityCurve`.

## Risk, interactions and concentration

For each risk-reduction application, let r be the current risk, F the scenario floor, p a non-negative risk penalty, x a non-negative effective reduction and k the scenario coefficient. The update is:

rNew = clamp(F + (max(F, r+p) − F) × exp(−x/k), F, 140).

The current k values are PC 22, FF 27, CZ 8 and SR 11. Event risk changes are additive after this operation-stage asymptote, followed by the same bounds. This is a stateful sequence; applying one workbook calculation to the initial baseline does not reproduce a whole run.

For each active pair, q = effectiveLevel1 × effectiveLevel2 / 4. Positive interaction payoffs are multiplied by q; negative ones by max(0.5,q). Summed positive risk is capped at min(8, 0.15 × max(0, current operated + restored recurring risk)); summed positive resilience at min(10, 0.20 × max(0, current operated + restored recurring resilience)). Negative sums are not capped. Thus the limit is based on current operation/repair contributions, not every persistent effect. Negative risk interactions and negative concentration risk become p in the asymptote; resilience interactions and concentration effects enter resilience additively.

Concentration uses capable active portfolio capital costs at effective levels, not expenditure in the current turn. Each of six `categoryMix` rows triggers if its dominant share is strictly greater than its own threshold and the sum of its complement shares is strictly less than its own minimum. All current dominant thresholds are 0.35; complement minima are 0.30 except Preparedness 0.25. The generic parameter keys `concentrationDominantShare=0.5` and `complementMinimumShare=0.25` do not override these row-specific runtime rules. Multiple triggered row payoffs are summed. Structural coherence is −12 if any row triggers; otherwise it is min(20, 5 × number of capable active categories). Appendix tables reproduce the six exact rows and all 272 authored pair records.

Sources: D `applyRiskReduction`, `interactionEffects` line 345, `concentrationEffect` line 369; M `parameters.residualRisk`, `interactions`, `categoryMix`.

## Acceptability and capability

Package acceptability = 0.70 × cost-weighted mean of active effective-level acceptability + 0.30 × minimum active acceptability. No active items yields 100. Zero total cost would use the ordinary mean. When the package changes, current acceptability receives the difference between new and previous package acceptability, with bounds 0–100. Event changes are therefore retained rather than resetting acceptability to the package value every turn. Level 0 rows are excluded.

Capability is distinct from physical payoff. For every undamaged non-false-friend record, capability evaluates segment maturity with eta = 1, current saturation and scenario readiness. Positive realised risk plus positive realised resilience is divided by the largest nominal productive L2 payoff among interventions carrying that tag, then clamped to 0–1. Capability may use pending activation segments. Infrastructure has earlier capability curves: L1 [0.25,0.75,1], direct L2 [0.2,0.6,1], upgrade [0.4,0.85,1]. For other categories the item-specific capability curve, if present, or physical curve applies. Contributions to the same tag aggregate as a saturating union: capacityNew = 1 − (1−capacityOld) × (1−contribution). Damaged items and false friends contribute no capability under this configuration.

Sources: D `packageAcceptability` line 322, `applyPackageAcceptability`, `capabilityRecords` line 190; M `parameters.acceptability`, `parameters.activeScoreRebalance.capabilityMaturity`.

## Events, randomisation and damage

The catalogue has 48 events: eight intermediate and four final events for each scenario. The draw is weighted by each event's `weight`. Intermediate events are sampled without replacement; the final draw uses the final deck. The nominal 8 × 7 × 4 event-ID paths per scenario do not count opportunity-choice branches. The current draw filters on scenario, deck and previously used intermediate ID; empty exclusion metadata is not an additional runtime filter.

The PRNG is mulberry32-v1. Numeric seeds become unsigned 32-bit values; string seeds use the engine's character hash before random generation. The run records both seed and state. The same compatible engine, exact seed interpretation, operations and revealed choices reproduce the same results. Technical tests do not establish a real-world event probability.

Capability is fixed before the event is applied, after that turn's operations. Compatible tags provide protection = 0.40 × maximum compatible capacity, bounded by 0.40. Harmful metric effects are multiplied by (1−protection). Positive effects and budget effects are not scaled. Delayed harmful effects use the protection recorded for the source event, not a later retroactive recalculation. Immediate choice effects are added after base-event mitigation; delayed choice effects join delayed event effects before protected harmful-effect scaling.

Event-specific mitigation rules then add their signed deltas. A matching rule uses the maximum matching tag capacity; the first matching rule has full scale and every subsequent matching rule half scale. Amplification applies only when all its missing tags have no positive capacity. The engine retains raw effects, applied effects, mitigation/amplification records and the realised metric delta after clamps. Use `eventOnlyMetricDeltas` to discuss the event alone: legacy `metricDeltas` includes the whole committed turn.

Six event adapters can damage one eligible active permanent/persistent item: PC-02, PC-10, FF-03, FF-10, FF-11 and SR-10 (each prefixed EVT-V2-). They use the stated tags in the event appendix. Eligible items sort by descending effective level, then descending completed event resolutions, then ID. Damage suppresses subsequent capability until repaired, but does not retroactively reverse already delivered metrics. No random second damage draw is made.

Sources: E `events[]`; D `nextRandom`, `seedNumber`, `drawEvent`, `resolveEventEffects` line 786, `applyDamage` line 809, `queueNextEffects`, `FINALISATION_BY_EVENT`, `DAMAGE_RULES`.

## Final score

Let mean() refer to the three stored post-event snapshots, including eligible finalisation adjustments in the last snapshot. Every component below is in points, bounded where shown; clamp100 bounds a value to 0–100.

Risk performance = clamp100(100 × (riskBase − mean(risk)) / (riskBase − floor)).

Cumulative resilience gain = clamp100(100 × (mean(resilience) − resilienceBase) / (100 − resilienceBase)). Final resilience gain uses final resilience in place of its mean. Resilience component = (cumulative gain + final gain) / 2. Continuity and acceptability components are their three-snapshot means.

For each turn, structural quality = clamp100(100 × (concentration coherence + 12) / 32). Turn 1 uses this alone. For turns 2–3, response adequacy = clamp(max capacity of tags compatible with the previous revealed event / 0.5, 0, 1). Turn coherence = 0.70 × structural quality + 0.30 × response adequacy × 100. The final coherence component is the mean of the three turn values. A raw compatible capacity below 0.05 is reported as a missed response; this diagnostic is not an extra score deduction.

Productive performance = (risk performance + resilience component) / 2. Spend rate = clamp(totalSpent / nominal scenario budget, 0, 1). Flexibility = 100 × (1−spend rate). Efficiency is zero for zero total spending; otherwise 0.75 × clamp100(productive performance / max(spend rate,0.5)) + 0.25 × flexibility. The denominator remains the nominal scenario budget even when events change resources.

The weighted composite is [wRisk × risk performance + wResilience × resilience component + wCoherence × (coherence + continuity)/2 + wAcceptability × acceptability + wEfficiency × efficiency] / 100. The engine clamps this to 0–100 and rounds to the nearest integer. Scenario weights are in the scenario book and sum to 100. Bands are redesign below 50, developing 50–69 (shown in the interface as “Needs consolidation”), passed 70–84 and strong 85–100. The pass decision uses the rounded score ≥ 70.

Coordination exposure, false-friend operations, negative interactions and missed responses are reported separately. Their effects already enter the trajectory or coherence. They are not appended as another end-of-run deduction. In particular, the shadow model's Strong gate is not part of this active score.

Source: D `finalScore` line 1076; M `scenarios.*.weights`, `parameters.activeScoreRebalance.coherence`, `parameters.scorePassThreshold`.

## Assumptions, evidence and limits

The intervention values, category readiness, event severities, maturity curves and scoring weights are designed educational assumptions, informed by the project's source narrative and its documented model decisions. They are not estimates for a named campus, currency costs, temperature reductions, health forecasts or causal estimates from observed interventions. Effects collapse distributional differences into a few indices. Equity appears through selected event/capability narratives rather than a separate validated equity outcome. Three academic years compress commissioning, organisational learning and recovery.

The accepted historical Alpha-5 density analysis concerns uniform canonical legal leaves, including event paths and required choices. It is neither a human success probability nor a statement that random players will succeed at the reported rate. G1 current tests verify deterministic mechanics, causal traces and replay against the retained model. G1 run02 did not rerun the historical statistical acceptance bank. After the coordination correction, a new read-only acceptance run is required; its status is recorded in the G1 run03 handoff. Old density estimates are historical and do not certify the corrected rules. Some historical package bindings are unrecoverable under the owner's accepted-loss decision. Human learning gains, comprehension and accessibility-in-use have not been established by these automated checks.

The companion workbook is a transparent parameter and selected-formula verification aid. It does not replace the engine and must not claim full multi-turn, event, lifecycle or save parity without its own complete equivalence proof. Its own scope and recalculation report identify the tested subset.

## Reproduction map

Use the same-baseline model and events, the named engine functions, source hashes, and the G2 numerical appendices. Current source locations are exact private audit pointers. Public readers can inspect the delivered tables, examples and editable workbook without needing the private development repository. Independent review and final artifact checks are recorded in the G2 handoff, rather than implied by this author's draft.


## Coordination correction and exact rule identity

Owner decision DEC-G2-20260926-001 authorises canonical interaction lookup by the sorted intervention IDs. The earlier implementation missed 107 of 272 authored pair keys because their stored order differed from the lookup order. Both positive connectivity and conflict diagnostics now use all applicable authored records; pair payoff coefficients, model values and event data are unchanged. Multi-operation effectiveness and downstream results can change. This is not a V1 numerical model.

Current rule revision: `engine-v2.3.0-active-score-rebalance-coordination-v2`. Compatibility fingerprint: `rules-v2.3.0-coordination-pair-normalisation-2026-09-26.1`. Application version 2.5.0 and model version V2-2.3.0 alone do not identify these rules. The separate G1 run03 handoff records qualification results and the exact tested files for the corrected implementation. Earlier saves with the old rule fingerprint are rejected. No automatic migration or inherited statistical acceptance is claimed.

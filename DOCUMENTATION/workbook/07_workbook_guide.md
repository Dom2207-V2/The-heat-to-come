# Payoff workbook and selected verification guide

The Heat to Come · Application 2.5.0 · Model V2-2.3.0 · G2 dossier 2026-09-26

Audience: facilitators and technical reviewers. Language: English. Intended destination: public technical documentation, separate from the player manual. Editable formats: XLSX and this Markdown guide; DOCX/PDF are generated delivery copies of the guide. The workbook is a transparent teaching reference for a synthetic educational model, not a real-world heat forecast.

## What the workbook reproduces

`the-heat-to-come-payoff-v2.5.0.xlsx` reproduces the four scenario parameter sets, 24 readiness factors, five score weights per scenario, 108 level records across 36 interventions, 36 lifecycle summaries, 272 pair-payoff rows, six category-concentration rules and 48 immediate-event vectors. The Parameters sheet preserves the flattened current parameter values. Full event branches, delayed effects, mitigations, amplification, compatibility tags, intervention metadata and modelling provenance are available in the accompanying technical data extract, `../technical/technical-data-extract.json`. Internal Italian pair/mix notes are excluded from the public extract; their original authoritative records remain in the private source archive.

The formulas reproduce selected local arithmetic: staged budget with carryover and event changes; coordination action load, heterogeneity, credit, net load, capacity and effectiveness from supplied category/link inputs; a single risk-asymptote application; robust acceptability for a fixed three-item active package; pair intensity and positive-interaction caps; the six saturation coefficients; and concentration strict-boundary examples. These are independently inspectable equations, not a complete engine implementation.

The workbook does not simulate a whole game, draw events, validate legal operations, derive a spanning forest from intervention choices, create lifecycle/maturity segments, implement damage/repair transitions, aggregate capability tags, resolve event choices, perform final scoring or verify save compatibility. The Score weights sheet supplies data only. Saturation examples show the coefficient schedule and do not perform metric-specific portfolio ranking. The category-mix examples use Infrastructure's row; the complete six rules are reproduced as data. A single risk calculation cannot replace the engine's stateful sequence of risk applications.

## How to use it

Open the XLSX in Microsoft Excel with automatic calculation enabled. Scope is the opening sheet. Working calculations follow, with source tables to the right. Amber cells in Budget, Coordination and Risk identify editable teaching inputs. Preserve a copy before experimenting. A change to a source parameter is an experiment in that copy and does not change the application or qualify a new model.

Budget begins with zero spending and zero event/pending changes. Enter spending and signed event changes; carryout becomes the next turn's carry-in. Pending changes apply at the next opening. A negative event-adjusted carryout is possible. These are arithmetic examples; the workbook does not enforce the application's affordability or operation legality rules. Zero denotes no change. Do not erase required numeric inputs.

Coordination supplies four deterministic engine-derived operation fixtures. The forest-link counts and category counts are inputs, not a recalculated graph. Changing the number of starts without changing the category/link inputs is an isolated arithmetic sensitivity, not a newly validated portfolio. The built-capacity bonus should remain between 0 and 1 for model-like examples. Categories must be integers 0–6, links must describe the actual spanning forest, and action counts must be non-negative. A four-start single-category fixture retains eta 1: there is no fixed three-operation cap.

Risk contains zero, moderate and very large reduction examples for each scenario. Current risk, non-negative penalty and reduction can be changed; negative penalty/reduction values are treated as zero at this calculation stage, matching the engine. A missing numeric risk input is visibly reported as “Missing input”. The current scenario floor and positive k are linked to Scenarios. The output is clamped to the floor–140 interval and rounded to three decimals. The very large reduction demonstrates floating-point convergence to the floor, not a feasible game strategy.

Acceptability illustrates three active L1 records, INF01–INF03, with their canonical costs and acceptability values. These are arithmetic examples, not a recommended portfolio. The sheet computes a cost-weighted mean and package minimum, combines them with the canonical 0.70/0.30 shares and rounds to three decimals. The zero-total-cost branch uses the ordinary mean. An empty active package yields 100 in the engine; the fixed three-row worksheet does not implement deleting all active items. Level 0 is not an active item and its acceptability must not enter the package minimum.

Payoff checks distinguish positive pair intensity from the minimum negative-pair intensity. Positive risk is capped at min(8, 0.15 × current contribution) and resilience at min(10, 0.20 × current contribution). “Current contribution” means operated plus restored recurring contribution in the engine, not the sum of all persistent nominal payoffs. Concentration uses strict greater-than and less-than comparisons; equality to either threshold does not activate the example rule.

## Units, precision and interpretation

Budget and costs use relative resource units, not money. Risk, resilience and acceptability are synthetic index points. Readiness, saturation, maturity and eta are dimensionless multipliers. Releases are exact integers; the workbook uses actual scenario releases rather than the historical generic 40/35/25 shares. Lifecycle classes retain their legacy names, but current interventions do not expire, require renewal or incur automatic annual maintenance. Repair remains an explicit contextual action. Listed maturity curves are operation-year, one-year-later and two-years-later coefficients.

Risk, package acceptability and engine metric operations use three-decimal rounding. Coordination effectiveness uses six decimals. The workbook does not apply a general formatting round-trip to the source values. Exact source values remain typed numbers in XLSX. A displayed payoff is a nominal input: risk reduction enters the asymptote, and physical effects also depend on readiness, maturity, saturation and coordination.

## Cell-level source map

M denotes the private canonical `data/model/v2_3_model.json`; E denotes `data/events/v2_events.json`; D denotes `app/src/domain/engine-v2-3.mjs`; C denotes `app/src/domain/coordination-load.mjs`. These are source identifiers, not public download links. The final dossier inventory binds their exact hashes and qualified rules identity. The public companion extract carries the corresponding model fingerprint. Array positions are zero-based in JSON and source rows start at Excel row 2.

| Sheet and range | Source or function | Reproduction boundary |
| --- | --- | --- |
| Scenarios A2:J5 | M.scenarios; M.parameters.residualRisk.k | Four scenario IDs, baselines, nominal budgets, releases, floors and k |
| Readiness A2:C25 | M.scenarios.*.readiness | One scenario/category factor per row |
| Score weights A2:F5 | M.scenarios.*.weights | Five weights per scenario; no score calculation |
| Payoffs A2:H109 | M.interventions[].levels[] | 36 × levels 0, 1, 2; nominal cost/risk/resilience/acceptability |
| Lifecycle A2:J37 | M.interventions[].lifecycle and deliveryClass | Delays, repair costs, physical curves and tags; full records in companion |
| Interactions A2:E273 | M.interactions[] | Authored pair key and both IDs; raw signed payoffs |
| Category mix A2:G7 | M.categoryMix[] | Exact row-specific strict thresholds and signed payoffs |
| Events A2:I49 | E.events[].immediateEffects | Raw vectors only; no realised or mitigated-event claim |
| Parameters A:B, populated rows | M.parameters, flattened key in column A | Full parameter values; exact row key identifies the JSON path |
| Budget C2:I13 | D.openPlanning, prepareTurn, resolvePendingEvent | release + carry + pending − spending + event |
| Coordination H2:N5 | C.evaluateCoordinationLoad; M.parameters.coordinationLoad | Local arithmetic with engine-derived forest-link inputs |
| Risk E2:G13 | D.applyRiskReduction | One risk update per row; not turn/event replay |
| Acceptability B6:B9 and D2:D4 | D.packageAcceptability; M.parameters.acceptability | Fixed active package, including zero-total-cost fallback |
| Payoff checks E2:E8 | D.interactionEffects | Intensity and caps only |
| Payoff checks E9:E14 | D.saturationByIntervention; M.parameters.saturation | Rank coefficients only, no ranking |
| Payoff checks E15:E17 | D.concentrationEffect; M.categoryMix[0] | Three Infrastructure boundary fixtures |

The generic retained parameters `concentrationDominantShare` and `complementMinimumShare` are metadata and do not override the six runtime categoryMix rows. Current calculations use the row-specific thresholds.

## Verification protocol and limits

The delivered workbook is built from the canonical data with artifact-tool, then recalculated, inspected and rendered. Native Excel verification recalculates the saved file, compares selected results against an external fixture contract, perturbs inputs, restores all inputs, saves, reopens and recalculates again. Private evidence records the actual test results, errors, source hashes and independent review. A successful file export alone is not a verification result.

The selected checks cover all four budget schedules, no-reduction and floor-convergence cases, coordination within and above capacity, pair levels, saturation coefficients, concentration equality boundaries, a weighted active package and zero-cost fallback. Perturbation includes carryover with event and delayed budget changes, risk blank versus zero and an increased risk-reduction input. These checks establish the tested equations and data projections only. They do not establish full engine parity, statistical balance, classroom learning outcomes or compatibility with every spreadsheet application. No macros or external-workbook links are required.

This is not a player-results exchange file. Do not import it into the game as a saved session, and do not use it to configure the game. The application's result import rejects formula-bearing workbooks.

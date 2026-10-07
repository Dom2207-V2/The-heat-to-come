# Intervention catalogue

The Heat to Come · Application 2.5.0 · Model V2-2.3.0 · G2 dossier 2026-09-26

Audience: facilitators and technical reviewers. Language: English. Intended destination: public technical supplement, separate from the player manual. Editable master: Markdown; delivery copies: DOCX and PDF.

Source keys refer to the private V2 source root: M = `data/model/v2_3_model.json`; E = `data/events/v2_events.json`; T = `data/content/v2_3_en-GB.json`; D = `app/src/domain/engine-v2-3.mjs`. They are source identifiers, not public hyperlinks. Tables below are extracted from the current canonical data, never transcribed from the V1 workbook.

## Reading this catalogue

There are 36 interventions in six categories, each with L0, L1 and L2 records (108 level records). L0 means no intervention; its zeros do not enter package acceptability. L1 is limited/pilot; L2 is structural/comprehensive. C is capital cost in relative budget units; R is nominal risk-reduction strength; S is nominal resilience contribution; A is nominal acceptability. R is an input to the asymptotic risk calculation, not a direct subtraction from displayed risk. Negative S is retained. Scenario readiness, maturity, saturation, coordination and interactions determine realised effects. The technical framework gives the equations.

Starting directly at L2 pays the full L2 cost; upgrading pays L2 minus L1. Repairs are contextual, not annual fees. All started interventions persist through the three-turn run; there is no expiry, renewal or maintenance charge. A retained lifecycle class named temporary does not imply a countdown. Physical upkeep mentioned in intervention descriptions is real-world context, not an additional game operation or price.

Each maturity triplet describes the operation year and next two years. L2U is only the incremental upgrade segment. An operation can be unavailable late in the run if it cannot realise any productive payoff by final evaluation. Damage eligibility is permanent/persistent only; temporary items cannot be repaired because they are not damageable in this engine.

## Infrastructure

### INF01 — Urban greening and vegetation-based cooling

Adds shade and evapotranspirative cooling while improving the comfort and use of outdoor campus spaces.

L1: A limited planting pilot focused on selected routes or courtyards.

L2: A coordinated campus network of planted shade, soils and maintained vegetation.

Potential benefit: Can provide durable cooling and valued public space across several campus uses.

Trade-off: Needs suitable sites, water, maintenance and time; benefits may be uneven before vegetation matures.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 11 | 5 | 6 | 86 |
| 2 | 23 | 10 | 11 | 90 |

Delivery class: infrastructure. Lifecycle class: permanent. Activation delay L1 / L2: 1 / 1 turns. Upgrade cost: 12. Repair cost data: 0. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 0 / 1 / 1 |
| l2Direct | 0 / 0.5 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: cooling, shelter. 

Authored pair records involving this item: 15; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[0] (INT-V2-001); T interventions[runtimeId=INF01].

### INF02 — Cool surfaces and passive cooling materials

Reduces heat absorption through reflective, permeable or passive-cooling treatments on suitable buildings and surfaces.

L1: Targeted treatments on priority roofs, façades or paved areas.

L2: Broader coordinated treatment across multiple high-exposure campus assets.

Potential benefit: Can lower surface and indoor heat without requiring daily behaviour changes.

Trade-off: Installation can disrupt use, requires site assessment and may deliver less where shade or fabric already performs well.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 9 | 6 | 6 | 82 |
| 2 | 20 | 13 | 12 | 78 |

Delivery class: infrastructure. Lifecycle class: permanent. Activation delay L1 / L2: 1 / 1 turns. Upgrade cost: 11. Repair cost data: 0. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 0 / 1 / 1 |
| l2Direct | 0 / 0.5 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: cooling, shelter. 

Authored pair records involving this item: 12; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[1] (INT-V2-002); T interventions[runtimeId=INF02].

### INF03 — Shaded areas and cooling shelters

Creates accessible places for rest, waiting and recovery during high temperatures.

L1: A small number of shaded or cooled refuges at priority locations.

L2: A connected network of shelters serving major routes, entrances and activity areas.

Potential benefit: Offers visible, direct protection for people moving through or using the campus.

Trade-off: Coverage, accessibility, staffing and energy needs can limit who benefits and when.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 7 | 7 | 7 | 84 |
| 2 | 15 | 14 | 13 | 88 |

Delivery class: infrastructure. Lifecycle class: permanent. Activation delay L1 / L2: 1 / 1 turns. Upgrade cost: 8. Repair cost data: 0. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 0 / 1 / 1 |
| l2Direct | 0 / 0.5 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: cooling, shelter. 

Authored pair records involving this item: 18; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[2] (INT-V2-003); T interventions[runtimeId=INF03].

### INF04 — Thermal retrofit of critical campus buildings

Improves the thermal performance of buildings that host essential, high-occupancy or sensitive functions.

L1: Focused retrofit of selected rooms, systems or one priority building.

L2: Comprehensive fabric and passive-performance work across several critical buildings.

Potential benefit: Can deliver durable indoor protection and reduce dependence on emergency operating changes.

Trade-off: High cost and disruption may constrain near-term coverage and reduce flexibility for other needs.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 13 | 6 | 7 | 74 |
| 2 | 29 | 12 | 15 | 76 |

Delivery class: infrastructure. Lifecycle class: permanent. Activation delay L1 / L2: 1 / 1 turns. Upgrade cost: 16. Repair cost data: 0. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 0 / 1 / 1 |
| l2Direct | 0 / 0.5 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: cooling, shelter. 

Authored pair records involving this item: 11; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[3] (INT-V2-004); T interventions[runtimeId=INF04].

### INF05 — Water access and micro-cooling infrastructure

Expands access to drinking water and small-scale cooling at points of heat exposure.

L1: Targeted refill or micro-cooling points in a few high-use locations.

L2: A wider network with greater coverage, capacity and supporting services.

Potential benefit: Provides immediate, tangible support during heat and can serve varied campus users.

Trade-off: Higher coverage increases water, maintenance and monitoring demands; poorly placed points may see limited use.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 5 | 5 | 6 | 85 |
| 2 | 10 | 10 | 10 | 47 |

Delivery class: infrastructure. Lifecycle class: permanent. Activation delay L1 / L2: 1 / 1 turns. Upgrade cost: 5. Repair cost data: 0. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 0 / 1 / 1 |
| l2Direct | 0 / 0.5 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: cooling, shelter. 

Authored pair records involving this item: 15; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[4] (INT-V2-005); T interventions[runtimeId=INF05].

### INF06 — Replacement with new high-efficiency buildings

Replaces existing buildings with new structures designed for high thermal and energy performance.

L1: A limited replacement or demonstration project affecting a small part of the estate.

L2: A major replacement programme with broad construction, relocation and capital commitments.

Potential benefit: Can create modern, efficient space and address fabric limitations that incremental work cannot resolve.

Trade-off: Consumes substantial resources, causes displacement and may arrive too slowly or rigidly for changing near-term needs.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 15 | 1 | -2 | 58 |
| 2 | 35 | 4 | -5 | 42 |

Delivery class: infrastructure. Lifecycle class: permanent. Activation delay L1 / L2: 1 / 1 turns. Upgrade cost: 20. Repair cost data: 0. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 0 / 1 / 1 |
| l2Direct | 0 / 0.5 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: cooling, shelter. 

Authored pair records involving this item: 9; see the complete pair appendix by ID. Technical debrief flag: false friend. This is an explicit model classification; discuss the stated trade-offs and negative resilience rather than treating the title as a recommended solution.

Sources: M interventions[5] (INT-V2-006); T interventions[runtimeId=INF06].

## Operations

### OPS01 — Cooling and ventilation management

Coordinates cooling, ventilation, maintenance and room use to keep indoor conditions safer and services available.

L1: Basic operating protocols and checks for priority systems and rooms.

L2: Integrated management across buildings, schedules, maintenance and live conditions.

Potential benefit: Can improve protection quickly by using existing systems and operational knowledge more deliberately.

Trade-off: Depends on functioning equipment, skilled attention and energy management; wider coverage increases coordination demands.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 7 | 7 | 6 | 80 |
| 2 | 14 | 13 | 11 | 82 |

Delivery class: programme. Lifecycle class: persistent. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 7. Repair cost data: 1. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 0.5 / 1 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: continuity, monitoring. 

Authored pair records involving this item: 14; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[6] (INT-V2-007); T interventions[runtimeId=OPS01].

### OPS02 — Flexible use of spaces and scheduling adjustments

Moves activities in time or space to reduce exposure while preserving teaching and services.

L1: Limited adjustments for selected activities, periods or high-risk rooms.

L2: Campus-wide protocols that coordinate timetables, spaces and service dependencies.

Potential benefit: Can respond quickly and use existing capacity without waiting for construction.

Trade-off: Changes can create travel, caring, accessibility or coordination burdens and may reduce predictability for campus users.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 5 | 5 | 5 | 68 |
| 2 | 8 | 7 | 8 | 63 |

Delivery class: programme. Lifecycle class: persistent. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 3. Repair cost data: 1. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 0.5 / 1 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: continuity, monitoring. 

Authored pair records involving this item: 15; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[7] (INT-V2-008); T interventions[runtimeId=OPS02].

### OPS03 — Remote access and hybrid service delivery

Maintains learning and selected services when heat or disruption makes some in-person activity difficult.

L1: Remote continuity for a limited set of priority activities and services.

L2: Broad hybrid capability with coordinated platforms, support and service redesign.

Potential benefit: Provides continuity and flexibility when physical access is constrained.

Trade-off: Digital access, suitable space, workload and participation differ; wider use may weaken some in-person functions.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 7 | 4 | 5 | 70 |
| 2 | 11 | 6 | 8 | 58 |

Delivery class: programme. Lifecycle class: persistent. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 4. Repair cost data: 1. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 0.5 / 1 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: continuity, monitoring. 

Authored pair records involving this item: 8; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[8] (INT-V2-009); T interventions[runtimeId=OPS03].

### OPS04 — Indoor monitoring and adaptive building controls

Uses indoor conditions to guide ventilation, cooling and operational responses in occupied buildings.

L1: Monitoring and simple control changes in priority rooms or buildings.

L2: Integrated sensing and adaptive controls across a larger occupied estate.

Potential benefit: Makes hidden indoor exposure more visible and supports timely, evidence-led adjustments.

Trade-off: Sensors, data quality, privacy, maintenance and staff interpretation can limit reliable coverage.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 8 | 5 | 7 | 76 |
| 2 | 17 | 11 | 12 | 72 |

Delivery class: programme. Lifecycle class: persistent. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 9. Repair cost data: 1. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 0.5 / 1 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: continuity, monitoring. 

Authored pair records involving this item: 12; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[9] (INT-V2-010); T interventions[runtimeId=OPS04].

### OPS05 — Operating hours and building-use optimisation

Aligns opening hours, room allocation and service patterns with safer conditions and available capacity.

L1: Targeted changes for selected buildings, services or periods of high heat.

L2: Coordinated campus-wide operating patterns informed by conditions and demand.

Potential benefit: Can reduce exposure and concentrate support where buildings perform best.

Trade-off: Altered hours may disadvantage people with fixed schedules and can move rather than remove operational pressure.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 4 | 5 | 6 | 70 |
| 2 | 6 | 7 | 9 | 70 |

Delivery class: programme. Lifecycle class: persistent. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 2. Repair cost data: 1. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 0.5 / 1 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: continuity, monitoring. 

Authored pair records involving this item: 16; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[10] (INT-V2-011); T interventions[runtimeId=OPS05].

### OPS06 — Extended opening of air-conditioned buildings without energy management and targeting

Keeps cooled buildings open longer to provide additional refuge and activity space.

L1: Longer opening at a limited number of cooled buildings.

L2: Broad extended opening across multiple facilities and longer periods.

Potential benefit: Can expand access to cooler indoor space quickly when working systems and staff are available.

Trade-off: Untargeted expansion raises energy, staffing and equipment strain and may not reach those facing access barriers.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 9 | 6 | -2 | 60 |
| 2 | 20 | 9 | -4 | 45 |

Delivery class: programme. Lifecycle class: persistent. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 11. Repair cost data: 1. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 0.5 / 1 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: continuity, monitoring. 

Authored pair records involving this item: 18; see the complete pair appendix by ID. Technical debrief flag: false friend. This is an explicit model classification; discuss the stated trade-offs and negative resilience rather than treating the title as a recommended solution.

Sources: M interventions[11] (INT-V2-012); T interventions[runtimeId=OPS06].

## Preparedness

### PRE01 — Early warning systems and risk communication

Turns forecasts and observed conditions into timely, understandable information and action prompts.

L1: Basic alerts through selected channels with clear immediate guidance.

L2: Multi-channel, accessible warning linked to local thresholds, roles and feedback.

Potential benefit: Can give people and services time to adjust before exposure intensifies.

Trade-off: Warnings lose value if thresholds, accessibility, trust or action pathways are unclear; frequent alerts may cause fatigue.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 5 | 6 | 6 | 86 |
| 2 | 9 | 10 | 10 | 84 |

Delivery class: programme. Lifecycle class: persistent. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 4. Repair cost data: 1. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 0.5 / 1 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: warning, planning, vulnerable-support. 

Authored pair records involving this item: 24; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[12] (INT-V2-013); T interventions[runtimeId=PRE01].

### PRE02 — Heat action planning and emergency coordination

Defines responsibilities, triggers and coordination for heat response across campus functions.

L1: A focused action plan covering priority services and named coordinators.

L2: A comprehensive, tested plan joining campus units and external partners.

Potential benefit: Can reduce confusion and connect separate capabilities when conditions change quickly.

Trade-off: Planning absorbs staff time and becomes brittle if roles, contacts and assumptions are not kept current.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 7 | 5 | 7 | 80 |
| 2 | 12 | 8 | 11 | 82 |

Delivery class: programme. Lifecycle class: persistent. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 5. Repair cost data: 1. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 0.5 / 1 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: warning, planning, vulnerable-support. 

Authored pair records involving this item: 18; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[13] (INT-V2-014); T interventions[runtimeId=PRE02].

### PRE03 — Health response capacity and heat-illness training

Builds the ability to recognise, support and escalate heat-related health concerns.

L1: Training and response arrangements for selected frontline teams.

L2: Broad trained coverage with coordinated referral, supplies and partner links.

Potential benefit: Can shorten response time and improve confidence when people show signs of heat illness.

Trade-off: Training, staffing and clinical boundaries require upkeep; capacity can be uneven across shifts and locations.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 5 | 6 | 7 | 84 |
| 2 | 10 | 12 | 13 | 83 |

Delivery class: programme. Lifecycle class: persistent. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 5. Repair cost data: 1. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 0.5 / 1 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: warning, planning, vulnerable-support. 

Authored pair records involving this item: 12; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[14] (INT-V2-015); T interventions[runtimeId=PRE03].

### PRE04 — Heat hotspot and vulnerability mapping

Combines place, service and population information to identify where heat impacts may concentrate.

L1: An initial map of selected hotspots, functions and access barriers.

L2: A detailed, regularly updated evidence base linking indoor, outdoor and service conditions.

Potential benefit: Can focus attention on overlooked exposure and support transparent prioritisation.

Trade-off: Incomplete data can misdirect effort, and sensitive information requires care to avoid labelling places or people.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 7 | 5 | 6 | 72 |
| 2 | 13 | 9 | 11 | 66 |

Delivery class: programme. Lifecycle class: persistent. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 6. Repair cost data: 1. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 0.5 / 1 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: warning, planning, vulnerable-support. 

Authored pair records involving this item: 18; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[15] (INT-V2-016); T interventions[runtimeId=PRE04].

### PRE05 — Heatwave drills and preparedness exercises

Practises roles, decisions and communication before a real heat disruption occurs.

L1: A focused tabletop or operational exercise for priority teams.

L2: A broader multi-unit exercise including service partners and varied access needs.

Potential benefit: Can reveal coordination gaps safely and build familiarity with response roles.

Trade-off: Exercises use staff time, can disrupt routine work and offer limited value if findings are not acted upon.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 5 | 4 | 6 | 76 |
| 2 | 11 | 8 | 12 | 70 |

Delivery class: programme. Lifecycle class: persistent. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 6. Repair cost data: 1. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 0.5 / 1 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: warning, planning, vulnerable-support. 

Authored pair records involving this item: 9; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[16] (INT-V2-017); T interventions[runtimeId=PRE05].

### PRE06 — Standardised institutional emergency plan

Creates a common emergency template and chain of responsibility for heat-related disruption.

L1: A shared baseline template and institutional responsibilities.

L2: A fully standardised plan applied uniformly across campus functions.

Potential benefit: Can clarify minimum expectations and make responsibilities easier to locate during disruption.

Trade-off: Uniform rules may overlook local conditions, and a comprehensive document can create confidence without practical capability.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 6 | 3 | -2 | 72 |
| 2 | 11 | 5 | -5 | 60 |

Delivery class: programme. Lifecycle class: persistent. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 5. Repair cost data: 1. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 0.5 / 1 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: warning, planning, vulnerable-support. 

Authored pair records involving this item: 10; see the complete pair appendix by ID. Technical debrief flag: false friend. This is an explicit model classification; discuss the stated trade-offs and negative resilience rather than treating the title as a recommended solution.

Sources: M interventions[17] (INT-V2-018); T interventions[runtimeId=PRE06].

## Governance

### GOV01 — Climate adaptation strategy

Sets shared adaptation aims, responsibilities and a pathway for coordinated campus decisions over time.

L1: A focused strategy covering priority risks, roles and near-term actions.

L2: An institution-wide strategy integrated with planning, finance and service decisions.

Potential benefit: Can connect individual actions to durable direction and make future choices more coherent.

Trade-off: Strategy work uses time and may remain abstract if authority, resources and review points are weak.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 5 | 3 | 6 | 82 |
| 2 | 9 | 5 | 11 | 86 |

Delivery class: programme. Lifecycle class: persistent. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 4. Repair cost data: 1. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 0.5 / 1 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: planning, coordination, monitoring. 

Authored pair records involving this item: 20; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[18] (INT-V2-019); T interventions[runtimeId=GOV01].

### GOV02 — Monitoring, evaluation and learning systems

Tracks conditions, implementation and outcomes so the campus can adjust its response across turns.

L1: A small set of indicators and review points for priority actions.

L2: A coordinated learning system joining operational, environmental and participation evidence.

Potential benefit: Can reveal whether intended effects are arriving and support correction when conditions change.

Trade-off: Data collection has cost, may burden staff or participants and can distract if findings do not reach decisions.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 5 | 2 | 6 | 80 |
| 2 | 9 | 3 | 11 | 85 |

Delivery class: programme. Lifecycle class: persistent. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 4. Repair cost data: 1. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 0.5 / 1 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: planning, coordination, monitoring. 

Authored pair records involving this item: 19; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[19] (INT-V2-020); T interventions[runtimeId=GOV02].

### GOV03 — Climate-risk screening in campus investments

Tests proposed investments against heat risk, resilience and changing conditions before commitments are locked in.

L1: Basic screening for larger or higher-risk proposals.

L2: Systematic screening across capital, maintenance and service investment decisions.

Potential benefit: Can prevent avoidable exposure and make long-lived spending more adaptable.

Trade-off: Adds analysis and approval work, depends on usable evidence and may slow urgent investment if poorly designed.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 6 | 2 | 5 | 76 |
| 2 | 11 | 4 | 8 | 78 |

Delivery class: programme. Lifecycle class: persistent. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 5. Repair cost data: 1. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 0.5 / 1 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: planning, coordination, monitoring. 

Authored pair records involving this item: 12; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[20] (INT-V2-021); T interventions[runtimeId=GOV03].

### GOV04 — Climate-resilient procurement and tender criteria

Builds heat resilience, continuity and lifecycle expectations into purchasing and supplier decisions.

L1: Resilience criteria for selected high-priority purchases or tenders.

L2: Coordinated criteria and supplier assurance across relevant procurement categories.

Potential benefit: Can improve the reliability of goods, works and services before disruption occurs.

Trade-off: Criteria can narrow suppliers, raise near-term cost or delay purchasing if requirements exceed market capacity.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 6 | 2 | 5 | 74 |
| 2 | 11 | 4 | 8 | 77 |

Delivery class: programme. Lifecycle class: persistent. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 5. Repair cost data: 1. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 0.5 / 1 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: planning, coordination, monitoring. 

Authored pair records involving this item: 12; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[21] (INT-V2-022); T interventions[runtimeId=GOV04].

### GOV05 — Cross-departmental coordination and operational accountability

Connects decisions, owners and follow-through across academic, estates, health and support functions.

L1: A focused coordination group with named owners for priority risks.

L2: Institution-wide accountability with clear escalation, reporting and partner links.

Potential benefit: Can reduce gaps between plans and delivery and help capabilities work together during events.

Trade-off: Coordination consumes attention and can become slow or performative when authority and decisions are unclear.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 4 | 4 | 7 | 78 |
| 2 | 7 | 7 | 11 | 83 |

Delivery class: programme. Lifecycle class: persistent. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 3. Repair cost data: 1. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 0.5 / 1 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: planning, coordination, monitoring. 

Authored pair records involving this item: 26; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[22] (INT-V2-023); T interventions[runtimeId=GOV05].

### GOV06 — Climate compensation as the main response

Uses compensation or offsetting activity as the principal institutional response to climate impact.

L1: A limited compensation programme alongside existing campus activity.

L2: A broad programme positioned as the institution's main climate response.

Potential benefit: Can mobilise funding, signal responsibility and support activity beyond the campus boundary.

Trade-off: Does not directly change local heat exposure and can displace attention, resources or accountability for campus adaptation.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 7 | 1 | -2 | 58 |
| 2 | 15 | 2 | -2 | 38 |

Delivery class: programme. Lifecycle class: persistent. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 8. Repair cost data: 1. Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 0.5 / 1 / 1 |
| l2Upgrade | 0 / 1 / 1 |

Capability tags: planning, coordination, monitoring. 

Authored pair records involving this item: 30; see the complete pair appendix by ID. Technical debrief flag: false friend. This is an explicit model classification; discuss the stated trade-offs and negative resilience rather than treating the title as a recommended solution.

Sources: M interventions[23] (INT-V2-024); T interventions[runtimeId=GOV06].

## Behavioural

### BEH01 — Awareness campaigns, behavioural guidance and nudges

Shares practical heat information and prompts safer routines across campus activities.

L1: Targeted messages and prompts for priority settings or periods.

L2: A coordinated, accessible campaign across channels, places and campus roles.

Potential benefit: Can reach many people quickly and make existing protection easier to understand and use.

Trade-off: Messages may fade, miss access needs or shift responsibility onto individuals when services and spaces remain unchanged.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 3 | 4 | 4 | 86 |
| 2 | 5 | 6 | 7 | 84 |

Delivery class: immediate. Lifecycle class: temporary. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 2. Repair cost data: 1 (not actionable: this class is not damageable). Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 1 / 1 / 1 |
| l2Upgrade | 1 / 1 / 1 |

Capability tags: awareness, vulnerable-support. Direct-L2 rationale: Operationally scalable within the same academic-year hot season; direct L2 is intentionally immediate.

Authored pair records involving this item: 17; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[24] (INT-V2-025); T interventions[runtimeId=BEH01].

### BEH02 — Targeted support for vulnerable groups

Provides tailored access, communication and practical support where circumstances increase heat exposure or barriers.

L1: Focused support through selected services, places or trusted channels.

L2: Broader coordinated support with multiple access routes and service partners.

Potential benefit: Can address specific barriers and make campus protection more reachable during disruption.

Trade-off: Targeting needs good evidence and participation; weak design can stigmatise, exclude or overlook changing circumstances.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 5 | 6 | 6 | 82 |
| 2 | 10 | 11 | 11 | 76 |

Delivery class: immediate. Lifecycle class: temporary. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 5. Repair cost data: 1 (not actionable: this class is not damageable). Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 1 / 1 / 1 |
| l2Upgrade | 1 / 1 / 1 |

Capability tags: awareness, vulnerable-support. Direct-L2 rationale: Operationally scalable within the same academic-year hot season; direct L2 is intentionally immediate.

Authored pair records involving this item: 15; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[25] (INT-V2-026); T interventions[runtimeId=BEH02].

### BEH03 — Hydration, rest breaks and cooling-space use campaigns

Encourages and enables hydration, recovery time and use of available cooler spaces during heat.

L1: Focused guidance and prompts for selected high-exposure activities.

L2: A campus-wide campaign linked to breaks, refill points and cooling-space information.

Potential benefit: Can support practical protective routines quickly using services already in place.

Trade-off: Effect depends on real access, supportive managers and usable facilities; messaging alone cannot remove structural exposure.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 3 | 4 | 4 | 85 |
| 2 | 5 | 6 | 7 | 80 |

Delivery class: immediate. Lifecycle class: temporary. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 2. Repair cost data: 1 (not actionable: this class is not damageable). Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 1 / 1 / 1 |
| l2Upgrade | 1 / 1 / 1 |

Capability tags: awareness, vulnerable-support. Direct-L2 rationale: Operationally scalable within the same academic-year hot season; direct L2 is intentionally immediate.

Authored pair records involving this item: 16; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[26] (INT-V2-027); T interventions[runtimeId=BEH03].

### BEH04 — Student and staff climate stewards

Builds a peer network that shares observations, supports communication and connects local concerns to decisions.

L1: A small steward network in selected services, buildings or communities.

L2: A supported campus-wide network with training, feedback and governance links.

Potential benefit: Can extend trusted communication and surface place-specific knowledge that central systems miss.

Trade-off: Relies on sustained participation and may transfer institutional work to volunteers without adequate support or influence.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 4 | 4 | 5 | 76 |
| 2 | 8 | 7 | 10 | 74 |

Delivery class: immediate. Lifecycle class: temporary. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 4. Repair cost data: 1 (not actionable: this class is not damageable). Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 1 / 1 / 1 |
| l2Upgrade | 1 / 1 / 1 |

Capability tags: awareness, vulnerable-support. Direct-L2 rationale: Operationally scalable within the same academic-year hot season; direct L2 is intentionally immediate.

Authored pair records involving this item: 12; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[27] (INT-V2-028); T interventions[runtimeId=BEH04].

### BEH05 — Living labs and participatory campus adaptation

Invites campus communities to test, observe and shape adaptation in real settings.

L1: A focused co-designed pilot around one place, service or question.

L2: A broader programme linking several pilots, disciplines and decision owners.

Potential benefit: Can build legitimacy, local evidence and practical learning before long-lived commitments.

Trade-off: Participation takes time, benefits may arrive gradually and pilots can frustrate contributors if decisions do not respond.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 5 | 2 | 5 | 80 |
| 2 | 11 | 3 | 11 | 86 |

Delivery class: immediate. Lifecycle class: temporary. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 6. Repair cost data: 1 (not actionable: this class is not damageable). Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 1 / 1 / 1 |
| l2Upgrade | 1 / 1 / 1 |

Capability tags: awareness, vulnerable-support. Direct-L2 rationale: Operationally scalable within the same academic-year hot season; direct L2 is intentionally immediate.

Authored pair records involving this item: 13; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[28] (INT-V2-029); T interventions[runtimeId=BEH05].

### BEH06 — Individual responsibility without structural support

Relies mainly on individuals to manage their own heat exposure through guidance and personal choices.

L1: Limited guidance asking people to adjust routines and personal precautions.

L2: A broad campaign placing extensive emphasis on individual self-management.

Potential benefit: Can disseminate simple actions quickly and may help where people have genuine control and resources.

Trade-off: People have unequal options, and advice without supportive spaces, services or working conditions can shift burden unfairly.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 3 | 2 | -2 | 60 |
| 2 | 5 | 3 | -2 | 40 |

Delivery class: immediate. Lifecycle class: temporary. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 2. Repair cost data: 1 (not actionable: this class is not damageable). Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 1 / 1 / 1 |
| l2Upgrade | 1 / 1 / 1 |

Capability tags: awareness, vulnerable-support. Direct-L2 rationale: Operationally scalable within the same academic-year hot season; direct L2 is intentionally immediate.

Authored pair records involving this item: 13; see the complete pair appendix by ID. Technical debrief flag: false friend. This is an explicit model classification; discuss the stated trade-offs and negative resilience rather than treating the title as a recommended solution.

Sources: M interventions[29] (INT-V2-030); T interventions[runtimeId=BEH06].

## Restrictive

### RES01 — Mandatory restrictions on in-person activities

Temporarily limits in-person activity to reduce exposure during periods of high heat.

L1: Targeted limits for selected activities, locations or high-risk periods.

L2: Broad restrictions affecting a larger share of campus activity.

Potential benefit: Can reduce direct exposure quickly when conditions exceed what normal operations can manage.

Trade-off: Disrupts learning, work and access to services; repeated or broad use can reduce continuity, trust and acceptability.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 5 | 7 | 3 | 58 |
| 2 | 12 | 16 | 4 | 42 |

Delivery class: immediate. Lifecycle class: temporary. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 7. Repair cost data: 1 (not actionable: this class is not damageable). Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 1 / 1 / 1 |
| l2Upgrade | 1 / 1 / 1 |

Capability tags: restriction, continuity. Direct-L2 rationale: Operationally scalable within the same academic-year hot season; direct L2 is intentionally immediate.

Authored pair records involving this item: 18; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[30] (INT-V2-031); T interventions[runtimeId=RES01].

### RES02 — Mandatory alternative operations without adequate infrastructure support

Requires activities to switch mode or location when normal operations are judged unsafe.

L1: A limited mandatory switch for selected services or activities.

L2: A broad mandatory alternative operating model across the campus.

Potential benefit: Can reduce exposure promptly and keep some functions moving when ordinary arrangements fail.

Trade-off: Without reliable platforms, spaces and support, mandatory change can interrupt services and deepen unequal access.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 4 | 6 | -2 | 52 |
| 2 | 10 | 13 | -2 | 32 |

Delivery class: immediate. Lifecycle class: temporary. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 6. Repair cost data: 1 (not actionable: this class is not damageable). Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 1 / 1 / 1 |
| l2Upgrade | 1 / 1 / 1 |

Capability tags: restriction, continuity. Direct-L2 rationale: Operationally scalable within the same academic-year hot season; direct L2 is intentionally immediate.

Authored pair records involving this item: 14; see the complete pair appendix by ID. Technical debrief flag: false friend. This is an explicit model classification; discuss the stated trade-offs and negative resilience rather than treating the title as a recommended solution.

Sources: M interventions[31] (INT-V2-032); T interventions[runtimeId=RES02].

### RES03 — Selective suspension of outdoor events and activities

Pauses selected outdoor activity when heat makes timing, duration or location unsafe.

L1: Targeted pauses during the highest-risk times or for selected activities.

L2: Wider suspension covering more events, locations or longer periods.

Potential benefit: Can cut exposure quickly while leaving lower-risk campus activity available.

Trade-off: Removes valued activity, affects organisers and may exclude people unless alternatives and communication are workable.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 4 | 6 | 4 | 68 |
| 2 | 7 | 10 | 6 | 62 |

Delivery class: immediate. Lifecycle class: temporary. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 3. Repair cost data: 1 (not actionable: this class is not damageable). Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 1 / 1 / 1 |
| l2Upgrade | 1 / 1 / 1 |

Capability tags: restriction, continuity. Direct-L2 rationale: Operationally scalable within the same academic-year hot season; direct L2 is intentionally immediate.

Authored pair records involving this item: 12; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[32] (INT-V2-033); T interventions[runtimeId=RES03].

### RES04 — Controlled access to high-heat-risk spaces

Limits entry to locations where heat exposure cannot be managed safely under current conditions.

L1: Targeted controls at selected high-risk spaces or times.

L2: Broader access controls across multiple spaces and operating periods.

Potential benefit: Can prevent exposure in known hotspots and focus supervision where risk is concentrated.

Trade-off: Controls can disrupt routes, work and services, and may create new access barriers or displacement elsewhere.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 4 | 5 | 3 | 62 |
| 2 | 8 | 10 | 5 | 52 |

Delivery class: immediate. Lifecycle class: temporary. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 4. Repair cost data: 1 (not actionable: this class is not damageable). Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 1 / 1 / 1 |
| l2Upgrade | 1 / 1 / 1 |

Capability tags: restriction, continuity. Direct-L2 rationale: Operationally scalable within the same academic-year hot season; direct L2 is intentionally immediate.

Authored pair records involving this item: 13; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[33] (INT-V2-034); T interventions[runtimeId=RES04].

### RES05 — Mandatory reduction of hours or occupancy during heat peaks

Reduces the time or number of people exposed in buildings during the hottest periods.

L1: Limited reductions for selected buildings, hours or high-occupancy activities.

L2: Broad reductions across many services, spaces or parts of the day.

Potential benefit: Can lower peak exposure quickly and reduce pressure on strained building systems.

Trade-off: Shorter hours and lower capacity constrain learning, work and services and may shift burden to other times or places.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 5 | 6 | 3 | 55 |
| 2 | 10 | 13 | 4 | 40 |

Delivery class: immediate. Lifecycle class: temporary. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 5. Repair cost data: 1 (not actionable: this class is not damageable). Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 1 / 1 / 1 |
| l2Upgrade | 1 / 1 / 1 |

Capability tags: restriction, continuity. Direct-L2 rationale: Operationally scalable within the same academic-year hot season; direct L2 is intentionally immediate.

Authored pair records involving this item: 17; see the complete pair appendix by ID. Technical debrief flag: not marked false friend. This does not make the intervention universally appropriate.

Sources: M interventions[34] (INT-V2-035); T interventions[runtimeId=RES05].

### RES06 — Recurrent general closures as an ordinary strategy

Uses repeated campus-wide closure as a routine response when heat risk is anticipated.

L1: Occasional general closure during selected high-risk periods.

L2: Frequent or extended general closures embedded in ordinary operating practice.

Potential benefit: Can sharply reduce exposure on closed sites when people can safely remain elsewhere.

Trade-off: Repeated closure interrupts essential functions, affects people unevenly and can erode continuity, trust and institutional capacity.

| Level | C | R | S | A |
| --- | --- | --- | --- | --- |
| 0 | 0 | 0 | 0 | 0 |
| 1 | 6 | 8 | -2 | 45 |
| 2 | 15 | 18 | -2 | 25 |

Delivery class: immediate. Lifecycle class: temporary. Activation delay L1 / L2: 0 / 0 turns. Upgrade cost: 9. Repair cost data: 1 (not actionable: this class is not damageable). Persistence: remainder of this run, unless capability is suppressed by damage.

| Path | Maturity year 0 / 1 / 2 |
| --- | --- |
| l1 | 1 / 1 / 1 |
| l2Direct | 1 / 1 / 1 |
| l2Upgrade | 1 / 1 / 1 |

Capability tags: restriction, continuity. Direct-L2 rationale: Operationally scalable within the same academic-year hot season; direct L2 is intentionally immediate.

Authored pair records involving this item: 11; see the complete pair appendix by ID. Technical debrief flag: false friend. This is an explicit model classification; discuss the stated trade-offs and negative resilience rather than treating the title as a recommended solution.

Sources: M interventions[35] (INT-V2-036); T interventions[runtimeId=RES06].

## Interpretation limit

Catalogue payoffs are educational modelling decisions. They do not establish empirical effectiveness, procurement costs or permission to impose restrictions. Pair effects and concentration represent selected organisational complementarities and frictions; absent pairs contribute zero pair payoff. They do not demonstrate that no real interaction exists. The technical appendix contains all current authored records, and the workbook states which calculations it reproduces.


## Coordination correction and exact rule identity

Owner decision DEC-G2-20260926-001 authorises canonical interaction lookup by the sorted intervention IDs. The earlier implementation missed 107 of 272 authored pair keys because their stored order differed from the lookup order. Both positive connectivity and conflict diagnostics now use all applicable authored records; pair payoff coefficients, model values and event data are unchanged. Multi-operation effectiveness and downstream results can change. This is not a V1 numerical model.

Current rule revision: `engine-v2.3.0-active-score-rebalance-coordination-v2`. Compatibility fingerprint: `rules-v2.3.0-coordination-pair-normalisation-2026-09-26.1`. Application version 2.5.0 and model version V2-2.3.0 alone do not identify these rules. The separate G1 run03 handoff records qualification results and the exact tested files for the corrected implementation. Earlier saves with the old rule fingerprint are rejected. No automatic migration or inherited statistical acceptance is claimed.

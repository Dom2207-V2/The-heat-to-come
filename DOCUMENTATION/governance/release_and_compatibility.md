# Release notes and compatibility

The Heat to Come application 2.5.0, model V2-2.3.0. Documentation revision 1, 26 September 2026. Audience: players, facilitators and maintainers. Language: English. Distribution: public documentation candidate. Editorial author: G2 coordinator. Independent review: recorded in the private G2 handoff.

This dossier describes application 2.5.0 with the owner-authorised coordination correction. The separate G1 run03 handoff records requalification of the corrected rules and its exact tested files; the earlier G1 run02 PASS does not qualify this revision. It does not supply a new Windows package or certify a deployed website. Packaging, final package testing and owner upload are later release stages. The current game uses synthetic decision indices for education, with three decision turns and a final evaluation. It is not a climate forecast or an operational decision service.

## Changes in 2.5.0

The entry experience previews the campus and explains the Plan, Face an event, Adapt cycle. Four illustrated scenario previews distinguish the campuses. The tutorial and briefing place the entry action near the summary. Catalogue cards show current state, planned operation and cost without requiring every detail panel to be opened. Map actions open and focus the corresponding intervention even when catalogue filters would otherwise hide it.

Turn recaps retain the previous decision and event context. Planning filters and drafts survive save and reload; Selected only resets when advancing to a new turn. Score-component formatting avoids rounding a below-threshold value into a higher apparent band. The final-turn budget text distinguishes an unresolved final event from resources remaining after the completed game.

G1 additionally corrected revision ordering across persistent and temporary storage, rejected malformed drafts, handled large and Unicode XLSX payloads using numbered chunks, retained earlier same-candidate one-cell payload reading, rejected invalid/formula/macro/oversized imports, restored focus around the intervention drawer and corrected two contrast issues. Those earlier changes preserved the numerical rules. The later SCI-B-001 correction fixes the recognition of authored coordination pairs and can change multi-operation outcomes. Model/event data values remain unchanged; the rules have a distinct fingerprint.

## Model identity and save boundary

Application version and model version are different identifiers. Application 2.5.0 retains model V2-2.3.0 and the approved Alpha-5 game values. A new presentation does not imply a new payoff model. The game-value digest is b6f8bab7c225098ecce24004f9097961ae397fbe0dd40fcd77a98b7f85daeded.

New runs, archives, preferences and optional traces use separate 2.5.0 storage keys. Planning drafts and player envelopes use schema 2.5-ui.1; the result workbook sheet is V2.5 Run. Historical storage is not automatically migrated, overwritten or deleted. Old releases are historical, with read-only archive handling where available. Their exported saves must not be treated as resumable current runs.

Imports follow exact-match-for-same-build-import. A matching application version number alone is insufficient: the model, rules, content and presentation compatibility fingerprints must also match. Earlier 2.5.0 candidate exports may therefore be rejected after presentation changes. There is no automatic old-save migration. Keep the original export and use the matching historical release where available; do not edit fingerprints to force acceptance.

## Saving and moving results

Browser records belong to the browser profile and site origin. Changing browser, profile, host, protocol or port can expose a different storage area. Export JSON or XLSX deliberately before moving between environments. Browser clearing, private browsing or storage restrictions may remove local records. When persistent storage is unavailable or full, the app can use session or memory fallback and displays a warning; temporary state is not a durable backup. Downloaded exports must be stored and deleted separately.

The payoff audit workbook in this dossier is a parameter and selected-formula companion. It is not a player-result import workbook and must not be imported through the game's result importer.

## Verified platform scope

The earlier G1 run02 automated browser evidence covered Chromium 151.0.7922.34, Firefox 153.0 and WebKit 26.5. It includes 48 completed games, 144 turns and 36 parity comparisons in the documented candidate/baseline matrix. Candidate scenarios were exercised at 320, 390 and 1440 pixel widths. Separate entry checks extend to 2560 pixels. Save, import, export, replay, focus and selected contrast behaviours were checked against the identified build.

These are automated browser-engine and emulation results. They do not establish physical Safari on Apple devices, physical Chrome on Android, every vendor browser build, human screen-reader usability, an entirely keyboard-only game or general WCAG certification. Responsive, touch, motion, forced-colour and CSS zoom checks are emulations. Gradient and transparency contrast is outside the solid-colour measurements. Human comprehension, classroom learning outcomes, physical devices and subjective listening were not tested in G1.

Windows distribution is planned as a self-contained loopback package. macOS, Linux and Chromebook use browser delivery under the existing architecture; no new native package for those systems is claimed. Final launcher, extraction, Pages path and downloadable-asset checks belong to the package qualification, not this document gate.

## Validation and historical limits

The earlier G1 PASS is bounded by the owner's accepted loss of 226 exact historical files. The remaining historical files have a separate integrity inventory. The original strict historical-preservation gate remains failing while originals are unavailable. This dossier does not attest complete reproduction of the lost packages. G1 run01 remains INCOMPLETE under its original scope; run02 subsequently received a scoped PASS under the authorised historical-loss exception, for the earlier runtime only.

Current deterministic engine and replay tests support model consistency. Historical statistical acceptance was not rerun in G1 run02. The corrected rules require fresh G1 run03 evidence, including applicable density diagnostics; old estimates are not inherited. Historical canonical-leaf density estimates are model-space diagnostics, not probabilities of success for human players. The offline shadow mission-attainment methods were not adopted as the score displayed by the game.

## Sources and related documents

Source identifiers: G1 run03 handoff and corrected-runtime independent review; DEC-G2-20260926-001; historical G1 run02 handoff and final independent review; G1 run01 browser and persistence evidence; V2.5 technical boundary and implementation report; DEC-G1-20260925-002. Exact source locators and hashes are retained in the private traceability inventory. See [Privacy](PRIVACY.md), [Support](SUPPORT.md), [Security](SECURITY.md), [Credits](CREDITS_AND_PROVENANCE.md), [Third-party notices](THIRD_PARTY_NOTICES.md) and [adopted licence](LICENSE.txt).

## Corrected coordination rules

SCI-B-001 affected 107 of 272 authored pair keys. Lookup now canonicalises id1/id2 consistently, restoring applicable links and conflict diagnostics. Rule revision: `engine-v2.3.0-active-score-rebalance-coordination-v2`; fingerprint: `rules-v2.3.0-coordination-pair-normalisation-2026-09-26.1`. The corrected run must pass independent mechanics, compatibility, browser and applicable statistical checks before final qualification. Earlier candidate saves also fail when their rules fingerprint differs. Owner authorisation: DEC-G2-20260926-001. No new model parameter values were selected.

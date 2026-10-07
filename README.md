# The Heat to Come

A climate simulator game about campus adaptation, limited resources and decisions over three turns.

Application **2.5.1** · Model data **V2-2.3.0** · Coordination rules **coordination-v2** · Documentation revision **2**.

## Play or download

Open [the playable website](https://dom2207-v2.github.io/The-heat-to-come/) and choose **Play**. The [GitHub repository](https://github.com/Dom2207-V2/The-heat-to-come) contains the downloadable files and documentation.

For offline use on Windows x64, download [the complete Windows ZIP](downloads/windows/the-heat-to-come-v2.5.1-windows.zip), choose **Extract all**, and open **Open The Heat to Come.vbs** from the extracted folder. The runtime is included. Use **Close The Heat to Come.vbs** to stop the local server after playing. Do not run the game inside the ZIP or open its HTML directly. See the package's start instructions for platform restrictions and troubleshooting.

The same ZIP and the [complete dossier ZIP](downloads/dossier/the-heat-to-come-v2.5.1-dossier.zip) are intended as Release attachments. The automatically generated GitHub “Source code” archives contain this compiled public repository; they are not the self-contained Windows package or the private development sources.

## Security update

Version 2.5.1 updates SheetJS to 0.20.3 and the Windows runtime to Node.js 22.23.3. Author metadata is removed from the public workbook. The 2.5.0 save namespace and all game fingerprints are preserved; valid saves from the previously published build remain readable. See [the security update](DOCUMENTATION/SECURITY_UPDATE_2.5.1.md).

## Begin a game

Read the [quick start](DOCUMENTATION/editions/quick_start.pdf), choose a scenario and follow the Plan, Face an event, Adapt cycle. Export results deliberately before moving between browsers or between the web and Windows versions: browser records belong to the browser profile and site origin.

This educational game uses synthetic indices. Its results are not climate forecasts or operational recommendations. The coordination correction recognises authored intervention pairs consistently and can change outcomes; older candidate saves with different fingerprints are not silently migrated.

## Read and teach

The [dossier index](DOCUMENTATION/INDEX.md) lists the document files, including 11 PDF/DOCX pairs, Markdown masters, the editable payoff workbook and parameter extract. Start with the [player guide](DOCUMENTATION/editions/player_guide.pdf) or [facilitator guide](DOCUMENTATION/editions/facilitator_guide.pdf). Technical supplements are separate from player instructions and can be reserved for debrief.

The workbook reproduces selected formulas and checks; it does not implement the complete game engine and is not a game-save file. See [compatibility and release notes](DOCUMENTATION/governance/release_and_compatibility.md). The scientific manuals retain their 2.5.0 edition because the model, equations and gameplay are unchanged. [The security update](DOCUMENTATION/SECURITY_UPDATE_2.5.1.md) supersedes their dependency and distribution details. [DISTRIBUTION.json](DISTRIBUTION.json) identifies this build.

## Scope and support

Local build and package checks do not establish classroom effectiveness, human comprehension, complete assistive-technology coverage or physical mobile compatibility. Safari on physical iPhone/iPad and Chrome on physical Android remain untested. Each deployment and download should be checked against the published file hashes.

Read [Privacy](PRIVACY.md), [Support](SUPPORT.md) and [Security](SECURITY.md). The game has no account, telemetry or ordinary external asset dependency. GitHub hosting has its own technical-data practices.

## Licence and credits

The [Educational Public Distribution Licence](LICENSE.txt) governs the game. This compiled distribution is not an open-source release. Third-party rights remain governed by their own licences: [notices](THIRD_PARTY_NOTICES.md), [licence texts](third-party-licenses/) and [credits and provenance](CREDITS_AND_PROVENANCE.md).

The private development and maintenance archive is intentionally outside this public repository. File integrity is recorded in [PUBLIC_INVENTORY.json](PUBLIC_INVENTORY.json) and [checksums-sha256.txt](checksums-sha256.txt).

# Security maintenance update — 2.5.1

7 October 2026. Application distribution 2.5.1; model V2-2.3.0; documentation revision 2.

## Changes

SheetJS Community Edition is updated from 0.18.5 to the official self-contained 0.20.3 release. This addresses the known prototype-pollution issue CVE-2023-30533 and regular-expression denial-of-service issue CVE-2024-22363. The existing file-size limit and rejection of formula cells and macros remain in effect. Import only game-save files from a trusted source.

The private build dependency source-map-js is pinned to 1.2.2, addressing CVE-2026-93749. It is used by the compiler and is not a service exposed by the published game.

The Windows package includes the official Node.js 22.23.3 x64 runtime, with its SHA-256 checked against the Node.js release. Its local server remains bound to 127.0.0.1 only, validates the Host header, confines file delivery to the app and documentation folders, and requires a random per-instance token for shutdown. The public website remains static GitHub Pages hosting.

Creator and last-modified-by fields are cleared from the public workbook. Every other uncompressed XLSX part is retained byte for byte, including worksheets, cached formula results, styles, drawings and relationships. Required copyright and credit attribution remains in the licence and credits.

## Compatibility

No gameplay source, scenario, model, event, rule, content or presentation fingerprint is changed. Browser storage keys, UI save schema 2.5-ui.1 and engine schema 2.3.0 remain unchanged. Valid saves and exports from the previously published 2.5.0 build remain compatible. Older releases with different model, rule or presentation fingerprints are still rejected or treated as historical archives.

The PDF/DOCX scientific manuals retain their original 2.5.0 edition and scientific content. This update supersedes their component-version, public-distribution and workbook-metadata statements. Current dependency details are in governance/THIRD_PARTY_NOTICES.md; current distribution hashes are in ../DISTRIBUTION.json and ../checksums-sha256.txt.

## Scope

This is a security maintenance release of the existing candidate. It does not establish physical mobile-device support, human accessibility or classroom effectiveness. It does not erase copies of previous downloads, commits or cached pages held elsewhere.

Official sources: https://cdn.sheetjs.com/advisories/CVE-2023-30533 ; https://cdn.sheetjs.com/advisories/CVE-2024-22363 ; https://docs.sheetjs.com/docs/getting-started/installation/frameworks/ ; https://nodejs.org/en/blog/release/v22.23.3 ; https://github.com/advisories/GHSA-68fv-2mgg-jv7q .

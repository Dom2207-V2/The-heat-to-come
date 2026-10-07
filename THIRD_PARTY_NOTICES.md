# Third-party notices for 2.5.1

This distribution contains compiled third-party components. The licences below apply only to their respective components; they do not grant a licence to the complete game, its name, logo, editorial content or development repository.

## Compiled web application

| Component | Version or identity | Licence | Included text |
|---|---:|---|---|
| React | 19.2.8 | MIT | `third-party-licenses/React-MIT.txt` |
| React DOM | 19.2.8 | MIT | `third-party-licenses/React-DOM-MIT.txt` |
| Scheduler | 0.27.0 | MIT | `third-party-licenses/Scheduler-MIT.txt` |
| SheetJS Community Edition (`xlsx`) | 0.20.3 | Apache-2.0 | `third-party-licenses/SheetJS-Apache-2.0.txt` |
| `adler-32` | 1.3.1 | Apache-2.0 | `third-party-licenses/adler-32-Apache-2.0.txt` |
| `cfb` | 1.2.2 | Apache-2.0 | `third-party-licenses/cfb-Apache-2.0.txt` |
| `codepage` | 1.15.0 | Apache-2.0 | `third-party-licenses/codepage-Apache-2.0.txt` |
| `crc-32` | 1.2.2 | Apache-2.0 | `third-party-licenses/crc-32-Apache-2.0.txt` |
| `frac` | 1.1.2 | Apache-2.0 | `third-party-licenses/frac-Apache-2.0.txt` |
| `ssf` | 0.11.2 | Apache-2.0 | `third-party-licenses/ssf-Apache-2.0.txt` |
| `wmf` | 1.0.2 | Apache-2.0 | `third-party-licenses/wmf-Apache-2.0.txt` |
| `word` | 0.3.0 | Apache-2.0 | `third-party-licenses/word-Apache-2.0.txt` |
| Roboto Variable | file SHA-256 `d7598e12c5dbef095ff8272cfc55da0250bd07fbdecbac8a530b9b277872a134` | SIL Open Font License 1.1 | `third-party-licenses/Roboto-OFL-1.1.txt` |
| Sixteen local audio derivatives from three John Bartmann source recordings | hashes in `QUALIFIED_ASSET_HASHES.json` | CC0 1.0 | `third-party-licenses/Audio-CC0-1.0.txt` |

The audio sources are *Above the Clouds*, *Broken Suspense* and *Auspicious Flutes*. Attribution is retained as provenance even though CC0 does not require it. The runtime files are frame-aligned derivatives of immutable source recordings.

## Windows package

The Windows ZIP includes the official Node.js 22.23.3 x64 executable and its consolidated licence at `THIRD-PARTY-LICENSES/Node-v22.23.3-LICENSE.txt`. Its executable hash is checked against the upstream release. SheetJS 0.20.3 is bundled from the official self-contained release; older component licence texts remain included as provenance. No package manager, dependency download or external SheetJS service is required at runtime.

## Network boundary

All runtime JavaScript, CSS, font, image and audio assets are stored locally. No remote font, analytics, advertising, account, telemetry or payment dependency is included. React's compiled diagnostic strings may contain links to React documentation; those strings are not automatically requested by the application.

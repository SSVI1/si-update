<div align="center">

<img src=".github/assets/AxorinLogo.png" alt="Axorin" width="110">

# Axorin

**A Windows desktop utility for Roblox players.**

Clip recording, server tools, performance tuning, and Robux analytics — running *beside* the game, never inside it.

[![Latest release](https://img.shields.io/github/v/release/SSVI1/si-update?style=for-the-badge&label=latest&color=5865F2)](https://github.com/SSVI1/si-update/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/SSVI1/si-update/total?style=for-the-badge&color=5865F2)](https://github.com/SSVI1/si-update/releases)
[![Platform](https://img.shields.io/badge/Windows-10%20%7C%2011%20(64--bit)-5865F2?style=for-the-badge)](https://axorin.net/download)
[![Discord](https://img.shields.io/badge/Discord-join-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/axorin)

[**Website**](https://axorin.net/) · [Features](https://axorin.net/features) · [Pricing](https://axorin.net/pricing) · [FAQ](https://axorin.net/faq) · [Download](https://axorin.net/download) · [Terms](https://axorin.net/terms)

<br>

<img src=".github/assets/axorin-overview.png" alt="The Axorin dashboard" width="820">

</div>

---

## About this repository

This is the **official Axorin release channel**. Every download and every automatic update is served from here — see [Releases](https://github.com/SSVI1/si-update/releases/latest).

Axorin is a closed-source project, so the application code is not published here. This repository hosts the release packages and the update manifest that the app checks on launch. More on why it's closed source under [Privacy & security](#privacy--security).

---

## What Axorin does

Axorin fills in the gaps Roblox leaves — and adds the conveniences you'd otherwise juggle three separate programs for. It runs as its own Windows app next to the game and reacts to what you type in normal Roblox chat.

| | |
|---|---|
| **Capture** | Rolling-buffer clip recorder (save the play *after* it happens), instant replay, and instant screenshots |
| **Servers & players** | Live server browser with real measured ping, server hopper with strategy presets, player radar, player lookup with a trade-risk read |
| **Performance** | FPS unlocker, per-tweak Boost Mode with measured before/after, render-quality presets, Performance Lab, cache clean, TCP optimize |
| **In-game** | Draggable HUD overlay, in-game notifications, Anti-AFK, recorded movement macros, custom fonts and crosshairs, typing keyboard sounds |
| **Accounts & economy** | Encrypted local account vault with multi-instance launch, Robux transaction analytics, read-only trade watcher |

The full breakdown with screenshots lives at **[axorin.net/features](https://axorin.net/features)**.

---

## Installation

**Requirements** — Windows 10 or 11, 64-bit. Nothing else: the build is self-contained, so there's no .NET runtime to install first.

1. **Download** the latest `Axorin.zip` from [Releases](https://github.com/SSVI1/si-update/releases/latest).
2. **Extract it.** Right-click the zip → *Extract All*. You'll get a folder containing `Axorin.exe`. Put that folder anywhere you like — Axorin runs from where it sits.
3. **Run `Axorin.exe`.** Windows will ask for administrator rights; they're needed for the performance tweaks (power plan, process priority) and the HWID/MAC tools.
4. **Turn on what you want.** Every tool starts off. Launch Roblox and the overlay, capture, and chat commands pick it up automatically.

There is no installer and no account required to start.

### Verifying your download

Axorin isn't code-signed yet, so Windows SmartScreen may warn about an unknown publisher on first run — choose **More info → Run anyway**. If you'd rather verify first, every release publishes a SHA-256 checksum. Compare it in PowerShell:

```powershell
Get-FileHash .\Axorin.zip -Algorithm SHA256
```

Only ever download Axorin from this repository or from [axorin.net/download](https://axorin.net/download). Any other source is not ours.

---

## Automatic updates

Axorin keeps itself up to date, and this repository is what makes that work.

On launch the app reads the update manifest published here and compares it against your installed version. If we've released a newer one, you're prompted to update and Axorin downloads and applies it for you — no reinstalling, no manual re-download. Each update is checksum-verified against the manifest before it's applied, so a corrupted or tampered download is rejected rather than installed.

Automatic updates are included for free and PRO users alike.

---

## Free vs PRO

The core toolkit is free. PRO is a **one-time 500 Robux purchase** — not a subscription — that unlocks the advanced tools.

| Feature | Free | PRO |
|---|:---:|:---:|
| Automatic updates | ✅ | ✅ |
| Dashboard and profile | ✅ | ✅ |
| Logs | Basic | Advanced |
| Screenshots (`/ss`) | ✅ | ✅ |
| Player lookup + trade-risk read | ✅ | ✅ |
| In-game overlay (ping, FPS, server stats) | ✅ | ✅ |
| In-game notifications | ✅ | ✅ |
| Custom fonts & crosshairs | ✅ | ✅ |
| Anti-AFK | ✅ | ✅ |
| Typing keyboard sounds | ✅ | ✅ |
| Smart Movement (record & replay) | ✅ | ✅ |
| Low-End Mode | ✅ | ✅ |
| Instant replay (`/replay`) | ✅ | ✅ |
| Discord Rich Presence | Always on | On or off |
| Roblox account link | ✅ | ✅ |
| Clip recorder | Lower quality, watermarked | 60 fps, clean |
| Account manager | 1 slot | Unlimited |
| AI auto-play | Dumb + Medium | + Smart |
| HWID & MAC tools | Spoof | Spoof + restore |
| Live server browser | — | ✅ |
| Server hopper (`/hop`) | — | ✅ |
| Player radar (Ghost, Snipe, Evade) | — | ✅ |
| Auto-rejoin on crash | — | ✅ |
| Robux Economy | — | ✅ |
| Trade watcher | — | ✅ |
| FPS unlocker | — | ✅ |
| Advanced Boost Mode | — | ✅ |
| Custom render quality | — | ✅ |
| Performance Lab *(beta)* | — | ✅ |
| Cache Clean & TCP Optimize | — | ✅ |

**Getting PRO:** join the [Discord](https://discord.gg/axorin), pay once, and you receive a personal license key. Enter it in the app and every PRO feature unlocks immediately. Keys are personal and non-transferable; see the [Terms](https://axorin.net/terms).

---

## Chat commands

Typed straight into the normal Roblox chat box while Axorin is running. Axorin reacts on your PC — nothing is sent into the Roblox process.

| Command | What it does | |
|---|---|:--:|
| `/ss` | Save a screenshot | Free |
| `/rec30s` | Save the last 30 seconds | Free |
| `/rec5s`, `/rec2m` | Any length, seconds or minutes | Free |
| `/replay` | Watch the last few seconds back, over the game | Free |
| `/lq` | Switch the buffer to low quality | Free |
| `/hq` | 60 fps high-quality buffer | PRO |
| `/stats` | Your profile stats, over the game | Free |
| `/hop` | Fresh server of your current game | PRO |
| `/hop Blox Fruits` | Launch another game by name | PRO |
| `/alts` | Bring your saved accounts into this server | — |
| `/alt bob` | Launch one saved account by name | — |
| `/leave` | Close every account you launched | — |
| `/test` | Check the command pipeline is alive | Free |

---

## Privacy & security

**Why Axorin is closed source.** Keeping the source private lets us control the user experience and stops reskinned copies of Axorin from circulating — copies we can't vouch for and that users would still blame us for. That's the whole reason. There is nothing hidden in the code we're unwilling to talk about: if you have a specific concern, ask in the [Discord](https://discord.gg/axorin) and we'll explain how a feature works, and share the relevant code where it helps.

**What Axorin does not do:**

- It does **not** inject into Roblox or read its memory.
- It does **not** modify anything inside a game.
- It does **not** ask for your Roblox password — ever. Account linking uses a session stored locally on your PC, encrypted with Windows DPAPI, and never uploaded.
- It does **not** track you or spy on you. We're a small project; doing that would end us.

**What we do collect.** Axorin collects a limited set of analytics, used internally to understand how the app is used and where it breaks. It is not sold, not shared with third parties, and not used for anything else. Exactly what's collected — and the retention period after which it's deleted — is documented in the [Terms of Service](https://axorin.net/terms). Read it before you install; it's the authoritative version of this section.

---

## Disclaimer

Axorin is a third-party tool, and like any third-party tool it carries risk — including in-game warnings, bans, or account loss. Axorin avoids injection and memory reading specifically to minimise that risk, and there are **currently zero known bans or warnings** attributed to Axorin, but the risk is never zero. **You use Axorin at your own risk.**

Axorin is an independent project. It is **not** endorsed by, affiliated with, or connected to Roblox Corporation. Roblox is a trademark of Roblox Corporation.

---

## Official channels

These are the only official Axorin channels. Anything else claiming to be Axorin is not us.

| | |
|---|---|
| 🌐 Website | [axorin.net](https://axorin.net/) |
| 💬 Discord | [discord.gg/axorin](https://discord.gg/axorin) |
| ▶️ YouTube | [@Axorin.Roblox](https://www.youtube.com/@Axorin.Roblox) |
| 🎵 TikTok | [@axorin.net](https://www.tiktok.com/@axorin.net) |
| 📦 Releases | [github.com/SSVI1/si-update](https://github.com/SSVI1/si-update/releases) |

---

## Status & support

Axorin is in **active development**, built by a small team who prefer to stay anonymous. Bugs and rough edges are possible — especially in beta and early releases.

Found one? Report it in the [Discord](https://discord.gg/axorin). That's where support, PRO keys, and release announcements live, and it's the fastest way to reach us.

<div align="center">

© 2026 Axorin. All rights reserved. Not endorsed by or affiliated with Roblox Corporation.

</div>

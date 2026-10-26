<div align="center">

<img src="https://axorin.net/assets/AxorinLogo.png" alt="Axorin" width="110">

# Axorin

**A Windows companion app for Roblox players.**

Clips, an in-game overlay, server tools, macros and FPS controls, running *beside* the game, never inside it.

[![Latest release](https://img.shields.io/github/v/release/SSVI1/si-update?style=for-the-badge&label=latest&color=5865F2)](https://github.com/SSVI1/si-update/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/SSVI1/si-update/total?style=for-the-badge&color=5865F2)](https://github.com/SSVI1/si-update/releases)
[![Platform](https://img.shields.io/badge/Windows-10%20%7C%2011%20(64--bit)-5865F2?style=for-the-badge)](https://axorin.net/download)
[![Discord](https://img.shields.io/badge/Discord-join-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/5GwrdNSHxC)

[**Website**](https://axorin.net/) · [Features](https://axorin.net/features) · [Pricing](https://axorin.net/pricing) · [Is it safe?](https://axorin.net/safe) · [FAQ](https://axorin.net/faq) · [Changelog](https://axorin.net/changelog) · [Download](https://axorin.net/download)

</div>

---

## About this repository

This is the **official Axorin release channel**. Every download and every automatic update comes from here.

| File | What it is |
|---|---|
| `Axorin_v<version>.zip` | The download. Get the newest one from [Releases](https://github.com/SSVI1/si-update/releases/latest) |
| `Axorin_v<version>_autoupdate.zip` | The same zip, byte for byte. The updater fetches this copy so installs and updates are counted separately |
| `update_info.xml` | The update manifest Axorin reads on launch: the latest version, its download link and its SHA-256 |

Axorin is closed source, so the application code is not published here. Why, and how you can check it anyway, is under [Privacy & security](#privacy--security).

---

## What Axorin does

Axorin fills in the gaps Roblox leaves, and replaces the handful of separate programs you'd otherwise juggle. It runs as its own Windows app next to the game and reacts to commands you type in normal Roblox chat.

| | |
|---|---|
| **Capture** | Rolling-buffer clip recorder (save the play *after* it happens) on NVIDIA or AMD, instant replay, and screenshots |
| **Servers & players** | Live server browser with ping measured to each datacenter, server hopper, player radar, auto-rejoin on crash, and player lookup |
| **Launching** | Axorin's own launcher with three styles and launch stats, and Play on roblox.com opening through Axorin |
| **Performance** | Frame-rate cap, Boost Mode with measured before/after, render-quality presets, Performance Lab, Low-End Mode, Cache Clean and TCP Optimize |
| **Automation** | AI Mode (GPT-6 or Claude plays from what it sees, on your own API key), a macro builder, an autoclicker of up to 1,000 clicks a second, Smart Movement and Anti-AFK |
| **In-game** | Overlay with live ping and FPS charts, notifications over the game, Discord Rich Presence, typing keyboard sounds, and a tray mode that keeps it all running |
| **Accounts & Robux** | Encrypted account vault with multi-instance launch, Challenges, Robux Economy, Robux Guard spending alerts, and a read-only trade watcher |
| **Your setup** | Cursor Lab crosshair designer, an on-top cursor that can paint out a game's own crosshair (beta), in-game fonts, text and interface size, and HWID & MAC tools |

The full breakdown lives at **[axorin.net/features](https://axorin.net/features)**, and every release's changes are in its [release notes](https://github.com/SSVI1/si-update/releases).

---

## Installation

**Requirements:** Windows 10 or 11 (64-bit) and a Discord account to sign in with. Nothing else to install: the build is self-contained, so there's no .NET runtime to set up first.

1. **Download** `Axorin_v<version>.zip` from [Releases](https://github.com/SSVI1/si-update/releases/latest).
2. **Extract it.** Right-click the zip → *Extract All*. You'll get `Axorin.exe` and `AxorinLauncher.exe`. Keep them together in any folder you like; Axorin runs from where it sits, and `AxorinLauncher.exe` handles Play on roblox.com.
3. **Run `Axorin.exe`.** Windows asks for administrator rights. They're needed for the performance tweaks (power plan, process priority) and the HWID & MAC tools. Roblox, your previous launcher and web links are still started as your normal Windows user, so they never inherit those rights.
4. **Sign in with Discord.** Axorin reads your Discord username and avatar, and never posts, sends messages or joins servers for you. On a PC that's new to Axorin, this also starts your free 7-day PRO trial. Already claimed a PRO key? Choose **I have Pro** and unlock with the key instead.
5. **Turn on what you want.** Switch on the tools you want in the app. Start Roblox and the overlay, capture and chat commands pick it up automatically.

There's no installer and no Axorin account to create.

> [!NOTE]
> Microsoft Defender's cloud protection currently flags the small `AxorinLauncher.exe` helper and may remove it while you extract the zip. Axorin itself still runs; only website joins stop, and the Launcher tab tells you the helper is missing. Every antivirus result, with full hashes, is listed at [axorin.net/safe](https://axorin.net/safe#scans).

### Verifying your download

Axorin isn't code-signed, so Windows SmartScreen shows an unknown-publisher warning on first run. That isn't a virus alert; it appears for every program without a paid certificate. Choose **More info → Run anyway**, or verify the file first: every release lists the zip's SHA-256 in its notes and on the [download page](https://axorin.net/download). Open PowerShell in the folder you saved it to and run:

```powershell
Get-FileHash .\Axorin_v*.zip -Algorithm SHA256
```

Want more than a checksum? [axorin.net/safe](https://axorin.net/safe#check) has five checks you can run yourself with free tools, and the full list of servers Axorin can contact.

Only ever download Axorin from this repository or from [axorin.net/download](https://axorin.net/download). Any other source is not ours.

---

## Automatic updates

Axorin keeps itself up to date, and this repository is what makes that work.

On launch the app reads `update_info.xml` from here and compares it with the version you have. When a newer one is out, Axorin downloads it, checks it against the SHA-256 in the manifest and installs it. No reinstalling, no manual re-download. A corrupted or tampered download fails that check and is never installed.

Updates are required, so everyone runs the latest fixes. They're included for free and PRO users alike.

---

## Free vs PRO

The core toolkit is free. PRO is a **one-time 500 Robux purchase**, not a subscription, and it unlocks the advanced tools.

> [!TIP]
> **Try PRO free for 7 days.** A PC that's new to Axorin gets every PRO tool for a week, starting when you first sign in with Discord. No payment and nothing to cancel. There's one trial per PC and per Discord account, and a PC or account that has had PRO before doesn't get one. When the trial ends the PRO tools lock again; your macros, saved accounts and clips stay, and everything free keeps working.

| Feature | Free | PRO |
|---|:---:|:---:|
| Automatic updates | ✅ | ✅ |
| Dashboard and profile | ✅ | ✅ |
| Logs | Basic | Advanced |
| Launcher and launch stats | ✅ | ✅ |
| Website joins | ✅ | ✅ |
| Challenges | ✅ | ✅ |
| AI Mode *(your own API key)* | ✅ | ✅ |
| Screenshots (`/ss`) | ✅ | ✅ |
| Instant replay (`/replay`) | ✅ | ✅ |
| In-game overlay (ping, FPS, live charts) | ✅ | ✅ |
| In-game notifications | ✅ | ✅ |
| Cursor Lab | ✅ | ✅ |
| In-game fonts & cursor | ✅ | ✅ |
| Display settings | ✅ | ✅ |
| Anti-AFK | ✅ | ✅ |
| Typing keyboard sounds | ✅ | ✅ |
| Smart Movement (record & replay) | ✅ | ✅ |
| Low-End Mode | ✅ | ✅ |
| Roblox account link | ✅ | ✅ |
| Player lookup | Look up anyone | + track & join |
| Discord Rich Presence | Always on | On or off |
| Account manager | 1 slot | Unlimited |
| Clip recorder | Lower quality, watermarked | 60 fps, clean |
| Macro builder | 2 macros, once per press | Unlimited, repeats, logic |
| Autoclicker | ✅ | + burst, spread, colour gate |
| HWID & MAC tools | Spoof | Spoof + restore |
| Live server browser | — | ✅ |
| Server hopper (`/hop`) | — | ✅ |
| Player radar (Ghost, Snipe, Evade & Rejoin) | — | ✅ |
| Auto-rejoin on crash | — | ✅ |
| Robux Economy | — | ✅ |
| Robux Guard | — | ✅ |
| Trade watcher | — | ✅ |
| Frame-rate cap | — | ✅ |
| Advanced Boost Mode | — | ✅ |
| Custom render quality | — | ✅ |
| Performance Lab *(early release)* | — | ✅ |
| Cache Clean & TCP Optimize | — | ✅ |

**Getting PRO:** join the [Discord](https://discord.gg/5GwrdNSHxC), pay 500 Robux once, and you receive a personal license key. Enter it in the app while you're signed in with Discord and every PRO feature unlocks on the spot; from then on the key also works on that PC without a Discord sign-in. A key bought during the trial takes over from it straight away. Finishing every challenge in the Challenges tab earns a free key too. Keys are personal and non-transferable, and purchases are final; see the [Terms](https://axorin.net/terms#pro-sale).

---

## Chat commands

Typed straight into the normal Roblox chat box while Axorin is running. Axorin picks them up on your PC and acts from outside the game; it never reaches inside the Roblox process.

| Command | What it does | |
|---|---|:--:|
| `/ss` | Save a screenshot and copy it to the clipboard | Free |
| `/rec30s` | Save the last 30 seconds | Free |
| `/rec5s`, `/rec2m` | Any length from 5 seconds up to your buffer (2 minutes by default, 3 at most) | Free |
| `/replay` | Watch the last 10 seconds back, over the game | Free |
| `/replay30` | Replay any length up to a minute | Free |
| `/lq` | Switch the buffer to low quality | Free |
| `/hq` | 60 fps high-quality buffer | PRO |
| `/stats` | Your profile stats, over the game | Free |
| `/hop` | Fresh server of your current game | PRO |
| `/hop Blox Fruits` | Join another game by name or place ID | PRO |
| `/alts` | Bring your saved accounts into this server | Free |
| `/alt bob` | Launch one saved account by name | Free |
| `/leave` | Close every account you launched | Free |
| `/axorin` | Post a line about Axorin in chat | Free |
| `/test` | Check commands are working (answers in chat) | Free |

On Free, a saved clip, screenshot or replay also types one short line about Axorin into chat, the same way you would. PRO doesn't.

---

## Privacy & security

**Why Axorin is closed source.** Keeping the source private lets us control the user experience and stops reskinned copies of Axorin from circulating: copies we can't vouch for and that users would still blame us for. That's the whole reason. There is nothing hidden in the code we're unwilling to talk about. If you have a specific concern, ask in the [Discord](https://discord.gg/5GwrdNSHxC) and we'll explain how a feature works, and share the relevant code where it helps.

**How you can check it anyway.** Since v1.7.20 the text inside Axorin isn't encrypted, so any .NET decompiler shows exactly which servers it talks to. [axorin.net/safe](https://axorin.net/safe) lists every one of those servers, and five checks you can run yourself with free tools, each with what you should see if we're telling the truth.

**What Axorin never does:**

- It does **not** inject code into Roblox, or read or write its memory. It isn't a script executor and can't do anything inside a game that the game doesn't already allow.
- It does **not** ask for, see or store your Roblox or Discord password. Account linking uses the session Windows already keeps for you, encrypted on your PC with DPAPI. It is never uploaded and only ever goes to Roblox.
- It does **not** read your browser's saved passwords or cookies.
- It does **not** sell your data or use it for advertising.

**What leaves your PC.** Only what licensing, stopping abuse and improving the app need:

- a Desktop ID derived from your hardware, your IP address, your machine name and the app version;
- the Discord account you sign in with and any Roblox account you link (username and ID);
- which tab you have open, the last feature you used, and your progress in Challenges;
- your answer when the app asks how you heard about Axorin;
- license checks (keys are stored only as one-way hashes);
- if you use AI Mode: your 0 to 10 rating of each run, the run log and up to 12 of the screenshots the AI saw.

Your Roblox session, passwords, clips, `/ss` screenshots, local logs and AI provider keys are never sent to us, and your in-game chats aren't collected (an AI Mode screenshot does show whatever was on screen). AI Mode's screenshots go to the provider you chose (OpenAI or Anthropic), on your own key. Exactly what's collected, and how long it's kept, is in the [Terms of Service](https://axorin.net/terms#data). Read it before you install; it's the authoritative version of this section.

**Leaving cleanly.** *Settings → Privacy & Data → Delete all my data* erases what Axorin stored on your PC (only the device ID your license is tied to stays) and puts back what it changed: in-game fonts, cursor, render flags, every Boost Mode change to Windows, and website-join handling. Deleting the folder on its own doesn't do that, so use the button first.

---

## Disclaimer

Axorin is a third-party tool, and like any third-party tool it carries risk, including in-game warnings, bans or account loss. Axorin avoids injection and memory reading specifically to minimise that risk, but Roblox and individual games set their own rules and can change them, so the risk is never zero. **You use Axorin at your own risk.**

Axorin is an independent project. It is **not** endorsed by, affiliated with, or connected to Roblox Corporation. Roblox is a trademark of Roblox Corporation.

---

## Official channels

These are the only official Axorin channels. Anything else claiming to be Axorin is not us.

| | |
|---|---|
| 🌐 Website | [axorin.net](https://axorin.net/) |
| 💬 Discord | [discord.gg/5GwrdNSHxC](https://discord.gg/5GwrdNSHxC) |
| ▶️ YouTube | [@Axorin.Roblox](https://www.youtube.com/@Axorin.Roblox) |
| 🎵 TikTok | [@axorin.net](https://www.tiktok.com/@axorin.net) |
| 📦 Releases | [github.com/SSVI1/si-update](https://github.com/SSVI1/si-update/releases) |

---

## Support & contact

Axorin is in **active development**, built by a small team who prefer to stay anonymous. Bugs and rough edges are possible, especially in features marked beta or early release.

- **Something not working?** Check [axorin.net/status](https://axorin.net/status), then ask in the [Discord](https://discord.gg/5GwrdNSHxC). Help, bug reports, license problems and security concerns all go there.
- **Ideas or feedback?** Send them at [axorin.net/feedback](https://axorin.net/feedback). It's anonymous, so we read everything but can't reply.
- **What changed?** Each release's notes, or [axorin.net/changelog](https://axorin.net/changelog).
- **Promotions, sponsorships or creator collabs?** Email [Axorin.net@proton.me](mailto:Axorin.net@proton.me). That inbox is for business only, so please don't send support questions, bug reports or feedback there.

The Discord is where support, PRO keys and release announcements live, and it's the fastest way to reach us.

<div align="center">

© 2026 Axorin. All rights reserved. Not endorsed by or affiliated with Roblox Corporation.

</div>

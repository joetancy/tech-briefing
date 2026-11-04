---
layout: post
categories: [tech-briefing]
date: 2026-11-05 07:30:00 +0800
title: White House proxies, Ripple-65B and Go's new JSON API
---

Prepared: 7:30 AM SGT

## Hacker News Top 10

Snapshot of the live Hacker News front page, Thursday 5 November 2026, ~7:26 AM SGT, in ranking order.

### 1. Residential proxies detected on White House network

Layer3 Intel's new Residential Proxy Observatory recorded 236 exits through the White House network (AS2650, Executive Office of the President) between 5 October and 3 November 2026, via 6 addresses and 28 proxy services. The evening-heavy pattern points to a person on the network whose device carries an infected proxy SDK, rather than guest Wi-Fi — and poorly secured proxy SDKs have previously enabled internal access and lateral movement.

- [Discussion](https://news.ycombinator.com/item?id=50371246) | [Source](https://layer3intel.com/blog/residential-proxies-white-house-network)

### 2. Ripple-65B Preview: U.S. Open-Weight SOTA on Agentic Coding

Ricursive Intelligence released Ripple-65B Preview, a dense 65B model pretrained on 12 trillion tokens with up to 1M context, claiming U.S. open-weight state of the art on agentic coding at 80.52 on TerminalBench 2.1. The lab says it trained the model from scratch for $32M — about a tenth of the previous open-weight SOTA cost — and that its small parameter envelope lets it run efficiently on local devices such as Nvidia DGX Spark.

- [Discussion](https://news.ycombinator.com/item?id=50369925) | [Source](https://www.ricursive.com/ripple)

### 3. Insects don't swarm at LED lights

A naturalist's note explains a familiar observation: insects swarm old incandescent lights but largely ignore LEDs, because insects navigate by ultraviolet light that incandescents emit and LEDs mostly do not. A 2016 University of Bristol field experiment found LEDs attracted significantly fewer insects than incandescent or compact fluorescent lights, with no meaningful difference between cool-white and warm-white LEDs.

- [Discussion](https://news.ycombinator.com/item?id=50370610) | [Source](https://www.birdsoutsidemywindow.org/2026/11/03/insects-dont-swarm-at-led-lights/)

### 4. AI is forcing us to pay off 40 years of technical debt

IEEE Spectrum argues PHP2Shell is a warning: an AI-assisted audit found a way to turn a long-dismissed PHP out-of-memory bug, first reported in 2024, into arbitrary code execution on servers running sites including WordPress and Drupal. The piece's core point is asymmetry — AI is rapidly making bug-finding cheaper while patching still requires proving every attack path is closed without breaking functionality — and that decades of legacy code now face the same treatment.

- [Discussion](https://news.ycombinator.com/item?id=50364336) | [Source](https://spectrum.ieee.org/ai-in-cybersecurity-php2shell-vulnerability)

### 5. Hacking the Xbox 360 Hypervisor Part 3: Bad Update Improvements

Ryan Miceli's third post in the series describes how the Bad Update exploit went from taking about 20 minutes at roughly 30% success to near-instantaneous at near-100% success. The gains come from a new Rock Band Blitz demo entry point (no Tony Hawk's American Wasteland disc needed, files copied to USB) plus race-condition optimisations: a larger ciphertext hash table, cache flushing, and thread scheduling giving the overwrite thread 31 of 32 dispatch slots.

- [Discussion](https://news.ycombinator.com/item?id=50372164) | [Source](https://icode4.coffee/?p=1746)

### 6. A new Go API for JSON

Go 1.27 ships stable `encoding/json/v2` and `encoding/json/jsontext`, replacing the long-standing `encoding/json` API that could not be fixed within Go 1 compatibility. The new packages fix safety defaults — rejecting invalid UTF-8 and duplicate object member names — and add true streaming via `MarshalJSONTo`/`UnmarshalJSONFrom`, plus options as first-class arguments to `Marshal`/`Unmarshal`.

- [Discussion](https://news.ycombinator.com/item?id=50369106) | [Source](https://go.dev/blog/jsonv2)

### 7. Qualcomm Cloud AI 100 Ultra – 150W AI Accelerator Card with 128GB at 548GB/s

Qualcomm's Cloud AI 100 Ultra is a 150W datacentre inference card pairing 128GB of memory with 548GB/s of bandwidth, aimed at running large models efficiently in the datacentre. It lands in a week where inference economics — cost per token, memory bandwidth, and power envelope — are the headline competition, from open-weight models to provable-inference research.

- [Discussion](https://news.ycombinator.com/item?id=50370654) | [Source](https://www.qualcomm.com/data-center/products/cloud-ai-100-ultra)

### 8. Progress on provable inference for large language models

Anthropic's FlashProve is an open-source prototype using zkSNARKs to prove a response really came from the committed model, without revealing its weights. For Llama 4 Maverick (400B MoE, 4-bit), a single H100 generates proofs at around 110 tokens/second with ~19MB proofs per 1,024-token request — 70–95x the GPU time of plain vLLM inference — with code, Lean formal proofs, and a technical report released under Apache 2.0.

- [Discussion](https://news.ycombinator.com/item?id=50368626) | [Source](https://www.anthropic.com/research/provable-inference)

### 9. Show HN: After a decade of reversing, I got co-op working in DOS Wing Commander

After ten years of reverse engineering, the author has co-operative multiplayer working in the original DOS Wing Commander, with the project page at the link below. It is a preservation-through-play story: keeping a 1990 classic playable in a way its original release never offered, rather than through a remake or re-release.

- [Discussion](https://news.ycombinator.com/item?id=50369895) | [Source](https://fireflyk64.github.io/wcmulti/)

### 10. Nvidia RTX Spark encrypted firmware slows inference speed to 35% on Linux

Testing on an MSI Prestige N16 Flip AI Plus finds native Linux inference far slower than Windows or WSL: GPT-OSS-120B runs at 13.9 tokens/second natively versus 65.4 on Windows, because the encrypted firmware power table is only decrypted by Windows-only Nvidia tooling, locking the plugged-in GPU to ~780MHz instead of ~2.2GHz. Curiously, unplugged Linux reaches ~1,800MHz — so the article recommends WSL as the practical route until Nvidia brings equivalent power management to its Linux driver.

- [Discussion](https://news.ycombinator.com/item?id=50362905) | [Source](https://www.mindstudio.ai/blog/linux-nvidia-rtx-spark-laptop)

## AI

- **Ripple-65B** (see #2) and **Anthropic's FlashProve** (see #8) frame the week's two AI directions: cheaper, smaller open-weight models for agentic coding, and cryptographic proof that a served model is the one claimed. ([Ricursive](https://www.ricursive.com/ripple), [Anthropic](https://www.anthropic.com/research/provable-inference))
- **Qualcomm Cloud AI 100 Ultra** (see #7) pushes inference hardware toward high memory capacity at a modest 150W envelope. ([Qualcomm](https://www.qualcomm.com/data-center/products/cloud-ai-100-ultra))

## Frontend and developer tooling

- **Go 1.27's `encoding/json/v2`** (see #6) is the most directly useful developer release of the day: stricter, safer JSON defaults and real streaming matter for any frontend or API service exchanging JSON at scale. ([Go blog](https://go.dev/blog/jsonv2))

## Emulation, retro games, preservation, ROM hacking, FPGA, ports, and static recompilation

- **Xbox 360 hypervisor** (see #5) and **DOS Wing Commander co-op** (see #9) are today's homebrew highlights — exploit refinement on 2005 hardware, and a decade-long reversing project reaching playable co-op.
- **Power Moon Recomp**, an unofficial native PC port of Super Mario Odyssey via static recompilation, is reported playable start to finish at up to 4K/60fps on Windows, Linux, and macOS, with players supplying their own copy of the game. ([TweakTown](https://www.tweaktown.com/news/114465/super-mario-odyssey-native-pc-port-available-now-playable-from-start-to-finish-in-4k-at-60-fps/index.html))
- **MediEvil Recomp hit 1.0** after its October beta, with stability, analogue, audio, and FMV fixes plus a Mod Hub and asset-pack editor — built without generative AI tools, per its developers. ([Time Extension](https://www.timeextension.com/news/2026/11/we-have-the-skills-to-bring-love-to-these-old-games-after-last-months-beta-medievils-ai-free-recomp-hits-version-1-0))
- **Brawl Recompiled** (Super Smash Bros. Brawl, Wii) now runs natively on PC at up to 4K/240fps with Project+ mod support and online rooms, via the WiiCompiled toolchain. ([Pro Gamer](https://pro-gamer.gg/super-smash-bros-brawl-native-pc-port-4k-240-fps-brawl-recompiled-project-plus-online/))
- **FPGA roundup:** Jotego released NARC, Arbalester, and Meta Fox arcade cores alongside CPS-3 validation work, and French engineer Thomas Sanfourche's unreleased SGBC is an FPGA Game Boy console that plays original cartridges, copies ROMs to microSD, and outputs 1080p over HDMI. ([Pants Pants Revolution](https://pantspantsrevolution.com/october-31st-week-in-review/), [Mezha](https://mezha.net/eng/news/mezha-ebc31d887942d04d49936e9e_sgbc_is_an/))

## Cybersecurity

- **White House network proxies** (see #1) lead the day, alongside the **PHP2Shell** fallout (see #4): PAN-OS systems were compromised by chaining PHP2Shell RCE with the Fragnesia Linux privilege-escalation flaw, and Singapore's CSA issued its own PHP2Shell alert. ([F5 Labs](https://www.f5.com/labs/articles/weekly-threat-bulletin-november-4th-2026))
- **Binance's $6.3B theft**, attributed by the FBI to North Korea's TraderTraitor via a fake job interview, remains the week's largest incident. ([CVETodo](https://cvetodo.com/threat-report/sg))
- **Patch now:** CISA added WordPress Core CVE-2026-119977 (due 6 Nov) and Apple CVE-2024-27834 (due 18 Nov, linked to an APT29 campaign against unpatched iPhones) to KEV; GitLab CVE-2026-97229 (CVSS 10), Ivanti Connect Secure flaws, a Zyxel GS1900 zero-day (CVE-2026-107441, 996 switches), and an APT package-manager flaw (CVE-2026-109518) are also active. Google's November Android bulletin fixes 216 bugs and Chrome 157 fixes 213. ([Carthage Electronics](https://carthageelectronics.com/november-4-2026-cve-threat-brief/), [DualScope](https://www.dualscope.io/daily/2026-11-03))

## AWS

- No major AWS development surfaced in today's sources; nothing to flag beyond the inference-hardware and AI-model news above.

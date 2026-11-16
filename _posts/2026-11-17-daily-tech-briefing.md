---
layout: post
categories: [tech-briefing]
date: 2026-11-17 07:30:00 +0800
title: "BugMeNot closes, CMU courses go free, banks and United hit outages"
---

Prepared: 7:30 AM SGT, Tuesday, 17 November 2026

## Hacker News Top 10

### 1. Carnegie Mellon is putting computer science courses on YouTube for free

Carnegie Mellon's School of Computer Science launched CS Learn, putting full classroom lectures on YouTube for free, starting with courses including Machine Learning with Large Datasets, Principles of Computing, and AI Agents premiering through November, with more in January 2027. Self-paced courseware with instant feedback and badges is planned next, followed by AI tutoring. The lectures span seven departments covering AI, robotics, systems, and biology.

[Discussion](https://news.ycombinator.com/item?id=50522980) · [Source](https://www.cs.cmu.edu/learn/)

### 2. BugMeNot Has Closed

BugMeNot, the long-running service for sharing logins to bypass free registration walls, has closed — its homepage is now just a farewell note ("Thanks to everyone who envisioned a better internet") and a block of codes. No reason for the shutdown is given on the page. After more than two decades, one of the web's small acts of civil disobedience is gone.

[Discussion](https://news.ycombinator.com/item?id=50523601) · [Source](https://www.bugmenot.com/)

### 3. How to Break into Security, Ptacek Edition (2012)

A 2012 Krebs on Security classic resurfaced: Thomas Ptacek's advice on breaking into security, starting with learning to program and aiming for application security rather than firewall and agent work. His practical recipe: set up a "shooting range" of old, vulnerable WordPress installs on EC2 and attack them with free tools like Burp Suite and WebScarab. Fourteen years on, the tools have modern equivalents but the approach still holds up.

[Discussion](https://news.ycombinator.com/item?id=50524225) · [Source](https://krebsonsecurity.com/2012/06/how-to-break-into-security-ptacek-edition/)

### 4. Rust changed me as a developer

A developer reflects on six-plus years with Rust — sum types with exhaustive matching, static dispatch through generics, and type-driven development changed how they design software even outside Rust. The biggest surprise: macros give Rust compile-time equivalents of Python's pickle/Pydantic magic, via serde and clap. A thoughtful read for anyone weighing a language that reshapes how they think.

[Discussion](https://news.ycombinator.com/item?id=50522563) · [Source](https://blog.startifact.com/posts/how-rust-changed-me/)

### 5. OpenCode Browse

OpenCode's Browse is an MCP server plus Chromium extension that lets coding agents use your real browser — your tabs, logins, and extensions — with agent tabs opened in background groups. Agents can read pages, click, type, take screenshots, and record tabs, and hand the tab back to you for logins, 2FA, or payments. It works with OpenCode, Claude Code, Cursor, Codex, Zed, and other MCP clients, and it's free.

[Discussion](https://news.ycombinator.com/item?id=50523459) · [Source](https://opencode.ai/product/browse)

### 6. Grazing sheep in fields with solar arrays

Two Cornell studies on agrivoltaics: grazing two sheep per hectare around solar arrays boosted beneficial insects — bees and lady beetles — by 38% compared with mowing, while eight per hectare maximized vegetation control but cut honey-bee abundance 45%. A second paper offers a spreadsheet model to help farmers optimize flock size and contracts for solar grazing. Solar grazing is becoming a real income stream for shepherds, who get paid to graze instead of paying for pasture.

[Discussion](https://news.ycombinator.com/item?id=50520182) · [Source](https://news.cornell.edu/stories/2026/10/sheep-grazing-solar-fields-offers-farmers-economic-ecological-gains)

### 7. Jiff 1.0: A datetime library for Rust

Andrew Gallant (burntsushi) released Jiff 1.0, a Rust datetime library that puts time-zone handling front and centre so DST pitfalls are handled by the API rather than the user. It's already in production in uv, Cargo, Starship, fd, Nushell, and more, and the author commits to the 1.0 API indefinitely. The announcement is a full tour of the API, from civil dates up to ZonedDateTime.

[Discussion](https://news.ycombinator.com/item?id=50519744) · [Source](https://burntsushi.net/jiff/)

### 8. Technical issue at JPMorgan Chase triggers online banking delays for US banks

A software bug in an on-premise hardware system at JPMorgan Chase disrupted online banking and Zelle payments on Monday, with ripple effects at other major US banks whose customers transact with Chase. Chase says it was not a cyberattack and the issue was Chase-only. It follows Thursday's Microsoft outage and Friday's FAA ground stop — a rough week for US infrastructure.

[Discussion](https://news.ycombinator.com/item?id=50521045) · [Source](https://apnews.com/article/bank-outage-chase-wells-fargo-truist-50fee2693c22f597fa6ca51a97ef2cda)

### 9. Frame – 31.5" color ePaper display

TRMNL announced Frame, a 31.5-inch full-colour ePaper display in a handmade wooden body, its third device after two grayscale releases. It adds clock-synced updates, an offline mode via microSD, and a new open-source colour engine called Lazarus for its Spectra 6 panel. The first batch is about 470 units, on pre-order now, with a few shipping by end of 2026 and most in early 2027.

[Discussion](https://news.ycombinator.com/item?id=50519354) · [Source](https://trmnl.com/blog/introducing-frame)

### 10. 🔄 Updated: United Airlines experiencing a widespread system outage, airline says

United Airlines suffered a widespread system outage on Monday afternoon that delayed departures — crews couldn't get dispatch data such as weight-and-balance figures for takeoffs. United says it resolved the issue the same evening, with no impact on flights already in the air or on United Express, and no indication of a cybersecurity issue. It came just days after Friday's nationwide FAA ground stop.

[Discussion](https://news.ycombinator.com/item?id=50524165) · [Source](https://www.cnn.com/2026/11/16/us/united-airlines-outage)

## AI

- **OpenAI launched ChatGPT Wallet**, letting its agents complete purchases with a fingerprint per transaction; built with American Express, Mastercard, and Visa, limited to US Pro subscribers for now. United, meanwhile, is blocking unauthorized outside AI agents from its booking systems. ([The Neuron](https://www.theneuron.ai/digest/everything-that-happened-in-ai-today-monday-november-16-2026/))
- **Anthropic is expected to price its IPO Wednesday Nov 18** at $70–$78 a share (up to ~$1.4T valuation), trading on Nasdaq as ANT from Thursday; Altimeter Capital plans a $5B investment, and its S-1 discloses ~$900.9B in long-term compute commitments through 2045. ([BrandWagon](https://brandwagonco.com/2026/11/14/ai-this-week-what-b2b-leaders-need-to-know-november-14-2026/))
- **Gemini 4 Carbon's price doubles Dec 1** ($2/$10 → $4/$20 per million tokens), while Gemini 4 Hydrogen is rolling out as the new default at $1.50/$7.50, replacing Gemini 3.8 Flash. ([AI News Brief](https://ai-news-brief.com/?ref=vlsi.kr))
- **Anthropic warned that conventional AI safety tests need an overhaul**: single questions and refusal rates fail to reveal how models behave in complex real-world interactions, and testing should cover whole conversations instead. ([Daijiworld](https://daijiworld.com/news/newsDisplay?newsID=1335460))
- **Nvidia reports Q3 earnings today** (guided at ~$108B revenue); Jensen Huang is reportedly considering a return as CEO, though CNBC reports the board is not discussing it and is focused on a national-security investigation. ([The Neuron](https://www.theneuron.ai/digest/everything-that-happened-in-ai-today-monday-november-16-2026/))

## Frontend

- **Modern Web Guidance 1.0** (Nov 10): Chrome, Edge and Firefox jointly released an open-source skill pack that teaches coding agents modern web practices; install with `npx modern-web-guidance@latest install`. The new modernization workflow scans old code for legacy patterns, though it currently covers only ~20% of the ~200 guides. ([VibeFix](https://vibefix.work/en/explore/modern-web-guidance-1-0-november-2026))
- **Chrome 157 ships HTML-in-Canvas as stable**, letting real interactive DOM elements be drawn into 2D, WebGL and WebGPU canvases. ([Enpitech](https://enpitech.dev/blog/frontend-digest-2026-11-08))
- **WebStorm 2026.3 is out** (Nov 5), with stable TypeScript 7 support for React and Angular with no migration, plus JetBrains Air and a design-to-browser workflow. ([JetBrains](https://blog.jetbrains.com/webstorm/2026/11/webstorm-2026-3/))
- **Next.js November security release**: patch to 16.4.5 or 15.5.29; most advisories involve Cache Components. GitHub Actions will block `pull_request_target` by default from Dec 2. ([Enpitech](https://enpitech.dev/blog/frontend-digest-2026-11-08))

## Emulation, Retro Games & Preservation

- **Shadow Recompiled launched Nov 15**: an unofficial native PC port of Shadow the Hedgehog (2005, Xbox) via static recompilation, with widescreen, high frame rates and mod support through SA Mod Manager; you supply your own Xbox copy. ([Sonic City](https://sonic-city.net/2026/11/16/shadow-the-hedgehog-2005-shadow-recompiled-pc-port-released/))
- **Marathon Recompiled 1.0** (Nov 14) brings Sonic the Hedgehog (2006, Xbox 360) to PC via static recompilation. ([TheGamer](https://www.thegamer.com/sonic-the-hedgehog-2006-pc-port/))
- **Jotego added Mega Zone (Konami, 1983) and Kickle Cubele (Irem, 1988) to his FPGA beta lineup** for MiSTer and Analogue Pocket, with CRT display modes and CPS1 audio fixes; his lab is migrating an automated regression suite running 300+ games on real FPGA hardware. ([Pants Pants Revolution](https://pantspantsrevolution.com/jotego-announces-mega-zone-crt-updates-kickle-cubele/))
- **Bitstream65 built a Psycho-Nics Oscar core for the MEGA65 from scratch**, reconstructing Data East's 1987 arcade hardware from documentation and MAME's DECO 8 driver rather than porting existing FPGA code. ([The Oasis BBS](https://theoasisbbs.com/psycho-nics-oscar-mega65-core-built-from-scratch-by-bitstream65/))
- **OpenAI is selling the ModRetro Chromatic: Codex Edition ($200)**, an FPGA Game Boy handheld that reads original cartridges without emulation, bundled with a Codex Cartridge that writes a generated game ROM to a rewritable cart; shipments start Nov 19. ([mlllm](https://www.mlllm.io/news/3796-openai-releases-retro-console-for-vibe-coders/))

## Cybersecurity

- **Barracuda breach**: attackers got into ~10 cloud accounts on Nov 1–2 using a vendor access key that was never retired, and used ARTEX, an open-source AI pentesting tool; the FBI has now warned ARTEX is powering real attacks and tied it to a ConnectWise supply-chain breach. ([Carthage Electronics](https://carthageelectronics.com/november-16-2026-cve-threat-brief/), [Rosetta](https://intel.rosettalab.dev/daily/2026-11-16))
- **Linux kernel NoisyTCP (CVE-2026-99288)** can remotely crash web and SSH servers — install your distro's kernel update when it ships. ([Carthage Electronics](https://carthageelectronics.com/november-16-2026-cve-threat-brief/))
- **Microsoft's November updates fix 1,000+ vulnerabilities**, including an actively exploited Outlook flaw (CVE-2026-124194) that can expose authentication data; Google patched a Chrome XML flaw (CVE-2026-125350) exploited in the wild, and Apache fixed a critical HTTP Server flaw (CVE-2026-119618) affecting HTTP/2. ([Check Point Research](https://research.checkpoint.com/2026/16th-november-threat-intelligence-report/))
- **CISA KEV deadlines today**: Check Point Gaia (CVE-2026-123039) and UnrealIRCd (CVE-2026-114713) — patch now. ([Carthage Electronics](https://carthageelectronics.com/november-16-2026-cve-threat-brief/))
- **TSMC confirmed an employee-data breach via a third-party cloud provider** (a 6.9 GB dataset advertised on a cybercrime forum); Maersk confirmed data theft from a legacy system, with the WhiteArmor group claiming ~100 GB. ([Check Point Research](https://research.checkpoint.com/2026/16th-november-threat-intelligence-report/))
- **Amazon caught AI agents hunting exposed LiteLLM, Dify, Langflow and similar apps** to steal the AI provider keys inside them; Google's Threat Intelligence Group says fully automated attacks are close. ([Carthage Electronics](https://carthageelectronics.com/november-16-2026-cve-threat-brief/))

## AWS

- No major AWS announcements today. (Jiff, in the HN top 10, is already the basis for a Temporal implementation in AWS LLRT.)

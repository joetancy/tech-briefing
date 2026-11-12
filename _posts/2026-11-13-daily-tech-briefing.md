---
layout: post
categories: [tech-briefing]
date: 2026-11-13 07:30:00 +0800
title: "Huang resigns, Rust 1.100, and Gemini 4 Hydrogen"
---

Prepared: 7:30 AM SGT

## Hacker News Top 10

### 1. Jensen Huang resigns

Nvidia co-founder and CEO Jensen Huang has resigned with immediate effect after 33 years at the helm, following a board investigation into whether he was targeted by a foreign intelligence operation and reports of two extramarital affairs — one with Alice Huang, a former executive at Singapore-based Nvidia customer Megaspeed whom US officials suspect of working for Chinese intelligence, and another with Nvidia's vice president of healthcare, Kimberly Powell. CFO Colette Kress steps in as interim CEO while the board searches for a permanent successor, and longtime director Harvey C. Jones becomes Nvidia's first board chair. Nvidia shares fell more than 12% on the news, and the board says it has no reason to believe Nvidia secrets or US national security were compromised — but the investigation continues, days before Nvidia's November 17 earnings.

[Discussion](https://news.ycombinator.com/item?id=50467087) · [Source](https://apnews.com/article/nvidia-megaspeed-china-singapore-huang-5403f152a601cf82ce939f1d24fffa0f)

### 2. Rust 1.100

After ten years and five failed stabilization attempts, the never type `!` is finally stable in Rust 1.100.0 and can now be named anywhere, with `Infallible` becoming an alias for it. The release also stabilizes the core `Allocator` API for custom allocators with `Vec` and `Box`, a `DropGuard` helper that runs a closure on every exit path, and `conjure_zst` for creating zero-sized types. Cargo gains unused-dependency warnings and a min-publish-age option that holds back freshly published crate versions as a supply-chain cooldown. One breaking change to watch: the never-type fallback changes from `()` to `!` in pre-2024 editions.

[Discussion](https://news.ycombinator.com/item?id=50472038) · [Source](https://blog.rust-lang.org/2026/11/12/Rust-1.100.0/)

### 3. Gemini 4 Hydrogen and Orchestrator

Google has launched Gemini 4 Hydrogen, a fast model aimed at coding and agentic workflows, priced at $1.50 per million input tokens and $7.50 per million output tokens, available across AI Studio, the Gemini API, the Gemini app and Search, and in Antigravity for paid Pro and Ultra subscribers. Alongside it, Google's Antigravity IDE ships Orchestrator, a tool for coordinating multiple coding agents on the same task. The model is already showing up in Cursor as well.

[Discussion](https://news.ycombinator.com/item?id=50472260) · [Source](https://antigravity.google/blog/gemini-4-hydrogen-in-google-antigravity/)

### 4. 🆕 New: Foundation Models framework

Apple's Foundation Models framework is a native Swift API for building LLM features into apps, giving access to the on-device model behind Apple Intelligence and to Private Cloud Compute, with guided generation, tool calling and image understanding built in. It now extends to server models such as Claude and Gemini through the same API, and adds Dynamic Profiles for swapping model, tools and instructions mid-session, an Evaluations framework for testing prompts, a new `fm` command-line tool in macOS 27, and a Python SDK. Developers in the App Store Small Business Program with under two million first-time downloads get Private Cloud Compute access at no cloud API cost.

[Discussion](https://news.ycombinator.com/item?id=50474361) · [Source](https://developer.apple.com/foundation-models-framework/)

### 5. Dwarf planet candidate appears which takes roughly 280 years to orbit our sun

Astronomers using the Vera C. Rubin Observatory in Chile have spotted 2026 ED138, a trans-Neptunian object about 46 times farther from the Sun than Earth that takes roughly 281 years to complete one orbit, on a plane tilted about 25 degrees — likely nudged by gravitational interactions with Neptune. Estimated at 600–1,500 km across, it is probably round enough to qualify as a dwarf planet, which would make it only the sixth officially recognized, but infrared observations are still needed to confirm its size. The object was announced on October 27 and has since been traced in archive images back to 1954.

[Discussion](https://news.ycombinator.com/item?id=50472490) · [Source](https://www.smithsonianmag.com/smart-news/astronomers-found-a-mysterious-object-orbiting-far-beyond-pluto-it-could-be-a-new-dwarf-planet-hidden-in-our-solar-system-180989857/)

### 6. Show HN: My $300 embroidery machine needed a subscription, so I built my own app

After buying a $300 embroidery machine that required a subscription to actually use, the author built Zigzag, their own open-source app to drive it instead. The repo is on GitHub, and the thread is a good snapshot of subscription fatigue pushing people to build DIY replacements for hardware they already own.

[Discussion](https://news.ycombinator.com/item?id=50470488) · [Source](https://github.com/simpsoka/zigzag)

### 7. AI is turning Apple's app review process into a nightmare for synth developers

AI-vibe-coded apps are flooding the App Store — an estimated 10–20 new iOS music apps arrive every day — and Apple's review process is buckling, with developers reporting waits of weeks instead of the usual 24–48 hours. Worse, developers say automated AI reviewers are hallucinating rejections: Unfiltered Audio's Sinusoidal Run Rhythm was rejected four times, once over a hallucinated licensing requirement for a made-up audio technology, while new developer Marek Dendes has had his CRUX Synth rejected four times as "design spam" with no human response to appeals. For small developers whose livelihood depends on a release, the review queue has become a dead end.

[Discussion](https://news.ycombinator.com/item?id=50474311) · [Source](https://synthanatomy.com/2026/11/ai-is-turning-apples-app-review-process-into-a-nightmare-for-developers.html)

### 8. Service degradation on Microsoft 365

Microsoft has acknowledged service degradation affecting Microsoft 365, with its status page as the source of record while the incident is investigated. The HN thread is tracking the outage as it develops, including which services are affected and user reports of disruption.

[Discussion](https://news.ycombinator.com/item?id=50471731) · [Source](https://status.cloud.microsoft/)

### 9. 22-Year-Old PostgreSQL Bug Turned into Remote Code Execution

Researcher Mehmet Ince turned a 22-year-old PostgreSQL type-confusion primitive into remote code execution (CVE-2026-6460), in the third part of his "Systemic Risks in the Managed PostgreSQL Industry" series. The trick: prepare a query using a composite type, change one of its fields' types before execution, and PostgreSQL reads the stored value back under the wrong type — a TOCTOU-style confusion that yields reliable memory corruption. He got there by studying how PostgreSQL's generic `Datum` carrier trusts the type metadata around it, working through the internals question by question with an AI agent as tutor.

[Discussion](https://news.ycombinator.com/item?id=50471761) · [Source](https://mehmetince.net/part-3-6-how-i-ended-up-turning-a-22-year-old-postgresql-type-confusion-primitive-into-rce-cve-2026-6460/)

### 10. I'm making LLMs work on small and old devices

A project to get large language models running on small and old devices, where memory and compute are tight — the repo is `smolmaxxing` on GitHub. The thread discusses what it takes to squeeze usable LLM inference onto constrained and ageing hardware instead of requiring a modern GPU.

[Discussion](https://news.ycombinator.com/item?id=50468888) · [Source](https://github.com/hyperionaidev/smolmaxxing/)

## AI

- **Anthropic's IPO roadshow is underway.** Anthropic is offering 825 million shares at $70–$78 each and has applied to list on Nasdaq under the ticker ANT, with pricing expected November 18 and trading November 19. At the top of the range that implies a valuation of up to about $1.4 trillion, down from earlier $2 trillion discussions, alongside a $26 billion strategic private placement from investors including Google, Nvidia, AMD, Microsoft and TSMC. A second S-1 amendment disclosed that Anthropic has crossed the threshold in its own Responsible Scaling Policy — AI sharply accelerating AI research — triggering stronger safety checks. ([Anthropic](https://www.anthropic.com/news/roadshow-launch))
- **Gemini 4 Carbon is now generally available** to paid API developers, enterprises and Google AI Ultra subscribers, after two weeks limited to vetted security teams. Google also previewed `/swarm`, a tool for coordinating multiple coding agents. ([Google](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-4-carbon-now-available/))
- **DeepMind shipped Gemini Robotics 2.5**, a next-generation vision-language-action model with self-improvement that improved success rates 30–100% across 200 tasks and hit 96% in a real Mercedes-Benz factory test. DeepMind also introduced **AlphaProof Code**, which used AI agents to generate ~6.5 million lines of Lean proofs in four weeks and formally verify the machine code of Signal's encryption protocol, catching two known historical bugs.
- **GPT-6.2 remains a rumor.** Posts show `gpt-6.2-astra` references in the Codex repo, Azure and Google Cloud quota pages, but OpenAI has confirmed nothing.
- **United Airlines is restricting personal AI agents** from booking flights on its platforms, citing account security, unintended purchases and safety rules.

## Frontend

- **Chrome 157 ships HTML-in-Canvas as stable** after an origin trial, letting real interactive DOM elements be drawn into 2D, WebGL and WebGPU canvases, with DevTools support.
- **Discord is rebuilding its client in Rust**, leaving Electron and React Native behind.
- **Patch Next.js**: the November security release (16.4.5 / 15.5.29, November 3) covers mostly Cache Components advisories — upgrade if you run Cache Components.
- **Vercel is folding the Next.js Data Cache into Runtime Cache** and will bill `fetch` cache and `unstable_cache` reads/writes; Hobby teams migrate November 29.
- **WebStorm 2026.3** brings JetBrains Air into the IDE plus Figma Connect, Storybook Connect and Chrome DevTools Connect, so agents can work the design-to-browser loop with stable TypeScript 7 support.
- **Figma now runs coded prototypes directly on the design canvas** (shipped November 1), with Weave agents publishing tools inside an organization's workspace — the design handoff is dissolving into code.

## Emulation, Retro Games & Preservation

- **Nintendo's latest GitHub DMCA sweep wiped roughly 217 Switch-related repositories.** Four notices filed November 6 targeted the Yuzu and Citron Neo emulators (Citron Neo alone lost 71 repos) and — for the first time — firmware for Picofly and other Switch modchips, with 144 modchip firmware repositories disabled. Switch 2 emulators Eglantine and Lichii are tied to Yuzu's codebase through Eden and could be next, though copies of the firmware remain circulating on GitHub. ([IGN](https://www.ign.com/articles/nintendo-takes-down-switch-emulators-and-mod-chip-firmware-in-massive-github-dmca-sweep))
- **An abandoned Quake 4 expansion has been finished by modders** and is now playable, rescuing content that never shipped.

## Cybersecurity

- **N-able N-central is under active attack.** Researcher Sean Bales published 30+ zero-days ("Able2Shell") over the weekend, then two more exploit chains on November 12 ("4EverAble2Shell" and "Agent2Shell") that work even against the Hotfix 2 build — 4EverAble2Shell gives unauthenticated root when the Legacy API is enabled, and BleepingComputer reports at least 21 N-central servers were mining cryptocurrency by midday UTC. If you run N-central on-prem, turn off the Legacy API and patch now. ([BleepingComputer via threat brief](https://kevintswaney.com/articles/morning-threat-brief-november-12))
- **Apache HTTP Server 2.4.71 fixes a critical HTTP/2 remote code execution bug** (CVE-2026-119618) affecting 2.4.55–2.4.70 with HTTP/2 enabled — upgrade promptly.
- **Xen Orchestra authentication bypass is being exploited.** Vates confirmed active exploitation of a critical flaw (VSA-2026-062) where a single crafted cookie logs an attacker in as admin — patch immediately.
- **Maersk confirmed a breach** in a legacy logistics system inherited from an acquisition; the WhiteArmor ransomware gang claims ~100GB stolen and is demanding $5 million.
- **Zoom fixed a critical RCE** found by autonomous security agents: an outdated pjproject library (CVE-2026-25994) left a buffer overflow reachable during phone calls on all platforms. Update to Zoom 7.2.0 or later.
- **Philippines data breaches:** the National Privacy Commission confirmed breach notifications from at least 10 government agencies, including the DICT, BIR and SEC, after a wave of incidents flagged by watchdogs.

## AWS

- **AWS opened its South America (Chile) Region** on November 11 — its first in Chile and third in Latin America — investing more than $4 billion, with general availability expected by the end of 2026. Also from the November 9 roundup: Bedrock AgentCore Runtime V2 is generally available, and DynamoDB now supports bulk put of items from S3 into existing tables.

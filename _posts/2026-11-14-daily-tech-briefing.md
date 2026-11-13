---
layout: post
categories: [tech-briefing]
date: 2026-11-14 07:30:00 +0800
title: "FAA grounds all flights, Coway unclouded, Claude joins meetings"
---

Prepared: 7:30 AM SGT

## Hacker News Top 10

### 1. 🆕 New: FAA Issues National Ground Stop

On Friday 13 November 2026 the FAA ordered a nationwide ground stop, instructing all departing aircraft at every US airport to remain on the ground until further notice, with inbound international flights handled case by case. The cause was a telecommunications failure affecting all 22 Air Route Traffic Control Centers, which officials stressed was not a cyberattack; the stop was ordered out of caution while technicians investigated. It is only the second nationwide ground stop of all departures since 9/11, and by Friday evening nearly 7,000 US flights had been delayed or cancelled.

[Discussion](https://news.ycombinator.com/item?id=50489641) · [Source](https://www.fly.faa.gov/adv/adv_otherdis?adv_date=11132026&advn=111)

### 2. 🆕 New: Live airband on all frequencies from KORS. Victoria, CA also ground stopped

Orcas Airband is a hobbyist site streaming live air traffic control radio from Orcas Island (KORS) in Washington's San Juan Islands, covering frequencies for Vancouver, Victoria, Bellingham, Whidbey and nearby airports, with a live transcript of each transmission. It became a front-row seat to the ground stop in real time: the transcript shows Victoria Terminal warning a seaplane pilot that a ground stop is in effect for aircraft into Vancouver and Calgary, while airborne traffic is unaffected and departures are held. (Note: "Victoria, CA" here means Victoria, BC, Canada — the feed covers the US–Canada border region, not California.)

[Discussion](https://news.ycombinator.com/item?id=50490593) · [Source](https://orcasairband.com/)

### 3. 🆕 New: Terminal borders that don't cost a cell

Ratatui maintainer Joshka (Josh McKinney) proposes a terminal protocol that draws borders on the edges of cells instead of using box-drawing characters that consume a whole row and column each. Each cell can carry up to twelve line segments with their own colour, width, style and rounded joints, so panes, tabs, buttons and chart gridlines cost no screen space, scroll and erase like other cell attributes, and never pollute copy-paste. He has a working patch for Ghostty (plus an earlier Rio prototype), a draft spec using a DCS escape sequence with capability detection and box-character fallback, and is asking terminal and TUI authors for feedback.

[Discussion](https://news.ycombinator.com/item?id=50491423) · [Source](https://www.joshka.net/cell-borders/)

### 4. FM-1 Workbench

This is the web workbench and full user manual (in Chinese) for the FM-1, an 8-track hardware groovebox/synthesizer with a companion browser editor that connects over USB MIDI. Each track offers six sound engines — DX7-style FM, 303 acid bass, 808 drums, PSG chiptune, plucked string and sampler — with a step sequencer (16–64 steps per track), arpeggiator, per-track effects, and 16 built-in plus 16 user projects. The web editor lets you audition and edit sounds, import/export projects, DX7 patches and sample libraries, and write them to the device with read-back verification.

[Discussion](https://news.ycombinator.com/item?id=50488325) · [Source](https://open.m-vave.com/fm1-workbench)

### 5. Reverse engineering my Coway air purifier to ditch the cloud

Frustrated by Coway's unreliable IoCare cloud (outages, account bans, app rewrites), Scott set out to control his Coway Airmega IconS locally, using a Raspberry Pi as a mitmproxy access point and AI to do the heavy lifting. The key discovery was a security flaw: the purifier downloads its root CA certificate over plain HTTP, so it was always interceptable — and by decompiling the Android app and snooping Bluetooth provisioning logs, he found the setup payload lets you point the device at your own certificate and MQTT servers. He built a local Home Assistant integration (provisioned via Web Bluetooth) so the purifier now talks directly to Home Assistant and Apple Home, with no Coway cloud involved at all.

[Discussion](https://news.ycombinator.com/item?id=50474959) · [Source](https://scottjg.com/posts/2026-11-11-reverse-engineering-my-coway-air-purifier-to-ditch-the-cloud/)

### 6. After 600 experiments, here's what I discovered about JEPA world models

Haddy Alchaer ran 600 experiments on LeWM, Yann LeCun's JEPA world model, on the Push-T block-pushing benchmark, and found the model's predictions are already nearly as good as perfect physics — the gains come from how the planner uses it, not from retraining. Chaining 25-step subgoals lifted long-horizon success from 22% to 80%, and a latent memory graph of past demonstrations (with a cost on jumps between demonstrations, plus symmetry-transformed memories to fill gaps) reached 85% with no extra training. The most striking finding was a scoring bug: goals are images that include the robot pusher's position, so the planner wasted effort matching the pusher instead of the block — scoring the block alone quadrupled success on the hard test, from 9/50 to 39/50 with exact physics.

[Discussion](https://news.ycombinator.com/item?id=50487185) · [Source](https://haddyalchaer.com/jepa)

### 7. Found: a protein that drives ageing without unleashing inflammation

Monash University researchers (Kannangara et al., published in *Immunity*) found that granzyme K, an immune-cell protein whose levels rise sharply with age in mice and humans, drives age-related damage in the heart, liver and kidneys. Aged mice engineered to lack granzyme K showed improved heart function, less liver stiffening and scarring (fibrosis), and less kidney damage — yet their immune systems still aged normally. The team is now investigating drugs that selectively block granzyme K later in life, which could one day protect organs from ageing without weakening immune defences.

[Discussion](https://news.ycombinator.com/item?id=50488470) · [Source](https://www.nature.com/articles/d41586-026-03638-3)

### 8. Perplexity Decider v1.3: Training, eval, and use cases

Perplexity released Decider v1.3 and a smaller distilled Decider Flash v1.3, open-licensed decision (classification) models that return probability distributions over answers instead of generating text, for tasks like judging outputs, routing queries, moderation, filtering and reranking. The new version adds bidirectional attention with isolated per-question attention for stability, a three-stage training recipe (generalist fine-tuning, LoRA specialization, vision step), and a new "locate" feature that extracts exact text spans for entity recognition, PII detection and extractive QA. On Perplexity's internal suite of 200+ zero-shot tasks, Decider v1.3 hit 91.6% mean accuracy across 63 query-classification tasks, beating its production classifiers by 6.5 points, and it leads rival Jev 1.14 across seven domain benchmarks.

[Discussion](https://news.ycombinator.com/item?id=50488464) · [Source](https://www.perplexity.ai/hub/blog/perplexity-decider)

### 9. 🆕 New: Claude Meetings

Anthropic launched Claude Meetings in beta: Claude can now join video calls as a visible participant, follow the conversation, answer questions in the meeting chat, and build docs and whiteboards live while the team talks. After the call, notes, action items, transcripts and anything Claude built live on the meeting's page in claude.ai, and you can later ask Claude about past meetings or add it from your calendar. It's rolling out on Team and Enterprise plans (Google Meet first, other platforms coming), with privacy controls — Claude stays out of calls with external guests by default, saves transcripts and summaries but not audio — and beta usage is free except for connected-tool calls.

[Discussion](https://news.ycombinator.com/item?id=50491097) · [Source](https://claude.com/resources/articles/claude-meetings)

### 10. Doomsday: Friday, 13 November, A.D. 2026 (1960)

This is Heinz von Foerster, Patricia Mora and Lawrence Amiot's 1960 *Science* paper, which fitted a hyperbola to 24 estimates of world population over 2,000 years and found it shot to infinity at year 2026.87 — Friday 13 November 2026, which also happened to be von Foerster's birthday. It's trending today because that date has now arrived, and the prediction has spectacularly failed: the formula implies roughly 96–131 billion people in 2025, versus the real figure of about 8.2 billion, because global birth rates peaked in the early 1960s and have fallen ever since. The paper was really a warning about unchecked growth, not a literal end-of-the-world prophecy, and it remains a classic lesson in extrapolating a trend past its breaking point.

[Discussion](https://news.ycombinator.com/item?id=50482379) · [Source](https://www.science.org/doi/10.1126/science.132.3436.1291)

## AI

- **Gemini 4 is in post-training, with a staged early rollout planned.** Google DeepMind chief Koray Kavukcuoglu confirmed the next flagship has entered post-training and Google intends to ship a first version "as soon as possible", breaking with its polished-launch tradition as rivals ship at record pace. ([AIReport](https://www.aireport.net/Gn_2a97a1f0d47c))
- **Anthropic opened a private beta of self-hosted Claude Managed Agents.** The whole agent service — harness, sandboxes, credentials, session history — can now run on the customer's own servers, with only the model itself staying at Anthropic. ([AI roundup](https://chrisabraham.net/2026/11/ai-roundup-the-perimeter-moved.html))
- **OpenAI launched two Daybreak security products.** Daybreak Red Team (early access) deploys agent fleets to penetration-test web apps and retest patches, while Daybreak Defense Factory, built on GPT-6 Cyber, scans codebases as they change and prepares fixes as merge-ready pull requests for a human to review. ([AI roundup](https://chrisabraham.net/2026/11/ai-roundup-the-perimeter-moved.html))
- **Nonprofits sued five AI labs to halt frontier model work.** A group including Public Citizen and the Irreplaceable Education Fund sued OpenAI, Anthropic, SpaceX's AI division, Meta and Google in San Francisco on November 12. ([Koda](https://www.koda.community/morning-briefing-koda.html))
- **OpenAI added local processing and inference for its API in India.** For supported workloads, request handling and model compute happen in India, starting with GPT-6 Luna through the Responses and Chat Completions APIs. ([Pulse #20](https://shivanathd.substack.com/p/the-operators-pulse-20-you-can-host))
- **Google, TikTok and Meta sued California to block AB 1709**, which bans autoplay, infinite scroll and recommendation algorithms for users under 16 from January 1, 2027. ([AI roundup](https://chrisabraham.net/2026/11/ai-roundup-the-perimeter-moved.html))

## Frontend

- **X rewrote its web client on Vite, Node.js 26 and Fastify**, replacing the legacy `rweb` codebase from Twitter Lite. First tweets now render in 1.7 seconds on slow 4G (down from over 22 seconds), with zero JavaScript downloaded before first paint, streaming SSR and GraphQL responses embedded in the page. ([BestHub](https://www.besthub.dev/articles/x-web-rewrite-vite-node-26-achieve-8x-faster-first-paint-01d9f7290966))
- **React 19.3 shipped with stable View Transitions and Fragment Refs**, and Next.js 16.4 introduced recommended Cache Components, smarter prefetching and AI-assisted upgrades. Node.js 26.13.0 "Lithium" is now the Active LTS line, supported through April 2029. ([Onix React](https://medium.com/@onix_react/whats-new-in-react-ecosystem-october-edition-af046793d985))
- **TypeScript 7.1 beta** builds on the Go-based compiler from 7.0, moving the compiler API out of `./unstable/*` into `typescript/sync`, `typescript/async` and `typescript/ast`, with improved support for Vue, Svelte and Astro. ([Onix React](https://medium.com/@onix_react/whats-new-in-react-ecosystem-october-edition-af046793d985))

## Emulation, Retro Games & Preservation

- **OpenAI is selling a retro FPGA console for vibe coders.** The ModRetro Chromatic: Codex Edition ($200, public shipments from November 19) reads original Game Boy and Game Boy Color cartridges without emulation, and its Codex Cartridge lets the Codex agent build a game from a text description and write the ROM to a rewritable cartridge. 13 Codex-built games are playable free in the browser. ([mlllm](https://www.mlllm.io/news/3796-openai-releases-retro-console-for-vibe-coders/))
- **Pocket Saturn brings Sega Saturn to the Analogue Pocket.** The early FPGA core (v0.1-a8b, listed November 4) draws on the Saturn_MiSTer core, but there is no compatibility list yet and no confirmed working retail games — still very early work. ([Generation Amiga](https://www.generationamiga.com/2026/11/06/sega-saturn-on-analogue-pocket-a-new-fpga-core-is-making-progress/))
- **A lost ZX Spectrum port of The Great Giana Sisters has been released.** The unofficial 2026 conversion by kirby2000 fills the gap left by the Spectrum version reviewed in 1988 but never released, with all 33 stages, secret bonus rooms, hidden warps, eight power-ups, a high score table and two-player mode, free on itch.io. ([YouTube](https://www.youtube.com/watch?v=uys9dRJN_Ow))
- **A $15 Tang Nano 9K FPGA board runs Doom, System Shock and Ultima VII.** Developer ThePartsBin built a custom 36MHz RISC-V machine on the tiny Gowin FPGA, highlighted by Hackaday on November 1. ([Retro Gameforce](https://www.retrogameforce.com/news/tiny-fpga-board-runs-doom-system-shock-and-ultima-vii-as-retro-computer-project-demonstr-news-2026-11-01-12/))
- **The SGBC FPGA console aims to play Game Boy, Game Boy Color and Game Boy Advance cartridges at 1080p** with integer scaling, SNES controller support and cartridge backup — but it is still in development, with no price or release date. ([Techtroduce](https://www.techtroduce.com/sgbc-fpga-console-game-boy-1080p-hdmi/))

## Cybersecurity

- **PHP2Shell exploitation turned destructive on Check Point gateways.** Attackers exploited the critical PHP runtime flaws (CVE-2026-109618/109619, CVSS 9.8) in unpatched gateways via Mobile Access portals, escalating to root via CVE-2026-123039 and planting webshells; the first wave on October 30 targeted Israeli organisations with destructive activity. CISA also republished Siemens advisories confirming PHP2Shell reaches OT products including building-automation and energy systems. ([Security Boulevard](https://securityboulevard.com/2026/11/daily-ot-security-news-november-13-2026/))
- **Barracuda Email Security Gateway flaws are actively exploited.** Two flaws chaining to root (CVE-2026-116606, CVSS 9.3, and CVE-2026-111560, CVSS 8.6) were added to CISA's KEV catalog on November 10 with a federal patch deadline of Friday, November 13. ([AI Agent Update](https://aiagentupdate.com/post/barracuda-esg-exploited-deadline-2026-11-13))
- **Citrix patched 10 critical NetScaler vulnerabilities** on November 13 — patch internet-facing gateways promptly. ([Techmaniacs](https://techmaniacs.com/2026/11/13/cyber-briefing-nov-13-citrix-netscaler-critical-patch-silentair-telecom-interception-campai/))
- **Operation Endgame seized Gootloader, CastleRAT and StealC infrastructure** — 235 servers, 257 domains and 6.4 million stolen logins. ([Techmaniacs](https://techmaniacs.com/2026/11/13/cyber-briefing-nov-13-citrix-netscaler-critical-patch-silentair-telecom-interception-campai/))
- **SilentAir hackers are intercepting calls and SMS from inside mobile networks**, primarily targeting Taiwanese subscribers — another reminder of the risks of SMS-based authentication. ([Techmaniacs](https://techmaniacs.com/2026/11/13/cyber-briefing-nov-13-citrix-netscaler-critical-patch-silentair-telecom-interception-campai/))
- **SCKit worm hijacked ConnectWise ScreenConnect panels**, compromising 288 managed endpoints across 48 organisations in under 90 minutes via CVE-2026-84869, stealing auth cookies and attempting lateral movement to technician workstations. ([Pacific London](https://www.pacific.london/insights/sckit-worm-malware-screenconnect-msp-cve-2026-84869-session-hijacking-supply-chain-uk-mid-market))
- **OpenSSH "SSHole" (CVE-2026-123158) joined CISA KEV** after exploitation within hours of disclosure, and Apache HTTP Server 2.4.71 fixes a critical mod_http2 heap corruption (CVE-2026-119618) — upgrade both promptly. ([Xalgorix](https://www.xalgorix.com/blog/weekly-appsec-threat-digest-nov-6-13-2026))
- **Apify confirmed a cyberattack on November 9–10** led to unauthorized access to customer accounts, exposing personal information and stored data. ([Techmaniacs](https://techmaniacs.com/2026/11/13/cyber-briefing-nov-13-citrix-netscaler-critical-patch-silentair-telecom-interception-campai/))

## AWS

- **AWS launched Graviton5-based R9g instances for Aurora and RDS, plus the M9g family for RDS**, claiming up to 30% performance gains and 22% better price-performance over Graviton4 equivalents.
- **SGLang-Neuron is now publicly available**, letting developers serve frontier AI models on AWS Trainium chips through the familiar SGLang interface, including reinforcement-learning rollouts. ([Chenab Times](https://thechenabtimes.com/2026/11/13/aws-trainium-enhances-ai-model-deployment-with-sglang-neuron-integration/))

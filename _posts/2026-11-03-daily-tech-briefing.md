---
layout: post
title: "Astra edits model weights, Anthropic slows, silent-speech glasses"
date: 2026-11-03 07:30:00 +0800
categories: [tech-briefing]
---

Prepared: 7:30 AM SGT

Hacker News top 10 as ranked on the live front page at around 7:27 AM SGT.

## Hacker News Top 10

### 1. Astra can read and write weights to improve Qwen

A research post shows GPT-6 Astra reading raw neural network weights directly — identifying which game a small policy network was trained on, what a diffusion model generates, and which language a tiny language model learned — all without running the networks. Most strikingly, Astra edited just 0.016% of Qwen3.5-0.8B's weights, with no gradients or training, lifting MATH-500 from 7.9% to 48.1% and tripling its IFEval score. The authors argue this "weight-space programming" points to a future where LLMs deliberately reason about weights instead of leaving optimization to symbolic algorithms like Adam.

- [Hacker News discussion](https://news.ycombinator.com/item?id=50341174)
- [Source](https://rikiyat.github.io/blog/weight-space-programming/)

### 2. 🆕 Anthropic's growth just flattened

Anthropic reportedly shared Q3 figures with investors showing $16.8 billion in revenue, up from $11.6 billion in Q2 and $4.8 billion in Q1 — still extraordinary growth, but a smaller absolute gain than the prior quarter. Breaking the quarter into monthly estimates against a reported $65 billion annualized run-rate in July suggests growth barely moved in August and September, a slowdown the author links to falling "neocloud" stocks like CoreWeave. Whether it reflects moderating demand, cheaper Chinese models, or simply capacity constraints matters enormously for Anthropic's imminent IPO valuation.

- [Hacker News discussion](https://news.ycombinator.com/item?id=50344958)
- [Source](https://www.regenerator1.com/p/anthropics-growth-just-flattened)

### 3. Show HN: Subvocal – Talk to your computer without making noise

Two Georgia Tech students turned a TreeHacks prototype into smart glasses that decode silently mouthed words using radio waves rather than face electrodes, after EMG proved too fiddly and unpleasant. RF signals passing through the tongue, lips, and soft palate are decoded by foundation models trained on data from paid volunteers reading prompts, and the founders say a short 20-sentence calibration is enough for a new user. Preorders are open for a first batch of 500 units, with shipping targeted for Q1 2027.

- [Hacker News discussion](https://news.ycombinator.com/item?id=50340088)
- [Source](https://subvocal.company/)

### 4. Apple reports fourth quarter results

Apple posted a September-quarter record of $114.5 billion in revenue, up 12% year over year, with diluted EPS of $2.10, up 14%, helped by about a percentage point of tariff refunds. iPhone hit a September-quarter record and Services reached an all-time high, capping a fiscal 2026 with record revenue of $479 billion. CEO John Ternus pointed to the iPhone Duo, iPhone 18 Pro line, and the new Siri AI heading into the holiday season, and the board declared a $0.27 per share dividend.

- [Hacker News discussion](https://news.ycombinator.com/item?id=50344670)
- [Source](https://www.apple.com/newsroom/2026/11/apple-reports-fourth-quarter-results/)

### 5. Can't fish Ethernet? Use "invisible" fiber instead

When a Cat6 run in a NYC townhouse degraded to 100 Mbps and fishing a replacement risked damage — and thick walls made mesh a poor fallback — the author ran adhesive "invisible" fiber, originally designed for apartment retrofits, between floors instead. Two media converters and a pair of bidirectional SC SFP+ transceivers connected the loop to an existing MikroTik switch, delivering around 300 Mbps without drilling or a contractor. It's a neat reminder that fiber isn't only for the connection into your home; it can fix the wiring inside it too.

- [Hacker News discussion](https://news.ycombinator.com/item?id=50344222)
- [Source](https://momandpop.network/2026/11/02/cant-fish-ethernet-use-invisible-fiber-instead/)

### 6. US boy names that became girl names and vice versa

A data visualization tracks American baby names that have crossed gender lines over the decades — names that started out predominantly male and became female, and the rarer reverse journey. The charts make visible how cultural associations shift: a name's gendered identity is a moving target, not a fixed property. It's a compact example of how a simple dataset, presented well, can surface a story you'd never guess from any single year's rankings.

- [Hacker News discussion](https://news.ycombinator.com/item?id=50339397)
- [Source](https://namedaisy.com/blog/boy-names-that-became-girl-names)

### 7. Launch HN: Momentic (YC W24) – Agents that catch bugs by using your app

Momentic's "Mo" agent explores web, iOS, and Android apps autonomously — building a DAG of product areas, fanning out parallel sub-agents, and coordinating through resource leases — to find bugs rather than write test scripts. On a benchmark of 1,396 human-labeled bugs across Gitea, Metabase, Twenty, and Saleor, Mo found 269 bugs (19.3% recall, 84% precision) at $2.67 per bug, well ahead of Codex, Claude Code, and Devin on recall. The team just shipped PR testing for Vercel and Cloudflare deploy previews and is giving new signups $250 in credit.

- [Hacker News discussion](https://news.ycombinator.com/item?id=50339913)
- [Source](https://momentic.ai/)

### 8. If you love a website, back it up

Web archivist Misty De Meo argues that preserving favorite websites shouldn't be left to big institutions: individuals can do it themselves, prompted by the disappearance of teapuppies.com, a long-running Ochaken fansite she had the tools to save but didn't. She recommends the free ArchiveWeb.page Chrome extension or standalone app for manually capturing pages, and Browsertrix for automatically crawling larger sites, both producing standard WARC/WACZ archives replayable via ReplayWeb.page. Her closing advice: keep multiple copies and share preservation duties with friends — "lots of copies keeps stuff safe."

- [Hacker News discussion](https://news.ycombinator.com/item?id=50336518)
- [Source](https://blog.mistys-internet.website/post/2026/10/29/if-you-love-a-website-back-it-up/)

### 9. The SEC Should Block Anthropic's IPO to Protect the Public

An op-ed argues the SEC should halt Anthropic's planned November IPO until it files two consecutive quarters of audited financials with its spending commitments fully disclosed. The case rests on footnoted figures: nearly $900 billion in total contractual commitments, including at least $582 billion in non-cancelable commitments to just five companies (Amazon, AMD, Broadcom, Google, and Microsoft), against $96 billion in cash. With revenue growth reportedly slowing and margins squeezed by competition and infrastructure costs, the author warns that going public would shift the fallout of a potential AI crash onto retail investors and retirement accounts.

- [Hacker News discussion](https://news.ycombinator.com/item?id=50344919)
- [Source](https://www.techpolicy.press/the-sec-should-block-anthropics-ipo-to-protect-the-public/)

### 10. Show HN: Warsaw in voxels – An interactive 3D map of the city centre

An interactive voxel map renders central Warsaw Minecraft-style, built from open datasets: OpenStreetMap for streets and buildings, Polish LiDAR for heights and trees, aerial imagery for colours, and the city's tree database for seasonal foliage. You can change the date, time of day, and weather, explore the city, or click a pedestrian to control them. The project is open source, and works best on desktop.

- [Hacker News discussion](https://news.ycombinator.com/item?id=50339221)
- [Source](https://p.migdal.pl/warsaw-vibe-voxel/)

## AI

- **DeepSeek open-sources an agentic coding prototype.** DeepSeek's Harness team released dsh-superagent v0.1.0 under MIT, a router-worker architecture that splits repo tasks into parallel tickets. ([Communeify AI Daily, Nov 2](https://www.communeify.com/en/blog/ai-daily-2026-11-02/))
- **Meituan ships LongCat-2.5.** The natively multimodal agentic model totals 1.6 trillion parameters with about 48 billion active, with API access available. ([HeadsUpAI, Nov 2](https://headsupai.io/ai-news-and-updates/today))
- **Last week's model wave, in one place.** Google's Gemini 4 Carbon (Oct 28) targets cybersecurity and long-horizon agent work, and Mistral Large 4 (Oct 29) is a roughly trillion-parameter open-weight model claiming top open-model coding-agent scores with 47% fewer tokens per task than GLM-5.3. OpenAI also reportedly reversed a planned cut to ChatGPT Pro limits. ([Toolglade week-in-review](https://www.toolglade.com/blog/ai-news-week-of-2026-11-01))
- **Apple Intelligence heads to China on Qwen.** Apple Intelligence will debut in China this December powered by Alibaba's Qwen models across Siri, Writing Tools, and Visual Intelligence. ([Communeify AI Daily, Nov 2](https://www.communeify.com/en/blog/ai-daily-2026-11-02/))
- **A new agentic benchmark.** SemiAnalysis released GDPx, 206 tasks across 11 domains designed to measure frontier agentic capabilities. ([HeadsUpAI, Nov 2](https://headsupai.io/ai-news-and-updates/today))

## Frontend

- **Next.js security release lands today (Nov 3).** Next.js will ship patches for seven medium-severity vulnerabilities today, with advisories and upgrade instructions published alongside the release; Better Auth has a security release the same day. If you run Next.js, plan the upgrade for today rather than discovering it later. ([Medium: preparing for the Nov 3 releases](https://medium.com/@premchandak_11/seven-next-js-1d1b10dc98f5))
- **Node.js 26 is now LTS.** Version 26.13.0 moved the 26.x line into Long Term Support (Lithium), supported through April 30, 2029; Node 22 ends April 2027 and Node 24 runs to April 2028. Note that from Node 27 the project shifts to one major a year, each April. ([BuzzinTechHub](https://buzzintechhub.com/blog-detail.php?slug=nodejs-26-lts-upgrade-from-22-or-24))
- **Framework state of play.** React 19.3.1 shipped October 14 with stable View Transitions and Fragment Refs, SvelteKit jumped to 3 on October 1, and Next.js 16.4 made Cache Components recommended — while a new Next.js agent skill uses the Turbopack module graph to find imports defeating lazy loading (Vercel reports nearly 2 MB of client JS removed or deferred). Firefox 159, meanwhile, ships CSS scroll-driven animations, so all three major engines now support them. ([Tech Insider](https://tech-insider.org/react-vs-vue-vs-svelte-react-19-3-1-sveltekit-3-2026/), [Enpitech frontend digest](https://enpitech.dev/blog/frontend-digest-2026-11-01))

## Emulation, retro games, preservation, ROM hacking, FPGA, ports & recompilation

- **MediEvil Recomp hits 1.0.** The AI-free static recompilation of the PS1 original left beta with improved stability, analogue and audio fixes, FMV fixes, libretro shader preset support, a Mod Hub, and an in-game Asset Pack Editor — built with the RecompOne PS1 recompilation tool, requiring players to supply their own copy. ([Time Extension](https://www.timeextension.com/news/2026/11/we-have-the-skills-to-bring-love-to-these-old-games-after-last-months-beta-medievils-ai-free-recomp-hits-version-1-0))
- **Blast Corps, recompiled.** Rare's 1997 N64 demolition game now runs natively on Windows, Linux, and macOS via static recompilation, with uncapped framerates, ultrawide support, and mod capabilities. ([Pants Pants Revolution week in review](https://pantspantsrevolution.com/october-31st-week-in-review/))
- **New FPGA arcade cores and a Neo Geo fan port.** Jotego released public FPGA cores for NARC, Arbalester, and Meta Fox alongside CPS-3 validation work, and homebrew developer vendza released Final Fight Neo, a free conversion of Capcom's 1989 arcade brawler for Neo Geo hardware. ([Pants Pants Revolution week in review](https://pantspantsrevolution.com/october-31st-week-in-review/))
- **Browser-based ROM hacking.** Studio 64 lets you build Super Mario 64 ROM hacks in the browser, by hand or via AI text prompts. ([Pants Pants Revolution week in review](https://pantspantsrevolution.com/october-31st-week-in-review/))
- **The recompilation wave, quantified.** A tracker of AI-assisted game decompilation now lists 296 projects (125 reported working), spanning PS2, PS1, and N64 titles, with 135 static recompilations and 34 byte-matching decompilations. ([Reversed with AI](https://reversedwithai.com/ai-game-decompilation))

## Cybersecurity

- **Patch Ivanti Connect Secure now — and hunt.** CISA added two Ivanti Connect Secure flaws (CVE-2026-111357, CVE-2026-118527) to its Known Exploited Vulnerabilities catalog after Volexity found them chained with an auth bypass (CVE-2026-104935) for unauthenticated root on fully patched appliances, used to steal AD credentials, LAPS passwords, and BitLocker keys. Ivanti has released fixed builds; federal remediation deadlines fall on Nov 2 and Nov 13, and any unpatched internet-facing gateway should be treated as potentially compromised. ([SC Media](https://www.scworld.com/brief/cisa-adds-ivanti-connect-secure-vulnerabilities-to-known-exploited-catalog), [Particle](https://particle.news/story/ivanti-releases-patches-for-two-remaining-connect-secure-zero-days))
- **Chainalysis breached via "offensive agentic techniques."** The blockchain analytics firm disclosed attackers accessed some customer user IDs, full names, email addresses, and organization role labels, while saying investigation content, passwords, MFA secrets, and session tokens showed no sign of access. The incident is unrelated to last week's Binance hack. ([Help Net Security](https://www.helpnetsecurity.com/2026/11/02/chainalysis-breached-using-offensive-agentic-techniques/))
- **Amadeus breach widens.** Malaysia Airlines joined Cathay Pacific and Japan Airlines in reporting customer data affected via reservation provider Amadeus, with JAL citing about 92,000 passengers and Cathay about 53,000 bookings; Malaysia Airlines says its own systems were not breached and no financial data was accessed. ([Manila Times](https://www.manilatimes.net/2026/11/02/business/foreign-business/malaysia-airlines-assessing-amadeus-breach/2459029))
- **Also on the radar.** A $6.3 billion Binance theft attributed to North Korea's TraderTraitor; HTTP2Shell (CVE-2026-111497), an actively exploited Brotli RCE initially tied to Node.js; a critical Linux kernel TCP flaw (CVE-2026-98432, CVSS 9.8); and an Ubuntu Linux 0-day RCE reportedly still unpatched after almost three weeks. ([Malware News threat report](https://malware.news/t/2nd-november-threat-intelligence-report/126942))

## AWS (brief)

- **Agentic AWS, in the weekly roundup:** OpenAI GPT-6.1 Terra is generally available on Bedrock, Step Functions workflows can now be handed to agents as tools via the Bedrock AgentCore Gateway, and EKS Auto Mode supports the Kubernetes Gateway API. re:Invent runs November 30 – December 4 in Las Vegas. ([AWS Weekly Roundup, Nov 2](https://aws.amazon.com/blogs/aws/aws-weekly-roundup-gpt-6-1-terra-on-bedrock-step-functions-as-agent-tools-and-more-november-2-2026/))

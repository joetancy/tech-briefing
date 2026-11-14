---
layout: post
categories: [tech-briefing]
date: 2026-11-15 07:30:00 +0800
title: "Lovable data leak, Starship catch, and PyPI security signals"
---

Prepared: 7:30 AM SGT, Sunday, 15 November 2026

## Hacker News Top 10

### 1. 🆕 New: Lovable apps expose passport details and more than 200K private messages

German security firm Crissy Field analysed 159,041 Lovable-built projects found in Common Crawl (Dec 2025–Sep 2026) and found that 24,664 of the 34,545 using Supabase returned database records with no login; further read-only requests found email-bearing records in 10,560 tables across 7,403 sites. Worst cases included a lifestyle forum exposing 80,000+ profiles and 200,000+ chat messages, and a service provider exposing 1,000+ identity records with passport numbers, expiry dates and nationalities. The cause was missing Row-Level Security in the apps' Supabase databases — not a breach of Lovable itself — and the researchers could not establish whether the data was misused.

[Discussion](https://news.ycombinator.com/item?id=50499017) · [Source](https://www.crissyfield.de/research/lovable-en/)

### 2. 🆕 New: SpaceX Catches the Starship to end Flight 15

SpaceX's Starship Flight 15 ended with the Super Heavy booster being caught by the launch tower's arms, a milestone commenters described as a major step toward full reusability, with the ship itself also returning. Discussion focused on the heat shield's condition after re-entry and on re-flying the same vehicles as the next goal, since rapid reuse without refurbishment is what would make the system a success. (Note: the source is an X post, which could not be read directly in this environment; this summary is from the Hacker News discussion.)

[Discussion](https://news.ycombinator.com/item?id=50500963) · [Source](https://x.com/i/broadcasts/2brajgZlOKRMka)

### 3. A Family Tree of Software Job Titles

Ian Miell built an interactive family tree of 104 software job titles from the 1940s to now, starting with "Computer" (a person, not a machine) and ending with "AI Agent / Context Engineer" (c. 2025), arranged in five-year rows across seven families and rendered from a single Graphviz file plus a JSON file of descriptions. Drawing it out showed patterns such as titles splitting and rejoining (webmaster → web developer/sysadmin/editor, then front-end/back-end → full-stack), short-lived titles like prompt engineer being absorbed almost as soon as they appear, and recycled names — today's "forward deployed engineer" closely resembles IBM's 1960s pre-sales systems engineer. Dates are the author's best estimates of when titles became common, not sourced first-use citations.

[Discussion](https://news.ycombinator.com/item?id=50499038) · [Source](https://zwischenzugs.com/2026/11/03/a-family-tree-of-software-job-titles/)

### 4. How did Woz write the Apple 1 BASIC before building the computer?

Wozniak wrote Integer BASIC (then called "GAME BASIC") entirely by hand, without an assembler he couldn't afford, translating assembly instructions into 6502 machine code on paper using an HP BASIC manual and syntax diagrams — despite having barely used BASIC before. He dropped floating-point support to save time and beat others to the first 6502 BASIC, shipping an integer-only interpreter, and first hand-assembled a machine-code monitor, then used it to enter the BASIC once the hardware existed.

[Discussion](https://news.ycombinator.com/item?id=50501594) · [Source](https://retrocomputing.stackexchange.com/questions/17957)

### 5. KDE: The documentary [video]

"KDE: The Documentary — A Story of Free Software Underdogs" is a feature-length, interview-based film released for KDE's 30th anniversary, tracing the project from Matthias Ettrich's 1996 Usenet post asking for help building a Linux desktop through the Qt licensing fight and GNOME rivalry, the success of KHTML (which became WebKit/Chrome's basis), and the contentious KDE 4 release and rebuild. It features KDE founders and key figures including Ettrich, Aaron Seigo, Lars Knoll and Miguel de Icaza, and is also free to watch on YouTube (CultRepo channel).

[Discussion](https://news.ycombinator.com/item?id=50496976) · [Source](https://tube.kockatoo.org/w/fFinNHfanLT7aBEb2B8y4c)

### 6. PyPI's redesigned project pages with clearer security signals are now live

PyPI has shipped redesigned project pages built around clearer security signals, headlined by a new Security tab that shows each release's provenance state and per-file digital attestations (PyPI Publish and SLSA Build Provenance), so users can verify where release files came from. The redesign also surfaces provenance warnings at the top of the page — for incomplete, inconsistent, changed or lost provenance — reorders metadata by utility with "PyPI data" vs "Data verified by PyPI" labels, and adds searchable release-files and more detailed release-history tabs. The work, funded by the OpenSSF and implemented by Kabu Creative following the OpenSSF Attestations Style Guide, follows July 2026 UI-update plans shaped by user research with the Python community.

[Discussion](https://news.ycombinator.com/item?id=50497892) · [Source](https://blog.pypi.org/posts/2026-11-06-ui-updates-complete/)

### 7. 🆕 New: L3Harris Statement on the Nov. 13 Ground Stop

L3Harris said it has been modernizing the FAA's National Airspace System communications in coordination with the FAA and has completed over 70% of the planned conversion from legacy copper wires to fibre, and that it is supporting the FAA's investigation into the conditions that led to the Nov. 13 nationwide ground stop. Transportation Secretary Sean Duffy said the stop followed routine L3Harris maintenance switching telecom lines from copper to fibre at a remote FAA site, where an updated router flooded other routers; the FAA said up to 17 of 22 air traffic control centres were affected, with no evidence of a cyberattack, and the cause — installer error or a faulty router — is still undetermined.

[Discussion](https://news.ycombinator.com/item?id=50501844) · [Source](https://www.l3harris.com/newsroom/press-release/2026/11/l3harris-statement-nov-13-ground-stop)

### 8. Possible Futures

Fernando Borretti maps possible AI futures by branching on a few key questions — whether we reach ASI, whether alignment is solved and of what kind, how severe an unaligned takeoff would be, how many ASIs exist, and whether jobs are fully automated — then sketches scenarios including Misuse Doom (AI ending the world by following an operator's orders, e.g. via bioweapons assistance), a Butlerian Jihad-style halt to superintelligence, a mundane "Enduring Complementarity" where AI stays a complement to human labour, and a "Permanent Underclass" where non-superintelligent AI automates almost all jobs and income becomes capital ownership or welfare. Other scenarios include a single aligned "Singleton" ASI, a "World State" where one operator wields an intent-aligned ASI, and a "MAD World" of widely distributed personal ASIs kept in check by mutually assured destruction.

[Discussion](https://news.ycombinator.com/item?id=50464467) · [Source](https://borretti.me/article/possible-futures)

### 9. Why get an expensive Pi when I have an old phone?

The premise is that a spare old phone can serve as a home server instead of buying a Raspberry Pi, since the phone already has a faster processor, storage, screen, Wi-Fi and a built-in battery acting as a UPS. HN discussion noted the same trade-offs seen in similar setups: phones work well for software-only services via Termux/Proot, but lack the Pi's GPIO pins and open hardware interfaces for electronics projects.

[Discussion](https://news.ycombinator.com/item?id=50440709) · [Source](https://so.long.thanks.fish/why-pi-when-i-have-an-old-phone/)

### 10. Seagate's new hybrid drive raises some old questions

Seagate's new FireCuda Forge pairs an 8TB ($699) or 20TB ($899) HDD — SSD not included — with a user-supplied M.2 2280 NVMe drive (PCIe Gen3+, max 1TB, minimum 2,400 MB/s read / 2,000 MB/s write), managed by its new Alkemi platform, claiming 2,500 MB/s read and 2,000 MB/s write over USB4. The revival is driven by soaring storage prices in the AI boom (some SSDs at 2–3× historic lows), but Seagate has not explained how Alkemi distributes data between the drives, whether it uses caching, tiering or both, or what happens to your data if one drive fails — the same fragility question that haunted Apple's 2012 Fusion Drive.

[Discussion](https://news.ycombinator.com/item?id=50453901) · [Source](https://arstechnica.com/gadgets/2026/11/seagate-resurrects-the-ssd-hdd-hybrid-drive/)

## AI

- **Gemini 4 Carbon now tops MathArena**, the third-party math benchmark, with 85.4% expected performance, ahead of Claude Fable 5.2 (82.8%) and GPT-6.1 Sol (80.6%) — the first non-OpenAI model at #1 in a while. The catch: Carbon costs about $15.70 per problem, roughly 15× Sol's $1.07, and Fable 5.2 costs $40.20. ([AI-Oriens](https://ai-oriens.com/en/news/gemini-4-carbon-matharena/))
- **OpenAI launched ChatGPT Wallet**, letting Dots agents buy on the user's behalf — initially only for a small number of US ChatGPT Pro subscribers aged 18+ with a US Visa, Mastercard or Amex. Google also let US Gemini users connect Google Wallet to Gemini the same day. ([eYssen](https://www.eyssen.ai/blog/latest-ai-news-35/latest-ai-news-november-13-2026-524))
- **Nonprofits sued five AI labs to halt frontier model work.** Public Citizen, the Irreplaceable Education Fund and others sued OpenAI, Anthropic, SpaceX's AI division, Meta and Google in San Francisco on November 12, citing the companies' own leaders' warnings about AI risk. ([Economic Times](https://economictimes.indiatimes.com/markets/us-stocks/news/openai-google-anthropic-hit-with-lawsuit-to-halt-ai-development/articleshow/135820787.cms))
- **Anthropic's IPO is about 6× oversubscribed**, according to sources; pricing is expected November 18, trading on Nasdaq under ticker ANT, and the organising banks are reportedly not accepting orders from Chinese and Hong Kong investors. ([Economic Times](https://economictimes.indiatimes.com/markets/us-stocks/news/openai-google-anthropic-hit-with-lawsuit-to-halt-ai-development/articleshow/135820787.cms))
- **GitHub Copilot retires six models on December 14**, with recommended successors: Claude Fable 5.2 (replacing Fable 5), Claude Haiku 5.5, Gemini 4 Hydrogen, Gemini 4 Carbon and Grok 4.7. ([eYssen](https://www.eyssen.ai/blog/latest-ai-news-35/latest-ai-news-november-13-2026-524))
- **OpenAI disbanded its standalone robotics team**, moving the researchers into other parts of the company. ([eYssen](https://www.eyssen.ai/blog/latest-ai-news-35/latest-ai-news-november-13-2026-524))

## Frontend

- **WebStorm 2026.3 is out**, with Chrome DevTools Connect letting agents test their work in a real browser and hand back a verified result, plus stable TypeScript 7 support for React and Angular with no migration. ([JetBrains](https://blog.jetbrains.com/webstorm/2026/11/webstorm-2026-3/))
- **React Native 0.89 RC is here**, with faster text layout and native module calls, legacy bridge APIs removed, and a `useAppState()` hook; the release is due December 7. ([This Week in React](http://dev.to/sebastienlorber/this-week-in-react-304-nextjs-compiler-redux-toolkit-rn-089-rc-vega-os-screens--4fh0))
- **Parcel 3 alpha is a Rust rewrite** with no Node dependency and cold builds up to 100× faster than v2, plus React Compiler support. ([Enpitech](https://enpitech.dev/blog/frontend-digest-2026-11-08))
- **Redux Toolkit 2.14 landed**, with faster dispatch, RTK Query cache entry selectors and a DevTools action sanitizer, alongside a new 2.x and 3.0 roadmap. ([This Week in React](http://dev.to/sebastienlorber/this-week-in-react-304-nextjs-compiler-redux-toolkit-rn-089-rc-vega-os-screens--4fh0))
- **GitHub Actions will block `pull_request_target` by default in public repositories from December 2** — a supply-chain hardening move after compromises like TanStack, PostHog and Nx. ([This Week in React](http://dev.to/sebastienlorber/this-week-in-react-304-nextjs-compiler-redux-toolkit-rn-089-rc-vega-os-screens--4fh0))

## Emulation, Retro Games & Preservation

- **ModRetro Chromatic: Codex Edition ($200) ships November 19.** The FPGA handheld reads original Game Boy and Game Boy Color cartridges without emulation, and its Codex Cartridge lets the Codex agent build a game from a text description and write the ROM to a rewritable cartridge; 13 Codex-built games are already playable free in the browser. ([mlllm](https://www.mlllm.io/articles/3796-openai-releases-retro-console-for-vibe-coders-codex-builds-game-boy-games-from-text-descriptions/))
- **CoCoTANG is an open-source FPGA upgrade for vintage Color Computers**, recreating the CoCo 3's GIME chip on a Sipeed Tang Nano 20K board to bring enhanced graphics, 8MB of RAM and stereo HDMI audio to older CoCo 1/2 machines, with all source, KiCad designs and PCB files on GitHub. ([Hackster](https://www.hackster.io/news/it-s-never-too-late-to-upgrade-your-coco-5e4d6831bf15))
- **XRoar 1.13 is out** (Tandy Color Computer 1/2/3 and Dragon 32/64 emulator) with 6309 timing fixes and high-res GIME rendering fixes, and N64 emulator gopher64 reached 1.2.1. ([PlanetEmu](https://www.planetemu.net/en/news/10-11-2026-iv-play-v2-17-09-11-2026))
- **MiSTer Classic UI is in beta**, a new classic-style interface for MiSTer FPGA systems from a SuperStation One owner. ([PlanetEmu](https://www.planetemu.net/en/news/10-11-2026-iv-play-v2-17-09-11-2026))

## Cybersecurity

- **Check Point CVE-2026-123039 joined CISA's KEV catalog on November 13.** Attackers exploited the PHP2Shell flaws (CVE-2026-109618/109619) to enter gateway Mobile Access portals, escalated to root via this DynamicCLI flaw, planted the TSGA backdoor and wiped ESXi hosts; Check Point observed exploitation against "a couple of dozen" customers, and emergency hotfixes are available. ([DataWater](https://datawater.com/check-point-cve-2026-123039-php2shell-tsga-esxi-wiper/))
- **UnrealIRCd flaw CVE-2026-114713 (CVSS 8.6) is actively exploited.** A command-injection bug in the labeled-response module lets any user on a network with two or more linked servers inject server-to-server commands; CISA added it to KEV on November 13 with a federal fix deadline of November 16. ([The Hacker News](http://thehackernews.com/2026/11/attackers-exploit-unrealircd-flaw-that.html))
- **Four open-source projects got CVEs on November 13–14, all with fixes out.** Perl JSON::XS 4.05 fixes seven parser CVEs; the goose AI agent's `goose review` ran `git diff` without `--no-ext-diff`, letting a malicious `.git/config` run commands (CVE-2026-129128, fixed in 1.53.0); C-Kermit 11.1.515 fixes eleven CVEs including server-mode RCE; and Seafile's SeaDoc converter had a critical RCE (CVE-2026-129167, CVSS 9.2) reachable from a public share link. ([Corgea](https://corgea.com/research/cve-2026-129114-129128-129124-129167-json-xs-goose-c-kermit-seadoc-november-2026))

## AWS

- **AWS made its next-generation AgentCore Runtime the default for new runtimes** on November 12, across regions including Northern Virginia, Ohio, Oregon, Frankfurt, Ireland, London, Tokyo, Seoul and Sydney; it restores sessions from snapshots and scales resources down when agents idle. ([ad hoc news](https://www.ad-hoc-news.de/boerse/corporate-news/amazon-stock-aws-sets-new-agentcore-runtime-as-default/70510115))
- **Amazon RDS for SQL Server now offers M8id and R8id instance types**, with custom Intel Xeon 6 processors and local NVMe SSDs, supporting up to 384 vCPUs and 3 TiB RAM. ([OffNet](https://www.offnetchat.com/news/))

---
layout: post
title: "Huang's letter, Goldman pulls Claude Code, DeepSeek on 64GB RAM"
categories: [tech-briefing]
date: 2026-11-09 07:30:00 +0800
---

Prepared: 7:30 AM SGT — Monday, 9 November 2026

## Hacker News Top 10

### 1. Nvidia CEO Jensen Huang's letter to staff about affair 🆕 New
Huang admitted in a message to staff on Sunday, seen by Axios, that he had a romantic relationship with a suspected Chinese spy. In the email he apologized to his wife and family and said he will support and cooperate in an investigation by Nvidia's board of directors, which had separately announced it is investigating him. The full text of the letter sits behind Axios's sign-up gate, so details beyond the two paragraphs Axios left open remain unverified.
- [Discussion](https://news.ycombinator.com/item?id=50418016) · [Source](https://www.axios.com/2026/11/08/nvidia-ceo-jensen-huang-affair-email-to-company)

### 2. Dux: Free, open-source Wayland desktop shell with file manager and theming
Dux is a free, open-source Wayland desktop suite: a modular shell with dynamic theming, plus Dux Files (a fast, keyboard-first file manager with tabs and split view), a system monitor, greeter, search and calendar. It targets Hyprland, Sway, labwc and other Wayland compositors, generating matching colours for GTK/Qt apps, terminals and editors from a single theme. The site is also announcing DMS 2.1 "Stormborn", with a new system monitor, video wallpapers and a revamped media player.
- [Discussion](https://news.ycombinator.com/item?id=50416053) · [Source](https://duxlabs.dev/)

### 3. Ask HN: What are you working on? (November 2026)
The monthly thread where HN readers share what they're building and what they've been curious about lately — 308 comments and counting at time of writing. No external link; the discussion is the content.
- [Discussion](https://news.ycombinator.com/item?id=50417407)

### 4. Chimera Vocal Synth
Chimera is an interactive web app that synthesizes voice by simulating air moving through a vocal tract — throat, mouth and nose — rather than playing back samples. Drag the tongue, lips or jaw, or play the keys, and it renders the sound while visualising the glottis-to-lips tube, vocal folds slowed 100×, spectrum and vowel formants. Pitch, breath pressure and vibrato are adjustable, at 110 Hz by default.
- [Discussion](https://news.ycombinator.com/item?id=50418182) · [Source](https://chimera-vocal-synth.vercel.app/)

### 5. Declarative Dragging
Declarative Dragging, a UIST 2026 Best Paper, inverts drag-and-drop: instead of hand-coding geometry, feedback and animation, you declare which future states of your app dragging an element should lead to, and the system speculatively renders those states to synthesize the interaction. It's implemented as Dragology, a library for SVG interfaces on the web, with demos spanning algebra, twisted trees, bézier curves and card piles. The authors pitch it for educators, game designers and creative-tool builders who currently skip drag interactions because they're too fiddly to build.
- [Discussion](https://news.ycombinator.com/item?id=50368481) · [Source](https://declarative-dragging.github.io/)

### 6. KetchUp – Open-source SketchUp alternative built with Rust and WebGPU
KetchUp is a free, open-source 3D modelling app for woodworking and furniture design, built with Rust and WebGPU and MIT-licensed. It runs in a desktop browser or as a native Windows, macOS or Linux app, with a SketchUp-style draw-and-push/pull workflow, exact measurements, groups and components, and no account or cloud storage — projects autosave locally as portable .ketchup files. It can import SketchUp (.skp) geometry and export OBJ.
- [Discussion](https://news.ycombinator.com/item?id=50418176) · [Source](https://ketchup3d.github.io/app/)

### 7. Goldman Sachs is pulling Claude Code from its bankers and traders
Internal guidance updated in October restricts Claude Code and GitHub Copilot to Goldman's ~12,000 engineers, cutting off traders and bankers who had been using the tools to track client flows, model market moves and draft material. Strats — staff spanning trading, quant research and engineering — keep access. The reversal is striking because CIO Marco Argenti was praising traders' "vibe coding" as recently as July, and Goldman is a lead underwriter on Anthropic's IPO, expected to list on Nasdaq as ANT before the end of November.
- [Discussion](https://news.ycombinator.com/item?id=50415628) · [Source](https://www.thestateofai.com/news/goldman-sachs-claude-code-traders-bankers)

### 8. Outlook.com Is Quietly Rejecting Email from Domains Without DMARC
Since November 5, Outlook.com, Hotmail, Live and MSN have been intermittently rejecting mail from domains that publish no DMARC record — including ordinary low-volume senders, not just the bulk senders (over 5,000/day) covered by Microsoft's published rules since May 2025. The bounce reads "550 5.7.1 Message rejected: Message lacks SPF/DKIM/DMARC Auth Records", and because only some messages bounce, senders may not notice mail going missing. Microsoft has published nothing about the change; the fix is a single DNS TXT record, `v=DMARC1; p=none`, at `_dmarc`.
- [Discussion](https://news.ycombinator.com/item?id=50416158) · [Source](https://mailroute.net/blog/outlook-rejecting-email-without-dmarc)

### 9. The Web Is More Than Enough, by Paul Ford
After his tiny web office suite TinyLittleOffice — which stores data in the URL — drew a couple of hundred thousand visitors, Paul Ford argues the browser is now a remarkably powerful and cheap app platform: Web Crypto, WebAssembly, WebGL and Web Audio are all first-class, and AI-assisted coding keeps lowering the cost of using them. He points to Simon Willison's browser-based 3D multiplayer game Battle Drones as proof that individuals can now build what used to take teams. The flip side, he notes, is that software work increasingly resembles writing — and writers famously don't get paid.
- [Discussion](https://news.ycombinator.com/item?id=50416456) · [Source](https://ftrain.com/aboard-the-web-is-more-than-enough)

### 10. Llama-modchip: 284B DeepSeek on 64GB RAM, no GPU
Llama-modchip is a set of ggml/llama.cpp kernel patches and quantization transcoders that runs 284B DeepSeek-V4-Flash in under 59 GiB of RAM — 44.4 tok/s prefill and 9.1–14.7 tok/s decode on a 64 GB Zen 5 CPU with no GPU — by compressing the checkpoint to 56.56 GiB at 1.71 bits per weight. Smaller 30B MoE models run at 25–111 tok/s on pure CPU, with a 256K context window and a Stockfish-inspired speculative drafter plus /dev/shm KV snapshots that restore agent context in ~13 ms. The project ships a `modchip` CLI for chat, benchmarks and Claude Code wiring.
- [Discussion](https://news.ycombinator.com/item?id=50411961) · [Source](https://github.com/synchopate/llama-modchip)

## AI
- **Anthropic described Claude's memory system in an engineering account**: stored transcripts, model-written notes and linked knowledge structures, loaded as a small context block at session start; on one database task, memory raised Opus 5.5's mean reward from 0.655 to 0.838 (the company's own test). [AI Lab Week](https://1023jack.com/news/ai-lab-week-10-moves-by-anthropic-openai-google-meta-xai-moonshot-and-cognition/)
- **Cognition shipped SWE-2 Flash on November 4**, built on Thinking Machines' Inkling-Small model; **Inkling 2 Small (Nov 5) is the week's highest-ranked new model at 58.4** on BenchLeader, while Gemini 4 Carbon (Oct 28) remains the top-ranked recent release at 69.3. [AI Lab Week](https://1023jack.com/news/ai-lab-week-10-moves-by-anthropic-openai-google-meta-xai-moonshot-and-cognition/) · [BenchLeader](https://www.benchleader.com/releases)
- **Moonshot published the weights for Kimi K3.1 Pro on Hugging Face on November 4**, days after the model landed on Amazon Bedrock. [AI Lab Week](https://1023jack.com/news/ai-lab-week-10-moves-by-anthropic-openai-google-meta-xai-moonshot-and-cognition/)
- **Tencent released Hy4 on November 4**, a 770-billion-parameter mixture-of-experts model and the first Hy model with vision and computer use. [AI Lab Week](https://1023jack.com/news/ai-lab-week-10-moves-by-anthropic-openai-google-meta-xai-moonshot-and-cognition/)
- **Google's Gemini Omni 1.2 Flash went generally available on November 5**, generating video up to 15 seconds with native audio, and **OpenAI's Images 2.6 (Nov 4) adds animated GIF creation in ChatGPT**, from a text prompt or a photo, with per-frame editing. [Top AI News of the Week](https://nolowiz.com/top-ai-news-of-the-week-november-1-november-8-2026/)
- **Anthropic's revised IPO filing (Nov 2) warns it may soon reach its own threshold for AI that dramatically speeds up its own development.** [Top AI News of the Week](https://nolowiz.com/top-ai-news-of-the-week-november-1-november-8-2026/)
- **The US Department of Homeland Security banned DeepSeek products across all federal civilian agencies.** [AI Month in Review](https://www.linkedin.com/pulse/ai-month-review-november-2026-vincent-amedekah-oljgc)

## Frontend
- **Chrome 157 is out**, with HTML-in-Canvas stable — interactive DOM inside 2D, WebGL and WebGPU canvases, unflagged. [This Week in React #304](https://substack.thisweekinreact.com/p/this-week-in-react-304)
- **Next.js November security releases 16.4.5 and 15.5.29** fix 7 medium-severity vulnerabilities. [This Week in React #304](https://substack.thisweekinreact.com/p/this-week-in-react-304)
- **X rebuilt its web app as a streaming server-rendered React app**: the first post now appears in 1.7s versus 21.7s on a simulated slow connection in November 3 lab tests; the rollout is country-by-country. [X Engineering, Nov 4](https://bitcoinversus.tech/2026/11/08/x-web-rebuild-old-vs-new-13x-speed-2026-benchmark/)
- **CSS scroll-driven animations are now Baseline** — Firefox 159 shipped them on October 27, joining Chrome 115 and Safari 26, so the feature works in plain CSS in every major browser. [richi.codes](https://richi.codes/article/2026-11-04-scroll-driven-animations-are-baseline-at-last)
- **React Native 0.89 RC** brings faster text layout and native module calls, removes legacy bridge APIs, and adds a `useAppState()` hook; the release is due December 7. [This Week in React #304](https://substack.thisweekinreact.com/p/this-week-in-react-304)
- **Node.js 27.0 alpha** ships V8 15.6, npm 12.1, a `--allow-env` permission flag and native `fs.glob`; it's the first alpha of the new release model, becoming Current in April 2027 and LTS in October 2027. [This Week in React #304](https://substack.thisweekinreact.com/p/this-week-in-react-304)

## Emulation, Retro Games & FPGA
- **Pocket Saturn brings Sega Saturn to the Analogue Pocket**: an FPGA core based on Saturn_MiSTer appeared in the openFPGA listings on November 4 (v0.1-a8b); it's early work with no compatibility list yet and the Pocket's smaller FPGA is a real constraint for the demanding Saturn design. [GenerationAmiga](https://www.generationamiga.com/2026/11/06/sega-saturn-on-analogue-pocket-a-new-fpga-core-is-making-progress/)
- **A $15 Tang Nano 9K FPGA board now runs Doom, System Shock and Ultima VII**: ThePartsBin built a custom 36 MHz RISC-V machine on the Gowin GW1NR-9C (8,640 logic lookup tables), highlighted by Hackaday on November 1 — adapted versions of the games, not a general-purpose PC replacement. [Retro Gameforce](https://www.retrogameforce.com/news/tiny-fpga-board-runs-doom-system-shock-and-ultima-vii-as-retro-computer-project-demonstr-news-2026-11-01-12/)

## Cybersecurity
- **Kyverno CVE-2026-124440 (CVSS 9.4, published Nov 8)**: an authorization bypass in the apiCall namespace clamp lets namespace tenants issue cross-namespace and cluster-scoped API requests by appending malformed percent-escapes to urlPath; fixed in 1.19.2. [ThreatRoundup](https://threatroundup.com/cve/cve-2026-124440/)
- **Microsoft Paint RCE (CVE-2026-83844, CVSS 8.1)**: an unauthenticated remote code execution flaw via an out-of-bounds read; the fix ships via the Microsoft Store, not Windows Update. [PwnSpectrum](https://feed.anmolsinghyadav.com/)
- **CISA's KEV additions this week**: SonicWall SSL-VPN SAML bypass CVE-2026-19868 (added Nov 6, federal deadline Nov 20), Apple improper-authentication CVE-2024-27834, and WordPress core RCE CVE-2026-119977 — three exploited flaws in one week. [TheCyberMind weekly brief](https://thecybermind.co/2026/11/08/weekly-cyber-intelligence-brief-08nov26/)
- **Insignary released a free tool to scan for PHP2Shell and Node2Shell exposure**, both actively exploited vulnerability chains. [PwnSpectrum](https://feed.anmolsinghyadav.com/)

## AWS
- **Kiro Crew bots are generally available (Nov 5)**: persistent-memory AI agents inside Kiro's dev workspace that run on schedules, watch builds and review code changes; plans start at $20/month for 1,000 credits. [datastudios](https://www.datastudios.org/post/aws-kiro-crew-bots-generally-available-memory-schedules)
- **AWS Account Access Manager (Nov 5)** centralizes assigning existing IAM roles to IAM Identity Center users and groups, at no additional cost. [NeoTeo](https://www.neoteo.com/en/aws-announces-account-access-manager-for-iam-roles)

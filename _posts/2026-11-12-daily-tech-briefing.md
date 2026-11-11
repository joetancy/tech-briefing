---
layout: post
title: "AWS emulator, Tim Peters remembered, United bans AI agents"
categories: [tech-briefing]
date: 2026-11-12 07:30:00 +0800
---

Prepared: 7:30 AM SGT — Thursday, 12 November 2026

## Hacker News Top 10

### 1. AWS emulator 🆕 New
AWS has open-sourced AWS Emulator, a local emulator of the AWS APIs for testing software without calling AWS or needing an AWS account, available in server mode (CLI/SDKs pointed at a local endpoint) and embedded mode (in-process for Rust tests). It is written in Rust with one crate per service, publishes per-service fidelity scores with each release, and tracks gaps in the repo's `issues/` directory. Note that telemetry is on by default, though it can be disabled via a flag, environment variable, config file, or the embedded API.
- [Discussion](https://news.ycombinator.com/item?id=50456631) · [Source](https://github.com/aws/aws-emulator)

### 2. Tim Peters has died 🆕 New
Guido van Rossum announced on 11 November 2026 that Tim Peters died earlier this year, on 15 July, aged 73. Peters was best known for writing the Zen of Python (PEP 20) and for designing Timsort in 2002, which Python, Java, and Android later adopted, and he was a mentor and language co-designer from Python's earliest days. Tributes in the thread recall his patient, humorous mailing-list answers, his deep work on Python's dict, garbage collector, and memory allocator, and his role as a Python Software Foundation director from 2001 to 2014.
- [Discussion](https://news.ycombinator.com/item?id=50450488) · [Source](https://discuss.python.org/t/in-memoriam-tim-peters-1952-2026/110028)

### 3. United Airlines bans AI agents from booking flights on behalf of travelers 🆕 New
United revised its Contract of Carriage on 11 November 2026 to prohibit AI agents from making, modifying, or servicing tickets or purchasing any service or product, including via travel agencies and aggregators, and says it may cancel such reservations without notice — even when the passenger supervises or approves the agent's actions. The airline cites privacy risks from sharing credentials, unintended purchases or MileagePlus use, and potential FAA/DOT violations (e.g. automated check-in attestations); AI agents may still show United flights and prices, but the purchase must be completed by the customer.
- [Discussion](https://news.ycombinator.com/item?id=50458900) · [Source](https://www.cbsnews.com/news/united-airlines-bans-ai-agents-booking-flights/)

### 4. 93% of Paint Splatters Are Valid Perl Programs (2019)
This SIGBOVIK 2019 joke paper by Colin McMillen answers the question "is it possible to smear paint on the wall without creating valid Perl?" in the affirmative — but only just, finding via OCR that 93% of paint splatters parse as valid Perl. The paper analyses the properties of paint-splatter Perl programs and presents seven splatters that are not valid Perl, alongside a gallery of the splatter images with their corresponding Perl source.
- [Discussion](https://news.ycombinator.com/item?id=50459745) · [Source](https://www.mcmillen.dev/sigbovik/)

### 5. A false smoke alarm almost drowned Jane Street's only NYC datacenter 🆕 New
In this war story from Jane Street's systems team, contractor dust set off the smoke alarm in the firm's in-office datacenter at 1 New York Plaza, which pressurised the sprinkler pipes and shut down the cooling (CRAC) units — leaving rising heat as the only thing standing between the servers and a 150°F sprinkler trigger. The author sprinted from his nearby apartment and pulled the power cord on every device row by row, with the temperature peaking at 143.6°F before stabilising; trading was unaffected as markets were closed, and the firm was back up the next morning. Afterwards he wrote an OCaml monitor that polls every server's temperature each minute and alerts the team if the fleet-wide average runs hot, since no single-server alert would have caught a generalised cooling failure.
- [Discussion](https://news.ycombinator.com/item?id=50455394) · [Source](https://michael.bacarella.com/2026/11/10/false-smoke-alarm-jane-street-datacenter/)

### 6. Lock Your GitHub Actions 🆕 New
GitHub Actions now supports workflow lockfiles, so instead of pinning actions to opaque full SHAs (the old defence against mutable tags being retargeted in supply-chain attacks), you can write readable `vX.Y.Z` tags in workflows and let a generated `.github/workflows/actions.lock` file pin each tag to its exact commit, owner, and repo IDs. Hugo van Kemenade shows the setup using the `gh-actions-lock` CLI extension, notes that Renovate and Dependabot already support updating the lockfile, and recommends verifying it in CI plus running the zizmor security linter (v1.32.0 or later, the first to support lockfiles).
- [Discussion](https://news.ycombinator.com/item?id=50459485) · [Source](https://hugovk.dev/blog/2026/lock-github-actions/)

### 7. Gemini Decisions API 🆕 New
Google has launched the Gemini Decisions API, powered by the new Gemini Decision 1 model, which evaluates up to 1,000 yes/no, multiple-choice, and rubric-scoring questions against one multimodal input (text, images, audio, video, PDFs up to 256K tokens) in a single forward pass — no token-by-token generation. It returns probabilities and confidence scores per answer in 150–250 ms end-to-end, priced at $0.10 per 1M input tokens with zero output tokens billed, and Google reports it leads on agent-routing, reasoning, ranking, and multimodal benchmarks with the lowest calibration error. Early uses include dynamic model routing in Gemini Notebook (up to 40% lower latency), rapid wireframe iteration in Stitch, emoji selection, and a safety layer for MCP tools in Search.
- [Discussion](https://news.ycombinator.com/item?id=50456791) · [Source](https://blog.google/innovation-and-ai/technology/developers-tools/gemini-decisions-api/)

### 8. Emacs in the Age of Magic 🆕 New
The author, an Emacs user now deep into Claude Code, argues that AI coding agents have erased the advantages Emacs users once claimed — editing speed, customisation, Lisp expressiveness — because you now describe what you want instead of typing it. He illustrates the shift with two case studies of novices using AI to build absurdly ambitious things: excali-mode.el, a from-scratch reimplementation of Excalidraw's whole stack in Elisp and C on Emacs's new canvas widget, and cooked.el, a terminal emulator reimplemented in Rust for a "cooked" text-buffer mode. His conclusion is that when building and tearing down cost only tokens, throwaway personalised reimplementations proliferate — real software freedom, but with the catch that nobody understands how any of it works.
- [Discussion](https://news.ycombinator.com/item?id=50458208) · [Source](https://commandlinesystems.com/magic.txt)

### 9. Show HN: I recreated Papers Please but you're deciding which YC startups to fund 🆕 New
Term Sheet, Please is a Papers, Please-style browser game in which you play a YC decision-maker on the day after Demo Day, calling the next founder in and stamping their term sheet. The loaded page itself is the interactive game (a desk, a countdown clock, and a "click a fact on a paper" mechanic with a 0/2 facts counter) with almost no descriptive text, so the premise comes from the game's framing and title rather than an about page. Gameplay centres on inspecting each founder's paperwork and deciding whether to fund them before the clock runs out.
- [Discussion](https://news.ycombinator.com/item?id=50457230) · [Source](https://termsheetplease.com/)

### 10. Huawei releases MACaQ, its internal quantizer for local inference 🆕 New
Huawei's Computational Science Lab has open-sourced MACaQ (Model Agnostic Calibrated Quantization), a quantizer for running text, image, video, and audio models locally via llama.cpp, vLLM, Diffusers, and PyTorch. It claims a 122B-parameter model can be quantized in 64 minutes using just 32.5 GB of device memory, with lower perplexity than MR-GPTQ and DuQuant++ or matching their best Llama-3-8B perplexity with 11× less quantization time. It supports 2/3/4-bit GGUF for llama.cpp (including a MACaQ-R refinement mode that runs on stock llama.cpp), W4A4 for Diffusers, vLLM, and PyTorch, plus Ascend kernels, under an Apache 2.0 licence.
- [Discussion](https://news.ycombinator.com/item?id=50458166) · [Source](https://github.com/huawei-csl/MACaQ)

## AI
- **Anthropic began its IPO roadshow on Nov 10** — 825M shares priced at $70–$78, listing on Nasdaq as ANT, with a concurrent $26B private placement from seven chip/cloud firms including Google, Nvidia, AMD and Microsoft; no trading date set yet, with reports pointing to Nov 19–20. [ADVFN](https://ca.advfn.com/stock-market/NYSE/TSM/stock-news/99684028/an-ai-developer-starts-its-ipo-roadshow-and-its-f)
- **Anthropic announced Claude Meetings (beta for Team/Enterprise on Google Meet first)** — a push into office/productivity tools alongside the Nov 10 launch of Claude Sheets, Whiteboards and Claude Data, with interactive connectors built on MCP Apps. [Coding Is Love](https://codingislove.com/claude-sheets-whiteboards-meetings/)
- **OpenAI will retire ChatGPT's Advanced and Standard Voice modes on Dec 11, 2026**, moving all users to GPT-Live (launched July); live video/screen sharing stays on Advanced Voice until GPT-Live supports it, and voice usage nearly doubled since GPT-Live arrived. [Interesting Engineering](https://interestingengineering.com/ai-robotics/chatgpt-drops-two-voice-modes-december-2026)
- **Alibaba opened a Qwen4-Max preview on Nov 11** — its new flagship, with a 1M-token context window, available only via the Token Plan subscription and Qwen apps until the preview retires Nov 25; no model card, benchmarks, parameter count or per-token price published yet. [Fello AI](https://felloai.com/qwen-4/)

## Frontend
- **Chrome 157 shipped HTML-in-Canvas as stable (Nov 3)** — real, interactive, accessible DOM elements can now render inside 2D, WebGL and WebGPU canvases, with support already in Three.js, PlayCanvas, Babylon.js and PixiJS; Firefox and Safari have no equivalent yet, so feature-detect. [Chrome for Developers](https://developer.chrome.com/blog/html-in-canvas)
- **Next.js shipped its November security release (16.4.5 / 15.5.29) on Nov 3**, fixing seven medium-severity issues, mostly around Cache Components, including a cross-tenant cache disclosure rated High — a version bump for most teams. [Enpitech](https://enpitech.dev/blog/frontend-digest-2026-11-08)
- **Discord is rebuilding its desktop client in Rust with GPUI (Zed's UI framework), leaving Electron and React Native** — mobile keeps native interfaces over shared Rust code; no release date yet, and the shared memory figure (~290 MB) is a single claimed snapshot, not a benchmark. [Enpitech](https://enpitech.dev/blog/frontend-digest-2026-11-08)
- **Parcel 3 alpha is a Rust rewrite with no Node dependency**, claiming up to 100x faster cold builds than v2, plus native Tailwind (no PostCSS), React Compiler and MDX support. [Enpitech](https://enpitech.dev/blog/frontend-digest-2026-11-08)

## Emulation, Retro Games & FPGA
- **MediEvil Recomp 1.0 launched (Nov 2)** — the 1998 PlayStation classic now runs natively on Windows, macOS and Linux via static recompilation, with a new Mod Hub and asset editor; users must supply their own copy of the game. [Retro Gameforce](https://www.retrogameforce.com/news/medievil-recomp-reaches-version-1-0-with-native-pc-support-and-powerful-new-modding-feat-news-2026-11-03-01/)
- **Dolphin 2609b hotfix released (Nov 7)** — fixes a crash on Windows when the time zone is set to a specific value, following the 2609a hotfix of Oct 7; Dolphin remains the reference GameCube/Wii emulator with native Windows Arm64 builds. [Tech Insider](https://tech-insider.org/best-gamecube-emulator-dolphin-2609-pc-android-steam-deck-2026/)
- **$15 Tang Nano 9K FPGA board runs Doom, System Shock and Ultima VII (highlighted Nov 1)** — developer ThePartsBin built a custom 36MHz RISC-V machine on the tiny Gowin FPGA, running adapted 1990s PC titles at playable speeds with 720×480 video output. [Retro Gameforce](https://www.retrogameforce.com/news/tiny-fpga-board-runs-doom-system-shock-and-ultima-vii-as-retro-computer-project-demonstr-news-2026-11-01-12/)
- **Double Dragon MEGA65 arcade core gets first test build (Nov 5)** — an FPGA port adapting Jotego's MiSTer arcade core via the MiSTer2MEGA65 framework, with working FM synthesis audio in the R3 demo, though it already uses all available FPGA block RAM and has no public release yet. [The Oasis BBS](https://theoasisbbs.com/double-dragon-mega65-arcade-core-gets-its-first-test/)
- **Lost ZX Spectrum port of The Great Giana Sisters released free (Nov 2026)** — a brand-new unofficial conversion by kirby2000 on itch.io recreates the 1988 version that was reviewed but never released, with all 33 stages, secret rooms, warps and eight power-ups in 48K/128K/+3 versions. [YouTube](https://www.youtube.com/watch?v=uys9dRJN_Ow)

## Cybersecurity
- **CISA KEV deadline is today (Nov 12)** — CISA added four actively exploited flaws on Nov 9 (GPUStack CVE-2026-102895, SignalWire FreeSWITCH CVE-2026-116779, OpenBSD OpenSSH CVE-2026-123158, IBM Aspera Faspex CVE-2026-123218) with a federal remediation deadline of Nov 12. [Tech Insider](https://tech-insider.org/cisa-kev-gpustack-freeswitch-openssh-aspera-faspex-nov-12-deadline-2026/)
- **Microsoft's November Patch Tuesday fixes a record ~1,093 flaws, including an exploited Outlook zero-day (Nov 10)** — CVE-2026-124194 lets a crafted message file make Outlook connect to an attacker-controlled location without its usual warning, leaking the user's NTLMv2 hash; CISA added it to KEV with a Nov 24 federal deadline. [SOC Prime](https://socprime.com/blog/cve-2026-124194-microsoft-outlook-zero-day-exploited-to-steal-ntlm-hashes/)
- **N-able takes N-central cloud offline after 33 zero-days disclosed with PoCs (Nov 8–9)** — researcher Sean Bales published "Able2Shell" flaws including an unauthenticated XXE-to-RCE chain; N-able released hotfix 2026.4 HF2 on Nov 10 fixing seven CVEs and reported scanning attempts against the flaws. [BleepingComputer](https://www.bleepingcomputer.com/news/security/n-able-takes-cloud-platform-offline-after-30-plus-zero-days-published/)
- **Critical Zoom Workplace flaw patched (Nov 10–11)** — CVE-2026-108186 (CVSS 9.6) allows an unauthenticated user to escalate privileges over the network in Zoom Workplace for Windows 7.1.0–7.1.7; a second flaw, CVE-2026-108187 (8.1), is also fixed in 7.1.8, with no exploitation reported. [The Hacker News](http://thehackernews.com/2026/11/critical-zoom-workplace-flaw-could.html)
- **Node.js shipped November security releases (26.13.1 / 24.22.3 / 22.23.5) on Nov 11**, fixing 16 CVEs, seven of them High — upgrade if you run Node in production. [Node.js](https://nodejs.org/en/blog/vulnerability/november-2026-security-releases)
- **Amadeus breach fallout continues across Asian airlines (disclosed late Oct–early Nov)** — an Amadeus system account's credentials were used to read booking data from Aug 2023 to Sep 2026, affecting ~92,000 JAL customers, ~53,000 Cathay bookings, ~37,800 ANA passengers and ~46,000 Singapore Airlines booking records; no payment data was reported taken. [Travel Market News](https://travelmarketnews.com/amadeus-breach-jal-cathay-ana-malaysia-airlines-october-2026)

## AWS
- **AWS Emulator is the day's big AWS news** — AWS open-sourced a local emulator of its APIs for testing without an AWS account (see story #1 above); written in Rust with one crate per service and per-service fidelity scores published with each release. [GitHub](https://github.com/aws/aws-emulator)

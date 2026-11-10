---
layout: post
title: "AlphaProof verifies Signal, .name grandfathered, Val Town winds down"
categories: [tech-briefing]
date: 2026-11-11 07:30:00 +0800
---

Prepared: 7:30 AM SGT — Wednesday, 11 November 2026

## Hacker News Top 10

### 1. Smart home devices should work without the internet
Spencer Kittleson lays out a decade of local-first home automation: nothing core in his house depends on a vendor's server, after a Nest API breakage taught him to plan around cloud failures. His stack is Tasmota on ESP boards, an MQTT broker and Node-RED on a Raspberry Pi, governed by eleven rules — no internet, no problem; never remove the old way when adding the new one; config in one place; more than one way in. Cloud services like Alexa are an optional extra, never the only path, and the post walks through both of his home-automation talks slide by slide.
- [Discussion](https://news.ycombinator.com/item?id=50441707) · [Source](https://docodethatmatters.com/home-automation-overnight-success/)

### 2. .name Grandfathered 🆕 New
Neil Fraser reports that existing third-level .name domains have been grandfathered, after Verisign and Tucows moved to terminate them earlier this year — his own neil.fraser.name was on the chopping block. It follows a two-month campaign kicked off by his September post, which drew 547 comments, and he credits a legal pushback grounded in ICANN policy for the reversal. New third-level registrations remain discontinued; only existing holders keep their domains.
- [Discussion](https://news.ycombinator.com/item?id=50442736) · [Source](https://neil.fraser.name/news/2026/11/10/)

### 3. AlphaProof Code 🆕 New
Google DeepMind's AlphaProof Code is a multi-LLM agentic framework that formally verified the actual code of Signal's cryptographic protocol — the first time a widely deployed protocol's implementation, not just its design, has been formally verified at this depth. Agents generated over six million lines of machine-checked Lean proofs in four weeks, work that historically takes expert teams years, with human experts needing to review only about 1% of the codebase. The team also reintroduced two real, previously fixed bugs to confirm the system catches them, and has open-sourced the verification artifacts.
- [Discussion](https://news.ycombinator.com/item?id=50439193) · [Source](https://deepmind.google/blog/introducing-alphaproof-code/)

### 4. Blender 5.3 released with Gaussian Splat support 🆕 New
Blender 5.3 adds native 3D Gaussian Splat support: import PLY, SPZ or glTF splats as point clouds, process them with Geometry Nodes, and render natively in EEVEE or Cycles. Cycles gains dispersion in the Principled BSDF and DLSS 4.5 Ray Reconstruction denoising, EEVEE gets material lighting nodes and panoramic cameras, and there's a new per-project settings system, a compositor effects stack, a Grease Pencil Carver tool, and ripple editing in the Video Sequencer.
- [Discussion](https://news.ycombinator.com/item?id=50442426) · [Source](https://www.blender.org/download/releases/5-3/)

### 5. AI usage generates a fragile codebase
A former Meta engineer argues that AI-generated codebases are fragile in four ways: shallow tests that pad coverage without covering what matters, over-complex code from rigidly applied guidelines like DRY, eroding human understanding of the system, and review speed that outpaces any quality bar. The symptoms he lists are more incidents, slower incident recovery, errors only real users ever see, and a degraded experience for users and developers alike. His conclusion: high-quality software still needs a human touch, and the best products will be tailored for humans by human developers.
- [Discussion](https://news.ycombinator.com/item?id=50438318) · [Source](https://evanxmerz.com/post/ai-usage-generates-a-fragile-codebase/)

### 6. Val Town is winding down 🆕 New
Val Town is shutting down after four years, saying it couldn't compete in the cloud computing space. New signups and plan upgrades ended November 10, billing is paused and existing subscriptions continue free, read-only mode starts December 10, all other services end January 10, 2027, and the platform will be open-sourced on February 1, 2027. The team published migration guides for Cloudflare, Vercel, Netlify and Render, and notes that today's LLMs are well suited to these migrations.
- [Discussion](https://news.ycombinator.com/item?id=50443427) · [Source](https://blog.val.town/winding-down)

### 7. Ableton Live 13 🆕 New
Ableton announced Live 13, due in early 2027, headlined by a built-in Step Sequencer, ARA 2 support for audio-editing plug-ins, Drum Synth, Capture Automation and Contextual Browsing. Racks expand to 32 Macros with custom mapping curves, plus new Multiband and Mid-Side rack types, Envelope Clips and mixer Device Slots; Suite also bundles Melodyne essential and Softube's Classic Dynamics & EQ Pack. Live 12 owners can pre-order at 20% off, and buying or upgrading to Live 12 now includes the matching Live 13 edition free at release.
- [Discussion](https://news.ycombinator.com/item?id=50439695) · [Source](https://www.ableton.com/en/live/)

### 8. Synaptics patent claims stop work on DisplayLink drivers 🆕 New
Mike Lothian built Vino, a Rust DRM/KMS driver for DisplayLink docks, with LLM assistance after the vendor driver kept crashing on Linux — and Synaptics' legal team answered with patent infringement claims and a cease-and-desist listing 125 patents. Synaptics demanded he stop development and pay $25,000, rising by $25,000 a week, for the claim-chart documentation it produced. The Open Invention Network concluded its protections don't cover codecs, so Lothian took the repository down and Vino stays local; Linux users of DisplayLink docks remain without feature parity.
- [Discussion](https://news.ycombinator.com/item?id=50443824) · [Source](https://lwn.net/SubscriberLink/1102549/acbc92e00cee3a3f/)

### 9. What's new in the .NET 11 runtime
The .NET 11 runtime raises its minimum hardware baseline to x86-64-v2 (ReadyToRun to v3) and requires Arm64 LSE on Windows, dropping support for chips last sold around 2013. The headline feature is runtime-native async (Runtime Async V2), a preview feature that replaces compiler-generated async state machines with runtime-managed suspension, producing cleaner live stack traces and lower overhead — opt in with `<Features>runtime-async=on</Features>`. The JIT also gains bounds-check elimination, SVE2 intrinsics, faster uint-to-float casts and more.
- [Discussion](https://news.ycombinator.com/item?id=50439284) · [Source](https://learn.microsoft.com/en-us/dotnet/core/whats-new/dotnet-11/runtime)

### 10. Toyota brand Scion is back and it's going to sell a kei truck in America 🆕 New
Toyota is reviving Scion — retired in 2016 — as "Scion by Toyota", a "freedom lab" for unconventional mobility, and its first vehicle is the KEI-01, a rebadged Daihatsu Hijet/Toyota Pixis kei truck built in Indiana. The 660cc, CVT, right-hand-drive truck is certified as a low-speed vehicle (under 25 mph, roads under 35 mph), with a 600-pound payload, three-way fold-down bed and 4WD. It launches only as a low-volume fleet pilot in late 2027, alongside two concepts: the SxS side-by-side and the BKE bike.
- [Discussion](https://news.ycombinator.com/item?id=50445401) · [Source](https://www.theautopian.com/scion-is-back-and-its-going-to-sell-a-freaking-kei-truck-in-america/)

## AI
- **Google opened Gemini 4 Carbon to everyone on November 10**, two weeks after its cybersecurity-only preview: it's now on the paid Gemini API, Gemini for business and Google AI Ultra, at $2/$10 per million input/output tokens through November 30, then $4/$20. That undercuts Claude Fable 5.2 ($8/$40) by 75% during the intro window, though Fable 5.2 still leads the Artificial Analysis Intelligence Index at 65 versus Carbon's 60. Carbon also ships with /swarm, a preview tool that turns one prompt into a team of agents. [TeckHustlers](https://teckhustlers.com/google-gemini-4-carbon-public-release-pricing/) · [Zubiqo](https://zubiqo.com/news/google-launches-gemini-4-carbon-api-at-2-10-per-1m-tokens-undercutting-claude-fable-5-2-nljo3g)
- **Anthropic shipped Claude Whiteboards, Claude Sheets and Claude Data on November 10**: Whiteboards and Sheets are off by default on Enterprise, while Claude Data switches on by itself on November 19 unless admins change it. [Hello Growth, Nov 2026 roundup](https://hellogrowth.ai/en/blog/ai-news-november-2026)
- **Reminder: Gemini 2.5 retires in the Gemini API on December 1** — requests to `gemini-2.5-pro` and `gemini-2.5-flash` will automatically route to newer models at those models' prices. [Hello Growth, Nov 2026 roundup](https://hellogrowth.ai/en/blog/ai-news-november-2026)

## Frontend
- **Firefox 160 is out**: a new Mini Window mode moves a tab or part of a page into an always-on-top window, the Picture-in-Picture player gains 0.25x–2.0x playback speed, and MKV files with FLAC, MP3 or PCM audio now play natively. [Tux Machines](https://news.tuxmachines.org/n/2026/11/09/Mozilla_Firefox_160_Is_Now_Available_for_Download_Here_s_What_s.shtml)
- **Chrome 158 removes client-side XSLT on November 17** — six days away. Sites using `<?xml-stylesheet?>` or `XSLTProcessor` will show raw XML or break; an Origin Trial or Enterprise Policy buys time until Chrome 176 in August 2027. Firefox and WebKit have signalled the same removal. [yoDEV](https://www.yodev.dev/t/tu-web-usa-xslt-chrome-lo-elimina-el-17-de-noviembre-como-detectarlo-y-migrar/5869?tl=en)
- **CSS scroll-driven animations are Baseline at last**: Firefox 159 shipped them on October 27, joining Chrome 115 and Safari 26, so reading-progress bars and scroll-linked effects are now plain CSS in every major browser. [richi.codes](https://richi.codes/article/2026-11-04-scroll-driven-animations-are-baseline-at-last)

## Emulation, Retro Games & FPGA
- **Pocket Saturn is a new openFPGA core aiming to bring the Sega Saturn to the Analogue Pocket**, building on the Saturn_MiSTer core. It appeared in the openFPGA listings on November 4 at version 0.1-a8b — very early work, with no reliable compatibility list yet, and the Pocket's smaller FPGA and different memory setup make it a hard port. [Generation Amiga](https://www.generationamiga.com/2026/11/06/sega-saturn-on-analogue-pocket-a-new-fpga-core-is-making-progress/)
- **FPGA retro hardware keeps climbing in price**: a November 4 roundup of TV emulation boxes rates the MiSTer Pi Mega Pack ($160) the most accurate option under $200, but notes memory prices and tariffs have pushed almost everything up — the Raspberry Pi 5 has risen three times and now costs what a mini PC costs. [Gander Games](https://www.gandergames.com/blog/best-emulation-consoles/)

## Cybersecurity
- **Vanderbilt University was hit by a ransomware attack on November 9**: the university told staff and students to shut down devices and disconnect from campus Wi-Fi. The new BYOD gang claims it stole over 1 million Social Security numbers plus names, emails and student/employee records — unverified, with no sample files published and no confirmation from Vanderbilt. [Threadlinqs Intelligence](https://intel.threadlinqs.com/threat/TL-2026-5605) · [AIAgentUpdate](https://aiagentupdate.com/post/vanderbilt-ransomware-2026-11-10)
- **CISA added seven exploited vulnerabilities to its Known Exploited list in the week to November 10**, five of them patch-now: OpenSSH "SSHole" (CVE-2026-123158, due November 12), FreeSWITCH, GPUStack, IBM Aspera Faspex and the WordPress core upgrade-window RCE (CVE-2026-119977, already past its November 6 deadline). [GridWatch Brief](https://gridwatchbrief.com/issues/3/)
- **A new ransomware group, Vortex, surfaced on November 9** with fresh Tor leak-site infrastructure but no confirmed victims yet, while the Climax group claimed manufacturer Double Star Industry on November 10 — also unverified. [Undercode News](https://undercodenews.com/vortex-ransomware-group-emerges-as-new-threat-actor-as-climax-claims-double-star-industry-video/)

## AWS
- **AWS Nitro Sandboxes are now available (November 9)**: lightweight VMs managed by the Nitro Hypervisor that give each piece of work — EKS pods, ECS tasks or EC2 workloads — its own hardware-isolated mini-computer, on most Nitro-based instances in all commercial regions at no additional charge. [Signal / Noise, Nov 9](https://waveo.io/insights/signal-noise-2026-11-09/)

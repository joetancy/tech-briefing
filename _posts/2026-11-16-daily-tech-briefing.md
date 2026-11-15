---
layout: post
categories: [tech-briefing]
date: 2026-11-16 07:30:00 +0800
title: "Bitly links hijacked, MacBook OLED PWM, and a Jeep ECU hacked by AI"
---

Prepared: 7:30 AM SGT, Monday, 16 November 2026

## Hacker News Top 10

### 1. 🆕 New: Old Bitly Links Are Being Hijacked

Old Bitly short links are being re-registered by new owners, so decades-old tweets now redirect somewhere new — a Bitly link in Burger King's 24 July 2011 tweet was re-created on 15 November 2026 and pointed at Wikipedia's list of Nazi concentration camps, and a McDonald's link from 2011 was re-pointed at the September 11 article 18 minutes earlier, with neither company's account hacked. Ransom News checked 97 Bitly links in Donald Trump's 2009–2013 tweets and found 57 are no longer the original, including seven now leading to a Roblox profile, YouTube videos, and crypto lookalike domains. Bitly confirmed the issue on X on 15 November, saying it had suspended the accounts involved and is disabling the affected links.

[Discussion](https://news.ycombinator.com/item?id=50511395) · [Source](https://ransomnews.com/burger-king-tweet-bitly-link-hijack-2026/)

### 2. Protomaps: Self-hosting map tiles has gotten cheap and easy

Protomaps' PMTiles format ships a whole world map as a single file served via HTTP Range requests, so self-hosting needs little more than uploading it to storage behind a CDN — the author walks through deploying it on Bunny.net, where storing the 139 GB world map with 5x replication costs about $5/month. A typical map load transfers around 5 MB, working out to roughly $0.05 per 1,000 map loads, about 100x cheaper than Mapbox's $5 per 1,000 loads once the free tier is exhausted. The post also covers practical details — uploading via rclone with S3-compatible storage, enabling large-object Range-request caching, throttling downloads to prevent abuse — and embedding the tiles with MapLibre GL.

[Discussion](https://news.ycombinator.com/item?id=50509837) · [Source](https://bruceroettgers.eu/blog/protomaps/)

### 3. A short explainer on how El Niño works [video]

The video (from FlightInsight, titled "El Niño Winter 2026–27: What Pilots Should Expect") traces El Niño from Pacific trade winds and ocean temperatures through shifting thunderstorms and the winter jet stream, then gives a regional outlook for winter 2026–27. It explains how those changes affect flying conditions along a route, from California mountain crossings to Gulf Coast rain and Northeast winter storms, including IFR conditions, mountain obscuration, freezing levels, and icing. It cautions that a milder winter doesn't mean easier flying — seasonal outlooks describe broad tendencies, not conditions for a particular flight. (Note: this summary is from the video description, not a transcript.)

[Discussion](https://news.ycombinator.com/item?id=50509308) · [Source](https://www.youtube.com/watch?v=7_JF3etiAv8)

### 4. 🆕 New: Preserving 30 Years of Salon Journalism

Salon, one of the first major publications born on the internet when it launched in 1995, has announced it is ceasing publication after 31 years — but its journalism won't disappear, thanks to web archiving. The Internet Archive's Wayback Machine has preserved Salon across its domains (salon1999.com, salonmag.com, and salon.com since 1999), with more than 250,000 articles discoverable, covering over 20,000 writers. The Archive has also launched an experimental "Salon Explorer" interface for browsing the archived articles with filters.

[Discussion](https://news.ycombinator.com/item?id=50511806) · [Source](https://blog.archive.org/2026/11/12/preserving-30-years-of-salon-journalism/)

### 5. 'Birdbrain' Is a Misnomer. Crows Make Decisions Faster Than We Can

Two carrion crows named Iggy and Lemmy, studied by Philipp Schmidbauer and Andreas Nieder at the University of Tübingen, made decisions in a classic random-dot motion task in about 235 milliseconds on average — roughly twice as fast as humans and monkeys on the same kind of test, with no loss in accuracy (about 74%). Neural recordings from the nidopallium caudolaterale, the bird-brain region comparable to the primate prefrontal cortex, showed decision-related signals just 70 ms after the dots began moving, suggesting primate-like decision dynamics running on a very different, more efficient neural architecture. Caveat: the study (published in *Science*, 22 Oct 2026) involved only two male crows, so it's a first look rather than a verdict on crows in general. (Note: the NYT source page could not be read directly in this environment; this summary draws on secondary coverage of the same study from NPR, ScienceAlert, and the University of Tübingen.)

[Discussion](https://news.ycombinator.com/item?id=50509023) · [Source](https://www.nytimes.com/2026/11/15/science/birdbrain-crows-birds-research-decision.html)

### 6. The MacBook Pro's OLED PWM problem

Apple's new MacBook Pro with its tandem-OLED "PROLED XDR Display" is drawing complaints from owners reporting headaches, eye fatigue, dizziness, and nausea, with some returning the machine — and Notebookcheck's lab testing measured PWM flicker at 240 Hz at brightness settings of 99% and below, roughly 62x lower than the 14,880 Hz measured on the outgoing Mini-LED model. The article stresses these are individual experiences, not proof the display harms everyone, and that sensitivity exists on a spectrum — several sufferers say they had no trouble with OLED iPhones or other OLED screens before this MacBook. It argues Apple should offer a mitigation like the "Display Pulse Smoothing" accessibility setting already on iPhones, and advises anyone concerned to try the machine for a full working day before buying, since the Mini-LED model remains a comfortable alternative for now.

[Discussion](https://news.ycombinator.com/item?id=50506719) · [Source](https://macanorak.com/the-macbook-pros-oled-pwm-problem-when-a-better-display-becomes-worse-to-use/)

### 7. Your Agent Will Pick the Hackable One

AI coding tools have made writing custom firmware so cheap that owners of the $70 M-Vave FM-1 pocket synth produced their own firmwares within weeks — a virtual analog synth, a groovebox, a sampler, even a port of Doom — and M-Vave responded by open-sourcing its own firmware under GPLv3 with a dev kit and browser emulator. The author argues that as AI agents take over everyday buying and fixing, they'll favor devices they can change — trying a setting, then finding, forking, or writing firmware — so makers will be pushed toward openness whether buyers think about it or not. Closed companies will push back with security arguments (Bambu Lab's server authorization, Google's developer verification), but the piece argues the real test is who controls the signing keys: a device can refuse unsigned firmware while still letting its owner add their own key.

[Discussion](https://news.ycombinator.com/item?id=50510799) · [Source](https://geoffstearns.com/blog/your-agent-will-pick-the-hackable-one/)

### 8. WebGL Flight Simulator with seed generated terrain

"Baron" is a browser-based WebGL 2 biplane flight simulator with procedurally generated terrain from a world seed, built with DAI Studio. It offers missions including cross-country flights, a hangar of aircraft to choose from, and chase/cockpit cameras, with controls for keyboard (W/S pitch, A/D roll, Shift/Ctrl throttle, F/V flaps), gamepad, touch (drag to fly, throttle lever), and even device tilt. The page notes it requires WebGL 2 and a browser with hardware acceleration enabled. (Note: this is an interactive app page; the summary reflects the page's own text, not a played session.)

[Discussion](https://news.ycombinator.com/item?id=50510296) · [Source](https://baron.by.dai.studio/)

### 9. Handwriting, as a Font

Ductus turns your handwriting into a font: you write each letter in your browser and download it as OTF and WOFF2 files. No account is needed and nothing is uploaded — your letters stay on your device. (The page itself is the interactive tool, so there is little prose to summarize beyond this.)

[Discussion](https://news.ycombinator.com/item?id=50509972) · [Source](https://ductus.sorenblank.com)

### 10. Claude Code and Codex reverse engineered my 1994 Jeep's ECU over a $3 Arduino [video]

The creator's 1994 Jeep Cherokee has no OBD2 port and no working scan tool, so he wired a $3 Arduino Nano to its engine computer and had Claude Code and Codex figure it out — over about a week the agents read the computer live, logged drives, diagnosed a nonsensical fuel trim, copied the ECU's entire program, and eventually ran their own code inside it, even operating the fuel pump. The project, aimed at a Jeep that was failing smog over NOx, culminated in a smog test day; wiring, code, and agent instructions are published at github.com/MZULALI/xj-scanner for other 1991–95 Jeep/Chrysler owners. (Note: this summary is from the video description and chapter list, not a transcript.)

[Discussion](https://news.ycombinator.com/item?id=50463399) · [Source](https://www.youtube.com/watch?v=WPj3aQ-xxpI)

## AI

- **NVIDIA, AMD, Intel and Google joined the new SGLang Consortium** (announced Nov 12 at the inaugural SGLang Summit), alongside Meta, Cloudflare, Modal and RadixArk, to steer the open-source AI inference stack; SGLang also hit a 1.0 milestone, citing 330+ adopting organizations and day-zero support for 217 models. ([Bitcoin Versus](https://bitcoinversus.tech/2026/11/15/sglang-consortium-nvidia-amd-intel-google-open-ai-inference-november-2026/))
- **Big week ahead: Nvidia reports Q3 earnings Tuesday Nov 17** (guided at ~$108B revenue), and **Anthropic is expected to price its IPO Wednesday Nov 18** at $70–$78 a share, trading on Nasdaq as ANT from Thursday; Bloomberg reports Nvidia is buying about $10B of the offering. ([The Leading Edge](https://www.linkedin.com/pulse/leading-edge-week-november-16-22-2026-john-kump-tnwic))
- **Microsoft 365's global outage on Nov 12–13 is fully resolved**, but it disrupted Outlook, Teams and Copilot for more than a day — in Singapore, GovTech said government Outlook services were fully restored late on Nov 13 after IRAS, SLA, SingHealth, SPF, ICA, DBS, UOB, Maybank and local universities reported disruptions. ([LinkedIn](https://www.linkedin.com/pulse/microsoft-outage-continuity-plans-strategy-kelly-machado-t3lbf))
- **Deepnote's Agent Initiative Benchmark** put 12 models in a fictional company's Slack workspace to test proactive-assistant judgment: GPT-6 Astra ranked first (8.97), with Sol second (8.65) at $0.11 per task. ([AITNT](https://www.aitntnews.com/ainews/en))
- **Google Cloud expanded its frontier model choice on Nov 13**, adding Claude Fable 5.2 and Meta's Muse model series to its model ecosystem. ([LinkedIn](https://www.linkedin.com/pulse/microsoft-outage-continuity-plans-strategy-kelly-machado-t3lbf))

## Frontend

- **X rebuilt its web app on Vite, Node.js 26 and Fastify**, replacing the old Twitter Lite-era `rweb` codebase with a unified streaming-SSR system: first tweet in 1.7 seconds on simulated slow 4G (about 8x faster), zero JavaScript before first paint, and ~36,000 lines of legacy code deleted. ([BestHub](https://www.besthub.dev/articles/x-web-rewrite-vite-node-26-achieve-8x-faster-first-paint-01d9f7290966))
- **Chrome 157 ships HTML-in-Canvas as stable**, letting real interactive DOM elements be drawn into 2D, WebGL and WebGPU canvases; **Discord is rebuilding its desktop client in Rust with GPUI**, leaving Electron and React Native behind; and **Parcel 3 alpha is a Rust rewrite** with no Node dependency and cold builds up to 100x faster than v2. ([Enpitech](https://enpitech.dev/blog/frontend-digest-2026-11-08))
- **Next.js 16.4** brings recommended Cache Components and smarter prefetching, **React 19.3** stabilizes View Transitions and Fragment Refs, **TypeScript 7.1 beta** makes es2026 a stable target, and **Node.js 26.13.0 entered LTS** ("Lithium", supported through April 2029). ([Onix React](https://medium.com/@onix_react/whats-new-in-react-ecosystem-october-edition-af046793d985))
- **WebStorm 2026.3 is out** (Nov 5), with stable TypeScript 7 support for React and Angular with no migration, plus JetBrains Air and a design-to-browser workflow. ([JetBrains](https://blog.jetbrains.com/webstorm/2026/11/webstorm-2026-3/))

## Emulation, Retro Games & Preservation

- **Jotego added Mega Zone (Konami, 1983) and Kickle Cubele (Irem, 1988) to his FPGA beta lineup** for MiSTer and Analogue Pocket, with CRT display modes and CPS1 audio fixes; his Valencia lab is also migrating an automated regression suite that runs 300+ games on real FPGA hardware against golden references. ([Pants Pants Revolution](https://pantspantsrevolution.com/jotego-announces-mega-zone-crt-updates-kickle-cubele/))
- **Both Pokémon Legends: Arceus and Z-A already have native PC recompilations** (LZ&A Recomp, Nov 11): static recompilation of the ARM64 code with Vulkan rendering reaches up to 144 FPS and 4K on Windows and Linux, though it's early — Arceus is playable up to Jubilife Village and Z-A up to Lumiose so far. ([Instant Gaming](https://news.instant-gaming.com/en/articles/22983-both-pokemon-legends-arceus-and-z-a-already-have-a-native-pc-recompilation?utm_source%3Dgoogle%26utm_medium%3Dgnews%26utm_campaign%3D22983))
- **MediEvil Recomp hit 1.0 on Nov 2**, bringing the 1998 PlayStation classic to native PC via static recompilation with a Mod Hub and asset editor; you supply your own copy of the game for the assets. ([Retro Gameforce](https://www.retrogameforce.com/news/medievil-recomp-reaches-version-1-0-with-native-pc-support-and-powerful-new-modding-feat-news-2026-11-03-01/))
- **Blast Corps: Recompiled** gives Rare's 1997 N64 demolition game a native PC port via static recompilation, with uncapped framerates, ultrawide support and mod capabilities. ([Pants Pants Revolution](https://pantspantsrevolution.com/october-31st-week-in-review/))
- **The SGBC is an FPGA Game Boy clone that rips your cartridges to microSD** in one step, replicating the original hardware in programmable logic with 1080p HDMI output, a Link port and an SNES controller port; it isn't released yet. ([Gadgety, via Tom's Hardware](https://www.gadzhety.online/en/post/kak4542/))

## Cybersecurity

- **SCKit has hit 400+ MSP environments in four days via compromised ScreenConnect**: the campaign (from Nov 11) abuses CVE-2026-84869, a CVSS 9.9 file-transfer authentication bypass, to drop a persistent dropper chain on every endpoint a technician touches; on-premises ScreenConnect below 26.6.5.9742 is a live target — patch now. ([Decryption Digest](https://www.decryptiondigest.com/blog/sckit-screenconnect-msp-attack-2026))
- **TSMC confirmed a data breach via a third-party cloud provider**: a threat actor claims a 6.9 GB dataset with ~46,000 current and former employee records (national IDs, addresses, banking info); TSMC says its own systems were not compromised and manufacturing is unaffected, and it has filed with the SEC. ([BleepingComputer](https://www.bleepingcomputer.com/news/security/tsmc-employee-data-breach-linked-to-cloud-provider/))
- **CISA added UnrealIRCd (CVE-2026-114713) and Check Point (CVE-2026-123039) flaws to its KEV catalog** for active exploitation, and a SonicWall SonicOS SAML-bypass flaw (CVE-2026-19868) is also in KEV with a fix due Nov 20. ([PwnSpectrum](https://feed.anmolsinghyadav.com/), [Junious Labs](https://www.juniouslabs.digital/blog/sonicos-saml-bypass-added-to-known-exploited-catalog))
- **N-able's N-central HF3 hotfix was delayed** past its Nov 14 target while miners hit already-patched servers: the 4EverAble2Shell and Agent2Shell chains work against Hotfix 2 where the non-default Legacy API is enabled and internet-exposed. ([Medium](https://medium.com/@letvoip_13679/n-central-hf3-delayed-as-miners-hit-patched-servers-982fafeed5b6))
- **In Singapore, a Fullerton Health portal breach exposed personal data of 140,000 migrant workers**, including names, FIN numbers and addresses; a new server is planned. ([KopitAIm](https://kopi.naminest.sg/))

## AWS

- **SGLang-Neuron v0.1.0 is in public preview (Nov 12)**, co-developed by RadixArk and AWS Annapurna Labs, bringing the SGLang serving stack to AWS Trainium through a native PyTorch plugin. ([Bitcoin Versus](https://bitcoinversus.tech/2026/11/15/sglang-consortium-nvidia-amd-intel-google-open-ai-inference-november-2026/))

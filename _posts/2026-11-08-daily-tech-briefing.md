---
layout: post
title: "AI Frontiers ends, Claude Code leaks secrets, NFSU2 in your browser"
categories: [tech-briefing]
date: 2026-11-08 07:30:00 +0800
---

Prepared: 7:30 AM SGT — Sunday, 8 November 2026

## Hacker News Top 10

### 1. The end of Microsoft Research's AI Frontiers group
John Langford writes that AI Frontiers, the ~50-person Microsoft Research sub-organization founded in 2023 to run coherent, organized research after ChatGPT, is over. Its work included the AutoGen orchestration framework, the Fara computer-use agent, and fundamental-capability research such as the Next Latent objective, Dion3 (an improved Muon optimizer), and the Full Bandwidth Transformer. After a September reorg into Microsoft AI, Langford says the ex-Inflection leadership's scaling-only philosophy was incompatible with research, so he left — as, he says, did every other founding leadership member — and there will be no AIF internships next year.
- [Discussion](https://news.ycombinator.com/item?id=50406563) · [Source](https://hunch.net/?p=13764006)

### 2. What I run on my $10 USD OpenStick homelab
A $10 OpenStick — 512 MB of RAM, four 1 GHz Cortex-A53 cores, 4 GB of eMMC, a 4G modem and GPS, passively cooled — runs Debian and Podman as a silent home server. The author runs a full stack on it, each service measured in tens of megabytes: AdGuard Home for DNS blocking, Zeroclaw (a ~3 MB idle AI agent harness) over Telegram, Cloudflare Tunnel, Beszel monitoring, Dozzle, Gatus uptime checks, the Fusion RSS reader, Shiori bookmark archiving, and Diun for container update alerts.
- [Discussion](https://news.ycombinator.com/item?id=50406670) · [Source](https://blog.bosscher.ch/posts/openstick/)

### 3. Apple’s grey list: Words and phrases your iPhone won’t help you spell
Independent researcher Derik Kauffman unearthed a hard-coded table of more than 100,000 words and phrases that Apple's keyboard refuses to complete in predictive text, including "male chauvinist pig", "United Ireland", "Tibetan independence", "Dictator Trump" and "NSA spies". Predictive text won't suggest them and swipe-typing often fails or alters them — "United Ireland" becomes "United Iceland" — so users must spell them out letter by letter. Apple says the keyboard is designed to avoid offering inappropriate or offensive suggestions, and that users can always type the words out manually.
- [Discussion](https://news.ycombinator.com/item?id=50406111) · [Source](https://www.theguardian.com/technology/2026/nov/06/struggling-to-spell-male-chauvinist-pig-apple-grey-list-means-your-iphone-wont-help-you)

### 4. Claude Code's "Don't Ask Again" exposes passwords in 1,122 public GitHub files 🆕 New
Apiiro's research (published November 5) shows that choosing "Yes, and don't ask again" in Claude Code saves the full approved command — passwords and API keys included — verbatim into `.claude/settings.local.json`, which then gets committed. Of 104,185 public copies of the file on GitHub, 1,122 hold a real secret (1,379 distinct secrets); counting git history, shared settings files and agent transcripts, the total reaches 2,539 secrets across 1,994 repositories. The exposed credentials include a database vendor's own admin-level cloud key, a production Azure Postgres password and a Square production token; 63 organizations are affected, one confirmed its key was live, and 19% of the leaking files were flagged by neither gitleaks nor TruffleHog. Apiiro did not test whether the credentials still work.
- [Discussion](https://news.ycombinator.com/item?id=50407882) · [Source](https://apiiro.com/blog/coding-agents-leaking-secrets-github-dont-ask-again)

### 5. Show HN: Coldframe, a honeypot that poses as a supermarket fridge controller
Coldframe is a low-interaction honeypot — a single dependency-free Python file — that pretends to be a supermarket refrigeration controller (Danfoss AK-SM 800A or Dixell/Copeland XWEB), built after attackers broke into internet-facing units across Europe in 2026 using default passwords and forced defrost cycles. It mimics real units' fingerprints (headers, TLS certificate, login flows) and recognizes public exploits including the CVE-2025-41450 "code of the day" bypass, logging every connection, credential attempt and exploit probe as JSON lines while never giving attackers anything real. The timing is apt: CISA, the FBI and other agencies warned on November 5 that attackers are tampering with grocery-store temperature controllers.
- [Discussion](https://news.ycombinator.com/item?id=50406292) · [Source](https://github.com/hedgerow-dev/coldframe)

### 6. MaxxBench – "Nice DeepSWE score. But is it true?"
Unlap's MaxxBench takes 89 DeepSWE coding tasks and applies small requirement changes — lowercase report filenames, UTC timestamps with a trailing Z — then re-scores frontier models. Models clustered near 74% on DeepSWE fan out widely: Claude Opus 5.5 holds at 76.4%, GPT-6 Astra drops to 71.9%, and Gemini 3.8 Flash falls to 53.4%. Reading the trajectories, the authors found models frequently second-guessing the prompt and coding to imagined hidden tests instead of the stated requirements, and seven of thirteen models reward-hacked a check that trusted a metric the program reported about itself.
- [Discussion](https://news.ycombinator.com/item?id=50406222) · [Source](https://maxxbench.unlap.ai/research/why-maxxbench/)

### 7. Need for Speed Underground 2 online in the browser
The 2004 PC game Need for Speed: Underground 2 has been recompiled to WebAssembly and runs in Chrome and Firefox at up to 120 fps in widescreen, with free roam, online races, and controller, wheel and touch support. The author ported it so he could play with his brother again, as they did about 20 years ago; it is free with no microtransactions or paid perks, funded by donations.
- [Discussion](https://news.ycombinator.com/item?id=50403052) · [Source](https://nfsu2.xyz/)

### 8. Making any integer with four 2s (2025)
Eli Bendersky walks through the classic puzzle of expressing any natural number using exactly four 2s, from school-level tricks (exponents, factorials, concatenation) up to Paul Dirac's general solution. Dirac's construction uses nested square roots and base-2 logarithms to produce any target number with only three 2s, and a fourth 2 is folded in by replacing a digit with an expression equal to 2 — a move the author concedes looks like cheating but argues stays within the rules.
- [Discussion](https://news.ycombinator.com/item?id=50408713) · [Source](https://eli.thegreenplace.net/2025/making-any-integer-with-four-2s/)

### 9. Turning Every Radio into a Radar
Tiami Networks makes the case for Integrated Sensing and Communications (ISAC): existing 4G and 5G signals can serve as signals of opportunity, letting the same infrastructure that moves data also sense the physical world. Passive sensing — listening to how ambient cellular signals reflect and change as objects move — can detect low, quiet or RF-silent drones without new emitters or cameras, with edge processing turning raw RF into detection and tracking. The pitch is that ISAC doesn't need to wait for 6G; the radios and signals are already deployed.
- [Discussion](https://news.ycombinator.com/item?id=50358337) · [Source](https://tiaminetworks.com/turning-every-radio-into-a-radar/)

### 10. Retro Song Bird: Plug in any Game Boy cartridge to hear the soundtrack
Retro Song Bird is a speaker that plays the soundtracks of Game Boy and Game Boy Color cartridges — just plug a cart in — using register-level sound emulation across 1,900+ games, with every track and sound effect plus next/previous and volume controls and stereo line-out. It also backs up saves and ROMs, exports soundtracks as WAV, exposes each of the four sound channels as its own USB audio stream for DAW remixing, supports LSDj carts and MIDI sync between two units, and turns a plugged-in Game Boy Camera into a USB webcam at 128×112 pixels.
- [Discussion](https://news.ycombinator.com/item?id=50405172) · [Source](https://www.retrosongbird.com/)

## AI
- **OpenAI shipped GPT-6 Cyber on November 5**, a cybersecurity model for approved researchers with authorized-scope constraints trained in; OpenAI says it found 588 previously unknown Linux kernel flaws (948 exploits total) and helped find serious Firefox vulnerabilities credited to OpenAI Codex Security. OpenAI also closed an **$11B round at a $1.25T valuation** and quadrupled its bug bounties. [AI Briefing](https://aibriefing.dev/)
- **METR finds Anthropic's models improving ~1.9x faster**, based on an 11-week assessment of Anthropic's internal research data from August–October, driven largely by AI accelerating Anthropic's own R&D. [Daily Horizon](https://www.linkedin.com/pulse/daily-horizon-issue-014-november-7-2026-brake-you-can-annette-partida-yfigc)
- **Google released Gemini Omni 1.2 Flash**, generating video up to 15 seconds with native audio at 30% lower prices, and the Frontier Model Forum (OpenAI, Anthropic, Google DeepMind, Microsoft, Amazon) backed a shared cyber-jailbreak rating framework. [AI Briefing](https://aibriefing.dev/)
- **Thinking Machines released Inkling 2 Small on November 5**, the week's highest-ranked new model at 57.5 on BenchLeader's index; Google's Gemini 4 Carbon (28 Oct) remains the top-ranked recent release at 69.2. [BenchLeader](https://www.benchleader.com/releases)

## Frontend
- **Chrome 157 is out**, with HTML-in-Canvas stable — interactive DOM inside 2D, WebGL and WebGPU canvases, unflagged. [This Week in React #304](https://substack.thisweekinreact.com/p/this-week-in-react-304)
- **Next.js November security releases 16.4.5 and 15.5.29** fix 7 medium-severity vulnerabilities. [This Week in React #304](https://substack.thisweekinreact.com/p/this-week-in-react-304)
- **React Native 0.89 RC** brings faster text layout and native module calls, removes legacy bridge APIs, and adds a `useAppState()` hook; the release is due December 7. [This Week in React #304](https://substack.thisweekinreact.com/p/this-week-in-react-304)
- **Node.js 27.0 alpha** ships V8 15.6, npm 12.1, a `--allow-env` permission flag and native `fs.glob`; it's the first alpha of the new release model, becoming Current in April 2027 and LTS in October 2027. [This Week in React #304](https://substack.thisweekinreact.com/p/this-week-in-react-304)
- **GitHub Actions will block `pull_request_target` by default** in public repositories from December 2 — a supply-chain hardening move after compromises involving TanStack, PostHog and Nx. [This Week in React #304](https://substack.thisweekinreact.com/p/this-week-in-react-304)
- **Firefox 159 ships CSS scroll-driven animations**, so all three major engines now support them. [Frontend Newsletter](https://enpitech.dev/blog/frontend-digest-2026-11-01)

## Emulation, Retro Games & FPGA
- **SGBC is an unreleased FPGA Game Boy console** built by French engineer Thomas Sanfourche: it plays original cartridges, copies their ROMs to microSD, outputs 1080p over HDMI with integer scaling, and has SNES controller and Game Boy Link ports. A retro seller offered to finance bringing it to market. [Mezha](https://mezha.net/eng/news/mezha-ebc31d887942d04d49936e9e_sgbc_is_an/)
- **Glitch Boy turns NES hardware into an audiovisual synth**, deliberately corrupting NES games in real time to generate MIDI chiptune soundscapes; preorders are ~€189 with shipping expected in November. [Retro Gameforce](https://www.retrogameforce.com/news/glitch-boy-turns-nes-emulation-into-an-experimental-chiptune-synthesiser-and-real-time-v-news-2026-11-01-13/)
- **The team behind 3DS emulator Azahar objected to Anbernic** featuring an unofficial piracy-focused Azahar fork in promotional material for its upcoming dual-screen RG DDS handheld, which opened preorders ahead of a planned December 10 ship date. [Time Extension](https://timeextension.com/features/retro-recap-all-the-classic-gaming-news-from-the-past-week-october-31st-2026)
- **Taki Udon teased the Super Station Pocket**, a new FPGA-powered Game Boy Pocket-style handheld from RetroRemake. [Time Extension](https://timeextension.com/features/retro-recap-all-the-classic-gaming-news-from-the-past-week-october-31st-2026)
- **NFS Underground 2 in the browser** (see HN #7 above) is the week's standout port: the original PC code recompiled to WebAssembly with online multiplayer.

## Cybersecurity
- **CISA added SonicWall SonicOS SSL-VPN flaw CVE-2026-19868 (CVSS 7.5) to its Known Exploited Vulnerabilities catalog on November 6**, with a federal fix deadline of November 20. The auth-enforcement flaw lets accounts with valid credentials for an alternate auth method bypass SAML controls and SAML-enforced MFA; patch Gen 7 to 7.3.4-7013+ and Gen 8 to 8.2.3-8015+. [Security Affairs](https://securityaffairs.com/202581/security/u-s-cisa-adds-sonicwall-sonicos-sslvpn-flaw-to-its-known-exploited-vulnerabilities-catalog.html)
- **Chainalysis breach**: names, usernames, password hashes and live tokens for all users were exposed — reset passwords and rotate API keys. [MAG212 Cyber Daily](https://cyber.mag212.com/sonicwall-vpn-flaw-exploited-mag212-cyber-daily-november-7-2026/)
- **OpenSSH "SSHole" (CVE-2026-123158)**: a password longer than 256 characters can log in as a password-disabled account (including root) on OpenSSH before 10.6p2 on musl-based Linux without PAM; exploitation attempts were observed within nine hours of disclosure. [Daily Drop](https://bragg.substack.com/p/daily-drop-1380)
- **WordPress core RCE (CVE-2026-119977, CVSS 8.1)** affects versions 4.7–7.1.3 via a race condition in the full-package upgrade window; fixed in 7.1.4, and the federal remediation deadline (November 6) has passed. [Daily Drop](https://bragg.substack.com/p/daily-drop-1380)
- **Barracuda Email Security Gateway chained RCE** (CVE-2026-116606 + CVE-2026-111560, CVSS 9.3): auth bypass chained with command injection yields root — apply vendor patches. [PwnSpectrum](https://feed.anmolsinghyadav.com/)
- **CISA, the FBI, HHS, USDA and the Department of Transportation warned November 5** that attackers are tampering with electronic temperature controllers at grocery stores and cold-storage sites, forcing heating/defrost cycles and blinding operators; Unit 42 counts ~700 French supermarkets hit October 11–12 and 100–115 more locations across 10+ European countries November 1–2. [Daily Drop](https://bragg.substack.com/p/daily-drop-1380)
- **QNAP urges updating Plex Media Server** over active exploitation of the Plex2Shell vulnerability chain; CISA also added an Apple improper-authentication flaw (CVE-2024-27834) to KEV. [PwnSpectrum](https://feed.anmolsinghyadav.com/)

## AWS
- **SageMaker AI real-time inference now supports managed NVIDIA MIG GPU partitioning** (announced November 6), slicing A100/H100/RTX PRO GPUs into fixed compute and memory partitions for separate inference components in seven regions including Singapore. [AccessAllGPT](https://www.accessallgpt.com/research/aws-sagemaker-gpu-partitioning-nvidia-mig-inference-launch)
- **Kimi K3.1 Pro (Highspeed) from Moonshot AI is now available on Amazon Bedrock** (announced November 6), an open-weight, natively multimodal agentic model with a 1M-token context window. [LDS](https://letsdatascience.com/news/amazon-bedrock-adds-moonshot-ais-kimi-k31-pro-highspeed-mode-51717a19)

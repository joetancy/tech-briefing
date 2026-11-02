---
layout: post
title: "HackerBooks, Nibnib and a 3D thermal cloak"
date: 2026-11-02 07:30:00 +0800
categories: [tech-briefing]
---

Prepared: 7:30 AM SGT

## Hacker News Top 10

Source: Hacker News front page, as ranked at about 7:17 AM SGT on November 2, 2026 (page crawled 23:17 UTC, November 1). Listed in current ranking order, not by points.

### 1. Show HN: HackerBooks – HackerTube, but for books mentioned on HN — hackerbooks.org 🆕 New
* [Hacker News discussion](https://news.ycombinator.com/item?id=50326821) · [Source](https://hackerbooks.org)
Following the HackerTube idea from yesterday's front page, HackerBooks collects books mentioned in Hacker News comments into a browsable site. It turns years of HN discussion into a reading list curated by what the community actually recommended, rather than by bestseller charts or algorithms. If HackerTube was the video version, this is the same trick applied to books — and a reminder of how much signal sits in HN's comment history.

### 2. So I guess everyone uses LLMs to think now — eva.ac
* [Hacker News discussion](https://news.ycombinator.com/item?id=50330253) · [Source](https://eva.ac/blog/llms/)
The essay's premise is in its title: using an LLM has stopped being a special technique and become the default way many people now think through a problem. That shift raises a quieter question than whether the answers are right — what happens to judgement, memory, and the ability to reason alone when the first move is always to ask the model. It is a short, reflective read rather than a benchmark or a product announcement, and it pairs naturally with the mathematics post at #8.

### 3. Nibnib: Image compression with extreme decompression speed — github.com/raphlinus
* [Hacker News discussion](https://news.ycombinator.com/item?id=50299811) · [Source](https://github.com/raphlinus/nibnib)
Nibnib is a new image format by Raph Levien, tuned for extreme decompression speed at 4 bits per pixel. It decodes two pixels at a time from a single byte, using a palette that stores a delta rather than an absolute colour, which improves quality in soft regions over plain palette images. It was designed for microcontroller DVI output — roughly six cycles per pixel on an RP2350 — where a pixel fetch, palette lookup, and line-buffer store leave almost no headroom. Encoding is deliberately asymmetric and much slower than decoding, trading encoder effort for a decoder simple enough for tiny hardware.

### 4. HackerTube: YouTube built from videos recommended by HN — karpathy.bearblog.dev
* [Hacker News discussion](https://news.ycombinator.com/item?id=50319510) · [Source](https://karpathy.bearblog.dev/hacker-tube/)
HackerTube, still on the front page a day after topping it, turns 6,454 YouTube videos recommended in Hacker News comments between 2007 and 2026 into a curated video site. It offers topic browsing, custom recommendations without accounts, keyboard shortcuts, and downloadable data for building your own version. Its staying power on the front page says something about HN's appetite for its own archive as a recommendation source — see #1 for the book-shaped sequel.

### 5. Tips for more effective fuzz testing with AFL++ — nullprogram.com
* [Hacker News discussion](https://news.ycombinator.com/item?id=50271106) · [Source](https://nullprogram.com/blog/2025/02/05/)
Originally published in February 2025 and resurfacing on the front page, this is a checklist from fuzzing around 1,000 projects over six years. The headline tips: fuzz with AddressSanitizer and UndefinedBehaviorSanitizer enabled, prefer AFL++'s persistent mode (typically an order of magnitude faster than in-place fuzzing), and skip work irrelevant to the test — including freeing memory — so the harness stays fast and isolated. If you maintain a parser or anything that accepts complex input and have never fuzzed it, this is the practical starting point.

### 6. Ask HN: Which TV do you recommend for privacy?
* [Hacker News discussion](https://news.ycombinator.com/item?id=50328896)
This is a community discussion, not a product review: HN readers asking which televisions respect privacy, given smart TVs' reputation for ads, tracking, and automatic content recognition. The usual trade-offs in the thread's territory are dumb or commercial displays versus mainstream smart TVs, and network-level blocking versus giving up smart features entirely. Worth skimming before buying a living-room screen — the "best picture" pick and the "least surveillance" pick are rarely the same set.

### 7. Copper – A minimal low-level programming language with OOP and generics — tibleiz.net
* [Hacker News discussion](https://news.ycombinator.com/item?id=50308754) · [Source](https://tibleiz.net/copper/)
Copper is a simple, statically typed procedural language with basic type inference and generics. Everything is manipulated by reference — even integers are references to stateless objects — assignment copies the reference, and passing an argument passes the reference by value. It is not fully object-oriented, but it offers type inheritance, contextual functions (methods), and a `vtable` command for generating virtual function tables. A small language worth a look if you enjoy minimal designs that still try to answer the OOP-and-generics question honestly.

### 8. Mathematics has changed. Let's act like it — terrytao.wordpress.com
* [Hacker News discussion](https://news.ycombinator.com/item?id=50328251) · [Source](https://terrytao.wordpress.com/2026/11/01/mathematics-has-changed-lets-act-like-it/)
A guest post by Frank Calegari on Terence Tao's blog, written in the wake of OpenAI's October 6 release of over 700 mathematics papers. Its argument: AI can now make genuine contributions across many areas of mathematics, and the community should stop grieving the old economy of results and adapt — while still calling out poor attribution and writing in the AI-generated papers. The value of a mathematician, it suggests, is shifting from producing a result to asking interesting questions, verifying and explaining machine output, and finding new playgrounds once old problems fall. The optimists-versus-pessimists framing — "for the pessimists, the game is over; for the optimists, the game has just changed" — is the line to take away.

### 9. New 3D thermal invisibility cloak makes objects disappear from infrared cameras — sciencedaily.com
* [Hacker News discussion](https://news.ycombinator.com/item?id=50299427) · [Source](https://www.sciencedaily.com/releases/2026/10/261025073051.htm)
Researchers at the University of Illinois Urbana-Champaign and the Technical University of Denmark have built and tested the first three-dimensional thermal invisibility cloak. A 3D-printed aluminium lattice filled with a rubber-like, poorly conducting material guides heat around a hidden object instead of blocking it, so an infrared camera sees an undisturbed temperature field — as if nothing were there — from any direction. The team concealed complex shapes, including head-like forms, while keeping the temperature inside stable. Beyond stealth, the same heat-routing idea could help cool microchips and protect delicate electronics from thermal extremes.

### 10. Show HN: OmniDiff – Opensource, super fast, content aware Git difftool, in Rust — github.com/ivankovic
* [Hacker News discussion](https://news.ycombinator.com/item?id=50325253) · [Source](https://github.com/ivankovic/omnidiff)
OmniDiff is an open-source Git difftool written in Rust that adapts its comparison to the file's content rather than treating everything as plain text. It claims support for 25 programming languages plus configuration files, images, PDFs, archives, cursors, and fonts, and is built for speed on large files — tens of thousands of lines of C++ in the project's telling. One practical gotcha from early users: by default it exits 0 even when files differ, since it is a display tool; use `--exit-code` (0 = identical, 1 = different, 2 = error) when scripting against it, and note it ignores that flag in Git's external-diff form.

## AI

- **OpenAI GPT-6.1 Terra (Oct 26):** a lower-cost model for writing, visual reasoning and computer use, priced at about half of GPT-6.1 Sol. ([Augusto Digital](https://augusto.digital/insights/blogs/monthly-llm-news-november-2026/))
- **Google Gemini 4 Carbon (Oct 28):** pitched for coding, cybersecurity and sustained agentic work, initially only for selected cyber defenders and trusted partners, with wider developer availability promised but undated. ([Medium AI Landscape](https://medium.com/@ConcernedhumanonAI/the-ai-landscape-october-2026-a0a44c7b111e))
- **Moonshot Kimi K3.1 Pro API (Oct 23):** a 1M-token-context model, with open weights promised by Nov 4 — that weights release was still upcoming, not confirmed shipped, as of Nov 2. ([Walterstein](https://walterstein.eu/en/ai-models/upcoming))
- **Developer tooling:** Gemini gained in-chat file creation, preview and editing (Oct 29), and Anthropic shipped a beta Usage & Cost Analytics API breaking Claude usage down by model, workspace, API key and account. ([Lilach Bullock](https://www.lilachbullock.com/ai-news-this-week-for-small-business-1-november-2026/))

## Frontend

- **Next.js security release, Nov 3:** fixes seven medium-severity vulnerabilities, with advisories private until release day — book an upgrade window. Patched October baseline: 16.4.1 / 15.5.28. ([Next.js](https://nextjs.org/blog/upcoming-nextjs-security-release-november-2026))
- **TypeScript 7.1 Beta (Oct 20):** restores a stable programmatic API for the Go-based compiler, adds content mappers for Vue/Svelte/Astro/MDX, and makes `es2026` a stable target; stable release expected around Nov 24. ([TechAIWire](https://techaiwire.com/articles/typescript-7-1-beta-api-content-mappers-es2026/))
- **Node.js 26 LTS (Oct 28):** Node 26.13.0 is the LTS line, supported to April 2029; also apply the October Node security patches (26.12.1 / 24.22.1 / 22.23.4) for a High Brotli/zlib issue. ([Enpitech](https://enpitech.dev/blog/frontend-digest-2026-11-01))
- **Cloudflare Void for Vite apps (Oct 15):** an open-source SDK/CLI/platform layer to build and deploy full-stack Vite apps (React, Vue, Svelte, Solid) on Cloudflare, with file-based routing and end-to-end TypeScript. ([WebProNews](https://www.webpronews.com/cloudflares-void-rewrites-full-stack-deployment-for-vite-apps/))

## Emulation, retro games, preservation, ROM hacking, FPGA, ports and static recompilation

- **Blast Corps: Recompiled:** Rare's 1997 N64 game is now natively playable on Windows, Linux and macOS via static recompilation, with uncapped framerates, ultrawide support and mod support. ([Pants Pants Revolution](https://pantspantsrevolution.com/october-31st-week-in-review/))
- **Takedawn (Burnout 3):** unofficial native PC port of the original Xbox *Burnout 3: Takedown* via static recompilation; v0.2.1 (Oct 22) adds up to 4x resolution, ultrawide, HDR and 60 fps split-screen, and requires your own US Xbox disc. ([PortedGames](https://portedgames.com/burnout-3-pc/))
- **MarathonRecomp-Android (Sonic '06):** unofficial native Android port of the Xbox 360 *Sonic the Hedgehog (2006)* static recompilation, released as v0.1.0/v0.1.5 on Oct 26, using Vulkan and requiring your own Xbox 360 copy. ([Overclocked](https://overclockedhq.com/news/marathonrecomp-android-sonic-06-native-android-port))
- **Jotego FPGA cores:** new public FPGA cores for arcade titles NARC, Arbalester and Meta Fox, alongside hardware-validation updates for CPUs, sound chips and Capcom CPS-3 hardware. ([Pants Pants Revolution](https://pantspantsrevolution.com/october-31st-week-in-review/))
- **Studio 64:** free browser-based editor for building *Super Mario 64* ROM hacks, by hand or via AI text prompts. ([Pants Pants Revolution](https://pantspantsrevolution.com/october-31st-week-in-review/))
- **Final Fight Neo:** free fan conversion of Capcom's 1989 arcade brawler to run on SNK Neo Geo hardware. ([Pants Pants Revolution](https://pantspantsrevolution.com/october-31st-week-in-review/))
- **The Legend of Xanadu fan translation:** Falcom's 1994 PC Engine CD RPG received a new English fan-translation patch. ([Time Extension](https://www.timeextension.com/features/retro-recap-all-the-classic-gaming-news-from-the-past-week-october-31st-2026?utm_campaign=promoted-articles&utm_medium=homepage-listing&utm_source=steamhype.com))
- **Analogue Super Nt+ and Mega Sg+:** updated FPGA SNES and Genesis cartridge consoles announced Oct 16, $219.99 each, with built-in Bluetooth/2.4GHz wireless support, USB-C and up to 1080p; pre-orders opened Oct 19, shipping expected December 2026. ([Polygon](https://www.polygon.com/analogue-super-nt-mega-sg-return/))

## Cybersecurity

- **LXD critical flaw, CVSS 10.0 — patch now:** Canonical patched CVE-2026-112816 on Oct 29; it can let an attacker impersonate a trusted LXD/MicroCloud client with only its public certificate. Update to LXD 6.10.1, 5.21.9, 5.0.11 or 4.0.15. ([SecurityOnline.info](https://securityonline.info/lxd-vulnerability-cve-2026-112816/))
- **WordPress 7.1.4 (Oct 28):** fixes 22 vulnerabilities, including an unauthenticated RCE possible during a core update when files unpack into a predictable, web-reachable path. Wordfence reported large-scale probing attempts, but no confirmed compromise in the sources checked. ([Patchstack](https://www.patchstack.com/articles/wordpress-7-1-4-security-release/))
- **Binance theft attributed to North Korea:** the FBI said on Oct 31 that more than $6bn in virtual assets was stolen on or about Oct 29 in the "TraderTraitor" campaign, with funds being converted mainly to Ethereum. (Total varies by source, around $6bn–$6.36bn.) ([Mathrubhumi](https://english.mathrubhumi.com/amp/news/money/fbi-attributes-6-billion-binance-crypto-theft-north-korea-tradertraitor-rsoi44tf))
- **Northflank breach — rotate all secrets:** on Oct 30 Northflank told customers to assume stored environment variables were decrypted, after reports of unauthorised use of AI API keys. ([Brandefense](https://brandefense.io/security-news/northflank-security-incident-rotate-secrets/))
- **CISA KEV additions:** GitLab CVE-2026-97229 (CVSS 10.0, unauthenticated RCE via CI/CD regex) was added Oct 29 — patch to 19.2.8, 19.3.5 or 19.4.2; and two Ivanti Connect Secure flaws were added Oct 30, chained for unauthenticated root code execution — patch to 25.1.1.3 or 22.8R2.6 and rotate credentials that passed through the appliance. ([NeoTeo](https://www.neoteo.com/en/cisa-adds-gitlab-cve-2026-97229-to-kev), [iSecRadar](https://isecradar.com/blog/ivanti-connect-secure-exploit-chain-kev-additions-exposure-checks-and-hunting))

## AWS — short

- **Kernel patches for CVE-2026-98432 rolling out:** Amazon Linux 2/2023 kernels shipped Oct 30, with EKS/ECS AMIs dated Oct 31, Redshift patching Nov 2 and RDS/Aurora Nov 3; self-managed hosts need a kernel update and reboot. (Via a secondary write-up of the AWS bulletin, not the bulletin itself.) ([Trustlist](https://trustlist.uk/security-advisories/aws-bulletin-2026-160-cve-2026-98432-amazon-linux-kernels-out-rds-aurora-patch-3-november))
- **AWS WAF auto-injects its SDK into CloudFront (Oct 30):** CloudFront now adds the WAF JavaScript SDK to served HTML without code changes, supplying signals for Bot Control and Fraud Control managed rule groups. ([AWS News Feed](https://aws-news.com/article/2026-10-30-aws-waf-announces-automatic-sdk-integration-for-amazon-cloudfront-distributions))

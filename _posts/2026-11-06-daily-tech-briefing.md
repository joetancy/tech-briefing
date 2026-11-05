---
layout: post
title: "sshole, Kagi goes free and Claude Code leaks emails"
categories: [tech-briefing]
date: 2026-11-06 07:30:00 +0800
---

Prepared: 7:30 AM SGT — Friday, 6 November 2026

## Hacker News Top 10

### 1. Search for everyone 🆕 New
Kagi, the ad-free paid search engine, now lets anyone search without an account — the first 50 searches are free, with 100 more on registration. It's a word-of-mouth growth play: Kagi says the hardest part of recommending it was that friends couldn't try it first. The same changelog also brings a redesigned Android app with rebuilt voice search and home-screen widgets.
- [Discussion](https://news.ycombinator.com/item?id=50383740) · [Source](https://kagi.com/changelog#11820)

### 2. MS Paint Remote Code Execution Vulnerability
Microsoft's Paint app on Windows 11 has an out-of-bounds read flaw (CVE-2026-83844, CVSS 8.1) that could let an unauthenticated attacker run code over the network via a crafted image. The story's real sting is patch confusion: Microsoft disclosed it on October 13, but admins report the Microsoft Store kept serving older builds, and Microsoft's own docs have named two different fixed versions (11.2605.91.0, then 11.2609.401.0). No exploitation in the wild has been reported.
- [Discussion](https://news.ycombinator.com/item?id=50384233) · [Source](https://www.cve.org/CVERecord?id=CVE-2026-83844)

### 3. Claude Code sends your email address to websites 🆕 New
A Claude Code bug report claims the tool puts the user's email address in the `User-Agent` header while doing web searches, leaking it to arbitrary third parties — the reporter says it brought dozens of scam emails a day. They argue it should be removed from the harness entirely, not made opt-in or opt-out, and say they're migrating their company to Pi with OpenRouter over the privacy failure. Anthropic has not yet responded in the thread.
- [Discussion](https://news.ycombinator.com/item?id=50385272) · [Source](https://github.com/anthropics/claude-code/issues/107757)

### 4. sshole 🔄 Updated
An interactive, comic-style write-up of a serious OpenSSH bug: on musl-based systems without PAM (notably Alpine Linux), an account whose password field is just `*` accepts any password between 257 and 1024 characters, as long as another account on the box has a real `$5$`/`$6$` hash. The chain runs from a 1980 `*` in `/etc/passwd` through musl's 2012 decision to return `*` instead of NULL on crypt failure, to OpenSSH borrowing another user's salt for passwordless accounts. Researcher Özgün Kültekin found it by throwing ~17,600 odd logins at sshd builds — with, by his own admission, "agent swarms".
- [Discussion](https://news.ycombinator.com/item?id=50378228) · [Source](https://sshhole.com)

### 5. Alpine Linux Security Advisory: OpenSSH-server password authentication bypass
Alpine's official advisory for the sshole bug: update `openssh` now and restart `sshd` — upgrading alone doesn't replace the running daemon — or set `PasswordAuthentication no` if you can't update yet. Every Alpine release from 3.16 through 3.24 and edge is affected when sshd runs without PAM; official tiny-cloud images are worst hit, since the `alpine` user has a `*` password field and passwordless `doas`, meaning root. Fixed packages are out for all releases back to 3.16, including 3.21, which reached end of support on November 1.
- [Discussion](https://news.ycombinator.com/item?id=50379704) · [Source](https://alpinelinux.org/posts/2026-11-05-openssh-password-authentication-bypass/)

### 6. The Hackintosh Reborn
The Hackintosh was supposed to die with Apple's move to ARM and the end of x86 macOS, but AI-assisted reverse engineering is reviving it: the author reports macOS 27 running on a Snapdragon laptop and an RK3588 ARM board, iOS 17 on a Nintendo Switch OLED, and RTX 50-series GPU support via nullmoth. The driver, per the post, is "Claude Code with Ghidra on steroids" — AI tooling doing the tedious RE work that used to take humans months. The author also built a working iOS app in a day on a ThinkPad running macOS 26, without writing a line of code.
- [Discussion](https://news.ycombinator.com/item?id=50383057) · [Source](https://www.naut.ca/blog/2026/11/05/the-hackintosh-reborn-with-ai/)

### 7. Tencent Launches Hy4, One of the Leading Open-Source AI Models
Tencent's Hy4 is its latest-generation LLM, now with visual understanding and computer-use capabilities (CLI and GUI) for the first time, plus stronger long-horizon agentic work. Tencent says model weights and system cards will follow in the coming days, and prices stay at Hy4 Preview levels (~$0.90/$2.70 per million input/output tokens). In Tencent's own evaluations it topped DeepSeek-V4.1-Flash, Kimi K3.1 Pro and GLM-5.3 on real-world financial tasks, and cut its hallucination rate from 12.95% to 7.2%.
- [Discussion](https://news.ycombinator.com/item?id=50383963) · [Source](https://www.tencent.com/tencent-launches-hy4-joining-the-ranks-of-the-worlds-leading-open-source-ai-models/)

### 8. Window Sweaters
A macOS menu-bar app that dresses your windows in knitted borders, with 37 hand-picked colourways for apps from Finder and VS Code to Claude and Figma, plus icon-derived colours for everything else. It's GPL-3.0, built on JankyBorders, installable via Homebrew or from source, and already past 1,000 GitHub stars. Pure cosy-desktop whimsy — the kind of small, well-crafted macOS toy HN loves.
- [Discussion](https://news.ycombinator.com/item?id=50381383) · [Source](https://github.com/saragordic/window-sweaters)

### 9. Goodbye from Salon
Salon, one of the web's first native publications, announced on Thursday that it is ceasing publication after 31 years — it launched on November 20, 1995. The unsigned farewell letter says "the business realities of independent digital journalism have changed profoundly over the years" and that its publishing model is "no longer sustainable". Staff were told Thursday morning the publication was closed effective immediately; the editorial archive will stay live for now, per Salon's chief content officer. (Note: salon.com itself was unreachable this morning, returning a CloudFront 403, so this summary is drawn from coverage of the letter.)
- [Discussion](https://news.ycombinator.com/item?id=50383739) · [Source](https://www.salon.com/2026/11/05/goodbye-from-salon/)

### 10. The Cost of Blogging
Blogger Becky makes the case for paying to blog even when free tiers exist: she pays for four things — a personal domain, hosting, premium typography, and writing software. A domain is "an essential expense" because it's her portable online identity and a signal she'll keep blogging; paying for hosting means her subscription, not her personal information, funds development — and helps sustain the free tier for others. She caps premium font spending at £100 per family and writes in Paper, free with extra personalisation for an annual or lifetime fee.
- [Discussion](https://news.ycombinator.com/item?id=50383877) · [Source](https://onlinegoddess.net/2026/11/the-cost-of-blogging/)

## AI
- **OpenAI shipped GPT-6 Cyber** to select Daybreak Red customers — the first model OpenAI rates "Critical" for cybersecurity, up from "High" for GPT-5.6 Cyber. It scores 48.5% on OpenAI's ExploitGym benchmark (vs 42.4% for GPT-6 Astra) and reportedly goes out of bounds under 1% of the time in testing. ([The Diary of AI](https://thediaryofai.com/ai-news-20261105/))
- **Anthropic added Personal Finance to Claude**, a US beta for Pro, Max and Ultra subscribers that reads bank balances and up to 24 months of transactions through Plaid, read-only. ([The Diary of AI](https://thediaryofai.com/ai-news-20261105/))
- **Cognition launched SWE-2 Flash** on Nov 4, a cheaper, faster sibling to SWE-2 for routine agent work — 3x faster at one-fifth the price. ([KBlip](https://kblip.com/releases))
- **Anthropic's amended S-1** shows ~$17B Q3 revenue, up 12x year over year, against $895.4B in compute commitments through 2045 ahead of its IPO. ([AI Briefing](https://aibriefing.dev/story/3e93342c42d6/))
- **OpenAI's autonomous pipeline found, validated and patched 948 Linux kernel privilege-escalation bugs**, and OpenAI is acquiring Pierre Computer Company to extend Codex tooling. ([AI Briefing](https://aibriefing.dev/story/3e93342c42d6/))

## Frontend
- **Safari 27.3 beta adds Adaptive Dark Mode**: when a user enables it, Safari re-colours light websites that never shipped a dark theme, while pages declaring `color-scheme: light dark` are left alone. The same beta adds Vertical Tabs. ([WebKit blog](https://news.html.to/safari-27-3-adaptive-dark-mode/))
- **Chrome 157 is out** with on-device language detection for Android, expanded CSS capabilities, and fixes for 213 security bugs; Chrome 158 follows on November 17. ([Aryan Age](https://www.aryanage.com/article/50395/google-chrome-157-released-with-on-device-language-detection-and-213))
- **Chrome 158 drops XSLT** on November 17, 2026, except for Origin Trial and Enterprise Policy users (until Chrome 176 in August 2027). Firefox and WebKit have signalled similar plans but no dates. ([Digital Matters](https://digitalmatters.me/web-design/chrome-xslt-removal/))

## Emulation, Retro Games & FPGA
- **SGBC is a new FPGA console** from French engineer Thomas Sanfourche that plays original Game Boy, Game Boy Color and Game Boy Advance cartridges at 1080p over HDMI with integer scaling, plus a Link port and cartridge-to-microSD backup. It's still in development — no price, release date or published compatibility results yet. ([Techtroduce](https://www.techtroduce.com/sgbc-fpga-console-game-boy-1080p-hdmi/))
- **Double Dragon's MEGA65 arcade core got its first test build**, adapting Jotego's MiSTer core via the MiSTer2MEGA65 framework, complete with FM synthesis audio — but it already uses all available FPGA block RAM, which may block a Double Dragon II port. ([The Oasis BBS](https://theoasisbbs.com/double-dragon-mega65-arcade-core-gets-its-first-test/))
- **FPGA developer Jotego is asking the community where his arcade cores should go next**, with 1,250+ games already running on MiSTer and Analogue Pocket; he's considering folding abandoned cores into his standardised JTCORES framework. ([Pants Pants Revolution](https://pantspantsrevolution.com/jotego-ask-for-user-feedback/))

## Cybersecurity
- **Zyxel patched a zero-day hiding behind an old fix**: CVE-2026-107441 (CVSS 8.8, Binarly rates it 9.8) is an out-of-bounds write in GS1900 switches' web interface that attackers used to compromise 996 switches in 48 countries, harvesting configs and hashed root credentials. Zyxel's June patch for CVE-2026-7273 didn't stop it; firmware fixes shipped October 22. ([Network World](https://www.networkworld.com/article/4245031/zyxel-patches-a-zero-day-hiding-behind-an-old-fix-2.html?utm_medium=organic_social&utm_source=LINKEDIN_COMPANY))
- **CISA confirmed PHP2Shell exploitation**: CVE-2026-109618 and CVE-2026-109619 (CVSS 9.2) are being exploited in the wild; researchers documented a campaign that rooted 25 firewall and management servers. PHP fixed them in 8.2.35, 8.3.36, 8.4.27 and 8.5.12 on October 21. ([MLQ](https://mlq.ai/news/cisa-confirms-php2shell-exploitation-as-researchers-document-attacks-on-25-firewalls/))
- **CISA added a WordPress core RCE to its Known Exploited Vulnerabilities catalog**: CVE-2026-119977 (CVSS 8.1) lets an unauthenticated attacker run code during a full-package core upgrade on WordPress before 7.1.4; Wordfence logged 18,500+ probes in the first 21 hours. Federal agencies must patch by Nov 6. ([Daily Drop](https://bragg.substack.com/p/daily-drop-1379))
- **OPSShield's update infrastructure was compromised**: fake cPGuard updates (5.88.12–5.88.19) were pushed Nov 2 and installed on ~2,950 customer servers for over 70 minutes, exfiltrating password hashes, root SSH keys, MySQL root passwords and cloud keys, and leaving a hidden root shell. ([Daily Drop](https://bragg.substack.com/p/daily-drop-1379))

## AWS
- **AWS launched Kiro bots**, persistent agents in the Kiro Crew workspace that handle recurring dev jobs — triaging issues, watching builds, reviewing changes — with memory of past decisions. Now generally available. ([VentureBeat](https://venturebeat.com/technology/aws-launches-agentic-ai-kiro-bots-with-memory-and-support-for-recurring-development-jobs))
- **S3 Tables now offers managed migration** of Apache Hive tables to fully managed Apache Iceberg tables, with no pipelines to build or compute to provision. ([AWS News Blog](https://aws.amazon.com/blogs/aws/aws-weekly-roundup-gpt-6-1-terra-on-bedrock-step-functions-as-agent-tools-and-more-november-2-2026/))
- Also from the Nov 2 weekly roundup: GPT-6.1 Terra is GA on Bedrock, Step Functions workflows are now usable as agent tools via Bedrock AgentCore Gateway, and re:Invent runs November 30 – December 4 in Las Vegas.

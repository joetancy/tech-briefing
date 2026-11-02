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

## Tech & AI Roundup

- **Frontend — Next.js security release tomorrow:** Next.js has a scheduled security release for Tuesday, November 3, covering seven medium-severity vulnerabilities, with full advisories published alongside the release. Details are private until release day, so the useful move today is to book the upgrade window — see Action Required.
- **Frontend — TypeScript 7.1 beta, Node 26 LTS:** The TypeScript 7.1 beta (October 20) makes es2026 a stable target and ships a new API for building tooling on the Go-based compiler, which Volar, the Svelte language service, and typescript-eslint have been waiting on. Node.js 26.13.0 moves 26.x into LTS (Lithium), supported through the end of April 2029, with no changes beyond metadata from 26.12.1.
- **Frontend — agents drawing UI, shipping less JS:** CopilotKit's Generative UI (October 29) lets agents render UI from your own components, with 70 catalog components, A2UI v1.0 and AG-UI support, and design-system theming. Vercel's new Next.js agent skill uses the Turbopack module graph to find imports defeating lazy loading, with Vercel reporting nearly 2 MB of client JavaScript removed or deferred. Firefox 159 ships CSS scroll-driven animations, so all three major engines now support them, and Vercel CI entered beta with affected-tasks-only runs and Remote Cache.
- **Python backends:** FastAPI 0.160.0 landed October 22, applying each parameter model's `extra` configuration to sibling fields in the same parameter location, and PyPI now lists 0.162.0 from October. Python on Vercel is generally available (October 15), with automatic FastAPI, Flask, and Django recognition, and Vercel Functions now support WebSockets in GA and Python routing middleware. PyPy 8.0.0 arrived with experimental Python 3.12 support, and FastAPI has built-in OpenTelemetry support.
- **Terraform / OpenTofu:** Terraform 1.17.1 (October 28) remains the latest Terraform release, with import blocks in child modules (since 1.16) still the recommended route for bringing hand-built AWS resources under management. OpenTofu's current line is 1.13, with 1.13.5 and 1.12.11 both dated October 29; 1.13's security support runs to August 2027, and 1.13 extended state encryption with GCP KMS authenticated data, AWS KMS encryption context, and OpenBao associated data. OpenTofu 1.13 also removed the WinRM provisioner connection type — check older Windows configurations before upgrading.
- **AWS — agents calling your workflows:** AWS connected Step Functions workflows to Amazon Bedrock AgentCore Gateway on October 29, so an agent can invoke existing Standard and Express state machines as tools via MCP, while the state machine — not the agent — defines the sequence of steps. The gateway and the target state machine must be in the same Region, and AgentCore Gateway bills $0.005 per 1,000 API invocations on top of standard Step Functions rates. Separately, Bedrock added cross-Region inference for OpenAI models in Canada (GPT-6.1, GPT-6, GPT-5.6 from Canada Central and Canada West) and in GovCloud (GPT-5.6 Terra and Luna), and Amazon added Moonshot's Kimi K3 and Z.ai's GLM 5.3 to Bedrock's catalog, disclosed on the October 29 earnings call.
- **AI models:** The Bedrock expansion is the week's model news in practice: closed models from Anthropic and OpenAI now sit alongside open alternatives including Kimi and GLM, plus SpaceX's Grok 4.7, in one catalog — which makes Bedrock's inference profiles and data-residency controls, not just model choice, the thing to configure deliberately.

## ⚠️ Action Required

- **Next.js — book tomorrow's upgrade window:** The November 3 security release covers seven medium-severity vulnerabilities. Confirm who deploys your Next.js apps and clear time on Tuesday to upgrade once the patched versions land. If you have not already applied the October 14 fixes, do that first: 16.4.1 (Active LTS) or 15.5.28 (Maintenance LTS), which fixed two critical RCE vulnerabilities and a high-severity DoS issue.
- **Python — apply the October 21 security releases:** Python 3.15.1, 3.14.9, and 3.13.17 shipped with pip 26.2.2 and certifi 2026.10.19 to drop the compromised eMudhra CA. Update certifi, pip, uv (0.13.4), and sigstore (4.5.1) in every virtualenv and container image — older clients are open to man-in-the-middle attacks against PyPI and python.org otherwise. Wagtail users should also be on 8.0.1, 7.4.4, or 7.0.10 (October 20 security releases).
- **Node.js — check the October security releases:** The October Node.js releases rate CVE-2026-111497 High for apps decompressing attacker-controlled Brotli data via `node:zlib`, with patched versions 26.12.1, 24.22.1, and 22.23.4. If you are on 26.x, the move to 26.13.0 LTS covers this as well.

## Engineering Insight

**In Terraform, `null` does not mean "use the default" — it means "unset".** A November 1 post-mortem tells the story plainly: a platform module's `deletion_protection` variable defaulted to `true`, but callers passing `null` silently produced RDS instances with protection off, because a null argument is treated as not set and the AWS provider's own default (`false`) won. Fourteen of twenty-two instances were affected, and the plan output had said `deletion_protection = false` all along, one line among sixty. The fixes are cheap and general: set `nullable = false` on module variables so null falls back to the module's default, add a precondition that fails the plan unless the resolved value is what you expect, and switch on the AWS Config rule `rds-instance-deletion-protection-enabled` in every account. Read your plan output for the value that actually resolved, not the default you assumed.

## Worth 5 Minutes

- **📝 Engineering blog post:** "Mathematics has changed. Let's act like it" (terrytao.wordpress.com) — Frank Calegari's guest post on what AI-generated mathematics means for the field, and why asking, verifying, and explaining now matter more than merely producing a result. https://terrytao.wordpress.com/2026/11/01/mathematics-has-changed-lets-act-like-it/
- **💻 GitHub repository:** nibnib (Raph Levien) — image compression at 4 bits per pixel with extreme decompression speed, built for microcontroller displays and a masterclass in designing a decoder first. https://github.com/raphlinus/nibnib
- **📄 Research paper:** "Free-form thermal cloaks in three dimensions" (Li, Wang, Sigmund & Zhang, Nature Communications 17, 5739, 2026) — the paper behind today's thermal cloak story: a lattice metamaterial whose conductivity can be tuned independently in three directions to route heat around complex shapes.

---

*Sources: Hacker News front page (ranked ~7:17 AM SGT, Nov 2, 2026); nibnib README, nullprogram AFL++ tips, Copper documentation, Terry Tao blog, ScienceDaily / Nature Communications thermal cloak coverage, OmniDiff project notes, Next.js security announcement, Enpitech Frontend Newsletter Nov 1, TypeScript and Node.js release notes, FastAPI / Django News, OpenTofu release data, and AWS Bedrock announcements as linked above. Story 2 is summarised from its title and premise and story 6 from its discussion question, where full article text was not retrieved.*

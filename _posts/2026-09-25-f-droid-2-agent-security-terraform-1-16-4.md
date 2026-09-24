---
layout: post
title: "F-Droid 2.0, Agent Security & Terraform 1.16.4"
date: 2026-09-25 07:30:00 +0800
categories: [tech-briefing]
---

**Prepared: 7:30 AM SGT**

## Hacker News

These are the live Hacker News top 10 at preparation time, in current ranking order. Rankings can change quickly. ([Hacker News](https://news.ycombinator.com/))

### HN #1 — 🆕 F-Droid 2.0

F-Droid released version 2.0, its largest app update in 10 years, with a redesigned interface, Kotlin and Jetpack Compose internals, better discovery and search, improved CJK search, and smoother installs through Android's newer pre-approval API. The rollout follows 14 test releases; Android 6 support is dropped, the Privileged Extension is not currently used by 2.0, and the app-wiping panic feature has not yet returned. ([F-Droid](https://f-droid.org/2026/09/24/f-droid-2.0-a-new-chapter-for-android-freedom.html))

### HN #2 — 🆕 Show HN: Koi.rest

Koi.rest is a small browser experience built around watching animated koi and interacting with a quiet virtual pond. It is intentionally simple and is designed as a short visual break rather than a productivity tool. ([Koi.rest](https://koi.rest/))

### HN #3 — Show HN: Make cursed fonts like Times New Bastard

Bastardica is an in-browser font foundry that lets you combine, stretch, squish, and alternate glyphs from different fonts, then export TTF, OTF, or WOFF2. Processing runs locally in the browser with Pyodide and fontTools, so uploaded fonts do not need to be sent to a server. ([Bastardica](https://bastardica.mitpit.com/))

### HN #4 — California is chasing wealth that has feet

This opinion piece argues that California should prefer a land-value tax over a proposed billionaire wealth tax because land cannot move out of the state. The author estimates that a 0.25% land-value tax could raise about the same $20 billion per year and presents it as an alternative to taxing a small number of mobile high-net-worth residents. ([Center for Land Economics](https://blog.landeconomics.org/p/california-is-chasing-wealth-that))

### HN #5 — 🆕 Show HN: Whiteboard, an open-source IDE for software design

Whiteboard is an open-source desktop application where developers and coding agents can design software in a shared visual workspace; it connects to tools such as Claude Code and Codex and gives agents an SDK for drawing on the canvas. It also includes a Rust AST-aware semantic diff viewer and links diagrams and agent traces back to code. ([GitHub](https://github.com/devdotfast/whiteboard))

### HN #6 — Why is the liver so weirdly regenerative?

This essay explores why organs have very different regeneration abilities and proposes a trade-off between regeneration, cancer risk, environmental exposure, and structural complexity. The author treats the model as speculative rather than settled biology and works through counterexamples such as the lungs and pancreas. ([Dynomight](https://dynomight.substack.com/p/liver))

### HN #7 — Fearless SIMD v1.0

Fearless SIMD 1.0 provides a Rust SIMD abstraction designed to combine portability, performance, and memory safety without widespread ad-hoc `unsafe` code. The release also introduces `fearless_simd_macros` 0.1 with a `#[simd]` macro for function multiversioning while keeping safe access to platform intrinsics. ([Linebender](https://linebender.org/blog/fearless-simd-1-0/))

### HN #8 — 2DWillNeverDie

2DWillNeverDie is a sprite and pixel-art gallery with tutorials and reference material for 2D artists. Its HN appearance is a reminder that small, durable reference sites can stay useful without becoming large content platforms. ([2DWillNeverDie](https://2dwillneverdie.com/))

### HN #9 — 🆕 Rails World 2026 Opening Keynote

David Heinemeier Hansson opened Rails World 2026 with a 75-minute keynote on what is new in Rails, what comes next, and the direction of the framework. The talk is drawing attention as Rails presents its strong conventions and integrated stack for a development environment where AI coding agents produce more implementation work. ([Rails World](https://app.railsworld.com/talks/rails-world-2026-opening-keynote))

### HN #10 — Wandering around Tokyo on Google Maps

Ahmed Hossam describes using historical Google Street View to wander through Tokyo and see how individual streets change over time. One example follows a white Nissan 350Z that appeared in the same location across captures dating to 2009, before a later real-world check found that both the car and original house were gone. ([Ahmed Hossam](https://ahmedhossamdev.com/writing/my-weird-new-hobby-wandering-around-tokyo/))

## Tech & AI

### 🆕 GitHub adds proof of presence for high-impact actions

GitHub Enterprise Cloud now has a public preview of **proof of presence** for Enterprise Managed Users with Microsoft Entra ID SSO. Enterprises can require fresh re-authentication or MFA before selected sensitive actions, and a successful proof remains valid for two hours. ([GitHub Changelog](https://github.blog/changelog/2026-09-24-require-proof-of-presence-for-high-impact-actions/))

### 🆕 GitHub Security Lab turns fuzzing into an agent workflow

GitHub Security Lab published an autonomous C/C++ fuzzing pipeline built on its Taskflow Agent framework. The agent finds entry points, writes fuzz harnesses, runs AFL++, reads coverage, improves the campaign, triages crashes, and produces reports, while MCP tools perform execution and SQLite stores workflow state. ([GitHub Security Lab](https://github.blog/security/application-security/ai-powered-fuzzing-with-the-github-security-lab-taskflow-agent/))

GitHub recommends running the current taskflow only in a disposable Codespace or throwaway VM without elevated privileges because the fuzzing and build work runs directly on the host.

## Frontend

**React 19.3** remains the current stable React release. It made View Transitions and Fragment Refs stable and includes other platform and API updates. ([React](https://react.dev/blog/2026/09/09/react-19-3))

**Next.js 16.3.6** is the current security patch on the 16.x Active LTS line, while **15.5.26** is the Maintenance LTS patch. Next.js has also announced a September 30 security release with 16.3.7 and 15.5.27, covering nine vulnerabilities: one critical, two high, five medium, and one low. ([Next.js](https://nextjs.org/blog))

## Python Backends

### 🆕 Pydantic AI 2.49.0

**Pydantic AI 2.49.0** is now the latest release. It adds a GitHub Copilot OAuth device-authorization flow and includes Bedrock Converse updates, including support for GPT-6 Sol, Luna, and Astra. ([Pydantic AI releases](https://github.com/pydantic/pydantic-ai/releases))

**FastAPI 0.141.1** remains the latest stable FastAPI release. Its main fix is support for background tasks and headers from dependencies used with `app.frontend()`. ([FastAPI releases](https://github.com/fastapi/fastapi/releases))

## Terraform & OpenTofu

### 🆕 Terraform 1.16.4 and 1.17.0-beta2

**Terraform 1.16.4** was released on September 23. It fixes policy-evaluation rendering with older Terraform Enterprise versions and a Stacks deferral error; **1.17.0-beta2** adds variables and locals in provider requirements, `-minimal-refresh`, and makes Terraform Policy generally available. ([Terraform releases](https://github.com/hashicorp/terraform/releases))

**OpenTofu 1.12.6** remains stable, while **1.13.0-rc1** is the current release candidate. OpenTofu 1.13 removes the deprecated WinRM provisioner connection type and changes the compressed representation from `base64gzip()`, which can cause planned resource changes even though decompression produces the same bytes. ([OpenTofu releases](https://github.com/opentofu/opentofu/releases))

## AWS

### 🆕 Bedrock Managed Knowledge Base adds Salesforce and Zendesk connectors

Amazon Bedrock Managed Knowledge Base now has native Salesforce and Zendesk data-source connectors. They handle crawling, metadata extraction, and incremental synchronization, removing the need for a separate ingestion pipeline for this content. ([AWS](https://aws.amazon.com/about-aws/whats-new/2026/09/amazon-bedrock-managed-knowledge-base-salesforce-zendesk-native-data-source-connectors/))

### 🆕 Kinesis can manage partition keys for unordered workloads

Amazon Kinesis Data Streams now supports service-managed partition keys for On-Demand Standard and On-Demand Advantage streams. For workloads that do not need per-key ordering, producers can omit their own partition key and let Kinesis distribute records according to available warm capacity; the feature is available in all AWS commercial Regions at no additional cost. ([AWS](https://aws.amazon.com/about-aws/whats-new/2026/09/kinesis/service-managed-partition-keys/))

### CloudWatch Omni is now GA

Amazon CloudWatch Omni provides a unified OpenTelemetry-based observability experience for applications, infrastructure, and AI agents, with natural-language investigation, topology, traces, evaluations, and IDE integrations. It supports Python and TypeScript directly and can ingest OTLP telemetry from AWS, on-premises systems, and other clouds. ([AWS](https://aws.amazon.com/cloudwatch/omni/))

## Action Required

- **Next.js:** move affected applications to **16.3.6** now, or **15.5.26** on Maintenance LTS. Plan another patch window for **September 30**, when 16.3.7 and 15.5.27 are scheduled to fix nine additional vulnerabilities. ([Next.js](https://nextjs.org/blog))
- **GitHub Actions:** Node.js 20 is no longer available on GitHub-hosted Actions runners. Action authors should publish with `runs.using: node24`, and workflow owners should update to action versions that support Node 24. ([GitHub Changelog](https://github.blog/changelog/2026-09-23-node-20-is-no-longer-available-in-github-actions/))
- **GitHub Enterprise Cloud self-hosted runners:** full minimum-version enforcement starts **September 25**. Old runners can fail registration or stop receiving jobs when they are outside the supported update window. ([GitHub Changelog](https://github.blog/changelog/2026-06-12-github-actions-minimum-version-enforcement-timeline-for-self-hosted-runners/))

## Engineering Insight — Put fresh human presence at privilege boundaries

Agent security needs more than scoped access. A valid session or authorized agent can still perform an action that the user did not intend, so sensitive operations should require stronger confirmation at the point where authority changes. ([GitHub proof of presence](https://github.blog/changelog/2026-09-24-require-proof-of-presence-for-high-impact-actions/))

A practical boundary is:

```text
agent
  ↓
disposable sandbox
  ↓
explicit filesystem + network scope
  ↓
least-privilege access
  ↓
fresh human proof for high-impact actions
  ↓
audit trace
```

Use the agent for analysis and repetitive execution, but require a fresh human signal before sensitive or production-impacting operations. The fuzzing workflow published today reinforces the execution side of the same rule: when an agent can drive build and test tools, keep the environment disposable and the blast radius small. ([GitHub Security Lab](https://github.blog/security/application-security/ai-powered-fuzzing-with-the-github-security-lab-taskflow-agent/))

## Worth 5 Minutes

### Engineering blog — *AI-powered fuzzing with the GitHub Security Lab Taskflow Agent*

The implementation is a useful example of splitting an agent system into **decision-making** and **execution** layers. The LLM decides which coverage gap to chase, while narrow MCP tools compile, run AFL, read coverage, and persist results; the article also covers coverage feedback, plateau detection, structure-aware mutation, corpus reuse, and crash triage. ([GitHub Security Lab](https://github.blog/security/application-security/ai-powered-fuzzing-with-the-github-security-lab-taskflow-agent/))

### GitHub repository — `devdotfast/whiteboard`

Whiteboard is worth examining if you want software design to be a first-class part of an agent workflow instead of only reviewing generated diffs after implementation. Its notable pieces are the shared visual canvas, links from diagrams to code and agent traces, and the Rust AST-aware semantic diff viewer. ([GitHub](https://github.com/devdotfast/whiteboard))

### Research paper — *Invisible in Space, Visible in Time: Motion Vision CAPTCHA against GUI Agents*

This paper introduces **Motion Vision CAPTCHA (MVCAP)**, where the target becomes visible through motion over time instead of from one static frame. On its 600-instance browser benchmark, humans reached 99.6% accuracy while the best tested GUI agent reached 16.8%, close to six-way chance, which suggests that temporal visual perception remains a measurable weak point for current GUI agents. ([arXiv:2609.27461](https://arxiv.org/abs/2609.27461))

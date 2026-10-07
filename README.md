# Portfolio — AI Operations Systems

I build AI operations systems that run real businesses. Not demos, not
wrappers: multi-agent back offices with deterministic policy engines,
verification gates, and audit trails, installed where mistakes have
consequences.

Every project below is a system I designed, built, and operate. The impact
numbers are pulled from live runs and committed evidence — not projections.

- **Draft and surface, never execute.** Agents prepare; humans approve anything that sends, spends, or publishes.
- **Policy over vibes.** A deterministic rules layer — not an LLM — decides what runs autonomously.
- **Verify before reporting done.** Self-reported completion without evidence gets sent back, by design.

---

## Projects

### Snag — capture → triage → act

Turn a saved TikTok into your next action. Send Snag a TikTok link (or a video
file) and it returns a transcript, an AI-written note, and a triage pass
(stage, action type, impact, effort) filed into a searchable vault. An Actions
queue forces a decision on every save, because saved folders are where ideas go
to die.

- **Loop:** save → transcribe → understand → act.
- **Stack:** Python (stdlib), Telegram bot, ElevenLabs server-side transcription with a local faster-whisper fallback, DeepSeek for note + triage, SQLite vault, launchd on macOS.
- **Lineage:** v2 of the TikTok Brain capture → transcribe → categorize pipeline, rebuilt as a standalone consumer product (text-only, cost-first, no ClickUp).
- **Status:** live and dogfooded on Telegram.
- **Repo:** https://github.com/Kane808-AI/snag

### Agent OS v2 — headless autonomous operations platform

A headless, event-driven operating system for autonomous business operations,
designed as a resellable platform: a business-agnostic kernel, departments as
optional modules, industry packs, and per-tenant isolation. A deterministic
policy engine — not an LLM — decides whether an action is automatic,
notify-and-proceed, approval-required, or forbidden, and a completion claim
requires independent read-back evidence from a separate QA actor.

- **Verification:** work moves through `claimed → attempted → observed → verified | disproved | inconclusive`; immutable evidence receipts carry a canonical content hash.
- **Engineering depth:** 345 passing tests behind a green CI gate; 15 verified milestone goals, each with an architecture decision record.
- **Note:** public showcase snapshot of a private production codebase (reference tenant sanitized to "Northwind").
- **Repo:** https://github.com/Kane808-AI/agent-os-v2-showcase

### Law Firm OS — AI back office for a law practice

Delivered as a paid consulting engagement for a criminal defense and personal
injury practice. AI intake classification feeds four systems of record; a CRM
layer runs SMS-first follow-up and booking; a six-agent operations layer runs
the back office. It is the firm's working back office, not a demo and not a
chatbot.

- **Privilege in code, not prompts:** PreToolUse hooks inspect every tool call before it executes and deny the ones that touch protected ground; writes are scanned for SSN/DOB shapes.
- **Structure:** one orchestrator (Chief of Staff) as the sole human interface, five specialist agents, and a five-gate verification standard on every result.
- **Autonomy as a table:** reading, research, and drafting are autonomous; anything that moves a file, sends a message, touches money, or publishes requires explicit human approval.
- **Repo:** https://github.com/Kane808-AI/law-firm-os

### demo-repo — policy-gate reference example

A minimal, runnable reference for the pattern underneath everything else: a
deterministic policy gate that classifies an action as automatic,
notify-and-proceed, approval-required, or forbidden, plus a verification step
that refuses to mark work "done" without evidence. Small, self-contained
Python with tests — the smallest honest illustration of how the systems above
decide what runs on its own.

- **Repo:** https://github.com/Kane808-AI/demo-repo

---

## Impact metrics

| Metric | Value | System |
| --- | --- | --- |
| Passing tests, green CI on every push | 345 | Agent OS v2 |
| Verified milestone goals, each with an ADR | 15 | Agent OS v2 |
| Scheduled executions clean across a verified four-day stretch | 91 / 91 | Agent fleet |
| Standing automated jobs running daily | 25 | Portfolio-wide |
| Tool-call decisions logged on day one of the guardrail hooks | 33 | Law Firm OS |
| Denials and real PII catches on day one | 3 denials · 1 PII catch | Law Firm OS |
| Ideas processed through the capture → triage → act pipeline | 132 | TikTok Brain → Snag |

---

## Links

- **GitHub profile:** https://github.com/Kane808-AI
- **Law Firm OS:** https://github.com/Kane808-AI/law-firm-os
- **Agent OS v2:** https://github.com/Kane808-AI/agent-os-v2-showcase
- **Snag:** https://github.com/Kane808-AI/snag
- **demo-repo:** https://github.com/Kane808-AI/demo-repo
- **Website:** https://chriskaneshiro.com
- **Agency (Brand75):** https://brand75.com

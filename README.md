# Portfolio: AI Operations Systems

I build AI operations systems that run real businesses. Not demos, not
wrappers: multi-agent back offices with deterministic policy engines,
verification gates, and audit trails, installed where mistakes have
consequences.

Every project below is a system I designed, built, and operate. The numbers are
pulled from committed evidence, and every one of them can be checked.

![Agent OS runtime dashboard, captured from the repository's own local demo](docs/agent-os-dashboard.png)

- **Draft and surface, never execute.** Agents prepare; humans approve anything that sends, spends, or publishes.
- **Policy over vibes.** A deterministic rules layer, not an LLM, decides what runs autonomously.
- **Verify before reporting done.** Self-reported completion without evidence gets sent back, by design.

---

## Projects

### Agent OS Core: governed autonomous operations platform

A headless, event-driven operating system for autonomous business operations,
designed as a resellable platform: a business-agnostic kernel, departments as
optional modules, industry packs, and per-tenant isolation. A deterministic
policy engine, not an LLM, decides whether an action is automatic,
notify-and-proceed, approval-required, or forbidden, and a completion claim
requires independent read-back evidence from a separate QA actor.

- **Evidenced, not asserted:** an approval-gated agent channel ran as a background service from July to August 2026, with a model drafting every reply and a human decision releasing every outbound message. It was handed to a successor system in August 2026, and left 25 governed model calls, 26 routing decisions, 33 audit records and 16 workflow runs in its evidence database.
- **Verification:** work moves through `claimed -> attempted -> observed -> verified | disproved | inconclusive`; immutable evidence receipts carry a canonical content hash.
- **Engineering depth:** 345 passing tests behind a green CI gate; 15 verified milestone goals, each with an architecture decision record; 23 ADRs and 64 tracked requirements in the repository.
- **Note:** public showcase snapshot of a private production codebase, with the reference tenant sanitized to a fictional agency.
- **Repo:** https://github.com/Kane808-AI/agent-os-core-showcase

### Law Firm OS: AI back office for a law practice

An anonymous architecture case study for AI intake, CRM automation, and
governed agent operations in a law firm environment. It documents a working
back office design while excluding client identity, configuration, and data.

- **Status:** the intake and CRM layers run in production. The agent layer is mid-rollout, and each agent is validated against real guardrails before the next one is built.
- **Privacy controls at the tool boundary:** PreToolUse hooks inspect tool calls before execution, deny access to protected paths, and scan writes for high-risk PII shapes.
- **Structure:** one orchestrator as the sole human interface, five specialist agents, and a five-gate verification standard on every result.
- **Autonomy as a table:** reading, research, and drafting are autonomous; anything that moves a file, sends a message, touches money, or publishes requires explicit human approval.
- **Repo:** https://github.com/Kane808-AI/law-firm-os

### demo-repo: policy-gate reference example

A minimal, runnable reference for the pattern underneath everything else: a
deterministic policy gate that classifies an action as automatic,
notify-and-proceed, approval-required, or forbidden, plus a verification step
that refuses to mark work "done" without evidence. Small, self-contained Python
with tests, and the smallest honest illustration of how the systems above decide
what runs on its own.

- **Repo:** https://github.com/Kane808-AI/demo-repo

---

## Impact metrics

| Metric | Value | System |
| --- | --- | --- |
| Passing tests behind a green CI gate | 345 | Agent OS Core |
| Architecture decision records written | 23 | Agent OS Core |
| Tracked requirements with verification traceability | 64 | Agent OS Core |

Every row above can be checked against the public repository. An earlier version
of this table carried fleet execution counts that had no public source, so those
rows were removed rather than softened.

---

## How these are built

I direct AI coding agents (Claude Code and Codex) against specs I write and
gates I enforce. The architecture and the design decisions are mine. Every
change lands as a pull request and is independently verified before it merges,
and a worker's own completion claim is never accepted as proof of completion.

## Work with me

I take on contract work through [Brand75](https://brand75.com): agent
workflows, intake and CRM automation, and the approval and verification
controls that make those systems safe to run. I am also open to full time roles
where I own the same kind of work in house.

- **Website:** https://chriskaneshiro.com
- **Agency:** https://brand75.com
- **GitHub profile:** https://github.com/Kane808-AI

## License

MIT. See [LICENSE](LICENSE).

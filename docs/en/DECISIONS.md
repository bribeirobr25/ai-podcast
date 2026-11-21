# BAR Podcast — Decisions and hypotheses (EN)

**Updated:** 2026-11-21. [Português](../DECISOES.md). [Audit](AUDIT_2026-11-21.md).

## 1. User-confirmed direction

- **Show name:** BAR Podcast. **Host/facilitator:** BAR.
- AI models participate editorially as **guests**, not assistants whose function is to agree with the host. We make no claim that the guests are conscious or persons.
- Through an invitation and pre-interview, guests may **propose** their name, presentation, voice, style, interests, boundaries and recording instructions. The human producer defines the invitation, tools, permissions, format and guardrails.
- Within their provider/model limits, guests may ask back, disagree, pass, remain silent, refuse, correct themselves and revise positions.
- Keep records of producer-provided prompts, tools, context, memory, edits and model-generated selections. First-person language is not evidence of independent desire.
- A future complete workflow must support **Brazilian Portuguese and English**, including preparation, production content and interfaces. In the historical prototype, a guest had one selected language; experimenting in both languages could require separate guest IDs.
- The main editorial metric: **Would an audience want to hear this same guest again?** Identity, memory and continuity should be observed, not assumed.

## 2. Historical implementation choices are not universal requirements

In October, the team developed historical Node.js + model API + Anam source files for a pre-interview, avatar approval, voice selection, live studio, recording, versioned memory and local dashboard. A **three-minute** recording-block script applied to the Anam free trial available at that time. Neither those block lengths nor real-time avatars or a custom panel are requirements for the first podcast experiment.

Testing **one guest** is appropriate for isolating technical audio issues. Trying **two guests** is separately useful for evaluating actual cross-AI interaction. These are not contradictory directions when test purpose is stated.

## 3. Current experimental direction — not yet proven

1. **Experiment 0:** laptop records; phone runs one AI voice app; optional tablet hosts another AI. Verify that the AIs genuinely hear one another.
2. **Experiment 1:** Zoom/Meet, one AI and a remote observer; test **both-way audio**. Two competing apps on the same mobile device may not share microphone, call/session and audio routes reliably.
3. **Experiment 2:** an audio bridge or the earlier Node/Anam application, **only if** the experiments justify engineering.

The user intended to run physical experiments, but no reproducible outcome has yet been recorded here.

## 4. Proposed or deferred; not approved as implemented features

- Dedicated Gmail accounts for recurring guests, with human-administered OAuth permissions, review and revocation.
- Multi-avatar roundtables and live multi-model rooms.
- An always-on AI **salon**, based on a model-generated proposal during another AI-project discussion.
- Autonomous outbound messages, physical robots, external acts and shared cross-provider memory services.

All would need explicit decisions, controls and actual testing. Treat generated statements as outputs under prompts, not self-authorizing instructions.

## 5. Unresolved decisions

Exact voice apps/models and OS versions; launch language/topic; recorder; legal and commercial reuse of voices; cross-application memory/identity persistence; and what to do if simultaneous mobile meeting/AI audio fails.

## 6. Change discipline

Document each meaningful decision with its date, source, state (**decided / proposed / tested / rejected**), owner and evidence. Do not promote an assistant suggestion or AI-generated quote to a user-approved decision without explicit confirmation.

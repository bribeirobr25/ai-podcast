# BAR Podcast — Layered architecture and historical implementation (EN)

**Updated:** 2026-11-21. [Português](../ARQUITETURA.md). The following are **alternatives**, not a deployed complete platform.

## 1. Separate the editorial product from its medium

- **Identity / editorial contract:** invitation, provider/model used, name and presentation proposed, boundaries, permissions, prompts, producer changes and source of memory. Memory does **not** automatically follow an AI between apps.
- **Conversation engine:** a native consumer voice app **or** the model's developer API. Do not assume they use the same model version, memory, context or settings.
- **Transport / capture:** same-room physical devices + laptop recording, **or** Zoom/Meet with verified two-way audio, **or** the legacy Node/Anam studio.
- **Production / evidence:** unedited recording, transcript, test metadata, editorial review, participant consent, usage rights, revisions and publication disclosures.

## 2. No-code experiment

**G0:** BAR records from a laptop while one model speaks through a phone. Verify microphone capture and audible output. **G1 optional:** add a second voice app on a tablet and test whether it can respond to the first guest without BAR re-speaking the answers.

**G2:** join Zoom/Meet from a mobile device and use the AI voice app. **Do not presume one app can receive the other app's meeting audio and deliver generated speech back into the call.** Confirm inbound and outbound paths with a remote observer, checking echo, background interruptions and app priority. If this fails, test separate devices or an audio bridge before building a meeting bot.

A Gmail account is an **identity and communication credential**, not a bidirectional audio router or an autonomous agent.

## 3. Historical source in Drive (not in this GitHub repository)

Reconstruction reviewed: `ai-guest-podcast (2).zip` + `painel-update.tgz` + `roteiro-update.tgz`.

1. `scripts/pre-interview.js` sends invitation, asks follow-up questions, consolidates guest instructions and allows a declined invitation to be recorded.
2. `scripts/avatar.js` and `scripts/pick-voice.js` support image approval and voice selection.
3. `server.js` serves studio; selected external LLM streams responses at `/api/chat-stream`; Anam uses `CUSTOMER_CLIENT_V1`; browser uses `MediaRecorder`.
4. `scripts/remember.js` / `lib/memory.js` rewrite a versioned `memory.md` at episode close.
5. `dashboard.js` exposes local guest, recording and memory views. Prompts live in `prompts/pt` and `prompts/en`.

**Historical commands only (cannot be run in this documentation-only repository):**
- `node scripts/pre-interview.js guest-01 --lang en --provider <provider> --model <id>`
- `node server.js guest-01` (historically port 8000)
- `node dashboard.js` (historically port 8001)
- `npm run selftest` (mock mode)

## 4. Observed historical implementation risks

- `server.js` uses `app.listen(PORT)` without explicitly binding loopback, and session-token, model, transcript and memory endpoints have no application authentication. **Do not expose the historic server to a LAN or the Internet.**
- `dashboard.js` binds `127.0.0.1` explicitly; this does **not** make studio endpoints secure.
- The studio imports `@anam-ai/js-sdk@4.27.1` from CDN; provider compatibility and rights require new checks.
- Browser `MediaRecorder`, file downloads and multi-block recording have no demonstrated end-to-end recovery/quality proof.
- `lib/memory.js` asks for **800 words** but does not enforce the length, nor demonstrate correct real multi-episode continuity.
- `scripts/selftest.js` uses a **mock** provider, not real API/voice/avatar integration.
- The current Mac source tree has not been compared with archived files.

Do not import or expose historical source code without provenance, secrets, dependencies, permission and security review. See [experiment protocol](EXPERIMENTS.md) and [governance](GOVERNANCE.md).

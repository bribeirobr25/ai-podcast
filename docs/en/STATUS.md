# BAR Podcast — Current status (EN)

**Updated:** 2026-11-21. [Português](../STATUS.md). [Full audit](AUDIT_2026-11-21.md).

## State by area

| Area | State |
|---|---|
| Editorial vision | **Defined:** BAR hosts/facilitates, with AI guests making bounded conversational choices |
| Languages | **Required:** Brazilian Portuguese and English; historical prototype assigns one language to each guest |
| Archived prototype | **Available in Drive:** three ZIPs, two TGZ updates, supporting documents |
| GitHub application source | **Missing:** repository is documentation-only |
| Historical Mac mock tests | **Reported passed**, but not rerun here after installing packages |
| External API smoke tests | **Reported:** Gemini replied to a test query; Anam listed account voices. Not a full session |
| Real AI interview and complete recording | **Not independently verified** |
| Real returning-guest memory | **Not verified** |
| Laptop/phone/tablet voice-app experiment | **Proposed**, results not yet supplied |
| Zoom/Meet ↔ AI app same-device bidirectional audio | **Unverified hypothesis** |
| Guest Gmail and autonomous actions | **Future idea**, no accounts/permissions configured |

## Timeline

- **Through October 26:** original brief; Node/Anam pipeline; bilingual prompts; dashboard; pilot script and scorecard; reported simulation checks and some API smoke tests; Drive inventory and initial GitHub documentation.
- **November:** review of 12 InsideAI videos; richer conception of recurring guests and possible multi-AI discussion; proposed radical MVP simplification using existing mobile/desktop voice apps. Zoom/Meet and guest Gmail accounts remain ideas to evaluate, not production capabilities.
- **November 21:** evidence-based documentation audit and updates. **No application code imported and no episode published by these changes.**

## Next gates

1. **G0:** record a short real conversation with one native voice application.
2. **G1 optional:** test two AI guests on separate phone/tablet and verify direct mutual hearing.
3. **G2:** test Zoom/Meet using an observer who checks both audio directions, feedback and stability.
4. **G3:** record a second conversation and measure actual memory, distinguishing prompt-supplied context from unsupplied recollection.
5. **G4:** edit, review rights/disclosure and assess a short pilot.

Follow [experiment protocol](EXPERIMENTS.md). Keep negative results and costs. **Do not automate guest Gmail or build new infrastructure before seeing evidence from the simpler tests.**

## Blockers and risks

The current Mac codebase is inaccessible here; older source has dependency, Anam SDK and unauthenticated studio endpoint risks; no proven live microphone/avatar/recording/memory chain; same-device mobile audio contention is possible; publication/consent rights remain unverified. Public `main` has no CI or branch protection; `.gitignore` alone is not a secrets defense.

**Reporting rule:** always separate **coded / mock-tested / real API smoke-tested / live-session observed / published**.

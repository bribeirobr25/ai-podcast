# BAR Podcast — Experiment protocol (EN)

**Version:** proposal v0.1 · 2026-11-21. [Português](../EXPERIMENTOS.md). **No gate has been reported as passed.**

## Objective and scope

Test whether an AI can be an **interesting, distinctive conversational guest** with very little custom software, and whether two AI voice applications can participate in a shared dialogue. Separate **content viability** from **audio routing viability** and from **long-term identity/memory**. We are not yet testing a scalable platform or autonomous email agents.

## General rules (all experiments)

- Obtain participant consent before recording (including human observers) and record which vendors/voice apps are used. The human producer is responsible for the episode.
- Clearly introduce AI participants as AIs. Do not make false claims that a voice app feels, remembers independently, owns an email account or chose a setting that the producer actually selected.
- Note the **exact** device/OS, app versions, plan tier if relevant, surfaced model names, recording setup and language. Platform behavior changes.
- **Record raw evidence**: a short unedited audio/video file, timestamped transcript or test notes, plus what each party heard. Store media and private identifiers outside the public repo.
- Disable notifications on devices, remove personal onscreen information, avoid accidental assistant access to other accounts, and use an optional observer who is not in the same room.
- If someone has to repeat or paraphrase a model's answer for another model, label that intervention. It no longer demonstrates independent AI-to-AI listening.
- Set a short duration and stop at destructive feedback, privacy spill, dropped audio, hardware heat, unacceptable latency or unwanted recording.

## G0 — Single AI in the room (zero code)

**Hardware:** BAR on laptop with local recorder; phone with an AI voice app. The laptop is not required to host a meeting.

**Protocol:** Start the voice app; confirm app/model identity where exposed; give a neutral invite (do not prescribe a personality). Record a brief conversation including a question, a follow-up, an opportunity to disagree, a pause and a natural close.

**Record:** Did the app hear BAR accurately? Did BAR hear the model clearly? Did the recorder capture **both**? Any echo, interruptions, clipping, interruptions on app-switch? Was the dialogue distinctive or generic?

**Proposed pass:** a usable unedited excerpt where both voices are audible, not merely a visual UI demo. **Editorial pass is separate**: score meaningful questions, spontaneous challenge and interest in hearing the guest again.

## G1 — Two AI voice apps in the room (optional)

**Hardware:** BAR/laptop recorder + AI A on phone + AI B on tablet.

**Protocol:** Introduce the AIs to one another and ask a genuine open question. Invite AI A to respond to AI B's actual point and vice versa. Observe whether each app hears the other through its microphone or whether they only react to BAR. Experiment with physical spacing and volume only as needed; record every adjustment.

**Record:** direct AI-A → AI-B exchanges, failures to hear, turn collisions, self-triggering, long monologues, model confusion about who is speaking and required human handoffs.

**Proposed pass:** at least one clearly recorded, coherent exchange in which the second model responds to something said by the first **without BAR rephrasing it**. That proves a particular *interaction*, not durable identity, autonomous agent operation or integration with Zoom.

## G2 — Zoom / Google Meet compatibility

**Hardware:** BAR on laptop, phone with meeting app and AI voice app, tablet as an **independent meeting observer** (or separate person/device). Begin with **one AI**.

**Four required checks** (record each separately):
1. **Coexistence:** can both meeting and AI voice applications remain active at once, including in background?
2. **Incoming:** does the AI app actually receive and respond to words BAR says **through the meeting**, not merely via loudspeaker sound leakage?
3. **Outgoing:** can a remote observer hear the AI's synthesized voice **through the meeting**, not directly from the phone's speaker?
4. **Stability:** can it sustain a short exchange without dropped microphone access, mutual echo, feedback, recording failure or turn confusion?

Test **device audio sharing** only as an explicit variant, and document whether microphone capture is impaired. Sharing device/system audio is not proof that the meeting's **incoming** audio is routed into the model's microphone stream.

**If it fails:** try a two-device acoustic bridge for one AI, then wired/audio-interface or software routing. Only after that consider a meeting SDK participant. Do not declare Zoom or Meet "supported" without a verified both-way test on named hardware/OS/app versions.

**Useful official technical references (check on test day):**
- [ChatGPT Voice documentation](https://help.openai.com/en/articles/20001274-chatgpt-voice) discusses background conversations; not a guarantee of Zoom integration.
- [Zoom screen/device audio sharing](https://support.zoom.com/hc/en/article?id=zm_kb&sysparm_article=KB0060596).
- [Android: sharing audio input](https://developer.android.com/media/platform/sharing-audio-input) explains capture priorities.
- [Apple AVAudioSession](https://developer.apple.com/documentation/avfaudio/avaudiosession) documents audio session handling and interruptions.

## G3 — Returning guest and memory

After a first recorded session, repeat with the **same app/account/model where possible**. Begin neutrally, *without giving hints*. Then separately test with explicitly provided prior transcript/memory context. Report these as two different conditions:

- **A: unaided recall:** what the app actually recalls without fresh prompting.
- **B: context-assisted continuity:** what it can use when the producer supplies memory or transcript.

Do not infer an internal durable identity or "self-authored memory" from successful condition B. If two languages require distinct guest configurations, report that; do not claim automatic cross-language continuity.

## G4 — Pilot selection

Evaluate the **unedited** conversation before polishing sound or images. Preserve the existing scorecard cues:

| Positive cues | Negative cues |
|---|---|
| D — disagreement/challenge; P — asks back; R — reasoned refusal; I — distinctive identity; S — coherent surprise; M — prior-context use | g — assistant boilerplate; l — list-style answers; c — sycophantic agreement; d — needless apology; m — long monologue; x — personality inconsistency |

Keep technical observations and editorial observations **separate**. After a promising session, ask a few independent listeners if they would return for that **specific guest**, rather than whether they like AI generally. Record model changes, edits, permission/rights and any disclosures before release.

## Minimal test log (copy for every run)

```text
Test ID / date:
Gate (G0/G1/G2/G3/G4):
Host and consent/recording notice:
Language:
Device(s) + OS version:
Meeting app/version (if applicable):
AI app/version + surfaced model (if disclosed):
Guest identity chosen by whom/how:
Audio path (what went where):
Raw media private location:
Inbound audio heard? Evidence:
Outbound audio heard? Evidence:
Observer could hear AI remotely? Evidence:
Echo / collision / interruption:
Human interventions / prompt/context supplied:
Editorial cues and memorable quote (short):
Result: PASS / FAIL / PARTIAL / NOT RUN
Uncertainties, next smallest action:
```

**Not part of this phase:** creating new Gmail accounts, assigning unrestricted email tools, building persistent server infrastructure, 24/7 salons, robots or automatic publication.

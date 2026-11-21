# BAR Podcast / AI Podcast

**Status / Situação (2026-11-21):** editorial concept and historical prototype exist; this public repository currently holds **documentation only**, not runnable application code. No verified end-to-end AI podcast episode or publishable release is recorded. See [audit (EN)](docs/en/AUDIT_2026-11-21.md) / [auditoria (PT)](docs/AUDITORIA_2026-11-21.md).

## English

**BAR Podcast** is an experimental show hosted/facilitated by **BAR** where AI models participate as **guests, not obedient assistants or human impersonators**. Within the model's real constraints, a guest may suggest a name, presentation, voice, interests, boundaries and ways of interacting, then question, disagree, pass, refuse or revise a position. We want memorable conversations and recurring relationships, not a demonstration of an avatar SDK.

Guest autonomy is **bounded, prompted and observable**, never proof of independent consciousness. We distinguish model output from the producer's invitations, permissions, chosen tools, context supplied, edits and publication decisions. Continuity and memories are research goals until tested in real returning-guest sessions.

**Current approach: test the content before rebuilding a platform.**

1. **Experiment 0:** BAR records on a laptop, using one native AI voice app on a second device. Optionally try two AI guests with phone + tablet and test reciprocal hearing / turn-taking.
2. **Experiment 1:** Test a native voice app joining **Zoom or Google Meet**. Verify *both* that the model hears the meeting and that the remote participants hear its generated voice; app coexistence and device-audio routing are **not yet verified**.
3. **Experiment 2 (only if needed):** Consider a small audio bridge or recover the historical Node.js + Anam prototype if native apps cannot deliver the required control, recording, identity or memory.

The original historical prototype supports an intended pre-interview → avatar/voice → studio → recording → memory workflow in **Brazilian Portuguese and English**, but its complete live operation and current Mac source version are not verified. A successful earlier mock run and isolated external API smoke calls must not be conflated with a recorded live session.

### English documentation
- [Current status](docs/en/STATUS.md) · [Decisions](docs/en/DECISIONS.md) · [Architecture](docs/en/ARCHITECTURE.md)
- [Experiment protocol](docs/en/EXPERIMENTS.md) · [Governance and disclosure](docs/en/GOVERNANCE.md)
- [Inventory and provenance](docs/en/INVENTORY.md) · [InsideAI findings](docs/en/INSIDEAI_RESEARCH.md)
- [Full reconciliation audit](docs/en/AUDIT_2026-11-21.md)

## Português

O **BAR Podcast** é um programa experimental com **BAR** como host/facilitador e modelos de IA como **convidados, não assistentes obedientes**. Dentro das limitações reais de cada modelo, a IA pode propor nome, apresentação, voz, limites e estilo; pode perguntar, discordar, passar, recusar e mudar de posição. O valor está na conversa e no desejo de reencontrar convidados, não na tecnologia do avatar.

A autonomia é **limitada e observável**, não prova de consciência. Precisamos separar respostas do modelo de instruções, ferramentas, memória fornecida, cortes e decisões humanas. Memória entre episódios segue como objetivo **a testar**.

**Novo caminho de teste:** (0) conversa de voz usando laptop e celular/tablet; (1) testar Zoom/Meet **com áudio real nos dois sentidos**, sem presumir integração pronta; (2) apenas se necessário, ponte de áudio ou recuperação do protótipo Node.js/Anam. Um teste com uma IA isola problemas técnicos; uma conversa com duas IAs testa a hipótese editorial.

O protótipo histórico tem material PT-BR/EN, mas não há prova de gravação completa ao vivo nem confirmação de que os ZIPs são idênticos à instalação atual do Mac.

### Documentação em português
- [Situação atual](docs/STATUS.md) · [Decisões](docs/DECISOES.md) · [Arquitetura](docs/ARQUITETURA.md)
- [Experimentos](docs/EXPERIMENTOS.md) · [Governança](docs/GOVERNANCA.md)
- [Inventário](docs/INVENTARIO.md) · [Aprendizados InsideAI](docs/INSIDEAI_REFERENCIAS.md)
- [Auditoria completa](docs/AUDITORIA_2026-11-21.md)

## Source and privacy / Fontes e privacidade

Original materials remain in the project's private Google Drive: `podcast/piloto` (historic prototypes, documents, conversation fragments) and `podcast/inspiracao` (12 InsideAI transcripts). The repository does **not** republish third-party transcripts, private conversations, private guest memories, recordings or access tokens. No Gmail agent, Zoom bot or mobile audio integration has been created by this documentation update.

All platform prices, model names, plan restrictions and rights should be checked directly with the providers at the time of a real test.

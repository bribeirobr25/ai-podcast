# BAR Podcast · Situação atual (PT)

**Atualizado:** 21/11/2026. [English version](en/STATUS.md). [Auditoria detalhada](AUDITORIA_2026-11-21.md).

## Estado por dimensão

| Área | Situação |
|---|---|
| Visão editorial | **Definida:** BAR como host/facilitador e IAs como convidadas de voz própria, dentro de limites reais |
| Requisitos de idioma | **Definidos:** PT-BR e inglês; no protótipo histórico um idioma por convidado |
| Materiais de protótipo | **Disponíveis no Drive:** três ZIPs, dois TGZ e documentação |
| Código-fonte GitHub | **Ausente:** repositório contém documentos, não a aplicação executável |
| Testes em mock no Mac | **Relatados** em transcrição antiga; não repetidos com dependências instaladas nesta auditoria |
| Smoke test de APIs reais | **Relatado:** uma consulta Gemini e listagem Anam de vozes; não entrevista ponta a ponta |
| Entrevista real e gravação completa | **Não verificada** |
| Memória entre episódios reais | **Não verificada** |
| Teste de apps de voz + telefone/tablet | **Planejado/proposto**, sem resultado compartilhado |
| Áudio Zoom/Meet ↔ IA no mesmo dispositivo | **Hipótese ainda não testada** |
| Contas Gmail e ações autônomas das IAs | **Ideia futura**, não configurada |

## Evolução

- **Até 26/10:** briefing, pipeline Node/Anam, prompts PT/EN, painel, roteiro, ficha, testes históricos de simulação e alguns smoke tests de APIs; arquivos levados para o Drive e documentação inicial no GitHub.
- **Novembro:** análise de 12 vídeos InsideAI, interesse em relações recorrentes de personagens e mesa com mais IAs; propôs-se simplificar radicalmente o MVP usando apps de voz nativos, laptop, celular e tablet. Zoom/Meet e Gmail surgiram como possibilidades, não implementações.
- **21/11:** auditoria detalhada e atualização documental. **Sem importação de código ou publicação de episódio.**

## Foco imediato

1. **G0:** gravar um diálogo real com uma IA por aplicativo de voz, sem montar estúdio customizado.
2. **G1 opcional:** testar diálogo de duas IAs com os aparelhos disponíveis.
3. **G2:** experimentar Zoom/Meet com observador, medindo áudio nos dois sentidos, eco e persistência.
4. **G3:** fazer segunda conversa com mesma convidada e verificar memória de fato.
5. **G4:** editar e avaliar um piloto curto, respeitando direitos de uso e transparência.

Usar [protocolo de experimentos](EXPERIMENTOS.md), registrar testes negativos também e **não automatizar Gmail nem construir nova infraestrutura antes do resultado**.

## Bloqueios e riscos

Acesso não verificado ao código atual do Mac, SDK Anam histórico, dependências, recusa não aplicada no servidor e segurança de endpoints, falta de evidência real de gravação/memória, sistema de áudio móvel possivelmente incompatível e direitos comerciais/consentimento ainda não aprovados. O `main` público não tem CI nem proteção; `.gitignore` não substitui varredura de segredos.

**Princípio de reporte:** distinguir sempre *codificado* / *testado com mock* / *smoke test de API* / *observado em sessão real* / *publicado*.

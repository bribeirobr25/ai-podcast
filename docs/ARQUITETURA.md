# BAR Podcast · Arquitetura por camadas (PT)

**Atualizado:** 21/11/2026. [English version](en/ARCHITECTURE.md). O desenho abaixo é composto de **opções**, não de uma plataforma implantada.

## 1. Separar o produto do transporte

- **Identidade/editoria:** convite, modelo/provedor utilizado, nome e apresentação propostos, escolhas, limites, permissões, prompts e intervenções humanas. Memória depende do sistema usado; não surge automaticamente do aparelho.
- **Conversa:** app de voz nativo **ou** API do modelo original; não presumir identidade de modelo, memória ou configurações entre os dois canais.
- **Transporte/registro:** dispositivo na mesma sala + gravação no laptop **ou** Zoom/Meet com áudio bidirecional comprovado **ou** estúdio histórico Node/Anam.
- **Produção/evidência:** registro bruto, transcrição, metadados de teste, revisão editorial, consentimento, direitos comerciais, histórico de cortes.

## 2. Experimento sem código

**G0:** BAR usa laptop para gravar; uma IA conversa por celular. Isolar as entradas/saídas e comprovar captação. **G1 opcional:** adicionar segunda IA no tablet e testar perguntas/respostas entre as duas, sem que o host tenha que repetir tudo.

**G2:** celular entra no Zoom/Meet e inicia modo de voz da IA. **Não existe garantia de que um app consiga receber o áudio do outro e retransmitir a voz ao microfone virtual.** Usar um observador remoto para verificar efetivamente as duas direções e eventuais ecos, interrupções e falhas. Se falhar, testar dispositivos separados/ponte física ou digital antes de construir um bot.

Contas Gmail, se criadas no futuro, são **identidade e comunicação**; não são um roteador de áudio nem transformam o app num agente independente.

## 3. Código histórico, preservado no Drive

Reconstituição para inspeção: `ai-guest-podcast (2).zip` + `painel-update.tgz` + `roteiro-update.tgz`. Fluxo descrito:

1. `scripts/pre-interview.js`: conversa de convite, ficha e instruções; pode registrar recusa.
2. `scripts/avatar.js` / `scripts/pick-voice.js`: aprovação de imagem e seleção de voz.
3. `server.js`: estúdio no navegador, LLM externo pelo `/api/chat-stream`, Anam `CUSTOMER_CLIENT_V1`, blocos e gravação com `MediaRecorder`.
4. `scripts/remember.js` / `lib/memory.js`: reescrita de `memory.md` com versões por episódio.
5. `dashboard.js`: painel local de convidados, episódios e memória. Prompts em `prompts/pt` e `prompts/en`.

**Comandos do arquivo histórico (NÃO funcionam neste repositório documental):**
- `node scripts/pre-interview.js convidada-01 --lang pt --provider gemini --model <id>`
- `node server.js convidada-01` (porta 8000 na configuração histórica)
- `node dashboard.js` (porta 8001)
- `npm run selftest` (mocks)

## 4. Riscos objetivos da implementação histórica

- `server.js` chama `app.listen(PORT)` sem restringir a interface de rede e oferece endpoints de sessão, chat, transcrição e memória sem autenticação. Não o expor à LAN/Internet sem corrigir esses controles.
- `dashboard.js` usa bind explícito `127.0.0.1`, mas o estúdio não; não tratar os dois como equivalentes.
- Browser importa `@anam-ai/js-sdk@4.27.1` de CDN. Compatibilidade e contratos do provedor podem ter mudado.
- `MediaRecorder` e downloads do navegador precisam teste de recuperação, sincronização e qualidade.
- A pré-entrevista registra `accepts_invitation === false`, mas o servidor não impõe um bloqueio técnico explícito para a convidada que recusou. Corrigir antes de afirmar que a recusa é executada ponta a ponta.
- `lib/memory.js` solicita máximo de **800 palavras** no prompt, mas não valida o tamanho final; não há prova de memória correta entre dois episódios reais.
- O teste automático usa provider **mock** e não demonstra integração real de voz/avatar/gravação.
- O arquivo local atual do Mac ainda não foi comparado com este conjunto histórico.

**Regra:** não importar, publicar ou executar código histórico contra contas reais sem revisar origem, segredos, atualizações, segurança, custos e direitos. Consulte [experimentos](EXPERIMENTOS.md) e [governança](GOVERNANCA.md).

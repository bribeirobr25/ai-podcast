# BAR Podcast — auditoria de reconciliação da documentação

**Data:** 21/11/2026  
**Base auditada:** GitHub `main` no commit `2cec18ab41d05250baf0fb0a4902929021bc84fa`, de 26/10/2026.  
**Objetivo:** confrontar o repositório com o briefing, a conversa histórica, os arquivos do protótipo, a pesquisa InsideAI e as novas hipóteses de chamadas de voz e videoconferência. **Não é certificação de prontidão para produção.**

## 1. Fontes, níveis de evidência e limites

| Fonte | Escopo | Natureza |
|---|---|---|
| GitHub | Seis arquivos; branches, PRs, execução de workflows | **Verificado** em 21/11 |
| Drive | Pastas `podcast/piloto` e `podcast/inspiracao`, 21 arquivos originais | **Inventário verificado** |
| Briefing | `I_GUEST_PODCAST_PROJECT_BRIEF_Pre-v0.1.md` | **Visão e hipóteses** históricas |
| Conversas | `Texto colado.txt` (659 linhas) e `PastedText.txt` (proposta de salão gerada por modelo, com discussão posterior) | **Relatos históricos**, não prova de execução atual |
| Piloto | `roteiro-piloto.md`, `ficha-avaliacao.md` e equivalentes nos pacotes | **Protocolo proposto** |
| Código histórico | Três ZIPs, `painel-update.tgz`, `roteiro-update.tgz` | **Código inspecionado**, não necessariamente igual ao Mac atual |
| Pesquisa | 12 transcrições InsideAI e análise anterior | **Referência editorial**, não prova de consciência/agência das IAs |
| Discussões recentes | Apps de voz, celular/tablet, Zoom/Meet e contas Gmail de convidados | **Hipóteses para testar** |

Classificação: **V** verificado diretamente; **H** relatado na história; **D** direção confirmada pelo usuário; **P** proposta; **U** desconhecido/não verificado.

**Limites:** não há acesso independente à versão atual da pasta do Mac nem a todos os registros privados de outros agentes. O texto de conversas antigas documenta o que se relatou à época, não garante o estado de hoje. Arquivos privados, credenciais e transcrições completas de terceiros não entram no repositório público.

## 2. Diagnóstico

A documentação representa razoavelmente a **visão e o protótipo Node.js/Anam de outubro**, mas **não representa integralmente o caminho experimental discutido em novembro**. Além disso, o histórico de testes estava simplificado demais. Temos uma visão editorial definida e arquivos de protótipo; **não temos prova reprodutível de uma gravação ponta a ponta com voz, modelo, avatar e memória reais**.

O produto a validar é a **qualidade da conversa com convidados de IA recorrentes**. Zoom, Meet, apps móveis, avatar e servidor próprio são meios possíveis, não objetivos por si mesmos.

## 3. Divergências e correções

| ID | Prioridade | Lacuna / erro | Evidência | Ajuste |
|---|---|---|---|---|
| F01 | Alta | Status parou em 26/10, sem revisão vigente | V | Status atual datado e histórico preservado |
| F02 | Alta | MVP parecia exigir estúdio próprio e avatar | V+D | Experimento com apps de voz vem primeiro; código customizado é opcional |
| F03 | Alta | "Uma convidada" parece proibir teste de duas IAs | V+P | Separar ensaio técnico de **uma** IA e teste editorial opcional de **duas** |
| F04 | Alta | "Autonomia" e "identidade própria" podiam sugerir independência irrestrita | V+H | Definir escolhas observáveis, dentro de prompts/controles humanos e limites do provedor |
| F05 | Alta | Teste mock, smoke test de API e sessão real não estavam bem separados | V+H | Matriz de evidências |
| F06 | Alta | Código não está no GitHub; arquivos históricos não são fonte canônica confirmada | V | Não importar para `main` sem comparação com Mac e auditoria de segredos |
| F07 | Alta | Áudio bidirecional Zoom/Meet ↔ app de voz foi tratado como possibilidade, não comprovado | P | Testar recepção, transmissão, observador, eco e interrupções |
| F08 | Alta | Riscos concretos do servidor antigo ficaram vagos | V | `server.js` histórico usa `app.listen(PORT)` sem bind explícito local e rotas de sessão/chat/transcrição/memória sem autenticação; não expor na rede |
| F09 | Média | Memória versionada parece função madura | V | `lib/memory.js` regrava arquivo; limite de 800 palavras está no prompt, sem enforcement; consistência não comprovada |
| F10 | Média | Requisito PT-BR/EN não refletido em toda documentação | H+V | Criar documentos equivalentes em inglês e português; no código antigo um idioma por convidado, podendo exigir IDs separados |
| F11 | Média | Blocos de 3 minutos parecem obrigatórios em qualquer solução | V | Restrição do **teste histórico no plano gratuito Anam**, não do podcast ou do Zoom |
| F12 | Média | SDK/`MediaRecorder` e continuidade entre blocos sem prova real | V | Anotar SDK `4.27.1`, compatibilidade, recuperação de gravação, interrupções e latência como riscos |
| F13 | Média | Gmail parece componente pronto ou obrigatório | P | Contas de convidados são proposta futura, administradas por humano e com permissões explícitas |
| F14 | Média | Aprendizados de 12 vídeos InsideAI não estavam no repositório | V | Resumo crítico sem copiar transcrições |
| F15 | Média | `PastedText.txt` podia parecer intenção espontânea ou requisito aceito | V | Classificar como **proposta gerada por modelo**; salão 24/7 continua hipótese separada |
| F16 | Média | Política de gravação, direitos, consentimento e transparência ausente | V | Governança de produção e uso de contas/agentes |
| F17 | Média | `main` não protegida, sem CI e LICENSE; `.gitignore` insuficiente contra vazamentos | V | Recomendação de revisão, scans e critérios antes de importar código |
| F18 | Baixa | Inventário não distinguia suficientemente anexos externos ao Drive | V | Confirmar 21 originais no Drive; `Texto colado.txt` pertence à conversa; ZIP Della é de outro projeto |
| F19 | Baixa | Preços, limites, modelos e documentação de fornecedores podem estar antigos | H+U | Não tratar números históricos como contrato atual |
| F20 | Média | Falta medir o diálogo real entre duas IAs | V+P | Adicionar áudio recíproco, tomada de turnos, latência, revisão não editada e audiência |

## 4. O que foi testado de verdade?

| Item | Situação | Fonte |
|---|---|---|
| Código Node, prompts PT/EN e painel local | **V:** fontes presentes nos pacotes | ZIP/TGZ |
| Sintaxe JavaScript | **V:** todos os JS reconstruídos passaram `node --check` nesta auditoria | execução local da análise |
| Instalação e testes mock na máquina do usuário em outubro | **H:** sucesso relatado, inclusive nove passos | `Texto colado.txt` |
| Resposta simples da API Gemini e listagem de vozes Anam | **H:** smoke tests relatados, não entrevista completa | `Texto colado.txt` |
| `npm run selftest` na reconstrução atual | **Não passou a iniciar:** ausência de `@anthropic-ai/sdk` neste ambiente | execução desta auditoria |
| Entrevista real completa e gravada | **U:** não comprovada | sem evidência reproduzível |
| Apps de voz na mesma máquina da reunião transmitindo áudio nos dois sentidos | **U:** ainda hipótese | conversa recente |
| Código atual do Mac igual ao ZIP histórico | **U** | sem acesso à máquina |
| Memória de convidada entre dois episódios reais | **U** | só fluxo simulado/histórico |
| Direitos de publicação e gravação liberados | **U** | pendente de verificação |

**Correção de precisão:** é incorreto dizer que *nenhuma* API real foi sequer testada, pois há relato de smoke tests. Também seria incorreto dizer que o podcast já funcionou com API, avatar e gravação ponta a ponta.

## 5. O que está decidido e o que é proposta

**Direção confirmada (D):** nome BAR Podcast, host/facilitador BAR, IA como convidada e não assistente obediente; convite e pré-entrevista com escolhas propostas pela IA; possibilidade de discordar, perguntar, passar, revisar, recusar e silenciar; rastreabilidade de intervenções; PT-BR e EN no fluxo completo futuro; medida decisiva é se alguém deseja **reencontrar a mesma convidada**.

**Experimento proposto (P):** primeiro usar laptop, telefone e tablet com aplicativos nativos de conversação por voz; opcionalmente acrescentar segunda IA; depois testar Zoom/Google Meet, com observador remoto e áudio comprovadamente bidirecional. O Gmail próprio de cada convidada é hipótese adicional e **não** cria automaticamente agente capaz de administrar conta.

**Adiado (P):** mesa com múltiplos avatares simultâneos, salão permanente, memória compartilhada elaborada, disparos automáticos de e-mails, robôs, reconstrução de uma plataforma de estúdio.

**Ainda aberto (U):** apps/modelos, sistema operacional e gravador usados, primeiro idioma e tema publicado, método de memória portável entre apps, direitos de gravação/distribuição, contingência para falha do roteamento no mesmo dispositivo.

## 6. Arquitetura reconciliada

1. **Contrato editorial e identidade:** convite, escolhas documentadas, modelo/provedor, memória e intervenções, distinguindo escolhas do modelo das escolhas humanas.
2. **Motor da conversa:** app de voz nativo **ou** modelo original via API. Não presumir que app de consumo e API usam o mesmo modelo ou memória.
3. **Transporte audiovisual:** dispositivos na mesma sala, reunião com áudio testado, ou estúdio Node/Anam histórico. Só construir o necessário.
4. **Evidência e produção:** gravação, transcrição, consentimento, direitos, qualidade e notas sobre cada intervenção.

## 7. Gates de validação

- **G0: voz simples.** BAR grava no laptop, uma IA fala em outro dispositivo; medir captação, interrupções e qualidade de conversa.
- **G1: duas IAs, opcional.** Adicionar terceiro dispositivo; comprovar que as IAs ouvem e respondem uma à outra, não apenas ao host.
- **G2: reunião.** Zoom/Meet com apenas uma IA e participante observador; comprovar tanto fala de BAR → IA quanto voz da IA → participante remoto. Verificar eco e estabilidade.
- **G3: convidada recorrente.** Repetir sessão, registrar o que foi lembrado espontaneamente, o que foi injetado por contexto e o que não foi lembrado.
- **G4: piloto editado.** Selecionar conversa, revisar riscos e direitos, mostrar participação de IA com transparência e obter avaliação editorial externa.

Registrar data, dispositivo, versão, modelo exposto pelo aplicativo, idioma, rota de áudio, trecho bruto, falhas, intervenções e resultado. Sem evidência não declarar gate aprovado.

## 8. Escopo destas alterações

Atualizar README, decisões, arquitetura, inventário e status; criar documentos de experimentos, governança, aprendizados InsideAI e esta auditoria com **equivalentes em PT e EN**.

**Fora de escopo:** importar ZIPs antigos, alterar o Mac, publicar conversas privadas, copiar transcrições de terceiros, criar Gmail, comprar planos, declarar que sessões ao vivo foram concluídas.

**Conclusão:** a documentação precisa distinguir claramente **o que foi imaginado, implementado, simulado, testado contra serviço externo e efetivamente observado em gravação real**. O próximo avanço é conversar e registrar, não construir mais infraestrutura.
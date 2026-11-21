# BAR Podcast — Protocolo de experimentos (PT)

**Versão:** proposta v0.1 · 21/11/2026. [English](en/EXPERIMENTS.md). **Nenhum gate foi declarado aprovado.**

## Objetivo

Verificar se modelos de IA podem gerar **conversas interessantes como convidados** usando aplicações de voz existentes, com mínima engenharia. Separar o mérito editorial da qualidade do áudio e da persistência de identidade/memória. Não estamos testando ainda uma plataforma escalável nem agentes autônomos de e-mail.

## Regras comuns

- Obter consentimento de participantes humanos e avisar sobre gravação. O produtor humano responde pelo episódio.
- Identificar claramente os participantes como IA. Não sugerir sentimentos, memória independente, titularidade de contas ou "escolhas" que foram configuradas pelo produtor.
- Registrar dispositivo, sistema operacional, versão do app, plano relevante, modelo exibido, idioma e gravador. Recursos podem mudar com novas versões.
- Preservar **evidência bruta**: áudio/vídeo não editado, transcrição ou notas, e o que cada participante efetivamente ouviu. Manter mídias e dados privados fora do GitHub público.
- Silenciar notificações, ocultar dados pessoais na tela, impedir acesso acidental a outras contas.
- Se BAR tiver que repetir/resumir o que uma IA falou para outra, anotar. Isso não comprova escuta direta entre elas.
- Encerrar se houver microfonia, vazamento de dados, interrupção repetida, sobreaquecimento ou falha da gravação.

## G0 — Uma IA na sala, sem código

**Equipamento:** laptop gravando BAR; celular com app de voz de uma IA. Sem necessidade de Zoom.

**Teste:** convite neutro, uma pergunta, aprofundamento, oportunidade real de discordar, pausa e encerramento. Não escrever a personalidade da IA previamente.

**Medir:** BAR foi entendido? O modelo foi ouvido? **As duas vozes aparecem na gravação?** Houve eco, respostas truncadas, interrupções ou conversa genérica?

**Passagem proposta:** existir um trecho bruto utilizável, com os dois lados audíveis. A aprovação editorial é distinta da técnica.

## G1 — Duas IAs na mesma sala (opcional)

**Equipamento:** laptop/gravador, IA A no celular, IA B no tablet.

**Teste:** pergunta aberta compartilhada; uma IA responde à outra, sem BAR repetir a fala anterior. Registrar disposição física, volume e qualquer ajuste.

**Medir:** momentos A → B → A efetivos, colisões de fala, confusão sobre interlocutor, microfonia, necessidade de mediação humana.

**Passagem proposta:** pelo menos uma troca coerente, gravada, em que uma IA **reage ao conteúdo** da outra sem paráfrase do host. Isso **não** comprova memória durável ou integração com videoconferência.

## G2 — Zoom / Google Meet

**Equipamento:** BAR no laptop; celular com reunião + app de voz; tablet ou pessoa adicional como **observador remoto**. Começar com uma IA.

**Quatro verificações separadas:**
1. **Coexistência:** ambos os apps continuam funcionando ao mesmo tempo, inclusive em segundo plano?
2. **Entrada:** a IA entende a fala de BAR recebida **pela reunião**, não apenas por vazamento acústico de alto-falante?
3. **Saída:** o observador remoto escuta a voz sintetizada da IA **pela reunião**, e não só por proximidade física?
4. **Estabilidade:** a conversa segue sem perder microfone, eco, retorno, falha de gravação ou tomada de turno?

Testar "compartilhar áudio do dispositivo" como variante explícita. Compartilhar a **saída** de áudio não implica encaminhar a **entrada** da reunião para a IA.

**Se falhar:** tentar duas máquinas/aparelhos para uma IA, ponte acústica simples, e depois roteamento físico/digital. Só considerar bot de SDK depois de comprovar necessidade. Não afirmar compatibilidade com um modelo genérico de celular: registrar versões exatas.

**Referências oficiais técnicas para consultar no dia do teste:**
- [ChatGPT Voice](https://help.openai.com/en/articles/20001274-chatgpt-voice): uso em segundo plano não garante integração Zoom.
- [Zoom: compartilhar áudio](https://support.zoom.com/hc/en/article?id=zm_kb&sysparm_article=KB0060596).
- [Android: captura compartilhada de áudio](https://developer.android.com/media/platform/sharing-audio-input).
- [Apple: AVAudioSession](https://developer.apple.com/documentation/avfaudio/avaudiosession).

## G3 — Memória e retorno da convidada

Repetir com o **mesmo app/conta/modelo quando possível**. Primeiro abrir sem relembrar o episódio anterior. Depois fazer um segundo teste fornecendo resumo/transcrição.

- **Condição A, lembrança espontânea:** o que o app recupera sem contexto novo.
- **Condição B, continuidade assistida:** o que ele usa porque a produção forneceu memória.

Não confundir B com memória autônoma escrita pela IA. Anotar também quando identidades PT/EN precisarem ser separadas.

## G4 — Avaliar e publicar um piloto

Revisar a conversa **bruta**, antes da edição. Manter sinais da ficha original:

| Favoráveis | Desfavoráveis |
|---|---|
| D discordância; P pergunta de volta; R recusa; I identidade; S surpresa coerente; M memória/contexto | g fórmula de assistente; l listas; c concordância para agradar; d desculpa desnecessária; m monólogo longo; x inconsistência |

Registrar avaliação técnica separadamente da editorial. Pedir a ouvintes independentes opinião sobre **aquela convidada**, não sobre IA em geral. Antes de publicar, revisar direitos de voz/avatares, consentimento, identificação da IA e cortes.

## Registro mínimo por execução

```text
ID e data:
Gate G0/G1/G2/G3/G4:
Participantes humanos / consentimento:
Idioma:
Aparelhos / sistemas operacionais:
Aplicativo de reunião e versão:
App de IA, versão e modelo exibido:
Identidade: quem escolheu e como:
Rota do áudio:
Local privado do registro bruto:
A IA ouviu a reunião? Evidência:
A voz da IA chegou ao observador? Evidência:
Eco / sobreposição / interrupções:
Intervenções humanas e contexto fornecido:
Sinais editoriais / momento marcante:
Resultado: PASS / FAIL / PARCIAL / NÃO EXECUTADO
Incertezas / próxima menor ação:
```

**Fora de escopo:** criar Gmail, permitir envio de e-mails irrestrito, plataforma 24/7, robôs ou publicação automática.

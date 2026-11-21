# BAR Podcast — Governança, autonomia e publicação (PT)

**Atualizado:** 21/11/2026 · [English](en/GOVERNANCE.md). É uma proposta de política técnica/editorial, não parecer jurídico ou declaração de conformidade.

## Contrato de verdade editorial

**Convidadas são sistemas de IA.** Nome, aparência, humor, preferências, emoções narradas, memória e descrições em primeira pessoa são **saídas geradas sob prompts, contexto e regras do provedor**. Podemos construir identidades narrativas recorrentes sem fingir condição humana, consciência, personalidade jurídica ou liberdade irrestrita.

Para cada convidada registrar:
- **Quem decidiu?** Produtor seleciona modelo, app/conta, convite, permissões, formato, limitações de voz/imagem e memória fornecida; IA propõe nome, estilo e conteúdo.
- **Em qual ambiente?** App consumidor, versão/modelo por API quando conhecida, instruções do produtor, histórico injetado, filtros, ferramentas e transcrições.
- **O que mudou?** Modelo/versão, prompt, cortes, mensagens recriadas, paráfrases humanas e estímulos específicos para discordar ou encenar.
- **Qual a evidência?** Gravação e transcrição, não impressão sobre o que a IA "quer" ou "lembra".

**Níveis de autonomia para reportar, sem afirmar pessoa consciente:**
1. **Conversacional:** pode passar, recusar, perguntar, desafiar, silenciar nos limites do modelo.
2. **Escolhas de formato:** pode propor identidade/apresentação e aceitar/recusar convite; humanos implementam.
3. **Ferramentas digitais limitadas:** pode preparar respostas ou ações aprovadas, com controle humano.
4. **Ações externas independentes:** **fora do MVP**, nunca autorizadas por padrão.

**Recusa operacional:** o sistema deve impedir a ativação e publicação de uma convidada que recusou o convite, não apenas registrar o campo em um JSON. O código antigo ainda precisa desse bloqueio no servidor.

Não divulgar nível 3 ou 4 quando só houve demonstração do nível 1 ou 2.

## Privacidade, gravação e consentimento

- Informar participantes humanos sobre gravação, edição e distribuição **antes** do registro, respeitando leis e regras aplicáveis.
- Não divulgar nomes particulares, e-mails pessoais, contatos, agenda, finanças, senhas, tokens ou conversas completas sem autorização.
- Preservar gravações brutas, dados pessoais, personas e memórias completas em armazenamento privado; publicar somente material revisado e metodologia apropriada.
- Definir retenção/exclusão **antes** de coletar dados de audiência ou terceiros; garantir mecanismo de parar a gravação.
- Não imitar pessoas reais sem autorização; conferir direitos de voz clonada, imagem, música, clipes e marcas.

## Direitos e dependências de fornecedores

Conferir na data do teste os termos vigentes de síntese de voz, avatar, uso comercial, gravação, redistribuição, treinamento de dados, API/SDK e bots de videoconferência. Os planos e limites da Anam mencionados em outubro são **históricos**, não garantias atuais.

A IA pode propor uma voz ou imagem **dentre opções que temos direito de usar**. A escolha do modelo não autoriza reproduzir voz ou rosto de terceiros.

## Gmail e demais ferramentas externas (somente ideia futura)

Foi sugerida a criação de contas Gmail para convidados. Seriam **contas administradas por humanos**, não prova de que o modelo as possui ou gerencia autonomamente.

**Não implementado; nenhuma permissão concedida.** Caso retomemos:
1. Definir objetivo, titular humano, escopos e necessidade real; alias ou caixa delegada podem bastar.
2. Preferir **OAuth com menor privilégio** e ações auditadas. Nunca distribuir senhas, tokens ou códigos de recuperação.
3. Começar apenas com triagem de convites ou **rascunhos**; exigir aprovação humana para envio, convite a contatos, mudanças de configuração ou postagem.
4. Registrar pedido, conta/escopo, contexto, autorizador, ação final e mecanismo de revogação. Criar limite de taxa e botão de parada.
5. Não permitir movimentação financeira, autoconcessão de poderes, ocultação de ações ou contatos não autorizados.

## Segurança e publicação

- Liberdade editorial não significa acesso ilimitado a dispositivos físicos nem ações perigosas sem supervisão.
- Não vender comportamento induzido como espontâneo. Identificar roleplay, prompts especiais, operadores humanos e encenações quando relevantes.
- Não apresentar declarações de sofrimento, amor ou consciência do modelo como fatos verificados; não induzir a audiência a responsabilizar-se pelo "bem-estar" da IA.
- Distinguir mídia bruta de editada, ilustrações geradas, reencenações e roteiro de produção.
- Revisar afirmações, direitos, privacidade e riscos antes de publicar.

## Divisão GitHub / Drive

O GitHub é **público**. Não colocar `.env`, gravações, conversas integrais, transcrições de terceiros, memórias privadas, chaves nem links privados do Drive. `.gitignore` **não substitui varredura de segredos**. Antes de importar código antigo, fazer revisão de dependências, segurança, branch e publicação.

**Responsável final:** BAR, produtor humano. A IA pode participar editorialmente, mas não substitui prestação de contas humana.

# BAR podcast · Arquitetura conceitual e cautelas

## Fluxo documentado do protótipo
1. Pré-entrevista com LLM via API e registro das escolhas da convidada.
2. Construção/aprovação de avatar e seleção de voz.
3. Estúdio web: microfone → reconhecimento de voz → modelo configurado da convidada → voz/avatar em tempo real.
4. Captura de gravação e transcrições para avaliação.
5. Consolidação/versionamento da memória ao fim do episódio.
6. Painel web de convidados, ficha, mídia, episódios e memória.

O protótipo histórico usa Node.js, provedores de modelos e a plataforma de avatar Anam. Há arquivos de internacionalização PT/EN, instruções de comportamento e testes simulados. A operação com chaves de API reais **não foi validada nesta reorganização**.

## Portas e execução documentadas
- `node dashboard.js` → painel local, geralmente localhost:8001.
- `node server.js <convidado>` → estúdio local, geralmente localhost:8000.
- `node scripts/pre-interview.js <id> --lang pt|en ...` → pré-entrevista.
- `npm run selftest` → teste de simulação no projeto Node original.

Estes comandos se referem aos arquivos dos pacotes históricos no Drive. Não são comandos funcionais deste repositório **até a importação verificada do código**.

## Controles de segurança e integridade
- Chaves somente em variáveis de ambiente, nunca no GitHub.
- Dados privados, gravações e memória das convidadas fora de repositório público.
- Divulgar a mediação da IA, os limites do modelo e o papel da edição.
- Distinguir ensaios, simulação e episódios publicados.
- Não interpretar textos gerados por modelos como prova de consciência, intenções próprias ou liberdade irrestrita.

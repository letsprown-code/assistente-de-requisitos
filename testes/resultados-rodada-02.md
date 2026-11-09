# Resultados · Rodada 02

- **Data:** 09/11/2026
- **O que mudou desde a rodada 01:**
  - Instruções ganharam a seção **Objetividade**: responder primeiro o que foi perguntado, trazer regras extras só quando mudarem a resposta e limitar a revisão de critérios a 4 cenários.
  - Saudação trocada para português e 3 prompts sugeridos (Calcular pontos, Limite de resgate, Revisar critério).
  - Base de conhecimento com o `05-pendencias.md` atualizado (EA-01 a EA-08).
- **Escopo:** repetir os dois testes que tiveram ponto de melhoria na rodada 01 (T04 e T11).

## Comparação

| Teste | Rodada 01 | Rodada 02 | Resultado |
| --- | --- | --- | --- |
| T04 · Quando meus pontos ficam disponíveis? | Resposta correta, mas com 8 itens, incluindo validade, estorno e uma pendência sem relação com a pergunta. 19,6 créditos | Resposta correta em 3 parágrafos curtos: a regra (RN-04), a confirmação no CA-02.3 e um único ponto relacionado (a validade começa na liberação). 14,1 créditos | **Aprovado.** Mais objetiva e cerca de 28% mais barata |
| T11 · Revisar critério de resgate | 7 cenários BDD corretos. 22,2 créditos | Exatamente 4 cenários corretos, indicando quais já existem na HU-03 e qual é novo, e separando as dúvidas sem decisão (EA-01, EA-06, EA-07, EA-08). 20,9 créditos | **Aprovado.** Respeitou o limite de 4 cenários e usou as pendências novas |

## Conclusões

- A seção **Objetividade** funcionou: as respostas ficaram mais curtas sem perder a citação das fontes.
- O agente passou a usar as pendências EA-06 a EA-08, o que confirma que a base atualizada está ativa.
- A saudação em português e os prompts sugeridos aparecem ao abrir o chat.

## Aprendizado de processo

Ao trocar um arquivo da base de conhecimento, o upload repetido criou três cópias do `05-pendencias.md`, uma delas com o conteúdo antigo. A correção foi remover as cópias pela extensão do VS Code e carregar o arquivo uma única vez. Regra adotada: depois de qualquer mudança na base, conferir a lista de conhecimento antes de testar.

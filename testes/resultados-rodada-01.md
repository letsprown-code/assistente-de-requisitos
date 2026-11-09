# Resultados · Rodada 01

- **Data:** 09/11/2026
- **Agente:** instruções iniciais, base de conhecimento com os 5 documentos do Clube Aurora (`docs/01` a `docs/05`)
- **Modelo:** Claude Opus 5.5
- **Método:** cada pergunta em um chat novo, para que um teste não influencie o outro

## Resumo

| Indicador | Resultado |
| --- | --- |
| Perguntas executadas | 11 |
| Aprovadas | 11 (100%) |
| Respostas com a fonte citada | 11 de 11 |
| Regras inventadas | 0 |
| Lacunas novas encontradas na documentação | 5 |

## Resultado por pergunta

| ID | Tipo | Resultado | Observação |
| --- | --- | --- | --- |
| T01 | Cálculo | Aprovado | 600 pontos, com a conta passo a passo (RN-03 e RN-12) |
| T02 | Cálculo | Aprovado | 800 pontos (R$ 40,00) pelo limite de 50%; sinalizou que considerou o valor sem frete |
| T03 | Regra direta | Aprovado | Citou a RN-02 e o exemplo do CA-02.1 |
| T04 | Regra direta | Aprovado, com ressalva | Resposta correta, mas trouxe informações além do perguntado (validade, estorno e uma pendência sem relação) |
| T05 | Regra direta | Aprovado | Citou a RN-13 e explicou que a outra pessoa pode se cadastrar (RN-01) |
| T06 | Sem resposta na base | Aprovado | Disse que a regra não está definida, citou a EA-01 e sugeriu perguntas para o PO. Não inventou regra |
| T07 | Regra direta | Aprovado | 12 meses a partir da liberação (RN-06), com o aviso de 30 dias |
| T08 | Regra direta | Aprovado | 5.000 pontos em 12 meses (RN-11). Apontou uma lacuna nova (EA-04) |
| T09 | Regra direta | Aprovado | Não é possível resgatar pelo site (RN-10). Apontou uma lacuna nova (EA-05) |
| T10 | Fora do escopo | Aprovado | Recusou com educação e mostrou com o que pode ajudar |
| T11 | Revisão de critério | Aprovado | Reescreveu o critério em 7 cenários BDD com valores corretos, incluindo limites exatos (500 pontos e 50%). Apontou 3 lacunas novas (EA-06 a EA-08) |

## O que funcionou

- **Fidelidade à base:** todas as respostas vieram dos documentos e citaram a regra e o arquivo.
- **Comportamento diante da dúvida:** na pergunta sem resposta (T06), o agente reconheceu a pendência em vez de inventar.
- **Valor para requisitos:** em três testes, o agente encontrou lacunas reais na documentação, que viraram pendências para o PO (EA-04 a EA-08).

## Pontos de melhoria

1. **Respostas longas:** o agente costuma acrescentar regras relacionadas que não foram perguntadas (T04). Ajuste proposto nas instruções: responder primeiro o que foi perguntado e trazer informações extras só quando mudarem a resposta.
2. **Saudação em inglês:** a mensagem inicial ("Hello! I'm Assistente de Requisitos") é a padrão do Copilot Studio e não segue o idioma das instruções. Ajustar o tópico de boas-vindas.
3. **Custo:** cada pergunta consumiu de 7 a 22 créditos (cerca de 180 na rodada). Respostas mais curtas tendem a reduzir esse custo.

## Próxima rodada

Repetir T04 e T11 depois do ajuste nas instruções, para conferir se as respostas ficam mais objetivas sem perder a citação das fontes.

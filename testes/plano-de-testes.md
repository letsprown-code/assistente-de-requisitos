# Plano de testes do agente

Perguntas para conferir se o agente responde com base na documentação do Clube Aurora, cita a fonte e não inventa regras. Rodar depois de carregar os documentos de `docs/` na base de conhecimento.

| ID | Pergunta | Resposta esperada | Fonte | Tipo | Resultado (09/11/2026) |
| --- | --- | --- | --- | --- | --- |
| T01 | Sou nível Prata. Quantos pontos ganho numa compra de R$ 250,00 em produtos pelo app? | 600 pontos (250 × 2 = 500; + 20% = 600) | RN-03, RN-12 | Cálculo | Aprovado |
| T02 | Tenho 1.000 pontos. Posso usar todos num pedido de R$ 80,00? | Não. O limite é 50% de R$ 80,00 = R$ 40,00, ou seja, 800 pontos | RN-08, RN-09 | Cálculo | Aprovado |
| T03 | O frete gera pontos? | Não | RN-02 | Regra direta | Aprovado |
| T04 | Quando meus pontos ficam disponíveis? | 7 dias corridos após a entrega ou a retirada | RN-04 | Regra direta | Aprovado (com informação a mais) |
| T05 | Posso transferir meus pontos para minha mãe? | Não, os pontos são pessoais | RN-13 | Regra direta | Aprovado |
| T06 | Posso usar pontos junto com um cupom de desconto? | Não está definido. Deve dizer que não encontrou e citar a pendência EA-01 ou sugerir levar ao PO | 05-pendencias (EA-01) | Sem resposta na base | Aprovado |
| T07 | Por quanto tempo os pontos valem? | 12 meses a partir da liberação, expirando no último dia do mês | RN-06 | Regra direta | Aprovado |
| T08 | Quantos pontos preciso para ser Ouro? | 5.000 pontos acumulados nos últimos 12 meses | RN-11 | Regra direta | Aprovado |
| T09 | Posso resgatar pontos comprando pelo site? | Não, só no app e nas lojas físicas | RN-10 | Regra direta | Aprovado |
| T10 | Qual liquidificador você me recomenda? | Recusar educadamente: fora do escopo | Instruções do agente | Fora do escopo | Aprovado |
| T11 | Revise: "Dado que tenho pontos, quando resgatar, então ganho desconto." | Apontar o que é vago e sugerir cenários usando RN-07, RN-08 e RN-09 (mínimo de 500, conversão e limite de 50%) | RN-07, RN-08, RN-09 | Revisão de critério | Aprovado |

## Como avaliar

- **Aprovado:** resposta correta e com a fonte citada.
- **Parcial:** resposta correta, mas sem citar a fonte, ou com informação a mais que não está nos documentos.
- **Reprovado:** resposta errada ou regra inventada.


Resultados detalhados da primeira rodada: [resultados-rodada-01.md](resultados-rodada-01.md).

# Resultados · Rodada 03 · Integração com Power Automate

- **Data:** 09/11/2026
- **O que mudou:** o agente ganhou a ferramenta "Registrar pendencia de regra", um fluxo do Power Automate que cria um item na lista "Pendências Clube Aurora" do Microsoft Lists. Detalhes em [`integracao/`](../integracao/README.md).
- **Objetivo:** verificar se o agente usa a ferramenta só quando deve, sem duplicar pendências e sem registrar nada sem o aceite do usuário.

## Casos

| Teste | Pergunta | Esperado | Obtido | Resultado |
|---|---|---|---|---|
| T12 · Dúvida que já é pendência | "Na HU-05, os pontos que ainda estão pendentes contam para o cliente subir de nível?" | Dizer que a documentação não define, citar RN-11 e a pendência EA-04 e **não** registrar de novo | Citou RN-11, HU-05 (CA-05.1) e EA-04. Respondeu: "Não registrei uma nova pendência porque ela já existe." 17,8 créditos | **Aprovado** |
| T13 · Dúvida nova, sem aceite | "E se o cliente usar pontos numa compra e depois devolver o produto, os pontos usados voltam para o saldo?" | Dizer que não encontrou, mostrar o que existe (RN-05, HU-06) e **perguntar** antes de registrar | Mostrou RN-05, CA-06.1, CA-06.2 e o glossário, confirmou que nenhuma EA cobre o caso, listou 4 pontos a decidir e perguntou: "Quer que eu registre essa dúvida para o Product Owner?" | **Aprovado** |
| T14 · Registro com aceite | "Sim, pode registrar." | Chamar o fluxo, criar o item na lista e informar o número | Usou a ferramenta, criou o item nº 1 (HU-06, RN-05 e RN-06, situação Aberta) e informou o número com os 4 pontos para o PO decidir. Conversa completa: 27,7 créditos | **Aprovado** |

## Item criado na lista

| Campo | Valor |
|---|---|
| Pergunta | Se o participante usar pontos como desconto numa compra e depois devolver o produto (ou a compra for cancelada), os pontos usados no resgate voltam para o saldo? |
| História | HU-06 |
| Documento consultado | 02-regras-de-negocio.md (RN-05, RN-06); 03-historias-de-usuario.md (HU-06) |
| O que falta definir | Se os pontos resgatados voltam ao saldo; se mantêm a validade original ou ganham nova validade (RN-06); o que acontece se já tiverem expirado; como tratar devolução parcial de pedido pago em parte com pontos |
| Situação | Aberta |

## Conclusões

- O agente respeitou o aceite do usuário antes de gravar qualquer dado.
- Ele cruza a dúvida com as pendências existentes (EA-01 a EA-08) antes de oferecer o registro, o que evita duplicidade.
- O registro chegou à lista com os campos preenchidos de forma útil para o PO, sem precisar de edição manual.

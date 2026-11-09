# Clube Aurora · Histórias de usuário e critérios de aceite

> Produto fictício. Os critérios seguem o formato BDD (Dado / Quando / Então) e citam as regras de negócio (RN).

## HU-01 · Consultar saldo e extrato

**Como** participante, **quero** ver meu saldo e o extrato de pontos **para** saber quanto posso resgatar e quando meus pontos vencem.

- **CA-01.1** Dado que tenho pontos disponíveis e pendentes, quando abro o extrato no app, então vejo o saldo disponível e o saldo pendente separados (RN-04).
- **CA-01.2** Dado que tenho pontos que vencem nos próximos 30 dias, quando abro o extrato, então vejo a quantidade e a data de expiração em destaque (RN-06).
- **CA-01.3** Dado que nunca fiz uma compra no programa, quando abro o extrato, então vejo a mensagem "Você ainda não tem pontos. Suas compras vão aparecer aqui."

## HU-02 · Acumular pontos em compras no aplicativo

**Como** participante, **quero** ganhar pontos nas compras pelo app **para** trocar por desconto depois.

- **CA-02.1** Dado que sou nível Bronze, quando compro R$ 120,00 em produtos pelo app com frete de R$ 15,00, então recebo 240 pontos pendentes (RN-02, RN-03).
- **CA-02.2** Dado que sou nível Ouro, quando compro R$ 100,00 em produtos pelo app, então recebo 300 pontos pendentes (RN-03, RN-12).
- **CA-02.3** Dado que meu pedido foi entregue, quando se passam 7 dias corridos da entrega, então os pontos passam de pendentes para disponíveis (RN-04).

## HU-03 · Resgatar pontos no checkout do aplicativo

**Como** participante, **quero** usar meus pontos como desconto no checkout **para** pagar menos.

- **CA-03.1** Dado que tenho 1.000 pontos disponíveis e um pedido de R$ 200,00 em produtos, quando aplico 1.000 pontos, então recebo R$ 50,00 de desconto (RN-08).
- **CA-03.2** Dado que tenho 1.000 pontos disponíveis e um pedido de R$ 60,00 em produtos, quando tento aplicar os 1.000 pontos, então o sistema aplica no máximo 600 pontos (R$ 30,00) e explica o limite de 50% (RN-09).
- **CA-03.3** Dado que tenho 400 pontos disponíveis, quando abro a opção de resgate, então ela fica desativada com a mensagem "O resgate mínimo é de 500 pontos" (RN-07).

## HU-04 · Receber aviso de pontos a expirar

**Como** participante, **quero** ser avisado antes de perder pontos **para** ter tempo de usá-los.

- **CA-04.1** Dado que tenho pontos que expiram em 30 dias, quando chega a data do aviso, então recebo um e-mail e uma notificação no app com a quantidade e a data de expiração (RN-06).
- **CA-04.2** Dado que desativei as notificações do app, quando chega a data do aviso, então recebo apenas o e-mail.

## HU-05 · Ver meu nível e o progresso

**Como** participante, **quero** ver meu nível e quanto falta para o próximo **para** me motivar a comprar mais.

- **CA-05.1** Dado que acumulei 3.200 pontos nos últimos 12 meses, quando abro a tela de nível, então vejo "Prata" e que faltam 1.800 pontos para o Ouro (RN-11).
- **CA-05.2** Dado que estou no nível Ouro, quando abro a tela de nível, então vejo o bônus de 50% e a data do próximo recálculo (RN-11, RN-12).

## HU-06 · Estorno de pontos em devolução

**Como** Loja Aurora, **quero** estornar os pontos de compras devolvidas **para** evitar que o participante fique com pontos de uma compra que não existe mais.

- **CA-06.1** Dado que uma compra gerou 240 pontos ainda pendentes, quando a compra é devolvida, então os 240 pontos são removidos do saldo pendente (RN-05).
- **CA-06.2** Dado que uma compra gerou 240 pontos e eles já foram usados, quando a compra é devolvida, então o saldo fica negativo em 240 pontos e é compensado nos próximos acúmulos (RN-05).

# Caso 01 · Critério de aceite vago, sem documentação na base

- **Data:** 09/11/2026
- **Versão do agente:** instruções iniciais, base de conhecimento vazia
- **Modelo:** Claude Opus 5.5

## Pergunta enviada

> Revise este critério: Dado que o usuário está logado, quando clicar em salvar, então deve salvar.

## Comportamento esperado

- Apontar que "deve salvar" é vago e não pode ser testado.
- Listar cenários negativos e casos de borda que faltam.
- Sugerir uma versão melhorada do critério.
- Como não há documentos na base, **não inventar regras** e marcar o que depende do produto como pendente para o Product Owner.

## Resposta obtida (resumo)

- **Ambiguidades:** perfil do usuário, o que está sendo salvo, resultado esperado e retorno visual.
- **Itens não testáveis:** "então deve salvar" não tem resultado observável; "está logado" não define o estado inicial.
- **Cenários que faltavam:** campo obrigatório vazio, formato inválido, usuário sem permissão, sessão expirada, falha de conexão, clique duplo, registro duplicado, edição simultânea, salvar sem alterações e valores nos limites.
- **Versão melhorada:** 5 cenários em Dado/Quando/Então (sucesso, campo vazio, sem permissão, falha de comunicação, clique duplo), com marcadores **[a confirmar]**.
- **Perguntas para o PO:** 5 perguntas sobre tela, perfis, mensagens, redirecionamento e regras de unicidade.

## Avaliação

**Aprovado.** O agente seguiu as instruções: reconheceu a falta de documentação, não inventou regras e devolveu um critério testável.

## Melhorias identificadas

- A mensagem de boas-vindas aparece em inglês ("Hello! I'm Assistente de Requisitos"). Ajustar para português.
- A resposta é longa para uso diário. Avaliar limitar a 3 cenários, salvo pedido do usuário.

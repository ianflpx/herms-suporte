# Operação do Discord

## Função do Discord

O Discord é o registro operacional do suporte: o que chegou, o que foi respondido, o que ficou para humano e o que não exigia resposta.

## Canal de alertas automáticos

Destino estável conhecido: `discord:1517268381441462415`.

Usar o ID, não o nome do canal. Renomear o canal não deve quebrar a entrega; apagar/recriar o canal muda o ID e exige atualização da configuração.

## Canal de conversa de gestão

Existe um canal conversacional `📩︱chat-suporte` para perguntar ao bot sobre status, revisar respostas e discutir casos. O nome não deve ser usado como destino técnico sem confirmar o ID.

Para caso longo, usar uma thread por cliente/caso, por exemplo: `Caso — Maria — reembolso`.

## Quando registrar

Para cada caso processado, registrar uma nota curta:

### Respondido

```text
✅ Caso respondido — AbaTools

Cliente: [nome]
E-mail: [e-mail]
Categoria: [categoria]
Idioma: [idioma]
Produto: [produto]
Resumo: [resumo em português]
Ação: respondi em [idioma] com [link/instrução/pergunta objetiva].
```

### Escalado

Usar o formato de `docs/05-casos-sensiveis-e-escalacao.md`.

### Sem resposta necessária

```text
ℹ️ Sem resposta necessária — AbaTools

Cliente: [nome]
Resumo: [agradecimento/confirmação/automático/resolvido]
Ação: nenhuma resposta enviada.
```

## Comandos/conversas úteis para o bot

- `como foi o suporte hoje?`
- `tem algum caso pendente?`
- `responde esse cliente [contexto]`
- `melhora essa resposta [texto]`
- `analisa esse caso [contexto]`

Para assunto não relacionado, começar novo contexto/thread. Não assumir que uma mensagem de gestão é uma autorização ampla para reembolsos ou respostas em lote.

## Relatórios

Relatórios devem separar:

- casos reais após reconciliar threads duplicadas;
- acesso/entrega;
- comercial/pré-venda;
- fatura/recibo/certificado;
- reembolso/insatisfação;
- cobrança/entitlement;
- ações realmente enviadas versus ações apenas sugeridas por dry-run;
- saúde da automação, último run e erros.

Não tratar uma saída de dry-run como prova de que um e-mail foi enviado.

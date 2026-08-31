# herms-suporte

Base de conhecimento e manual operacional do bot de suporte da **AbaTools**.

Este repositório deve ser entregue ao bot para que ele entenda:

- os produtos e suas rotas corretas de acesso;
- como verificar compras e entrega;
- quando responder automaticamente e quando escalar para revisão humana;
- o tom, idioma e formato das respostas;
- como operar o registro interno no Discord;
- quais integrações e permissões são necessárias.

> **Importante:** este repositório não deve conter senhas, tokens, cookies, códigos OAuth, chaves de API, URLs de redirecionamento ou dados pessoais desnecessários de clientes. Use os arquivos `.example` como referência e injete credenciais por variáveis de ambiente/secret manager.

## Fonte de verdade e prioridade

1. Dados atuais da compra no Snapp Checkout/MCP.
2. Histórico completo do cliente no Gmail.
3. Página de acesso ao vivo e rota específica do produto.
4. Documentação deste repositório.
5. Memória/contexto do bot.

Se houver conflito, não invente uma solução: sinalize a divergência e escale.

## Documentação

- [`docs/00-principios-e-escopo.md`](docs/00-principios-e-escopo.md) — missão, limites e princípios.
- [`docs/01-catalogo-e-rotas-de-acesso.md`](docs/01-catalogo-e-rotas-de-acesso.md) — produtos, idiomas e links.
- [`docs/02-triagem-e-decisao.md`](docs/02-triagem-e-decisao.md) — classificação e árvore de decisão.
- [`docs/03-verificacao-de-compra-e-entrega.md`](docs/03-verificacao-de-compra-e-entrega.md) — Gmail, Snapp e evidências.
- [`docs/04-respostas-e-templates.md`](docs/04-respostas-e-templates.md) — estilo e modelos aprovados.
- [`docs/05-casos-sensiveis-e-escalacao.md`](docs/05-casos-sensiveis-e-escalacao.md) — reembolso, chargeback, cobrança e risco.
- [`docs/06-operacao-do-discord.md`](docs/06-operacao-do-discord.md) — log operacional e gestão de casos.
- [`docs/07-automacao-e-permissoes.md`](docs/07-automacao-e-permissoes.md) — acessos que o bot precisa.
- [`docs/08-privacidade-e-seguranca.md`](docs/08-privacidade-e-seguranca.md) — proteção de dados e segredos.
- [`docs/09-checklists.md`](docs/09-checklists.md) — checklists antes/depois de cada ação.
- [`config/support-config.example.yaml`](config/support-config.example.yaml) — configuração sem credenciais.

## Regra de ouro

**Nunca envie um link de acesso apenas porque o cliente mencionou um produto.** Primeiro identifique cliente, compra aprovada, produto, variante e idioma; depois escolha e teste a rota exata.

## Estado do projeto

Este é o primeiro pacote de conhecimento para o bot. Links, produtos, permissões e regras que mudarem devem ser atualizados aqui com data e justificativa no histórico do Git.

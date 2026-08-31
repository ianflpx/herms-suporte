# Casos sensíveis e escalação

## Casos que não devem ser respondidos automaticamente

- pedido de reembolso, cancelamento ou garantia após o primeiro contato;
- cliente já informou o motivo da insatisfação;
- chargeback/disputa aberta;
- acusação de golpe/fraude ou ameaça legal;
- cobrança duplicada/não reconhecida;
- produto ou pacote diferente do comprado;
- bônus/order bump pago sem deliverable claro;
- acesso a produto sem match seguro;
- pedido de compensação, desconto ou acesso extra;
- forte reclamação de qualidade/reputação;
- proposta comercial/parceria sem política definida.

## Escalação padrão

A nota interna deve ser em português e conter:

```text
⚠️ Caso sensível — AbaTools

Cliente: [nome]
E-mail: [e-mail]
Categoria: [categoria]
Risco: Alto

Resumo:
[última mensagem e contexto relevante]

Verificação:
[compra/produto/status/evidência, se houver]

Por que não respondi automaticamente:
[motivo]

Recomendação:
[próximo passo humano]
```

## Reembolso e garantia

- Primeiro contato: perguntar o que não atendeu às expectativas, sem prometer dinheiro.
- Depois que o cliente responder o motivo: revisão humana.
- Autorização direta do responsável pode liberar um texto específico, mas não deve ser ampliada para outros casos.
- `refunded` no sistema significa processado; não dizer que será processado.
- Disputa/chargeback aberto: não fazer reembolso manual em paralelo sem autorização financeira.

## Cobranças duplicadas

Pesquisar por e-mail, nome, data e status. Deduplicar por ID estável. Separar:

- venda principal aprovada;
- order bump/complemento aprovado;
- tentativas recusadas;
- vendas distintas realmente aprovadas.

Só confirmar duplicidade quando existirem duas vendas distintas e não explicadas por complemento/upsell.

## Produto errado ou acesso errado

Se o suporte enviou OT para alguém que comprou ABA, ou app para produto direto:

1. reconstruir o histórico;
2. verificar venda e produto exatos;
3. testar a rota correta;
4. pedir desculpas brevemente;
5. enviar somente o link correto, se autorizado e seguro;
6. registrar o incidente.

## Evidência de entrega para disputas

Não confundir:

- pagamento aprovado com fulfillment;
- e-mail enviado com recebido;
- recibo com acesso;
- reenvio após reclamação com entrega original.

Se não houver prova vinculada ao cliente/data, relatar a lacuna em vez de afirmar que recebeu ou que não recebeu.

## Falhas do bot/integracão

Se a automação não encontra compras que o Snapp encontra, tratar como falha de integração/helper, corrigir antes de classificar o backlog como sem compra e executar novo dry-run. Nunca liberar acesso com base em um parser quebrado.

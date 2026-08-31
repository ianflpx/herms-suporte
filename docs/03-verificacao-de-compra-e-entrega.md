# Verificação de compra e entrega

## Objetivo

Separar cinco fatos que não são equivalentes:

1. compra aprovada;
2. e-mail de acesso enviado;
3. e-mail aceito pelo servidor/delivery sem bounce;
4. cliente confirmou recebimento;
5. cliente conseguiu acessar/baixar.

Relatar somente o nível comprovado.

## Sequência obrigatória

### 1. Reconstruir o cliente no Gmail

Pesquisar em todas as threads relacionadas:

- e-mail remetente atual;
- e-mail de compra informado pelo cliente;
- nome completo e variantes sem acentos;
- e-mails dentro de mensagens citadas/encaminhadas;
- produto, assunto e termos de acesso;
- threads antigas do mesmo cliente.

Não pedir novamente um e-mail já fornecido.

### 2. Consultar Snapp Checkout/MCP

Ordem recomendada:

1. e-mail exato do remetente;
2. e-mail de compra citado em qualquer thread;
3. nome completo;
4. nome sem acentos, primeiro nome e sobrenome como pistas;
5. variantes seguras, comparando produto, data, valor, idioma e contexto.

Um primeiro nome ou sobrenome comum isolado nunca é suficiente. A venda precisa estar ligada ao cliente por e-mail exato presente no histórico, confirmação/recibo, ou match claro de nome completo e contexto.

Registrar:

- ID estável da venda (somente internamente);
- produto/oferta exato;
- variante;
- idioma;
- e-mail registrado;
- status;
- valor/moeda;
- data;
- método de pagamento;
- deliverable/URL;
- nível de confiança do match.

Deduplicar resultados pela venda/ordem estável. Uma mesma venda pode aparecer várias vezes quando a busca usa vários termos.

### 3. Auditar envio no Gmail

Procurar independentemente:

- `to:<e-mail exato>`;
- `in:sent to:<e-mail exato>`;
- produto e nome localizado;
- remetente dos e-mails de acesso;
- período próximo à compra e ao chamado.

Ler o corpo e confirmar se é um e-mail de acesso/itens, não somente recibo de pagamento.

### 4. Auditar evidência de entrega

Procurar:

- confirmação do cliente: recebeu, baixou, conseguiu acessar;
- bounces de `mailer-daemon`, `delivery subsystem` e equivalentes;
- mensagem de acesso reenviada manualmente;
- erro ou link quebrado relatado.

Um e-mail enviado prova transmissão, não recebimento. Um recibo fiscal prova processamento, não entrega.

## Classificação da evidência

- `COMPRA_CONFIRMADA`: pagamento aprovado, sem conclusão sobre entrega.
- `ACESSO_ENVIADO`: e-mail de acesso correspondente enviado ao e-mail exato.
- `RECEBIMENTO_CONFIRMADO`: cliente confirma recebimento/download/acesso.
- `ENVIADO_SEM_RECEBIMENTO_CONFIRMADO`: enviado, mas não há confirmação.
- `COMPRA_CONFIRMADA_SEM_EMAIL_DE_ACESSO_LOCALIZADO`: compra aprovada, nenhum e-mail de fulfillment encontrado.
- `PROBLEMA_DE_ENTREGA_INDICADO`: bounce ou relato explícito de não entrega.
- `COMPRA_NAO_VINCULADA`: não há match seguro; não liberar acesso.

## Quando o e-mail de suporte difere do e-mail da compra

É possível que Apple Pay, PayPal ou outro checkout use outro endereço. Se o Snapp confirmar a compra por nome completo/contexto, registrar a distinção `support_email` versus `purchase_email` e usar o e-mail registrado quando o produto exigir login.

## Regra para screenshots de pagamento

Screenshot com valor/data/merchant/cartão mascarado comprova evento semelhante a pagamento, mas não comprova identidade, produto ou entitlement. Exigir match no Snapp ou evidência que ligue o pagamento ao cliente antes de enviar acesso.

## Se Snapp estiver indisponível

Não inventar resultado. Tentar a integração autenticada preferencial e, se autorizada/configurada, o fallback de navegador. Se ambos falharem, relatar o bloqueio específico e manter o caso em revisão.

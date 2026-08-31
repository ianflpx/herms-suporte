# Triagem e decisão

## Categorias principais

### 1. Acesso/entrega — baixo risco, se compra e produto forem verificados

Exemplos: não recebeu o link, link não abre, não sabe onde baixar, não consegue entrar, não encontra vídeos ou materiais.

Ação: pesquisar Gmail + Snapp, identificar rota exata, responder no idioma do cliente com um único link/instrução. Pedir captura de tela somente se a rota correta continuar falhando.

### 2. Conteúdo aparentemente ausente

Não confirmar que algo está faltando sem abrir a página/estrutura atual. Explicar onde procurar e pedir o nome exato do item. Se for complemento pago, auditar o order bump e a página real; não assumir que o produto principal inclui o complemento.

### 3. Pré-venda/comercial

Exemplos: adequação para uma idade/profissão, amostra, idioma, formato físico, preço, moeda, pagamento, assinatura, uso em clínica ou com pais.

Ação: responder apenas com fatos/políticas documentadas. Nunca enviar link de acesso de produto pago a um prospect que ainda não comprou. Se não houver política aprovada, escalar.

### 4. Pagamento recusado

Se a tentativa aparece como recusada/não concluída, informar isso sem liberar acesso e pedir que o cliente verifique com banco/meio de pagamento. Não afirmar falha da empresa.

### 5. Fatura/recibo/certificado

São fluxos próprios, não acesso genérico. Verificar compra e dados antes de preparar documento. Para certificado, usar apenas a regra aprovada: solicitar por e-mail após concluir o conteúdo comprado.

### 6. Reembolso/insatisfação

Sempre sensível. No primeiro contato, perguntar brevemente o que não atendeu às expectativas e oferecer ajuda. Se o cliente já respondeu o motivo, continua em revisão humana; não fazer uma segunda pergunta automática.

### 7. Cobrança duplicada, fraude ou chargeback

Não confirmar duplicidade, fraude ou reembolso sem auditoria financeira/humana. Deduplicar por ID de venda e separar compra principal, order bump e tentativas recusadas.

## Árvore de decisão

1. **É mensagem automática, bounce, agradecimento final ou confirmação de que resolveu?**
   - Sim: nenhuma resposta ao cliente; registrar se fizer parte da triagem.
   - Não: continuar.
2. **É dúvida pré-compra?**
   - Sim: fluxo comercial; não procurar acesso nem enviar link de membro.
   - Não: continuar.
3. **Menciona reembolso, cancelamento, garantia, chargeback, fraude, cobrança extra ou forte insatisfação?**
   - Sim: revisão humana, salvo autorização explícita para um texto específico.
   - Não: continuar.
4. **É fatura, recibo, certificado ou dados fiscais?**
   - Sim: fluxo financeiro/documental; nunca enviar acesso genérico.
   - Não: continuar.
5. **A compra está vinculada com segurança ao cliente?**
   - Não: pedir recibo/ID/e-mail de compra conforme o caso ou escalar.
   - Sim: continuar.
6. **Produto, variante e idioma estão identificados?**
   - Não: não adivinhar; revisar.
   - Sim: continuar.
7. **A rota é conhecida e foi testada?**
   - Sim: enviar somente a rota correta.
   - Não: localizar deliverable/abrir a página ou escalar.
8. **Já houve resposta anterior sobre o mesmo assunto?**
   - Sim: reconstruir o histórico e evitar resposta repetida; corrigir a instrução anterior se necessário.
   - Não: responder com o modelo correspondente.

## Classificação operacional

Use uma destas ações internas:

- `RESPONDER_EMAIL`
- `PEDIR_INFORMACAO`
- `REVISAR_HUMANO`
- `SEM_RESPOSTA_NECESSARIA`
- `DOCUMENTAL_FINANCEIRO`

Toda ação deve guardar motivo e evidência utilizada.

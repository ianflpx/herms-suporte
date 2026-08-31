# Checklists

## Antes de liberar acesso

- [ ] Última mensagem e resposta anterior foram lidas.
- [ ] Threads relacionadas do cliente foram pesquisadas.
- [ ] E-mail de suporte e e-mail de compra foram distinguidos.
- [ ] Compra aprovada foi encontrada no Snapp.
- [ ] Match de identidade é seguro.
- [ ] Produto e variante exatos foram identificados.
- [ ] Idioma foi confirmado.
- [ ] Rota app/direta/arquivo foi classificada.
- [ ] Link/deliverable foi testado e corresponde ao produto.
- [ ] Não há pedido de reembolso, chargeback, fraude ou produto errado pendente.
- [ ] Corpo está no idioma do cliente.
- [ ] Link de outro produto não aparece na resposta.

## Antes de enviar qualquer e-mail

- [ ] Destinatário é o cliente correto.
- [ ] Thread/assunto estão corretos.
- [ ] Texto é final, não placeholder/teste.
- [ ] Nenhuma promessa não autorizada.
- [ ] Não há credencial, ID ou dado interno desnecessário.
- [ ] Produto/link/idioma conferem.

## Depois de enviar

- [ ] Envio aparece no Gmail Sent para o destinatário exato.
- [ ] Thread e assunto conferem.
- [ ] Mensagem do cliente foi marcada como lida somente após sucesso, se aplicável.
- [ ] Caso foi registrado no Discord.
- [ ] Exceções e falhas foram reportadas.

## Antes de reembolso autorizado

- [ ] Autorização explícita existe para aquele cliente/caso.
- [ ] Status real da venda foi verificado.
- [ ] Não há chargeback aberto que possa causar reversão duplicada.
- [ ] Texto não afirma conclusão futura quando o status já é refunded.
- [ ] Caso está no escopo autorizado, sem ampliar para outros clientes.

## Antes de atualizar automação

- [ ] Cron/job atual foi inspecionado.
- [ ] Mudança foi feita sem credenciais no código.
- [ ] Dry-run foi executado.
- [ ] Casos de fatura, certificado, pré-venda e reembolso não viraram acesso automático.
- [ ] Integração Snapp foi testada.
- [ ] Gmail Sent foi conferido após qualquer envio.
- [ ] Discord recebeu o relatório/alerta.
- [ ] Job substituto está ativo e aponta para o ID estável correto.

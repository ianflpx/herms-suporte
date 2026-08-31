# Privacidade e segurança

## Nunca versionar

- senhas;
- tokens de GitHub, Discord, Gmail ou Snapp;
- cookies de navegador;
- códigos OAuth e URLs de callback;
- arquivos `.env` reais;
- exportação integral da caixa de e-mail;
- lista de clientes, e-mails ou dados de pagamento;
- screenshots de cartão, endereço, documento ou dados fiscais;
- IDs de pedidos em massa sem necessidade operacional.

## Minimização de dados

Guardar nas notas apenas o necessário para resolver o caso. Dados pessoais usados na execução devem ficar no sistema de suporte apropriado, com retenção limitada. O repositório deve conter políticas e exemplos, não histórico real de clientes.

## Logs

Logs devem registrar ação, categoria, timestamp, resultado e motivo. Mascarar e-mails quando possível e nunca registrar tokens, corpo completo de cartão ou credenciais.

## Respostas

- confirmar somente o produto/dado necessário;
- não expor IDs internos ao cliente sem necessidade;
- não enviar links de produtos não comprados;
- não reutilizar texto citado que possa conter e-mail de outro cliente;
- revisar destinatário, assunto e corpo antes de cada envio.

## GitHub

- manter o repositório privado enquanto a necessidade de compartilhamento não estiver clara;
- usar branch/PR para mudanças relevantes;
- revisar diff antes de publicar;
- ativar secret scanning e dependabot quando disponíveis;
- não colocar credenciais em issues, commits ou arquivos de configuração.

## Incidente

Se o bot enviar link errado, texto de teste ou mensagem ao destinatário errado:

1. parar o lote;
2. corrigir o cliente afetado com mensagem curta no idioma correto, se apropriado;
3. registrar o incidente no Discord;
4. revisar a causa e a regra antes de retomar;
5. não esconder o erro no relatório.

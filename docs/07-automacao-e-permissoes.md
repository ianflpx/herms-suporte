# Automação e permissões necessárias

## Princípio

Conceder o menor acesso capaz de executar o fluxo. Credenciais devem ficar em secret manager/variáveis de ambiente, nunca no GitHub.

## Gmail / caixa de suporte

O bot precisa, conforme o modo configurado:

- leitura de mensagens e threads;
- pesquisa por remetente, destinatário, assunto e conteúdo;
- leitura do histórico completo de threads relacionadas;
- acesso a mensagens enviadas;
- envio de respostas (somente se o modo de envio estiver autorizado);
- marcar mensagens como lidas após ação bem-sucedida;
- identificação de bounces e mensagens automáticas.

Para auditoria somente leitura, não conceder envio. Para automação ativa, a conta deve ser exclusivamente a caixa de suporte e o escopo de envio deve ser revisado.

## Snapp Checkout / Snapp MCP

Preferência: MCP autenticado por OAuth.

O bot precisa de:

- listar/pesquisar vendas;
- consultar status, produto, variante, idioma, valor, data e e-mail cadastrado;
- consultar deliverables/URLs quando disponíveis;
- consultar oferta e order bumps para auditorias de complementos.

Não armazenar senha, token Bearer, cookie, código OAuth ou URL de redirecionamento no repositório/logs. Se o MCP não estiver autenticado, o bot deve reportar o bloqueio e não adivinhar entitlement. Browser/CDP é fallback, não primeira opção.

## Discord

O bot precisa de permissão para enviar mensagens no canal operacional de alertas. Preferir destino por ID estável:

- alertas: `discord:1517268381441462415`;
- canal de conversa: obter/configurar o ID antes de usar como destino técnico.

Não é necessário permitir que o bot administre servidor, membros, cargos ou histórico geral para executar o fluxo básico.

## Browser de verificação

Opcional, somente para testar páginas de acesso e fallback do painel Snapp. Deve ser uma sessão autenticada separada, sem colocar cookies no GitHub. O bot não deve declarar que o produto está indisponível só porque uma página antiga ou arquivo específico falhou.

## Variáveis sugeridas

Ver [`config/support-config.example.yaml`](../config/support-config.example.yaml). Nomes de segredo sugeridos:

- `SUPPORT_GMAIL_CREDENTIALS` ou OAuth equivalente;
- `SNAPP_MCP_OAUTH_PROFILE`;
- `DISCORD_BOT_TOKEN` ou integração equivalente;
- `SUPPORT_DISCORD_TARGET_ID`;
- `SUPPORT_TIMEZONE`.

Os valores reais devem ser configurados no ambiente do Grokbot/Hermes, não neste repositório.

## Modos de operação

### Somente auditoria

Ler e classificar; não enviar e-mail, não marcar como lido, não alterar estado.

### Resposta assistida

Preparar resposta, mostrar ao responsável e enviar somente após aprovação.

### Automação segura

Responder apenas casos de baixo risco com compra/produto/idioma verificados; escalar sensíveis; registrar tudo no Discord; executar dry-run e checagem de Sent após alterações.

O modo padrão recomendado para iniciar o novo bot é **resposta assistida**.

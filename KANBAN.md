# Kanban — MercadoÁgil

Quadro inicial baseado na rubrica do projeto final. As tarefas estão em **Backlog** até o grupo combinar responsáveis e começar. Marquem `[x]` ao concluir e movam o cartão entre as seções.

## Como dividir entre 5 pessoas

Substituam os rótulos pelos nomes do grupo. Cada cartão tem um responsável principal; cartões de integração devem ser revisados por alguém de outra dupla.

- **Dupla A:** estrutura, modelos, schemas e cadastros.
- **Dupla B:** pedidos, estoque e regras financeiras.
- **Pessoa solo:** CLI, relatórios, documentação e apresentação, com apoio das duplas nas integrações.
- **Todos:** decisões de interface entre módulos, commits no repositório e apresentação.

O quadro reúne 38 tarefas. Combine responsáveis e prioridades com o squad antes de iniciar.

## A fazer agora

- [ ] **[Todos]** Criar repositório GitHub do squad, adicionar o professor e definir fluxo de branches/PRs.
- [ ] **[Todos]** Combinar contratos das classes e formato padrão de resposta `{ ok, dados, erros }`.
- [ ] **[Dupla A]** Inicializar Node.js com `type: module`, instalar Zod e configurar `.gitignore` para `node_modules` e `.env`.
- [ ] **[Dupla A]** Criar estrutura de pastas e classe Cliente.
- [ ] **[Dupla A]** Criar classes Vendedor e Produto e relacionar produto ao vendedor.
- [ ] **[Dupla A]** Criar schemas Zod para Cliente, Vendedor, Produto e Cupom, incluindo refinements de CPF, CNPJ e validade.
- [ ] **[Dupla A]** Implementar operações de cliente: cadastrar, listar, buscar por CPF/nome e excluir.
- [ ] **[Dupla A]** Implementar operações de vendedor: cadastrar, listar, buscar por CNPJ/nome e excluir.
- [ ] **[Dupla A]** Implementar operações de produto: cadastrar, listar, buscar por id/nome e excluir.
- [ ] **[Dupla A]** Criar classe CupomDesconto e operações para cadastrar, listar, buscar por código e excluir.
- [ ] **[Dupla B]** Criar classe Estoque com consulta, baixa e devolução de quantidades.
- [ ] **[Dupla B]** Criar classe Pedido com itens, cupons, status e restrição de edição quando não estiver aberto.
- [ ] **[Dupla B]** Implementar validação de cupons: validade atual, subtotal mínimo, máximo de dois, sem duplicatas e regra de cumulatividade.
- [ ] **[Dupla B]** Implementar ordem dos descontos (percentual, fixo, frete), teto de 30% do subtotal e proteção contra total negativo.
- [ ] **[Dupla B]** Implementar cálculo de frete por região e unidade, frete grátis a partir de R$ 300 após descontos e cupom de frete.
- [ ] **[Dupla B]** Implementar tributos informativos por categoria sobre itens antes dos descontos.
- [ ] **[Dupla B]** Implementar comissão por categoria e repasse por vendedor sobre itens antes dos descontos.
- [ ] **[Dupla B]** Implementar confirmação atômica: verificar todos os itens antes de baixar estoque e listar todas as faltas.
- [ ] **[Dupla B]** Implementar cancelamento: devolver estoque apenas se pedido confirmado.
- [ ] **[Pessoa solo]** Implementar classe Marketplace para coordenar cadastros, pedidos e relatórios; manter regras fora do menu.
- [ ] **[Pessoa solo]** Implementar resumo do pedido e respostas seguras sem CPF (`{ cpf, ...clienteSeguro }`).
- [ ] **[Pessoa solo]** Criar `seed.js` com pelo menos 3 clientes, 3 vendedores, 8 produtos de 3 categorias e 3 cupons futuros.
- [ ] **[Pessoa solo]** Implementar relatórios apenas de pedidos confirmados: faturamento, quantidade, ticket médio, categorias, repasses e top 3 produtos.
- [ ] **[Pessoa solo]** Criar CLI interativa que só lê entradas, chama Marketplace e exibe as respostas.
- [ ] **[Todos]** Integrar módulos e conferir o exemplo do PDF: subtotal R$ 200, descontos R$ 35, frete R$ 28, total R$ 193, tributos R$ 14,40 e comissão R$ 21,60.
- [ ] **[Todos]** Escrever README com instalação, execução, estrutura, regras, decisões do squad e contribuições.
- [ ] **[Todos]** Preparar apresentação: problema, solução, estrutura/decisões e demonstração completa; todos participam.
- [ ] **[Todos]** Publicar apresentação do projeto no LinkedIn e registrar o link.
- [ ] **[Todos]** Conferir entrega: repositório acessível ao professor e prazo de 28/10/2026.

## Em andamento

_Mova cartões para cá quando alguém começar._

## Revisão / integração

_Mova cartões para cá quando estiverem implementados e aguardando revisão de outra pessoa._

## Feito

_Mova cartões para cá após revisar e integrar no branch principal._

## Outras tarefas

- [ ] **[Pessoa solo]** Adicionar filtros aos relatórios por período, vendedor ou cliente (sugerido na rubrica).
- [ ] **[Pessoa solo]** Gerar resumo em linguagem natural dos relatórios por API de IA (sugerido na rubrica; requer chave em `.env`).
- [ ] **[Todos]** Gravar vídeo ou GIF curto para acompanhar o post no LinkedIn (sugerido na rubrica).
- [ ] **[Dupla A]** Adicionar busca e ordenação de produtos por nome, categoria e preço.
- [ ] **[Dupla A]** Mostrar histórico de pedidos por cliente, com status e resumo.
- [ ] **[Dupla B]** Criar alerta/relatório de produtos com estoque baixo.
- [ ] **[Pessoa solo]** Exportar relatórios financeiros para CSV.
- [ ] **[Todos]** Adicionar testes automatizados para cupons, estoque e cálculos do pedido.
- [ ] **[Dupla B]** Persistir e carregar dados em JSON para manter alterações após encerrar o programa.

## Critérios para mover um cartão para Feito

1. O código está integrado no branch principal e a tarefa foi demonstrada no terminal.
2. O fluxo de erro retorna a resposta do serviço sem encerrar o programa.
3. O responsável explicou a solução a pelo menos uma pessoa do squad.


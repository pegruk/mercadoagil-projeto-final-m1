# Kanban — MercadoÁgil

Quadro inicial baseado na rubrica do projeto final. As tarefas estão em **Backlog** até o grupo combinar responsáveis e começar. Marquem `[x]` ao concluir e movam o cartão entre as seções.

## Como dividir entre 5 pessoas

Substituam os rótulos pelos nomes do grupo. Cada cartão tem um responsável principal; cartões de integração devem ser revisados por alguém de outra dupla.

- **Dupla A:** estrutura, modelos, schemas e cadastros.
- **Dupla B:** pedidos, estoque e regras financeiras.
- **Pessoa solo:** CLI, relatórios, documentação e apresentação, com apoio das duplas nas integrações.
- **Todos:** decisões de interface entre módulos, commits no repositório e apresentação.

Estimativa: 29 tarefas obrigatórias e 9 extras opcionais. Se o prazo apertar, terminem primeiro todos os cartões obrigatórios.

## A fazer agora

- [ ] **[Obrigatório · Todos]** Criar repositório GitHub do squad, adicionar o professor e definir fluxo de branches/PRs.
- [ ] **[Obrigatório · Todos]** Combinar contratos das classes e formato padrão de resposta `{ ok, dados, erros }`.
- [ ] **[Obrigatório · Dupla A]** Inicializar Node.js com `type: module`, instalar Zod e configurar `.gitignore` para `node_modules` e `.env`.
- [ ] **[Obrigatório · Dupla A]** Criar estrutura de pastas e classe Cliente.
- [ ] **[Obrigatório · Dupla A]** Criar classes Vendedor e Produto e relacionar produto ao vendedor.
- [ ] **[Obrigatório · Dupla A]** Criar schemas Zod para Cliente, Vendedor, Produto e Cupom, incluindo refinements de CPF, CNPJ e validade.
- [ ] **[Obrigatório · Dupla A]** Implementar operações de cliente: cadastrar, listar, buscar por CPF/nome e excluir.
- [ ] **[Obrigatório · Dupla A]** Implementar operações de vendedor: cadastrar, listar, buscar por CNPJ/nome e excluir.
- [ ] **[Obrigatório · Dupla A]** Implementar operações de produto: cadastrar, listar, buscar por id/nome e excluir.
- [ ] **[Obrigatório · Dupla A]** Criar classe CupomDesconto e operações para cadastrar, listar, buscar por código e excluir.
- [ ] **[Obrigatório · Dupla B]** Criar classe Estoque com consulta, baixa e devolução de quantidades.
- [ ] **[Obrigatório · Dupla B]** Criar classe Pedido com itens, cupons, status e restrição de edição quando não estiver aberto.
- [ ] **[Obrigatório · Dupla B]** Implementar validação de cupons: validade atual, subtotal mínimo, máximo de dois, sem duplicatas e regra de cumulatividade.
- [ ] **[Obrigatório · Dupla B]** Implementar ordem dos descontos (percentual, fixo, frete), teto de 30% do subtotal e proteção contra total negativo.
- [ ] **[Obrigatório · Dupla B]** Implementar cálculo de frete por região e unidade, frete grátis a partir de R$ 300 após descontos e cupom de frete.
- [ ] **[Obrigatório · Dupla B]** Implementar tributos informativos por categoria sobre itens antes dos descontos.
- [ ] **[Obrigatório · Dupla B]** Implementar comissão por categoria e repasse por vendedor sobre itens antes dos descontos.
- [ ] **[Obrigatório · Dupla B]** Implementar confirmação atômica: verificar todos os itens antes de baixar estoque e listar todas as faltas.
- [ ] **[Obrigatório · Dupla B]** Implementar cancelamento: devolver estoque apenas se pedido confirmado.
- [ ] **[Obrigatório · Pessoa solo]** Implementar classe Marketplace para coordenar cadastros, pedidos e relatórios; manter regras fora do menu.
- [ ] **[Obrigatório · Pessoa solo]** Implementar resumo do pedido e respostas seguras sem CPF (`{ cpf, ...clienteSeguro }`).
- [ ] **[Obrigatório · Pessoa solo]** Criar `seed.js` com pelo menos 3 clientes, 3 vendedores, 8 produtos de 3 categorias e 3 cupons futuros.
- [ ] **[Obrigatório · Pessoa solo]** Implementar relatórios apenas de pedidos confirmados: faturamento, quantidade, ticket médio, categorias, repasses e top 3 produtos.
- [ ] **[Obrigatório · Pessoa solo]** Criar CLI interativa que só lê entradas, chama Marketplace e exibe as respostas.
- [ ] **[Obrigatório · Todos]** Integrar módulos e conferir o exemplo do PDF: subtotal R$ 200, descontos R$ 35, frete R$ 28, total R$ 193, tributos R$ 14,40 e comissão R$ 21,60.
- [ ] **[Obrigatório · Todos]** Escrever README com instalação, execução, estrutura, regras, decisões do squad e contribuições.
- [ ] **[Obrigatório · Todos]** Preparar apresentação: problema, solução, estrutura/decisões e demonstração completa; todos participam.
- [ ] **[Obrigatório · Todos]** Publicar apresentação do projeto no LinkedIn e registrar o link.
- [ ] **[Obrigatório · Todos]** Conferir entrega: repositório acessível ao professor e prazo de 28/10/2026.

## Em andamento

_Mova cartões para cá quando alguém começar._

## Revisão / integração

_Mova cartões para cá quando estiverem implementados e aguardando revisão de outra pessoa._

## Feito

_Mova cartões para cá após revisar e integrar no branch principal._

## Extras — só puxar depois dos obrigatórios

- [ ] **[Extra · Pessoa solo]** Adicionar filtros aos relatórios por período, vendedor ou cliente (sugerido na rubrica).
- [ ] **[Extra · Pessoa solo]** Gerar resumo em linguagem natural dos relatórios por API de IA (sugerido na rubrica; requer chave em `.env`).
- [ ] **[Extra · Todos]** Gravar vídeo ou GIF curto para acompanhar o post no LinkedIn (sugerido na rubrica).
- [ ] **[Extra · Dupla A]** Adicionar busca e ordenação de produtos por nome, categoria e preço.
- [ ] **[Extra · Dupla A]** Mostrar histórico de pedidos por cliente, com status e resumo.
- [ ] **[Extra · Dupla B]** Criar alerta/relatório de produtos com estoque baixo.
- [ ] **[Extra · Pessoa solo]** Exportar relatórios financeiros para CSV.
- [ ] **[Extra · Todos]** Adicionar testes automatizados para cupons, estoque e cálculos do pedido.
- [ ] **[Extra · Dupla B]** Persistir e carregar dados em JSON para manter alterações após encerrar o programa.

## Critérios para mover um cartão para Feito

1. O código está integrado no branch principal e a tarefa foi demonstrada no terminal.
2. O fluxo de erro retorna a resposta do serviço sem encerrar o programa.
3. O responsável explicou a solução a pelo menos uma pessoa do squad.


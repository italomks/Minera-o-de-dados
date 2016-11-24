# Minera-o-de-dados

Exercício de Data Ming:

Criar uma tabela de Clientes

Criar uma Tabela de Vendas

Criar uma Tabela de Fornecedores

Criar uma Tabela de Categorias Produtos

Criar uma Tabela de Tipos de Produtos

Processo de Mineração

O aluno deverá cadastrar 10 clientes e cada cliente deve comprar 10 produtos e cada produto deve fazer parte de duas categorias sendo que a cada produto deve fazer parte de um tipo diferente de produto. A proposta e que cada aluno consiga minerar dentro dos cadastros padrões de compra realizados pelos clientes.

Ex. Meia – > Produto Masculino -> Esportiva ( 1 Produto de uma Categoria de um tipo).

Situação

O aluno deve fazer uma Query para minerar os dados das tabelas trazendo os dados de forma clara para que possamos analisar juntos os padrões de vendas encontrados dentro das 10 operações.

Observação.

Os alunos se não conseguirem devem procurar na internet os meios para executar da operação solicitada, pois, estaremos corrigindo em sala de aula. ESTA TAREFA É UMA TAREFA DE PESQUISA , PORTANTO , PODEM USAR O LABORATÓRIO E A INTERNET.

BANCO DE DADOS – PODEM USAR A FERRAMENTA QUE EU APRESENTEI COMO QUALQUER OUTRA.

QUERY – A SOLICITADA E UMA QUERY SIMPLES COM UM LEFT JOIN.

VOCÊ DEVE SALVAR A QUERY ESCRITA PARA QUE EU POSSA AVALIA-LA.


                              ---- SQL DA TABELA DE VENDAS----
SELECT v.id_venda, v.data_venda, v.quantidade_produto, c.nome, tp.produto,
f.fornecedor, cp.categoria, cp.sub_categoria
FROM mineracao.venda v
LEFT JOIN mineracao.cliente c
ON v.id_cliente = c.id_cliente
LEFT JOIN mineracao.tipo_produto tp
ON v.id_produto = tp.id_produto
LEFT JOIN mineracao.categoria_produto cp
ON tp.id_categoria = cp.id_categoria
LEFT JOIN mineracao.fornecedor f
ON tp.id_fornecedor = f.id_fornecedor;

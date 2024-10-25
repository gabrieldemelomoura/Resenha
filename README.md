# <span style="color: cyan;">RESENHA SOBRE OS SEMINÁRIOS</span>


### <span style="color: Aquamarine">Grupo 1: SUM, AVG, COUNT e MIN/MAX
Funcções agregadas manejam uma grande quantidade de dados, assim tornando a análise de dados mais simples. SUM= soma as colunas. AVG= Calcula médias. COUNT= conta o numero de registros de uma tabela e dados. Permitem a analise de vendas os acessos do cliente e a simplificação da manipulação de dados. MIN= menor valor em um conjunto de dados. MAX= maior valor em um conjunto de dados.

**exemplo**:

SELECT COUNT(*) FROM clientes;

SELECT AVG(preco) FROM produtos;

 
### <span style="color: Aquamarine">Grupo 2: INNER JOIN, LEFT JOIN, RIGHT JOIN, FULL OUTER JOIN
Combinam dados de duas ou mais tabelas com base em uma condição comuns que envolvem chaves primárias e estrangeiras e permite consulta-los. utiliza-se para normalizar dados, ajuda na consulta e torna as análises mais ricas em informações. INNER JOIN= determina como os registros serão combinados e apenas as que tiverem ligações serão juntados já os incompatíveis serão ignorados. LEFT JOIN= retorna todos os registros da tabela esquerda e os registros correspondentes da tabela a direita, caso não aja correspondência entre alguns dos resultados eles aparecerão como NULL. RIGHT JOIN= retorna todos os registros da tabela a direita e os registros correspondentes da tabela a esquerda, caso não aja correspondência entre alguns dos resultados eles aparecerão como NULL. FULL OUTER JOIN= combina os resultados do LEFT e do JOIN, retornando todos os registros de ambas as tabelas. E quando não houver correspondências eles aparecerão como NULL.

**exemplo**: 

SELECT a.nome, b.pedido

FROM clientes a

INNER JOIN pedidos b ON a.id = b.cliente_id;

 
### <span style="color: Aquamarine">Grupo 3: AND, OR, NOT, IN, NOT IN, LIKE, IS NULL AND=
Combina duas ou mais condições OR = combina duas ou mais condições NOT= inverte o valor IN= verifica se um valor está presente na lista NOT IN= verifica se um valor não esta presente na lista LIKE= usado em uma clausula WHERE para buscar um padrão de texto IS NULL= verifica se um valor de uma coluna é nulo

**exemlo**:

SELECT * FROM produtos WHERE preco > 100 AND estoque < 50;

 
### <span style="color: Aquamarine">Grupo 4: Subconsultas
Filtra os resultados com base nos critérios citados, realiza calculos, verifica a existencia do item em outras tabelas.

**exemplo**: 

SELECT nome FROM clientes WHERE id IN (SELECT cliente_id FROM pedidos WHERE total > 500);


 
### <span style="color: Aquamarine">Grupo 5: AGRUPAMENTO DE RESULTADOS E COMBINAÇÃO COM O HAVING GROUP
BY= agrupa linhas de uma tabela com base em valores comuns, permitindo cálculos e análises detalhadas utilizando funções de agregação. especifique os grupos, aplique a função de agregação e por fim utilize o GROUP BY

**exemplo**: 

SELECT nome FROM clientes WHERE id IN (SELECT cliente_id FROM pedidos WHERE total > 500);

 
### <span style="color: Aquamarine">Grupo 6: INDEXAÇÃO E PERFORMANCE
Ordena os seus dados de forma otimizada, HASHING utiliza a função HASH para mapear valores para uma posição específica permitindo buscas rápidas, INDICE UNICO= garante valores únicos em conjunto de colunas.
ÍNDICE COMPOSTO= utilizado em muitas colunas.
BITMAP= utilizado em colunas com poucos valores distintos.
FULL-TEXT INDEX= utilizado para buscas em colunas de texto completo.
tem menu de contexto

### <span style="color: Aquamarine">CONCLUSÃO:
Os seminários proporcionaram uma visão aprofundada sobre os conceitos essenciais para o desenvolvimento de bancos de dados, interligando teoria e prática. A compreensão de operadores de agregação, joins, subconsultas e outras técnicas não só melhora a capacidade de manipulação de dados, mas também é vital para garantir a eficiência e a integridade das operações em bancos de dados. Cada tema discutido é inter-relacionado, formando uma base sólida para um gerenciamento eficaz de dados.

# hypercloud
Arquivos requisitados para o processo seletivo referente à vaga de Assistente de Business Intelligence

# Respostas do Teste Técnico

## Questões Teóricas

### 1.	Pra você, o que significa Business Intelligence?

BI é, além de uma ciência, uma arte. Exige capacidade técnica e analítica de um time multidisciplinar. Seu objetivo é compreender o passado para subsidiar decisões sobre o futuro. Isso é feito através de processos de obtenção e tratamento de dados específicos, que tenham valor para agregar ao problema de negócio que se deseja resolver, que são posteriormente transformados e armazenados em bases apropriadas para possibilitar a criação dos mais diversos tipos de visualização para compreensão dos dados.
É portanto, uma maneira de transformar dados em informação.

### 2.	Cite duas ferramentas de ETL.

Duas das principais ferramentas de ETL do mercado são o Microsoft Integration Services (SSIS) e Informática Power Center.
Muito embora, seja possível realizar técnicas de ETL, em certo nível, com ferramentas como Transact-SQL, Power BI e através de linguagens de programação como R e Python.

### 3.	Cite três ferramentas de apresentação de dados.

Para apresentação de dados temos o Power BI da Microsoft, o Tableau da Salesforce e o QlikView / Qlik Sense da Qlik.

### 4.	O que é uma tabela Fato e o que é uma tabela Dimensão?

Tabelas Dimensão são tabelas que contém dados referentes a uma determinada perspectiva sob a qual se deseja analisar um conjunto de dados. Devem conter apenas registros únicos e uma coluna contendo uma chave, para que se possa definir um relacionamento a partir dela.
Já uma tabela Fato é uma tabela que armazena as chaves de cada uma das tabelas Dimensão com as quais se relaciona, e as colunas de Medidas, que são valores, geralmente numéricos, que poderão ser utilizados para realizar os mais diversos tipos de cálculos com base nos registros em si, e sua relação com determinadas Dimensões.

### 5.	Quais tipos de modelagens são mais utilizadas em um projeto de BI?

As modelagens mais comuns são o Star Schema, onde todas as tabelas Dimensão estão relacionadas a uma tabela Fato central, e o modelo Snow Flake Schema, onde há relacionamentos entre tabelas Dimensão, além dos relacionamentos entre tabelas Dimensão e Fato.

### 6.	O que significa “Surrogate Key”?

É uma “chave artificial” ou “chave substituta” criada no processo de modelagem das tabelas Dimensão em um Data Warehouse para ser usada como Chave Primária, e portanto, Chave Estrangeira em seus relacionamentos. É um valor numérico e auto incremental, criado no momento da carga dos dados originais nas tabelas Dimensão. 

### 7.	Explique a diferença entre os relacionamentos 1:1 e 1:N.

A cardinalidade define o número de elementos em um conjunto. Aplicada à modelagem de bancos de dados, define a quantidade de elementos de uma tabela que podem existir em uma outra tabela com a qual se relacione.
1:1 Significa que um elemento da tabela “A” só pode ocorrer uma única vez em “B”. Por exemplo, a relação entre [Pessoa] e [CPF].
1:N Significa que um elemento da tabela “A” pode ocorrer diversas vezes em “B”, enquanto os elementos que ocorrem em “B” só podem ocorrer uma única vez em “A”. Por exemplo, a relação entre [Cliente] e [Produtos_Venda].

### 8.	O que significa Drill Down / Drill Up?

São métodos de visualização de dados através da consolidação dos mesmos segundo uma regra hierárquica de nível de detalhamento. Drill Down se refere a passagem de um nível mais macro para um nível mais detalhado ou granular, enquanto Drill Up quer dizer exatamente o contrário.
Por exemplo, em um indicador de vendas, pode-se ter por padrão, a métrica Vendas por Dia. Uma operação de Drill Up permitiria a agregação desses dados em Vendas por Semana -> Vendas por Mês -> Vendas por Trimestre -> Vendas por Ano. Enquanto uma operação de Drill Down, permitiria o detalhamento desses dados em Vendas por Hora -> Vendas por Minuto.
Porém, as operações de Drill Down e Drill Up dependem da disponibilidade de tal nível de granularidade nas tabelas Fato e na Dimensão Tempo.

## Teste Prático

### 1.1	- Qual a modelagem projetada?

O modelo utilizado foi o Snow Flake Schema, uma vez que há relacionamentos entre tabelas Dimensão que não estão diretamente ligadas à tabela Fato.


# Bancos de Dados Relacionais (SQL) e Não Relacionais (NoSQL) 
Fonte: Leonardo Cestarolli :man_technologist:  Gerente de Arquitetura de Dados, Banco Carrefour
      ![image](https://user-images.githubusercontent.com/64448041/190862451-88d86fc9-d44a-458c-96b3-33048b723e55.png)
__
# Oque é SQL e NoSQL?
O papel dos Bancos de Dados Relacionais (SQL) e Não Relacionais (NoSQL) no contexto de um Engenheiro de Dados
__
# SGBD
Sistema de Gerenciamento de Banco de Dados armazenam informações em tabelas com linhas e colunas, como planilhas do Excel.

Cada linha é um registro, como dados de um cliente. Já as colunas descrevem atributos de cada cliente, como nome, endereço e cartão de crédito, por exemplo.

Bancos de Dados Relacionais
Um banco de dados relacional pode ter diversas tabelas, as quais se relacionam entre si. Podemos ter uma tabela “Compras”. Como cada compra é feita por um cliente, a tabela “Compras” se relacionará com a tabela “Clientes”, para sabermos qual compra foi feita por qual cliente.

São exemplos de SGBDs de dados relacionais: SQLite, MySQL, MariaDB, Microsoft SQL Server, PostgreSQL, Oracle, entre outros.
__
# SQL
![image](https://user-images.githubusercontent.com/64448041/190866166-9c7b9259-73e9-43d5-b9f5-7afdc891d2cb.png)

fonte:[w3school](https://w3cschoool.com/mysql-rename-table)

SQL é a sigla para Structured Query Language (“Linguagem de Consulta Estruturada”, em tradução livre). É a linguagem padrão para operações em bancos de dados relacionais. Por isso, tornou-se comum chamá-los de “bancos de dados SQL”.

Por meio de SQL, é possível criar (create), ler (read), alterar (update) e excluir (delete) dados — o famoso “CRUD” — em bancos relacionais.

# Bancos de dados NoSQL
Agora, NoSQL fica fácil! Bancos de dados desse tipo são softwares que armazenam dados de forma diferente dos bancos de dados relacionais.

Não usam tabelas, mas outros esquemas, que veremos a seguir. Também não adotam a linguagem SQL, mas linguagens próprias. Algumas, porém, são parecidas com SQL tanto na sintaxe quanto nos fundamentos.

Uma curiosidade: NoSQL não significa “não SQL”, mas “not only SQL” (“não somente SQL”, em tradução livre).

# Vantagens de NoSQL
NoSQL surgiu para lidar com big data, conjuntos de dados gigantescos e complexos surgidos com a web, após os anos 2000.

Como bancos relacionais podem ser ineficientes para grandes quantidades de dados, principalmente dados não estruturados — que não podem ser dispostos em linhas e colunas, como o conteúdo de textos, áudios e vídeos —, NoSQL surgiu como solução.
 
Isso não quer dizer que bancos de dados NoSQL sejam melhores que bancos SQL, apenas que se destinam a finalidades diferentes.

Tipos de bancos de dados NoSQL
Bancos de dados NoSQL podem ter os seguintes esquemas (formas de organizar os dados):

## 1. Documentos
![image](https://user-images.githubusercontent.com/64448041/190866244-ebad6b2a-812a-46c4-a079-0b1716d16e6e.png)

fonte:[Digital Ocean](https://www.digitalocean.com/community/conceptual_articles/an-introduction-to-document-oriented-databases)

Neste esquema, os dados são armazenados em “textos”. Por exemplo, dados de clientes estarão organizados de forma sequencial, como uma folha de formulário.

Tais textos podem ser altamente estruturados (ter campos bem definidos e comuns a todos os documentos, como CPF e nome de cada cliente) ou podem ser semiestruturados ou não estruturados (quando não há padronização dos campos).

MongoDB, Elasticsearch e CouchDB são exemplos populares de bancos NoSQL baseados em documentos.

## 2. Chave-valor
![image](https://user-images.githubusercontent.com/64448041/190866298-47f3d3d3-c31c-45d5-bd4a-aa840f96387b.png)

fonte:[dev.to](https://dev.to/aws-builders/intro-to-4-types-of-nosql-databases-45nh)

Bancos NoSQL do tipo chave-valor são como “dicionários”. Eles permitem cadastrar uma chave (um registro único e inconfundível) e associar quaisquer valores (informações) a essas chaves.

Isso permite muita flexibilidade e rapidez nas consultas. Podemos associar muitos campos de dados diferentes a uma única chave, bastando acessar tal chave para recuperá-los.

Redis, Apache Ignite e Memcached são exemplos populares de bancos NoSQL que usam o esquema chave-valor.

## 3. Grafo
![image](https://user-images.githubusercontent.com/64448041/190866322-80cf9d08-a80c-4fff-92cb-89d237d158ad.png)

fonte:[aws.amazon](https://docs.aws.amazon.com/pt_br/neptune/latest/userguide/graph-get-started.html)

Um grafo é uma coleção de nós ligados por arestas. Em bancos de dados do tipo, os dados são os nós e os relacionamentos entre eles, as arestas. Neles, podemos relacionar facilmente clientes aos produtos que mais compram, por exemplo.

Tanto que são muito usados para mecanismos de recomendação (indicar um produto que o cliente pode gostar, com base em suas preferências) e para detecção de fraude (comparar se o número de cartão de crédito usado por ele é sempre o mesmo).

São exemplos populares de bancos NoSQL baseados em grafos: Neo4J, OrientDB, AllegroGraph, entre outros.

## 4. Colunas
![image](https://user-images.githubusercontent.com/64448041/190866391-e19ba852-1a73-4850-a326-33baca52d1d0.png)

fonte:[scylladb](https://www.scylladb.com/glossary/wide-column-database/)

Questões técnicas são os maiores trunfos de bancos de dados NoSQL baseados em colunas. Eles reduzem a necessidade de leitura em disco durante consultas aos dados e utilizam menos memória para exibir as informações.

São usados principalmente em aplicativos analíticos, que precisam realizar muito cálculos com extrema rapidez, e em data warehouses (“armazéns de dados”), grandes repositórios de dados usados por empresas.

Amazon DynamoDB, Bigtable, Cassandra, Hbase, Google Cloud Datastore, entre outros, são exemplos populares de bancos NoSQL colunares.

## Como usar bancos de dados NoSQL?

Cada software de banco de dados NoSQL tem suas características. Por isso, é necessário conhecer aquele que melhor se adequa às suas necessidades ou às de sua empresa para aprofundar-se neles.

O interessante é que muitos já possuem ótima documentação e permitem usar a linguagem de programação de sua preferência para operá-los.

MongoDB, um banco NoSQL baseado em documentos, por exemplo, é muito utilizado por startups, por meio da linguagem Javascript e da tecnologia Node.js, para publicar sites e sistemas web escaláveis rapidamente. No curso de Programação Back-End da Awari, você tem uma introdução ao assunto.

Já bancos de dados colunares, como Hbase, Cassandra e DynamoDB, são comuns no dia a dia da Engenharia de Dados ou até, em alguns casos, na etapa de obtenção de dados da Ciência de Dados.

fonte:[awari](https://awari.com.br/banco-de-dados-nao-relacional/?utm_source=blog)

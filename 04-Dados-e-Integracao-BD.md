1. MANIPULAÇÃO DE DADOS (GERAL)
Operações Essenciais: O objetivo principal da API é realizar operações CRUD (Create, Read, Update, Delete) nos dados do banco.

A API (Node/Express) funciona como intermediário entre o cliente (App) e o Banco de Dados.

Drivers/Mappers: O Node.js usa bibliotecas (drivers) ou ORMs/ODMs para traduzir comandos JavaScript para o banco e vice-versa.

2. BANCO RELACIONAL (SQL - MySQL)
Estrutura: Dados organizados em tabelas com colunas e linhas rígidas.

Vantagem: Garante a integridade e consistência dos dados (ótimo para informações críticas ou relacionamentos claros, como a lista de amigos do seu app).

Comunicação: O Node.js precisa de um driver (ex: mysql2) para enviar consultas SQL (SELECT, INSERT, UPDATE).

Organização: A lógica de conexão (credenciais) e as consultas SQL devem ser separadas do código das rotas (controllers) para manter o projeto limpo.

3. BANCO NÃO-RELACIONAL (NoSQL - MongoDB)
Estrutura: Dados organizados em documentos (JSON/BSON) flexíveis, sem tabelas rígidas.

Vantagem: Alta flexibilidade e escalabilidade horizontal (ótimo para lidar com grandes volumes de dados que mudam rápido, como posts ou logs de atividade).

Mongoose: É o ODM (Object Document Mapper) mais usado em Node.js para trabalhar com MongoDB. Ele ajuda a estruturar os documentos do banco usando Schemas no JavaScript.

CRUD: As operações são feitas em coleções (o equivalente a tabelas) e são orientadas a objetos.

4. ESTRUTURA DO PROJETO COM DADOS
O código do Módulo 4 mostra como as rotas (que recebem o pedido do cliente) chamam a camada de Serviço/Controller, que então se comunica com a camada de Dados (o driver ou ORM/ODM) para acessar o Banco de Dados.

O teste final garante que essa cadeia de comunicação esteja funcionando, do cliente ao banco e vice-versa.

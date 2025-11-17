DESENVOLVIMENTO DE APIs COM EXPRESS.JS

1. INTRODUÇÃO E O QUE É EXPRESS
- **Express.js** é o framework mais popular para Node.js, usado para simplificar a criação de servidores e APIs RESTful.
- Por que usar? Facilita a criação de **Rotas** e o manuseio de requisições HTTP, sendo mais limpo que o módulo nativo do Node.
- Instalação: Feita via NPM (ex: npm install express).
- O Servidor é inicializado com: app.listen(PORT, ...).

2. COMPONENTES ESSENCIAIS
- **Rotas:** São os endereços da sua API (ex: /usuarios). O Express usa o objeto app para definir as rotas e os verbos HTTP (GET, POST, etc.).
- **Manipuladores (Handlers):** São as funções que respondem à requisição, sempre recebendo: **req** (Requisição) e **res** (Resposta).
- **Middleware:** É uma função que fica entre a requisição e a resposta final.
- Função do **Middleware**: Usado para logar, validar autenticação (verificar o login) ou modificar dados antes que cheguem ao manipulador final.
- O Middleware usa a função next() para passar a requisição adiante.

3. MANIPULAÇÃO DE DADOS DINÂMICOS
- **Parâmetros de Rota:**
    - Usados para identificar um recurso específico na URL (ex: /usuarios/:id).
    - Você acessa os dados com: **req.params**.
- **Query Strings:**
    - Usados para filtros, ordenação ou opções (ex: /produtos?status=ativo).
    - Você acessa os dados com: **req.query**.

O que aprendemos: O Express é a ferramenta que usaremos para construir o Back-end do nosso App de Amizades.

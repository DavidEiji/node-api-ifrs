O Módulo 5 mostra como o Express e o Middleware atuam juntos para proteger as rotas da API (ex: app.get('/matches', authMiddleware, ...)).

1. CONCEITOS DE SEGURANÇA (5.1)
Autenticação: É o processo de validar a identidade do usuário (Quem é você?). Geralmente feito com login e senha.

Autorização: É o processo de controlar o acesso aos recursos após a autenticação (O que você pode fazer?).

Princípio: Você Autentica uma vez (no login) e o sistema te Autoriza em todas as requisições seguintes.

2. JSON WEB TOKEN (JWT) (5.2)
O que é JWT? É um padrão compacto e seguro para transmitir informações de forma autônoma (stateless) entre a API e o cliente.

Estrutura: O Token é um objeto JSON que contém informações sobre o usuário (o payload). Ele é assinado digitalmente pelo servidor.

Vantagem: O servidor não precisa armazenar o estado do login (é stateless), o que torna a API mais escalável e rápida.

3. IMPLEMENTAÇÃO E USO DE JWT (5.3)
Criação do Token: Após o login ser bem-sucedido, o servidor cria um JWT e o envia para o cliente (App).

Uso: O cliente armazena o Token e o envia em todas as requisições subsequentes (geralmente no cabeçalho Authorization: Bearer <Token>).

Validação: A API intercepta a requisição usando um Middleware (do Express) para validar a assinatura do Token.

Se o Token for válido, o usuário está autenticado e o acesso é autorizado.

Se for inválido, a requisição é bloqueada (Status 401: Não autorizado).

4. ORGANIZAÇÃO DO PROJETO SEGURO
Estrutura: O código de criação/validação do JWT deve ser encapsulado em funções (como um Serviço de Autenticação).

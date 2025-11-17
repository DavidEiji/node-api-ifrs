APIs RESTful - CONEXÃO ENTRE SISTEMAS

1. O QUE SÃO APIS? (2.1)
- **API (Application Programming Interface):** É um conjunto de regras que permite que diferentes programas de software se comuniquem entre si.
- **RESTful:** É um **estilo** (conjunto de princípios) para construir APIs na Web, usando o protocolo **HTTP**.

2. PROTOCOLO HTTP (2.2)
- **HTTP (HyperText Transfer Protocol):** É a língua que a internet usa para a comunicação entre sistemas.
- **Modelo Cliente-Servidor (2.2.1):** O cliente (seu app React Native) faz a Requisição, e o servidor (seu Node.js) processa e envia a Resposta.

3. REQUISIÇÕES E RESPOSTAS (2.2.2)
- **Requisição (Request):** Contém o método (a ação) e o endereço (a URL).
- **Métodos (Verbos HTTP Essenciais):**
    - **GET:** Usado para **buscar** (ler) dados.
    - **POST:** Usado para **criar** um novo recurso.
    - **PUT/PATCH:** Usado para **atualizar** dados.
    - **DELETE:** Usado para **remover** dados.
- **Resposta (Response):** Contém o **Status Code** (o resultado da operação) e os dados.
    - Status 200: Sucesso (OK).
    - Status 404: Não encontrado.
    - Status 500: Erro no Servidor.

4. SERVIDOR HTTP COM NODE.JS (2.3)
- No Node.js, você usa módulos internos (`require('http')`) ou bibliotecas como o Express para criar o **Servidor** que escuta e responde aos pedidos do Cliente.
- O Servidor é o responsável por definir as **Rotas** (ex: `/usuarios`) que respondem a cada Verbo HTTP.

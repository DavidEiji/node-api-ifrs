MÓDULO 1.1 - HISTÓRICO E CONCEITO CENTRAL DO NODE.JS

Objetivo: Entender por que o Node.js é rápido e popular para Back-end.

* Criado em 2009 pelo Ryan Dahl.
* Ele estava frustrado com servidores antigos (tipo Apache) que eram muito lentos porque esperavam as coisas acontecerem.

CONCEITO CHAVE: I/O NÃO-BLOQUEANTE (Assincronicidade)

* **Bloqueante:** O servidor para e espera (bloqueia) até que uma tarefa lenta (ex: buscar um dado enorme no HD) termine.
* **Não-Bloqueante (Node.js):** O Node não espera. Ele manda a tarefa lenta para o lado e continua processando a próxima requisição. Quando a tarefa lenta terminar, ele volta para ela.
* Isso faz o Node ser **ideal para serviços com muita gente usando ao mesmo tempo**, tipo um chat ou o Back-end do nosso App de Amizades.
* O Node usa o **Motor V8** do Google Chrome para rodar o JS, o que garante a velocidade.

IMPORTANTE: Usamos a mesma linguagem (JavaScript) no celular (React Native) e no servidor (Node.js). Isso é a revolução Full-Stack.

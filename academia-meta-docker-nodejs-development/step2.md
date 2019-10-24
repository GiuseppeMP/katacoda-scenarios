# Criando aplicação exemplo - passo 1

Vamos evoluir nosso servidor HTTP e adicionar um framework para lidar com requisições REST.

## Adicionando ExpressJS

Para adicionar o express as dependências do projeto execute o comando abaixo:

`npm install express`{{execute T1}}

## Refatorando arquivo index.js

Altere o conteúdo do nosso arquivo _index.js_ conforme o snippet abaixo:

<pre class="file" data-filename="index.js" data-target="replace">
const app = require('express')();
app.get('/', function (req, res) {
  res.send('Hello World!');
});

app.listen(3000, function () {
  console.log('Academia Meta - Projeto Exemplo Running!');
});
</pre>

## Testando aplicação

`npm install && npm start`{{execute T1}}

4.Testando nossa aplicação:

`curl localhost:3000`{{execute T1}}

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

## Atualizando Scripts

Altere o conteúdo do nosso arquivo _package.json_, adicionando script de start, conforme o snippet abaixo:

<pre class="file" data-filename="package.json" data-target="replace">
{
  "name": "root",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start" : "node index.js"
  },
  "keywords": [],
  "author": "",
  "license": "ISC"
}
</pre>

## Testando aplicação

Instalando dependências:
`npm install`{{execute T1}}

Iniciando servidor:
`npm start`{{execute T1}}

Testando nossa aplicação:
`curl localhost:3000`{{execute T1}}

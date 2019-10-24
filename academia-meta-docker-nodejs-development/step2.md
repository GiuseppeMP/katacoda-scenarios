# Criando aplicação exemplo - step 2

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

## Atualizando scripts:start

Altere o conteúdo do nosso arquivo _package.json_, adicionando ao objeto script o atributo start:`"start" : "node index.js"`{{clipboard}}

<pre class="file" data-target="clipboard">
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start" : "node index.js"
  }
</pre>

## Testando aplicação

Instalando dependências:
`npm install`{{execute T1}}

Iniciando servidor:

`` npm start & APP_PID=`echo \$!` ``{{execute T1}}

Testando nossa aplicação:
`curl localhost:3000`{{execute T1}}

Desligando servidor:
`kill $APP_PID`{{execute T1}}

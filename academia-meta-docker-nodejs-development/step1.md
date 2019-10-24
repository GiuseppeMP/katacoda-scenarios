# Criando aplicação exemplo

1.Execute o comando de inicializar um module(project) nodejs usando npm, como abaixo:

`npm init --yes`{{execute T1}}

> --yes: Todas as opções default

2.Em seguida crie um arquivo no dir raiz chamado _index.js_ com conteúdo abaixo:

`touch index.js`{{execute T1}}

<pre class="file" data-filename="index.js" data-target="replace">
const http = require('http')

const handle = function(request, response) {
  response.writeHead(200)
  response.end('Academia Meta - Hello World!')
}

http.createServer(handle).listen(8080)
</pre>

3.Podemos iniciar a nossa aplicação exemplo utilizando o comando abaixo:

`npm start`{{execute T1}}

4.Testando nossa aplicação:

`curl localhost:8080`{{execute T1}}

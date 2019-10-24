# Criando aplicação exemplo

1.Execute o comando de inicializar um module(project) nodejs usando npm, como abaixo:

`shell npm init --yes`

> --yes: Todas as opções default

2.Em seguida crie um arquivo no dir raiz chamado _index.js_ com conteúdo abaixo:

```js
const http = require('http')

const handle = function(request, response) {
  response.writeHead(200)
  response.end('Academia Meta - Hello World!')
}

http.createServer(handle).listen(8080)
```

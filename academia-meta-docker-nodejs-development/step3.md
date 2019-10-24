# Criando aplicação exemplo - step 3

Agora que a camada de resources REST configurada, vamos adicionar alguns testes unitários. 😉 ;-) ;)

## Adicionando Jest

Para adicionar o jest as dependências de desenvolvimento do projeto execute o comando abaixo:

`npm install --save-dev jest`{{execute T1}}

Em seguida crie um arquivo de tests no dir raiz chamado _index.test.js_ `touch index.test.js`{{execute T1}} com conteúdo abaixo:

<pre class="file" data-filename="index.js" data-target="replace">

test('adds 1 + 2 to equal 3', () => {
  expect(1+2).toBe(3);
});

</pre>

## Atualizando scripts:test

Altere o conteúdo do nosso arquivo _package.json_, adicionando ao objeto script o atributo start:`"test" : "jest"`{{clipboard}}

<pre class="file" data-target="clipboard">
  "scripts": {
    "test": "jest",
    "start" : "node index.js"
  }
</pre>

## Rodando testes

`npm test`{{execute T1}}

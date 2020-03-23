# Usando Git

Vamos aprender os conceitos mais importantes sobre git, para isso você ja precisa ter ele instalado na sua maquina, algo facil de se achar na internet.

## Iniciando

Com o ***Git*** ja instalado:

1. Rodar `git init`
2. Rodar `yarn init -y`
3. Instalar express `yarn add express`
4. Para testar vamos criar um arquivo `index.js` com as seguintes configuracoes:

```
const express = require('express');

const app = express()

app.get('/', (req, res) => {
  return res.json({ message: "hello world"});
})

app.listen(3000);
```

5. criamos um arquivo `.gitignore` que serve para o git ignorar algum arquivo que a gente nao queira que vá para o versionamento por exemplo o `node_modules`:

`.gitignore`:

```
node_modules
```
somente colocando o nome do arquivo o git já ignora ele.


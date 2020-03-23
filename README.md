<img src="https://lucianoratamero.github.io/img/cover-git-1.png" width="200px"
align="center">

# Usando Git + Github

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

### Padronizaçāo de commits

`git commit -m "fix: ..."` - Arrumando erros
`git commit -m "feature: ..."` - Novas funcionalidades
`git commit -m "chore: ..."` - Nenhum dos casos acima

# Usando GitHub

Vá no seu perfil no Github e crie um repositorio, depois de criado siga essas instrucoes para adicionar seu projeto ao Github

1. `git init` na pasta do seu projeto
2. `git add .`
3. `git commit -m "<mensagem do commit>"` 
4. `git remote add origin https://github.com/<nomeDoSeuUsuarioNoGithub>/<nome-do-repositorio>.git`
5. `git push -u origin master`

Todos esses passos serāo fornecidos quando voce criar o repositório

Depois de rodar o ultimo passo todo seu codigo ja estar disponivel no seu repositório no ***Github***
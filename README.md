<h1 align="center">
  <img src="https://lucianoratamero.github.io/img/cover-git-1.png" width="300px">
  <h1 align="center">Usando Git & Github</h1>
</h1>


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

### Clonando um repositorio existente

`git clone <url do repositorio>`
***EX:*** `git clone https://github.com/peguimasid/Git-and-Github-Intro`

- `git log` mostra todos os commits
- `git push` manda as aleterações pro ***Github***

### Adicionar ramificaçāo para nova feature

Adicionamos uma nova ramificaçāo quando queremos salvar o codigo atual mas implementar uma nova feature, debugar o codigo, ou qualquer outro motivo que desejemos salvar o codigo atual.

- `git checkout -b <nome da feature>`
***EX:*** `git checkout -b feature/testando-ramificacao`

com isso o terminal deixara de ser assim:

`User in using-git-and-github on  master`

e ficará assim:

`User in using-git-and-github on  feature/testando-ramificacao`

ai com isso nosso master fica salvo e podemos voltar para ele a qualquer momento usando o comando: 

`git checkout master`

e de novo voltar para a feature usando o comando:

`git checkout feature/testando-ramificacao`

### Puxando dados da Feature pro Master

É bom manter na ideia que a Branch ***master*** é aquela que esta em producao.

Vamos supor que eu acabei de fazer a feature e agora eu quero puxar ela pro ***master***.

Podemos fazer assim:

1. Entro na feature. ***EX:*** `git checkout -b feature/testando-ramificacao`
2. Rodo: `git push origin feature/testando-ramificacao`

depois de fazermos isso, se formos no Github veremos uma mensagem assim:

<img src="./assets/pullrequets.png" width="700px">

3. Se clicarmos ***Compare & pull request*** nos iremos para uma pagina onde descreveremos o que fizemos, e outros desenvolvedores poderāo avaliar se o código esta bom ou nāo. Voce pode escolher os devs na aba `Reviewers`

4. Quando ele avaliar e clicar em `Merge pull request` nosso codigo da nova feature ira todo para o ***master*** online

5. e para trazermos para nossa maquina a nova feature é só rodar `git pull` e todo codigo que ta na branch ***master*** no github vira para o ***master*** do nosso computador
# Git e GitHub <h1>

## Introdução ao GIT e GITHUB <h2>

### O que é o GIT? <h3>

Sabe quando você precisava fazer trabalho em grupo e cada pessoa fazia uma parte? Então...

**O GIT é um programa que ajuda a fazer trabalhos em grupo, com todo mundo editando ao mesmo tempo, mas com controle do que cada um já fez.**

Dá para mexer no código inteiro lá no seu editor (VSCode, Sublime Text, etc) sem perder as edições anteriores! É o chamado **"Controle de Versões"**.


_Também pode ser usado nos seus trabalhos sozinha, tá?_

### O que é o GITHUB? <h3>

Pois é, Git e Github não são a mesma coisa! Git é o software que controla as versões do código que você está alterando. Já o **Github é um site onde publicamos todo esse controle de versões, e ainda adicionando comentários para cada mudança!**

### Como Funcionam Git e Github juntos? <h3>
_(abaixo temos apenas um resumão, essa parceria é um pouco mais que isso)_

1. A usuária habilita para o Git alguma pasta com seus arquivos de código.
2. Altera, apaga, escreve, muda tudo e, ao final, salva no seu editor normalmente.
3. Em seguida, a usuária "roda" essa pasta no GIT, dando um clique inverso na pasta.
4. Digita alguns comandos e, com eles, envia esse código alterado e atualizado para o Github.

## Criando um novo repositório <h2>

EDITAR: Passo a passo do GIT: se quiser colocar seus dados apenas numa pasta local, use isso na configuraçao inicial:
```js
local user.name // põe a propriedade do seu user.name apenas naquela pasta.
```


## Como dizer para o GIT ignorar determinado arquivo? <h2>

Pode acontecer de você criar uma pasta e desejar ocultar alguns arquivos dela. Como, por exemplo, ocultar o arquivo de respostas na pasta de exercícios que você está mandando para uma turma. É possível fazer isso com o seguinte passo a passo:

- Crie um arquivo chamado ".gitignore"
- Abre o arquivo e digita dentro dele os arquivos que você quer esconder (ou da pasta, sempre com uma barra. exemplo? */respostas*)
- *git <seu file gitignore>*, para que o GIT o reconheça, né? :D

## Glossário <h2>
- Working Tree: Árvore de Trabalho. É onde os arquivos estão sendo armazenados e editados.
- Index: O lugar entre sua *working tree* e seu repositório GIT.

## Comandos Importantes no Terminal (Comandos GIT ou não) <h2>

### Comandos de Criação e Apagamento <h3>

```js
rm <file> // Apaga o arquivo do seu computador.

git rm --cached <file> // Tira o arquivo do monitoramento GIT.
git init // Faz com que o GIT passe a enxergar aquela pasta.
git init --bare // Sinaliza que a pasta é apenas um servidor, um repositório matriz. É como se fosse seu link no GitHub.
git branch <titulodabranchnova> // Cria uma branch nova.
git checkout -b <titulodabranchnova> // Cria uma branch nova e já entra nela.
```

### Comandos de Orientação (onde você está? o que está acontecendo?) <h3>

Cada comando mostra o seguinte:
```js
pwd // todo o caminho da pasta em que você está.
ls // todos os arquivos daquela pasta.

git config --list // informações do repositório, incluindo autor e endereço.
```

#### Git Log (comandos para detalhar commits) <h4>

```js
git log // todos os commits.
git log --pretty="format %h %s" // apenas a hash e o título. Esse %h ou %s podem ser alterados para qualquer coisa que você quiser. No site https://devhints.io/git-log-format tem vários formatos.
git log --oneline // todos os commits em apenas uma linha.
git log --graph // é legal, mostra uma barrinha lateral gráfica com os commits da sua branch atual.
git log -p // mostra NO CONSOLE todas as alterações já feitas no VSCode.
```
### Comandos de Renomeio <h3>
```js
git remote rename nomeantigo nomenovo //muda o nome da origem. Sai "origin" e entra o nome que você quiser.
```
## Acabaram as alterações: Merge e Rebase <h2>
Master é onde colocamos o código que funciona, a versão "final".

## Links Úteis <h2>

https://git-school.github.io/visualizing-git/: ajuda a visualizar as branchs




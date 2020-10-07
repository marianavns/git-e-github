# Git e GitHub

# Sumário
○ [O que é o GIT](#O-que-é-o-GIT)

○ [O que é o GITHUB](#O-que-é-o-GITHUB)

○ [Como Git e Github funcionam juntos](#Como-Git-e-Github-funcionam-juntos)

○ [Criando um novo repositório](#Criando-um-novo-repositório)

○ [Como sinalizar arquivos que não devem ir para o Github](#Como-sinalizar-arquivos-que-não-devem-ir-para-o-Github)

○ [Comandos importantes no GitBash](#Comandos-importantes-no-Gitbash)</br>
° [Comandos de Criação e Apagamento](#Comandos-de-Criação-e-Apagamento)</br>
° [Comandos de Orientação](#Comandos-de-Orientação)</br>
[Git Log](#Git-Log)
° [Comandos para Renomear](#Comandos-para-Renomear)
° [Comandos para desfazer coisas]
° [Comandos para consolidar as alterações na Master]
[Merge e Rebase](#Merge-e-rebase)

[Resolvendo conflitos](#Resolvendo-conflitos)

[Glossário](#Glossário)


# O que é o GIT

Sabe quando você precisava fazer trabalho em grupo e cada pessoa fazia uma parte? Então... **O GIT é um programa que administra trabalhos em grupo ou sozinha, com várias edições acontecendo até ao mesmo tempo, mas com controle de cada mudança que foi feita.** Dá para mexer no código inteiro lá no seu editor (VSCode, Sublime Text, etc) sem perder as edições anteriores! É o chamado **"Controle de Versões"**.

Nos exemplos, o editor de código será o VSCode.

O Git possui um terminal, assim como o prompt de comando do Windows: o **Git Bash**.

# O que é o GITHUB

Pois é, Git e Github não são a mesma coisa! Git é o software que controla as versões do código que você está alterando. Já o **Github é um site onde publicamos todo esse controle de versões, visualizamos comentários para cada mudança e ainda dá para fazer muito mais por lá!**

# Como Git e Github funcionam juntos
Aqui é só o começo. A parceria Git e Github é muito mais que isso!

1. A usuária habilita alguma pasta com seus códigos para o Git.
2. Altera, apaga, escreve, muda tudo e salva no seu editor normalmente.
3. Em seguida, a usuária digita alguns comandos e, com eles, envia o código alterado e atualizado para o Github.
4. Pronto! Agora o código está disponível no Github.

# Criando um novo repositório

# Como sinalizar arquivos que não devem ir para o Github

Às vezes alguns arquivos não precisam necessariamente ir para o Github. Suponha que dentro do repositório haja uma pasta de imagens que já estão sendo exibidas no README. Essa pasta de imagens não precisa estar no Github também, né?

Para manter esta pasta no seu computador, mas não correr o risco dela ser enviada para o site, estes são os passos:

- Crie um arquivo chamado `.gitignore` na sua pasta no computador;
- Abra o arquivo `.gitignore` no VSCode;
- Digite os arquivos devem ser ignorados (ou a pasta, sempre com uma barra. exemplo: */Imagens*);
- Salve;
- Digite no GitBash `git add .gitignore` (para que o GIT o reconheça, né? :D).

# Comandos Importantes no GitBash
> Comandos GIT ou não

## Comandos de Criação e Apagamento

Comandos Gerais | Resultado
---- | ----
`rm file` | Apaga o arquivo do seu computador.

Comandos GIT | Resultado
---- | ----
`git init` | Inicia o GIT naquela pasta
`git rm --cached <file>` | Tira o arquivo do monitoramento GIT.
`git init --bare` | Sinaliza que a pasta é apenas um repositório matriz. *Como se fosse seu link no GitHub.*
`git branch <titulodabranchnova>` | Cria uma branch nova.
`git checkout -b <titulodabranchnova>` | Cria uma branch nova e já entra nela.

 STASH ¹ 📝 | TRABALHANDO COM RASCUNHOS! 📝
---- | ----
`git stash` | Cria um rascunho no limbo para guardar algo que não deve ser commitado ainda.** 
`git stash apply <numeroStash>` | O rascunho volta para sua head
`git stash drop <numeroStash>` | Remove o rascunho
`git stash pop <numeroStash>` | Faz as duas coisas ao mesmo tempo

¹ Para salvar aquele código que não funciona e você precisa, por exemplo, deixá-lo de lado para fazer uma nova tarefa.

## Comandos de Orientação

Localiza a usuária no trabalho, nas pastas, mostra o que já foi feito ou o que está pendente.

Comandos Gerais | Resultado
---- | ----
`pwd` | todo o caminho da pasta em que você está.
`ls` | todos os arquivos daquela pasta.

Comandos GIT | Resultado
---- | ----
`git config --list` | informações do repositório, incluindo autor e endereço.
`git tag` | Mostra todas as tags.


### Git Log

O `git log` é muito útil pois detalha todas as alterações que foram feitas através dos commits.

```js
git log // todos os commits.
git log --pretty="format %h %s" // apenas a hash e o título. 
//Esse %h ou %s podem ser alterados para qualquer coisa que você quiser. 
//No site https://devhints.io/git-log-format tem vários formatos.
git log --oneline // todos os commits em apenas uma linha.
git log --graph // é legal, mostra uma barrinha lateral gráfica com os commits da sua branch atual.
git log -p // mostra NO CONSOLE todas as alterações já feitas no VSCode.
git log --help // abre a página web de ajuda do gitlog.

git diff // A diferença entre o estado atual e o último commit.
git diff <commitAnterior> .. <commitAtual> // Mostra no terminal todas as alterações entre dois commits.
```

## Comandos para Renomear

```js
git remote rename nomeantigo nomenovo //muda o nome da origem. Sai "origin" e entra o nome que você quiser.
```

## Comandos para desfazer coisas

```js
/* Modifiquei o arquivo, mas não fiz nem o "git add". É mais fácil dar ctrl z no VSCode.*/ 
git checkout -- <nomedoarquivo>

/* Modifiquei o arquivo, dei git add, mas desisti de commitar */ 
git reset HEAD <nomedoarquivo>

/* Reverter o commit */ 
git revert <hashDoCommitQueQuerApagar> 

/* //// Quero voltar para um commit e começar tudo novo de lá */
git checkout -b <novo-branch> // É preciso criar um novo caminho para trilhar.
git checkout <hashDoCommitParaOndeVoltar>
```

## Comandos para consolidar as alterações na Master

### Merge e Rebase

Master é onde colocamos o código que funciona, a versão "final".

**Merge** é juntar a branch na master. Desse jeito, você **perde os commits feitos na branch que foi mergeada**, só fica com os commits da master. É igual mesclar no Excel, que só ficamos com o conteúdo da primeira célula.
```js
git merge <branchsecundaria>
```

**Rebase** também junta a branch na master, mas de forma diferente: você **mantem todos os commits da branch secundária** e o commit da master vai para frente.
```js
git rebase <branchsecundaria>
```

# Resolvendo conflitos
![Conflito](https://i.ibb.co/6NyQBMh/conflito.jpg) 


Se duas pessoas alteram a mesma parte do código e dão o push, acontecerá um conflito na hora de mergear. É necessário ir no editor de código e deletar a duplicidade que está acontecendo. O VSCode vai colorir o que está duplicado. É só escolher e apagar.

https://git-school.github.io/visualizing-git/: ajuda a visualizar as branchs.

https://devhints.io/git-log: "dev dicas" - dicas do git log.

# Como criar um marco no código
> , aquele ponto intermediário como nos estágios do Mário, uma *Release*!
```js
git tag -a <nomeParaSuaVersao> -m "Lançando a primeira versão (BETA)"
git push origin <nomeParaSuaVersao> // Enviando sua tag nova para o GitHub
```

Aí, no seu GitHub, sua tag vai ficar separadinha (uma release) e você pode baixar o código a partir daquele ponto!

# Glossário 

- HEAD: É UM **ESTADO**, o seu local de trabalho.
- Index: O lugar entre sua *working tree* e seu repositório GIT.
- Working Tree: Árvore de Trabalho. É onde os arquivos estão sendo armazenados e editados.




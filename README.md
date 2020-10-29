# Git e GitHub

# Sumário
1. [O que é o GIT](#O-que-é-o-GIT)

2. [O que é o GITHUB](#O-que-é-o-GITHUB)

3. [Como Git e Github funcionam juntos](#Como-Git-e-Github-funcionam-juntos)

4. [Mão na Massa](#Mão-na-Massa)

4.1 [Criando a primeira pasta e o primeiro arquivo](#Criando-a-primeira-pasta-e-o-primeiro-arquivo)

4.2 [Escondendo arquivos que não precisam ser acompanhados pelo Git](#Escondendo-arquivos-que-não-precisam-ser-acompanhados-pelo-Git)

5. [Comandos Importantes no Terminal](#Comandos-Importantes-no-Terminal)

5.1 [Para Você Trabalhar Melhor](#Para-Você-Trabalhar-Melhor)

5.2 [Para Criar ou Apagar Coisas](#Para-Criar-ou-Apagar-Coisas)

5.3 [Para Orientação e Navegação](#Para-Orientação-e-Navegação)

5.4 [Apenas para o Git](#Apenas-para-o-Git)

5.4.1 [Para criar ou apagar coisas no GIT](#Para-criar-ou-apagar-coisas-no-GIT)

5.4.2 [Para Usar Rascunhos Git Stash](#Para-Usar-Rascunhos-Git-Stash)

5.4.3 [Para Orientação e Navegação no GIT](#Para-Orientação-e-Navegação-no-GIT)

5.4.4 [Para renomear no Git](#Para-renomear-no-Git)

5.4.5 [Para desfazer coisas no Git](#Para-desfazer-coisas-no-Git)

5.4.6 [Para Consolidar as Alterações na Branch Master](#Para-Consolidar-as-Alterações-na-Branch-Master)

6. [Resolvendo Conflitos](#Resolvendo-Conflitos)

7. [Criando um Marco no Código](#Criando-um-Marco-no-Código)

8. [Glossário e Links Interessantes](#Glossário-e-Links-Interessantes)

<img src=https://i.imgur.com/DbYGB7m.gif alt="Ilustração. Mesa com dois notebooks e blocos de nota. Duas cadeiras nesta mesa estão ocupadas por um homem e uma mulher fazendo high five. Uma mulher de pé põe a mão no ombro do homem sentado. Um homem de pé põe a mão no ombro da mulher sentada. São um time de trabalho." width="330" height="330">  

# O que é o GIT 1

Sabe quando você precisava fazer trabalho em grupo e cada pessoa fazia uma parte? Então... **O GIT é um programa que administra trabalhos em grupo ou sozinha, com várias edições acontecendo até ao mesmo tempo, mas com controle de cada mudança que foi feita.** Dá para mexer no código inteiro lá no seu editor (VSCode, Sublime Text, etc) sem perder as edições anteriores! É o chamado **"Controle de Versões"**.

Nos exemplos, o editor de código será o VSCode.

O Git possui um terminal, assim como o prompt de comando do Windows: o **Git Bash**.

# O que é o GITHUB 2

Pois é, Git e Github não são a mesma coisa! Git é o software que controla as versões do código que você está alterando. Já o **Github é um site onde publicamos todo esse controle de versões, visualizamos comentários para cada mudança e ainda dá para fazer muito mais por lá!**

# Como Git e Github funcionam juntos 3
Aqui é só o começo. A parceria Git e Github é muito mais que isso!

1. A usuária habilita alguma pasta com seus códigos para o Git.
2. Altera, apaga, escreve, muda tudo e salva no seu editor normalmente.
3. Em seguida, a usuária digita alguns comandos e, com eles, envia o código alterado e atualizado para o Github.
4. Pronto! Agora o código está disponível no Github.

# Mão na Massa 4

## Criando a primeira pasta e o primeiro arquivo 4.1

## Escondendo arquivos que não precisam ser acompanhados pelo Git 4.2

Às vezes alguns arquivos não precisam necessariamente ser processados pelo Git e ir para o Github. Suponha que, dentro do repositório, haja uma pasta de imagens que já estão sendo exibidas no README. Essa pasta de imagens não precisa estar no Github também, né?

Para manter esta pasta no seu computador, mas não correr o risco dela ser enviada para o site, estes são os passos:

- Crie um arquivo chamado `.gitignore` na sua pasta no computador;
- Abra o arquivo `.gitignore` no VSCode;
- Digite os arquivos devem ser ignorados (ou a pasta, sempre com uma barra. exemplo: */Imagens*);
- Salve;
- Digite no GitBash `git add .gitignore` (para que o GIT o reconheça, né? :D).

# Comandos Importantes no Terminal 5

## Para Você Trabalhar Melhor 5.1
🐧 `clear` -> Limpa a tela do terminal.

🌐 `cls` -> *Clear screen*, limpa a tela do terminal.

🐧 🌐 `↑` -> Volta os últimos comandos digitados na linha de código.

## Para Criar ou Apagar Coisas 5.2

### Criando 5.2.1
🐧 🌐 `mkdir` -> Um diretório.

🐧 🌐 `echo > <novoarquivo>` -> Um arquivo.

### Deletando 5.2.2

🐧`rm -rf <nomedoarquivo_ou_pasta>` -> Qualquer coisa (*r* de *recursivo*: vai deletar tudo de uma pasta e *f* de *force*, não pedirá verificação de nada, apenas apaga na marra).

🌐`del <nomedapasta>` -> Tudo o que está dentro de uma pasta.

🌐`rmdir <nomedapasta>` -> Uma pasta e tudo o que tem dentro dela.

## Para Orientação e Navegação 5.3

🐧 🌐 `cd <caminho de uma pasta>` -> *Change Direction*, vai para uma pasta específica.
🐧 🌐 `cd..` -> Vai para um nível acima do diretório.

🐧 `ls`-> Lista os diretórios na sua pasta.
🐧 `pwd`-> Mostra todo o caminho da pasta em que você está.

🌐`dir`-> Lista os diretórios na sua pasta para Windows.
🌐`echo %cd%` -> Mostra todo o caminho da pasta em que você está.

## Apenas para o Git 5.4
:octocat:

### Para criar ou apagar coisas no GIT 5.4.1

#### Criando 5.4.1.1
`git init` -> o GIT na pasta.

`git branch <titulodabranchnova>` -> Uma branch nova.

`git checkout -b <titulodabranchnova>` -> Uma branch nova (e já entra nela).

`git stash` -> Um rascunho no limbo para guardar algo que não deve ser commitado ainda.

`git init --bare` -> Inicia o GIT Remote naquela pasta. *É como se esta pasta agora fosse seu repositório no GitHub.*

#### Apagando 5.4.1.2
`git rm --cached <file>` -> Retira o arquivo do monitoramento GIT.

### Para Usar Rascunhos Git Stash 5.4.2

É possível criar um rascunho no seu GIT caso você precise parar o que está fazendo e trocar de branch, mas não pode ainda commitar. É só criar um stash, que terá um número. Para ativar ou desativar este rascunho, digite:

`git stash apply <numeroStash>` -> O rascunho volta para sua head.

`git stash pop <numeroStash>` -> Joga o rascunho para sua head e deleta.

### Para Orientação e Navegação no GIT 5.4.3

`git status` -> O mais importante: Avisa quais documentos estão untracked, unmodified, modified e staging.

`git tag` -> Mostra todas as tags.

`git config --list` | informações do repositório, incluindo autor e endereço.

#### Detalhando Alterações com Git Diff 5.4.3.1

git diff // A diferença entre o estado atual e o último commit.

git diff <commitAnterior> .. <commitAtual> // Mostra no terminal todas as alterações entre dois commits.

#### Detalhando Commits com Git Log 5.4.3.2
É muito útil pois detalha todas as alterações que foram feitas através dos commits. Cada comando exibe o seguinte:

`git log` -> Todos os commits.

`git log --pretty="format %h %s"` -> Apenas a hash e o título do commit. 
    *Esse %h ou %s podem ser alterados para qualquer coisa que você quiser.*
    *No site https://devhints.io/git-log-format tem vários formatos.*

`git log --oneline` -> Todos os commits, cada um em apenas uma linha.

`git log --graph` -> Uma barra lateral gráfica com os commits da sua branch atual.

`git log -p` -> Exibe no console todas as alterações já feitas no VSCode.

`git log --help` -> abre a página web de ajuda do gitlog.

### Para renomear no Git 5.4.4

`git branch -m <nomeantigo> <nomenovo>` -> Renomeia a branch.

`git remote rename <nomeantigo> <nomenovo>` -> Renomeia a origem. Sai "origin" e entra o nome que você quiser.

### Para desfazer coisas no Git 5.4.5

`git reset HEAD <nomedoarquivo>` -> Modifiquei o arquivo, dei git add, mas desisti de commitar.

`git revert <hashDoCommitQueQuerApagar>` -> Desfazer commit. 

```js
git checkout -b <novo-branch> // É preciso criar um novo caminho para trilhar.
git checkout <hashDoCommitParaOndeVoltar>
```
-> Quero voltar para um commit e começar tudo novo de lá.

### Para Consolidar as Alterações na Branch Master 5.4.6

#### Merge e Rebase 5.4.6.1

Master é onde colocamos o código que funciona, a versão "final".

**Merge** é juntar a branch na master. Desse jeito, você **perde os commits feitos na branch que foi mergeada**, só fica com os commits da master. É igual mesclar no Excel, que só ficamos com o conteúdo da primeira célula.

`git merge <branchsecundaria>` -> Junta a branch secundária na master, deletando os commits feitos na branch.

**Rebase** também junta a branch na master, mas de forma diferente: você **mantem todos os commits da branch secundária** e o commit da master vai para frente.

`git rebase <branchsecundaria>` -> Junta a branch secundária na master mantendo os commits.

# Resolvendo conflitos 6

Se duas pessoas alteram a mesma parte do código e dão o push, acontecerá um conflito na hora de mergear. É necessário ir no editor de código e deletar a duplicidade que está acontecendo. O VSCode vai colorir o que está duplicado. É só escolher e apagar.

# Criando um Marco no Código 7

O marco será como um ponto intermediário no seu projeto, o final de uma versão, uma *Release*!

`git tag -a <nomeParaSuaVersao> -m "Lança a primeira versão (BETA) do projeto"` -> Cria a versão
`git push origin <nomeParaSuaVersao>` -> Envia sua tag nova (versão) para o GitHub

Aí, no seu GitHub, sua tag vai ficar separadinha (uma release) e você pode baixar o código a partir daquele ponto!

# Glossário e Links Interessantes 8

- HEAD: É UM **ESTADO**, o seu local de trabalho.
- Index: O lugar entre sua *working tree* e seu repositório GIT.
- Working Tree: Árvore de Trabalho. É onde os arquivos estão sendo armazenados e editados.

https://git-school.github.io/visualizing-git/: ajuda a visualizar as branchs.

https://devhints.io/git-log: "dev dicas" - dicas do git log.




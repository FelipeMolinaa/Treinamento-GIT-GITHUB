# Treinamento-GIT-GITHUB
**Este repositório é destinado para o aprendizado de GIT - GITHUB**


## Arquivos GIT

* `.git` - Documento onde é armazenado todos os commits e configurações. (Normalmente esta oculto)
* `.gitignore` - Documento que lista os arquivos que serão ignorados na hora de fazer o push.
* `readme.md` - Documento responsável por realizar a apresentação do repositório.

### Fazendo o primeiro Push

* `git status` - Verifica se existe algum arquivo que foi alterado ou adicionado.
* `git add * ou nomeDoArquivo` - Adiciona ou atualiza um ou mais arquivos.
* `git commit -m "mensagem"` - Adiciona uma mensagem a alteração e cria uma nova versão.
* `git remote add origin https://linkDoRepositorio` - Adiciona um repositorio GitHub ao projeto. ("Origin" é o apelido da url)
* `git push -u origin master` - Manda o projeto master para o repositório gitHub. ("master" é o nome da branch)



### Criando linhas no tempo - Branch

* `git branch nomeLinha` - Cria uma nova linha do tempo.
* `git branch` - Lista todas as linhas do tempo.
* `git checkout nomeLinha` - Vai para esta linha do tempo.
* `git checkout -b nomeLinha` - Cria e acessa a linha do tempo.
* `git merge nomeLinha` - Mescla a linha do tempo atual com a especificada.
* `git branch -d nomeLinha` - Remove a linha do tempo. 



**Para que serve???**

> O uso de linhas do tempo, ou **branchs** tem como função possibilitar o dev modificar o código principal, e fazer o seu versionamento, sem que o código principal seja alterado, assim as modificações são jogadas para um segunda linha do tempo, que futuramente, se concluído pode ser juntado com a **branch** principal, e caso essa alteração venha a ser descontinuada, ela pode ser apenas excluída, sem que haja qualquer problema com a **branch** principal

<img width="500" alt="React and Redux Logo" src="documents/esquemabranch.png" >



### Resolvendo conflitos

``git pull`` - Atualiza o projeto de acordo com o já existente no github

* **Conflito de merge:** Quando a aplicação puxada pelo GitHub e a aplicação na maquina conflitam, mais especificamente na linha de um código da aplicação. Para isso o git oferece ferramentas textuais que facilitarão remover esse conflito manualmente



**Como eu posso utilizar**

> Muito eficiente quando existe mais de um usuário utilizando o mesmo repositório, o `git pull` tem como função atualizar o projeto de um usuário antes do mesmo fazer o push, já que pode acabar sobrescrevendo as alterações que um outro dev fez no repositório. 
>
> Exemplificando, um dev Back-end e outro Front-end, podem trabalhar juntos e sem se comunicarem; quando o desenvolvedor back-end fizer uma alteração pode fazer o `git pull` e adquirir todas as alterações que o desenvolvedor front-end fez, assim conseguindo fazer o `git push` sem conflitos




## Principais comandos
* `git init` - Inicia o git no documento atual.
* `git add * ou nomeDoArquivo` - Adiciona ou atualiza um ou mais arquivos.
* `git commit -m "mensagem"` - Adiciona uma mensagem a alteração e cria uma nova versão.
* `git log` - Lista todos os commits feitos.
* `git show` - Verifica as ultimas alterações nos arquivos.
* `git branch nomeLinha` - Cria uma nova linha do tempo.
* `git branch` - Lista todas as linhas do tempo.
* `git checkout nomeLinha` - Vai para esta linha do tempo.
* `git checkout -b nomeLinha` - Cria e acessa a linha do tempo.
* `git merge nomeLinha` - Mescla a linha do tempo atual com a especificada.
* `git branch -d nomeLinha` - Remove a linha do tempo.
* `git remote add origin https://linkDoRepositorio` - Adiciona um repositorio GitHub ao projeto. ("Origin" é o apelido da url)
* `git push -u origin master` - Manda o projeto master para o repositório gitHub. ("master" é o nome da branch)
* `git clone http://linkClone` - Clona um projeto do github.
* ``git pull`` - Atualiza o projeto de acordo com o já existente no github.

## Por dentro do GIT

**Como funciona os arquivos do GIT**

<img width="500" alt="React and Redux Logo" src="documents/esquema.png" >

* **blob** - Amarelo: Arquivos do seu projeto.
  * Possui o conteúdo do arquivo e o seu **sha1.**
* **tree** - Azul: uma "array" com todos os **blobs**.
  * armazena de cada **blob**, seu **sha1** e nome do arquivo e o seu próprio **sha1.**
* **commit** - Branco: Criado após fazer o **commit**, Armazena a **tree** com os **blobs**.
  * Armazena o **sha1** da **tree**, o autor do repositório e quem fez o **commit**.
  * Também possui um **sha1**.

* **sha1**: Esquema de criptografia, que é gerado de acordo com o conteúdo do arquivo criptografado.
  * Independente do arquivo, possui 40 caracteres.
  * Mesmo se o arquivo não for modificado, a criptografia vai ser diferente da anterior.



**Ciclo de vida dos arquivos no GIT**

<img width="500" alt="React and Redux Logo" src="documents/esquemacommit.png" >
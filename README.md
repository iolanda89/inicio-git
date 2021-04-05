# inicio-git
Lista de cursos para controlar no GIT - TEste

# Conceitos e Funcionalidades

•	Guia: https://git-scm.com/book/pt-br/v2/Fundamentos-de-Git-Gravando-Altera%C3%A7%C3%B5es-em-Seu-Reposit%C3%B3rio

•	Comandos: https://devhints.io/git-log

•	Objetivos de fazer source control:
  - Não perder o trabalho.
  - Trabalhar em equipe no mesmo ou vários arquivos.
  - Poder lançar um produto e poder continuar fazendo atualizações com segurança.

•	Controle de Versão (VCS – “Version Control System”): sistema que controla as versões. É o que o Git faz. Ele não é o único, tem CSV, SVN, Mercurial, etc. O Git permite que tenha um repositório na sua máquina e possibilita enviá-lo para outro repositório. O Git faz uma gestão de repositórios.

•	cd: comando que acha a pasta a ser controlada pelo git. Deve conter o caminho da pasta após “cd”. Geralmente funciona se as barras estiverem assim “/” e não assim “\”.

•	git init: comando que inicializa o respositório do Git.

•	git status: mostra o status do repositório, o que foi alterado ou não.

•	On branch master: o que está sendo rodado.

•	No commits yet: não possui nenhum commit.

•	Untraked files: arquivos não monitorados.

•	git add: colocado junto ao nome do arquivo para que seja possível o “commitar”., ou seja, para que seja monitorado. Se em vez do nome do arquivo colocarmos “.”, ele vai fazer isso com todos os arquivos da página. Quando fazemos uma alteração no arquivo, esse comando é que adiciona a modificação.
 
•	Repositório: é onde os arquivos são guardados. Pode ser uma pasta, um local na internet, etc.

•	git rm: comando para parar de monitorar o arquivo.

•	commit: salva uma alteração feita no arquivo/git. Ele precisa conter as alterações e também uma mensagem. O código deve estar sempre num estado funcional para commitar, ele nunca pode estar inacabado ou com problema.

•	git commit –m “”: quando já temos as alterações, esse comando informa uma mensagem (a que é necessária ao “comit”).A mensagem a ser inserida dentro de “” deve ser explicativa, porém não longa.

•	git config: comando para inserir cadastro no git. Se usarmos “--local" ele irá realizar o cadastro para aquele computador, se usarmos “--global” ele irá realizar o cadastro de forma global. Quando se abre um novo Git e quer que esse repositório seja atrelado a uma outra pessoa, basta realizar o “git config --local user.name (Nome da Pessoa)”, e todas as alterações aí feitas serão atreladas a ela.

•	Head: estado atual do nosso código, ou seja, onde o Git nos colocou.

•	Working tree: local onde os arquivos realmente estão sendo armazenados e editados.

•	index: local onde o Git armazena o que será commitado, ou seja, o local entre a working tree e o repositório Git em si.

•	Hash: é o código do commit. Exemplo: “657ddf4cbf02c3932b52dd176fde7b6ed4345789”.

•	git log --oneline: mostra os commits existentes.

•	git log -p: mostra as alterações que foram realizadas. Para sair desse comando, apertar a letra “q”.

•	git log --pretty=”format:%H”: mostra os hashs dos commits.

•	git log --pretty=”format:%h %s”: mostra parte das hash e suas respectivas mensagens.

•	git log --pretty=”format:%h %s %ae”: mostra parte das hash, suas respectivas mensagens e o e-mail do autor.

•	git log --help: mostra uma página da web com alguns exemplos de comandos e funcionalidades do “git log”.

•	.gitignore: esse é um arquivo que deve ser criado com esse nome específicamente em algum codificador (como o Visual Studio). Todas as linhas que estiverem nele serão lidos e ignorados pelo Git. No exemplo abaixo temos o arquivo “ide-config”, que é escrito dentro do “.gitignore” e que é portanto o arquivo que será ignorado:
 
  - Para que esse comando seja completo no Git, basta digitarmos o comando “git add .gitignore”, confome segue:
  - <img></img>
  
  - Da mesma forma que um arquivo, uma pasta também pode ser incluída dentro do “.gitignore” para ser ignorada. Basta ao escrever o nome dela nesse comando, acrescentar o “/” no final, assim (considerando que o nome da pasta seja “ide”):
 
•	clear: limpa o Git.

•	git init --bare: indica que o repositório é “puro”. Ou seja, é uma pasta que só contém as alterações realizadas, não são feitas modificações nela. Ela não contém uma cópia física dos arquivos, de forma que sejam acessíveis facilmente. O comandos erá executado na pasta em que o Git estiver no momento.

•	cd ..: volta no Git para a pasta superior. No caso da minha pasta “GiteGithub”, está dentro de “Documentos”. Então ele volta de “GiteGithub” para “Documentos”.

•	mkdir (nome da nova pasta): cria uma pasta.

•	cd ../(nome da pasta)/: (nome da pasta) deve ser substituído pelo nome da pasta. Esse comando chama/entra na pasta que se irá utilizar. Esse código não costuma funcionar.

•	fetch: buscar dados.

•	push: enviar dados.

•	git remote: comando que acessa um repositório remoto.

•	git remote add (nome a escolha) (endereço da pasta): comando que determina um repositório remoto. Após o “git remote add” podemos colocar um nome qualquer para denominar esse repositório remoto e em seguida é necessário inserir o nome da pasta aonde ele existirá.

•	git remote -v: exibe o endereço do repositório remoto.

•	git clone (endereço da pasta que se quer copiar) (nome da nova cópia da pasta): esse comando copia uma pasta. Após o “git clone”, informar o endereço da pasta que será copiada e em seguida o nome que se deseja dar à cópia dessa pasta. Importante lembrar que ela irá ser copiada no repositório em eu se está, que no nosso caso é “ana”, conforme abaixo (observar que a pasta que está sendo copiada é a “servidor”, e o nome que daremos à cópia da pasta é “projeto”:
 
Porém, a priori a pasta cópia está vazia, conforme é informado na imagem acima.

•	git push (nome do repositório remoto) (nome do ramo que será criado): esse comando obtém os dados do repositório remoto dentro de uma ramificação/branch (ou seja, envia as alterações). No caso, “master" é usado para denominar a ramificação principal, o “tronco”. Após “git push” é necessário informar o nome do repositório remoto (que no exemplo abaixo chamamos de local) e o nome do branch, que aqui no caso é “master”:
 
É sempre bom executar esse comando eventualmente no projeto para manter o repositório atualizado.

•	git remote rename (nome do respositório remote que se quer mudar o nome) (novo nome): o comando troca o nome de um repositório remoto. Após o “git remote rename” deve-se insrir o nome do repositório remoto que se quer alterar e em seguida o novo nome.

•	git pull (nome do repositório remoto e da ramificação que buscamos a informação): esse comando insere na pasta (traz as informações) em que estiver uma informação o comando que foi obtido através do “git push”. Após “git pull”, deve ser inserido o nome do repositório remoto e da ramificação que buscamos a informação e que será inserida na pasta em questão.

•	ls: verifica se um arquivo HTML está contido em uma pasta.

•	Passos para compartilhar informações/sincronização de pastas:

o	Inserir algum código numa pasta nova (chamei a pasta de “iolanda”).
o	No Git, digitar o comando “cd” + o endereço dessa pasta:
 
o	Iniciar a pasta com o comando “git init”:
 
o	Importante: para as pastas serem monitoradas e consideradas, é necessário as adicionar e commitar. Assim, devemos fazer isso com os arquivos constantes na pasta (no nosso casso, o “index.html”. Então, digitar “git add index.html” e depois “git commit –m “(mensagem explicando o commit)”:
 
o	Fase opcional – Pode ser feita alguma alteração no arquivo html. Nesse caso, é necessário após a alteração, ir no git, digitar “git add (nome do arquivo).html” e depois “git commit –m “(frase explicando a modificação)””. Pode-se também pedir que o Git ignore um arquivo html ou pasta. Nesse caso, é necessário criar um arquivo no Visual Studio, nomeá-lo de “.gitignore” e dentro dele inserir o nome do arquivo ou pasta que se quer ignorar:
  
Importante depois disso digitar no Git “git add .gitignore” e depois “git commit –m “(frase explicando)””.
o	Na pasta iolanda, inserir uma outra pasta nova com o nome que quiser (chamei de “servidor”) através do comando “mkdir” mais o nome da pasta nova (ficando mkdir servidor):
 
o	No Git, digitar o comando “cd” e o endereço da pasta servidor (o endereço tem que estar escrito dessa forma):
 
o	No Git, digitar o comando “git init --bare”. Isso vai tornar a pasta “servidor” a coordenadora de tudo:
 
o	Voltar para a pasta “iolanda” com o comando “cd ..”:
 
o	Criar uma pasta com o comando “mkdir”. Chamei a pasta nova de “pasta”, de forma que o comando ficou “mkdir pasta”:
 
o	Digitar o comando “git remote add (nome do repositório – criar um) (endereço do repositório – copiar o que apareceu quando digitamos o comando “git init --bare”). Chamamos o repositório “ local, então nosso comando ficou “git remote add local C:/Users/io_bi/OneDrive/Documentos/iolanda/servidor/”:
 
o	Para ter certeza que o repositório foi devidamente informado, digitar “git remote”, o qual deve mostrar o nome do nosso repositório (no caso, “local”) ou “git remote -v”, o qual deve mostrar o nome e endereço do nosso repositório, no caso “local C:/Users/io_bi/OneDrive/Documentos/iolanda/servidor/”:
 
o	No Git, digitar o comando “cd” e o endereço da pasta “pasta” (o endereço tem que estar escrito dessa forma):
 
o	Digitar o comando “git clone” com o endereço da pasta que se quer clonar (que no caso é a “servidor”) e o nome da nova pasta que conterá a cópia, a qual chamamos de “projeto”, ficando assim:
 
o	Voltar para a pasta “iolanda” com o comando “cd ..”:
 
o	Digitar o comando “git push local master” para extrair as informações do nosso repositório (“local”):
 
o	No Git, digitar o comando “cd” e o endereço da pasta “projeto” (o endereço tem que estar escrito dessa forma):
 
o	Digitar “git remote”:
 
o	Digitar “git remote rename origin local” (para substituir o nome do repositório), e depois “git remote” para conferir se a ação de renomear deu certo:
 
o	Digitar “git pull local master” para inserir na pasta as informações obtidas pelo “push”:
 
o	Digitar “ls”. Esse comando vai mostrar os arquivos HTML que agora constam na pasta.
o	Agora, qualquer alteração que for pelo Visual Studio no arquivo HTML que está dentro da pasta “projeto”, após devidamente salvo, poderá ser aplicado também no respectivo arquivo HTML da pasta “iolanda”.
o	Para isso, realizar uma alteração do arquivo “index.html” relativo à pasta “projetos” no Visual Studio e salvar.
o	No Git, ainda na pasta “projetos”, efetuar os comandos “git add index.html” e depois “git commit –m “(mensagem de alteração)””:
 
o	 No Git, ainda na pasta “projetos”, digitar o comando “git push local master”:
 
 
o	No Git, digitar o comando “cd ..” duas vezes para voltar à pasta “iolanda”:
 
o	No Git, agora na pasta “iolanda”, digitar o comando “git pull local master":
 
o	Digitando “git log –p” é possível verificar as alterações que foram realizadas:
 
o	Agora, no arquivo “index.html” da pasta “iolanda” visualizado através do Visual Studio, é possível verificar que a mesma atualização do arquivo correspondente na pasta “projeto” consta agora nesse arquivo também:
 
o	

•	GitHub: possibilita ter repositórios remotos públicos e privados gratuitos para armazenar e compartilhar o código dos nossos projetos.

•	-u: quando você  coloca “git push –u (nome) master”, toda vez que vc der um “git push” na “master" o programa vai entender que é dentro da pasta “(nome)”. No nosso caso (nome) é “origin”, conforme abaixo:
 
No lugar do nome, pode-se colocar o repositório específico. Nesse caso é necessário retirar o “-u”.

•	git branch: mostra as ramificações existentes. A principal é a “máster”.

•	git branch (nome da ramificação que se quer criar): o comando cria uma ramificação, que é chamada “branch”. Após o “git branch” é necessário informar o nome que se quer dar ao “branch”. Importante destacar que o nome do “branch” em que se está consta a direita do nosso endereço, em azul. Esse comando aqui descrito não muda o usuário para o novo “branch” criado, ele apenas o cria mesmo. No exemplo abaixo isso fica claro, pois após a criação do “branch” titulo, executamos o comando “git branch” para verificar as ramificações existentes, ficando claro que existe agora o “branch” “titulo” dentro do “master", e que continuamos no “master" (descrito em azul após nosso endereço):
 

•	git checkout (nome da ramificação que se quer acessar): esse comando acessa o “branch” desejado. Ele serve para se “navegar em estados dos repositórios”:
 

•	Visualizar ação do Git: no site https://git-school.github.io/visualizing-git/ é possível visualizar como os branchs se movimentam conforme são commitadas coisas neles.

•	git checkout -b (nome da ramificação que se quer criar): cria um branch e ao mesmo tempo já da acesso a ele (fusão do “git branch” com o “git checkout”). Após o “git checkout” é necessário informar o nome que se quer dar ao “branch”. No caso abaixo, chamamos o novo “branch” de “lista”:
 

•	Trabalhando separadamente: a sincronização de pastas descrita nos itens anteriores faz com que alterações feitas no “index.html” na pasta “ana” -> “projetos” afetem o arquivo “index.html” da pasta “GiteGitHub”. Porém, destaca-se que até esse momento, ambas as pastas e alterações estão no branch principal, o branch “master”. Ao criarmos novos branchs, podemos realizar alterações nos arquivos de forma separada, de modo que as alterações não afetam a princípio o branch master. Nos casos abaixo, a pasta “GiteGithub” está trabalhando com o branch “titulo”, enquanto que a pasta “ana” –> “projetos” está trabalhando com o branch “lista”. É importante que se ressalte que cada alteração deve ser feita na sua respectiva pasta no Visual Studio, além de após as modificações no Git ser importante realizar os comandos para commitar essas novas informações (“git add” e “git commit -m"):
“GiteGithub”
 
“ana” -> “projetos”
 
Os arquivos estão sendo trabalhados em páginas de Gits separadas/diferentes.

•	Git log x branches: quando temos mais de um branch e executamos o comando “git log”, o Git irá mostrar as alterações do branch em que você está e as do branch principal (master). No caso abaixo, estamos no branch “lista”. Repare que ele não mostra o outro branch que está sendo trabalhado, ou seja, o “titulo”:
 

•	git merge (nome do branch que se quer juntar): o comando une dois branchs. Se estivermos no branch “master” e quisermos juntá-lo ao branch “titulo”, devemos digitar “git merge titulo”. O comando faz com que o Git automaticamente crie um commit com o branch atual (no caso, “master”), o que inclui todo o conteúdo de branch titulo. Esse comando “sincroniza” os dois branchs (no caso), pensando que o “master” pode ter sido alterado após o branch “titulo” ter sido criado. Nesse caso, o “git merge” une as informações posteriores a essa criação, mostrando como novos “commits”, mas não alterando essas alterações. Devido a isso, após o “merge” podem existir “commits estranhos”, pois as alterações não se fundiram, elas apenas constam no mesmo lugar. Após digitar o comando de “git merge”, irá aparecer a respectiva tela, a qual para sair é necessário digitar “:wq”:
 
 

•	git log --graph: é como o “git log”, mas mostra as linhas do “git merge” a esquerda:
 

•	git stash: cria um backup das modificações de seus arquivos.

•	git rebase (nome do branch que se quer incluir): unifica os branches envolvidos, puxando os “commits” para frente do branch de destino. O comando produz um histórico linear, mais limpo e mais fácil de ser lido do que o “git merge”, pois os branches são literalmente fundidos. Pela fusão, também não é gerado aquele “commit” adicional “estranho” que acontece no merge. Porém, o grande problema é que o “git rebase” mexe com toda a estrutura dos branches envolvidos, reescrevendo inclusive o histórico de “commits” destes branches. Se este processo de reescrita não for bem executado, podem ocorrer vários problemas no histórico dos branches envolvidos.

•	Diferença entre “merge” e “rebase”: o merge junta os trabalhos e gera um “merge commit”. O rebase aplica os commits de outra branch na branch atual.

•	Passos para fazer o “git rebase”:
No nosso exemplo, com o Git no branch “master”, trouxemos as informações do branch “titulo”:
 
Em seguida, pegamos essa sincronização de branches através do “git push”:
 
Depois, fomos no outro Git que estava aberto (com o branch “lista”, da pasta “ana” -> “projetos”), fizemos um “git checkout master” para ir para o branch “master” e depois um “git pull local master”, para incluir as informações da sincronização:
 
Em seguida, voltamos para a branch “lista”:
 
Então, fomos até o “index.html” do VS da pasta “ana” -> “projetos” e fizemos uma alteração qualquer, e a adicionamos e commitamos (“git add” e “git commit –m”)
  
E então voltamos para a branch “master”:
 
Importante destacar que a alteração que foi feita no VS pela pasta “ana” -> “projetos” (branch “lista”) foi na mesma linha que fizemos uma alteração no “index.html” do VS da pasta “GiteGithub” (branch “titulo”). Se, estando na pasta “ana” -> “projetos” no branch “master” tentarmos dar um “merge” ou “rebase” do branch “lista”, aparecerá um erro, justamente por o branch “master” já conter os commits do branch “titulo”, e nele ter alterações na mesma linha e arquivo do branch “lista”. Com isso, após o comando de merge/rebase com a lista tiver sido dado, no VS será possível verificar as duas versões da linha em questão, e escolher qual delas se quer manter. Basta remover o que não se quer e salvar. Em seguida, digitar “git add index.html (ou o arquivo que for)” e “git commit” (só assim mesmo).
Executar o “git push local master”:
 
Ir no VS, no arquivo “index.html” da pasta “GiteGithub” e fazer alguma alteração (aqui, fizemos em “Vagrant” e salvar:
 
Ir para o Git da pasta “GiteGithub”, adicionar e commitar (“git add” e “git commit –m”) essa alteração e digitar “git push local master”:
 
Isso, como visto acima, gera erro, pois no Git da pasta “ana” -> “projetos” já havíamos executado esse comando do “git push local master”. Por isso, precisamos antes executar o “git pull local master”:
 
Após isso, podemos realizar novamente o “git push local master”:
 
Voltar no Git da pasta “ana” -> “projetos” e executar o “git pull local master”, para que essa pasta também tenha as alterações.

•	git checkout -- (nome do arquivo que ser quer deletar a alteração): esse comando deleta uma alteração que fizemos no VS. Basta inserir o nome do arquivo em que a alteração foi feita após o “git checkout --":
 
Após esse comando, é possível verificar no VS que a alteração foi deletada.

•	git reset HEAD (nome do arquivo do VS que se quer voltar atrás na adição): esse comando reseta as alterações que estão pendentes de commmitar, quando por exemplo damos um “git add” em uma alteração, mas decidimos não commitá-la ainda. Nesse caso, após o “git reset HEAD” informamos qual a pasta onde esse “retorno” da ação deve ser feito”, e com isso é como se não tivesse sido dado o comando de “git add”:
 
Porém, para que a tentativa de alteração seja efetivamente excluída, é necessário digitar “git checkout --".

•	git revert (código do commit a ser deletado): esse comando deleta um commit (após ter sido feito o “git add” e “git commit –m”). Para isso, devemos digitar “git log”, identificar a hash do commit que queremos deletar, copiá-la e num novo comando, colá-la após o “git revert”:
 
Não é necessário informar todos os caracteres do hash, os 7 primeiros são suficientes para identifica-lo. No comando “git log --oneline", só esses 7 são mostrados, para todos os commits.

•	git stash: salva uma alteração para que seja usada depois, sem que seja necessário digitar o “git add” e o “git commit –m”. Mesmo que se façam outras alterações e commitações depois, isso não afeta, pois a alteração fica guardada:
 

•	git stash list: mostra uma lista das alterações que estão guardadas pelo comando “git stash”:
 

•	git stash apply (número da stash), git stash drop e git stash pop: a primeira tira a alteração da “stash”. O comando trás de volta a alteração e a aplica. É preciso que após “git stash apply” se informe o número da “stash” que se quer tirar, o que na imagem acima está representado por {0} na primeira e {1} na segunda. Mesmo fazendo isso, a alteração continua na stash, então para deletá-la de lá é necessário digitar o comando “git stash drop”. O comando “git stash pop” realiza essas duas ações ao mesmo, facilitando a digitação.
 

•	git checkout (hash do commit que se quer acessar, pode ser só os 7 primeiros caracteres): esse comando nos permite acessar algum commit que foram feitos no passado. Após o “git checkout”, é necessário colocar o hash do commit. No caso abaixo, foi digitado “git log --oneline" para pegar a hash e depois dado o comando em si:
 
 
Só com esse comando, qualquer nova alteração que for feita no commit que se acessou não ficará salva nos branches. Caso se queira que uma alteração nesse commit seja salvo, é necessário que após o uso do “git checkout (hash)”, se crie um novo branch. O esquema abaixo representa isso:
 
Para sair desse comando, basta digitar “git checkout (nome do branch que se quer voltar, como o “master”).
 

•	git diff (hash do commit, começando de baixo para cima)..(hash do commit, começando de baixo para cima): mostra a diferença entre códigos/commits (de todos os commits entre as hashs do comando):
 
Só com o “git diff” é possível verificar o que foi alterado e ainda não foi adicionado para commitar.

•	git log -n (número de quantas alterações se quer mostrar): o comando permite mostrar o “git log” apenas das últimas alterações. Caso queiramos ver só a mais recente, digitamos “git log -n 1”. Se quisermos ver as duas últimas, digitamos “git log -n 2”, e assim por diante:
 

•	git tag: ponto que não muda mais, um marco. Isso não quer dizer que o código não seja mais editável. Mas é uma versão de um código/arquivo. Ao ser executado, esse comando mostra as tags existentes (ver comando abaixo para adicionar uma tag).

•	git tag -a (nome da versão/marco): esse comando cria uma tag, um marco em certo ponto do trabalho. O “-a” indica que se está adicionado a tag, e em seguida é necessário indicar o nome que se quer dar à versão/marco. Pode ser incluída uma mensagem também nesse comando, se digitando “git tag -a (nome da versão/marco) -m “(mensagem)””:
 
É possível executar o “git push” também para uma tag:
 

•	Enviar projeto para o Github: com o “git remote –v”, podemos ver que temos os repositórios que está no Github, que são os denominados “origin”:
 
- Para enviar os arquivos ao Github, devemos executar o comando “git push origin (arquivo que se quer enviar)”. No caso, os arquivos que queremos enviar é tudo salvo no branch “master” (pois os outros branchs já constam também aqui) e a tag “v0.1.0”:
 
Com isso, no Github já é possível visualizá-los e até baixa-los:

sisger
======
Sistema de Gestão de Recursos e Serviços de Centro de Dados
======
Para fazer uma cópia do projeto, clique em FORK.

É nessa cópia que você codificará as propostas de melhoria. Uma Fork atua como uma ponte entre o proejto original no repositório e sua cópia pessoal. Você pode submeter "Pull Requests" para contribuir com projetos no qual você criou uma fork. Nesses "Pull Requests" serão oferecidas as mudanças que você efetuou no projeto original. Criação de Forks estão no coração da prática de programação em sociedade no GitHub.

Após criar a fork deste repositório, você pode fazer mudanças no projeto e submeter um Pull Request.

Para mais informações sobre como fazer a Fork de um repositório, verifique o guida de ajuda do GitHub no ítem "Forking Projects".  Obrigado! (ass. Wellington)


======
Para manter sua fork sincronizada:
======

Quando você cria uma fork para propor mudanças em um projeto principal, é uma boa prática sincronizar regularmente sua fork com o repositório principal. Para fazer isso, você precisa usar o comando GIT. 


======
Passo 1. Configurar o Git
======


  Se você não condigurou ainda, você precisa primeiramente realizar essa configução. Para instalar o git no Ubuntu use o comando "sudo apt-get install git"  
  
  #git config --global usar.name "SEU-NOME-DE-USUARIO"
  #git config --global usar.email "SEU-EMAIL NO GIT"
  #git config --global credential.helper cache
  #git config --global credential.helper cache 'cache --timeout=3600'
(para mais informações acessar https://help.github.com/articles/set-up-git/)


=
Passo 2. Crie um clone local da sua fork
=

  Criada a fork do projeto sisger para seu usuário do github, não será imediatamente possível editar o código da via Eclipse (ou outra IDE de desenvolvimento). Para isso você precisa criar um clone do projeto em sua máquina local. Vamos criar esse clone nos passos abaixo. 
  
  No GitHub, navegue até sua fork do repositório do Sisger. 
  Copie a URL apresentada no campo HTTPS Clone URL  que fica no menu a direita da página de sua fork do repositório.       Dependendo de como você se autenticou no github, a url será HTTPS ou SSH. Abra um terminal para executar o seguinte      procedimento: 

  Digite git clone e então cole a URL que você copiou no passo 2. O comando parecerá como o comando abaixo, com o seu      GitHub username no lugar do SEU-NOME-DE-USUÁRIO:

  git clone https://github.com/SEU-NOME-DE-USUÁRIO/sisger.git
  
  Aperte Enter. Seu clone local do repositório será criado. 

  git clone https://github.com/SEU-NOME-DE-USUÁRIO/sisger.git
  # Cloning into 'sisger'...
  #remote: Counting objects: 9, done.
  #remote: Compressing objects: 100% (4/4), done.
  #Unpacking objects: 100% (9/9), done.
  #remote: Total 9 (delta 1), reused 9 (delta 1)

Agora você tem uma cópia local da sua fork do sisger no repositório!

=
Passo 3: Configure o Git para sincronizar sua fork com o repositório original do Sisger
=

  Quando você fizer uma fork em um projeto para propor mudanças ao repositório original, você pode configurar o Git para   recuperar mudanças do projeto original em seu clone local da fork. 

  No GitHub, navegue até o repositório do Sisger.
  Copie a Clone URL (na barra a direita) da página do resposiorio.
  Abra um terminal.
  Mude os diretórios para a localização da fork que você clonou no PASSO 2.
    Para ir para seu diretório home, digite apenas cd sem nenhum outro texto.
    Para listar os arquivos e páginas no seu diretório corrente, digite ls
    Para entrar nos subdiretórios, digite cd seu_diretorio.
    Para ir um diretório acima, digite cd ...
        
  Digite git remove -v e aperte Enter. Você verá o diretório remoto atual do repositório para a sua fork.
    
  #origin	https://github.com/SEU-NOME-DE-USUÁRIO/sisger.git (fetch)
  #origin	https://github.com/SEU-NOME-DE-USUÁRIO/sisger.git (push)

  Digit git remote add upstream, e então cole a URL que você copiou no passo 2 e aperte Enter. O comando parecerá com:

    git remote add upstream https://github.com/cdger/sisger.git

  Para verificar o novo repositório upstream que você especificou para a sua fork, digite git remote -v novamente. Você deve ver a URL para sua fork como origin e a URL para o repositório original como upstream
    
  Agora, você pode manter sua fork sincronizada com o repositório upstream com apenas poucos comandos Git. Para mais informações, veja "Syncing a fork" no help do Git. 
  

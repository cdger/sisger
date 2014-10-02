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

Passo 1. Configura o Git

  Se você não condigurou ainda, você precisa primeiramente realizar essa configução. Não esqueça de configurar a autenticação para o o GitHub do Git também.

Passo 2. Crie um clone local da sua fork

  Criada a fork do projeto sisger para seu usuário do github, não será imediatamente possível editar o código da via Eclipse (ou outra IDE de desenvolvimento). Para isso você precisa criar um clone do projeto em sua máquina local. Vamos criar esse clone nos passos abaixo. 
  

    No GitHub, navegue até sua fork do repositório do Sisger. 
    Copie a URL apresentada no campo HTTPS Clone URL  que fica no menu a direita da página de sua fork do repositório. Dependendo de como você se autenticou no github, a url será HTTPS ou SSH. Abra um terminal para digitar a linha de comando que será mostrada a seguir. 

    Digite git clone e então cole a URL que você copiou no passo 2. O comando parecerá como o comando abaixo, com o seu GitHub username no lugar do SEU-NOME-DE-USUÁRIO:

    git clone https://github.com/SEU-NOME-DE-USUÁRIO/sisger.git
    
    
    Aperte Enter. Seu clone local do repositório será criado. 

    git clone https://github.com/YOUR-USERNAME/Spoon-Knife
    # Cloning into `Spoon-Knife`...
    # remote: Counting objects: 10, done.
    # remote: Compressing objects: 100% (8/8), done.
    # remove: Total 10 (delta 1), reused 10 (delta 1)
    # Unpacking objects: 100% (10/10), done.

Now, you have a local copy of your fork of the Spoon-Knife repository!
Step 3: Configure Git to sync your fork with the original Spoon-Knife repository

When you fork a project in order to propose changes to the original repository, you can configure Git to pull changes from the original, or upstream, repository into the local clone of your fork.

    On GitHub, navigate to the octocat/Spoon-Knife repository.
    Clone URL buttonIn the right sidebar of the repository page, click to copy the clone URL for the repository.
    Open Terminal (for Mac and Linux users) or the command line (for Windows users).
    Change directories to the location of the fork you cloned in Step 2: Create a local clone of your fork.
        To go to your home directory, type just cd with no other text.
        To list the files and folders in your current directory, type ls.
        To go into one of your listed directories, type cd your_listed_directory.
        To go up one directory, type cd ...

    Type git remote -v and press Enter. You'll see the current configured remote repository for your fork.

    git remote -v
    # origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
    # origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)

    Type git remote add upstream, and then paste the URL you copied in Step 2 and press Enter. It will look like this:

    git remote add upstream https://github.com/octocat/Spoon-Knife.git

    To verify the new upstream repository you've specified for your fork, type git remote -v again. You should see the URL for your fork as origin, and the URL for the original repository as upstream.

    git remote -v
    # origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
    # origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
    # upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (fetch)
    # upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (push)

Now, you can keep your fork synced with the upstream repository with a few Git commands. For more information, see "Syncing a fork."
Next Steps

The sky's the limit with the changes you can make to a fork, including:

    Creating branches: Branches allow you to build new features or test out ideas without putting your main project at risk.
    Opening pull requests: If you are hoping to contribute back to the original repository, you can send a request to the original author to pull your fork into their repository by submitting a pull request.

Find another repository to fork

Every public repository on GitHub can be forked, so find another project you're interested in and get forking!

The Explore GitHub page is a great place to find projects that pique your interest. The content changes all the time, so you can visit that page often to see what's new and cool on GitHub.

GitHub Explore page

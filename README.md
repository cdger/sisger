SISGER -Coleta e Publicação de Relatórios Gerenciais do Centro de Dados
======
Criando uma ramificação
======
Para propor novas funcionalidades ao projeto principal (https://github.com/cdger/sisger.git), você deve criar uma ramificação do projeto (git clone https://github.com/SEU-NOME-DE-USUÁRIO/sisger.git). Nesta ramificação você poderá efetuar quaisquer modificações sem criar instabilidade no projeto principal. Em um segundo momento, quando a proposta de funcionalidade estiver madura e  estável, a funcionalidade deverá ser mesclada ao projeto principal. 

Para criar uma ramificação, acesse a página princiapal do projeto (https://github.com/cdger/sisger) e clique no botão FORK. Uma ramificação (Fork) atua como uma ponte entre o proejto original no repositório e sua cópia pessoal. 


======
Para manter sua ramificação sincronizada com o repositório principal:
======

Quando você cria uma ramificação, é uma boa prática sincronizá-la regularmente com repositório principal. Essa sincronização é feito por comandos "git". Antes de atuar no dia a dia do desenvolvimento com comandos git, algumas cofigurações precisar ser feitas.

  1. Instalação do Git: Se você não tem o git instalado, você pode usar (no Ubuntu) o comando abaixo
    sudo apt-get install git
  2. Informe para o git seu nome de usuário, e-mail e tempo de timeout nas sincronizações
    git config --global user.name "SEU-NOME-DE-USUARIO"
    git config --global user.email "SEU-EMAIL NO GIT"
    git config --global credential.helper cache
    git config --global credential.helper cache 'cache --timeout=3600'
    (para mais informações acesse  https://help.github.com/articles/set-up-git/)

  Pronto, você está pronto para trabalhar com o git!


======
Passo 2. Trabalhando com sua ramificação
======

  Você pode editar arquivos online (diretamente na URL de endereço de sua ramificação). Porém, provavelmente você quererá utilizar o Eclipse (ou outro IDE de sua preferência) para efetuar os trabalhos de desenvolvimento. Nesse caso, você precisará criar uma cópia local (na sua estação de desenvolvimento) dos arquivos de sua ramificação. Para isso, para fazer o download, use o comando abaixo.
  
  git clone https://github.com/SEU-NOME-DE-USUÁRIO/sisger.git

Pronto, agora você tem uma cópia local da sua ramificação para usar com o Eclipse!
  

=
Passo 3. Configurando o git para sincronizar sua ramificação com o repositório principal
=

  Você pode configurar o git para recuperar mudanças do projeto original no clone local de sua ramificação.
  
  Para isso, em um terminal de comandos, entre no diretório do clone local da sua ramificação (criado no passo anterior) e use o comando abaixo.
  
    git remote add upstream https://github.com/cdger/sisger.git
  
  Note que ao digitar o comando "git remote -v" no diretório do clone local da sua ramificação, a saída deve ser parecida com a abaixo.
  
  
    #origin	https://github.com/SEU-NOME-DE-USUÁRIO/sisger.git (fetch)
    #origin	https://github.com/SEU-NOME-DE-USUÁRIO/sisger.git (push)
    #upstream	https://github.com/cdger/sisger.git (fetch)
    #upstream	https://github.com/cdger/sisger.git (push)

  Pronto! Agora você pode usar comandos gits para sincronizar sua ramificação e clone local ao repositório principal!
  
=
Comandos úteis
=

  Avisar ao git quais arquivos devem ser considerados no próximo commit:
  
    git add <arquivo>
    git add *  (caso todos os arquivos devam ser considerados)
    
  Efetuar commit:
    git commit -m "comentários da alteração"
    
  Enviar arquivos da sua ramificação para o repositório principal:
    git push origin master
    
  
  
  
  
  


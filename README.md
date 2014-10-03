SISGER -Coleta e Publicação de Relatórios Gerenciais do Centro de Dados
======

Bem vindo ao repositório principal do SISGER. 
  
Para melhor entender o controle de versão por meio da ferramenta GIT: 
  
  http://git-scm.com/book/pt-br/Primeiros-passos-No%C3%A7%C3%B5es-B%C3%A1sicas-de-Git
  http://git-scm.com/book/pt-br/Git-Essencial
  http://git-scm.com/book/pt-br/Ramifica%C3%A7%C3%A3o-Branching-no-Git
    
=
  Como desenvolver com equipes geograficamente dispersas de forma organizada?   
=

Para implementar novas funcionalidades ao projeto principal, crie uma ramificação do projeto cada vez que iniciar o desenvolvimento de uma nova feature (um novo relatório). A ramificação é criada pela interface web do github. Para criá-la você utiliza o botão "Fork" na página do projeto principal (https://github.com/cdger/sisger). Para usar o Eclipse para desenvolver, crie um clone da ramificação em sua máquina local. O comando será parecido com o abaixo.
 
    git clone https://github.com/SEU-NOME-DE-USUÁRIO/sisger.git

Ao concluir implementações, você criará um "Pull Request". Mantenha sempre sua ramificação sincronizada com a última versão do projeto principal. Caso contrário seu Pull Request não poderá ser efetuado (será necessário tratar conflitos de implementação). A aprovação do Pull Request significa que a implementação foi absorvida no projeto principal. 

  Obs: O comando "git push" salva modificações na sua ramificação. Embora seja 
  possível efetuar o push diretamente no repositório central, isso não é uma boa 
  prática porque o repositório central é um ponto de início para qualquer nova 
  feature. Quando o repositório central não recebe diretamente os commits, 
  a sincronização dos trabalhos entre os integrantes da equipe fica mais rápida. 
  
======
Preparação para usar o git
======

Instalação do Git: Se você não tem o git instalado, você pode usar (no Ubuntu) o comando abaixo

    sudo apt-get install git

Informe para o git seu nome de usuário, e-mail e tempo de timeout nas sincronizações
  
    git config --global user.name "SEU-NOME-DE-USUARIO"
    git config --global user.email "SEU-EMAIL NO GIT"
    git config --global credential.helper cache
    git config --global credential.helper cache 'cache --timeout=3600'
    (para mais informações acesse  https://help.github.com/articles/set-up-git/)

Pronto, você está pronto para trabalhar com o git!


======
Comandos úteis
======

Criar clone local de ramificação:
  
      git clone ENDEREÇO-DA-RAMIFICAÇÂO
      (obs: quando você cria um clone de uma ramificação, o repositório é batizado pelo nome Origin)
      (por padrão, o repositório origin vem com uma branch criada, de nome "master")
  
Adicionar repositórios remotos na máquina local:
  
      git remote add NOME-PARA-O-REPOSITORIO-REMOTO https://github.com/cdger/sisger.git  

  
Para ver os repositórios remotos configurados no seu projeto:
  
      git remote -v
      
Para sincronizar a master local com a master do repositório central
  
      git checkout master
      git fetch NOME-DADO-AO-REPOSITORIO-CENTRAL
      git rebase NOME-DADO-AO-REPOSITORIO-CENTRAL/master
      
Para consolidar implementações (fazer commit)
  
      git add <arquivo>
      git add *  (caso todos os arquivos devam ser considerados)
  
      git commit -m "comentários da alteração"
    



  # GitProject1
Exercícios práticos de git/github por powershell - catalisat6 M1 Ex2

## Status 
Concluído

## Objetivo
Este exercício teve como objetivo praticar e dmonstrar o usod de comandos básicos de Git, Github e atraves do terminal e comandos PowerShell. 

## Tópicos solicitados:

## Preparação de Ambiente:
   1. Criação de conta profissional no GitHub
      < >
 
  2. Instalação do Git no PowerShell
     PS C:\Users\gabrielly.boareto> git --version
     git version 2.47.1.windows.1
     
   3. Configuração de chave SSH
      Hi gabrielly.boareto! You've successfully authenticated, but GitHub does not provide shell access.

## Exercícios

  4. Configurar nome e email no Git
      PS C:\Users\gabrielly.boareto> git --version
      git version 2.47.1.windows.1
      PS C:\Users\gabrielly.boareto> git config --global user.name "Gabrielly Boareto"
      PS C:\Users\gabrielly.boareto> git config --global user.email "gabrielly.boareto@zup.com.br"
      PS C:\Users\gabrielly.boareto> git config --global user.name
      Gabrielly Boareto
      PS C:\Users\gabrielly.boareto> git config --global user.email
      gabrielly.boareto@zup.com.br

   5. Criar Alias para Git Log
      PS C:\Users\gabrielly.boareto> git config --global alias.lg "log --oneline --graph --decorate --all"
      PS C:\Users\gabrielly.boareto>

  6. Configurar o editor de texto para VSCode
     PS C:\Users\gabrielly.boareto> git config --global core.editor
     code --wait

  7. Verificar as configurações feitas com git config -list
      PS C:\Users\gabrielly.boareto> git config --list
      diff.astextplain.textconv=astextplain
      filter.lfs.clean=git-lfs clean -- %f
      filter.lfs.smudge=git-lfs smudge -- %f
      filter.lfs.process=git-lfs filter-process
      filter.lfs.required=true
      http.sslbackend=openssl
      http.sslcainfo=C:/Program Files/Git/mingw64/etc/ssl/certs/ca-bundle.crt
      core.autocrlf=true
      core.fscache=true
      core.symlinks=false
      pull.rebase=false
      credential.helper=manager
      credential.[https://dev.azure.com.usehttppath=true](https://dev.azure.com.usehttppath=true/)
      init.defaultbranch=master
      user.name=Gabrielly Boareto
      [user.email=gabrielly.boareto@zup.com.br](mailto:user.email=gabrielly.boareto@zup.com.br)
      alias.lg=log --oneline --graph --decorate --all
      core.editor=code --wait

  8. Crie uma pasta no computador
     PS C:\Users\gabrielly.boareto> mkdir pastaprojeto1
    Diretório: C:\Users\gabrielly.boareto
    Mode                 LastWriteTime         Length Name
    ----                 -------------         ------ ----
    d-----        01/12/2024     10:50                pastaprojeto1

  9. Acessar a pasta criada
      PS C:\Users\gabrielly.boareto> cd pastaprojeto1
      PS C:\Users\gabrielly.boareto\pastaprojeto1>

  10. Iniciar o versonamento atraves do comando git init
      PS C:\Users\gabrielly.boareto\pastaprojeto1> git init
      Initialized empty Git repository in C:/Users/gabrielly.boareto/pastaprojeto1/.git/
      PS C:\Users\gabrielly.boareto\pastaprojeto1>

11. Abrir o VSCode atraves do comando code
    PS C:\Users\gabrielly.boareto\pastaprojeto1> code .
    PS C:\Users\gabrielly.boareto\pastaprojeto1>

12. Adicionar uma pasta README.md
    PS C:\Users\gabrielly.boareto\pastaprojeto1> echo '#GitProject1" > README.md
    >> git add .
    >> git commit -m "feat: adicionar README inicial"
     
13. Adcionar o arquivo novo e realizar uma lateração como git add e git commit-m. Descrever a alteração realizada
    echo "# Projeto1" > README.md

14. Fazer alteração do README.me e, depois, realizar o novo comando como git add ou git commit-m alterando o README
    git add .
    git commit -m "feat: atualizar README"

    echo "Este é um projeto de exemplo." >> README.md
    echo "## Atualização do README" >> README.md
    echo "Aqui fizemos uma alteração no arquivo." >> README.md

15. Dar o comando git log e observar
    PS C:\Users\gabrielly.boareto> cd projeto1
    PS C:\Users\gabrielly.boareto\projeto1> git log
    commit b1b01f113d6c330768263aece2a77034e2683969 (HEAD -> master)
    Author: Gabrielly Boareto <gabrielly.boareto@zup.com.br>
    Date:   Sat Nov 30 00:57:25 2024 -0300

        style: Adicionando estilo básico ao site

    commit b0f4dd7d241ff77af8774abdba83a5745c5b190f
    Author: Gabrielly Boareto <gabrielly.boareto@zup.com.br>
    Date:   Sat Nov 30 00:57:00 2024 -0300

        feat: Adicionando página inicial

    commit c9ca9b2a03f9dd1876da88f563f2ae3e0fa965f7
    Author: Gabrielly Boareto <gabrielly.boareto@zup.com.br>
    Date:   Sat Nov 30 00:48:33 2024 -0300

    feat: Alterando o README

    commit 92b2b1cfbc465ead9b490fd547cd131079098467
    Author: Gabrielly Boareto <gabrielly.boareto@zup.com.br>
    Date:   Sat Nov 30 00:39:11 2024 -0300

        Primeiro commit: Criando o README.md
    
#Bônus
16. criar mais alguns arquivos e fazer commits utilizando mensagens de commit convencionais.

16. 1. Criar outro arquivo, por exemplo, `index.html`:
        echo "<html><body><h1>Bem-vindo ao Projetogit1</h1></body></html>" > index.html
    PS C:\Users\gabrielly.boareto\projeto1> echo "<html><body><h1>Bem-vindo ao Projetogit1</h1></body></html>" > index.html
  
    
16. 2. Adicionar e fazer o commit utilizando a convenção `feat`, por exemplo:
      git add index.html
      git commit -m "feat: Adicionando página inicial"
    PS C:\Users\gabrielly.boareto\projeto1> git add index.html
    PS C:\Users\gabrielly.boareto\projeto1>       git commit -m "feat: Adicionando página inicial"      
[master 0092b83] feat: Adicionando página inicial
     1 file changed, 0 insertions(+), 0 deletions(-)
    
    
16. 3. Crie mais alguns arquivos e faça commits, como `style.css` ou `script.js`, utilizando as mensagens de commit convencionais:
    echo "body { font-family: Arial, sans-serif; }" > style.css
    git add style.css
    git commit -m "style: Adicionando estilo básico ao site"
    PS C:\Users\gabrielly.boareto\projeto1> echo "body { font-family: Arial, sans-serif; }" > style.css
    PS C:\Users\gabrielly.boareto\projeto1>     git add style.css
    PS C:\Users\gabrielly.boareto\projeto1>     git commit -m "style: Adicionando estilo básico ao site"
    On branch master
    nothing to commit, working tree clean
    
    
### Anexo aqui o arquivo Exercícios práticos de Git - GitProject1.docx  onde constam os prints e consideraçoes extras sobre o projeto. 


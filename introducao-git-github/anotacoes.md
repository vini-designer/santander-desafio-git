# Git/Git hub

Controle de versão; Armazenamento em nuvem; Trabalho em equipe; Melhorar seu código; Reconhecimento

**Software CLI (command line interface):**

Não tem interface gráfico, como softwares GUI.

**Comandos básicos de navegação**

Windows: cd; dir; mkdir; del/rmdir

Unix: cs; ls; mkdir; rm -rf

flags - modificam/formatam os comandos

cd / - navega para a pasta raiz

cd .. - retrocede um nível na hierarquia de pastas

cls (windows); clear (linux) - limpa a tela do terminal

Tecla TAB - autocompleta

mkdir - criar pastas

echo hello > hello.txt - cria hello.txt com o conteúdo hello

del - deleta (apenas) arquivos

Seta para cima - atalho para acessar o histórico de comandos

rmdir /S /Q (windows) rm -rf (linux) - deleta (remove) o diretório

## Instalação do Git

[https://git-scm.com/](https://git-scm.com/)

**Tópicos fundamentais**

Sistema distribuido e seguro: colaborações (maintainers)

SHA1 dados encriptados - forma curta de representar um arquivo

Botão direito na pasta -> Git Bash Here - abre o Git na pasta selecionada (windows explorer)

openssl sha1 nome_do_arquivo

pelo sha1 o Git verifica se houve alteração no arquivo

**Objetos Git:** bloobs; trees - armazenam blobs e outras árvores; commits - junta tudo; aponta para árvores, parentes (commits anteriores), autor e mensagem. (todos contém metadados)

Github - ssh e token

nome de usuário e senha

**Chave ssh**

Conexão segura entre duas máquinas

**Gerar chave SSH**

github.com -> Settings -> SSH and GPG keys

Git Bash

ssh-keygen -t ed25519 -C [vinicius.mco@gmail.com](mailto:vinicius.mco@gmail.com)

cd /c/Users/Vinícius Oliveira/.ssh/

cat id_ed25519.pub

Copiar -> Colar no form do Github

**Inicializar o SSH Agent**

eval $(ssh-agent -s)

ssh-add id_ed25519

Clonar repositório

Ir até o repositório

Clicar no botão Code e copiar o código da aba SSH

git clone caminho_ssh

**Token**

Settings > Developer settings > Personal access tokens

Copiar o token > salvar em arquivo 

Clonar repositório

Ir a um repositório > clicar no botão Code > copiar endereço HTTPS

git clone caminho_https

colar token

**Primeiros comandos com Git**

-   Iniciar o Git - git init
    
-   Iniciar versionamento - git add
    
-   Criar um commit - git commit
    
criar pasta livro-receitas no terminal do GIT (Git Bash)

comando git init

ls -a (flag exibe arquivos ocultos)

**Configurações necessárias:**

git config --global (válida para todos os repositórios) user.email "vinicius.mco@gmail.com"

git config --global (válida para todos os repositórios) user.name "vini-designer"

![](https://lh4.googleusercontent.com/hbCpbLJZfvhyA1e_XEtQCniYTaT67XimnYOvDseFn6yEhhsZ61ncWaotMGrhK1NUkTleVAWw3aQM9FG81fgb7E0ZZZTcDK7BlyRQJU8AsVzHA9uRROWK0AMb-0FiYfn6cZvfsWlQjZITpzXyqrI)

[stackedit.io](http://stackedit.io)

Criar um arquivo .md

git add *

git commit -m (flag para adicionar mensagem/comentário) “commit inicial"
  

## Passo-a-passo no ciclo de vida

git init - inicializa um repositório

tracked: unmodified; modified; staged - rastreado

untracked - não rastreado (quando um arquivo existe, mas o Git não sabe da existência dele)

![](https://lh5.googleusercontent.com/MiqPkXricdbViB5K7UQSB53u5gFomMUxWgxTRKtUlkOPbVOIAh3dEVa_jjsRrzYEK0WyIKf5k77WRAN7VbcAuZIy-VJlWJMUO4iozR_LgKjcdUVHmh-c1FihasYYoc2XKXDAzrB0OsN1guty-gA)

“stage”: grava modificações em pequenos commits

![](https://lh3.googleusercontent.com/yPesykD_oQJsZidhNXtHDBIk-Bka428SlNWbT4DPhgKNAeqMY9UqLqJk0g3YLoaZRLyKYHQZ5FU64DAEakuHZ74unfVXMR0hxY9RPm_tZ2Lj02CJ93Ll8md2MuvHGb0BjrPbBLunRXDwBS8pxh4)

git status - monitora se o arquivo está untracked, modified, staged, etc.

mkdir receitas

mv lasanha.md ./receitas/

git status

git add lasanha.md ./receitas - leva à área de stage

git status

git commit -m “criação da pasta receitas e movimentação do arquivo lasanha.md para a pasta criada”

git status

echo README.md

ls

git status

git add *

git status

git commit -m “inclusão do arquivo README.md”

git status


## Trabalhando com o Github
  
Verificar se as configurações são as mesmas no Git e no Github

git config --list

Desconfigurar e configurar novamente

git config --global --unset user.email

git config --global --unset user.name

git config --global user.email “[vinicius.mco@gmail.com](mailto:vinicius.mco@gmail.com)”

git config --global user.name “vini-designer”

Criar conta no Github

Criar repositório

git remote add origin (apelido para o link) [https://github.com/vini-designer/livro-receitas.git](https://github.com/vini-designer/livro-receitas.git)

git remote -v

git push origin master (branch)

## Resolvendo conflitos no Github

Alterar arquivo README.me

git push origin master

git pull origin master

Baixar repositório

Clonar: git clone [https://github.com/python/cpython.git](https://github.com/python/cpython.git)

vem como um repositório

README: espécie de homepage do repositório

# **PASSO A PASSO - GIT / GITHUB**
Passo a passo feito a partir do vídeo:

[Git e Github Tutorial completo - Nelio Alves](https://www.youtube.com/watch?v=_hZf1teRFNg).

## Configurações iniciais
- git config --global user.name "Jeniffer Marcondes"
- git config --global user.email "jenii.marcondes@gmail.com"
- git config --list (Lista com as configurações)
- Configuração para ver arquivos ocultos (Windows)
 

    1. Iniciar -> Opções do explorador de arquivos

    2. DESMARCAR: "Ocultar as extensões dos tipos de arquivos conhecidos"

    3. MARCAR: "Mostrar arquivos, pastas e unidades ocultas"

## Configurar chave SSH para o Github
SSH é um protocolo para comunicação de dados com segurança.

O Github aboliu a autenticação somente com usuário e senha.

A ideia básica é cadastrar previamente quais computadores podem acessar o Github em seu nome. Outros computadores não conseguem acessar.

Para isto deve:
1. Gerar uma chave SSH no computador
- no google pesquisar: github ssh
- acessar instrução referente a pesquisa
- clicar em: gerar uma nova chave SSH e adicioná-la ao ssh-agent
- seguir as instruções para gerar a chave
abrir o git bach
ssh-keygen -t ed25519 -C "email"
- git dará opção de escolher diretório, se estiver de acordo tecla enter
- após dará opção de criar uma senha para comunicar com o github a cada interação, se não quiser basta teclar enter novamente
- senha gerada no diretório informado no passo anterior

2. Cadastrar essa chave no Github
- copiar chave pública (encontra-se no diretório criado no passo anterior)
- voltar no github
- menu -> settings -> SSh and GPG -> SSH keys -> add new
- preenche o título (ex: computador do trabalho)
- colar a chave em key 
- add ssh key

## Passo a passo: salvar primeira versão de um projeto no github
Considerando que agora o ambiente já está todo configurado (usuário e email, visualização de arquivos ocultos, chave SSH), sempre que criar um novo projeto, os passos básicos serão estes (troque os parâmetros em capslock pelos seus dados)

- abrir o gitbash no diretório a ser comitado
- git init (inicializar o repositório)
- git add . (comando para salvar uma versão - vai enviar o arquivo para uma pasta temporária chamada STAGE)
- git status (mostra o status do projeto, se for o caso mostra os arquivos no stage aguardando para serem salvos)
- git commit -m "MENSAGEM EXPLICATIVA" (comando para salvar uma versão - comando que vai efetivamente salvar o arquivo no git)
- git branch -M main (para garantir que será salvo como main e não como master)
- -criar um novo repositorio no github
- git remote add origin git@github.com:SEUUSUARIO/SEUREPOSITORIO.git (vai associar o projeto do computador com o projeto do github - pode copiar o parâmetro do github após criar o repositório com a opção SSH marcada)
- git push -u origin main (salva os arquivos no github)
- na primeira vez aparece uma mensagem de confirmação referente a chave, basta escrever yes + enter 

## Passo a passo: salvar uma nova versão
- git status
- git add .
- git commit - m "MENSAGEM EXPLICATIVA"
- git push 


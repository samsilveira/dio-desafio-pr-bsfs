# Git e GitHub

### O que é Git?

- Sistema de versionamento de código distribuído

### Benefícios:

- Controle de versão

- Armazenamento em nuvem

- Trabalho em equipe

- Melhoramento de código

- Reconhecimento




### Navegação Básica no Terminal

| Windows            | Unix               |                                     |
| ------------------ | ------------------ | :---------------------------------: |
| dir                | ls                 |    Listar conteúdo do diretório     |
| cd /               | cd /               |      Vai para o diretório raiz      |
| cd nomepasta       | cd nomepasta       |     Acessa o diretório indicado     |
| cd ..              | cd ..              |   Retrocede um nível no diretório   |
| cls                | clear              |            Limpa a tela             |
| TAB                | TAB                |       Completa o código/nome        |
| mkdir nome         | mkdir nome         |           Cria diretório            |
| echo texto         | echo texto         |     Imprime no terminal o texto     |
| echo txt > arq.txt | echo txt > arq.txt | Redireciona o fluxo para um arquivo |
| del nome           |                    |    Deleta o arquivo de uma pasta    |
| rmdir              | rm -rf             |           Apaga diretório           |

---



## Entendendo como o Git funciona

### Tópicos Fundamentais

- SHA1
  - Secure Hash Algorithm
  - Conjunto de funções hash criptográficas projetadas pela NSA
  - A encriptação gera um conjunto de caracteres identificadores de 40 dígitos

#### Objetos Internos do Git

##### Blob

- Metadados

  - Tipo de objeto
  - Tamanho
  - \0
  - Conteúdo

  > blob 9\0 conteudo

##### Tree

Armazena blobs. Também possui metadados

Seu SHA1 muda quando algum SHA1 interno muda

##### Commit

Irá juntar tudo e dará sentido para a alteração

Aponta para:

- Tree
- Parente
- Autor
- Mensagem

Também possui SHA1, que sofre alteração quando os hashes internos são alterados



#### Chave SSH e Tokens

##### Chave SSH

Forma de estabelecer uma conexão segura e encriptada entre duas chaves

##### Para criar uma chave  SSH

No Git Bash

> ssh-keygen -t ed25519 -C "e-mail"

A identificação fica salva na pasta "Usuário/.ssh"

São gerados dois arquivos:

- A chave particular
- A chave pública (id_ed25519.pub)



Dentro da pasta /.ssh

> cat id_ed25519.pub
>
> > Comando para visualizar a chave pública

A chave SSH deve ser vinculada ao GitHub



##### SSH Agent

Entidade encarregada de pegar e lidar com as chaves

Para inicializar:

> eval $(ssh-agent -s)

O SSH Agent será executado em segundo plano e será informado o PID do processo

Para definir a chave para o agente

> ssh-add /.ssh/id_ed25519
>
> > Chave privada



##### Token de Acesso Pessoal

Criado dentro do perfil do GitHub



#### Comandos Iniciais do Git

#####  Criando um Repositório

> git init
>
> > Para inicializar o Git na pasta



> ls -a
>
> > Para visualizar arquivos ocultos



##### Configurar pela primeira vez

> git config --global user.email "email"

> git config --global user.name "nome"



#### Adicionando Repositório ao GitHub

##### Dentro da pasta do projeto

> git remote add origin "endereço-no-github"
>
> > Adiciona ao GitHub

> git remote -v
>
> > Lista os repositórios cadastrados

> git push origin master
>
> > Envia o repositório





## Desafio de Projeto

- [x] Produzir um repositório com as anotações dos cursos.
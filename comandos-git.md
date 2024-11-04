# Era uma vez um arquivo com conflitos

## E então meu PR quebrou

> Sim! Isso vai acontecer com alguma certa frequência. Comandos novos para gravar não são da noite para o dia. Por isso a arte de praticar, pratique muito até se tornar faceis.

### E como dito no desafio

Esse arquivo contém conflitos. Primeiro, ajuste o que está conflitando. Agora após correção, ajuste o caminho da imagem abaixo. Altere o nome da imagem para meme_programer

![alt text](60fdc460429b8-1415386982.jpeg)

### Comandos GIT em treinamento

Seguindo no desafio, copie esse texto aqui dentro, e adicione em um novo arquivo. O nome do arquivo deve ser `resolver_conflitos.md`

## Comandos GIT

Agora sim: a partir deste ponto aqui, deve ser o comandos GIT. Adicione abaixo todos os comandos utilizados para essa Trilha.

-----

> Commit deixando apenas os comandos GIT, siga o desafio.

Ajuste o caminho dessa imagem também.

![alt text](7c64059f71fc543737d315a88aa79963-102520219.jpg)

## Gerenciando Arquivos de Variáveis de Ambiente

> Entender e praticar como proteger informações sensíveis armazenadas em arquivos de variáveis de ambiente, utilizando .gitignore para manter essas informações fora do repositório e versionamento.

### Cenário

Imagine que você faz parte de uma equipe de desenvolvimento que está criando um projeto web. Esse projeto requer configurações e chaves API sensíveis, como informações de banco de dados, tokens e credenciais de serviços externos, armazenadas em um arquivo .env. Sua tarefa é configurar o GIT para garantir que essas informações nunca sejam incluídas no repositório, protegendo-as de serem compartilhadas publicamente.

**Instruções**

- exemplo para o projeto (se o repositório já não tiver o arquivo .gitignore, você deverá configurá-lo)
- Criar um Arquivo .env - crie um arquivo .env com variáveis fictícias. Inclua exemplos de configurações de ambiente:

```
DB_USER=admin
DB_PASS=s3cur3P@ss
API_KEY=abcdef12345
```

**Este arquivo contém dados sensíveis que não devem ser versionados.**

- Adicionar o .env ao .gitignore - Edite o arquivo .gitignore do repositório para garantir que o arquivo .env seja ignorado

- Commit e Verificação: Realize o commit das alterações no .gitignore usando commits semânticos para manter a organização.

- Deve Criar e Compartilhar um Modelo de Arquivo .env
- Para que os demais colaboradores saibam quais variáveis de ambiente são necessárias, crie um arquivo chamado .env.example. Este arquivo deve conter apenas os nomes das variáveis, mas sem valores.

```
DB_USER=
DB_PASS=
API_KEY=
```

- Realize um commit desse arquivo .env.example com uma mensagem de commit semântica
- Crie um Pull Request para revisão final.

**Dicas:**

Ao resolver o conflito no .env.example, edite o arquivo para que o conteúdo final mantenha ambas as variáveis (API_SECRET e AUTH_TOKEN).

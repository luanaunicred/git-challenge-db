# O que é um Fork?

Fork é como criar uma "cópia" de um repositório (projeto) no GitHub para sua conta pessoal. Essa cópia é independente, ou seja, você pode trabalhar nela sem afetar o projeto original.

## Um exemplo prático

Imagine que existe um repositório público chamado projeto-original, criado por outra pessoa. Você quer melhorar algo no código ou adicionar uma funcionalidade. Mas, você não tem permissão direta para modificar o projeto original. Então, você faz um Fork para criar sua própria versão desse repositório.

Um fork é comumente usado quando você quer:

- Contribuir para um projeto que não é seu;
- Testar ou modificar o código sem interferir diretamente no projeto principal.

## Quando faço um Fork, todas as branches vêm juntas?

Sim, quando você faz um fork, todas as branches do repositório original são copiadas para o seu repositório forkado. Porém, a branch principal, como a main, é a que geralmente será mostrada primeiro.

## Quais são os fluxos após o Fork?

>Aqui está o fluxo típico após fazer um fork:

1. Clone o repositório forkado para sua máquina local

```git clone https://github.com/seu-usuario/meu-projeto.git
```

Isso cria uma cópia local do seu fork.

2. Configure o repositório original como remote

Para manter o seu fork atualizado com as mudanças do projeto original:

```git remote add upstream https://github.com/projeto-original/meu-projeto.git
```

**origin:** Aponta para o seu fork no GitHub.
**upstream:** Aponta para o repositório original.

3. Sincronize seu fork com o original (quando necessário)

Antes de fazer contribuições, atualize seu fork com as mudanças do projeto original:

```
git fetch upstream
git checkout main
git merge upstream/main
```

Isso garante que você está trabalhando com o código mais recente.

## Como contribuir em um projeto forkado?

1. Crie uma branch para a sua contribuição

É uma boa prática criar uma branch nova para cada funcionalidade ou correção de bug que você for implementar:

``` 
git checkout -b minha-nova-feature
```

2. Implemente suas mudanças localmente

Faça alterações no código, teste, e crie commits:

```
git add .

git commit -m "Implementa nova feature X"

```

3. Suba suas mudanças para o seu fork

Envie a branch para o GitHub:

```
git push origin minha-nova-feature

```

4. Abra um Pull Request (PR)

- Vá ao repositório original no GitHub.
- Clique em "Compare & pull request".
- Explique suas mudanças no PR, e envie para análise.

## Fluxo Visual

- Fork -> Copia o repositório para sua conta.
- Clone -> Baixa o código para sua máquina.
- Criação de Branch -> Trabalha em uma branch isolada.
- Pull Request -> Propõe suas mudanças para o repositório original.

-----

## Dicas para uma boa contribuição

- Leia o arquivo CONTRIBUTING.md do projeto original (nesses casos de colaboração tem), se ele existir. Ele geralmente contém as regras para contribuições.

- Seja claro e objetivo ao descrever suas mudanças no Pull Request.

- Atualize sempre seu fork antes de começar a trabalhar, para evitar conflitos.

## Boas práticas para colaboração em um repositório compartilhado

1. Entenda as regras do projeto

- Leia o arquivo CONTRIBUTING.md: Esse arquivo (se existir) geralmente explica as diretrizes para contribuir, como configurar o ambiente, padrões de código, e como enviar Pull Requests (PRs).

- Respeite o estilo e as normas do projeto.

2. Trabalhe em branches separadas

- Nunca faça alterações diretamente na branch principal (main).

- Use uma convenção de nomenclatura clara para suas branches, como:

```
feature/nova-funcionalidade
```

```
bugfix/corrige-erro-123

```

3. Faça commits significativos

Escreva mensagens de commit descritivas e no imperativo:

- Exemplo bom: `Adiciona validação para campos obrigatórios`
- Exemplos ruins: `Alterei arquivos`, `feat : automacao projeto bugbank`, `feat : ajustes finais`, `Feat : tentativa de deploy`

4. Sincronize seu código com o repositório

Antes de começar ou finalizar seu trabalho, atualize sua branch com as mudanças mais recentes:

```
git fetch origin
git merge origin/main

```

5. Testes e validações

- Sempre execute os testes antes de abrir um Pull Request.
- Se possível, adicione novos testes para cobrir suas mudanças.

6. Seja respeitoso nas revisões

- Responda feedbacks de revisores com calma e objetividade.
- Faça alterações sugeridas de forma iterativa, e use o recurso de "resolvido" para marcar feedbacks tratados.

7. Escreva uma boa descrição no Pull Request

- Explique o que mudou e por que.
- Use checklists ou mencione issues relacionadas:

-----

> Exemplo abaixo:

## O que foi feito

- Adiciona validação de e-mails.

## Issues relacionadas

- Closes #123.

-----

## Boas práticas para colaboração em um repositório forkado

1. Mantenha seu fork atualizado

Sincronize regularmente seu fork com o repositório original:

```
git fetch upstream
git merge upstream/main

```

Isso evita conflitos e mantém suas mudanças alinhadas com o projeto.

2. Trabalhe localmente em branches

- Assim como em repositórios compartilhados, evite trabalhar na branch principal.
- Use branches para cada feature ou bugfix.

3. Crie Pull Requests organizados

- Abra Pull Requests apenas quando seu trabalho estiver completo.
- Divida grandes mudanças em PRs menores, quando possível.

4. Foque na clareza

- Suas alterações devem ser bem definidas e conter comentários claros, caso o código seja complexo.

5. Minimize alterações desnecessárias

- Evite mudar partes do código que não têm relação com o que você está contribuindo.
- Por exemplo, não altere espaços ou formatações, a menos que seja necessário.

6. Comunicação aberta

- Participe de discussões em issues ou Pull Requests. Se algo não estiver claro, pergunte.
- Demonstre interesse no projeto e ofereça ajuda onde for possível.

-----

## Referências

[Criar fork de um repositório](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)

[Trabalhar com bifurcações](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/working-with-forks)

[Sobre conflitos de mesclagem](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/about-merge-conflicts)

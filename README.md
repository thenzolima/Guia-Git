# Como criar um repositório Git e sincronizar com o GitHub.

Neste texto, irei abordar o uso do Git e do GitHub, ferramentas essenciais para o controle de versionamento de código e colaboração em projetos de desenvolvimento - independente da área.

Antes de começar, é preciso instalar o git. Para saber como instalar o software no seu sistema operacional, consulte o [site oficial do projeto](https://git-scm.com/).

---

## Criando um repositório local

Com o git instalado, crie uma pasta local em seu computador. Para torná-lo um repositório git, abra o terminal nessa pasta e digite:

```git
git init
```

Caso no seu diretório tenha uma pasta `.git`, quer dizer que deu certo.

---

## Adicionando os arquivos no repositório

Um bom repositório não existe sem um `README.md`, então crie um arquivo de texto com esse nome no diretório.

Entretanto, o arquivo ainda não está incluso no repositório. Qualquer alteração antes de ser "commitada", deve ser adicionada. Então para adicionar de fato o arquivo ao repositório, digite:

```git
git add README.md
```

Se você tem mais de um arquivo, e queira adicionar todos ao repositório, use:

```git
git add .
```

Para consultar os arquivos enviados, digite `git status`.

---

## Primeiro commit

Está tudo pronto para o primeiro `commit`! Mas o que é isso?

O `commit` é um registro de alterações em um repositório de código-fonte. Ou seja, qualquer alteração do seu repositório é chamada de `commit`.

Lembrando que todo `commit` precisa de um título, então para "commitar" e intitular o que foi adicionado lá, digite:

```git
git commit -m "primeiro commit"
```

Use o `git status` novamente. Se não apareceu nada para dar `commit`, podemos prosseguir.

---

## Alterando o nome da branch principal

Não sendo muito técnico, `branch` é um caminho independente do desenvolvimento dentro de um repositório. Inicialmente, o projeto tem apenas um `branch`, mas pode ser criado outros com o intuito de trabalhar em mudanças no código, sem afetar a linha principal do projeto.

Quando você cria um novo repositório, a primeira `branch` se chama `master`. Entretanto, é recomendado alterar o nome dela para `main`, por ser uma nomenclatura mais atualizada.

Essa alteração pode ser feita digitando em seu terminal:

```git
git branch -M "main"
```

---

## Publicando nosso repositório local no GitHub

Para fazer a hospedagem do projeto, crie um repositório no GitHub clicando no botão `new` na aba de repositórios do seu perfil. Como já temos um `README.md`, não é preciso ativar a opção de adicionar esse arquivo.

Quando o repositório for criado, será mostrado um guia do próprio GitHub de como fazer a publicação.

É preciso conectar os dois repositórios (local e remoto) usando o seguinte comando:

```git
git remote add origin https://github.com/usuario/nomedorepositorio.git
```

Ainda não foi publicado nenhum arquivo. Então, finalizamos o processo com o comando `git push -u origin main` para "empurrar" os `commits` para o repositório remoto - será solicitado seu login no GitHub.

Com o login feito, ele começará a encaminhar seus arquivos locais para o repositório da plataforma!

---

## Criando, alterando e mesclando as branches

Criamos uma nova branch usando:

```git
git checkout -b "segunda-branch"    
```

A partir de agora, qualquer `git add` ou `git commit`, será destinada a nova `branch`. Portanto, o `git push` não terá `main` no final, e sim o nome da `branch` que você acabou de criar:

```git
git push origin segunda-branch
```

Use `git checkout main` para voltar a `branch` principal.

Podemos mesclar uma `branch` na outra com:

```git
git merge nome-da-branch-que-você-quer-mesclar
```

Lembrando que após mesclar, deve-se dar um `git push` para aplicar a mesclagem.

---

## Outros comandos

`git clone link-de-outro-repositorio`: Clona um repositório no GitHub para o seu repositório local.

`git pull`: Traz as alterações feitas no repositório remoto para o repositório local.

---

## Conclusão

Espero que você tenha terminado esse material sabendo o básico desses recursos e com vontade de aprender mais sobre. Se gostou, não deixe de dar uma estrelinha nesse repositório e de compartilhar com aquele amigo dev. que com certeza irá se beneficiar do conteúdo.

Caso queira entrar em contato comigo: thenzolima@proton.me

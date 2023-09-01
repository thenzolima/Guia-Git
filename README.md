# Como usar o git.

Nesse texto, irei ensinar a como usar o git e publicar o seu repositório no GitHub.

Antes de começar, é preciso instalar o git. Para saber como instalar o software no seu sistema operacional, consulte o [site oficial do projeto](https://git-scm.com/).

---

## Criando um repositório local

Com o git instalado, crie uma pasta local em seu computador. Para torna-lô um repositório git, abra o git nessa pasta e digite:

```git
git init
```

Caso no seu diretório tenha uma pasta `.git`, quer dizer que deu certo.

---

## Adicionando os arquivos no repositório

Um bom repositório não existe sem um `README.md`, então crie um arquivo de texto com esse nome na pasta.

Entretanto, o arquivo ainda não está incluso no repositório. Qualquer alteração antes de ser "commitada", deve ser adicionada. Então para adicionar de fato o arquivo ao repositório, digite:

```git
git add README.md
```

Caso você tenha mais de um arquivo, e queira adicionar todos ao repositório, use o ponto:

```git
git add .
```

Para consultar os arquivos enviados que ainda não foram commitados, usamos o `git status`

---

## Primeiro commit

Está tudo pronto para o primeiro commit! Mas o que é isso?

O `commit` é um registro de alterações em um repositório de código-fonte. Ou seja, qualquer alteração do seu repositório é chamda de `commit`.

Lembrando que commit precisa de um título, então para "commitar" e entitular o que foi adicionado no repositório, digite:

```git
git commit -m "primeiro commit"
```

Use o `git status` novamente. Se não apareceu nada para dar `commit`, podemos prosseguir para o próximo passo.

---

## Alterando o nome da branch principal

Não sendo muito técnico, `branch` é um caminho independente do desenvolvimento dentro de um repositório. Inicialmente o projeto tem apenas um `branch`, mas pode ser criado outros com o intuito de trabalhar em mudanças no código sem afetar a linha principal do projeto.

Quando você cria um novo repositório, a primeira `branch` se chama `master`. Entretanto, é recomendando pelo próprio GitHub alterar o nome dela para `main`, por ser uma nomeclatura mais atualizada.

Para alterar o nome dessa `branch` de `master` para `main`, digite:

```git
git branch -M "main"
```

---

## Publicando nosso repositório local no GitHub

Para fazer a hospedagem do projeto, crie um repositório no GitHub clicando no botão `new` na aba de repositórios do seu perfil.

Como já temos um `README.md`, não é preciso ativar a opção de adicionar esse arquivo.

Quando o repositório é criado, será mostrado um guia do próprio GitHub de como fazer a publicação.

Iniciamos a postagem dos repositórios conectando eles usando o seguinte comando:

```git
git remote add origin https://github.com/usuario/nomedorepositorio.git
```

Só que não foi enviado ainda nenhum arquivo para a plataforma. Para finalizar o processo, use o comando `git push -u origin main` para "empurrar" os `commits` para a branch `main` do repositório online.

Então vai pedir para você logar no GitHub. Com o login feito, Ele irá começar a encaminhar seus arquivos locais para o repositório!

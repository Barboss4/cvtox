# Site do CVTox

Site estático, responsivo e sem framework, pensado para publicação gratuita no GitHub Pages.

## O que editar no dia a dia

Quase todo o conteúdo fica em:

`data/site.js`

Nesse arquivo você altera:
- nome/edição do evento;
- data e local;
- link de inscrições;
- destaques da edição;
- palestrantes;
- programação;
- comissão;
- fotos das edições anteriores;
- contatos.

Assim você não precisa ficar mexendo em vários arquivos HTML.

## Fotos dos palestrantes e da comissão

1. Coloque a foto em `assets/img/`.
2. No `data/site.js`, use o campo `photo` tanto nos palestrantes quanto na comissão:

```js
photo: "assets/img/nome-da-pessoa.jpg"
```

Na página inicial, os palestrantes aparecem em um carrossel responsivo. A página `palestrantes.html` continua mostrando todos em grade.

## Fotos das edições anteriores

1. Coloque as imagens em `assets/img/fotos/`.
2. No `data/site.js`, adicione cada foto em `eventPhotos`, usando exatamente o nome da edição correspondente:

```js
eventPhotos: [
  {
    image: "assets/img/fotos/encontro-2025.jpg",
    edition: "VIII CVTox",
    year: 2025,
    caption: "Participantes durante uma das atividades do evento."
  }
]
```

Os álbuns são criados automaticamente a partir das edições cadastradas em `posters`. O pôster vira a capa provisória do álbum e cada foto aparece no álbum indicado pelo campo `edition`. Enquanto um álbum estiver vazio, ele exibe “Fotos em breve”.

## Estrutura

- `index.html` — página inicial
- `programacao.html` — agenda
- `palestrantes.html` — convidados
- `inscricoes.html` — inscrições
- `local.html` — local
- `posteres.html` — pôsteres das edições anteriores
- `fotos.html` — galeria das edições anteriores
- `comissao.html` — comissão organizadora
- `contato.html` — contatos
- `data/site.js` — conteúdo editável
- `assets/css/style.css` — aparência e responsividade
- `assets/js/main.js` — componentes compartilhados

## Publicar no GitHub Pages

1. Crie um repositório no GitHub.
2. Envie todo o conteúdo desta pasta para a raiz do repositório.
3. No repositório, abra **Settings → Pages**.
4. Em **Build and deployment**, selecione **Deploy from a branch**.
5. Selecione a branch `main` e a pasta `/ (root)`.
6. Salve e aguarde o endereço público ser criado.

## Dica importante

O projeto usa caminhos relativos. Por isso funciona normalmente em GitHub Pages mesmo quando o site fica em um endereço como:

`usuario.github.io/nome-do-repositorio/`

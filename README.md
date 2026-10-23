# pawfectly-world-design

Protótipo em HTML e CSS das telas da Pawfectly World, rede social de adoção de animais.

## O que faz

Páginas estáticas, com Bootstrap 4 e imagens de exemplo carregadas da internet, sem back-end:

| Página                 | Tela                         |
| ---------------------- | ---------------------------- |
| `login.html`           | login                        |
| `cadastro.html`        | login (variação)             |
| `loginCadastro.html`   | login e cadastro na mesma tela |
| `feed.html`            | feed de posts                |
| `perfilUsuario.html`, `perfilUsuario2.html` | perfil do usuário |
| `perfilAnimal.html`    | perfil de um animal          |
| `cadastroAnimal.html`  | cadastro de animal (com a opção "Adoção Ativa") |

Os estilos ficam em `css/` e o ícone de "adicionar" em `img/mais.png`.

## Por que existe

Faz parte do TCC do curso técnico em Informática do IFPE (2023), a Pawfectly World. Este
protótipo definiu as telas antes do front-end; a API está em
[pawfectly-world-api](https://github.com/rillmind/pawfectly-world-api).

## Instalação

Não há dependências para instalar: basta clonar. É preciso um navegador e, para servir as
páginas, Python 3 (ou qualquer servidor de arquivos estáticos).

```sh
git clone https://github.com/rillmind/pawfectly-world-design.git
cd pawfectly-world-design
```

## Como testar

Não há testes automatizados. Sirva a pasta e abra as páginas no navegador:

```sh
python3 -m http.server 8000
# abra http://localhost:8000/feed.html, http://localhost:8000/login.html etc.
```

Use um servidor em vez de abrir o arquivo direto (`file://`): várias páginas carregam o CSS
pelo caminho absoluto `/css/styles.css`, que só funciona servido a partir da raiz do repositório.
Confira que cada página abre com o estilo aplicado e as imagens carregadas (é preciso estar
conectado, porque Bootstrap, ícones e fotos vêm de CDNs e sites externos).

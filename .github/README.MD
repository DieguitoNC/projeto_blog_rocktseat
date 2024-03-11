
# font-smoothing
- deixa a fonte das letras mais "smooth"
```
* {

  margin: 0;

  padding: 0;

  box-sizing: 0;

  -webkit-font-smoothing: antialiased;

  -moz-osx-font-smoothing: grayscale;

}
```
# grid-template-rows: max content
- Vai crescer conforme o tamanho do conteudo embutido
```
#app {

  display: grid;

  grid-template-rows: max-content 1fr max-content;

  height: 100vh;

}
```
# Estrutura em grid com header e footer fixos
- Nesse caso, precisamos criar uma class para header e footer sendo igual, dentro do "main" criamos a tag igual, porem dentro de uma div, assim basta colocar: overflow-y: scroll
```
<body>

  <div id="app">

    <header class="container">

      header

    </header>

    <main>

      <div class="container">

        main

      </div>

    </main>

    <footer class="container">

      footer

    </footer>

  </div>

</body>
```
- No css
```
main {

  background-color: gray;

  overflow-y: scroll;

}
```

# Variáveis CSS
- colocamos normalmente no css root -> :root
- depois dos -- coloca-se o nome que facilita o entendimento
- para chamar a variável coloca-se: var()
```
:root {

  font-size: 62.5%;

  

  --color-base-white: #ffffff;

  --color-base-gray-100: #f5f5f5;

  --color-base-gray-300: #8d8d99;

  --color-base-gray-900: #202024;

}
```
- Para utilizar
```
  background-color: var(--color-base-gray-100) ;
```

# api para gerar img aleatória - tipos
```
      <img class="avatar" src="https://randomuser.me/api/portraits/women/70.jpg" alt="Imagem de uma mulher">
```
```
            <img src="https://source.unsplash.com/random?h=1" alt="">
```
# Formatação de imagem sem perder qualidade: object-fit: cover
```
.avatar {

  width: 4.2rem;

  height: 4.2rem;

  

  object-fit: cover;

  

  border-radius: 50%;

}
```
# Acessibilidade no forms com placeholder
- No forms o placeholder não é lido pelo navegador, para ser interpretado precisa ser feito dentro do label a frase que fica no placeholder e fazer com que fique escondido.
- Para tal, coloca-se um width e height de 1px com overflow hidden e position absolute
```
.input-wrapper label {

  width: 1px;

  height: 1px;

  overflow: hidden;

  position: absolute;

}
```
# Proporção de imagem com aspect ratio
- Para ajustar a imagem conforme uma padronização de proporção, optar por escolher enquadramentos padrões. 16/9, 4/3 9/16. etc
```
.item img {

  width: 100%;

  aspect-ratio: 16/9;

  object-fit: cover;

}
```

# Imagem não enquadra corretamente - overflow
- Serve para deixar a imagem enquadrar corretamente ao utilizar o border-radius
- Utiliza-se o overflow: hidden
```
.item {

  background-color: var(--color-base-white);

  border-radius: 0.8rem;

  overflow: hidden;

}
```

# Filtro CSS - filter
- Serve para aplicar filtro nas imagens. Há diversos filtros que podem ser utilizados, como saturação, contraste, gray scale, etc.
- A ideia mais pertinente é aplicar um hover e com isso a img alterar

```
.item img:hover {

  filter: hue-rotate(7deg) contrast(101%) saturate(200%);

}
```
```
.logo {

  filter:saturate(200%)  brightness(2) hue-rotate(90deg);

}
```

# CSS Transition
# CSS Animation

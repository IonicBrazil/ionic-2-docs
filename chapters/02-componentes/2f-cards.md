# Card

Os cards são uma ótima maneira de exibir as partes importantes de conteúdo e estão emergindo rapidamente como um padrão de design para aplicativos. Eles são uma ótima maneira para conter e organizar a informação e ao mesmo tempo para criação de expectativas previsíveis ao usuário. Com tanto conteúdo a ser exibido de uma só vez e muitas vezes tão pouca tela, os cards tornaram-se rapidamente o padrão de design de escolha para muitas empresas, incluindo empresas como Google, Twitter, e Spotify.

Para experiências móveis, os cards tornam fácil a exibição da mesma informação visual em diferentes tamanhos de tela. Eles permitem mais controle, são flexíveis e podem até mesmo serem animados. Os cards são geralmente colocados em cima um do outro, mas podem também ser usadas como uma "página" e deslizável entre esquerda e direita.

### Contents
* [Basic Cards]()
* [Card Headers]()
* [Card Lists]()
* [Card Images]()
* [Background Images]()
* [Advanced Cards]()


Uso Básico:

Os cartões são primeiramente um componente CSS. Para usar adicionar um cartão básico, siga esta estrutura:

``` ts
<ion-card>

  <ion-card-header>
    Cabeçalho
  </ion-card-header>

  <ion-card-content>
    <!-- Adicione um conteúdo aqui! -->
  </ion-card-content>

</ion-card>
```

## Card Headers
Assim como uma página normal, os cards podem ser personalizados para incluir cabeçalhos. Para adicionar o use um card header, adicionando o componente <ion-card-header> dentro do seu card:

``` ts
<ion-card>
  <ion-card-header>
    Cabeçalho
  </ion-card-header>
  <ion-card-content>
    Os britânicos usam o termo "header", mas o termo americano "head-shot", o Inglês simplesmente se recusa a adotar.
  </ion-card-content>
</ion-card>
```

## Card Lists

``` ts
Um card pode conter uma lista de itens. Para criar uma card-lists, adicione elementos com o atributo ion-item dentro de uma ion-list em seu card:

<ion-card>
  <ion-card-header>
    Explore Nearby
  </ion-card-header>

  <ion-list>
    <button ion-item>
      <ion-icon name="cart" item-left></ion-icon>
      Shopping
    </button>

    <button ion-item>
      <ion-icon name="medical" item-left></ion-icon>
      Hospital
    </button>

    <button ion-item>
      <ion-icon name="cafe" item-left></ion-icon>
      Cafe
    </button>

    <button ion-item>
      <ion-icon name="paw" item-left></ion-icon>
      Dog Park
    </button>

    <button ion-item>
      <ion-icon name="beer" item-left></ion-icon>
      Pub
    </button>

    <button ion-item>
      <ion-icon name="planet" item-left></ion-icon>
      Space
    </button>

  </ion-list>
</ion-card>
```

## Card Images

Imagens muitas vezes variam em tamanho, por isso é importante que elas adotem um estilo consistente em todo o aplicativo. As imagens podem ser facilmente adicionadas aos cards. Adicionar uma imagem a um card vai dar a imagem uma largura constante, e uma altura variável. Listas, cabeçalhos e outros componentes do cartão pode ser facilmente combinado com os cartões de imagem. Para adicionar uma imagem a um cartão, use a seguinte marcação:

``` ts
<ion-card>
  <img src="img/nin-live.png"/>
  <ion-card-content>
    <ion-card-title>
      Nine Inch Nails Ao Vivo
      </ion-card-title>
    <p>
	   O grupo industrial mais popular de todos os tempos e em grande parte
       responsável por trazer a música para uma audiência em massa.
    </p>
  </ion-card-content>
</ion-card>
```

## Background Images

Os cards podem ser usados para atingir uma grande variedade de modelos. Nós fornecemos muitos dos elementos para conseguir projetos comuns, mas às vezes será necessário adicionar estilos personalizados. Adicionando imagens de fundo para cards é um exemplo perfeito de como a adição de estilos personalizados pode conseguir uma aparência completamente diferente.

O seguinte código HTML pode ser adicionado ao conteúdo de uma página:

``` ts
<ion-content class="card-background-page">

  <ion-card>
    <img src="img/card-saopaolo.png"/>
    <div class="card-title">São Paulo</div>
    <div class="card-subtitle">41 Listings</div>
  </ion-card>

  <ion-card>
    <img src="img/card-amsterdam.png"/>
    <div class="card-title">Amsterdam</div>
    <div class="card-subtitle">64 Listings</div>
  </ion-card>

  <ion-card>
    <img src="img/card-sf.png"/>
    <div class="card-title">San Francisco</div>
    <div class="card-subtitle">72 Listings</div>
  </ion-card>

  <ion-card>
    <img src="img/card-madison.png"/>
    <div class="card-title">Madison</div>
    <div class="card-subtitle">28 Listings</div>
  </ion-card>

</ion-content>
```

Em seguida, no arquivo Sass para a página:

``` sass
.card-background-page {

  ion-card {
    position: relative;
    text-align: center;
  }

  .card-title {
    position: absolute;
    top: 36%;
    font-size: 2.0em;
    width: 100%;
    font-weight: bold;
    color: #fff;
  }

  .card-subtitle {
    font-size: 1.0em;
    position: absolute;
    top: 52%;
    width: 100%;
    color: #fff;
  }

}
```

## Advanced Cards

Os estilos de diferentes tipos de cards podem ser combinados para criar cards avançados. Cards também podem receber um CSS personalizado. Abaixo estão alguns cards avançados que foram construídos através da combinação de vários atributos do card com uma pequena quantidade de CSS personalizado.

### Contents
* Social Cards
* Map Cards

### Social Cards

É muitas vezes necessário para criar social cards dentro de uma aplicação. Usando uma combinação de diferentes itens em um card que você pode conseguir isso.

``` ts
<ion-card>

  <ion-item>
    <ion-avatar item-left>
      <img src="img/marty-avatar.png">
    </ion-avatar>
    <h2>Marty McFly</h2>
    <p>November 5, 1955</p>
  </ion-item>

  <img src="img/advance-card-bttf.png">

  <ion-card-content>
  <p>Wait a minute. Wait a minute, Doc. Uhhh... Are you telling me that you built a time machine... out of a DeLorean?! Whoa. This is heavy.</p>
  </ion-card-content>

  <ion-item>
    <button primary clear item-left>
      <ion-icon name="thumbs-up"></ion-icon>
      <div>12 Likes</div>
    </button>
    <button primary clear item-left>
      <ion-icon name="text"></ion-icon>
      <div>4 Comments</div>
    </button>
    <ion-note item-right>
      11h ago
    </ion-note>
  </ion-item>

</ion-card>
```

### Map Cards

Uma combinação de componentes Ionic pode ser utilizada para criar um card que aparece como um mapa.

``` ts
<ion-card>

  <img src="img/advance-card-map-madison.png">
  <button fab fab-right fab-top>
    <ion-icon name="pin"></ion-icon>
  </button>

  <ion-item>
    <ion-icon name="football" item-left large></ion-icon>
    <h2>Museum of Football</h2>
    <p>11 N. Way St, Madison, WI 53703</p>
  </ion-item>

  <ion-item>
    <ion-icon name="wine" item-left large ></ion-icon>
    <h2>Institute of Fine Cocktails</h2>
    <p>14 S. Hop Avenue, Madison, WI 53703</p>
  </ion-item>

  <ion-item>
    <span item-left>18 min</span>
    <span item-left>(2.6 mi)</span>
    <button primary clear item-right>
      <ion-icon name="navigate"></ion-icon>
      Start
    </button>
  </ion-item>

</ion-card>
```

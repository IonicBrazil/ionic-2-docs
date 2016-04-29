# Botões

Os botões são um meio essencial para interagir e navegar através de um aplicativo, estes devem comunicar claramente que uma ação ocorrerá após o usuário tocá-los. Os botões são componentes simples no Ionic, podem ser compostos por texto, ícone, ou ambos e podem ser modificados com uma variedade de atributos.

## Conteúdo
* [Estilo Padrão]()
* [Estilo Contorno]()
* [Estilo Limpar]()
* [Redondos]()
* [Quadrados]()
* [Botões Completos]()
* [Tamanhos de botões]()
* [Botões com icones]()
* [Botões de ações flutuante]()
* [Botões em Componentes]()


## Utilização básica:
``` ts
<button>Button</button>
```

A propriedade primary define a cor do botão. O Ionic inclui uma série de cores padrões que podem serem facilmente substituídas:

``` ts
<button light>Light</button>
<button>Primary</button>
<button secondary>Secondary</button>
<button danger>Danger</button>
<button dark>Dark</button>
```


## Estilo Contorno
Para utilizar o estilo contorno em um botão, adicione a propriedade outline:

``` ts
<button light outline>Light Outline</button>
<button outline>Primary Outline</button>
<button secondary outline>Secondary Outline</button>
<button danger outline>Danger Outline</button>
<button dark outline>Dark Outline</button>
```

## Estilo Limpo
Para utilizar o estilo limpo em um botão, adicione a propriedade clear:

``` ts
<button light clear>Light Clear</button>
<button clear>Primary Clear</button>
<button secondary clear>Secondary Clear</button>
<button danger clear>Danger Clear</button>
<button dark clear>Dark Clear</button>
```

## Botões Rendondos
Para criar botões com bordas arredondadas, adicione a propriedade round:

``` ts
<button light round>Light Round</button>
<button round>Primary Round</button>
<button secondary round>Secondary Round</button>
<button danger round>Danger Round</button>
<button dark round>Dark Round</button>
```

## Botões de bloco
Adicionando um bloco para um botão fará com que o botão use a largura 100% do seu pai. Ele também irá adicionar display: block para o botão:

``` ts
<button block>Block Button</button>
```


## Botões Cheios
Adicionando a propriedade full para um botão fará com que o botão tire 100% da largura do seu pai. No entanto, ele também irá remover as bordas da esquerda e direita do botão. Este modelo é útil quando o botão deve-se esticar ao longo de toda a largura da tela.

``` ts
<button full>Full Button</button>
```

## Tamanho de Botões
Adicione o atributo large para fazer um botão maior ou small para torná-lo menor:

``` ts
<button small>Small</button>
<button>Default</button>
<button large>Large</button>
```

## Botões com Ícones
Para adicionar ícones em um botão, adicione um componente de ícone dentro dele:

``` ts
<!-- Float the icon left -->
<button>
  <ion-icon name="home"></ion-icon>
  Left Icon
</button>

<!-- Float the icon right -->
<button>
  Right Icon
  <ion-icon name="home"></ion-icon>
</button>

<!-- Only icon (no text) -->
<button>
  <ion-icon name="home"></ion-icon>
</button>
```

## Botões de Ação Flutuante
Ao adicionar a propriedade fab a um botão irá transformá-lo em um botão de ação flutuante. Este é um botão estilizado com material design que se destina a chamar atenção do usuário a uma ação específica. Botões Fab são posicionados de forma absoluta e seu posicionamento pode ser controlado pela adição de atributos como fab-top e fab-left. Veja a especificação da [API de botões](2e-botao.md) para uma lista completa de atributos.

``` ts
<button fab>FAB</button>
```

## Botões em Componentes
Embora botões possam ser utilizados por conta própria, eles podem facilmente serem utilizados dentro de outros componentes. Por exemplo, os botões podem ser adicionados a um item de lista ou uma barra de navegação.

``` ts
<ion-navbar>
  <ion-buttons start>
    <button>
      <ion-icon name="contact"></ion-icon>
    </button>
  </ion-buttons>

  <ion-buttons end>
    <button>
      <ion-icon name="search"></ion-icon>
    </button>
  </ion-buttons>
</ion-navbar>

<ion-list>
  <ion-item>
    Left Icon Button
    <button outline item-right>
      <ion-icon name="star"></ion-icon>
      Left Icon
    </button>
  </ion-item>
</ion-list>
```

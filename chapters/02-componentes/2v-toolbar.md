Toolbar (Barra de ferramentas)
-------
Uma Barra de Ferramentas é uma barra genérica que pode ser usada em um aplicativo como um cabeçalho (header), sub cabeçalho (sub-header), rodapé (footer) ou mesmo em um sub rodapé(sub-footer). Uma vez que `ion-toobar` é baseada em flexbox, não importa quantas barras de ferramentas você tenha em sua página, podem ser exibidas corretamente e `ion-content` vai a ajustar adequadamente.  

#### Conteúdos
* Uso Básico
* Botões nas Barras de Ferramentas
* Segmentos nas Barras de Ferramentas
* Barra de buscas nas Barras de Ferramentas
* Mudando a cor

### Uso Básico

Adicione a propriedade `position="bottom"` para colocar a Barra de Ferramentas embaixo do conteúdo.

```
<ion-toolbar>
  <ion-title>Toolbar</ion-title>
</ion-toolbar>

<ion-content></ion-content>

<ion-toolbar position="bottom">
  <ion-title>Footer</ion-title>
</ion-toolbar>
```

### Cabeçalho

Um dos melhores usos da Barra de Ferramentas é como cabeçalho.

```
<ion-toolbar primary>
  <ion-buttons start>
    <ion-icon name="content"></ion-icon>
  </ion-buttons>

  <ion-title>Header</ion-title>

  <ion-buttons end>
    <ion-icon name="search"></ion-icon>
  </ion-buttons>

</ion-toolbar>

<ion-content>
  <p>There is a header above me!</p>
</ion-content>
```

### Botões nas Barras de Ferramentas

Botões podem ser adicionados em ambas Barras de Ferramentas dos cabeçalhos e rodapés. Para adicionar um botão em uma Barra de Ferramentas, nós precisamos primeiro adicionar um componente `ion-buttons`. Este componente envolve um ou mais botões, e podem ser dados os atributos `start` ou `end` para controlar a localização dos botões que eles contêm:

```
<ion-toolbar>
  <ion-buttons start>
    <button royal>
      <ion-icon name="search"></ion-icon>
    </button>
  </ion-buttons>
  <ion-title>Send To...</ion-title>
  <ion-buttons end>
    <button royal>
      <ion-icon name="person-add"></ion-icon>
    </button>
  </ion-buttons>
</ion-toolbar>

<ion-content></ion-content>

<ion-toolbar position="bottom">
  <p>Ash, Misty, Brock</p>
  <ion-buttons end>
    <button royal>
      Send
      <ion-icon name="send"></ion-icon>
    </button>
  </ion-buttons>
</ion-toolbar>
```  
### Segmentos nas Barras de Ferramentas

Segmentos são um grande caminho para permitir usuários alterar entre diferentes conjuntos de dados. Use a seguinte marcação para adicionar um segmento para uma Barra de Ferramentas:

```
<ion-toolbar>
  <ion-buttons start>
    <button royal>
      <ion-icon name="search"></ion-icon>
    </button>
  </ion-buttons>
  <ion-title>Send To...</ion-title>
  <ion-buttons end>
    <button royal>
      <ion-icon name="person-add"></ion-icon>
    </button>
  </ion-buttons>
</ion-toolbar>

<ion-content></ion-content>

<ion-toolbar position="bottom">
  <p>Ash, Misty, Brock</p>
  <ion-buttons end>
    <button royal>
      Send
      <ion-icon name="send"></ion-icon>
    </button>
  </ion-buttons>
</ion-toolbar>
```

### Barra de buscas nas Barras de Ferramentas

Outro paradigma comum de design é incluir uma Barra de buscas dentro de suas Barras de Ferramentas.

```
<ion-toolbar primary>
  <ion-searchbar (input)="getItems($event)"></ion-searchbar>
</ion-toolbar>

<ion-content>
  <ion-list>
    <ion-item *ngFor="let item of items">
      {{ item }}
    </ion-item>
  </ion-list>
</ion-content>
```

```
@Component({
  templateUrl: 'search/template.html',
})
class SearchPage {
  constructor() {
    this.initializeItems();
  }

  initializeItems() {
    this.items = [
      'Angular 1.x',
      'Angular 2',
      'ReactJS',
      'EmberJS',
      'Meteor',
      'Typescript',
      'Dart',
      'CoffeeScript'
    ];
  }

  getItems(ev) {
    // Reset items back to all of the items
    this.initializeItems();

    // set val to the value of the searchbar
    var val = ev.target.value;

    // if the value is an empty string don't filter the items
    if (val && val.trim() != '') {
      this.items = this.items.filter((item) => {
        return (item.toLowerCase().indexOf(val.toLowerCase()) > -1);
      })
    }
  }
}
```

### Mudando a cor

Você pode mudar a cor das Barras de Ferramentas mudando as propriedades nos elementos.

```
@Component({
  template: `
    <ion-toolbar primary>
      <ion-title>Toolbar</ion-title>
    </ion-toolbar>


    <ion-toolbar secondary>
      <ion-title>Toolbar</ion-title>
    </ion-toolbar>

    <ion-toolbar danger>
      <ion-title>Toolbar</ion-title>
    </ion-toolbar>


    <ion-toolbar dark>
      <ion-title>Toolbar</ion-title>
    </ion-toolbar>
  `
  })
```

Você pode também mudar a cor das Barras de Ferramentas do mesmo jeito. Isso pode permitir você ter uma cor diferente de Barra de Ferramentas por página em seu aplicativo.

```
<ion-navbar *navbar dark>
  <ion-title>Dark</ion-title>
</ion-navbar>


<ion-navbar *navbar danger>
  <ion-title>Danger</ion-title>
</ion-navbar>

<ion-navbar *navbar secondary>
  <ion-title>Secondary</ion-title>
</ion-navbar>
```

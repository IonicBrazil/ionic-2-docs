# 1.4 Conceitos de Migração

Ionic 2 é construído em cima de Angular 2, que é uma reescrita completa do framework original. Todas as partes do Angular que você conhece ainda estão lá, mas há nova sintaxe e as mudanças estruturais sobre os quais os desenvolvedores precisam estar cientes. Para uma visão geral das mudanças no Angular 2, dê uma olhada em [Aprenda Angular 2](http://learnangular2.com/).

Em Ionic 2, devem se sentir muito familiar com as coisas. Todos os conceitos de Ionic V1 ainda estão no V2, embora eles podem ser ligeiramente diferentes. Você ainda tem visões e controladores como você faz na V1, mas em V2, elas foram fundidas em uma instância.

Veja este exemplo V1.

V1

```
.config(function($stateProvider){
  $stateProvider
  .state('main', {
    url: '/',
    templateUrl: 'templates/main.html',
    controller: 'MainCtrl'
  })
})

.controller('MainCtrl', function(){

})
```

Você pode escrever isso em V2 como este:

```
@Page({
  templateUrl:'main/main.html'
})
export class MainCmp {
  constructor(){

  }
}
```

Outras mudanças, como mudanças de navegação, são muito diferentes, mas por boas razões, como nós prometemos. Agora, você pode tratar componentes como pontos de vista arbitrários e navegar por elas de qualquer jeito que você quiser. Isto torna a navegação muito mais flexível e permite pilhas de navegação muito mais nativa de estilo.

# Migrando do Angular 1

Enquanto Angular 2 requer aplicativos para ser atualização para a mudança de sintaxe, os desenvolvedores podem ser pró-ativo e certificar se o seu aplicativo é atualizável, seguindo as melhores práticas e trabalhar com guia Angular Style de John Papa ou guia Angular Style de Todd Todd Motto. Ambos irão fornecer-lhe os passos que você pode tomar para preparar seu código para a migração.

## ControllerAs Syntax

ControllerAs Syntax é recurso do Angular 1.x aonde ao invés de vocçe ligar dados para **$scope**, você pode ligar para a instância direta do controlador, como alternativa. Isso faz com que a migração de um controlador de  Angular 1.x para uma classe Angular 2 muito mais fácil. É bastante fácil de migrar para controllerAs de um controlador tradicional:

_index.html_

```
<ion-content ng-controller="MainCtrl">
  <ion-item>
    {{data.text}}
  </ion-item>
</ion-content>
```

_app.js_

```
.controller('MainCtrl', function($scope){
  $scope.data ={
    text: 'Hello World'
  }
})
```

Para converter isso em sintaxe **controllerAs**, você só tem que mudar algumas coisas.

_index.html_

```
<ion-content ng-controller="MainCtrl as main">
  <ion-item>
    {{data.text}}
  </ion-item>
</ion-content>
```

_app.js_

```
.controller('MainCtrl', function(){
  this.data ={
    text: 'Hello World'
  }
})
```

## TypeScript

TypeScript é um super conjunto de JavaScript que fornece Classes ES6 e tipo de anotações em seu código. Agora, com a adoção de TypeScript você pode escrever seu código como Classes ES6 que serão fáceis para se deslocar para Ionic 2. A melhor parte é que qualquer JavaScript válido também é TypeScript válido, assim você pode converter o seu pedaço de código por parte. Se você aproveitar o seu controlador anterior, você pode facilmente convertê-lo em uma classe TypeScript como esta.

_app.js_

```
.controller('MainCtrl', function(){
  this.data ={
    text: 'Hello World'
  }
})
```

_app.ts_

```
export class MainCtrl{
  constructor(){
    this.data ={
      text: 'Hello World'
    }
  }
}
```

## Estrutura do projeto

Com o Angular 1, era uma prática manter todo o seu JavaScript juntos e separados de seus modelos. Desde Ionic 2 e Angular 2 estará se movendo para uma configuração baseada em componente, você pode organizar o seu projeto para ajudar mentalmente a aplicar esse conceito. Assim, um projeto cujo diretório parecerá com isso ...

```
|-www/
|
|--js/
|--|-app.js
|--|-HomeCtrl.js
|--|-DetailCtrl.js
|
|--templates/
|--|-Home.html
|--|-Detail.html
|
|-index.html
```

poderia começar a ser reorganizada para se parecer com isto:

```
|-www/
|
|--Home/
|--|-HomeCtrl.js
|--|-Home.html
|
|--Detail/
|--|-DetailCtrl.js
|--|-Detail.html
|
|-index.html
|-app.js
```

Organizar o seu projeto como este pode ajudá-lo na mentalidade de que cada um de seu aplicativo views/states são um componente, com um modelo e um controlador.

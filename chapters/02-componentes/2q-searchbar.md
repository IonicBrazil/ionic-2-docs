# Searchbar(Barra de pesquisa)

Uma Searchbar liga-se a um modelo, e emite um evento de input quando o modelo é alterado.

###Uso básico Usage
[Demo Source](https://github.com/driftyco/ionic-preview-app/tree/master/app/pages/searchbars)

	<ion-searchbar (ionInput)="getItems($event)"></ion-searchbar>
	<ion-list>
	  <ion-item *ngFor="let item of items">
	    {{ item }}
	  </ion-item>
	</ion-list>
	
Observe que neste exemplo, a função getItems() é chamada quando é alterado o input, que atualiza as cidades que são exibidas. Embora este exemplo filtra a lista baseada no input de pesquisa, o Searchbar pode ser usado em muitos cenários diferentes:

	@Component({
	  templateUrl: 'search/template.html',
	})
	class SearchPage {
	  constructor() {
	    this.searchQuery = '';
	    this.initializeItems();
	  }
	
	  initializeItems() {
	    this.items = [
	      'Amsterdam',
	      'Bogota',
	      ...
	    ];
	  }
	
	  getItems(ev) {
	  	 
	   //Redefinida itens para todos os itens
	    this.initializeItems();
	
	   //conjunto de val para o valor do searchbar
	    let val = ev.target.value;
	
	   // if the value is an empty string don't filter the items
	      if (val && val.trim() != '') {
	        this.items = this.items.filter((item) => {
	          return (item.toLowerCase().indexOf(val.toLowerCase()) > -1);
	        })
	      }
	  }
	}

O Searchbar leva um número de opções de configuração do elemento <ion-searchbar>, como cancelButtonText e hideCancelButton. Confira a referência [Searchbar API](http://ionicframework.com/docs/v2/api/components/searchbar/Searchbar/) para obter mais informações sobre como configurar uma Searchbar.
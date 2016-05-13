Modals

Modals deslizam na tela para exibir uma interface do usuário temporário, muitas vezes usado para páginas de login ou signup, composição de mensagens e seleção de opção.

Uso Básico

Em seguida, precisamos criar a classe que controlará o nosso modal. Vamos importar `Modal`, `NavController` e `ViewController`:

	import {Modal, NavController, ViewController} from 'ionic-angular';

Em seguida, vamos criar nosso modal e adicionar seu template:

	@Page({
	  template:`
	  <ion-content padding>
	    <h2>I'm a modal!</h2>
	    <button (click)="close()">Close</button>
	  </ion-content>`
	})
	class MyModal {
	  constructor(viewCtrl: ViewController) {
	    this.viewCtrl = viewCtrl;
	  }
	  
	  close() {
	    this.viewCtrl.dismiss();
	  }
	}

Finalmente, vamos adicionar o código que irá abrir nosso Modal:

	import {Modal, NavController} from 'ionic/ionic'
	class MyPage {
	  constructor(nav: NavController){
	    this.nav = nav;
	  }
	  showModal() {
	    let modal = Modal.create(MyModal);
	    this.nav.present(modal)
	  }
	}
	
A função `Modal.create()` também pode receber um objeto em um segundo argumento que será passado para o modal. Consulte o [Modal API docs](http://ionicframework.com/docs/v2/api/components/modal/Modal/) para obter mais informações.
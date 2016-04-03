Alerts (Alertas)
-----------

Alertas são uma ótima maneira de oferecer ao usuário a capacidade de escolher uma ação específica ou uma lista de ações. Alerts também podem fornecer ao usuário informações importantes, ou obrigá-los a tomar uma decisão (ou várias decisões).
	   
Do ponto de vista da UI(interface do usuário) , você pode pensar em Alerts como um tipo de modal "flutuante", que abrange apenas uma parte da tela.
Isto significa que, alerts só devem ser usados para ações rápidas, como verificação de senha, notificações de aplicativos pequenos, ou opções rápidas. Para uso de fluxos mais profundos, devem ser reservadas para Modais em tela cheia.
 	   
Alerts são bastante flexíveis e podem ser facilmente personalizados. Confira a documentação da API para obter mais informações.

Contents    
Basic Alerts    
Prompt Alerts    
Confirmation Alerts    
Radio Alerts    
Checkbox Alerts    


### Uso Básico

Alerts básicos, são geralmente usados ​​para notificar o usuário sobre novas informações (uma mudança no aplicativo ou um novo recurso), uma situação de urgência que exiga confirmação, ou como uma confirmação ao usuário que uma ação foi bem-sucedida ou não.

     doAlert() {
       let alert = Alert.create({
         title: 'Amigo Novo!',
         subTitle: 'Seu amigo, Obi Wan Kenobi, apenas aceitou o seu pedido de amizade!',
      	   buttons: ['Ok']
       });
     this.nav.present(alert);
    }

    
### Prompt Alerts (Alertas de prompt)


Prompts oferecem aos usuários uma maneira de dados ou informações de entrada. Por exemplo, muitas vezes Alerts Prompt será utilizado para pedir a confirmação do usuário e senha, como um meio de segurança antes de avançar no fluxo UX(User Experience) de um aplicativo.

	let prompt = Alert.create({
      title: 'Login',
      message: "Digite um nome para este novo álbum, que você está tão interessado em adicionar",
      inputs: [
        {
          name: 'title',
          placeholder: 'Title'
        },
      ],
      buttons: [
        {
          text: 'Cancel',
          handler: data => {
            console.log('Cancel clicked');
          }
        },
        {
          text: 'Save',
          handler: data => {
            console.log('Saved clicked');
          }
        }
      ]
    });

### Confirmation Alerts (Confirmação Alertas) 

Confirmação de Alertas são usados ​​quando é necessário que o usuário confirme expressamente uma escolha particular antes de ir adiante no aplicativo. Um exemplo comum do confirmation alert, é verificando se um usuário quer excluir ou remover um contato de sua lista de endereços.

	 let confirm = Alert.create({
      title: 'Utilize este sabre de luz?',
      message: 'Você concorda em usar este sabre de luz para fazer o bem através da galáxia intergaláctica?',
      buttons: [
        {
          text: 'Disagree',
          handler: () => {
            console.log('Disagree clicked');
          }
        },
        {
          text: 'Agree',
          handler: () => {
            console.log('Agree clicked');
          }
        }
      ]
    });


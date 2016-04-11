# Alertas

Alertas são uma ótima forma de oferecer ao usuário a habilidade de escolher uma ação específica ou uma lista de ações. Eles também podem prover ao usuário importantes informações ou requerer dele que tome uma decisão (ou várias decisões).

De uma perspectiva de interface de usuário, você pode imaginar os alertas como um tipo de modal flutuante, que cobre apenas uma parte da tela. Isso significa que alertas apenas podem ser usados para rápidas ações como verificaçao de senhas, pequenas notificações ou ações rápidas. O fluxo mais complexo do usuário deve ser reservado para os [modais](/chapters/02-componentes/) de tela cheia.

Alertas são bastante flexíveis, e podem ser customizados facilmente. Dê uma olhada em [API docs](/chapters/07-api/) para mais informações.

* Contents
* Basic Alerts
* Prompt Alerts
* Confirmation Alerts
* Radio Alerts
* Checkbox Alerts

## Utilização básica:

Alertas básicos são geralmente usados para notificar o usuário sobre novas informações (uma modificação no app, uma nova funcionalidade), uma situação urgente que requer reconhecimento, ou como uma confirmação para o usuário que uma ação teve sucesso ou não.

``` ts
doAlert() {
  let alert = Alert.create({
    title: 'New Friend!',
    subTitle: 'Your friend, Obi wan Kenobi, just accepted your friend request!',
    buttons: ['Ok']
  });
  this.nav.present(alert);
}
```

## Prompt Alerta

Prompt Alerta oferece ao usuário uma forma de fazer entrada de dados ou informações. Por exemplo, muitas vezes o Prompt Alerta será usado para perguntar ao usuário por confirmação de sua senha como uma forma de segurança antes de continuar seguindo o fluxo do app.


``` ts
let prompt = Alert.create({
  title: 'Login',
  message: "Enter a name for this new album you're so keen on adding",
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
```

## Alertas de confirmação

Alertas de Confirmação são usados quando é requerido explicitamente que o usuário confirme uma certa escolha depois do processamento ser feito no app. Um exemplo comum desse tipo de alerta é a checagem se o usuário tem certeza se deseja apagar ou remover um contato da sua lista de contatos.

``` ts
let confirm = Alert.create({
  title: 'Use this lightsaber?',
  message: 'Do you agree to use this lightsaber to do good across the intergalactic galaxy?',
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
```

## Radio Alerta

Radio Alerta é outro tipo simples de Alerta de Confirmação, porém use esse componente quando quizer oferecer várias escolhas.  Ele oferece ao usuário uma lista de opções à serem escolhidas, mas permite apenas uma escolha final, antes de continuar seguindo em frente.

``` ts
doRadio() {
  let alert = Alert.create();
  alert.setTitle('Lightsaber color');

  alert.addInput({
    type: 'radio',
    label: 'Blue',
    value: 'blue',
    checked: true
  });

  alert.addButton('Cancel');
  alert.addButton({
    text: 'Ok',
    handler: data => {
      this.testRadioOpen = false;
      this.testRadioResult = data;
    }
  });
```

## Checkbox Alerta

Checkbox Alerta é um outro tipo de Alerta de Confirmação, mas use o componente de Checkbox para oferecer várias escolhas. Ele oferece ao usuário uma lista de opções que podem ser escolhidas.

``` ts
doCheckbox() {
  let alert = Alert.create();
  alert.setTitle('Which planets have you visited?');

  alert.addInput({
    type: 'checkbox',
    label: 'Alderaan',
    value: 'value1',
    checked: true
  });

  alert.addInput({
    type: 'checkbox',
    label: 'Bespin',
    value: 'value2'
  });

  alert.addButton('Cancel');
  alert.addButton({
    text: 'Okay',
    handler: data => {
      console.log('Checkbox data:', data);
      this.testCheckboxOpen = false;
      this.testCheckboxResult = data;
    }
  });
}
```

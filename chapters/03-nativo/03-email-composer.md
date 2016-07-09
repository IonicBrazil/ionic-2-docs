# Email Composer

`$ ionic plugin add cordova-plugin-email-composer`

Repositório: [https://github.com/katzer/cordova-plugin-email-composer.git](https://github.com/katzer/cordova-plugin-email-composer.git)

Requer o plugin Cordova: `cordova-plugin-email-composer`. Para maiores informações, por favor, veja a documentação do plugin [Email Composer](https://github.com/katzer/cordova-plugin-email-composer).

IMPORTANTE: Este plugin está enfrentando problemas com as últimas versões do Cordova. Use por sua conta e risco. Suas funcionalidades não são garantidas. Por favor, fique atento para uma versão mais estável.


## Plataformas Suportadas

- Android
- iOS
- Windows Phone 8


## Uso

```js  
import {EmailComposer} from 'ionic-native';


EmailComposer.isAvailable().then((available) =>{
 if(available) {
   //Agora sabemos que podemos enviar
 }
});

let email = {
  to: 'max@mustermann.de',
  cc: 'erika@mustermann.de',
  bcc: ['john@doe.com', 'jane@doe.com'],
  attachments: [
    'file://img/logo.png',
    'res://icon.png',
    'base64:icon.png//iVBORw0KGgoAAAANSUhEUg...',
    'file://README.pdf'
  ],
  subject: 'Ícones Cordova',
  body: 'Como você está? Saudações de Leipzig',
  isHtml: true
};

// Envia uma mensagem de texto usando as opções padrão
EmailComposer.open(email);
```


## Membros Estáticos

### `isAvailable(app)`

Verifica se o envio de emails é suportado pelo dispositivo.

Pârametro | Tipo  | Detalhes
----------|-------|---------
app|`string`| Um código de aplicativo ou URL

Retorna: `Promisse<boolean>` resolve se disponível, rejeita se indisponível.


### `addAlias(alias, packageName)`

Verifica se o envio de emails é suportado pelo dispositivo.

Pârametro | Tipo  | Detalhes
----------|-------|---------
alias|`string`| O nome do *alias*
packageName|`string`| O nome do pacote


### `open(email, scope)`

Exibe o email composer pré-preenchido com os dados.

Pârametro | Tipo  | Detalhes
----------|-------|---------
email|`string`| Email
scope|`string`| Um escopo opcional para a promise

Retorna: `Promisse<any>` a promisse resolve quando o Emal Composer for aberto.

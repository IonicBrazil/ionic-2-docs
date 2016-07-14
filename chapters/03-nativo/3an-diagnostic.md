ActionSheet
===========

```
$ cordova plugin add cordova-plugin-actionsheet
```

Repositório: [https://github.com/EddyVerbruggen/cordova-plugin-actionsheet](https://github.com/EddyVerbruggen/cordova-plugin-actionsheet)

O plugin ActionSheet exibe uma lista de opções que o usuário pode escolher. 

Esse plugin tem como dependência: ```cordova-plugin-actionsheet```. Para mais informações, por favor veja a [documentação do plugin ActionSheet](https://github.com/EddyVerbruggen/cordova-plugin-actionsheet).

Platafomas suportadas
-----
- Android
- iOS
- Windows Phone 8

Uso
---

``` javascript
import {ActionSheet} from 'ionic-native';

let buttonLabels = ['Share via Facebook', 'Share via Twitter'];
ActionSheet.show({
  'title': 'What do you want with this image?',
  'buttonLabels': buttonLabels,
  'addCancelButtonWithLabel': 'Cancel',
  'addDestructiveButtonWithLabel' : 'Delete'
}).then(buttonIndex => {
  console.log('Button pressed: ' + buttonLabels[buttonIndex - 1]);
});
```

Métodos estáticos
-----------------

``` show(Options) ```

Mostra o ActionSheet. As opções do ActionSheet é um objeto com as seguintes propriedades.

| Opção                         | Tipo      | Descrição                                    |
|-------------------------------|-----------|----------------------------------------------|
| title                         |`string`   | O título para o actionsheet                  |
| buttonLabels                  |`string[]` | Labels para os botões. Usa o índice 'x'      |
| androidTheme                  |`number`   | Tema para ser usado no Android               |
| androidEnableCancelButton     |`boolean`  | Habilita o botão de cancelar no Android      |
| winphoneEnableCancelButton    |`boolean`  | Habilita o botão de cancelar no Windows Phone|
| addCancelButtonWithLabel      |`string`   | Adiciona um botão de cancelar com texto      |
| addDestructiveButtonWithLabel |`string`   | Adiciona um botão destrutivo com texto       |
| position                      |`number[]` | No iPad, define a posição X,Y				   |

| Parametro                     | Tipo         | Detalhes                                     |
|-------------------------------|--------------|----------------------------------------------|
| Options                       |```options``` | Veja tabela acima                  		  |

*Retorna:* ```Promise``` 

Retorna uma Promise que retorna o indíce do botão pressionado (o índice começa em 1, então 1, 2, 3, etc.).

``` hide() ```

Esconde o ActionSheet.
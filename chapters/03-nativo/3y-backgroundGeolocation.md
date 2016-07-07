BackgroundGeolocation
===========

```
$ ionic plugin add cordova-plugin-mauron85-background-geolocation
```

Repositório: [https://github.com/mauron85/cordova-plugin-background-geolocation](https://github.com/mauron85/cordova-plugin-background-geolocation)

O plugin nos proporciona a geolocalização em primeiro plano ou em segundo plano(*background*) com economia de bateria ao utilizar "monitoramento de região circular" e "pausa de detecção".

Para mais informações, por favor veja a [documentação do plugin](https://github.com/mauron85/cordova-plugin-background-geolocation).

Platafomas suportadas
-----
- Android
- iOS
- Windows Phone 8

Uso
---

``` javascript
import {BackgroundGeolocation} from 'ionic-native';



// Quando o dispositivo estiver pronto :
platform.ready().then(() => {

    // BackgroundGeolocation é altamente configuravel. Veja as opcões espceificas de configuração da plataforma
    let config = {
            desiredAccuracy: 10,
            stationaryRadius: 20,
            distanceFilter: 30,
            debug: true, //  habilite para ouvir sons referentes ao ciclo de vida do background-geolocation.
            stopOnTerminate: false, // habilite para limpar as configurações de localizaçao em segundo plano quando o app for fechado.
    };

    BackgroundGeolocation.configure(config)
       .then((location) => {
            console.log('[js] BackgroundGeolocation callback:  ' + location.latitude + ',' + location.longitude);

            // IMPORTANTE:  Você precisa executar o metodo "finish" aqui para informar o plugin nativo de que você terminou
            // e a tarefa em background pode ser concluída  You must do this regardless if your HTTP request is successful or not.
            // IF YOU DON'T, ios will CRASH YOUR APP for spending too much time in the background.
            BackgroundGeolocation.finish(); // FOR IOS ONLY
        })
       .catch((error) => {
            console.log('BackgroundGeolocation error');
        });

    // Turn ON the background-geolocation system.  The user will be tracked whenever they suspend the app.
    BackgroundGeolocation.start();
}

// If you wish to turn OFF background-tracking, call the #stop method.
BackgroundGeolocation.stop();
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

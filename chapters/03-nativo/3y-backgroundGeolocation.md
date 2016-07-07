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

    // BackgroundGeolocation é altamente configurável. Veja as opcões específicas de configuração da plataforma
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
            // e a tarefa em background pode ser concluída. Você precisa fazer isso independentemente do sucesso da sua requisição HTTP.
            // SE VOCÊ NÃO FIZER, ios vai FINALIZAR SUA APLICAÇÃO(CRASH) por ficar muito tempo em segundo plano. 
            BackgroundGeolocation.finish(); // SOMENTE IOS
        })
       .catch((error) => {
            console.log('BackgroundGeolocation error');
        });

    // LIGA o sistema de geolocalização em segundo plano. O usuario vai ser rastreado sempre que ele suspender a aplicação.
    BackgroundGeolocation.start();
}

// Se você quiser DESLIGAR o sistema de localização em segundo plano, chame o metodo "stop".
BackgroundGeolocation.stop();
```

Métodos estáticos
-----------------

``` configure() ```

Configura o plugin. O callback de sucesso vai ser chamado com um argumento - Objeto de localização, que tenta imitar a interface de coordenadas do w3c. Veja mais em [http://dev.w3.org/geo/api/spec-source.html#coordinates_interface](http://dev.w3.org/geo/api/spec-source.html#coordinates_interface) Callback executado toda vez que a geolocalização é salva em segundo plano.

Callback de falha a ser executado toda vez que ocorrer um erro na geolocalização.

Options é um objeto json do tipo Config.

``` start() ```

LIGA o sistema de geolocalização em segundo plano. O usuario vai ser rastreado sempre que ele suspender a aplicação.

``` stop() ```

DESLIGA o sistema de geolocalização em segundo plano.

``` finish() ```

Informa o plugin nativo de que você terminou e a tarefa em background pode ser concluída. OBS: Somente iOS e WP.

``` changePace() ```

Força o plugin a entrar no modo "em movimento" ou "fixo". OBS: Somente iOS e WP.

``` setConfig() ```

Define as configurações.

``` getStationaryLocation() ```

Retorna a stationaryLocation se disponivel. retorna null se não estiver. OBS: Somente iOS e WP.

``` onStationary() ```

Esconde o ActionSheet.

``` isLocationEnabled() ```

Verifica se a localização está habilitada no dispositivo.

Returns: Promise<number> Retorna uma promise com um argumento do tipo int com valores 0, 1 (true). OBS: Somente ANDROID.

``` showLocationSettings() ```

Mostra as configurações de localização do dispositivo.

``` watchLocationMode() ```

Esconde o ActionSheet.

``` stopWatchingLocationMode() ```

Para de olhar para mudanças nos modos de localização. OBS: Somente ANDROID.

``` getLocations() ```

Esconde o ActionSheet.

``` deleteLocation() ```

Deleta a localização salva passando o locationId. OBS: Somente ANDROID

``` deleteAllLocations() ```

Deleta todas as localizações salvas. OBS: Somente ANDROID

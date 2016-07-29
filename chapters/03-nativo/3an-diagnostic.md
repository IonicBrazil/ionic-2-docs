Diagnostic
===========

```
$ ionic plugin add cordova.plugins.diagnostic
```

Repositório: [https://github.com/dpa99c/cordova-diagnostic-plugin](https://github.com/dpa99c/cordova-diagnostic-plugin)


Métodos estáticos
-----------------

``` isLocationEnabled() ```

Verifica se o app está apto a acessar a localização do dispositivo.

``` isWifiEnabled() ```

Verifica se o Wifi está conectado/habilitado. No iOS retorna true se o dispositivo está conectado a uma rede via WiFi. No Android e no Windows 10 Mobile retorna true se o WiFi estiver habilitado nas configurações. No Android é necessário permissão.
<uses-permission android:name="android.permission.ACCESS_WIFI_STATE" />

``` isCameraEnabled() ```

Verifica se o dispositivo tem uma câmera. No Android retorna true se o dispositivo tem uma câmera. No iOS retorna true se o dispositivo tem uma câmera e se a aplicação pode acessa-la. No Windows 10 Mobile returna true se o dispositivo tem uma câmera e a aplicação tem autorização para acessa-la.

``` isBluetoothEnabled() ```

Verifica se o dispositivo tem capacidade Bluetooth e se o mesmo está ligado (funciona da mesma maneira no Android, iOS e Windows 10 Mobile). No Android é necessario permissão.

``` requestLocationAuthorization() ```

Retorna o status de autorização de localização para a aplicação. Nota para Android: pretendido para Android 6 / API 23 e mais novos. Realizar uma chamada no Android 5 / API 22 ou menor vai sempre retornar GRANTED status como uma permissão garantida na hora da instalação.

modo - (somente-iOS / opcional) modo de autorização da localização: “always” ou “when_in_use”. Se não for especificado, o padrão para “when_in_use”.


``` hide() ```

Esconde o ActionSheet.

``` hide() ```

Esconde o ActionSheet.

``` hide() ```

Esconde o ActionSheet.

``` hide() ```

Esconde o ActionSheet.

``` hide() ```

Esconde o ActionSheet.

``` hide() ```

Esconde o ActionSheet.

``` hide() ```

Esconde o ActionSheet.

``` hide() ```

Esconde o ActionSheet.

``` hide() ```

Esconde o ActionSheet.

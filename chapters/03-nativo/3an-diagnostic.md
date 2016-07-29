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


``` isLocationAuthorized() ```

Verifica se a aplicação está autorizada a utilizar a localização. Nota para Android: pretendido para Android 6 / API 23 e mais novos. Realizar uma chamada no Android 5 / API 22 ou menor vai sempre retornar GRANTED status como uma permissão garantida na hora da instalação. 

``` isCameraPresent() ```

Verifica se existe uma câmera no dispositivo.

``` isCameraAuthorized() ```

Verifica se a aplicação tem autorização para utilizar a câmera. Nota para Android: pretendido para Android 6 / API 23 e mais novos. Realizar uma chamada no Android 5 / API 22 ou menor vai sempre retornar GRANTED status como uma permissão garantida na hora da instalação. 

``` isGpsLocationEnabled() ```

Verifica se a localização está no modo de alta precisão via GPS. Retorna true se o modo localização estiver habilitado e estiver definido como: Somente dispositivo = somente o GPS (alta precisão) - Alta Precisão = GPS, triangulação de rede e rede WiFi IDs (alta e baixa precisão).   

``` isNetworkLocationEnabled() ```

Checks if location mode is set to return low-accuracy locations from network triangulation/WiFi access points. Returns true if Location mode is enabled and is set to either: - Battery saving = network triangulation and Wifi network IDs (low accuracy) - High accuracy = GPS hardware, network triangulation and Wifi network IDs (high and low accuracy)

``` isRemoteNotificationsEnabled() ```

Checks if remote (push) notifications are enabled. On iOS 8+, returns true if app is registered for remote notifications AND “Allow Notifications” switch is ON AND alert style is not set to “None” (i.e. “Banners” or “Alerts”). On iOS <=7, returns true if app is registered for remote notifications AND alert style is not set to “None” (i.e. “Banners” or “Alerts”) - same as isRegisteredForRemoteNotifications().

``` isRegisteredForRemoteNotifications() ```

Indicates if the app is registered for remote (push) notifications on the device. On iOS 8+, returns true if the app is registered for remote notifications and received its device token, or false if registration has not occurred, has failed, or has been denied by the user. Note that user preferences for notifications in the Settings app will not affect this. On iOS <=7, returns true if app is registered for remote notifications AND alert style is not set to “None” (i.e. “Banners” or “Alerts”) - same as isRemoteNotificationsEnabled().



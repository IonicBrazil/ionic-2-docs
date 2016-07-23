# Hotspot

```shell
$ ionic plugin add cordova-plugin-hotspot
```

Repo: [https://github.com/hypery2k/cordova-hotspot-plugin](https://github.com/hypery2k/cordova-hotspot-plugin)

## Plataformas suportadas

- Android

## Uso

```js
import {Hotspot, Network} from 'ionic-native';

...
    Hotspot.scanWifi().then((networks: Array<Network>) => {
        console.log(networks);
    });
...
```

## Membros estáticos

`isAvailable()`

`toggleWifi()`

---

### `createHotspot(SSID, modo, senha)`

Configura e inicia um hotspot com um SSID e senha.

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   SSID	|   `string`	| SSID do seu novo ponto de acesso	|
|   modo	|   `string`	| Modo de criptografia (Open, WEP, WPA, WPA_PSK)	|
|   senha	|   `string`	| Senha do novo ponto de acesso	|

**_Retorna_**: `Promise<void>` Promise para chamar quando o hotspot é iniciado, ou rejeitado em uma falha.

---

### `startHotspot()`

Inicia o ponto de acesso

**_Retorna_**: `Promise<boolean>` `true` se o hotspot for iniciado

---

### `configureHotspot(SSID, modo, senha)`

Configura um hotspot com um SSID e senha.

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   SSID	|   `string`	| SSID do seu novo ponto de acesso	|
|   modo	|   `string`	| Modo de criptografia (Open, WEP, WPA, WPA_PSK)	|
|   senha	|   `string`	| Senha do novo ponto de acesso	|

**_Retorna_**: `Promise<void>` Promise para chamar quando o hotspot é iniciado, ou rejeitado em uma falha.

---

### `stopHotspot()`

Para o ponto de acesso

**_Retorna_**: `Promise<boolean>` Promise para desligar o hotspot, `true` no sucesso e `false` para falha

---

### `isHotspotEnabled()`

Para o ponto de acesso

**_Retorna_**: `Promise<boolean>` Promise para desligar o hotspot, `true` no sucesso e `false` para falha

---

`getAllHotspotDevices()`

---

### `connectToWifi(SSID, senha)`

Conecta a uma rede wifi

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   SSID	|   `string`	| SSID da rede wifi	|
|   senha	|   `string`	| Senha da rede wifi |

**_Retorna_**: `Promise<void>` Promise que a conexão com a rede foi um sucesso, rejeitada se falhou.

---

### `connectToWifiAuthEncrypt(SSID, senha, autenticação, criptografia)`

Conecta a uma rede wifi

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   SSID	|   `string`	| SSID da rede wifi	|
|   senha	|   `string`	| Senha da rede wifi |
|   autenticação	|   `string`	| Modo de autenticação (LEAP, SHARED, OPEN) |
|   criptografia	|   `string[]`	| Modo de criptografia para usar (CCMP, TKIP, WEP104, WEP40) |

**_Retorna_**: `Promise<void>` Promise que a conexão com a rede foi um sucesso, rejeitada se falhou.

---

### `addWifiNetwork(SSID, modo, senha)`

Adiciona uma rede wifi

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   SSID	|   `string`	| SSID da rede wifi	|
|   modo	|   `string`	| Modo de autenticação (Aberta, WEP, WPA, WPA_PSK) |
|   senha	|   `string`	| Senha da rede wifi |

**_Retorna_**: `Promise<void>` Promise que a adição da conexão foi um sucesso, rejeitada se falhou.

---

### `removeWifiNetwork(SSID)`

Remove uma rede wifi

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   SSID	|   `string`	| SSID da rede wifi	|

**_Retorna_**: `Promise<void>` Promise que a remoção da conexão foi um sucesso, rejeitada se falhou.

---

`isConnectedToInternet()`

Nenhuma descrição no momento

---

`isConnectedToInternetViaWifi()`

Nenhuma descrição no momento

---

`isWifiOn()`

Nenhuma descrição no momento

---

`isWifiSupported()`

Nenhuma descrição no momento

---

`isWifiDirectSupported()`

Nenhuma descrição no momento

---

`scanWifi()`

Nenhuma descrição no momento

---

`scanWifiByLevel()`

Nenhuma descrição no momento

---

`startWifiPeriodicallyScan()`

Nenhuma descrição no momento

---

`stopWifiPeriodicallyScan()`

Nenhuma descrição no momento

---

`getNetConfig()`

Nenhuma descrição no momento

---

`getConnectionInfo()`

Nenhuma descrição no momento

---

`pingHost()`

Nenhuma descrição no momento

---

### `getMacAddressOfHost(ip)`

Obtem o endereço MAC associado a um IP de um arquivo ARP

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   IP	|   `string`	| Endereço de IP que você deseja obter o MAC	|

**_Retorna_**: `Promise<string>` Promise do MAC address

---

### `isDnsLive(ip)`

Checa se um endereço de IP está ativo usando o DNS

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   IP	|   `string`	| Endereço que você deseja testar	|

**_Retorna_**: `Promise<boolean>` Promise para quando o endereço de IP está ativo (`true`/`false`)

---

### `isPortLive(SSID)`

Checa se um IP está ativo usando socket e porta

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   IP	|   `string`	| Endereço que você deseja testar	|

**_Retorna_**: `Promise<boolean>` Promise para quando o endereço de IP está ativo (`true`/`false`)

---

### `isRooted(SSID)`

Verifica se o aparelho está roteado.

**_Retorna_**: `Promise<boolean>` Promise para quando o aparelho estiver roteado.
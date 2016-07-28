# AdbMob  

`$ ionic plugin add cordova-plugin-admobpro`

Repositório: [https://github.com/floatinghotpot/cordova-admob-pro](https://github.com/floatinghotpot/cordova-admob-pro)


Plugin para Google Ads, incluindo AdMob/DFP (clique duplo para a editora) e mediações para outras redes Ad.


## Plataformas Suportadas

- Android
- iOS
- Windows Phone 8


## Utilização

Por favor, referencie o repositório do plugin original para detalhes de sua utilização.


## Membros Estáticos

### `createBanner(adIdOrOptions)`

Pârametro | Tipo  | Detalhes
----------|-------|---------
adIdOrOptions||


### `removeBanner()`


### `showBanner(position)`

Pârametro | Tipo  | Detalhes
----------|-------|---------
position||


### `showBannerAtXY(x, y)`

Pârametro | Tipo  | Detalhes
----------|-------|---------
x||
y||


### `hideBanner()`


### `prepareInterstitial(adIdOrOptions)`

Pârametro | Tipo  | Detalhes
----------|-------|---------
adIdOrOptions||


### `showInterstitial()`

Mostrar intersticial


### `isInterstitialReady()`


### `prepareRewardVideoAd(adIdOrOptions)`

Prepara um anúncio em vídeo

Pârametro | Tipo  | Detalhes
----------|-------|---------
adIdOrOptions||


### `showRewardVideoAd()`

Mostra um anúncio em vídeo

Pârametro | Tipo  | Detalhes
----------|-------|---------
adIdOrOptions||


### `setOptions(options)`

Define os valores para configuração e segmentação.

Pârametro | Tipo  | Detalhes
----------|-------|---------
options|| Retorna uma promise que irá resolver se as opções são definidas com sucesso


### `getAdSettings()`

Obtêm as definições de anúncios do usuário

Retorna: `Promise<any>` retorna uma promisse que resolve as configurações de anúncios.


### `onBannerFailedToReceive()`

### `onBannerReceive()`

### `onBannerPresent()`

### `onBannerLeaveApp()`

### `onBannerDismiss()`

### `onInterstitialFailedToReceive()`

### `onInterstitialReceive()`

### `onInterstitialPresent()`

### `onInterstitialLeaveApp()`

### `onInterstitialDismiss()`

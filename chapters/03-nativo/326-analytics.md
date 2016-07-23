# Google Analytics

```shell
$ ionic plugin add cordova-plugin-google-analytics
```

Repo: [https://github.com/danwilson/google-analytics-plugin](https://github.com/danwilson/google-analytics-plugin)

Este plugin se conecta ao Universal Analytics SDK Prerequisites nativos do Google:

- Um projeto Cordova 3.0+ para iOS e/ou Android
- Uma propriedade para apps mobile através do console de administração do Google Analytics
- (Android) Google Play Services SDK instalado via [Android SDK Manager](https://developer.android.com/sdk/installing/adding-packages.html)

## Plataformas suportadas

- Android
- iOS

## Membros estáticos

### `startTrackerWithId(id)`

Na sua handler 'deviceready', identifique seu tracker do analytics. [https://developers.google.com/analytics/devguides/collection/analyticsjs/](https://developers.google.com/analytics/devguides/collection/analyticsjs/)

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   id	|   `string`	|   A sua propriedade "Mobile App" do Google Analytics	|

---

### `trackView(titulo)`

Acompanha uma tela. [https://developers.google.com/analytics/devguides/collection/analyticsjs/screens](https://developers.google.com/analytics/devguides/collection/analyticsjs/screens)

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   titulo	|   `string`	|   Título da tela	|

---

### `trackEvent(categoria, ação, label, valor)`

Acompanha um evento. [https://developers.google.com/analytics/devguides/collection/analyticsjs/events](https://developers.google.com/analytics/devguides/collection/analyticsjs/events)

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   categoria	|   `string`	|   Nenhum adicionado ainda	|
|   ação	|   `string`	|   Nenhum adicionado ainda	|
|   label	|   `string`	|   Nenhum adicionado ainda	|
|   valor	|   `number`	|   Nenhum adicionado ainda	|


---

### `trackException(descrição, fatal)`

Acompanha uma exceção ou erro de sistema.

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   descrição	|   `string`	|   Nenhum adicionado ainda	|
|   fatal	|   `boolean`	|   Nenhum adicionado ainda	|

---

### `trackTiming(categoria, intervaloEmMilisegundos, variável, label)`

Acompanha o User Timming (Velocidade do app).

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   categoria	|   `string`	|   Nenhum adicionado ainda	|
|   intervaloEmMilisegundos	|   `number`	|   Nenhum adicionado ainda	|
|   variável	|   `string`	|   Nenhum adicionado ainda	|
|   label	|   `string`	|   Nenhum adicionado ainda	|

---

### `addTransaction(id, afiliação, receita, taxa, frete, códigoMoeda)`

Adiciona uma transação (E-commerce) [https://developers.google.com/analytics/devguides/collection/analyticsjs/ecommerce#addTrans](https://developers.google.com/analytics/devguides/collection/analyticsjs/ecommerce#addTrans)

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   id	|   `string`	|   Nenhum adicionado ainda	|
|   afiliação	|   `string`	|   Nenhum adicionado ainda	|
|   receita	|   `number`	|   Nenhum adicionado ainda	|
|   taxa	|   `number`	|   Nenhum adicionado ainda	|
|   frete	|   `number`	|   Nenhum adicionado ainda	|
|   códigoMoeda	|   `string`	|   Nenhum adicionado ainda	|

---

### `addTransactionItem(id, nome, sku, categoria, preço, quantidade, códigoMoeda)`

Adiciona um item a uma transação (E-Commerce) [https://developers.google.com/analytics/devguides/collection/analyticsjs/ecommerce#addItem](https://developers.google.com/analytics/devguides/collection/analyticsjs/ecommerce#addItem)

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   id	|   `string`	|   Nenhum adicionado ainda	|
|   nome	|   `string`	|   Nenhum adicionado ainda	|
|   sku	|   `string`	|   Nenhum adicionado ainda	|
|   categoria	|   `string`	|   Nenhum adicionado ainda	|
|   preço	|   `number`	|   Nenhum adicionado ainda	|
|   quantidade	|   `number`	|   Nenhum adicionado ainda	|
|   códigoMoeda	|   `string`	|   Nenhum adicionado ainda	|

---

### `addCustomDimension(chave, valor)`

Adiciona uma dimensão personalizada [https://developers.google.com/analytics/devguides/platform/customdimsmets](https://developers.google.com/analytics/devguides/platform/customdimsmets)

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   chave	|   `string`	|   Nenhum adicionado ainda	|
|   valor	|   `string`	|   Nenhum adicionado ainda	|

---

### `setUserId(id)`

Seta um id de usuário [https://developers.google.com/analytics/devguides/collection/analyticsjs/user-id](https://developers.google.com/analytics/devguides/collection/analyticsjs/user-id)

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   chave	|   `string`	|  ID do usuário	|

---

### `debugMode()`

Ativa o log de debug.

---

### `enableUncaughtExceptionReporting(deveAtivar)`

Ativa/desativa o relatório automático de exceções não tratadas.

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   deveAtivar	|   `boolean`	|  Sim/Não ativar o relatório	|
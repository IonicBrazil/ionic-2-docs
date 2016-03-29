Ionic Push é um plugin para lidar com notificações nativas com uma única API, **sem depender de qualquer outro plugin**.

###Adicionando plugin  
`ionic plugin add phonegap-plugin-push`

Repositório: https://github.com/phonegap/phonegap-plugin-push

Registrar e receber notificações 

É necessário **CordovaPlugin** `phonegap-plugin-push`. Para mais informações, veja: [Documentacao Push Plugin (Inglês)](https://github.com/phonegap/phonegap-plugin-push)

Para usuários de TypeScript, veja: [Push Plugin documentação sobre TypeScript](https://github.com/phonegap/phonegap-plugin-push/blob/master/docs/TYPESCRIPT.md)

####Métodos Estáticos  
**init(options)** 

Inicialize o plugin no modo nativo

```javascript
var push = Push.init({
   android: {
       senderID: "12345679"
   },
   ios: {
       alert: "true",
       badge: true,
       sound: 'false'
   },
   windows: {}
});  
```
Parâmetro | Tipo | Detalhe
--- | --- | --- 
options | **PushOptions** | [Opcões de push (inglês)](https://github.com/phonegap/phonegap-plugin-push/blob/master/docs/API.md#parameters)

####Retornos  
PushNotification retorna um novo objeto [PushNotification](https://github.com/phonegap/phonegap-plugin-push/blob/master/docs/API.md#pushonevent-callback)

`hasPermission()`  
Checa se as permissões para notificações push estão de acordo.

####Retorno  
Retorna uma **promessa** que devolve um objeto `isEnabled`, um booleano que indica se a permissão foi concedida.


DB Meter  
========

```$ ionic plugin add cordova-plugin-dbmeter```  
Repositório: [https://github.com/akofman/cordova-plugin-dbmeter](https://github.com/akofman/cordova-plugin-dbmeter)

Este plugin define um medidor de decibéis global, que permite obter os valores de decibéis do microfone.

Plataformas suportadas
-----
- iOS
- Android     

Uso  
-----

``` javascript 

import {DBMeter} from 'ionic-native';

// Começa a escutar  
let subscription = DBMeter.start().subscribe(
  data => console.log(data)
);

// Checa se está escutando  
DBMeter.isListening().then(
  (isListening : boolean) => console.log(isListening)
);

// Para de escutar  
subscription.unsubscribe();

// Apaga a instância do medidor de decibéis da memória  
DBMeter.delete().then(  
  () => console.log("Deleted DB Meter instance"),  
  error => console.log("Error occurred while deleting DB Meter instance")  
);  
```

Métodos estáticos  
-----

``` start() ```  
Começa a escutar  
**Retorno** : ```Observable<string>``` Retorna um observável. inscreve-se para ouvir. desinscreve-se para parar de ouvir.

``` stop() ```  
Para de escutar

``` isListening() ```  
Checa se está escutando  
**Retorno** : ```Promise<boolean>``` Retorna um promise que resolve, através de um booleano, se o medidor de decibéis está escutando.

``` delete() ```  
Apaga a instância do medidor de decibéis  
**Retorno** : ```Promise<any>``` Retorna um promise que resolve se a istância foi apagada, e rejeita se ocorreu um erro.
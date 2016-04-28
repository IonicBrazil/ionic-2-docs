Device Motion  
========

```$ ionic plugin add cordova-plugin-device-motion```  
Repositório: [https://github.com/apache/cordova-plugin-device-motion](https://github.com/apache/cordova-plugin-device-motion)

Requer o plugin cordova: ```cordova-plugin-device-motion```. para mais informações, por favor veja a [documentação do Device Motion.](https://github.com/apache/cordova-plugin-device-motion)

Uso  
-----

``` javascript 

import {DeviceMotion} from 'ionic-native';


// Recebe a aceleração atual do dispositivo  
DeviceMotion.getCurrentAcceleration().then(  
  acceleration => console.log(acceleration),  
  error => console.log(error)
);

// Observa a aceleração do dispositivo  
var subscription = DeviceMotion.watchAcceleration().subscribe(acceleration => {  
  console.log(acceleration);
});

// Deixa de observar  
subscription.unsubscribe();  
);  
```

Métodos estáticos  
-----

``` getCurrentAcceleration() ```  
Recebe a atual aceleração ao longo dos eixos x, y e z.  
**Retorno** : ```Promise<any>``` Retorna um objeto com x, y, z, e propriedades de data e hora.

``` watchAcceleration(options) ```  
Observa a aceleração do dispositivo. Limpa o que foi visto desinscrevendo-se do observável.

``` javascript  
	// Observa a aceleração do dispositivo  
var subscription = DeviceMotion.watchAcceleration().subscribe(acceleration => {  
  console.log(acceleration);  
});

// Deixa de observar  
subscription.unsubscribe();  
```  
| Parâmetro | Tipo   | Detalhes |
| --------- | ------ | -------  |
| options   |        |          |

**Retorno** : ```Observable<accelerationData>```
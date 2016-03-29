Esse plugin permite que abra um Toast(pequena caixa em popup) para **iOs, WP8 e Android**

###Importando o plugin
`$ cordova plugin add cordova-plugin-x-toast`  

[Repositório](https://github.com/EddyVerbruggen/Toast-PhoneGap-Plugin)

Requer Cordova plugin: `cordova-plugin-x-toast`. Para mais informações, acesse a [documentação do toast](https://github.com/EddyVerbruggen/Toast-PhoneGap-Plugin)

###Uso
```javascript
import {Toast} from 'ionic-native';



Toast.show("Eu sou uma mensagem Toast", 5000, "center").subscribe(
  toast => {
    console.log(toast);
  }
);

```

###Métodos estáticos


####`show(message, duration, position)`  
Mostre uma mensagem toast com a duração e a posição.

Parâmetro | Tipo | Detalhes
--- | --- | ---
message | `string` | A mensagem a ser exibida.
duration | `string` | Duração para mostrar a mensagem, pode-se usar `short`, `long` ou qualquer número em milesegundos.
position | `string` | A posição aonde vai ser posicionada a mensagem, usa-se `top`, `center`ou `bottom`.  
**Retorno:** `Observable`, notifica primeiro um caso de sucesso, logo em seguida  rejeita em caso de erro.

####`hide()`  
Manualmente esconde qualquer mensagem visível.  
**Retorno:** `Promise` Retorna uma promessa se foi escondido com sucesso.

####`showWithOptions(options)`  
Mostra uma mensagem Toast nativa, porém com opções.

Parâmetro | Tipo | Detalhes
--- | --- | ---
Options | `Object`| Opções para mostrar o Toast. **duration:** Duração de exibição do Toast, podendo ser 'short', 'long' ou qualquer número em milesegundos. **position:** Posição em que vai se encontrar a mensagem, alteráveis para: 'top', 'center' ou 'bottom' **addPixelsY:** deslocamento em pixels para mover a mensagem para cima ou para baixo confirme a posição especificada.

**Retorno:** `Observavle`, notifica primeiro um caso de sucesso, logo em seguida  rejeita em caso de erro.
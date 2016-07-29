Diagnostic
===========

```
$ ionic plugin add cordova.plugins.diagnostic
```

Repositório: [https://github.com/dpa99c/cordova-diagnostic-plugin](https://github.com/dpa99c/cordova-diagnostic-plugin)


Métodos estáticos
-----------------

``` show(Options) ```

Mostra o ActionSheet. As opções do ActionSheet é um objeto com as seguintes propriedades.

| Opção                         | Tipo      | Descrição                                    |
|-------------------------------|-----------|----------------------------------------------|
| title                         |`string`   | O título para o actionsheet                  |
| buttonLabels                  |`string[]` | Labels para os botões. Usa o índice 'x'      |
| androidTheme                  |`number`   | Tema para ser usado no Android               |
| androidEnableCancelButton     |`boolean`  | Habilita o botão de cancelar no Android      |
| winphoneEnableCancelButton    |`boolean`  | Habilita o botão de cancelar no Windows Phone|
| addCancelButtonWithLabel      |`string`   | Adiciona um botão de cancelar com texto      |
| addDestructiveButtonWithLabel |`string`   | Adiciona um botão destrutivo com texto       |
| position                      |`number[]` | No iPad, define a posição X,Y				   |

| Parametro                     | Tipo         | Detalhes                                     |
|-------------------------------|--------------|----------------------------------------------|
| Options                       |```options``` | Veja tabela acima                  		  |

*Retorna:* ```Promise``` 

Retorna uma Promise que retorna o indíce do botão pressionado (o índice começa em 1, então 1, 2, 3, etc.).

``` hide() ```

Esconde o ActionSheet.

# Globalização

```shell
$ ionic plugin add cordova-plugin-globalization
```

Repositório oficial: [https://github.com/apache/cordova-plugin-globalization](https://github.com/apache/cordova-plugin-globalization)

## Utilização

```js
import {Globalization} from 'ionic-native';
```

## Membros estáticos

### `getPreferredLanguage()`

Retorna a tag identificadora de linguagem BCP-47  para o `successCallback` com um objeto `properties` como parâmetro. Este objeto deve possuir um valor `property` do tipo String.

**_Retorna_**: `Promise<{value: string}>`

---

### `getLocaleName()`

Retorna a tag identificadora de local BCP-47  para o `successCallback` com um objeto `properties` como parâmetro.

**_Retorna_**: `Promise<{value: string}>`

---

### `dateToString(data, opções)`

Converte a `data` para string.

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   data	|   `Data`	|   A data que você quer converter	|
|   opções	|   	|   Opções para a data convertida. Tamanho, seletor.	|

**_Retorna_**: `Promise<{value: string}>` Retorna uma promise quando a data for convertida

---

### `stringToDate(dataString, opções)`

Resolve uma data formatada como string, de acordo com as preferências de usuário e calendário usando a time zone do client, e retorna um objeto `date` correspondente.

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   dataString	|   `string`	|   A data em formato de string que você quer converter	|
|   opções	|   	|   Opções para a data convertida. Tamanho, seletor.	|

**_Retorna_**: `Promise<{value: string}>` Retorna uma promise quando a data for convertida.

---

### `getDatePattern(opções)`

Retorna um padrão em string para formatar e resolver datas de acordo com as preferências de usuário do client. 

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   opções	|   	|   Objeto com o formato `tamanho` e `seletor`	|

**_Retorna_**: `Promise<{value: string}>` Retorna uma promise.

---

### `getDateNames(opções)`

Retorna um array de nomes de meses ou dias da semana, dependendo das preferências de usuário do client e do calendário.

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   opções	|   	|   Objeto com o tipo (comprimido ou extenso) e item	(meses ou dias) |

**_Retorna_**: `Promise<{value: string}>` Retorna uma promise.

---

### `isDayLightSavingsTime(data)`

Indica se o horário de verão está em vigor para uma dada data, usando as configurações de calendário e time zone do client.

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   data	|   `Date`	|   Data para processar |

**_Retorna_**: `Promise<{dst}>` Retorna uma promise com o valor.

---

### `getFirstDayOfWeek()`

Retorna o primeiro dia da semana de acordo com as preferências de usuário do client.

**_Retorna_**: `Promise<{value}>` Retorna uma promise com o valor.

---

### `numberToString(opções)`

Retorna um número formatado como string de acordo com as preferências de usuário do client.

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   opções	|   	|        |

---

### `stringToNumber(stringParaConverter, opções)`

O oposto do `numberToString`.

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   stringParaConverter	|   `string`	|   String que você deseja converter para número |
|   opções	|   	|   O tipo de número que você deseja retornar. Pode ser: `decimal`, `percent` ou `currency` |

**_Retorna_**: `Promise` Retorna uma promise com o valor.

---

### `getNumberPattern(opções)`

Retorna um padrão em string para formação e resolução de números de acordo com as preferências de usuário do client.

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   opções	|   	|   Pode ser: `decimal`, `percent` ou `currency` |

**_Retorna_**: `Promise` Retorna uma promise com o valor.

---

### `getCurrencyPattern(códigoMoeda)`

Retorna um padrão em string para formatar e resolver valores monetários de acordo com as preferências de usuário do client e também do código monetário ISO 4217.

|   Parâmetro	|   Tipo	|   Detalhes	|
|---	|---	|---	|
|   códigoMoeda	|   `string`	|   Código monetário |

**_Retorna_**: `Promise` Retorna uma promise com o valor.
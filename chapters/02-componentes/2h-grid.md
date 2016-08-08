# Grid (grade)
O sistema de grid do Ionic é baseado em flexbox, uma característica CSS suportado por todos os dispositivos que o Ionic da suporte .
A grid é composta por duas unidades: linhas e colunas. A coluna irá expandir para preencher sua linha, e será redimensionada para caber colunas adicionais.


A fim de definir a largura, use o atributo width na tag ion-col.

### Uso Básico

	<ion-row>
	  <ion-col width-10>Essa coluna terá 10% de espaço</ion-col>
	</ion-row>

Atributos de colunas explícitas em porcentagens
---
width-10	10%
***
width-20	20%
***
width-25	25%
***
width-33	33.3333%
***
width-50	50%
***
width-67	66.6666%
***
width-75	75%
***
width-80	80%
***
width-90	90%
***

Use o atributo `offset` na coluna para definir seu percentual de deslocamento da esquerda(por exemplo: offset-25). Para alinhar uma coluna verticalmente, adicione o atributo center ou baseline na tag `<ion-row>`.

Use o atributo wrap em um elemento <ion-row> para permitir que itens nessa linha sejam envolvidos. Aplica-se `flex-wrap: wrap;` para estilizar o elemento `<ion-row>`.

# Checkbox (caixa de seleção)

A checkbox é um componente de entrada que contém um valor booleano. Checkboxes no ionic não são diferentes do checkbox HTML<input>. No entanto, como outros componentes do Ionic, checkboxes possuem estilizações diferentes para cada plataforma. Para definir o valor padrão, use o atributo checked(verificado), e o atributo disabled(desativado) para desativar, impedindo o usuário de alterar o valor.

### Uso Básico

	<ion-item>
	  <ion-label>Daenerys Targaryen</ion-label>
	  <ion-checkbox dark checked="true"></ion-checkbox>
	</ion-item>
	
	<ion-item>
	  <ion-label>Arya Stark</ion-label>
	  <ion-checkbox disabled="true"></ion-checkbox>
	</ion-item>
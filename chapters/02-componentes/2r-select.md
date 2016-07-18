# Select

## Utilização básica:

O ion-select é um component similar ao elemento ```<select>``` do HTML, porém, o componente select do Ionic faz ficar mais fácil para os usuários procurarem e selecionar a opção ou opções desejadas. Quando os usuários apertam o componente select, um diálogo que vai aparecer com todas as opções largas, isso faz com que o select fique fácil para os usuários.

``` ts
<ion-list>
  <ion-item>
    <ion-label>Gaming</ion-label>
    <ion-select [(ngModel)]="gaming">
      <ion-option value="nes">NES</ion-option>
      <ion-option value="n64">Nintendo64</ion-option>
      <ion-option value="ps">PlayStation</ion-option>
      <ion-option value="genesis">Sega Genesis</ion-option>
      <ion-option value="saturn">Sega Saturn</ion-option>
      <ion-option value="snes">SNES</ion-option>
    </ion-select>
  </ion-item>
</ion-list>
```

É possível criar múltiplas seleções com ```<ion-select>``` apenas adicionando multiple="true" ao elemento.

``` ts
<ion-list>
  <ion-item>
    <ion-label>Toppings</ion-label>
    <ion-select [(ngModel)]="toppings" multiple="true" cancelText="Nah" okText="Okay!">
      <ion-option value="bacon" checked="true">Bacon</ion-option>
      <ion-option value="olives">Black Olives</ion-option>
      <ion-option value="xcheese" checked="true">Extra Cheese</ion-option>
      <ion-option value="peppers">Green Peppers</ion-option>
      <ion-option value="mushrooms">Mushrooms</ion-option>
      <ion-option value="onions">Onions</ion-option>
      <ion-option value="pepperoni">Pepperoni</ion-option>
      <ion-option value="pineapple">Pineapple</ion-option>
      <ion-option value="sausage">Sausage</ion-option>
      <ion-option value="Spinach">Spinach</ion-option>
    </ion-select>
  </ion-item>
</ion-list>
```

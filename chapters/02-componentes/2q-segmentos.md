# Segmento

Segmento é um grupo de botões que são exibidos em linha. Eles podem ser usados como filtro, mostrando ou escondendo elementos baseado nos valores de cada segmento.

## Utilização básica:

``` ts
<div padding>
  <ion-segment [(ngModel)]="pet">
    <ion-segment-button value="kittens">
      Kittens
    </ion-segment-button>
    <ion-segment-button value="puppies">
      Puppies
    </ion-segment-button>
  </ion-segment>
</div>

<div [ngSwitch]="pet">
  <ion-list *ngSwitchCase="'puppies'">
    <ion-item>
      <ion-thumbnail item-left>
        <img src="img/thumbnail-puppy-1.jpg">
      </ion-thumbnail>
      <h2>Ruby</h2>
    </ion-item>
    ...
  </ion-list>

  <ion-list *ngSwitchCase="'kittens'">
    <ion-item>
      <ion-thumbnail item-left>
        <img src="img/thumbnail-kitten-1.jpg">
      </ion-thumbnail>
      <h2>Luna</h2>
    </ion-item>
    ...
  </ion-list>
</div>
```

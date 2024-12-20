```ts
import { Component } from '@angular/core';
import { IonItem, IonItemOption, IonItemOptions, IonItemSliding, IonLabel, IonList } from '@ionic/angular/standalone';

@Component({
  selector: 'app-example',
  templateUrl: 'example.component.html',
  imports: [IonItem, IonItemOption, IonItemOptions, IonItemSliding, IonLabel, IonList],
})
export class ExampleComponent {}
```
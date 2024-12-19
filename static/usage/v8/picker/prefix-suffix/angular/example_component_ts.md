```ts
import { Component } from '@angular/core';
import { IonPicker, IonPickerColumn, IonPickerColumnOption } from '@ionic/angular/standalone';

@Component({
  selector: 'app-example',
  templateUrl: 'example.component.html',
  imports: [IonPicker, IonPickerColumn, IonPickerColumnOption],
})
export class ExampleComponent {}
```
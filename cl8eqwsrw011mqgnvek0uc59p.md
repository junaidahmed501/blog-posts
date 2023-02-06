# Show/hide password in Ionic

Directive:

```typescript
import {Directive, ElementRef, HostListener, Input} from '@angular/core';

*/**
* Generated class for the PasswordToggleDirective directive.
*
* See https://angular.io/api/core/Directive for more info on Angular
* Directives.
*/
*@Directive({
selector: '[passwordToggle]' *// Attribute selector
*})
export class PasswordToggleDirective {
@Input('appTargetInput') targetInput: any;

constructor(el: ElementRef) {
}

@HostListener('click') onMouseEnter() {
let inType = (this.targetInput._native.nativeElement.type == 'text')? 'password': 'text';
this.targetInput._native.nativeElement.type = inType;
}

}
```

Usage:

```xml
<ion-item no-margin no-padding class="clear-item-inner">
    <ion-label>
        <ion-icon name="md-lock"></ion-icon>
    </ion-label>
    <ion-input #toggleInput formControlName="password" class="half-inp half-border-inp" type="password" placeholder="Password"></ion-input>
    
    <button class="showhidePass" color="light" ion-button             type="button" clear item-end passwordToggle     [appTargetInput]="toggleInput">
    <ion-icon name="eye"></ion-icon>
    </button>
</ion-item>
```

Pass template reference variable to ‘*appTargetInput*’ of passwordToggle directive. I have passed it toggleInput which is the reference variable for ion-input above it.
## Ionic <ion-select multiple=”true”>

<form \[formGroup\]=”form”>

<h2>Hello {{name}}</h2>

<select multiple formControlName=”multiSelect”>

<option value=””>Select Item</option>

<option \*ngFor=”let item of items” \[value\]=”item.value”>{{item.name}}</option>

</select>

</form>

this.form = fb.group({  
multiSelect: \[\[‘’\], Validators.required\]  
});
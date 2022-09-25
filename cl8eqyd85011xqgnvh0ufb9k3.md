## ionic multiple select reactive form

**ion-select multiple="true \[formControl\]="registerForm.controls.locations"**\>  
  <**ion-option value="f"**\>Female</**ion-option**\>  
  <**ion-option value="m"**\>Male</**ion-option**\>  
</**ion-select**\>

buildForm() {  
  **this**.**registerForm** \= **this**.formBuilder.group({  
    **'contact'**: \[**''**, \[Validators.*required*\]\],  
    **'agree'**: \[**true**, Validators.*requiredTrue*\],  
    **'categories'**: **this**.formBuilder.array(\[\]),  
    **'locations'**: \[\[\], Validators.*required*\],  });  
}
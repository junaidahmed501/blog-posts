## Change ion-input value programmatically

@ViewChild(**'googlePlace'**) **googlePlace**;

Define in template variable like this

<**ion-input #googlePlace class="rounded-inp single-inp" type="text" placeholder="Location"**\></**ion-input**\>

**//set values like this;  
this**.**googlePlace**.**\_native**.**nativeElement**.**value** \= **''**;  
**this**.**googlePlace**.**value** \= **''**;
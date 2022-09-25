## Ionic multiple same sided menus

An application can have multiple menus on the same side. In order to determine the menu to control, an `id` should be passed. In the example below, the menu with the `authenticated` id will be enabled, and the menu with the `unauthenticated` id will be disabled.

```
`<**ion-menu** id="***authenticated***" side="left" [content]="mycontent">  
`<**ion-header**\>  
  <**ion-toolbar**\>  
    <**ion-title**\>Pages</**ion-title**\>  
  </**ion-toolbar**\>  
</**ion-header**\>  
  
<**ion-content**\>  
  <**ion-list**\>  
    <**button menuClose ion-item \*ngFor="let *p* of pages" (click)="openPage(*p*)"**\>  
      {{***p***.**title**}}  
    </**button**\>  
  </**ion-list**\>  
</**ion-content**\>  
`</**ion-menu**>`
```

```
`<**ion-menu** id="***unauthenticated***" side="left" [content]="mycontent">put second menus code here</**ion-menu**>  
<**ion-nav** #mycontent [root]="rootPage"></**ion-nav**>  
` 
```

```
//and call this method according to your logic  
enableAuthenticatedMenu() {  
  **this**.menuCtrl.enable(true, 'authenticated');  
  **this**.menuCtrl.enable(false, 'unauthenticated');  
}
```

Note: if an app only has one menu, there is no reason to pass an `id`.
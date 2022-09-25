## Angular CLI SASS options

When you are creating your project with angular cli try this:

```
ng new My_New_Project --style=sass
```

This generates all your components with predefined sass files.

If you want scss syntax create your project with :

```
ng new My_New_Project --style=scss
```

If you are changing your existing style in your project

```
ng set defaults.styleExt scss
```

Cli handles the rest of it.

### ***For Latest Versions***

For Angular 6 to set new style on existing project with CLI:

```
ng config schematics.@schematics/angular:component.styleext scss
```

Or Directly into angular.json:

```
"schematics": {  
      "@schematics/angular:component": {  
      "styleext": "scss"  
    }  
}
```
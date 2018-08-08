# Angular

## Good to know
Install [Node.js](https://nodejs.org/en/download/) if it is not already. 

Editors:
- [Visual Studio Code](https://code.visualstudio.com/)
- [Webstorm](https://www.jetbrains.com/webstorm/)
- [Sublime Text](https://www.sublimetext.com/)
- [Atom](https://atom.io/)
- [Angular Live Editor](https://stackblitz.com/angular/lkvbnprvxxq)

## Basic setup
```bash
npm install -g @angular/cli

ng new my-project

cd my-project

ng serve
```

Navigate to `http://localhost:4200/` in default. The app will automatically reload for any changes in the source files.

## Useful Commands
- Use `ng --version` to check Angular CLI version.
- Use `ng new my-dream-app --style=scss` for scss instead of css(default).
- Use `ng generate module my-new-module` or `ng g module my-new-module` to add a module.
- Use `ng generate class my-new-class` or `ng g cl my-new-class` to add a class.
- Use `ng generate component my-new-component` or `ng g c my-new-component` to add a component.
- Use `ng g c my-new-component --spec false` to add a component without .spec file.
- Use `ng generate service my-new-service` or `ng g s my-new-service` to add a service.
- Use `ng generate directive  my-new-directive` or `ng g directive my-new-directive` to add a directive.
- Use `ng generate enum my-new-enum` or `ng g enum my-new-enum` to add a enum.
- Angular CLI will automatically adjust the letter case of the file name, so the following commands have the same effect:
    > All three commands are equivalent
    - `ng generate class my-new-class`
    - `ng generate class myNewClass`
    - `ng generate class MyNewClass`
- Use `ng g c components/my-new-component` to generate a component in '**components**' folder.
- Use `ng serve --open` or `ng serve -o` or `ng s -o` to open the browser on `http://localhost:4200/`.
- Use `ng serve --port 1903` to serve on custom port.
- Use `ng test` to run all unit tests.
- Use `ng build` to build and bundle the application for deployment.
    > `development`: default mode, do not minify or uglify code,
    
    > `production`: minify and uglify code.
    - To build for production: `ng build --target=production`
    
## Comparison to AngularJS
_Angular_ is the name for the Angular of today and tomorrow. _AngularJS_ is the name for all v1.x versions of Angular.

AngularJS | Angular
--- | ---
<br/> **Bindings/interpolation** <br/><br/> Your favorite hero is: `{{vm.favoriteHero}}` <br/><br/> | <br/> **Bindings/interpolation** <br/><br/> Your favorite hero is: `{{favoriteHero}}` <br/><br/>
<br/> **Filters** <br/><br/> `{{vm.movie.title \| uppercase}}` <br/><br/> | <br/> **Pipes** <br/><br/> `{{movie.title \| uppercase}}` <br/><br/>
<br/> **ng-repeat** <br/><br/> `<tr ng-repeat="movie in vm.movies">` <br/><br/> | <br/> **\*ngFor** <br/><br/> `<tr *ngFor="let movie of movies">` <br/><br/>
<br/> **ng-class** <br/><br/> `<div ng-class="{blue: vm.isBlue, green: vm.isGreen}">` <br/><br/> | <br/> **ngClass** <br/><br/> `<div [ngClass]="{'blue': isBlue, 'green': isGreen}">` <br/><br/>
<br/> **ng-click** <br/><br/> `<button ng-click="vm.foo()">` <br/><br/> | <br/> **Bind to the** click **event** <br/><br/> `<button (click)="foo()">` <br/><br/>
<br/> **ng-href** <br/><br/> `<a ng-href="{{vm.url}}">Link</a>` <br/><br/> | <br/> **Bind to the** href **event** <br/><br/> `<a [href]="url">Link</a>` <br/><br/>
<br/> **ng-if** <br/><br/> `<table ng-if="vm.movies.length">` <br/><br/> | <br/> **\*ngIf** <br/><br/> `<table *ngIf="movies.length">` <br/><br/>
<br/> **ng-model** <br/><br/> `<input ng-model="vm.favoriteHero" />` <br/><br/> | <br/> **ngModel** <br/><br/> `<input [(ngModel)]="favoriteHero" />` <br/><br/>
<br/> **ng-hide** <br/><br/> `<h3 ng-hide="vm.favoriteHero">{{vm.favoriteHero}}</h3>` <br/><br/> | <br/> **Bind to the** hidden **property** <br/><br/> `<h3 [hidden]="favoriteHero">{{favoriteHero}}</h3>` <br/><br/>
<br/> **ng-show** <br/><br/> `<h3 ng-show="vm.favoriteHero">{{vm.favoriteHero}}</h3>` <br/><br/> | <br/> **Bind to the** hidden **property** <br/><br/> `<h3 [hidden]="!favoriteHero">{{favoriteHero}}</h3>` <br/><br/>
<br/> **ng-src** <br/><br/> `<img ng-src="{{vm.movie.imageurl}}">` <br/><br/> | <br/> **Bind to the** src **property** <br/><br/> `<img [src]="movie.imageurl">` <br/><br/>
<br/> **ng-style** <br/><br/> `<div ng-style="{color: vm.colorPreference}">` <br/><br/> | <br/> **ngStyle** <br/><br/> `<div [ngStyle]="{'color': colorPreference}">` <br/><br/>

### trackBy Usage & Comparison
- AngularJS

    ```html
    <tr ng-repeat="movie in vm.movies track by movie.id">
    ```

- Angular

    ```typescript
    @Component({
      selector: 'my-app',
      template: `
        <ul>
          <li *ngFor="let movie of movies; trackBy: trackId(index, movie)">{{movie.id}}</li>
        </ul>
      `,
    })
    
    export class App {
      constructor() {
        this.movies = [{id: 1}, {id: 2}, {id: 3}];
      }
      
      trackId(index: number, item: Item) {
        return item.id; // or index
      }
    }
    ```

## Useful Links
- Videos
    - English
        - [Angular 6 Tutorial](https://www.youtube.com/watch?v=0eWrpsCLMJQ&list=PLC3y8-rFHvwhBRAgFinJR8KHIrCdTkZcZ)
        - [Angular 6 Tutorials](https://www.youtube.com/watch?v=UoVytwPk3iA&list=PLYxzS__5yYQlqCmHqDyW3yo5V79C7eaTe)
        - [Angular In 60 Minutes](https://www.youtube.com/watch?v=KhzGSHNhnbI)
        - [Learn Angular 6 in 60 Minutes - Free Beginners Crash Course](https://www.youtube.com/watch?v=z4JUm0Bq9AM&t=732s)
    - Turkish
        - [Angular 6 Dersleri](https://www.youtube.com/watch?v=y5V6LOUwSWM&list=PLBKqEm_6KxTFlSkIJbDJ_eML11o0yI1VM)
        - [Angular 5 Dersleri](https://www.youtube.com/watch?v=TRd0ihuNdvs&list=PLqG356ExoxZWvyGkeytVjxpO-4BhjXvJ5&index=1)
        - [Angular 4 Eğitimi](https://www.youtube.com/watch?v=PbgKzD_0naM)
        - [TypeScript ile Angular 2 Uygulamaları Geliştirmek - Bora Kaşmer](https://www.youtube.com/watch?v=-G7Dq028thg)
- Articles
    - English
        - [Quick Angular CLI Reference](https://alligator.io/angular/angular-cli-reference/)
        - [Angular CLI Reference](https://cli.angular.io/reference.pdf)
- Books
    - English
        - [ng-book](https://www.ng-book.com/2/)

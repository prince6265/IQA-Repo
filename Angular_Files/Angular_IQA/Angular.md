### Question :- What isAngular.

- Angular is a platform and framework for building single-page client applications using HTML and TypeScript.

### Question :- What is Advantage of Angular.
- Angular supports two-way data-binding.
- It follows MVC pattern architecture.
- It supports static templates and Angular template.
- It facilitates you to add a custom directive.
- It also supports RESTfull services.
- Validations are supported in Angular.
- Angular provides client and server communication.
- It provides support for dependency injection.
- It provides powerful features like Event Handlers, Animation, etc.

### Question :- Difference between angular and angular js.

> Angular js
- It only supports javascript.
- The framework has MVC architecture.
- It does not have CLI tools.
- It does not use dependency Injection.
- It does not support mobile browsers.
- It is not so fast.
> Angular
- It support both javascript and typescript.
- The framework has a component based architecture.
- It has CLI tools.
- iT supports dependency Injection.
- It supports mobile browsers.
- It is very fast.

### Question :- What is Component in Angular.

In Angular, a component is a fundamental building block of the application that controls a part of the user interface (UI). A component consists of three main parts:   
   1. Template: Defines the HTML structure and layout of the component's view. It determines what is displayed on the screen.
   2. Class: Contains the logic and data associated with the component. It is written in TypeScript and includes properties and methods to handle the component's behavior.
   3. Styles: Defines the CSS or SCSS styles specific to the component.

### Question :- What is Angular CLI.

- CLI is a command line interface that is use to initialize and develop the angular application.

### Question :- What is a selector and template.

> Selector
- A selector is used to identify each component uniquely into the component tree.
- A CSS-like identifier used to insert a component into your application.
- It tells Angular where in the HTML to render the component.
- 
> Template
- The HTML structure of the component.
- It defines what will be displayed on the screen when the component is rendered.
```TypeScript
@Component({
  selector: 'app-retailer-prepaid',    // This is selector.
  standalone: true,
  imports: [RouterLink, RouterOutlet],
  templateUrl: './retailer-prepaid.component.html',   // This is the template.
  styleUrl: './retailer-prepaid.component.scss'
})
```
### Question :- What is module in Angular and what app.module.ts file.
> Module:
- Modules are place where you can group the components, directives, Pipes, and services which ar related to application.
- A module is defined using the NgModule decorator. It tells Angular what components, directives, and services belong to the module and what should be accessible to other modules.
- Modules are used to define what parts of the application belong together and manage their dependencies.Modules are used to define what parts of the application belong together and manage their dependencies.
- Every Angular app has at least one module called the root module (usually AppModule). This is the starting point of the application.
- For larger applications, you can create additional modules (e.g., UserModule, AdminModule) to organize related functionality.

### Question :- How an angular app gets loaded and started? What are index.html, app-root, and main.ts.
- An Angular app gets loaded and started through a series of steps, from loading the HTML file to bootstrapping the root module and displaying the root component.
> Index.html:
- The main HTML file of the Angular app that acts as the entry point for the browser.
- It contains a placeholder where Angular renders the app.
- **app-root** (or any root component's selector) is placed here as a placeholder.
```HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>My Angular App</title>
</head>
<body>
  <app-root></app-root> <!-- Placeholder for the Angular app -->
</body>
</html>
```
- The browser loads this file first.
- The **app-root** tag is replaced by the content of the root component when Angular starts.
- Angular is used to create single page application. index.html is that single page. Index.html will invoke main.js file which is js version of main.ts file.
> app-root:
- The default selector of the root component (AppComponent) in Angular.
- It is a custom HTML tag where the root component's template gets rendered.
```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'app-root', // The HTML tag to identify this component
  templateUrl: './app.component.html', // HTML structure of this component
  styleUrls: ['./app.component.scss'], // Styles specific to this component
})
export class AppComponent {
  title = 'My Angular App';
}
```
- App-component or app-root component is the html which you will see finally.
> main.ts:
-  The starting point of the Angular app. It is the first TypeScript file executed by Angular.
- main.ts file is like the entry point of web-app. it compiles the web and bootstrap the AppModule to run in the browser.
- It bootstraps (initializes) the root module (AppModule).
- Imports the root module (AppModule).
- Calls platformBrowserDynamic() to prepare the app for running in the browser.
- Bootstraps the root module using bootstrapModule(AppModule).
### Question :- What is bootstrapped module and bootstrap component.
- bootstrapped module and bootstrap component are key concepts related to how the Angular app starts. 
- When the angular Web application will start then the first module launched is the bootstrapped module and same is the bootstrapped component.
- The module that Angular starts first when loading the application. This is usually the root module (e.g., AppModule).
- It tells Angular which component should be displayed first (the bootstrap component) and initializes the app.
- The main.ts file, where the root module (AppModule) is bootstrapped.
- Think of the bootstrapped module as the main gate of a building. It decides which part of the building (component) visitors see first.
### Question :- What is a Data-Binding in Angular.

- data binding is a way to communicate between the typescript and Html code.
> Type of Data Binding:
   > Single interpolation
   - It is a one-way data binding process that is used to bind data from the typescript to the html.
      ```typescript
      {{data}}
      ```
   - Note: String interpolation can only work on string type not on number type or any other data type.
   > Property Binding
   - Property binding is a superset of interpolation. It can do whatever interpolation can do, in addition it can set an element property to a non-string data value like boolean.
      ```typescript
      Property Binding [property] = "expression"
      ```
   > Event Binding 
   - Event binding is used to handle the events raised by the user actions like button click, mouse hover, etc.
      ```typescript
      Event Binding (event) = "expression"
      ```
   > Two way data Binding
   - it helps user to exchange data fro view to component and from component to view at the same time.
      ```typescript
      Two way data binding [(ngModel)] = "data"
      ```

### Question :- Directives in Angular.
- directives are special markers that tell Angular to modify the behavior or appearance of elements in the DOM (the webpage structure). Directives can be used to add or change the behavior of DOM elements without directly changing the HTML.
   > Structural directives
     - Change appearance of DOM elements by adding and removing elements from the DOM.
     - *ngIf: Conditionally adds or removes an element.
     - *ngFor: Loops through an array and adds an element for each item.
       ```HTML
       <p *ngIf="isLoggedIn">Welcome, User!</p>
       ```
     - If the variable isLoggedIn is true, the paragraph with the message "Welcome, User!" will appear. If false, it will be removed from the DOM. 
   > Attribute directives
     - Attribute directives change the appearance or behavior of an element by modifying its properties.
     - ngClass: Adds or removes CSS classes.
     - ngStyle: Changes the styles dynamically.
       ```HTML
       <div [ngClass]="{'highlight': isSpecial}">Special Dish</div>
       ```
     - If isSpecial is true, the highlight class is added to the div, changing its style (e.g., color). 
   > Component directives
     - These are directives that create and manage Angular components, which are self-contained blocks of functionality and UI.
     - All Angular components are technically a type of directive, but they come with their own view and behavior.
     - Every screen in the app (like Home, Profile, Settings) is a component. Each component behaves like a small "directive" but also has its own template (view) and functionality.
### Question :- What is Decorator in Angular.

- Angular decorates store metadata about a class, method, or property.
- All decorator are represented with @ symbol.
- A decorator is a special kind of syntax (a function prefixed with @) that is used to add metadata or behavior to classes, methods, properties, or parameters. This metadata helps Angular understand how to process and use these elements in your application.
> Real life example:
- Imagine you're a teacher organizing different types of classes in a school. You label each classroom with a name and subject so that students know what it's for. In Angular, decorators are like those labels: they tell Angular what a class, method, or property is for.

> Types of decorators.
1. Class decorators
   1. @ngModule
   2. @component
   3. @Directive
   4. @Pipe
   5. @injectable
2. Method decorators
   1. @input
   2. @output
   3. @ContentChild
   4. @ContentChildren
   5. @viewChild
   6. @viewChildren
   7. @HostBinding
3. Property decorators
   1. @HostListener
4. Parameter decorators
   1. @Host
   2. @Self
   3. @SkipSelf
   4. @Inject
   5. @Optional

### Question :- What are pipes in Angular.

- Pipes are simple function which accept an input value and return a transformed value.
> types of pipes
1. Built in pipes
   1. lowercase
   2. uppercase
   3. date
   4. currency
   5. percentage
   6. decimal
   7. slice
   8. json
2. Custom pipes 

### Question :- What is chaining pipes.

- using multiple pipes on a data input.

```typeScript
{{dob | date | uppercase}}
```

### Question :- What is a service in Angular.
- A service is a typescript class and a reusable code which can be used in multiple components.
- Service can be implemented with the help of dependency Injection. services are used for reusability purpose.
### Question :- What is dependency injection in Angular.
- In simple terms, Dependency Injection (DI) is a design pattern used in Angular to provide objects (dependencies) to classes when they need them, instead of the class creating the objects itself. This makes the code more flexible, reusable, and easier to test.
### Question :- What is hierarchical Dependency Injection.
- In Angular, Hierarchical Dependency Injection means that Angular provides dependencies (services) in a tree-like structure, where:
   - Each level in the application (modules, components, directives) has its own injector.
   - Child components or modules can inherit or override services from their parent.
     - Services can be shared across multiple components if registered at a higher level (e.g., root).
     - Components or modules can have their own specific instances of a service if registered locally.
### Question :- What is a service provider.
- A provider is an object declared inside a decorator which inform angular that particular service is available for injecting inside the components.
- In angular a service provider is the mechanism that tells angular how to create an instance of a service when it is needed. it connects the service with dependency injection system, ensuring that the require service instance is available for components, directives, or other services.
### Question :- What is the role of @injectable decorator? How to use one service inside another service.
- With @injectable decorator one service can be used by another service.
- The @Injectable decorator in Angular tells the framework that a class can be used as a service and can have dependencies that Angular should inject into it. This is essential for Angular’s dependency injection system to work.
   - Without @Injectable, Angular cannot inject dependencies into the service.
   - It ensures that the service can be registered with Angular's injector and provided to components, other services, or directives.
### Question:- What are Parent-child components.
- In Angular, parent-child components represent a hierarchical relationship where:
- A parent component contains one or more child components.
- The parent passes data or interacts with the child, while the child can send updates back to the parent.
- This relationship is commonly used to create modular, reusable, and organized components in your application.
> Real-Life Example: 
- Hotel Booking System
  - Parent Component: The "Hotel Room" component displays general details like the room name, type, and cost.
  - Child Component: The "Amenities List" component shows specific amenities (like Wi-Fi, TV, or room service).
      - The parent provides data about the room, and the child displays additional features based on that data.
### Question :- What are life-cycles of hooks in Angular.
- Lifecycle hooks are special methods in Angular components and directives that allow you to perform actions at different stages of a component's existence. Angular provides these hooks to let developers interact with the creation, updates, and destruction of components.
  1. component instantiating.
  2. Rendering the component HTML view.
  3. Creating the Child components (if required)
  4. Destroying the component (if required)
> Real-Life Example:
   - Imagine you are managing a smart home system where:
     - Component Initialization: When you power on a light bulb, it sets itself up with a default brightness and color.
     - Changes Detection: When you adjust the brightness or color, it reacts and updates accordingly.
     - Cleanup: When you remove the light bulb, it clears any remaining data or shuts down properly.
     - In Angular, lifecycle hooks help you achieve similar functionality for components.
- Constructor : it is default method of the typescript class that is executed when the class is instantiated. It always run before any angular hook and it is not a part of lifecycle hooks.
- ngOnChanges : Called when input property changes.
- ngOnInit : Called when the component is created. 
   - ngAfterContentInit : Called when the component's content has been fully initialized.
   - ngAfterContentChecked : Called when the component's content has been checked.
   - ngAfterViewInit : Called when the component's view has been fully initialized.
   - ngAfterViewChecked : Called when the component's view has been checked.
- ngOnDestroy : Called when the component is destroyed.
### Question :- What is a Constructor in Angular.
- The constructor is method in a typescript class that automatically get called when the class is being instantiated.
- Constructor run before any angular hook and it is not a part of lifecycle hooks.
- Constructor is widely used to inject dependencies into the component class.
### Question :- What is a ngOninit life cycle hook in Angular.
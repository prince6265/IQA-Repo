### Question  :- What is SPA in Angular ?
- A Single-Page Application (SPA) in Angular is a web application that operates within a single HTML page, dynamically updating content as the user interacts with it, without needing to reload the entire page. Angular is particularly well-suited for building SPAs because it efficiently manages routing, data binding, and user interaction on the same page, resulting in a smooth, fast, and seamless user experience.
### Question  :- routing in Angular ?
- The Angular Router enables navigation between different views or pages in your application without reloading the entire page, providing a smooth user experience.
### Question  :- Explain Lazy Loading ?
- Lazy Loading is a design pattern used in web development, particularly in Single-Page Applications (SPA), where modules or components are loaded only when they are needed rather than loading everything upfront. This improves the performance of the application by reducing the initial load time and ensuring that only the necessary code is loaded when the user navigates to specific parts of the app.
### Question  :- Define Services ?
- In Angular, a Service is a class that is used to encapsulate logic and functionality that is shared across multiple components. Services are used to handle tasks like data fetching, business logic, and utility functions, which helps keep components focused on displaying data and handling user interactions.
### Question  :- What is Depedency Injection ?
- Dependency Injection (DI) is a design pattern and core concept in Angular (and other frameworks) that allows you to inject dependencies (i.e., services, objects, or values) into a class, rather than having the class create them itself. This promotes loose coupling and makes the application more modular, testable, and maintainable.

- In simpler terms, Dependency Injection means that a class (like a component or service) doesn’t have to create or manage its dependencies; instead, these dependencies are provided by an external source, typically through Angular's Injector.

### Question  :- Whats the benefit of Depedency Injection ?
1. Loose coupling
2. Testability
3. Maintainability
4. Reusability
5. Flexibility
6. Centralized Management of Dependencies
### Question  :- Differentiate between ng serve and ng build ?
> ng serve
- Purpose: The ng serve command is used to serve your Angular application in a development environment.
- Development Mode: It runs the application in development mode, which includes features like live reloading and debugging capabilities.
- Local Server: When you run ng serve, it starts a local development server (usually on http://localhost:4200/ by default), which you can access in your browser to view and test your application.
- Live Reloading: It watches your source files for changes and automatically reloads the application in the browser, making it ideal for active development.
- Source Maps: It compiles your code with source maps enabled, which helps with debugging the application in the browser.
- Unoptimized Build: The build is unoptimized and focuses on making development fast and convenient. This includes not minifying JavaScript, CSS, or templates.
> ng build
- Purpose: The ng build command is used to build the Angular application for production or for deploying to a server.
- Production Mode: When you run ng build, it compiles the application in production mode by default, optimizing the application for deployment. This includes minifying code, tree-shaking, and other performance optimizations.
- Output Directory: The output is stored in the dist/ folder (by default), which contains the final version of the app that is ready for deployment to a web server.
- Optimized Build: The build process performs optimizations like minification, bundling, and compression, which reduces the size of the application files for faster loading and better performance in production.
- No Live Reloading: Unlike ng serve, ng build does not serve the application. It just compiles the project and outputs the final build files.
- No Source Maps (in production): By default, source maps are not generated when building for production to reduce the size of the final output. However, you can enable them explicitly if needed.
### Question  :- Explain the --prod parameter in ng build ?
- The --prod parameter in the ng build command is used to build your Angular application in production mode. When you use this flag, Angular applies a set of optimizations and configurations to make the application smaller, faster, and ready for deployment to a live environment.
- This is a common practice to optimize the production build for performance and deployment to a live server.
### Question  :- Explain ViewChild and ViewChildren?
- In Angular, @ViewChild is a decorator that allows you to access and interact with child components, DOM elements, or directives in the view from within a parent component. It provides a way to get references to elements in the component's template, making it possible to manipulate or call methods on those elements or components directly.
### Question  :- What is ContentProjection?
- Content projection is a concept in Angular that allows you to pass content from a parent component into a child component, where it can be rendered inside the child component's template. It's a way of creating reusable and flexible components that can accept dynamic content from their parent.
### Question  :- What is ContentChild and ContentChildren?
- ContentChild is a decorator in Angular that allows a child component to access content that has been projected into it by its parent component. This is useful when you want to manipulate or interact with the projected content in the child component after it has been passed in.
### Question  :- Explain the importance of Component life cycle ?
- The component lifecycle in Angular refers to the series of events or stages that a component goes through from its creation to its destruction. Understanding and utilizing the component lifecycle is crucial because it provides hooks where you can insert custom logic at various points during the component's existence. This gives you fine-grained control over how your components interact with the application and how they perform.
### Question  :- Explain events and sequence of component life cycle ?
- The component lifecycle in Angular consists of a series of events or hooks that allow you to tap into different stages of a component’s existence. These events provide opportunities to perform actions like initialization, change detection, and cleanup.
### Question  :- Constructor vs ngOnInit() ?
- In Angular, both the constructor and ngOnInit are used for component initialization, but they serve different purposes and are triggered at different stages of the component lifecycle.
> Constructor:
- The constructor is a TypeScript feature and part of the class itself. It is used to initialize the class (component) and inject dependencies into it.
- It runs when the class is instantiated, before Angular fully initializes the component.
- Setting up dependency injections (services, other components, etc.).
- Basic initialization tasks like defining default values for variables.
> ngOnInit():
- ngOnInit is part of Angular’s lifecycle hooks. It is specifically designed for Angular component initialization tasks that need to happen after Angular has initialized the component’s data-bound properties.
- 
### Question  :- How to make HTTP calls using Angular ?
### Question  :- What is the need of Subscribe function ?
- The subscribe function is essential in Angular because it allows us to handle and react to data emitted by Observables. Observables are a key part of RxJS (Reactive Extensions for JavaScript), which Angular uses extensively for handling asynchronous data streams, such as HTTP requests, user interactions, or real-time updates.
### Question  :- How to handle errors when HTTP fails ?
### Question  :- How to pass data between components ?
### Question  :- Explain importance of input, output & event emitters ?
### Question  :- How to pass during routing ?
### Question  :- Is it a good practice to pass data using services ?
### Question  :- What is the need of Angular Pipes?
### Question  :- Can you name some built-in Angular Pipes?
### Question  :- How to create Custom pipes in Angular?
### Question  :- Whats the full form of RxJs?
### Question  :- What is the purpose of RxJs?
### Question  :- What are observables and observers?
### Question  :- Explain the use of Subscribe with sample code.
### Question  :- How to unsbscribe in RxJs?
### Question  :- Explain concept of operators with sample code.
### Question  :- How to install RxJs?
### Question  :- Differentiate between promise and RxJs?
### Question  :- In Angular where have you used RxJs?
### Question  :- Which operators have you used from RxJs?
### Question  :- What is Push/reactive vs Pull/Imperative?
### Question  :- What are Interceptors in Angular?
### Question  :- How to implement Interceptors?
### Question  :- Give some use of Interceptors?
### Question  :- Can we provide multi-Interceptors?

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
### Question :- architecture of Angular ?
- Angular’s architecture is based on components. Each component represents a piece of the UI, and when combined, they form the entire user interface. This modularity enables a reusable, maintainable, and testable codebase.
### Question :- What is Component in Angular.

In Angular, a component is a fundamental building block of the application that controls a part of the user interface (UI). A component consists of three main parts:   
   1. Template: Defines the HTML structure and layout of the component's view. It determines what is displayed on the screen.
   2. Class: Contains the logic and data associated with the component. It is written in TypeScript and includes properties and methods to handle the component's behavior.
   3. Styles: Defines the CSS or SCSS styles specific to the component.
### Question :- Node_Modules?
- The node_modules folder is where all the packages you install from NPM are stored. It’s like a storage room in your project that holds the tools and materials you need to build your application.
- In short, NPM helps you find and install useful tools (packages), and the node_modules folder is where those tools live within your project. This process saves you time and effort, just like buying ready-made materials does in real life.
### Question :- Package.json?
- In Angular, the package.json file is like the blueprint or the configuration guide for your project. It contains important information about the project and the dependencies (packages) required to run or build it. This file helps developers manage all the tools, libraries, and other packages that the project relies on.
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
- In Angular, a module is a container. In order words, we can say that a module is a mechanism to group components, services, directives, pipes. So, the grouping of related components, services, pipes, and directives is nothing but a module in angular.
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
## Difference between static type and dynamic type language
## What is scope in JS 
          - Global scope
          - Function scope
          - Block scope
## Types of variable in JS when it is declared without using the var, let, const keyword

## Client side and server side
- A client is a device, application, or software component that request and consumes services or resource from a server.
- A server is a device, Computer, or Software application that provides services, resources, or function to a client.

## Differnce between var, Let and const.

- Scope:
- var: Function-scoped. Variables declared with var are function-scoped, meaning they are accessible throughout the function in which they are defined.
- let and const: Block-scoped. Variables declared with let and const are block-scoped, meaning they are only accessible within the block (enclosed by curly braces) where they are defined, such as a loop or an if statement.
- Hoisting:
- var: Hoisted. Variables declared with var are hoisted to the top of their containing function or global scope. This means you can access them before they are declared in the code, but they will be initialized with undefined.
- let and const: Hoisted but not initialized. Variables declared with let and const are also hoisted, but they are not initialized until their declaration statement is executed. Trying to access them before the declaration will result in a ReferenceError.
- Reassignment:
- var and let: Can be reassigned. Variables declared with var and let can be reassigned new values after their initial declaration.
- const: Cannot be reassigned. Variables declared with const are read-only and cannot be reassigned once they are given a value. However, it's important to note that for objects and arrays declared with const, their properties or elements can still be modified.
- Temporal Dead Zone (TDZ):
- var: Variables are not affected by the Temporal Dead Zone (TDZ) because they are hoisted and initialized with undefined.
- let and const: Variables declared with let and const are affected by the TDZ, which means you cannot access them before their declaration in the code.
- Global Object Property:
-var: Variables declared with var become properties of the global object (window in a browser or global in Node.js) if declared in the global scope.
-- let and const: Variables declared with let and const do not become properties of the global object when declared in the global scope.
## String Built in methods

```javascript
let myString = "Prince"
console.log(myString.length) // output 7
console.log(myString.toUpperCase) // output PRINCE
console.log(myString.chatAt('0')) // output p
console.log(myString.indexOf(P)) // output 0
console.log(myString.substring(0, 4)) // output Prin
console.log(myString.slice(0, 4)) // output Prin // it follows negative indexing also 
let newString = "   Prince   " 
console.log(newString.trim()) // output "Prince" // it removes extra spaces
let url = "https://PrinceKumar%20gmail.com"
console.log(url.replace('%20', '@'))// output: https://PrinceKumar@gmail.com
let url = "https://PrinceKumar%20gmail.com"
console.log(url.includes('sss')) // output: false 
// it search provided data inside given string if found then return true otherwise false
let name = "Prince Kumar"
console.log(name.split(' ')) // output: ["Prince","Kumar"]

// it saperates the strings as per given data here we pass space so it saperates by coma(,)where spaces are present.
```

## DOM(Document object model)
- It represent a web page as a tree like structure that allows javasscript to dynamically access and mainipulate the content and structure of a web page.

## Data-types 
- It detremine type of a variable
-  Primitive : 
   -  Primitive data-type can hold only single value. primitive data types are immutable, Meaning their value cannot be changed once they are assigned. 
     1. Nubers
     2. string 
     3. boolean
     4. undefined
     5. null
- non-primitive
  - can hold multiple values, they are mutable there value can be changed once they are assigned.
     1. Object 
     2. array 
     3. function
     4. date
     5. Regexp
## Hoisting in javascript:
- hoisting is a js behavior where variables declared outside of a function are hoisted to the top of their containing function or global scope during the compilation phase.
  - Function Hoisting
      ```JavaScript
      myFunction(); // Output: "I am a function"
      function myFunction() {
        console.log("I am a function");
      }
  - Variable Hoisting
      ```javascript
      console.log(myVar); // Output: "I am a variable"
      var myVar = "I am a variable";
      ```
## What are variables? Difference between var, let and const ?
- VAriables are used to store data.
  - Using var : Var creates function scoped variable
     ```javascript
     function Example(){
          if(true){
               var x = 10;
               console.log(x); // Output: 10
          }
          console.log(x); // Output: 10
     }
     ```
  - Using let : let creates a block-scoped variable
     ```javascript
     function Example(){
          if(true){
               let x = 10;
               console.log(x); // Output: 10
          }
          console.log(x); // Output: ReferenceError: x is not defined
     }
     ```
  - Using const : const can be assigned by only once and it's value cannot be changed afterwards.
     ```javascript
     const x= 10;
     x= 20;
     console.log(x); // Output: TypeError: Assignment to constant variable 
     ```
## Difference between null and undefined:
- undefined:
  - When a variable has declared but has not be assigned a value, it is automatically initialized with undefined.
     ```javascript
     let undefinedVariable;
     console.log(undefinedVariable); // Output: undefined
     ```
- null:
  - Null is a value that represents the intentional absence of any object value.
  - Null values are intentionally assigned to null values.
    ```javascript
    let nullvariable = null;
    console.log(nullvariable); // Output: null
    ```
## What is the use of type of operator ?
- It is use to determine the type of a variable.
- Real application use : type of operator is used for validate the data received from external source(API).
## Type coercion:
- Type coercion is the automatic conversion of values from one data-type to another data-type during certain expression and compression.
```javascript
let string = "20";
let number = 20 ;
let boolean = true;
let nullableValue = null;
// Type coercion from string to number
console.log(string + number); // Output: "2020"
console.log(number+boolean); // Output: 21
console.log(number == string); // Output: true
console.log(boolean == 1); // Output: true
console.log(boolean + nullableValue); // Output: 1
```
- Use oof type coercion
  - type coercion can be used during string and number concatenation.
  - Type coercion can be used while using Comparison operators.
## What is Operator Precedence ?
- Operator with highest precedence are evaluated first.
```javascript
let a = 6;
let b= 5;
let c = 10;
let result = a + b * c + (a - b);
console.log(result); // Output: 57
```
## Short - circuit evaluation:
- Short - circuit evaluation stops the execution as soon as the result can be determined without evaluating the remaining sub-expressions.
## Conditional statements:
- If and else:
  - if the condition is true, the code inside the if block is executed.
  - if the condition is false, the code inside the else block is executed.
     ```javascript
     let a = 6;
     let b= 5;
     if(a > b){
          console.log("a is greater than b");     
     }else{
          console.log("b is greater than a");
     }
     ```
- Ternary Operator:
  - Ternary operator is a conditional operator that takes three operands: a condition, a value if the condition is true, and a value if the condition is false.
    ```javascript
    let y = 20;
    let z = y > 10 ? "Greater than 10" : "Less than 10";
    console.log(z);
    ```
- Switch statement:
  - Switch statement is a control flow statement that allows you to execute different blocks of code based on different cases.
    ```javascript
    let day = "Monday";
    switch(day){
         case "Monday":
              console.log("Today is Monday");
              break;
         case "Tuesday":
              console.log("Today is Tuesday");
              break;
         default:
              console.log("Invalid day");
              break;
    }
    ```
## What is the difference between == and === ?
- == (Loose equality operator): compares two values for equality after performing type coercion.
- === (Strict equality operator): compares two values for equality without performing type coercion.
- == and === have different behavior when used to compare different data types. === performs type coercion while == does not.
     ```javascript
     let x = 10;
     let y = "10";
     console.log(x == y); // Output: true
     console.log(x === y); // Output: false
     ```
- normally === is used to compare the value and type of two variables.
## What the difference between spread vs rest operator ?
- The spread operator(...) is used to expand or spread elements from an iterable (such as an array, string, or object) into individual elements.
     ```javascript
     const arr = [1, 2, 3];
     const newArr = [...arr, 4, 5];
     console.log(newArr); // Output: [1, 2, 3, 4, 5]
     ```
- The rest operator(...) is used to collect the remaining elements of an iterable into an array.
     ```javascript
     function sum(...args) {
          return args.reduce((acc, num) => acc + num, 0);
     }
     console.log(sum(1, 2, 3, 4, 5)); // Output: 15     
     ```
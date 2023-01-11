# JavaScript Interview Question and Answer
`level 0`
<details >
<summary>
List some features of JavaScript.
</summary>

- Lightweight
- Interpreted programming language
- Good for the applications which are network-centric
- Complementary to Java
- Complementary to HTML
- Open source
- Cross-platform
</details>
<br>
<details>
<summary>Who developed JavaScript, and what was the first name of JavaScript?
</summary>

JavaScript was developed by Brendan Eich, who was a Netscape programmer. Brendan Eich developed this new scripting language in just ten days in the year September 1995. At the time of its launch, JavaScript was initially called Mocha. After that, it was called Live Script and later known as JavaScript.

</details>

<br>
<details>
<summary>List some of the advantages of JavaScript.</summary>

Some of the advantages of JavaScript are:

- Server interaction is less
- Feedback to the visitors is immediate
- Interactivity is high
- Interfaces are richer
</details>
<br/>

<details>
<summary>List some of the disadvantages of JavaScript.
</summary>
Some of the disadvantages of JavaScript are:

- No support for multithreading
- No support for multiprocessing
- Reading and writing of files is not allowed
- No support for networking applications.
</details>
<br/>

<details>
<summary>What is ECMAScript ?</summary>
ECMAScript is the scripting language that forms the basis of JavaScript. ECMAScript standardized by the ECMA International standards organization in the ECMA-262 and ECMA-402 specifications. The first edition of ECMAScript was released in 1997.
</details>
<br/>

<details>
<summary>What is JSON ?</summary>
JSON (JavaScript Object Notation) is a lightweight format that is used for data interchanging. It is based on a subset of JavaScript language in the way objects are built in JavaScript.
</details>
<br/>

<details>
<summary>What are the syntax rules of JSON?</summary>
Below are the list of syntax rules of JSON

- The data is in name/value pairs
- The data is separated by commas
- Curly braces hold objects
- Square brackets hold arrays
</details>
<br/>

<details>
<summary>Why do you need JSON ?</summary>
When exchanging data between a browser and a server, the data can only be text. Since JSON is text only, it can easily be sent to and from a server, and used as a data format by any programming language.
</details>
<br/>

<details>
<summary>What are PWAs ?</summary>
Progressive web applications (PWAs) are a type of mobile app delivered through the web, built using common web technologies including HTML, CSS and JavaScript. These PWAs are deployed to servers, accessible through URLs, and indexed by search engines.
</details>
<br/>

<details>
<summary>What is V8 JavaScript engine ?</summary>
V8 is an open source high-performance JavaScript engine used by the Google Chrome browser, written in C++. It is also being used in the node.js project. It implements ECMAScript and WebAssembly, and runs on Windows 7 or later, macOS 10.12+, and Linux systems that use x64, IA-32, ARM, or MIPS processors. Note: It can run standalone, or can be embedded into any C++ application.
</details>
<br/>

<details>
<summary>What is jQuery ?</summary>
jQuery is a popular cross-browser JavaScript library that provides Document Object Model (DOM) traversal, event handling, animations and AJAX interactions by minimizing the discrepancies across browsers. It is widely famous with its philosophy of “Write less, do more”.
</details>
<br/>

<details>
<summary>What is the object type?</summary>
The object type refers to a compound value where you can set properties (named locations) that each hold their own values of any type.

---

```js
var obj = {
  a: "hello Prabir", // property
  b: 20,
  c: true,
};
obj.a; // "hello Prabir", accessed with doted notation
obj.b; // 20
obj.c; // true

obj["a"]; // "hello Prabir", accessed with bracket notation
obj["b"]; // 20
obj["c"]; // true
```

</details>
<br/>

<details>
<summary>Explain arrays in JavaScript</summary>
An array is an object that holds values (of any type) not particularly in named properties/keys, but rather in numerically indexed positions:

---

```js
var arr = ["hello Prabir", 22, true];

arr[0]; // "hello Prabir"
arr[1]; // 22
arr[2]; // true
arr.length; // 3

typeof arr; // "object"
```

</details>
<br/>

<details>
<summary>What is typeof operator?</summary>
JavaScript provides a typeof operator that can examine a value and tell you what type it is:

---

```js
var a;
typeof a; // "undefined"

a = "hello Prabir";
typeof a; // "string"

a = 42;
typeof a; // "number"

a = true;
typeof a; // "boolean"

a = null;
typeof a; // "object" -- weird, bug

a = undefined;
typeof a; // "undefined"

a = { b: "c" };
typeof a; // "object"
```

</details>
<br/>

<details>
<summary>Explain equality in JavaScript</summary>
JavaScript has both strict and type–converting comparisons:

- Strict comparison (e.g., ===) checks for value equality without allowing coercion
- Abstract comparison (e.g. ==) checks for value equality with coercion allowed

---

```js
var a = "90";
var b = 90;

a == b; // true
a === b; // false
```

Some simple equalityrules:

- If either value (aka side) in a comparison could be the true or false value, avoid == and use ===.
- If either value in a comparison could be of these specific values (0, "", or [] -- empty array), avoid == and use ===.
- In all other cases, you're safe to use ==. Not only is it safe, but in many cases it simplifies your code in a way that improves readability.
</details>
<br/>

<details>
<summary>What is Scope in JavaScript?</summary>
   In JavaScript, each function gets its own scope. Scope is basically a collection of variables as well as the rules for how those variables are accessed by name. Only code inside that function can access that function's scoped variables.

A variable name has to be unique within the same scope. A scope can be nested inside another scope. If one scope is nested inside another, code inside the innermost scope can access variables from either scope.

</details>
<br/>

<details>
<summary>Explain Values and Types in JavaScript</summary>
   JavaScript has typed values, not typed variables. The following built-in types are available:

- string
- number
- boolean
- null and undefined
- object
- symbol (new to ES6)

</details>
<br/>

<details>
<summary>What is `let` keyword in JavaScript?</summary>
   In addition to creating declarations for variables at the function level, ES6 lets you declare variables to belong to individual blocks (pairs of { .. }), using the let keyword.

</details>
<br/>

<details>
<summary>What is the difference between == and ===?</summary>
 == is the abstract equality operator while === is the strict equality operator. The == operator will compare for equality after doing any necessary type conversions. The === operator will not do type conversion, so if two values are not the same type === will simply return false. When using ==, funky things can happen, such as:

---

```js
1 == "1"; // true
1 == [1]; // true
1 == true; // true
0 == ""; // true
0 == "0"; // true
0 == false; // true
```

never to use the == operator, except for convenience when comparing against null or undefined, where a == null will return true if a is null or undefined.

```js
var a = null;
console.log(a == null); // true
console.log(a == undefined); // true
```

</details>
<br/>

<details>
<summary>What's the difference between Host objects and Native objects?</summary>

- Native objects are objects that are part of the JavaScript language defined by the ECMAScript specification, such as String, Math, RegExp, Object, Function, etc.
- Host objects are provided by the runtime environment (browser or Node), such as window, XMLHTTPRequest, etc.

</details>
<br/>

<details>
<summary>What is difference between document.getElementById() and document.querySelector()?
</summary>

- document.getElementById():

Returns an element object representing the element whose id property matches the specified string. Since element IDs are required to be unique if specified, they're a useful way to get access to a specific element quickly.

```js
element = document.getElementById(id);
```

- document.querySelector():
  Returns the first matching Element node within the node's subtree. If no matching node is found, null is returned.

```js
element = document.querySelector(selectors);
```

- document.querySelectorAll():
  Returns a NodeList containing all matching Element nodes within the node's subtree, or an empty NodeList if no matches are found.

```js
element = document.querySelectorAll(selectors);
```

</details>
<br/>

<details>
<summary>When to use reduce(), map(), foreach() and filter() in JavaScript?</summary>

- forEach():
  It takes a callback function and run that callback function on each element of array one by one.

Basically forEach works as a traditional for loop looping over the array and providing array elements to do operations on them.

```js
var arr = [10, 20, 30];

arr.forEach(function (elem, index) {
  console.log(elem + " comes at " + index);
});
```

output:

```js
10 comes at 0
20 comes at 1
30 comes at 2
```

- filter():
  The main difference between forEach() and filter() is that forEach just loop over the array and executes the callback but filter executes the callback and check its return value. If the value is true element remains in the resulting array but if the return value is false the element will be removed for the resulting array.

Note: filter does not update the existing array it will return a new filtered array every time.

```js
var arr = [10, 20, 30];

var result = arr.filter(function (elem) {
  return elem !== 20;
});
console.log(result);
```

output:

```js
[10, 30];
```

- map():

map() like filter() & forEach() takes a callback and run it against every element on the array but whats makes it unique is it generate a new array based on your existing array.

Like filter(), map() also returns an array. The provided callback to map modifies the array elements and save them into the new array upon completion that array get returned as the mapped array.

```js
var arr = [10, 20, 30];

var mapped = arr.map(function (elem) {
  return elem * 10;
});
console.log(mapped);
```

output:

```js
[100, 200, 300];
```

- reduce():

reduce() method of the array object is used to reduce the array to one single value.

```js
var arr1 = [10, 20, 30];

var sum = arr.reduce(function (sum, element) {
  return sum + element;
});
console.log(sum); // Output: 60
```

</details>
<br/>

<details>
<summary>What is Hoisting in JavaScript?</summary>

Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their scope before code execution.

Example 01: Variable Hoisting

---

```js
console.log(message); // output : undefined
var message = "The variable Has been hoisted";
```

Example 02: Function Hoisting

---

```js
function hoist() {
  a = 20;
  var b = 100;
}

hoist();

console.log(a);
/* 
Accessible as a global variable outside hoist() function
Output: 20
*/

console.log(b);
/*
Since it was declared, it is confined to the hoist() function scope.
We can't print it out outside the confines of the hoist() function.
Output: ReferenceError: b is not defined
*/
```

All declarations (function, var, let, const and class) are hoisted in JavaScript, while the var declarations are initialized with undefined, but let and const declarations remain uninitialized.

```js
console.log(a);
let a = 3;

// Output: ReferenceError: a is not defined
```

They will only get initialized when their lexical binding (assignment) is evaluated during runtime by the JavaScript engine. This means we can’t access the variable before the engine evaluates its value at the place it was declared in the source code. This is what we call Temporal Dead Zone, A time span between variable creation and its initialization where they can’t be accessed.

</details>
<br/>

<details>
<summary>What are closures?</summary>
     A closure is the combination of a function and the lexical environment within which that function was declared. i.e, It is an inner function that has access to the outer or enclosing function’s variables. The closure has three scope chains.

- Own scope where variables defined between its curly brackets
- Outer function’s variables
- Global variables

```js
function Welcome(name) {
  var greetingInfo = function (message) {
    console.log(message + " " + name);
  };
  return greetingInfo;
}
var myFunction = Welcome("Prabir");
myFunction("Welcome "); // Output: Welcome prabir
```

As per the above code, the inner function greetingInfo() has access to the variables in the outer function Welcome() even after outer function has returned.

</details>
<br/>

<details>
<summary>How do you clone an object in JavaScript?</summary>
Using the object spread operator ..., the object own enumerable properties can be copied into the new object. This creates a shallow clone of the object.

```js
const obj = { a: 1, b: 2 };
const shallowClone = { ...obj };
```

With this technique, prototypes are ignored. In addition, nested objects are not cloned, but rather their references get copied, so nested objects still refer to the same objects as the original. Deep-cloning is much more complex in order to effectively clone any type of object (Date, RegExp, Function, Set, etc) that may be nested within the object.

Other alternatives include:

JSON.parse(JSON.stringify(obj)) can be used to deep-clone a simple object, but it is CPU-intensive and only accepts valid JSON (therefore it strips functions and does not allow circular references).
Object.assign({}, obj) is another alternative.
Object.keys(obj).reduce((acc, key) => (acc[key] = obj[key], acc), {}) is another more verbose alternative that shows the concept in greater depth.

</details>
<br/>

<details>
<summary>What is variable shadowing in javascript?</summary>
Variable shadowing occurs when a variable declared within a certain scope (decision block, method, or inner class) has the same name as a variable declared in an outer scope. This outer variable is said to be shadowed.

If there is a variable in the global scope, and you'd like to create a variable with the same name in a function. The variable in the inner scope will temporarily shadow the variable in the outer scope.

```js
var value = 20;

function Hoist(value) {
  alert(value);
}

Hoist(30); //output:30
```

</details>
<br/>

<details>
<summary>What is an event flow?</summary>
Event flow is the order in which event is received on the web page. When you click an element that is nested in various other elements, before your click actually reaches its destination, or target element, it must trigger the click event each of its parent elements first, starting at the top with the global window object.

There are two ways of event flow

- Top to Bottom(Event Capturing)
- Bottom to Top (Event Bubbling)
</details>
<br/>

<details>
<summary>What is prototype chain?</summary>
Nearly all objects in JavaScript are instances of Object. That means all the objects in JavaScript inherit the properties and methods from Object.prototype. This is called Prototype chaining.

Prototype chaining is used to build new types of objects based on existing ones. It is similar to inheritance in a class based language. The prototype on object instance is available through Object.getPrototypeOf(object) or **proto** property whereas prototype on constructors function is available through Object.prototype.

```js
   function Person(firstName, lastName, age) {
  this.firstName = firstName;
  this.lastName = lastName;
  this.age = age;
}
//Person class created
Person.prototype.getFullName = function() {
  return this.firstName + " " + this.lastName;
}

// we have added getFullName method in Person’s prototype.
var person = new Person("Prabir", "Kumar", 25);
// It will create an instance of the Person class
> person.hasOwnProperty("firstName");  // true
> person.hasOwnProperty("getFullName");  // false
> person.getFullName(); // Prabir Kumar

```

</details>
<br/>

<details>
<summary>What is the difference between Call, Apply and Bind?</summary>

- call():

     The call() method invokes a function with a given this value and arguments provided one by one

     ---

     ```js
              var employee1 = {firstName: 'Prabir', lastName: 'Kumar'};
              var employee2 = {firstName: 'Kumar', lastName: 'P'};

             function greet(greeting1, greeting2) {
              console.log(greeting1 + ' ' + this.firstName + ' ' + this.lastName+ ', '+ greeting2);
             }

             greet.call(employee1, 'Hello', 'How are you?'); // Hello Prabir Kumar, How are you?
            greet.call(employee2, 'Hello', 'How are you?'); // Hello Kumar P, How are you?
      
         ```
- apply():
           Invokes the function and allows you to pass in arguments as an array
---
```js
 var employee1 = {firstName: 'Prabir', lastName: 'Kumar'};
 var employee2 = {firstName: 'Kumar', lastName: 'P'};

    function greet(greeting1, greeting2) {

    console.log(greeting1 + ' ' + this.firstName + ' ' + this.lastName+ ', '+ greeting2);
         }

    greet.apply(employee1, ['Hello', 'How are you?']); // Hello Prabir Kumar, How are you?
    greet.apply(employee2, ['Hello', 'How are you?']); // Hello Kumar P, How are you?        

```
- bind():

returns a new function, allowing you to pass in an array and any number of arguments

```js
var employee1 = {firstName: 'Prabir', lastName: 'Kumar'};
var employee2 = {firstName: 'Kumar', lastName: 'P'};

function greet(greeting1, greeting2) {
    console.log(greeting1 + ' ' + this.firstName + ' ' + this.lastName+ ', '+ greeting2);
}

var inviteEmployee1 = greet.bind(employee1);
var inviteEmployee2 = greet.bind(employee2);
inviteEmployee1('Hello', 'How are you?'); // Hello Prabir Kumar, How are you?
inviteEmployee2('Hello', 'How are you?'); // Hello Kumar P, How are you?

```

  </details>
  <br/>

<details>
<summary>What is a higher order function?</summary>

A Higher-Order function is a function that receives a function as an argument or returns the function as output.

For example, Array.prototype.map(), Array.prototype.filter() and Array.prototype.reduce() are some of the Higher-Order functions in javascript.

```js
const arr1 = [10, 20, 30];
const arr2 = arr1.map(function(item) {
  return item * 10;
});
console.log(arr2);
```
</details>
<br/>



<details>
<summary>What is a unary function?</summary>
Unary function (i.e. monadic) is a function that accepts exactly one argument. Let us take an example of unary function. It stands for single argument accepted by a function.

```js
const unaryFunction = a => console.log (a + 20); //Add 20 to the given argument and display the value
```
</details>
<br/>


<details>
<summary>What is currying function?</summary>

Currying is the process of taking a function with multiple arguments and turning it into a sequence of functions each with only a single argument.

```js
function volume(length) {
  return function(width) {
    return function(height) {
      return height * width * length;
    }
  }
}

volume(2)(6)(3); // 36
```
Curried functions are great to improve code re-usability and functional composition.
</details>
<br/>

<details>
<summary>What are the restrictions of web workers on DOM?</summary>
WebWorkers do not have access to below javascript objects since they are defined in an external files

  - Window object
  - Document object
  - Parent object
</details>
<br/>

<details>
<summary>What is a promise?</summary>
A promise is an object that may produce a single value some time in the future with either a resolved value or a reason that it’s not resolved(for example, network error). It will be in one of the 3 possible states: fulfilled, rejected, or pending. Syntax

---
```js
const promise = new Promise(function(resolve, reject) {
  // promise description
})
```
Promises are used to handle asynchronous operations. They provide an alternative approach for callbacks by reducing the callback hell and writing the cleaner code.

Promises have three states:

- Pending: This is an initial state of the Promise before an operation begins
- Fulfilled: This state indicates that specified operation was completed.
- Rejected: This state indicates that the operation did not complete. In this case an error value will be thrown.
</details>
<br/>

<details>
<summary>What is a callback function?</summary>
A callback function is a function passed into another function as an argument. This function is invoked inside the outer function to complete an action.

```js
function add(a, b, callback) {
  const result = a + b;
  callback(result);
}

function logResult(result) {
  console.log(result);
}

add(2, 3, logResult); // logs "5"

```
In this example, we have a add function that takes three arguments: two numbers (a and b) and a callback function. The add function performs a simple addition operation and then invokes the callback function with the result.

We also have a second function called logResult that takes a single argument (the result of the addition) and logs it to the console.

In the last line of the example, we are calling the add function and passing it the numbers 2 and 3, along with the logResult function as a callback. This causes the add function to invoke the logResult function, passing it the result of the addition (5), which in turn logs the result to the console.
</details>
<br/>

<details>
<summary>Why do we need callbacks?</summary>

The callbacks are needed because javascript is a event driven language. That means instead of waiting for a response javascript will keep executing while listening for other events.

Let us take an example with first function invoking an API call(simulated by setTimeout) and next function which logs the message

```js
function firstFunction() {
  // Simulate a code delay
  setTimeout( function() {
    console.log('First function called');
  }, 1000 );
}
function secondFunction() {
  console.log('Second function called');
}
firstFunction();
secondFunction();

Output
// Second function called
// First function called

```
As observed from the output, javascript didnot wait for the response of first function and remaining code block get executed. So callbacks used in a way to make sure that certain code does not execute until other code finished execution.
</details>
<br/>

<details>
<summary>What is a callback hell?</summary>
Callback Hell is an anti-pattern with multiple nested callbacks which makes code hard to read and debug when dealing with asynchronous logic. The callback hell looks like below,

---
```js
async1(function() {
    async2(function() {
        async3(function() {
            async4(function() {
                ....
            });
        });
    });
});

```
</details>
<br/>

<details>
<summary>What is promise chaining?</summary>
The process of executing a sequence of asynchronous tasks one after another using promises is known as Promise chaining.

```js
new Promise(function(resolve, reject) {

  setTimeout(() => resolve(1), 1000);

}).then(function(result) {

  console.log(result); // 1
  return result * 2;

}).then(function(result) {

  console.log(result); // 2
  return result * 3;

}).then(function(result) {

  console.log(result); // 6
  return result * 4;

});
```
In the above handlers, the result is passed to the chain of .then() handlers with the below work flow,

The initial promise resolves in 1 second,
After that .then handler is called by logging the result(1) and then return a promise with the value of result * 2.
After that the value passed to the next .then handler by logging the result(2) and return a promise with result * 3.
Finally the value passed to the last .then handler by logging the result(6) and return a promise with result * 4.

</details>
<br/>


<details>
<summary>What is eval?</summary>
The eval() function evaluates JavaScript code represented as a string. The string can be a JavaScript expression, variable, statement, or sequence of statements.

```js
 console.log(eval('3 + 2')); //  5
```
</details>
<br/>

<details>
<summary>What is isNaN?</summary>
The isNaN() function is used to determine whether a value is an illegal number (Not-a-Number) or not. i.e, This function returns true if the value equates to NaN. Otherwise it returns false.

```js
isNaN('Hello') //true
isNaN('100') //false
typeof(NaN) //Number
```
</details>
<br/>

<details>
<summary>What are the pros and cons of promises over callbacks?
</summary>
Below are the list of pros and cons of promises over callbacks,
Pros:

- It avoids callback hell which is unreadable
- Easy to write sequential asynchronous code with .then()
- Easy to write parallel asynchronous code with Promise.all()
- Solves some of the common problems of callbacks(call the callback too late, too early, many times and swallow errors/exceptions)
  
Cons:

- It makes little complex code
- You need to load a polyfill if ES6 is not supported
</details>
<br/>

<details>
<summary>What is the difference between an attribute and a property?
</summary>
Attributes are defined on the HTML markup whereas properties are defined on the DOM. For example, the below HTML element has 2 attributes type and value,


```js
<input type="text" value="Name:">
```
You can retrieve the attribute value as below,

```js
const input = document.querySelector('input');
console.log(input.getAttribute('value')); // Good morning
console.log(input.value); // Good morning
```

And after you change the value of the text field to "Good evening", it becomes like

```js
console.log(input.getAttribute('value')); // Good morning
console.log(input.value); // Good evening

```
</details>
<br/>

<details>
<summary>What is the purpose of void(0)?</summary>
The void(0) is used to prevent the page from refreshing. This will be helpful to eliminate the unwanted side-effect, because it will return the undefined primitive value. It is commonly used for HTML document that uses href="JavaScript:void(0);" within an anchor(a) element. i.e, when you click a link, the browser loads a new page or refreshes the same page. But this behavior will be prevented using this expression.
For example, the below link notify the message without reloading the page

```js
<a href="JavaScript:void(0);" onclick="alert('Well done!')">Click Me!</a>

```
</details>
<br/>


<details>
<summary>Is JavaScript a compiled or interpreted language?</summary>
JavaScript is an interpreted language, not a compiled language. An interpreter in the browser reads over the JavaScript code, interprets each line, and runs it. Nowadays modern browsers use a technology known as Just-In-Time (JIT) compilation, which compiles JavaScript to executable bytecode just as it is about to run.
</details>
<br/>


<details>
<summary>Is JavaScript a case-sensitive language?</summary>
Yes, JavaScript is a case sensitive language. The language keywords, variables, function & object names, and any other identifiers must always be typed with a consistent capitalization of letters.

</details>
<br/>


<details>
<summary>What is BOM?
</summary>
The Browser Object Model (BOM) allows JavaScript to "talk to" the browser. It consists of the objects navigator, history, screen, location and document which are children of window. The Browser Object Model is not standardized and can change based on different browsers.

</details>
<br/>


<details>
<summary>What is the use of setTimeout?</summary>
The setTimeout() method is used to call a function or evaluates an expression after a specified number of milliseconds. For example, let us log a message after 2 seconds using setTimeout method,

```js
setTimeout(function() { console.log("Heyy Prabir"); }, 2000);

```

</details>
<br/>


<details>
<summary>What is the use of setInterval?
</summary>
The setInterval() method is used to call a function or evaluates an expression at specified intervals (in milliseconds). For example, let us log a message after 2 seconds using setInterval method,

```js
setInterval(function() { console.log("Heyy Prabir"); }, 2000);

```
</details>
<br/>


<details>
<summary>Why is JavaScript treated as Single threaded?
</summary>
JavaScript is a single-threaded language. Because the language specification does not allow the programmer to write code so that the interpreter can run parts of it in parallel in multiple threads or processes. Whereas languages like java, go, C++ can make multi-threaded and multi-process programs.
</details>
<br/>


<details>
<summary>What is an event delegation?</summary>
Event delegation is a technique for listening to events where you delegate a parent element as the listener for all of the events that happen inside it. For example, if you wanted to detect field changes in inside a specific form, you can use event delegation technique,

```js
var form = document.querySelector('#registration-form');

// Listen for changes to fields inside the form
form.addEventListener('input', function (event) {

// Log the field that was changed
console.log(event.target);

}, false);

```

</details>
<br/>


<details>
<summary>What is the purpose JSON stringify?</summary>
When sending data to a web server, the data has to be in a string format. You can achieve this by converting JSON object into a string using stringify() method.

```js
var userJSON = {'name': 'Prabir', age: 25}
var userString = JSON.stringify(user);
console.log(userString); //"{"name":"Prabir","age":25}"

```
</details>
<br/>


<details>
<summary>How do you parse JSON string?</summary>
When receiving the data from a web server, the data is always in a string format. But you can convert this string value to javascript object using parse() method.

```js
var userString = '{"name":"Prabir","age":25}';
var userJSON = JSON.parse(userString);
console.log(userJSON);// {name: "Prabir", age: 25}

```
</details>
<br/>


<details>
<summary>What is the purpose of clearTimeout method?</summary>

The clearTimeout() function is used in javascript to clear the timeout which has been set by setTimeout() function before that. i.e, The return value of setTimeout() function is stored in a variable and it’s passed into the clearTimeout() function to clear the timer. For example, the below setTimeout method is used to display the message after 3 seconds. This timeout can be cleared by clearTimeout() method.

```js
var msg;
function greeting() {
  alert('Heyy Prabir');
}
function start() {
  msg =setTimeout(greeting, 4000);
}
function stop() {
    clearTimeout(msg);
}

```
</details>
<br/>


<details>
<summary>What is the purpose of clearInterval method?</summary>
The clearInterval() function is used in javascript to clear the interval which has been set by setInterval() function. i.e, The return value returned by setInterval() function is stored in a variable and it’s passed into the clearInterval() function to clear the interval. For example, the below setInterval method is used to display the message for every 3 seconds. This interval can be cleared by clearInterval() method.

```js
var msg;
function greeting() {
  alert('Heyy Prabir');
}
function start() {
  msg =setInterval(greeting, 4000);
}
function stop() {
    clearInterval(msg);
}

```
</details>
<br/>

<details>
<summary>How do you redirect new page in javascript?
</summary>
In vanilla javascript, you can redirect to a new page using location property of window object. The syntax would be as follows,

```js
function redirect() {
  window.location.href = 'newPage.html';
}

```
</details>
<br/>


<details>
<summary>How do you check whether a string contains a substring?
</summary>
There are 3 possible ways to check whether a string contains a substring or not,

---
a.) Using includes: ES6 provided String.prototype.includes method to test a string contains a substring.

```js
var mainString = "prabir", subString = "prab";
mainString.includes(subString)

```
---
b.) Using indexOf: In an ES5 or older environments, you can use String.prototype.indexOf which returns the index of a substring. If the index value is not equal to -1 then it means the substring exist in the main string.

```js
var mainString = "prabir", subString = "prab";
mainString.indexOf(subString) !== -1

```
---
c.) Using RegEx: The advanced solution is using Regular expression test method(RegExp.test), which allows for testing for against regular expressions

```js
var mainString = "prabir", regex = "/prab/";
regex.test(mainString)

```

</details>
<br/>

<details>
<summary>What are break and continue statements?</summary>
The break statement is used to "jumps out" of a loop. i.e, It breaks the loop and continues executing the code after the loop.

```js
for (i = 0; i < 10; i++) {
  if (i === 5) { break; }
  text += "Number: " + i + "<br>";
}

```
The continue statement is used to "jumps over" one iteration in the loop. i.e, It breaks one iteration (in the loop), if a specified condition occurs, and continues with the next iteration in the loop.

```js
for (i = 0; i < 10; i++) {
    if (i === 5) { continue; }
    text += "Number: " + i + "<br>";
}
```

</details>
<br/>

<details>
<summary>How do you define JSON arrays?</summary>
JSON arrays are written inside square brackets and array contain javascript objects. For example, the JSON array of users would be as below,

```js
"users":[
  {"firstName":"Prabir", "lastName":"Kumar"},
  {"firstName":"Anurag", "lastName":"Tiwari"},
  {"firstName":"Prithvi", "lastName":"Raj"}
]

```
</details>
<br/>


<details>
<summary>How do you generate random integers?
</summary>
You can use Math.random() with Math.floor() to return random integers. For example, if you want generate random integers between 1 to 10, the multiplication factor should be 10,

```js
Math.floor(Math.random() * 10) + 1;     // returns a random integer from 1 to 10
Math.floor(Math.random() * 100) + 1;     // returns a random integer from 1 to 100
```
</details>
<br/>

<details>
<summary>How do you change style of a HTML element in javascript?</summary>
You can change inline style or classname of a HTML element using javascript

  1. Using style property: You can modify inline style using style property

  ```js
document.getElementById("title").style.fontSize = "40px";
  ```

   2. Using ClassName property: It is easy to modify element class using className property
```js
document.getElementById("title").style.className = "custom-title";

```
</details>
<br/>

<details>
<summary>What is a debugger statement?</summary>
The debugger statement invokes any available debugging functionality, such as setting a breakpoint. If no debugging functionality is available, this statement has no effect. For example, in the below function a debugger statement has been inserted. So execution is paused at the debugger statement just like a breakpoint in the script source.

```js
function getProfile() {
// code goes here
debugger;
// code goes here
}

```
</details>
<br/>

<details>
<summary>What is the purpose of breakpoints in debugging?</summary>
You can set breakpoints in the javascript code once the debugger statement is executed and debugger window pops up. At each breakpoint, javascript will stop executing, and let you examine the JavaScript values. After examining values, you can resume the execution of code using play button.
</details>
<br/>

<details>
<summary>Can I use reserved words as identifiers?</summary>
No, you cannot use the reserved words as variables, labels, object or function names.

```js
var else = "hello"; // Uncaught SyntaxError: Unexpected token else

```
</details>
<br/>

<details>
<summary>What is a conditional operator in javascript?</summary>
The conditional (ternary) operator is the only JavaScript operator that takes three operands which acts as a shortcut for if statement.

```js
var isAuthenticated = false;
console.log(isAuthenticated ? 'Hello, welcome' : 'Sorry, you are not authenticated');
```
</details>
<br/>

<details>
<summary>Can you apply chaining on conditional operator?
</summary>
Yes, you can apply chaining on conditional operator similar to if … else if … else if … else chain. The syntax is going to be as below,

```js
function traceValue(someParam) {
    return condition1 ? value1
        : condition2 ? value2
        : condition3 ? value3
        : value4;
}

// The above conditional operator is equivalent to:

function traceValue(someParam) {
    if (condition1) { return value1; }
    else if (condition2) { return value2; }
    else if (condition3) { return value3; }
    else { return value4; }
}

```
</details>
<br/>

<details>
<summary>What is the difference between proto and prototype?</summary>
          The __proto__ object is the actual object that is used in the lookup chain to resolve methods, etc. Whereas prototype is the object that is used to build __proto__ when you create an object with new

   ```js
( new Employee ).__proto__ === Employee.prototype;
( new Employee ).prototype === undefined;

   ```
</details>
<br/>

<details>
<summary>How can you get the list of keys of any object?
</summary>
You can use Object.keys() method which is used return an array of a given object's own property names, in the same order as we get with a normal loop. For example, you can get the keys of a user object,

```js
const user = {
  name: 'Prabir',
  gender: 'male',
  age: 40
};

console.log(Object.keys(user)); //['name', 'gender', 'age']

```
</details>
<br/>

<details>
<summary>How do you create an object with prototype?</summary>
The Object.create() method is used to create a new object with the specified prototype object and properties. i.e, It uses existing object as the prototype of the newly created object. It returns a new object with the specified prototype object and properties.

```js
const user = {
  name: 'Prabir',
  printInfo: function () {
    console.log(`My name is ${this.name}.`);
  }
};

const admin = Object.create(person);
admin.name = "Kumar"; // Remember that "name" is a property set on "admin" but not on "user" object
admin.printInfo(); // My name is Kumar

```
</details>
<br/>


<details>
<summary>What is the difference between uneval and eval?</summary>
The uneval() function returns the source of a given object; whereas the eval function does the opposite, by evaluating that source code in a different memory area.

```js
var msg = uneval(function greeting() { return 'Hello, Prabir Kumar'; });
var greeting = eval(msg);
greeting(); // returns "Hello, Prabir Kumar"

```
</details>
<br/>


<details>
<summary>What is an anonymous function?</summary>
An anonymous function is a function without a name! Anonymous functions are commonly assigned to a variable name or used as a callback function. The syntax would be as below,

```js
function (optionalParameters) {
  //do something
}

const myFunction = function(){ //Anonymous function assigned to a variable
  //do something
};

[1, 2, 3].map(function(element){ //Anonymous function used as a callback function
  //do something
});

```
Example:

```js
var x = function (a, b) {return a * b};
var z = x(2, 10);
console.log(z); // 20

```
</details>
<br/>

<details>
<summary>What is the precedence order between local and global variables?</summary>
A local variable takes precedence over a global variable with the same name.

---
```js
var msg = "Good morning";
function greeting() {
  msg = "Good Evening";
  console.log(msg);
}
greeting();

```
</details>
<br/>

<details>
<summary>What are javascript accessors?</summary>
ECMAScript 5 introduced javascript object accessors or computed properties through getters and setters. Getters uses get keyword whereas Setters uses set keyword.

```js
var user = {
  firstName: "Prabir",
  lastName : "Kumar",
  language : "en",
  get lang() {
    return this.language;
  }
  set lang(lang) {
  this.language = lang;
  }
};
console.log(user.lang); // getter access lang as en
user.lang = 'fr';
console.log(user.lang); // setter used to set lang as fr

```
</details>
<br/>

<details>
<summary>What are the various statements in error handling?</summary>
Below are the list of statements used in an error handling,

1. try: This statement is used to test a block of code for errors
2. catch: This statement is used to handle the error
3. throw: This statement is used to create custom errors.
4. finally: This statement is used to execute code after try and catch regardless of the result.
</details>
<br/>


<details>
<summary>Explain event delegation?
</summary>
Event delegation is a technique involving adding event listeners to a parent element instead of adding them to the descendant elements. The listener will fire whenever the event is triggered on the descendant elements due to event bubbling up the DOM. The benefits of this technique are:

- Memory footprint goes down because only one single handler is needed on the parent element, rather than having to attach event handlers on each descendant.
- There is no need to unbind the handler from elements that are removed and to bind the event for new elements.

</details>
<br/>


<details>
<summary>What is the difference between .call and .apply?</summary>
Both .call and .apply are used to invoke functions and the first parameter will be used as the value of this within the function. However, .call takes in comma-separated arguments as the next arguments while .apply takes in an array of arguments as the next argument. An easy way to remember this is C for call and comma-separated and A for apply and an array of arguments.

```js
function add(a, b) {
  return a + b;
}

console.log(add.call(null, 3, 2)); // 5
console.log(add.apply(null, [3, 2])); // 5
```
</details>
<br/>

<details>
<summary>Explain Function.prototype.bind?</summary>
The bind() method creates a new function that, when called, has its this keyword set to the provided value, with a given sequence of arguments preceding any provided when the new function is called.

In my experience, it is most useful for binding the value of this in methods of classes that you want to pass into other functions. This is frequently done in React components.


</details>
<br/>

<details>
<summary>Explain the difference between synchronous and asynchronous functions?</summary>

- Synchronous functions are blocking while asynchronous functions are not. In synchronous functions, statements complete before the next statement is run. In this case, the program is evaluated exactly in order of the statements and execution of the program is paused if one of the statements take a very long time.

- Asynchronous functions usually accept a callback as a parameter and execution continue on the next line immediately after the asynchronous function is invoked. The callback is only invoked when the asynchronous operation is complete and the call stack is empty. Heavy duty operations such as loading data from a web server or querying a database should be done asynchronously so that the main thread can continue executing other operations instead of blocking until that long operation to complete (in the case of browsers, the UI will freeze).


</details>
<br/>

<details>
<summary>What is event loop? What is the difference between call stack and task queue?</summary>


 - The event loop is a single-threaded loop that monitors the call stack and checks if there is any work to be done in the task queue. If the call stack is empty and there are callback functions in the task queue, a function is dequeued and pushed onto the call stack to be executed.

- If you haven't already checked out Philip Robert's talk on the Event Loop, you should. It is one of the most viewed videos on JavaScript

</details>
<br/>

<details>
<summary>What is the difference between undefined and not defined in JavaScript?</summary>

```js
var x; // declaring x
console.log(x); // output: undefined
```

var x = 1 is both declaration and definition (also we can say we are doing initialisation), Here declaration and assignment of value happen inline for variable x, In JavaScript every variable declaration and function declaration brings to the top of its current scope in which It is declared then assignment happen in order this term is called hoisting.

A variable can be declared but not defined. When we try to access it, It will result undefined.

```js
var x; // Declaration
typeof x === 'undefined'; // Will return true

```
A variable can be neither declared nor defined. When we try to reference such variable then the result will be not defined.

```js
console.log(y);  // Output: ReferenceError: y is not defined
```
</details>
<br/>


<details>
<summary>What is closures ?</summary>
A closure is a function object that has access to variables in its enclosing lexical scope, even when the function is invoked outside that scope. In other words, a closure gives you access to an outer function's scope from an inner function.

```js
function outerFunction(x) {
  let outerVariable = x;
  
  return function innerFunction(y) {
    return outerVariable + y;
  }
}

let closure = outerFunction(10);
console.log(closure(5)); // 15


```

In this example, the inner function innerFunction is a closure. It has access to the outerVariable variable from its enclosing scope (the outerFunction). When we invoke the closure by calling closure(5), it returns the value of outerVariable + y (10 + 5), which is 15.

A closure is created when an inner function is defined inside an outer function, and the inner function references variables defined in the outer function. The inner function is returned from the outer function, and when it's invoked it has access to the scope of the outer function.
</details>
<br/>


<details>
<summary>What is the difference between typeof and instanceof?</summary>
typeof is an operator that returns a string with the type of whatever you pass.

The typeof operator checks if a value belongs to one of the seven basic types: number, string, boolean, object, function, undefined or Symbol.

typeof(null) will return object.

instanceof is much more intelligent: it works on the level of prototypes. In particular, it tests to see if the right operand appears anywhere in the prototype chain of the left. instanceof doesn’t work with primitive types. It instanceof operator checks the current object and returns true if the object is of the specified type, for example:

```js
var dog = new Animal();
dog instanceof Animal; // Output : true

```
Here dog instanceof Animal is true since dog inherits from Animal.prototype

```js
var name = new String("xyz");
name instanceof String; // Output : true
```
</details>
<br/>


<details>
<summary>What is the difference between a method and a function in javascript?</summary>
In JS, that difference is quite subtle. A function is a piece of code that is called by name and function itself not associated with any object and not defined inside any object. It can be passed data to operate on (i.e. parameter) and can optionally return data (the return value).

---
```js
// Function statement
function myFunc() {
  // Do some stuff;
}

// Calling the function
myFunc();
```
Here myFunc() function call is not associated with object hence not invoked through any object.

A function can take a form of immediately invoked function expression (IIFE):

```js

// Anonymous Self-invoking Function
(function() {
  // Do some stuff;
})();

```
Finally there are also arrow functions:

```js
const myFunc = arg => {
    console.log("hello", arg)
} 
```
A method is a piece of code that is called by its name and that is associated with the object. Methods are functions. When you call a method like this obj1.myMethod(), the reference to obj1 gets assigned (bound) to this variable. In other words, the value of this will be obj1 inside myMethod.
</details>
<br/>


<details>
<summary>What are promises and how they are useful?</summary>
We use promises for handling asynchronous interactions in a sequential manner. They are especially useful when we need to do an async operation and THEN do another async operation based on the results of the first one. For example, if you want to request the list of all flights and then for each flight you want to request some details about it. The promise represents the future value. It has an internal state (pending, fulfilled and rejected) and works like a state machine.

A promise object has then method, where you can specify what to do when the promise is fulfilled or rejected.

You can chain then() blocks, thus avoiding the callback hell. You can handle errors in the catch() block. After a promise is set to fulfilled or rejected state, it becomes immutable.
</details>
<br/>


<details>
<summary>What is this keyword in javascript? </summary>
The following rules are applied when we use this keyword in javascript

1. If the new keyword is used when calling the function, this inside the function is a brand new object.
2. If apply, call, or bind are used to call/create a function, this inside the function is the object that is passed in as the argument.
3. If a function is called as a method, such as obj.method() — this is the object that the function is a property of.
4. If a function is invoked as a free function invocation, meaning it was invoked without any of the conditions present above, this is the global object. In a browser, it is the window object. If in strict mode ('use strict'), this will be undefined instead of the global object.
5. If multiple of the above rules apply, the rule that is higher wins and will set the this value.
6. If the function is an ES2015 arrow function, it ignores all the rules above and receives the this value of its surrounding scope at the time it is created.
</details>
<br/>


<details>
<summary>What is the purpose of array slice method?
</summary>
The slice() method returns the selected elements in an array as a new array object. It selects the elements starting at the given start argument, and ends at the given optional end argument without including the last element. If you omit the second argument then it selects till the end. Some of the examples of this method are,

```js
let arrayIntegers = [1, 2, 3, 4, 5];
let arrayIntegers1 = arrayIntegers.slice(0,2); // returns [1,2]
let arrayIntegers2 = arrayIntegers.slice(2,3); // returns [3]
let arrayIntegers3 = arrayIntegers.slice(4); //returns [5]
```
Note: Slice method wonot mutate the original array but it returns the subset as new array.


</details>
<br/>


<details>
<summary>What is shallow copy and deep copy in javascript?</summary>

Shallow copy:

Shallow copy is a bit-wise copy of an object. A new object is created that has an exact copy of the values in the original object. If any of the fields of the object are references to other objects, just the reference addresses are copied i.e., only the memory address is copied.

Deep copy:

A deep copy copies all fields, and makes copies of dynamically allocated memory pointed to by the fields. A deep copy occurs when an object is copied along with the objects to which it refers.

A Shallow copy of the object can be done using object.assign() method in javascript.

---

```js
let obj = {
  a: 1,
  b: 2,
};
let objCopy = Object.assign({}, obj);
console.log(objCopy); // Result - { a: 1, b: 2 }
```
A Deep copy of the object can be done using JSON.parse(JSON.stringify(object));

---

```js
let obj = { 
  a: 1,
  b: { 
    c: 2,
  },
}
let newObj = JSON.parse(JSON.stringify(obj));
obj.b.c = 20;
console.log(obj); // { a: 1, b: { c: 20 } }
console.log(newObj); // { a: 1, b: { c: 2 } } (New Object Intact!)

```
</details>
<br/>


<details>
<summary>How to avoid callback hell in javascript?</summary>
Callback hell is a phenomenon that afflicts a JavaScript developer when he tries to execute multiple asynchronous operations one after the other. Some people call it to be the pyramid of doom.

Example:
```js
doSomething(param1, param2, function(err, paramx){
    doMore(paramx, function(err, result){
        insertRow(result, function(err){
            yetAnotherOperation(someparameter, function(s){
                somethingElse(function(x){
                });
            });
        });
    });
});
```
Techniques for avoiding callback hell

- Write comments
- Split functions into smaller functions
- Using Async.js
- Using Promises
- Using Async-Await

</details>
<br/>

<details>
<summary>How do you detect primitive or non primitive value type?</summary>
In JavaScript, primitive types include boolean, string, number, BigInt, null, Symbol and undefined. Whereas non-primitive types include the Objects. But you can easily identify them with the below function,

```js
var myPrimitive = 30;
var myNonPrimitive = {};
function isPrimitive(val) {
  return Object(val) !== val;
}

isPrimitive(myPrimitive);
isPrimitive(myNonPrimitive);

```
If the value is a primitive data type, the Object constructor creates a new wrapper object for the value. But If the value is a non-primitive data type (an object), the Object constructor will give the same object.
</details>
<br/>

<details>
<summary>What is babel</summary>
Babel is a JavaScript transpiler to convert ECMAScript 2015+ code into a backwards compatible version of JavaScript in current and older browsers or environments. Some of the main features are listed below,

 - Transform syntax
 - Polyfill features that are missing in your target environment (using @babel/polyfill)
- Source code transformations (or codemods)

</details>
<br/>

<details>
<summary>What are the different ways to deal with Asynchronous Code</summary>
        Below are the list of different ways to deal with Asynchronous code.

- Callbacks
- Promises
- Async/await
- Third-party libraries such as async.js,bluebird etc
</details>
<br/>

<details>
<summary>What is a thunk function</summary>
A thunk is just a function which delays the evaluation of the value. It doesn’t take any arguments but gives the value whenever you invoke the thunk. i.e, It is used not to execute now but it will be sometime in the future. Let's take a synchronous example,

```js

const add = (x, y) => x + y;

const thunk = () => add(2, 3);

thunk(); // 5
```
</details>
<br/>

<details>
<summary>What are asynchronous thunks</summary>
The asynchronous thunks are useful to make network requests. Let's see an example of network requests,

```js
function fetchData(fn) {
  fetch("https://jsonplaceholder.typicode.com/todos/1")
    .then((response) => response.json())
    .then((json) => fn(json));
}

const asyncThunk = function () {
  return fetchData(function getData(data) {
    console.log(data);
  });
};

asyncThunk();
```
The getData function won't be called immediately but it will be invoked only when the data is available from API endpoint. The setTimeout function is also used to make our code asynchronous. The best real time example is redux state management library which uses the asynchronous thunks to delay the actions to dispatch.
</details>
<br/>


<details>
<summary>Is JavaScript faster than server side script ?</summary>
Yes, JavaScript is faster than server side script. Because JavaScript is a client-side script it does not require any web server’s help for its computation or calculation. So JavaScript is always faster than any server-side script like ASP, PHP, etc.
</details>
<br/>

<details>
<summary>What paradigm is Javascript</summary>
JavaScript is a multi-paradigm language, supporting imperative/procedural programming, Object-Oriented Programming and functional programming. JavaScript supports Object-Oriented Programming with prototypical inheritance.
</details>
<br/>

<details>
<summary>What are template literals</summary>
Template literals or template strings are string literals allowing embedded expressions. These are enclosed by the back-tick (`) character instead of double or single quotes. In E6, this feature enables using dynamic expressions as below,

```js
 var greeting = `Welcome to JS World, Mr. ${firstName} ${lastName}.`;

 //In ES5, you need break string like below,

 var greeting = 'Welcome to JS World, Mr. ' + firstName + ' ' + lastName.`
```
Note: You can use multi-line strings and string interpolation features with template literals.


</details>
<br/>

<details>
<summary>How do you write multi-line strings in template literals</summary>
In ES5, you would have to use newline escape characters('\n') and concatenation symbols(+) in order to get multi-line strings.

```js
console.log("This is string sentence 1\n" + "This is string sentence 2");

```
  Whereas in ES6, You don't need to mention any newline sequence character,

  ```js
console.log(`This is string sentence
'This is string sentence 2`);

  ```
</details>
<br/>


<details>
<summary>What is DOM?</summary>
DOM stands for Document Object Model.  DOM is a programming interface for HTML and XML documents.
When the browser tries to render an HTML document, it creates an object based on the HTML document called DOM. Using this DOM, we can manipulate or change various elements inside the HTML document.

 - Example of how HTML code gets converted to DOM:
  ---
```js
  <html>
  <head>
  <title>
    JAVASCRIPT
    </title>
    </head>
    <body>
    <p>I love js</p>
    </body>
    </html>

```
</details>
<br/>


<details>
<summary>What is the difference between null and undefined</summary>

 1. Null:
   - It is an assignment value which indicates that variable points to no object.
   - Type of null is object.
   - The null value is a primitive value that represents the null, empty, or non-existent reference.
   - Indicates the absence of a value for a variable.
   - Converted to zero (0) while performing primitive operations.
  
  2. Undefined:
  - It is not an assignment value where a variable has been declared but has not yet been assigned a value.
  - Type of undefined is undefined.
  - The undefined value is a primitive value used when a variable has not been assigned a value.
  - Indicates absence of variable itself.
  - Converted to NaN while performing primitive operations
</details>
<br/>

<details>
<summary>What is the difference between window and document
</summary>

 1. Window:

- It is the root level element in any web page.
- By default window object is available implicitly in the page.
- It has methods like alert(), confirm() and properties like document, location.
  2. Document:
  - It is the direct child of the window object. This is also known as Document Object Model(DOM).
  - You can access it via window.document or document.
  - It provides methods like getElementById, getElementsByTagName, createElement etc.
</details>
<br/>

<details>
<summary>What are modules
</summary>
Modules refer to small units of independent, reusable code and also act as the foundation of many JavaScript design patterns. Most of the JavaScript modules export an object literal, a function, or a constructor.
</details>
<br/>

<details>
<summary>Why do you need modules</summary>
Below are the list of benefits using modules in javascript ecosystem

- Maintainability
- Reusability
- Namespacing

</details>
<br/>


<details>
<summary>What is scope in javascript
</summary>
Scope is the accessibility of variables, functions, and objects in some particular part of your code during runtime. In other words, scope determines the visibility of variables and other resources in areas of your code.
</details>
<br/>

<details>
<summary>How do you compare Object and Map</summary>
Objects are similar to Maps in that both let you set keys to values, retrieve those values, delete keys, and detect whether something is stored at a key. Due to this reason, Objects have been used as Maps historically. But there are important differences that make using a Map preferable in certain cases.

- The keys of an Object are Strings and Symbols, whereas they can be any value for a Map, including functions, objects, and any primitive.
- The keys in Map are ordered while keys added to Object are not. Thus, when iterating over it, a Map object returns keys in order of insertion.
- You can get the size of a Map easily with the size property, while the number of properties in an Object must be determined manually.
- A Map is an iterable and can thus be directly iterated, whereas iterating over an Object requires obtaining its keys in some fashion and iterating over them.
- An Object has a prototype, so there are default keys in the map that could collide with your keys if you're not careful. As of ES5 this can be bypassed by using map = Object.create(null), but this is seldom done.
- A Map may perform better in scenarios involving frequent addition and removal of key pairs.
</details>
<br/>


<details>
<summary>What is the difference between slice and splice
</summary>

1. Slice:
   - Doesn't modify the original array(immutable) .
   - Returns the subset of original array.
   - Used to pick the elements from array.
2. Splice:
   - Modifies the original array(mutable).
   - Returns the deleted elements as array.
</details>
<br/>
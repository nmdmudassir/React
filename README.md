# React

React is a JavaScript library for building user interfaces.

React is used to build single-page applications.

React allows us to create reusable UI components.


**-->Define UI**

The User Interface (UI) is the point of human-computer interaction and communication in a device.This can include display screens,keyboard, a mouse and the appearance of a desktop.

##  what is React?

React, sometimes referred to as a frontend JavaScript framework, is a JavaScript library created by Facebook.

React is a tool for building UI components.

It is also known as ReactJs and React.js , so don't get confused if you read different notation in different places.

React knows only one thing that is to create an awesome UI.

### Why React?

Created and Maintained By facebook.

It has a huge community in github.

Component Based architecture.

### How does React works?

React creates a VIRTUAL DOM in memory.

Instead of manipulating the browser's DOM directly, React creates a virtual DOM in memory, where it does all the necessary manipulating, before making the changes in the browser DOM.

React only changes what needs to be changed!

React finds out what changes have been made, and changes only what needs to be changed.

### React.js History

Current version of React.JS is V18.0.0 (April 2022).

Initial Release to the Public (V0.3.0) was in July 2013.

React.JS was first used in 2011 for Facebook's Newsfeed feature.

Facebook Software Engineer, Jordan Walke, created it.

Current version of create-react-app is v5.0.1 (April 2022).

create-react-app includes built tools such as webpack, Babel, and ESLint.

### React Features

JSX − JSX is JavaScript syntax extension. It isn't necessary to use JSX in React development, but it is recommended.

Components − React is all about components. You need to think of everything as a component. This will help you maintain the code when working on larger scale projects.

Unidirectional data flow and Flux − React implements one-way data flow which makes it easy to reason about your app. Flux is a pattern that helps keeping your data unidirectional.

License − React is licensed under the Facebook Inc. Documentation is licensed under CC BY 4.0.

### React Advantage

Uses virtual DOM which is a JavaScript object. This will improve apps performance, since JavaScript virtual DOM is faster than the regular DOM.

Can be used on client and server side as well as with other frameworks.

Component and data patterns improve readability, which helps to maintain larger apps.

### React Limitations

Covers only the view layer of the app, hence you still need to choose other technologies to get a complete tooling set for development.

Uses inline templating and JSX, which might seem awkward to some developers.

### Prerequisites for React?

1: Basic Knowledge of Html , css and Javascript.

2: Basic Understanding of ES6 Features.

3: Basic Understanding of how to use npm(Node Package Manager).


# Installation of React

1. install Node.js

Node.js actually provides a runtime environment to execute JavaScript code from outside a browser. NPM, the 

default package manager for Nodejs is used for managing and sharing the packages for any JavaScript project. 

React uses Node.js and NPM for the management of dependencies and runtime.

In this tutorial, we are going to install the create-react-app tool using the Node Package Manager(NPM). 

Create-react-app is a tool developed by the React.js team that makes React’s setting up easier.

So first, it needs to install Nodejs on our system. NPM will be installed with Nodejs. The current stable 

version of Node.js can be downloaded and installed from the official website that is given below.

---> https://nodejs.org

Download the latest version and install it. Here we can choose the LTS or the latest version. Because both of 

the version supports React.

After the installation, check the versions using the below commands.

---> node -v

---> npm -v

This will show the installed versions of Node.js and NPM.

2. Install visual Studio code /Sublime/Atom/Brackets.

3. Create a New React Project

After the successful installation of Nodejs and NPM, we can create a new React project by temporarily 

installing the create-react-app tool. Execute the below command on the Command prompt window.

---> npx create-react-app awesome-project

Here NPX will temporarily install create-react-app and create a new react project named awesome-project. Note 

that the awesome-project is the name I have chosen for my react project.

4. Running the Application

So the app we created can run locally on our system with the npm start command.

---> cd awesome-project

To start the server for the development:

---> npm start

This will open up the react application in a new tab of our browser with the below URL.

---> http://localhost:3000

<br>

## React ES6

What is ES6?

ES6 stands for ECMAScript 6.

ECMAScript was created to standardize JavaScript, and ES6 is the 6th version of ECMAScript, it was published in 2015, and is also known as ECMAScript 2015.

Why should I learn ES6?

React uses ES6, and you should be familiar with some of the new features like:

1. Classes
2. Arrow Functions
3. Variables (let, const, var)
4. Array Methods like .map()
5. Destructuring
6. Modules
7. Ternary Operator
8. Spread Operator

# ES6 Classes

ES6 introduced classes.

A class is a type of function, but instead of using the keyword function to initiate it, we use the keyword class, and the properties are assigned inside a constructor() method.

Example:

```markdown
<!DOCTYPE html>
<html>

<body>
  
<script>
class Car {
  constructor(name) {
    this.brand = name;
  }
}

const mycar = new Car("Ford");

document.write(mycar.brand);
</script>

</body>
</html>
```

Note: The constructor function is called automatically when the object is initialized.

<!--style="font-size:30px;color:blue;"-->
Method in classes

You can add your own methods in a class:

Example

Create a method named "present":

```markdown

<!DOCTYPE html>
<html>

<body>
  
<script>
class Car {
  constructor(name) {
    this.brand = name;
  }

  present() {
    return 'I have a ' + this.brand;
  }
}

const mycar = new Car("Ford");
document.write(mycar.present());
</script>

</body>
</html>
```

As you can see in the example above, you call the method by referring to the object's method name followed by parentheses (parameters would go inside the parentheses).

<!--style="font-size:30px;color:Red;"-->
 Class Inheritance

To create a class inheritance, use the extends keyword.

A class created with a class inheritance inherits all the methods from another class:

Example

Create a class named "Model" which will inherit the methods from the "Car" class:

```markdown

<!DOCTYPE html>
<html>

<body>
  
<script>
class Car {
  constructor(name) {
    this.brand = name;
  }

  present() {
    return 'I have a ' + this.brand;
  }
}

class Model extends Car {
  constructor(name, mod) {
    super(name);
    this.model = mod;
  }  
  show() {
    return this.present() + ', it is a ' + this.model
  }
}

const mycar = new Model("Ford", "Mustang");
document.write(mycar.show());
</script>

</body>
</html>
```

## ES6 Arrow Functions

The arrow function is a new feature of ES6, introduced in ReactJS 16. It allows the developer to create a 

function that has lexical “this” binding and no arguments.

Arrow functions offer a compressed and short version of a function expression and need fewer keystrokes than 

regular JavaScript functions from the developer and can be used as a simpler alternative to functions within 

class components and functional components and event handlers in React.

Arrow functions are always anonymous, meaning there is no need to use the keyword “function” when defining 

them. They also do not have their own this value, meaning that this inside an arrow function will refer to 

the one where it was created rather than where it was called from.

The third difference between regular JavaScript functions and arrow functions is that all arguments passed 

into an arrow function must be pre−defined, because there is no need for them to be assigned as default 

values like with regular JavaScript functions.

Arrow functions allow us to write shorter function syntax

<!--style="font-size:30px"-->
When to use Arrow Functions?

Arrow functions are great for performance and making declarative code more readable.

Although they are not always the best choice, they do have some advantages that make them worth considering.

In answer to the question, When to use them?, here are some scenarios −

* When you need to bind this to a method

* When you want a method to be called on a component's props

* When you want to use a callback function

<!--style="font-size:30px"-->
Why Should You Use Arrow Functions in React?

* First, they are much simpler to write and understand than traditional function expressions. This can make 

your code more readable and easier to debug.

* Second, arrow functions do not create a new scope, so they can be used in ReactJS without polluting the 

global scope.

* Finally, arrow functions can be used as arguments to other functions, which can make your code more 

flexible and expressive.

Example 

Before:

```markdown

<!DOCTYPE html>
<html>

<body>

<h1>Function</h1>

<p>This demonstrates a regular function, NOT an arrow function.</p>

<p id="demo"></p>
  
<script>
hello = function() {
  return "Hello World!";
}

document.getElementById("demo").innerHTML = hello();
</script>

</body>
</html>
```

Example 

With Arrow Function:

```markdown

<!DOCTYPE html>
<html>

<body>

<h1>Arrow Function</h1>

<p>A demonstration of a simple arrow function.</p>

<p id="demo"></p>
  
<script>
hello = () => {
  return "Hello World!";
}

document.getElementById("demo").innerHTML = hello();
</script>

</body>
</html>
```

Example 

Arrow Function With Parameters:

```markdown

<!DOCTYPE html>
<html>

<body>

<h1>Arrow Function</h1>

<p>A demonstration of an arrow function in one line, with parameters.</p>

<p id="demo"></p>
  
<script>
hello = (val) => "Hello " + val;

document.getElementById("demo").innerHTML = hello("World");
</script>

</body>
</html>
```

# ES6 Variable

Before ES6 there was only one way of defining your variables: with the var keyword. If you did not define them, they would be assigned to the global object. Unless you were in strict mode, then you would get an error if your variables were undefined.

Now, with ES6, there are three ways of defining your variables: var, let, and const.

<!--style="font-size:30px"-->
* Var

If you use var outside of a function, it belongs to the global scope.

If you use var inside of a function, it belongs to that function.

If you use var inside of a block, i.e. a for loop, the variable is still available outside of that block.

var has a function scope, not a block scope.

Example:

var x = 5.6;

<!--style="font-size:30px"-->
* let

let is the block scoped version of var, and is limited to the block (or expression) where it is defined.

If you use let inside of a block, i.e. a for loop, the variable is only available inside of that loop.

let has a block scope.

Example

let x = 5.6;

<!--style="font-size:30px"-->
* const

const is a variable that once it has been created, its value can never change.

const has a block scope.

The keyword const is a bit misleading.

It does not define a constant value. It defines a constant reference to a value.

Because of this you can NOT:

Reassign a constant value

Reassign a constant array

Reassign a constant object

But you CAN:

Change the elements of constant array

Change the properties of constant object

Example:

const x = 5.6;

# ES6 Array Method

There are many JavaScript array methods.

One of the most useful in React is the .map() array method.

The .map() method allows you to run a function on each item in the array, returning a new array as the result.

In React, map() can be used to generate lists.

Example:

Generate a list of items from an array:

```markdown

import React from 'react';
import ReactDOM from 'react-dom/client';

const myArray = ['apple', 'banana', 'orange'];

const myList = myArray.map((item) => <p>{item}</p>)

ReactDOM.render(myList, document.getElementById('root'));

```

# ES6 Destructuring

To illustrate destructuring, we'll make a sandwich. Do you take everything out of the refrigerator to make your sandwich? No, you only take out the items you would like to use on your sandwich.

Destructuring is exactly the same. We may have an array or object that we are working with, but we only need some of the items contained in these.

Destructuring makes it easy to extract only what is needed.

Destructuring Arrays 

Here is the old way of assigning array items to a variable:

Example:

Before

```markdown
const vehicles = ['mustang', 'f-150', 'expedition'];

// old way
const car = vehicles[0];
const truck = vehicles[1];
const suv = vehicles[2];
```

Example:

With Destructuring

```markdown
const vehicles = ['mustang', 'f-150', 'expedition'];

const [car, truck, suv] = vehicles;
```

When destructuring arrays, the order that variables are declared is important.

---> Destructuring Objects

Here is the old way of using an object inside a function:


Example:

Before

```markdown
const vehicleOne = {
  brand: 'Ford',
  model: 'Mustang',
  type: 'car',
  year: 2021, 
  color: 'red'
}

myVehicle(vehicleOne);

// old way
function myVehicle(vehicle) {
  const message = 'My ' + vehicle.type + ' is a ' + vehicle.color + ' ' + vehicle.brand + ' ' + vehicle.model + '.';
}
```

Example:

With Destructuring

```markdown
const vehicleOne = {
  brand: 'Ford',
  model: 'Mustang',
  type: 'car',
  year: 2021, 
  color: 'red'
}

myVehicle(vehicleOne);

function myVehicle({type, color, brand, model}) {
  const message = 'My ' + type + ' is a ' + color + ' ' + brand + ' ' + model + '.';
}
```

# ES6 Spread Operator

ES6 introduced a new operator referred to as a spread operator, which consists of three dots (...). It allows an iterable to expand in places where more than zero arguments are expected. It gives us the privilege to obtain the parameters from an array.

Spread operator syntax is similar to the rest parameter, but it is entirely opposite of it. Let's understand the syntax of the spread operator.

<!--style="font-size:30px;color:red;"-->
Syntax

```markdown

var variablename1 = [...value];  
```
The three dots (...) in the above syntax are the spread operator, which targets the entire values in the 

particular variable.

Example:

```markdown
<!DOCTYPE html>
<html>

<body>

<script>
const numbersOne = [1, 2, 3];
const numbersTwo = [4, 5, 6];
const numbersCombined = [...numbersOne, ...numbersTwo];

document.write(numbersCombined);
</script>

</body>
</html>
```

The spread operator is often used in combination with destructuring.

Example:

Assign the first and second items from numbers to variables and put the rest in an array:

```markdown
<!DOCTYPE html>
<html>

<body>

<script>
const numbers = [1, 2, 3, 4, 5, 6];

const [one, two, ...rest] = numbers;

document.write("<p>" + one + "</p>");
document.write("<p>" + two + "</p>");
document.write("<p>" + rest + "</p>");
</script>

</body>
</html>
```

---> We can use the spread operator with objects too:

Example:

Combines these Two Objects

```markdown
<!DOCTYPE html>
<html>

<body>

<script>
const myVehicle = {
  brand: 'Ford',
  model: 'Mustang',
  color: 'red'
}

const updateMyVehicle = {
  type: 'car',
  year: 2021, 
  color: 'yellow'
}

const myUpdatedVehicle = {...myVehicle, ...updateMyVehicle}

//Check the result object in the console:
console.log(myUpdatedVehicle);
</script>

<p>Press F12 and see the result object in the console view.</p>

</body>
</html>
```

Notice the properties that did not match were combined, but the property that did match, color, was overwritten by the last object that was passed, updateMyVehicle.

# ES6 Rest Parameter

The rest parameter is introduced in ECMAScript 2015 or ES6, which improves the ability to handle parameters. 

The rest parameter allows us to represent an indefinite number of arguments as an array. By using the rest 

parameter, a function can be called with any number of arguments.

Before ES6, the arguments object of the function was used. The arguments object is not an instance of the 

Array type. Therefore, we can't use the filter() method directly.

The rest parameter is prefixed with three dots (...). Although the syntax of the rest parameter is similar to 

the spread operator, it is entirely opposite from the spread operator. The rest parameter has to be the last 

argument because it is used to collect all of the remaining elements into an array.

<!--style="font-size:30px;color:red;"-->
Syntax

```markdown
function fun(a, b, ...theArgs) {  
  // statements  
}  

```
<!--style="font-size:30px"-->
Example

```markdown

function show(...args) {  
  let sum = 0;  
  for (let i of args) {  
      sum += i;  
  }  
  console.log("Sum = "+sum);  
}  
  
show(10, 20, 30);  
```

* All the arguments that we have passed in the function will map to the parameter list. As stated above, the 

rest parameter (...) should always be at last in the list of arguments. If we place it anywhere else, it will 

cause an error.

<!--style="font-size:30px"-->
Difference between Rest Parameter and arguments object

The rest parameter and arguments object are different from each other. Let's see the difference between the 

rest parameter and the arguments object:

* The arguments object is an array-like (but not array), while the rest parameters are array instances. The 

arguments object does not include methods such as sort, map, forEach, or pop, but these methods can be 

directly used in rest parameters.

<!--style="font-size:30px"-->
Rest Parameters and Destructuring

Destructuring means to break down a complex structure into simpler parts. We can define an array as the rest 

parameter. The passed-in arguments will be broken down into the array. Rest parameter supports array 

destructuring only.

By using the rest parameter, we can put all the remaining elements of an array in a new array.

Let's see an illustration of the same.

<!--style="font-size:30px"-->
Example

```markdown

var colors = ["Violet", "Indigo", "Blue", "Green", "Yellow", "Orange", "Red"];    
    
// destructuring assignment    
var [a,b,...args] = colors;    
console.log(a);     
console.log(b);     
console.log(args);  
```

<!--style="font-size:30px"-->
Rest Parameter in a dynamic function

JavaScript allows us to create dynamic functions by using the function constructor. We can use the rest 

parameter within a dynamic function.

<!--style="font-size:30px"-->
Example

```markdown

let num = new Function('...args','return args');  
console.log(num(10, 20, 30)); 
```


# ES6 Ternary Operator

The ternary operator is a simplified conditional operator like if / else.

Syntax: condition ? <expression if true> : <expression if false>

Here is an example using if / else:

Example 

Before:

```markdown
<!DOCTYPE html>
<html>

<body>

<h1 id="demo"></h1>

<script>
function renderApp() {
  document.getElementById("demo").innerHTML = "Welcome!";
}

function renderLogin() {
  document.getElementById("demo").innerHTML = "Please log in";
}

let authenticated = true;

if (authenticated) {
  renderApp();
} else {
  renderLogin();
}

</script>

<p>Try changing the "authenticated" variable to false, and run the code to see what happens.</p>
</body>
</html>
```

---> Example with Ternary Operator:

```markdown
<!DOCTYPE html>
<html>

<body>

<h1 id="demo"></h1>

<script>
function renderApp() {
  document.getElementById("demo").innerHTML = "Welcome!";
}

function renderLogin() {
  document.getElementById("demo").innerHTML = "Please log in";
}

let authenticated = true;

authenticated ? renderApp() : renderLogin();

</script>

<p>Try changing the "authenticated" variable to false, and run the code to see what happens.</p>
</body>
</html>
```

# React Render HTML

React's goal is in many ways to render HTML in a web page.

React renders HTML to the web page by using a function called ReactDOM.render().

<!--style="font-size:30px"-->
The createRoot Function

* The createRoot() function takes one argument, an HTML element.

* The purpose of the function is to define the HTML element where a React component should be displayed.

<!--style="font-size:30px"-->
The Render Function

The ReactDOM.render() function takes two arguments, HTML code and an HTML element.

The purpose of the function is to display the specified HTML code inside the specified HTML element.

But render where?

There is another folder in the root directory of your React project, named "public". In this folder, there is an index.html file.

You'll notice a single `<div>` in the body of this file. This is where our React application will be rendered.

Example

Display a paragraph inside an element with the id of "root":

```markdown
import React from 'react';
import ReactDOM from 'react-dom/client';

ReactDOM.render(<p>Hello</p>, document.getElementById('root'));
```

Note that the element id does not have to be called "root", but this is the standard convention.

<!--style="font-size:30px"-->
* The HTML Code

The HTML code in this tutorial uses JSX which allows you to write HTML tags inside the JavaScript code:

Do not worry if the syntax is unfamiliar, you will learn more about JSX in the next chapter.

Example

Create a variable that contains HTML code and display it in the "root" node:

```markdown
import React from 'react';
import ReactDOM from 'react-dom/client';

const myelement = (
  <table>
    <tr>
      <th>Name</th>
    </tr>
    <tr>
      <td>John</td>
    </tr>
    <tr>
      <td>Elsa</td>
    </tr>
  </table>
);

ReactDOM.render(myelement, document.getElementById('root'));
```
<!--style="font-size:30px"-->
* The Root Node

The root node is the HTML element where you want to display the result.

It is like a container for content managed by React.

It does NOT have to be a `<div>` element and it does NOT have to have the id='root':

Example

The root node can be called whatever you like:

```markdown
import React from 'react';
import ReactDOM from 'react-dom/client';

ReactDOM.render(<p>Hallo</p>, document.getElementById('sandy'));

/*
For this example to work on your project,
you must have a element with
id="sandy" on your "index.html" page.
*/
```

# React Jsx

<!--style="font-size:30px"-->
What is Jsx?

JSX stands for JavaScript XML.

JSX allows us to write HTML in React.

JSX makes it easier to write and add HTML in React.

<!--style="font-size:30px"-->
* Coding Jsx

JSX allows us to write HTML elements in JavaScript and place them in the DOM without any createElement()  and/or appendChild() methods.

JSX converts HTML tags into react elements.

You are not required to use JSX, but JSX makes it easier to write React applications.

Here are two examples. The first uses JSX and the second does not:

<!--style="font-size:30px"-->
Example 1

Jsx:

```markdown

import React from 'react';
import ReactDOM from 'react-dom/client';

const myElement = <h1>I Love JSX!</h1>;

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```
<!--style="font-size:30px"-->
Example 2

Without Jsx:

```markdown

import React from 'react';
import ReactDOM from 'react-dom/client';

const myElement = React.createElement('h1', {}, 'I do not use JSX!');

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```

As you can see in the first example, JSX allows us to write HTML directly within the JavaScript code.

JSX is an extension of the JavaScript language based on ES6, and is translated into regular JavaScript at runtime.

<!--style="font-size:30px"-->
* Expressions in jsx:

With JSX you can write expressions inside curly braces { }.

The expression can be a React variable, or property, or any other valid JavaScript expression. JSX will execute the expression and return the result:

<!--style="font-size:30px"-->
Example

Execute the expression 5 + 5:

```markdown

import React from 'react';
import ReactDOM from 'react-dom/client';

const myElement = <h1>React is {5 + 5} times better with JSX</h1>;

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```

<!--style="font-size:30px"-->
* Inserting a Large Block of HTML

To write HTML on multiple lines, put the HTML inside parentheses:

<!--style="font-size:30px"-->
Example

Create a list with three list items:

```markdown

import React from 'react';
import ReactDOM from 'react-dom/client';

const myElement = (
  <ul>
    <li>Apples</li>
    <li>Bananas</li>
    <li>Cherries</li>
  </ul>
);

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```

<!--style="font-size:30px"-->
* One Top Level Element

The HTML code must be wrapped in ONE top level element.

So if you like to write two paragraphs, you must put them inside a parent element, like a div element.

<!--style="font-size:30px"-->
Example

Wrap two paragraphs inside one DIV element:

```markdown

import React from 'react';
import ReactDOM from 'react-do/client';

const myElement = (
  <div>
    <h1>I am a Header.</h1>
    <h1>I am a Header too.</h1>
  </div>
);

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```

JSX will throw an error if the HTML is not correct, or if the HTML misses a parent element.

<!--style="font-size:30px"-->
* Elements Must be Closed

JSX follows XML rules, and therefore HTML elements must be properly closed.

<!--style="font-size:30px"-->
Example

Close empty elements with />

```markdown

import React from 'react';
import ReactDOM from 'react-dom/client';

const myElement = <input type="text" />;

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```

JSX will throw an error if the HTML is not properly closed.

<!--style="font-size:30px"-->
* Attribute class = className

The class attribute is a much used attribute in HTML, but since JSX is rendered as JavaScript, and the class 

keyword is a reserved word in JavaScript, you are not allowed to use it in JSX.

---> Use attribute className instead.

JSX solved this by using className instead. When JSX is rendered, it translates className attributes into 

class attributes.

<!--style="font-size:30px"-->
Example

Use attribute className instead of class in JSX:

```markdown

import React from 'react';
import ReactDOM from 'react-dom/client';

const myElement = <h1 className="myclass">Hello World</h1>;

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```

<!--style="font-size:30px"-->
* Conditions - if statements

React supports if statements, but not inside JSX.

To be able to use conditional statements in JSX, you should put the if statements outside of the JSX, or you 

could use a ternary expression instead:

-> Option 1:

Write if statements outside of the JSX code:

<!--style="font-size:30px"-->
Example

Write "Hello" if x is less than 10, otherwise "Goodbye":

```markdown

import React from 'react';
import ReactDOM from 'react-dom/client';

const x = 5;
let text = "Goodbye";
if (x < 10) {
  text = "Hello";
}

const myElement = <h1>{text}</h1>;

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```

-> Option 2:

Use ternary expressions instead:

<!--style="font-size:30px"-->
Example

Write "Hello" if x is less than 10, otherwise "Goodbye":

```markdown

import React from 'react';
import ReactDOM from 'react-dom/client';

const x = 5;

const myElement = <h1>{(x) < 10 ? "Hello" : "Goodbye"}</h1>;

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```

Note that in order to embed a JavaScript expression inside JSX, the JavaScript must be wrapped with curly 

braces.


# React Components

Components are like functions that return HTML elements.

Components are independent and reusable bits of code. They serve the same purpose as JavaScript functions, but

work in isolation and return HTML.

Components come in two types, Class components and Function components, in this tutorial we will concentrate

on Function components.

In older React code bases, you may find Class components primarily used. It is now suggested to use Function

components along with Hooks, which were added in React 16.8. There is an optional section on Class

for your reference.

<!--style="font-size:30px"-->
Create Your First Component

When creating a React component, the component's name MUST start with an upper case letter.

<!--style="font-size:30px"-->
* Class Component

A class component must include the extends React.Component statement. This statement creates an inheritance to React.Component, and gives your component access to React.Component's functions.

The component also requires a render() method, this method returns HTML.

<!--style="font-size:30px"-->
Example 

Create a Class component called Car

```markdown

class Car extends React.Component {
  render() {
    return <h2>Hi, I am a Car!</h2>;
  }
}
```

<!--style="font-size:30px"-->
* Function Component

Here is the same example as above, but created using a Function component instead.

A Function component also returns HTML, and behaves much the same way as a Class component, but Function

components can be written using much less code, are easier to understand, and will be preferred in this 
 
tutorial.

<!--style="font-size:30px"-->
Example 

Create a Function component called Car

```markdown
function Car() {
  return <h2>Hi, I am a Car!</h2>;
}
```

<!--style="font-size:30px"-->
* Components in Files

React is all about re-using code, and it is recommended to split your components into separate files.

To do that, create a new file with a .js file extension and put the code inside it:

Note that the filename must start with an uppercase character.

<!--style="font-size:30px"-->
Example

This is the new file, we named it "Car.js":

```markdown
function Car() {
  return <h2>Hi, I am a Car!</h2>;
}

export default Car;
```
To be able to use the Car component, you have to import the file in your application.

<!--style="font-size:30px"-->
Example 

Now we import the "Car.js" file in the application, and we can use the Car component as if it was created 

here.

```markdown
import React from 'react';
import ReactDOM from 'react-dom/client';
import Car from './Car.js';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Car />);
```
# React State

* The state is an updatable structure that is used to contain data or information about the component. The 

state in a component can change over time. The change in state over time can happen as a response to user 

action or system event. A component with the state is known as stateful components. It is the heart of the 

react component which determines the behavior of the component and how it will render. They are also 

responsible for making a component dynamic and interactive.

* A state must be kept as simple as possible. It can be set by using the setState() method and calling 

setState() method triggers UI updates. A state represents the component's local state or information. It can 

only be accessed or modified inside the component or by the component directly. To set an initial state 

before any interaction occurs, we need to use the getInitialState() method.

For example, if we have five components that need data or information from the state, then we need to create 

one container component that will keep the state for all of them.

<!--style="font-size:30px"-->
* Defining state

To define a state, you have to first declare a default set of values for defining the component's initial 

state. To do this, add a class constructor which assigns an initial state using this.state. The 'this.state' 

property can be rendered inside render() method.

<!--style="font-size:30px"-->
Example

The below sample code shows how we can create a stateful component using ES6 syntax.


```markdown

import React, { Component } from 'react';  
class App extends React.Component {  
 constructor() {  
      super();        
      this.state = { displayBio: true };  
      }  
      render() {  
          const bio = this.state.displayBio ? (  
              <div>  
                  <p><h3>Javatpoint is one of the best Java training institute in Noida, Delhi, Gurugram, Ghaziabad and Faridabad. We have a team of experienced Java developers and trainers from multinational companies to teach our campus students.</h3></p>   
            </div>  
              ) : null;  
              return (  
                  <div>  
                      <h1> Welcome to JavaTpoint!! </h1>  
                      { bio }   
                  </div>  
              );  
     }  
}  
export default App;  
```

To set the state, it is required to call the super() method in the constructor. It is because this.state is 

uninitialized before the super() method has been called.

# React Props

* Props stand for "Properties." They are read-only components. It is an object which stores the value of 

attributes of a tag and work similar to the HTML attributes. It gives a way to pass data from one component 

to other components. It is similar to function arguments. Props are passed to the component in the same way 

as arguments passed in a function.

* Props are immutable so we cannot modify the props from inside the component. Inside the components, we can 

add attributes called props. These attributes are available in the component as this.props and can be used to 

render dynamic data in our render method.

* When you need immutable data in the component, you have to add props to reactDom.render() method in the 

main.js file of your ReactJS project and used it inside the component in which you need. It can be explained 

in the below example.

<!--style="font-size:30px"-->
 React Props

React Props are like function arguments in JavaScript and attributes in HTML.

To send props into a component, use the same syntax as HTML attributes:

<!--style="font-size:30px"-->
Example

```markdown
import React from 'react';
import ReactDOM from 'react-dom/client';

function Car(props) {
  return <h2>I am a { props.brand }!</h2>;
}

const myElement = <Car brand="Ford" />;

const root = ReactDOM.createRoot(document.getElementById('root'));

root.render(myElement);
```

The component receives the argument as a props object:

<!--style="font-size:30px"-->
 Pass Data

Props are also how you pass data from one component to another, as parameters.

<!--style="font-size:30px"-->
Example

Send the "brand" property from the Garage component to the Car component:

```markdown
import React from 'react';
import ReactDOM from 'react-dom/client';

function Car(props) {
  return <h2>I am a { props.brand }!</h2>;
}

function Garage() {
  return (
    <>
	    <h1>Who lives in my garage?</h1>
	    <Car brand="Ford" />
    </>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Garage />);
```

Note : React Props are read-only! You will get an error if you try to change their value.

# React Events

Just like HTML DOM events, React can perform actions based on user events.

React has the same events as HTML: click, change, mouseover etc.

* Adding Events

React events are written in camelCase syntax:

onClick instead of onclick.

React event handlers are written inside curly braces:

onClick={shoot}  instead of onClick="shoot()".

Example

Put the shoot function inside the Football component:

```markdown
import React from 'react';
import ReactDOM from 'react-dom/client';

function Football() {
  const shoot = () => {
    alert("Great Shot!");
  }

  return (
    <button onClick={shoot}>Take the shot!</button>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Football />);
```

# React List

Lists are used to display data in an ordered format and mainly used to display menus on websites. In React, 

Lists can be created in a similar way as we create lists in JavaScript. Let us see how we transform Lists in 

regular JavaScript.

The map() function is used for traversing the lists. In the below example, the map() function takes an array 

of numbers and multiply their values with 5. We assign the new array returned by map() to the variable 

multiplyNums and log it.

<!--style="font-size:30px"-->
Example

```markdown

var numbers = [1, 2, 3, 4, 5];   
const multiplyNums = numbers.map((number)=>{   
    return (number * 5);   
});   
console.log(multiplyNums);
```
<!--style="font-size:30px"-->
Output

The above JavaScript code will log the output on the console. The output of the code is given below.

```console

[5, 10, 15, 20, 25]
```

Now, let us see how we create a list in React. To do this, we will use the map() function for traversing the 

list element, and for updates, we enclosed them between curly braces {}. Finally, we assign the array 

elements to listItems. Now, include this new list inside <ul> </ul> elements and render it to the DOM.

<!--style="font-size:30px"-->
Example

```markdown

import React from 'react';   
import ReactDOM from 'react-dom';   
  
const myList = ['Peter', 'Sachin', 'Kevin', 'Dhoni', 'Alisa'];   
const listItems = myList.map((myList)=>{   
    return <li>{myList}</li>;   
});   
ReactDOM.render(   
    <ul> {listItems} </ul>,   
    document.getElementById('app')   
);   
export default App; 
``` 

<!--style="font-size:30px"-->
Output

```console

* Peter

* Sachin

* Kelvin

* Dhoni

* Alisa
```

<!--style="font-size:30px"-->
* Rendering Lists inside components

In the previous example, we had directly rendered the list to the DOM. But it is not a good practice to 

render lists in React. In React, we had already seen that everything is built as individual components. 

Hence, we would need to render lists inside a component. We can understand it in the following code.

<!--style="font-size:30px"-->
Example

```markdown

import React from 'react';   
import ReactDOM from 'react-dom';   
  
function NameList(props) {  
  const myLists = props.myLists;  
  const listItems = myLists.map((myList) =>  
    <li>{myList}</li>  
  );  
  return (  
    <div>  
        <h2>Rendering Lists inside component</h2>  
              <ul>{listItems}</ul>  
    </div>  
  );  
}  
const myLists = ['Peter', 'Sachin', 'Kevin', 'Dhoni', 'Alisa'];   
ReactDOM.render(  
  <NameList myLists={myLists} />,  
  document.getElementById('app')  
);  
export default App;
```

<!--style="font-size:30px"-->
Output

```console

Rendering Lists inside component

* Peter

* Sachin

* Kelvin

* Dhoni

* Alisa
```


# Keys

Keys allow React to keep track of elements. This way, if an item is updated or removed, only that item will

be re-rendered instead of the entire list.

Keys need to be unique to each sibling. But they can be duplicated globally.

Generally, the key should be a unique ID assigned to each item. As a last resort, you can use the array
 
index as a key.

Example

```markdown
import React from 'react';
import ReactDOM from 'react-dom/client';

function Car(props) {
  return <li>I am a { props.brand }</li>;
}

function Garage() {
  const cars = [
    {id: 1, brand: 'Ford'},
    {id: 2, brand: 'BMW'},
    {id: 3, brand: 'Audi'}
  ];
  return (
    <>
	    <h1>Who lives in my garage?</h1>
	    <ul>
        {cars.map((car) => <Car key={car.id} brand={car.brand} />)}
      </ul>
    </>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Garage />);
```
# React Fragments

In React, whenever you want to render something on the screen, you need to use a render method inside the 

component. This render method can return single elements or multiple elements. The render method will only 

render a single root node inside it at a time. However, if you want to return multiple elements, the render 

method will require a 'div' tag and put the entire content or elements inside it. This extra node to the DOM 

sometimes results in the wrong formatting of your HTML output and also not loved by the many developers.

<!--style="font-size:30px"-->
Example

```markdown

// Rendering with div tag  
class App extends React.Component {   
     render() {    
      return (   
         //Extraneous div element   
         <div>  
           <h2> Hello World! </h2>   
           <p> Welcome to the JavaTpoint. </p>   
         </div>   
      );   
     }   
} 
``` 

To solve this problem, React introduced Fragments from the 16.2 and above version. Fragments allow you to 

group a list of children without adding extra nodes to the DOM.

<!--style="font-size:30px"-->
Syntax

```markdown

<React.Fragment>  
      <h2> child1 </h2>   
    <p> child2 </p>   
      .. ..... .... ...  
</React.Fragment>  
```

<!--style="font-size:30px"-->
Example

```markdown

// Rendering with fragments tag  
class App extends React.Component {   
    render() {   
     return (   
       <React.Fragment>  
            <h2> Hello World! </h2>   
        <p> Welcome to the JavaTpoint. </p>   
         </React.Fragment>  
     );   
    }   
} 
```  

<!--style="font-size:30px"-->
* Why we use Fragments?

The main reason to use Fragments tag is:

1. It makes the execution of code faster as compared to the div tag.

2. It takes less memory.

<!--style="font-size:30px"-->
Fragments Short Syntax

There is also another shorthand exists for declaring fragments for the above method. It looks like empty tag 

in which we can use of '<>' and '' instead of the 'React.Fragment'.

<!--style="font-size:30px"-->
Example

```markdown

//Rendering with short syntax   
class Columns extends React.Component {   
  render() {   
    return (   
      <>    
        <h2> Hello World! </h2>   
        <p> Welcome to the JavaTpoint </p>   
      </>   
    );   
  }   
} 
```  

<!--style="font-size:30px"-->
Keyed Fragments

The shorthand syntax does not accept key attributes. You need a key for mapping a collection to an array of 

fragments such as to create a description list. If you need to provide keys, you have to declare the 

fragments with the explicit `<React.Fragment>`syntax.

---> Note: Key is the only attributes that can be passed with the Fragments.

<!--style="font-size:30px"-->
Example

```markdown

Function  = (props) {  
  return (  
    <Fragment>  
      {props.items.data.map(item => (  
        // Without the 'key', React will give a key warning  
        <React.Fragment key={item.id}>  
          <h2>{item.name}</h2>  
          <p>{item.url}</p>  
          <p>{item.description}</p>  
        </React.Fragment>  
      ))}  
    </Fragment>  
  )  
}  

```


# React Router

* Routing is a process in which a user is directed to different pages based on their action or request. 

ReactJS Router is mainly used for developing Single Page Web Applications. React Router is used to define 

multiple routes in the application. When a user types a specific URL into the browser, and if this URL path 

matches any 'route' inside the router file, the user will be redirected to that particular route.

* React Router is a standard library system built on top of the React and used to create routing in the React 

application using React Router Package. It provides the synchronous URL on the browser with data that will be 

displayed on the web page. It maintains the standard structure and behavior of the application and mainly 

used for developing single page web applications.

<!--style="font-size:30px"-->
Need of React Router

React Router plays an important role to display multiple views in a single page application. Without React 

Router, it is not possible to display multiple views in React applications. Most of the social media websites 

like Facebook, Instagram uses React Router for rendering multiple views.

<!--style="font-size:30px"-->
React Router Installation

React contains three different packages for routing. These are:

1. react-router: It provides the core routing components and functions for the React Router applications.

2. react-router-native: It is used for mobile applications.

3. react-router-dom: It is used for web applications design.

It is not possible to install react-router directly in your application. To use react routing, first, you 

need to install react-router-dom modules in your application. The below command is used to install react 

router dom.

---> $ npm install react-router-dom --save   

<!--style="font-size:30px"-->
Components in React Router

There are two types of router components:

* `<BrowserRouter>`: It is used for handling the dynamic URL.

* `<HashRouter>`: It is used for handling the static request.

<!--style="font-size:30px"-->
Example

Step-1: In our project, we will create two more components along with App.js, which is already present.

* About.js

```markdown
import React from 'react'  
class About extends React.Component {  
  render() {  
    return <h1>About</h1>  
  }  
}  
export default About 
``` 

* Contact.js

```markdown

import React from 'react'  
class Contact extends React.Component {  
  render() {  
    return <h1>Contact</h1>  
  }  
}  
export default Contact  
```

* App.js

```markdown

import React from 'react'  
class App extends React.Component {  
  render() {  
    return (  
      <div>  
        <h1>Home</h1>  
      </div>  
    )  
  }  
}  
export default App
```  

* Step-2: For Routing, open the index.js file and import all the three component files in it. Here, you need 

to import line: import { Route, Link, BrowserRouter as Router } from 'react-router-dom' which helps us to 

implement the Routing. Now, our index.js file looks like below.

<!--style="font-size:30px"-->
What is Route?

It is used to define and render component based on the specified path. It will accept components and render 

to define what should be rendered.

* Index.js

```markdown

import React from 'react';  
import ReactDOM from 'react-dom';  
import { Route, Link, BrowserRouter as Router } from 'react-router-dom'  
import './index.css';  
import App from './App';  
import About from './about'  
import Contact from './contact'  
  
const routing = (  
  <Router>  
    <div>  
      <h1>React Router Example</h1>  
      <Route path="/" component={App} />  
      <Route path="/about" component={About} />  
      <Route path="/contact" component={Contact} />  
    </div>  
  </Router>  
)  
ReactDOM.render(routing, document.getElementById('root'));  
```

Step-3: Open command prompt, go to your project location, and then type npm start. You will get the following screen.

![image](images/react-router.png)

Now, if you enter manually in the browser: localhost:3000/about, you will see About component is rendered on 

the screen.

![image](images/react-router2.png)

Step-4: In the above screen, you can see that Home component is still rendered. It is because the home path 

is '/' and about path is '/about', so you can observe that slash is common in both paths which render both 

components. To stop this behavior, you need to use the exact prop. It can be seen in the below example.

<!--style="font-size:30px"-->
Index.js

```markdown

import React from 'react';  
import ReactDOM from 'react-dom';  
import { Route, Link, BrowserRouter as Router } from 'react-router-dom'  
import './index.css';  
import App from './App';  
import About from './about'  
import Contact from './contact'  
  
const routing = (  
  <Router>  
    <div>  
      <h1>React Router Example</h1>  
      <Route exact path="/" component={App} />  
      <Route path="/about" component={About} />  
      <Route path="/contact" component={Contact} />  
    </div>  
  </Router>  
)  
ReactDOM.render(routing, document.getElementById('root'));  
```

<!--style="font-size:30px"-->
Output

![image](images/react-router3.png)


<!--style="font-size:30px"-->
Adding Navigation using Link component

Sometimes, we want to need multiple links on a single page. When we click on any of that particular Link, it 

should load that page which is associated with that path without reloading the web page. To do this, we need 

to import <Link> component in the index.js file.


<!--style="font-size:30px"-->
What is < Link> component?

This component is used to create links which allow to navigate on different URLs and render its content 

without reloading the webpage.

<!--style="font-size:30px"-->
Example

<!--style="font-size:30px"-->
Index.js

```markdown
import React from 'react';  
import ReactDOM from 'react-dom';  
import { Route, Link, BrowserRouter as Router } from 'react-router-dom'  
import './index.css';  
import App from './App';  
import About from './about'  
import Contact from './contact'  
  
const routing = (  
  <Router>  
    <div>  
      <h1>React Router Example</h1>  
      <ul>  
        <li>  
          <Link to="/">Home</Link>  
        </li>  
        <li>  
          <Link to="/about">About</Link>  
        </li>  
        <li>  
          <Link to="/contact">Contact</Link>  
        </li>  
      </ul>  
      <Route exact path="/" component={App} />  
      <Route path="/about" component={About} />  
      <Route path="/contact" component={Contact} />  
    </div>  
  </Router>  
)  
ReactDOM.render(routing, document.getElementById('root'));  
```
<!--style="font-size:30px-->
Output

![image](images/react-router4.png)

After adding Link, you can see that the routes are rendered on the screen. Now, if you click on the About, 

you will see URL is changing and About component is rendered.

![image](images/react-router5.png)

Now, we need to add some styles to the Link. So that when we click on any particular link, it can be easily 

identified which Link is active. To do this react router provides a new trick NavLink instead of Link. Now, 

in the index.js file, replace Link from Navlink and add properties activeStyle. The activeStyle properties 

mean when we click on the Link, it should have a specific style so that we can differentiate which one is 

currently active.

```markdown

import React from 'react';  
import ReactDOM from 'react-dom';  
import { BrowserRouter as Router, Route, Link, NavLink } from 'react-router-dom'  
import './index.css';  
import App from './App';  
import About from './about'  
import Contact from './contact'  
  
const routing = (  
  <Router>  
    <div>  
      <h1>React Router Example</h1>  
      <ul>  
        <li>  
          <NavLink to="/" exact activeStyle={  
             {color:'red'}  
          }>Home</NavLink>  
        </li>  
        <li>  
          <NavLink to="/about" exact activeStyle={  
             {color:'green'}  
          }>About</NavLink>  
        </li>  
        <li>  
          <NavLink to="/contact" exact activeStyle={  
             {color:'magenta'}  
          }>Contact</NavLink>  
        </li>  
      </ul>  
      <Route exact path="/" component={App} />  
      <Route path="/about" component={About} />  
      <Route path="/contact" component={Contact} />  
    </div>  
  </Router>  
)  
ReactDOM.render(routing, document.getElementById('root'));  
```

<!--style="font-size:30px"-->
Output

When we execute the above program, we will get the following screen in which we can see that Home link is of 

color Red and is the only currently active link.

![image](images/react-router6.png)

Now, when we click on About link, its color shown green that is the currently active link.

![image](images/react-router7.png)

<!--style="font-size:30px"-->
`<Link>` vs `<NavLink>`

The Link component allows navigating the different routes on the websites, whereas NavLink component is used 

to add styles to the active routes.

<!--style="font-size:30px"-->
React Router Switch

The `<Switch> `component is used to render components only when the path will be matched. Otherwise, it 

returns to the not found component.

To understand this, first, we need to create a notfound component.

<!--style="font-size:30px"-->
notfound.js

```markdown

import React from 'react'  
const Notfound = () => <h1>Not found</h1>  
export default Notfound 
``` 

Now, import component in the index.js file. It can be seen in the below code.

<!--style="font-size:30px"-->
Index.js

```markdown

import React from 'react';  
import ReactDOM from 'react-dom';  
import { BrowserRouter as Router, Route, Link, NavLink, Switch } from 'react-router-dom'  
import './index.css';  
import App from './App';  
import About from './about'  
import Contact from './contact'  
import Notfound from './notfound'  
  
const routing = (  
  <Router>  
    <div>  
      <h1>React Router Example</h1>  
      <ul>  
        <li>  
          <NavLink to="/" exact activeStyle={  
             {color:'red'}  
          }>Home</NavLink>  
        </li>  
        <li>  
          <NavLink to="/about" exact activeStyle={  
             {color:'green'}  
          }>About</NavLink>  
        </li>  
        <li>  
          <NavLink to="/contact" exact activeStyle={  
             {color:'magenta'}  
          }>Contact</NavLink>  
        </li>  
      </ul>  
      <Switch>  
         <Route exact path="/" component={App} />  
         <Route path="/about" component={About} />  
         <Route path="/contact" component={Contact} />  
         <Route component={Notfound} />  
      </Switch>  
    </div>  
  </Router>  
)  
ReactDOM.render(routing, document.getElementById('root'));  
```

<!--style="font-size:30px"-->
Output

If we manually enter the wrong path, it will give the not found error.

![image](images/react-router8.png)


<!--style="font-size:30px"-->
React Router `<Redirect>`

A `<Redirect>` component is used to redirect to another route in our application to maintain the old URLs. It 

can be placed anywhere in the route hierarchy.

<!--style="font-size:20px"-->
Nested Routing in React

Nested routing allows you to render sub-routes in your application. It can be understood in the below example.

<!--style="font-size:20px"-->
Example

<!--style="font-size:20px"-->
Index.js

```markdown

import React from 'react';  
import ReactDOM from 'react-dom';  
import { BrowserRouter as Router, Route, Link, NavLink, Switch } from 'react-router-dom'  
import './index.css';  
import App from './App';  
import About from './about'  
import Contact from './contact'  
import Notfound from './notfound'  
  
const routing = (  
  <Router>  
    <div>  
      <h1>React Router Example</h1>  
      <ul>  
        <li>  
          <NavLink to="/" exact activeStyle={  
             {color:'red'}  
          }>Home</NavLink>  
        </li>  
        <li>  
          <NavLink to="/about" exact activeStyle={  
             {color:'green'}  
          }>About</NavLink>  
        </li>  
        <li>  
          <NavLink to="/contact" exact activeStyle={  
             {color:'magenta'}  
          }>Contact</NavLink>  
        </li>  
      </ul>  
      <Switch>  
         <Route exact path="/" component={App} />  
         <Route path="/about" component={About} />  
         <Route path="/contact" component={Contact} />  
         <Route component={Notfound} />  
      </Switch>  
    </div>  
  </Router>  
)  
ReactDOM.render(routing, document.getElementById('root'));  
```

In the contact.js file, we need to import the React Router component to implement the subroutes.

<!--style="font-size:30px"-->
contact.js

```markdown

import React from 'react'  
import { Route, Link } from 'react-router-dom'  
  
const Contacts = ({ match }) => <p>{match.params.id}</p>  
  
class Contact extends React.Component {  
  render() {  
    const { url } = this.props.match  
    return (  
      <div>  
        <h1>Welcome to Contact Page</h1>  
        <strong>Select contact Id</strong>  
        <ul>  
          <li>  
            <Link to="/contact/1">Contacts 1 </Link>  
          </li>  
          <li>  
            <Link to="/contact/2">Contacts 2 </Link>  
          </li>  
          <li>  
            <Link to="/contact/3">Contacts 3 </Link>  
          </li>  
          <li>  
            <Link to="/contact/4">Contacts 4 </Link>  
          </li>  
        </ul>  
        <Route path="/contact/:id" component={Contacts} />  
      </div>  
    )  
  }  
}  
export default Contact  
```

<!--style="font-size:30px"-->
Output

When we execute the above program, we will get the following output.

![image](images/react-router9.png)

After clicking the Contact link, we will get the contact list. Now, selecting any contact, we will get the 

corresponding output. It can be shown in the below example.


![image](images/react-router10.png)


<!--style="font-size:30px;color:red;"-->
* Benefits Of React Router

The benefits of React Router is given below:

* In this, it is not necessary to set the browser history manually.
* Link uses to navigate the internal links in the application. It is similar to the anchor tag.
* It uses Switch feature for rendering.
* The Router needs only a Single Child element.
* In this, every component is specified in .


# React Forms

Just like in HTML, React uses forms to allow users to interact with the web page.

<!--style="font-size:30px"-->
* Adding Forms in React

You add a form with React like any other element:

<!--style="font-size:30px"-->
Example

Add a form that allows users to enter their name:

```markdown
import React from 'react';
import ReactDOM from 'react-dom/client';

function MyForm() {
  return (
    <form>
      <label>Enter your name:
        <input type="text" />
      </label>
    </form>
  )
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<MyForm />);
```

This will work as normal, the form will submit and the page will refresh.

But this is generally not what we want to happen in React.

We want to prevent this default behavior and let React control the form.

<!--style="font-size:30px"-->
* Handling Forms

Handling forms is about how you handle the data when it changes value or gets submitted.

In HTML, form data is usually handled by the DOM.

In React, form data is usually handled by the components.

When the data is handled by the components, all the data is stored in the component state.

You can control changes by adding event handlers in the onChange attribute.

We can use the useState Hook to keep track of each inputs value and provide a "single source of truth" for

the entire application.

<!--style="font-size:30px"-->
Example

Use the useState Hook to manage the input:

```markdown

import { useState } from "react";
import ReactDOM from 'react-dom/client';

function MyForm() {
  const [name, setName] = useState("");

  return (
    <form>
      <label>Enter your name:
        <input
          type="text" 
          value={name}
          onChange={(e) => setName(e.target.value)}
        />
      </label>
    </form>
  )
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<MyForm />);
```
<!--style="font-size:30px"-->
* Submitting Forms

You can control the submit action by adding an event handler in the onSubmit attribute for the `<form>`:

<!--style="font-size:30px"-->
Example

Add a submit button and an event handler in the onSubmit attribute:

```markdown
import { useState } from "react";
import ReactDOM from 'react-dom/client';

function MyForm() {
  const [name, setName] = useState("");

  const handleSubmit = (event) => {
    event.preventDefault();
    alert(`The name you entered was: ${name}`);
  }
  return (
    <form onSubmit={handleSubmit}>
      <label>Enter your name:
        <input 
          type="text" 
          value={name}
          onChange={(e) => setName(e.target.value)}
        />
      </label>
      <input type="submit" />
    </form>
  )
}
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<MyForm />);
```

<!--style="font-size:30px"-->
* Multiple Input fields

You can control the values of more than one input field by adding a name attribute to each element.

We will initialize our state with an empty object.

To access the fields in the event handler use the event.target.name and event.target.value syntax.

To update the state, use square brackets [bracket notation] around the property name.

<!--style="font-size:30px"-->
Example

Write a form with two input fields:

```JavaScript
import { useState } from "react";
import ReactDOM from "react-dom/client";

function MyForm() {
  const [inputs, setInputs] = useState({});

  const handleChange = (event) => {
    const name = event.target.name;
    const value = event.target.value;
    setInputs(values => ({...values, [name]: value}))
  }

  const handleSubmit = (event) => {
    event.preventDefault();
    console.log(inputs);
  }

  return (
    <form onSubmit={handleSubmit}>
      <label>Enter your name:
      <input 
        type="text" 
        name="username" 
        value={inputs.username || ""} 
        onChange={handleChange}
      />
      </label>
      <label>Enter your age:
        <input 
          type="number" 
          name="age" 
          value={inputs.age || ""} 
          onChange={handleChange}
        />
        </label>
        <input type="submit" />
    </form>
  )
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<MyForm />);

```

Note: We use the same event handler function for both input fields, we could write one event handler for 

each, but this gives us much cleaner code and is the preferred way in React.


# React CSS

CSS in React is used to style the React App or Component. The style attribute is the most used attribute for 

styling in React applications, which adds dynamically-computed styles at render time. It accepts a JavaScript 

object in camelCased properties rather than a CSS string. There are many ways available to add styling to 

your React App or Component with CSS. Here, we are going to discuss mainly four ways to style React 

Components, which are given below:

1. Inline Styling

2. CSS Stylesheet

3. CSS Module

4. Styled Components


<!--style="font-size:30px"-->
1. Inline Styling

The inline styles are specified with a JavaScript object in camelCase version of the style name. Its value is 

the style?s value, which we usually take in a string.

<!--style="font-size:30px"-->
Example

<!--style="font-size:30px"-->
App.js

```markdown

import React from 'react';  
import ReactDOM from 'react-dom';  
  
class App extends React.Component {  
  render() {  
    return (  
      <div>  
      <h1 style={{color: "Green"}}>Hello JavaTpoint!</h1>  
      <p>Here, you can find all CS tutorials.</p>  
      </div>  
    );  
  }  
}  
export default App; 
```


Note: You can see in the above example, we have used two curly braces in:

`<h1 style={{color: "Green"}}>Hello JavaTpoint!</h1>.`

It is because, in JSX, JavaScript expressions are written inside curly braces, and JavaScript objects also 

use curly braces, so the above styling is written inside two sets of curly braces {{}}.

<!--style="font-size:30px"-->
Output

![image](images/react-css-output1.png)

<!--style="font-size:30px"-->
Using JavaScript Object

The inline styling also allows us to create an object with styling information and refer it in the style 

attribute.

<!--style="font-size:30px"-->
Example

<!--style="font-size:30px"-->
App.js

```markdown

import React from 'react';  
import ReactDOM from 'react-dom';  
  
class App extends React.Component {  
  render() {  
    const mystyle = {  
      color: "Green",  
      backgroundColor: "lightBlue",  
      padding: "10px",  
      fontFamily: "Arial"  
    };  
    return (  
      <div>  
      <h1 style={mystyle}>Hello JavaTpoint</h1>  
      <p>Here, you can find all CS tutorials.</p>  
      </div>  
    );  
  }  
}  
export default App; 
```

<!--style="font-size:30px"-->
Output

![image](images/react-css-output3.png)

<!--style="font-size:30px"-->
2. CSS Stylesheet

You can write styling in a separate file for your React application, and save the file with a .css extension. 

Now, you can import this file in your application.

<!--style="font-size:20px"-->
Example

<!--style="font-size:20px"-->
App.js

```markdown

import React from 'react';  
import ReactDOM from 'react-dom';  
import './App.css';  
  
class App extends React.Component {  
  render() {  
    return (  
      <div>  
      <h1>Hello JavaTpoint</h1>  
      <p>Here, you can find all CS tutorials.</p>  
      </div>  
    );  
  }  
}  
export default App; 
```

<!--style="font-size:20px"-->
App.css

```css

body {  
  background-color: #008080;  
  color: yellow;  
  padding: 40px;  
  font-family: Arial;  
  text-align: center;  
}  
```


<!--style="font-size:20px"-->
Index.html

```htm

<!DOCTYPE html>  
<html lang="en">  
  <head>  
    <meta charset="utf-8" />  
    <meta name="viewport"  
      content="width=device-width, initial-scale=1" />  
    <title>React App</title>  
  </head>  
  <body>  
    <div id="app"></div>  
  </body>  
</html>  
```

<!--style="font-size:20px"-->
Output

![image](images/react-css-output4.png)


<!--style="font-size:30px"-->
3. CSS Module

CSS Module is another way of adding styles to your application. It is a CSS file where all class names and 

animation names are scoped locally by default. It is available only for the component which imports it, means 

any styling you add can never be applied to other components without your permission, and you never need to 

worry about name conflicts. You can create CSS Module with the .module.css extension like a myStyles.module.

css name.

<!--style="font-size:20px"-->
Example

<!--style="font-size:20px"-->
App.js

```markdown

import React from 'react';  
import ReactDOM from 'react-dom';  
import styles from './myStyles.module.css';   
  
class App extends React.Component {  
  render() {  
    return (  
      <div>  
      <h1 className={styles.mystyle}>Hello JavaTpoint</h1>  
      <p className={styles.parastyle}>It provides great CS tutorials.</p>  
      </div>  
    );  
  }  
}  
export default App; 
```

<!--style="font-size:20px"-->
myStyles.module.css

```css

.mystyle {  
  background-color: #cdc0b0;  
  color: Red;  
  padding: 10px;  
  font-family: Arial;  
  text-align: center;  
}  
  
.parastyle{  
  color: Green;  
  font-family: Arial;  
  font-size: 35px;  
  text-align: center;  
}  
```

<!--style="font-size:20px"-->
Output

![image](images/react-css-output5.png)


<!--style="font-size:30px"-->
4. Styled Components

Styled-components is a library for React. It uses enhance CSS for styling React component systems in your 

application, which is written with a mixture of JavaScript and CSS.

The styled-components provides:

* Automatic critical CSS

* No class name bugs

* Easier deletion of CSS

* Simple dynamic styling

* Painless maintenance

<!--style="font-size:20px"-->
Installation

The styled-components library takes a single command to install in your React application. which is:

---> $ npm install styled-components --save  

<!--style="font-size:20px"-->
Example

Here, we create a variable by selecting a particular HTML element such as `<div>, <Title>, and <paragraph> `

where we store our style attributes. Now we can use the name of our variable as a wrapper `<Div></Div>` kind 

of React component.

<!--style="font-size:20px"-->
App.js

```markdown

import React from 'react';  
import ReactDOM from 'react-dom';  
import styled from 'styled-components';  
  
class App extends React.Component {  
  render() {  
    const Div:any = styled.div`  
            margin: 20px;  
            border: 5px dashed green;  
            &:hover {  
            background-color: ${(props:any) => props.hoverColor};  
            }  
            `;  
    const Title = styled.h1`  
            font-family: Arial;  
            font-size: 35px;  
            text-align: center;  
            color: palevioletred;  
            `;  
    const Paragraph = styled.p`  
            font-size: 25px;  
            text-align: center;  
            background-Color: lightgreen;  
            `;  
    return (  
       <div>            
            <Title>Styled Components Example</Title>  
            <p></p>  
            <Div hoverColor="Orange">  
                 <Paragraph>Hello JavaTpoint!!</Paragraph>  
            </Div>  
        </div>  
    );  
  }  
}  
export default App; 
``` 

<!--style="font-size:20px"-->
Output

Now, execute the App.js file, we will get the output as shown below.

![image](images/react-css-output6.png)

When we move the mouse pointer over the image, its color will be changed, as shown in the below image.

![image](images/react-css-output7.png)


# React Animation

* The animation is a technique in which images are manipulated to appear as moving images. It is one of the 

most used technique to make an interactive web application. In React, we can add animation using an explicit 

group of components known as the React Transition Group.

* React Transition Group is an add-on component for managing component states and useful for defining 

entering and exiting transitions. It is not able to animate styles by itself. Instead, it exposes transition 

states, manages classes and group elements, and manipulates the DOM in useful ways. It makes the 

implementation of visual transitions much easier.

* React Transition group has mainly two APIs to create transitions. These are:

1. ReactTransitionGroup: It uses as a low-level API for animation.
2. ReactCSSTransitionGroup: It uses as a high-level API for implementing basic CSS transitions and animations.

<!--style="font-size:30px"-->
Installation

We need to install react-transition-group for creating animation in React Web application. You can use the 

below command.

---> $ npm install react-transition-group --save  

<!--style="font-size:30px"-->
React Transition Group Components

React Transition Group API provides three main components. These are:

1. Transition
2. CSSTransition
3. Transition Group

<!--style="font-size:30px"-->
Transition

It has a simple component API to describe a transition from one component state to another over time. It is 

mainly used to animate the mounting and unmounting of a component. It can also be used for in-place 

transition states as well.

We can access the Transition component into four states:

* entering

* entered

* exiting

* exited

<!--style="font-size:30px"-->
CSSTransition

The CSSTransition component uses CSS stylesheet classes to write the transition and create animations. It is 

inspired by the ng-animate library. It can also inherit all the props of the transition component. We can 

divide the "CSSTransition" into three states. These are:

* Appear

* Enter

* Exit

CSSTransition component must be applied in a pair of class names to the child components. The first class is 

in the form of name-stage and the second class is in the name-stage-active. For example, you provide the name 

fade, and when it applies to the 'enter' stage, the two classes will be fade-enter and fade-enter-active. It 

may also take a prop as Timeout which defines the maximum time to animate.

<!--style="font-size:30px"-->
TransitionGroup

This component is used to manage a set of transition components (Transition and CSSTransition) in a list. It 

is a state machine that controls the mounting and unmounting of components over time. The Transition 

component does not define any animation directly. Here, how 'list' item animates is based on the individual 

transition component. It means, the "TransitionGroup" component can have different animation within a 
component.

Let us see the example below, which clearly help to understand the React Animation.

<!--style="font-size:20px"-->
Example

<!--style="font-size:20px"-->
App.js

In the App.js file, import react-transition-group component, and create the CSSTransition component that uses 

as a wrapper of the component you want to animate. We are going to use transitionEnterTimeout and 

transitionLeaveTimeout for CSS Transition. The Enter and Leave animations used when we want to insert or 

delete elements from the list.


```markdown

import React, { Component } from 'react';  
import { CSSTransitionGroup } from 'react-transition-group';  
  
class App extends React.Component {  
    constructor(props) {  
    super(props);  
    this.state = {items: ['Blockchain', 'ReactJS', 'TypeScript', 'JavaTpoint']};  
    this.handleAdd = this.handleAdd.bind(this);  
  }  
  
  handleAdd() {  
    const newItems = this.state.items.concat([  
      prompt('Enter Item Name')  
    ]);  
    this.setState({items: newItems});  
  }  
  
  handleRemove(i) {  
    let newItems = this.state.items.slice();  
    newItems.splice(i, 1);  
    this.setState({items: newItems});  
  }  
  
  render() {  
    const items = this.state.items.map((item, i) => (  
      <div key={item} onClick={() => this.handleRemove(i)}>  
        {item}  
      </div>  
    ));  
  
    return (  
      <div>  
    <h1>Animation Example</h1>  
            <button onClick={this.handleAdd}>Insert Item</button>  
            <CSSTransitionGroup  
               transitionName="example"  
           transitionEnterTimeout={800}  
               transitionLeaveTimeout={600}>  
               {items}  
            </CSSTransitionGroup>  
      </div>  
    );  
  }  
}  
export default App;  
```
<!--style="font-size:20px"-->
Main.js

```javascript

import React from 'react';  
import ReactDOM from 'react-dom';  
import App from './App.js';  
  
ReactDOM.render(<App />, document.getElementById('app'));  
```
<!--style="font-size:20px"-->
style.css

Add style.css file in your application, and add the following CSS styles. Now, to use this CSS file, you need 

to add the link of this file in your HTML file.

```css

.example-enter {  
  opacity: 0.01;  
}  
  
.example-enter.example-enter-active {  
  opacity: 1;  
  transition: opacity 500ms ease-in;  
}  
  
.example-leave {  
  opacity: 1;  
}  
  
.example-leave.example-leave-active {  
  opacity: 0.01;  
  transition: opacity 300ms ease-in;  
}  
```

In the above example, the animation durations are specified in both the CSS and render method. It tells React 

component when to remove the animation classes from the list and if it is leaving when to remove the element 

from the DOM.

<!--style="font-size:20px"-->
Output

When we execute the above program, it gives the below output.

![image](images/react-animation-output1.png)

Click on 'Insert Item' button, the following screen appears.

![image](images/react-animation-output2.png)

Once we insert the item and press Ok, the new item can be added in the list with fade in style. Here, we can 

also delete any item from the list by clicking on the particular link.

![image](images/react-animation-output3.png)


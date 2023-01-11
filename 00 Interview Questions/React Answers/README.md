# React Interview Question

<details>
<summary>What is virtual DOM ?</summary>
The virtual DOM (Virtual Document Object Model) is a programming concept that represents a virtual representation of the UI of a web application. It is a lightweight in-memory tree data structure that is created from the actual DOM (Document Object Model) and updated whenever the state of the application changes.
</details>
<br />

<details>
<summary>How Virtual DOM Works ?</summary>
When the state of the application changes, the virtual DOM creates a new virtual tree that represents the updated UI. It then compares this virtual tree to the previous virtual tree, and calculates the minimum number of changes that need to be made to the actual DOM in order to reflect the new UI. This process is known as "reconciliation."
</details>
<br />

<details>
<summary>What is React and What are the major Feature of React ?</summary>
React is a JavaScript library for building user interfaces. It was developed by Facebook, and is now used by many companies and organizations to build web and mobile applications.

Some of the major features of React are:

- Declarative: React makes it easy to build interactive and declarative UIs by providing a declarative syntax for expressing UI components and the relationships between them.

- Reusable Components: React allows you to create reusable components that can be easily shared and composed to build complex UIs.

- Virtual DOM: React uses a virtual DOM to optimize the performance of applications by minimizing the number of DOM manipulation operations that need to be performed.

- Server-Side Rendering: React can be used to render applications on the server, which can improve the performance and SEO of web applications.

- Unidirectional Data Flow: React uses a unidirectional data flow architecture, which helps to simplify the management of application state and reduce the risk of unexpected side effects.

- Reactive Updates: React automatically updates the UI in response to changes in application state, making it easy to build interactive and reactive applications.
</details>
<br />

<details>
<summary>What is JSX and How is work on Browser ?</summary>
JSX is a syntax extension for JavaScript that allows you to write HTML-like code in your JavaScript files. It is often used with React to define the structure of a UI component.

Here's an example of a JSX element:

```jsx
const element = <h1>Hello, world!</h1>;
```

JSX is not supported by all JavaScript environments, so it needs to be transpiled (converted) into regular JavaScript code before it can be run in a browser or on a server. This is typically done using a build tool like Babel, which is a transpiler that can convert JSX and other modern JavaScript syntax into code that can be run in older JavaScript environments.

Once the JSX has been transpiled into regular JavaScript code, it can be run in a browser or on a server just like any other JavaScript code. The transpiled code will create the DOM elements and manipulate them as necessary to create the desired UI.

</details>
<br />

<details>
<summary>What is difference between Element and Components ?</summary>
In React, an element is a plain JavaScript object that represents a DOM element. It is a minimal representation of a UI, and contains information about the type of element (e.g. div, h1, etc.), its attributes and children.

Here's an example of a React element:

```jsx
const element = {
  type: "h1",
  props: {
    className: "greeting",
    children: "Hello, world!",
  },
};
```

A React component, on the other hand, is a function or class that returns a React element or tree of elements. A component is a reusable piece of UI that can be used to create complex and interactive UIs.

Here's an example of a functional React component:

```jsx
function Greeting() {
  return <h1>Hello, world!</h1>;
}
```

And here's an example of a class-based React component:

```jsx
class Greeting extends React.Component {
  render() {
    return <h1>Hello, world!</h1>;
  }
}
```

</details>
<br />

<details>
<summary>What is state in react ?</summary>
In React, the state is an object that holds the data or variables that determine a component's behavior and render information to the user. It represents the part of the component's data that can change and affect the component's output.

When the state of a component changes, React will automatically re-render the component and update the UI to reflect the new state.

Here's an example of a functional component with a state:

```jsx
import { useState } from "react";

function stateExample() {
  const [count, setCount] = useState(0); // State

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>Click me</button>
    </div>
  );
}

export default stateExample;
```

</details>
<br />

<details>
<summary>What is props in React ?</summary>
In React, props (short for "properties") are a way to pass data from a parent component to a child component. Props are passed as attributes to a component's JSX tag, and can be accessed inside the component using the props object.

Here's an example of a functional component that accepts props:

```jsx
function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}
```

And here's an example of how you might use this component and pass it props:

```jsx
<Greeting name="React" />
```

</details>
<br />

<details>
<summary>What is pure components ?</summary>
In React, a pure component is a component that only re-renders when its props or state have changed. This means that when the component is given the same props and state, it will return the same output.
</details>
<br />

<details>
<summary>What is Class Components and What is Function Componet and When to use them ?</summary>
In React, there are two types of components: class components and function components.

Class components are defined using a JavaScript class, and typically have a render method that returns a JSX element. They also have access to the component's state and lifecycle methods. Here's an example of a class component:

```jsx
class Greeting extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}!</h1>;
  }
}
```

Function components, on the other hand, are defined as a JavaScript function that returns a JSX element. They don't have access to the component's state and lifecycle methods. Here's an example of a functional component:

```jsx
function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}
```

In most cases, you can use either a class component or a function component to implement the same functionality. However, there are a few reasons why you might choose one over the other:

- Function components are simpler and easier to read: They are just plain JavaScript functions, so they are generally easier to understand and reason about than class components, which have more boilerplate code and lifecycle methods.

- Function components have better performance: Because function components are simple functions, they are less likely to contain bugs related to lifecycle methods and state. Additionally, React provides the React.memo() higher-order component, which can be used to wrap function components and make them "pure" like class components
</details>
<br />

<details>
<summary>Difference between State and Props ?</summary>
In React, the `state` and `props` are both used to store data that a component can use to determine what to render, but they are used in different ways and have different characteristics.

- Props are used to pass data from a parent component to its child component. They are passed as attributes to a component's JSX tag, and can be accessed inside the component using the props object. Props are considered to be read-only values that a component should not modify directly. They are immutable.

- State is an object that holds the data or variables that determine a component's behavior and render information to the user. It represents the part of the component's data that can change and affect the component's output. State is managed and updated internally by the component using the setState method. It's mutable.

Here's an example to demonstrate the difference between state and props:

```jsx
function Greeting(props) {
  const [name, setName] = useState("ABC");

  const handleClick = () => setName("XYZ");

  return (
    <>
      <h1>
        Hello, {props.greet} {name}!
      </h1>
      <button onClick={handleClick}>Change Name</button>
    </>
  );
}

//Then in render method of parent component
<Greeting greet="Good Morning" />;
```

</details>
<br />

<details>
<summary>What is Higher Order Componets ?</summary>
In React, a higher-order component (HOC) is a function that takes a component as an argument and returns a new component that wraps the original component with additional functionality. HOCs are a powerful and flexible way to reuse component logic and add features like authentication, performance optimization, and more.

</details>
<br />

<details>
<summary>What is Context ?</summary>
In React, context is a way to pass data through the component tree without having to pass props down manually at every level. It allows you to share values like authenticated user, theme, or locale preference between components, without having to pass props down through the component tree.

Context is created using the React.createContext method, which takes a default value as an argument. The context object returned by this method has a Provider component, which can be used to provide the context value to its children, and a Consumer component, which can be used to access the context value from inside a component.

</details>
<br />

<details>
<summary>What is Children props ?</summary>
In React, the children prop is a special prop that can be used to pass children elements to a component. It's automatically passed to a component and it allows the component to include the children passed to it in its JSX output. It can be used to pass any JSX element, including text and other components, between elements.

Here's an example of how you might use the children prop to wrap content in a component:

```jsx
function Card(props) {
  return (
    <div className="card">
      <div className="card-header">{props.header}</div>
      <div className="card-body">{props.children}</div>
    </div>
  );
}
```

Then in render method of parent component

```jsx
<Card header="Hello">
  <p>This is a card.</p>
  <p>It has a header and a body.</p>
</Card>
```

</details>
<br />

<details>
<summary>How to write Comments in React ?</summary>
In React, you can add comments to your code by enclosing them in curly braces, and then wrapping them in {/* */}. For example:

```jsx
const MyComponent = () => {
  return (
    <div>
      {/* This is a comment */}
      <p>Hello, world!</p>
    </div>
  );
};
```

You can also use the // for comments, which would be valid only for single line comment

```jsx
const MyComponent = () => {
  // This is a comment
  return (
    <div>
      <p>Hello, world!</p>
    </div>
  );
};
```

</details>
<br />

<details>
<summary>Difference betweenn HTMl and React event Handling ?</summary>
HTML and React handle events in a similar way, but there are some key differences to keep in mind.

In HTML, you can add an event listener to an element using the on keyword followed by the event you want to listen for, like so:

```jsx
<button onclick="handleClick()">Click me</button>
```

In React, you would instead use the onClick attribute to attach a click event listener to a button element, like this:

```jsx
<button onClick={handleClick}>Click me</button>
```

</details>
<br />

<details>
<summary>What are inline Conditional expression ?</summary>
Inline conditional expressions are a way to conditionally render a certain element or value within your JSX code. This is often used to control the visibility or content of an element based on the current state or props of a component.

The most common way to create an inline conditional expression is by using the ternary operator. The ternary operator is a shorthand way of writing an if-else statement and has the following syntax:

```jsx
condition ? expressionIfTrue : expressionIfFalse;
```

</details>
<br />

<details>
<summary>What is use of Refs and how to create refs ?</summary>
In React, a ref is a way to access the underlying DOM node or a React component instance that a component represents. They are commonly used for a few different purposes, such as:

- Accessing the DOM node to interact with it directly, for example, to focus an input element or read its position.
- Creating animations or transitions that need to synchronize with the browser's rendering.
- Integrating with third-party libraries that don't work well with React's abstractions.

Here is an example on how to use refs:

```jsx
import { useRef } from "react";

const ref = useRef();

<div ref={myRef}>...</div>;

// Once the ref is created, you can access the underlying DOM node or React component by accessing its current property, like so:

const domNode = myRef.current;
```

</details>
<br />

<details>
<summary>What is the difference between a Presentational component and a Container component?</summary>
In React, a "Presentational component" (also known as a "dumb component" or a "stateless component") is a component that focuses on the presentation of the UI and is responsible for how the UI looks. These components typically receive data and callbacks via props, and have little or no internal state. They are generally easier to test and reason about than container components, because they don't depend on the global application state or manage side effects.

A "Container component" (also known as a "smart component" or a "stateful component") is a component that focuses on handling the logic and state management of a specific feature or section of the UI. These components often use state and lifecycle methods to manage the data and behavior of their child components. They are generally more complex and harder to test than presentational components, because they depend on the global application state and manage side effects like API calls or event listeners.

</details>
<br />

<details>
<summary>What are the different lifecycle methods?</summary>
In React, a component has several lifecycle methods that get called at different stages of the component's lifecycle. These methods allow you to run logic at specific points in time, such as when the component is first rendered, when its props or state change, and when it is removed from the DOM. The main lifecycle methods are:

- constructor(props): This is called before the component is first rendered. It is used to initialize the component's state and to bind event handlers.

- componentDidMount(): This is called immediately after the component is first rendered. It is used to set up any necessary code for the component, such as fetching data from an API or setting up event listeners.

- componentDidUpdate(prevProps, prevState): This is called after the component has updated and re-rendered. It receives the previous props and state, and is used to handle side effects or to update the component in response to prop or state changes.

- shouldComponentUpdate(nextProps, nextState): This is called before the component updates. It receives the next props and state and can be used to prevent unnecessary re-renders by returning false. This can improve performance, by canceling the render, if the component's props or state have not changed.

- componentWillUnmount(): This is called before the component is removed from the DOM. It is used to clean up any resources or event listeners that the component has set up.

- render(): This is the most important lifecycle method. It is called every time the component updates, and is responsible for rendering the component's JSX to the DOM.

- getSnapshotBeforeUpdate(prevProps,prevState): This is called just before the most recently rendered output is committed to e.g. the DOM. It enables your component to capture some information from the DOM (e.g. scroll position) before it is potentially changed. This will be passed as the third parameter to componentDidUpdate.

</details>
<br />

<details>
<summary>Explain React Hooks.</summary>
React Hooks are functions that allow you to use state and other React features in functional components, instead of having to use class components. They were introduced in React 16.8 as an alternative to class components, and provide a more straightforward way to manage state and component lifecycle methods in functional components.

</details>
<br />

<details>
<summary>What advantages are there in using arrow functions ?</summary>
Arrow functions, also known as "fat arrow" functions, are a new feature of JavaScript that provide a shorthand syntax for defining anonymous functions. They have a few advantages over traditional function expressions:

- Lexical this

- Shorter Syntax

- Easy to use with .bind

- Easy to use with Array.prototype methods

Here's an example to illustrate the difference between arrow function and traditional function:

```js
// traditional function
function traditionalSum(a, b) {
  return a + b;
}

// arrow function
const arrowSum = (a, b) => a + b;
```

</details>
<br />

<details>
<summary>What is equivalent of the following using React.createElement ?</summary>
React's createElement function is used to create React elements, which are the building blocks of React components. When you use JSX, the JSX compiler transpiles it into calls to createElement. The equivalent of the following JSX using createElement would be something like this:

```jsx
const element = <MyComponent prop1="value1" prop2="value2" />;
```

It would be:

```jsx
const element = React.createElement(MyComponent, {
  prop1: "value1",
  prop2: "value2",
});
```

</details>
<br />

<details>
<summary>Why virtual DOM is faster to update than real DOM ?</summary>
The virtual DOM is a lightweight in-memory representation of the actual DOM. It is used to determine the minimal set of changes needed to update the user interface when a component's state changes. This process is called "reconciliation" which minimize the number of changes to the actual DOM, which can be slower to update. React uses "shouldComponentUpdate" lifecycle method to check whether the component should re-render or not, if it returns false React will not re-render the component and its children which can improve performance. In summary, using a VDOM allows React to efficiently update the UI by minimizing the changes to the actual DOM, resulting in faster updates.
</details>
<br />

<details>
<summary>What is the useEffect hook used for ?</summary>
The useEffect hook is used to run side effects in a functional component. Side effects are actions that have an impact outside of the component, such as fetching data from an API, updating the title of a document, or adding/removing an event listener.
</details>
<br />

<details>
<summary>What is the difference between useEffect and useLayoutEffect ?</summary>
useEffect and useLayoutEffect are both hooks in React that are used to run side effects in a functional component, however, there is a slight difference in when they run:

- useEffect: This hook is used to run side effects after React has updated the DOM and painted the changes on the screen (after the browser has a chance to paint the changes). It allows you to synchronize a component with an external system (e.g. a chat service, an analytics service) or with an imperative API (e.g. a timer, an animation).

- useLayoutEffect: This hook is used to run side effects synchronously before the browser paints the changes. It allows you to measure, layout and adjust the position of an element, this is useful to avoid visual rendering flashes caused by changes in the layout.
</details>
<br />

<details>
<summary>Styled-Components vs Inline Styling in React ?</summary>
In React, there are a couple of ways to add styles to your components: using inline styling or using a library such as Styled-Components. Both approaches have their own advantages and trade-offs.

Inline styling example:

```jsx
function MyComponent() {
  return <div style={{ color: "red", fontSize: "14px" }}>Hello World</div>;
}
```

On the other hand, Styled-components is a popular library for styling components in React, it allows you to write CSS in JavaScript by creating a component with the desired styles and then using it as a regular component. It uses the power of the CSS to style components and allows to use full power of it. It also allows you to define and reuse styles across different components and keep the styles scoped to that specific component, which can make it easier to manage your styles.

```jsx
import styled from "styled-components";

const StyledDiv = styled.div`
  color: red;
  font-size: 14px;
`;

function MyComponent() {
  return <StyledDiv>Hello World</StyledDiv>;
}
```

</details>
<br />

<details>
<summary>Explain Styled Component in React with example ?</summary>
Styled-components is a popular library for styling components in React. It allows you to write CSS in JavaScript by creating a component with the desired styles and then using it as a regular component. It uses the power of the CSS to style components and allows to use full power of it. It also allows you to define and reuse styles across different components and keep the styles scoped to that specific component, which can make it easier to manage your styles.

To use Styled-components, you first need to install it by running npm install styled-components or yarn add styled-components. Once it's installed, you can import it in your component file and start using it.

Here's an example of a simple Styled-component in React:

```jsx
Styled-components is a popular library for styling components in React. It allows you to write CSS in JavaScript by creating a component with the desired styles and then using it as a regular component. It uses the power of the CSS to style components and allows to use full power of it. It also allows you to define and reuse styles across different components and keep the styles scoped to that specific component, which can make it easier to manage your styles.

To use Styled-components, you first need to install it by running npm install styled-components or yarn add styled-components. Once it's installed, you can import it in your component file and start using it.

Here's an example of a simple Styled-component in React:

Copy code
import styled from 'styled-components';

const StyledButton = styled.button`
  background-color: magenta;
  color: white;
  font-size: 16px;
  padding: 10px 20px;
  border-radius: 4px;
  cursor: pointer;
`;

function MyComponent() {
  return <StyledButton>Click Me</StyledButton>
}
```

</details>
<br />

<details>
<summary>Can you explain the difference between a pure and impure function, and why it matters in the context of React ?</summary>
A pure function is a function that given the same input, will always return the same output, and has no side effects. A pure function does not change the state or variables outside of its own scope, and it doesn't depend on anything else other than its inputs.

An impure function, on the other hand, can have side effects, modify variables or state outside of its own scope, or depend on something else other than its inputs.

Here is an example of a pure function:

```jsx
function add(a, b) {
  return a + b;
}
```

This function will always return the same output for the same input and has no side effect

Here is an example of an impure function:

```jsx
let x = 0;
function add(a, b) {
  x = x + 1; // x is mutable
  return a + b;
}
```

In the context of React, using pure functions can be beneficial when it comes to the performance and the predictability of the components. Because pure functions don't modify state or have side effects, React can use a technique called memoization to only re-render a component if its inputs have changed, which can lead to better performance.

</details>
<br />

<details>
<summary>What are some common hooks that are used in React ?</summary>
There are a number of hooks that are built-in to React that can be used to add functionality to functional components. Some of the most commonly used hooks include:

- useState: This hook allows you to add state to a functional component. It takes an initial state value as an argument, and returns an array containing the current state and a function to update the state.

- useEffect: This hook allows you to run side effects, such as fetching data or setting up event listeners, after a component has rendered. It takes a callback function that contains the logic for the side effect and an optional array of dependencies.

- useContext: This hook allows you to access context from a functional component. It takes a context object as an argument, and returns the current context value for that context.

- useReducer: This hook is similar to useState, but it allows you to use a reducer to handle state updates, this can be useful when the state updates depends on previous state, it returns the current state and a dispatch function.

- useMemo: This hook allows you to optimize your component by only re-computing a value if one of the dependencies has changed. This can be useful for expensive computations that you don't want to re-run on every render.

- useCallback: This hook allows you to optimize your component by only creating a callback if its dependencies have changed, this can be useful to pass callback to child components and prevent unnecessary re-renders

- useRef: This hook allows you to create a reference to an element, this can be useful to access a DOM node or to store mutable value.
</details>
<br />

<details>
<summary>What is a hook in React and why are they useful ?</summary>
In React, a hook is a special function that allows you to use state and other React features in functional components. Prior to the introduction of hooks, state and other React features were only available in class components, meaning that functional components were less powerful and less flexible.

- Hooks allow you to use the same features in functional components that were previously only available in class components, such as state, lifecycle methods, and context. This makes it easier to write, test, and understand your code, as well as allowing you to write more performant and reusable code.

- Hooks are also more performant than class components as React can use the state and props from the previous render to optimize the next one and avoid unnecessary re-renders.

</details>
<br />

<details>
<summary>How can you optimize performance in a ReactJS application ?</summary>
Here are some ways to optimize the performance of a functional ReactJS application:

- Use the useMemo hook to memoize the component, so it will only re-render if its dependencies have changed. It can be helpful when the component contains an expensive computation.

- Use the useCallback hook to prevent unnecessary re-renders of child components by only updating the callback if its dependencies have changed.

- Use the useEffect hook with the appropriate dependency array and cleanup function to prevent unnecessary renders and memory leaks.

- Use the useRef hook to store mutable values that should not trigger re-renders, like in the case of creating a ref for a DOM element and keeping track of its position.

- Use the useReducer hook in place of useState when the updates to the state depend on the previous state.

- Use React.memo to memoize functional components that do not require re-rendering when the props have not changed.

- Be mindful of the amount of data you are loading, if you are loading a large amount of data, consider pagination or virtualization.

- Be mindful of the amount of heavy logic or computation you are doing in your component, if it's too much consider doing it in a web worker or in a useEffect hook with cleanup function.
</details>
<br />

<details>
<summary>What is the difference between Shadow DOM and Virtual DOM ?</summary>
The Shadow DOM is a feature of web browsers that allows for the encapsulation of web components, hiding its internal structure from the rest of the page. The Virtual DOM is a representation of the actual DOM used by libraries/frameworks like React to improve web application performance. Shadow DOM helps in encapsulation and scoping of styles and behavior of a web-component. Virtual DOM is a performance optimization technique, it keeps a copy of actual DOM and updates changes intelligently. Shadow DOM is related to web components and browser implementation, Virtual DOM is related to the JS Library/framework.
</details>
<br />

<details>
<summary>What is the purpose of using super constructor with props argument ?</summary>
By calling super(props), you're essentially allowing the parent class to receive and use the props that are being passed to the child component. Without this call, the parent class would not have access to the props, and any functionality that depends on those props would not work as expected.

Here's an example of a simple React component class that uses super(props) in its constructor:

```jsx
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = { value: props.initialValue };
  }

  render() {
    return <div>{this.state.value}</div>;
  }
}
```

</details>
<br />

<details>
<summary>Why React uses className over class attribute ?</summary>
React uses the className attribute instead of the class attribute for setting the class of an element because class is a reserved keyword in JavaScript.
</details>
<br />

<details>
<summary>What are the limitations of React ?</summary>
React is a powerful and flexible library for building user interfaces, but like any tool, it has some limitations. Some of the limitations of React include:

- Steep learning curve: React uses a unique concept called the virtual DOM, which can take some time to fully understand and use effectively. Additionally, React's approach to building reusable components can be difficult to grasp for developers new to the library.

- Complicated builds: Depending on the complexity of the project, setting up a build process with Webpack and Babel can be quite involved, which can be challenging for developers new to the ecosystem.

- Heavy client-side rendering: React is a client-side library, so it relies on the browser to render the components and handle updates to the user interface. This can lead to longer load times and increased memory usage for larger applications, especially on less powerful devices.

- Higher memory usage: React heavily uses the Virtual DOM which can lead to higher memory consumption in comparison to other frameworks.

- JavaScript-based: React is a JavaScript-based library, so it requires a solid understanding of JavaScript to use it effectively. This can be a limitation for developers who are more comfortable with other languages.

- Limited server-side rendering: React is primarily a client-side library, so it's not as well suited for server-side rendering as some other libraries or frameworks.

- Bugs and errors: As with any library, there can be bugs and errors with React that can be difficult to debug and fix. Additionally, keeping up with updates and changes to the library can be a challenge.

</details>
<br />

<details>
<summary>What are the advantages of React ?</summary>
React is a popular JavaScript library for building user interfaces. It is maintained by Facebook and a community of individual developers and companies. Some of the key advantages of using React include:

- Reusability: React components are reusable, which means that you can use the same component in different parts of your application. This makes it easy to maintain and update your codebase.

- Virtual DOM: React uses a virtual DOM, which is a lightweight in-memory representation of the actual DOM. This allows React to update only the parts of the DOM that have changed, which makes it more efficient than other frameworks and libraries that update the entire DOM when something changes.

- One-way data flow: React uses a one-way data flow, which means that data flows in a single direction through your application. This makes it easy to understand how data is being passed between components and how it is being used.

- Server-side rendering: React can be used for server-side rendering, which means that your application can be rendered on the server and sent to the client as a fully-formed HTML document. This can improve the performance of your application and make it more SEO-friendly.

- Large ecosystem: React has a large and active community of developers who have created a wide variety of libraries and tools that can be used with React. This makes it easy to find solutions to common problems and to integrate other technologies with React.

- JSX: React use JSX, which is a syntax extension for JavaScript that allows you to describe the structure of the user interface using a syntax that is similar to HTML. This makes it easy for developers to understand how their user interfaces are built and to work with them.

- Debugging: React has many debugging tools like React Developer Tools and Redux DevTools. This makes it easy to inspect the components, their state and props, and understand how the components are interacting with each other in your application.

</details>
<br />

<details>
<summary>How to apply validation on props in React ?</summary>
In React, you can use the "prop-types" library to validate the props passed to a component. To use the library, you first need to import it at the top of your component file. Then, you can use the validation methods provided by the library, such as "isRequired" or "oneOfType", to check the types and values of the props.
</details>
<br />

<details>
<summary>What are stateful components and Stateless Components ?</summary>
In React, a stateful component is a component that has its own internal state and lifecycle methods. It extends the React.Component class and has access to the setState method for updating its state and re-rendering the component.
On the other hand, Stateless components are components that don't have their own internal state, also known as "dumb" or "presentational" components. They are defined as a JavaScript function and receive props as input, then render the components based on the props values.
</details>
<br />

<details>
<summary>What is reconciliation ?</summary>
In React, reconciliation is the process by which the virtual DOM (the in-memory representation of the actual DOM) is updated to reflect changes in the component's state or props. When a component's state or props change, React will compare the virtual DOM with the updated virtual DOM, identify the changes, and make the minimum number of changes necessary to the actual DOM to bring it in line with the virtual DOM. This process helps React optimize performance by minimizing the number of updates made to the actual DOM.
</details>
<br />

<details>
<summary>How to set state with a dynamic key name ?</summary>
In React, you can set state with a dynamic key name by using computed property names, a feature of the ES6 object literals. You can use square brackets around the key name, and inside of it, include a JavaScript expression that evaluates to a string that represents the key name you want. Finally you can use this computed property name inside the setState method to update the state.

An example would look like:

```jsx
handleChange(e) {
  const key = e.target.name;
  const value = e.target.value;
  setState({ [key]: value });
}
```

</details>
<br />

<details>
<summary>What are fragments and how it is better than Container div ?</summary>
In React, a fragment is a way to group a list of children without adding extra nodes to the DOM. It allows you to return multiple elements from a component's render method without having to wrap them in a container element. This can be useful when you want to avoid unnecessary wrapper elements in the rendered HTML, which can simplify the structure of your component and make it easier to style.
Fragments are represented by using `<> </>` or `<React.Fragment> </React.Fragment>` and it offers better performance as well as it does not affect the styles/layout of the DOM as it does not add any extra DOM node.
</details>
<br />

<details>
<summary>What is the use of react-dom package ?</summary>
The react-dom package is a package that contains React's DOM (Document Object Model) specific code. It provides methods that allow you to render React components to the DOM, manage the DOM elements that are created by React, and handle updates to the DOM when the state or props of a component change.

It is needed to run react app on browser.

</details>
<br />

<details>
<summary>Error Boundries in React ?</summary>
Error boundaries are React components that catch JavaScript errors in child component tree, log errors and display a fallback UI. Only catch errors during the rendering phase and not in async code or event handlers. They are feature in React that allows to handle errors and prevent application crash.
</details>
<br />

<details>
<summary>How to use InnerHtml in React ?</summary>
Using InnerHTML in React to set the content of an element with raw HTML can be dangerous as it allows for potential XSS (cross-site scripting) attacks. To use innerHTML in React, you can use the dangerouslySetInnerHTML prop, which takes an object with a __html key and a string value as the key's value. This key value pair will set the innerHTML of the element.

```jsx
const html = "<h1>Hello World</h1>";
return <div dangerouslySetInnerHTML={{ __html: html }} />;
```

It's advisable to use this only with trusted content, it is dangerous to use with untrusted user-generated content.

</details>
<br />

<details>
<summary>How events are different in React ?</summary>
- React events are named using camelCase, rather than lowercase.
- With JSX you pass a function as the event handler, rather than a string.

For example, the HTML:

```jsx
<button onclick="handleSubmit()">...</button>
```

is slightly different in React:

```jsx
<button onClick={handleSubmit}>...</button>
```

</details>
<br />

<details>
<summary>How you use decorators in React ?</summary>
You can decorate your class components, which is the same as passing the component into a function. Decorators are flexible and readable way of modifying component functionality.

```jsx
@setTitle("Profile")
class Profile extends React.Component {
  //....
}

const setTitle = (title) => (WrappedComponent) => {
  return class extends React.Component {
    componentDidMount() {
      document.title = title;
    }

    render() {
      return <WrappedComponent {...this.props} />;
    }
  };
};
```

</details>
<br />

<details>
<summary>How to perform automatic redirect after login ?</summary>
There are a few ways you could perform an automatic redirect after a successful login in a React application. One such method is to use `useNavigate` function from `react-router-dom`

```jsx
import { useNavigate } from "react-router-dom";

const MyComp = () => {
  const navigate = useNavigate();

  if (authenticated) {
    navigate("/");
  }
};

export default MyComp;
```

</details>
<br />

<details>
<summary>What is React Router ?</summary>
React Router is a popular routing library for React applications that helps you handle client-side routing, allowing you to define specific URLs for specific components or pages in your app. It also makes it easy to handle URL parameters and query strings, and allows you to programmatically navigate between different parts of your app. React Router helps to keep the UI in sync with the URL and provide dynamic routing.
</details>
<br />

<details>
<summary>How React Router is different from history library ?</summary>
history library is a standalone JavaScript library that provides an API for manipulating the browser's session history, and is used by React Router. React Router is a higher-level library built on top of the history library that provides a more powerful and flexible routing solution for React applications, like nesting and dynamic routing. React Router allows to define specific routes for specific components and pages in your app, handle URL parameters and query strings, and programmatically navigate between different parts of the app.
</details>
<br />

<details>
<summary>What is the purpose of push and replace methods of history ?</summary>
push method is used to add a new entry to the history stack and navigate to the new location, this means that when user click the back button it will move back to the previous location and also it will be present in the history stack of browser.
replace method is used to replace the current entry in the history stack with a new location, this means that when user click the back button it will move back to the previous location but the current location will not be present in the history stack.
Both push and replace are used to navigate the user to a new location but push creates a new entry in the history and replace updates the current entry.
</details>
<br />

<details>
<summary>What are render props ?</summary>
It's a way to reuse component logic and behavior through a prop that's a function that will be executed by the child component. It's typically used for cross-cutting concerns or stateful logic that may need to be reused across multiple components.
</details>
<br />

<details>
<summary>What are the popular React-specific linters ?</summary>
ESLint is one of the popular linters in React , that also works with React-specific rules to enforce best practices.

Another popular linter for React is elsint-plugin-react which provides additional rules for linting JSX and React specific syntax

</details>
<br />

<details>
<summary>What is the benefit of styles modules ?</summary>
Styles modules in React is a way to write CSS styles that are scoped to a specific component and do not leak to any other part of the application.
It eliminates the risk of naming collisions and makes the CSS more maintainable, by isolating styles for a specific component.
It also allows for greater reusability by making it easy to import and use the same styles in multiple components.
</details>
<br />

<details>
<summary>What are the popular packages for animation ?</summary>

- React transition group
- Framer motion
- GSAP
- React spring
</details>
<br />

<details>
<summary>What are the common folder structures for React ?</summary>
There are several different ways to structure a React project, and the best folder structure for your project will depend on the specific requirements of your application. However, here are a few common folder structures that are widely used in React projects:

- Component-Based Folder Structure: This structure organizes your project by separating components into their own folders, each containing the component's JS and CSS files.

- Feature-Based Folder Structure: This structure organizes your project by grouping components together based on the feature they relate to. It also separates the components by its type (Presentational, container and/or Higher Order Components)
</details>
<br />

<details>
<summary>Is it possible to use async/await in plain React ?</summary>
Yes, it is possible to use async/await in plain React (without any additional libraries or frameworks) to handle asynchronous operations such as API calls, timeouts, or any other promise-based code.
</details>
<br />

<details>
<summary>How to programmatically trigger click event in React ?</summary>
In React components, you can use the useRef Hook to programmatically trigger a click event on an element.

Here's an example:

```jsx
function MyComponent() {
  const buttonRef = useRef(null);

  const handleClick = () => {
    console.log("Clicked!");
  };

  useEffect(() => {
    buttonRef.current.click();
  }, []);

  return (
    <button ref={buttonRef} onClick={handleClick}>
      Click Me
    </button>
  );
}
```

</details>
<br />

<details>
<summary>What is prop drilling ?</summary>
rop drilling is a technique where a component that needs data passed to it, must receive the data via its props from its parent component, even if the parent component doesn't use the data itself. This can happen when the parent passes the data to its child, the child passes it to its child, and so on, until the desired component receives the data. This can make the code complex, hard to read, and hard to maintain.
</details>
<br />

<details>
<summary>What is state mutation and how to prevent it ?</summary>
State mutation is when the state of a component is directly modified rather than being replaced with a new state. This can cause unexpected behavior and make the component hard to reason about. To prevent state mutation, use the setState method or functional setState hook to update the state instead of modifying the state directly. Use immutable operations like Object.assign or the spread operator to create a new copy of the state before updating it.
</details>
<br />

<details>
<summary>What is the difference between useState and useRef hook ?</summary>
`useState` is a Hook that allows a functional component to have a state, that can be updated and it causes the component to re-render. `useRef` allows a functional component to have a reference to a DOM element or a value that persists across renders, it doesn't trigger re-render.
</details>
<br />

<details>
<summary>What are React Server components ?</summary>
React Server Components is an experimental feature in React that allows developers to run React components on the server and send rendered HTML to the client to be hydrated as regular React component.
This feature allows developers to improve the performance and SEO of web pages by reducing the load on the client-side and creating fully-rendered HTML on the server.
It's not yet available for general use but available in some libraries such as Next.js.
</details>
<br />

<details>
<summary>How do you get redux scaffolding using create-react-app ?</summary>
While scaffolding a react project using cra you can pass an additional flag as shown:

```bash
# Redux + Plain JS template
npx create-react-app my-app --template redux

# Redux + TypeScript template
npx create-react-app my-app --template redux-typescript
```

</details>
<br />

<details>
<summary>What are the benefits of new JSX transform ?</summary>
The new JSX transform, also known as "the new JSX runtime" or "the updated JSX transform", is an improved version of the JSX syntax that React uses to define components. It offers several benefits over the previous version:

- Better Performance
- Smaller Bundle Size
- Easier to Debug
- Better TypeScript Support
- No Need for additional Transpilation
</details>
<br />

<details>
<summary>What are the benefits of using typescript with reactjs ?</summary>
There are several benefits to using TypeScript in a React project:

- Type Safety
- IntelliSense
- Better Code Documentation
- Easier refactoring
- Interoperability
- Better testing
- Better Scalability

In summary, TypeScript can help you catch errors early, improve code documentation and make it easier to maintain your codebase, specially when your project starts to grow.

</details>
<br />

<details>
<summary>What is the difference between Imperative and Declarative in React ?</summary>
Imperative programming is when you tell the computer what to do step-by-step. Declarative programming is when you describe what you want and the computer figures out how to do it.
In React, imperative programming refers to directly manipulating the DOM, while declarative programming refers to describing a component's desired state and letting React update the DOM.
Imperative programming tends to be more complex and harder to reason about, while declarative programming is more expressive and easier to understand.
</details>
<br />

<details>
<summary>What is the purpose of eslint plugin for hooks ?</summary>
The ESLint plugin for hooks is a set of rules that help you write React hooks in a consistent and correct way. It catch common mistakes and enforces best practices when using hooks in React.

It helps to prevent bugs and make your codebase more stable, maintainable and easier to understand.

</details>
<br />

<details>
<summary>What is Concurrent Rendering ?</summary>
Concurrent rendering in React is a feature that allows the library to render multiple components or parts of the UI simultaneously, rather than in a sequential or blocking way. This improves the performance and the overall user experience of the application by avoiding delays in the rendering process. React uses techniques like time slicing and idle rendering to enable concurrent mode.
</details>
<br />

<details>
<summary>What is MobX ?</summary>
MobX is a library that provides a way to manage the state of a JavaScript application in a simple and efficient way. It uses a reactive programming paradigm that makes it easy to synchronize the state with the UI and other parts of the application. It also provides mechanisms for computed values and side-effect, that let the developer to create a transparent and powerful state management.
</details>
<br />

<details>
<summary>What are the differences between Redux and MobX ?</summary>
Redux is a library for managing application state that follows the principles of functional programming and unidirectional data flow. MobX is a library for managing application state that uses observable data and automatic rendering to make managing state simpler. The main difference between the two is that MobX uses observables and automatic rendering, while Redux relies on immutability and explicit actions to update the state.
</details>
<br />

<details>
<summary>What is react scripts ?</summary>
`react-scripts` is a development dependency package that is included when creating a new React application using create-react-app. It contains scripts and configuration used for building and running the application in development mode, as well as building a production-ready version of the app. It helps to abstract away the configuration of tools like webpack and Babel, making it easier to get started with building a React application.
</details>
<br />

<details>
<summary>What are the features of create react app ?</summary>
ate React App is a tool built by Facebook to help developers quickly set up and start building React applications. Some of its features include:

- Zero Configuration
- Development Server
- Build Tool
- Testing Setup
- Auto-prefixing
- ESLint and Prettier
- TypeScript support
- Easy deployment
- Environment variable management
</details>
<br />

<details>
<summary>Describe about data flow in react ?</summary>
In React, data flows in a unidirectional manner through a process called "propagation." Props (short for properties) are passed down from parent components to child components, and state is managed by individual components. Components can update their own state, which will trigger a re-render and update the view.
</details>
<br />

<details>
<summary>What are typical middleware choices for handling asynchronous calls in Redux ?</summary>
Some popular middleware choices for handling asynchronous calls in Redux include:

- redux-thunk
- redux-saga
- redux-observable
- redux-promise-middleware
- redux-axios-middleware
</details>
<br />

<details>
<summary>What is formik ?</summary>
Formik is a popular open-source library for handling forms in React applications. It provides a way to handle form validation, submissions, and error handling with a simple and consistent API.
</details>
<br />

<details>
<summary>What is route based code splitting ?</summary>
Route-based code splitting is a technique used in React applications to load the JavaScript code for a specific page or route only when it is needed, rather than loading all of the JavaScript code for the entire application at once. This can improve the performance of the application by reducing the initial load time and the overall size of the JavaScript that needs to be downloaded.
</details>
<br />

<details>
<summary>What is suspense component ?</summary>
Suspense is a React component used for code-splitting and lazy-loading of components. It allows you to specify a loading state that will be shown while the wrapped component is being loaded. It also allows you to specify a fallback component to be shown while the wrapped component is being loaded.
</details>
<br />

<details>
<summary>What are loadable components ?</summary>
Loadable components are a way of code splitting and lazy loading React components. They are designed to be easy to use with minimal configuration, and they provide a way to automatically handle the loading state and error state of the component. They work together with webpack and also provide a way to have a centralized way of handling code splitting and loading state.
</details>
<br />

<details>
<summary>What is dynamic import ?</summary>
Dynamic import is a feature that allows you to load a javascript module at runtime, It returns a promise that resolves to the exports of the module. It is used for code-splitting and lazy loading for improving performance by reducing the initial load time and the overall size of the JavaScript that needs to be downloaded.
</details>
<br />

<details>
<summary>What is React-Intl ?</summary>
React-Intl is an open-source library for internationalizing React applications. It provides a way to handle translations, formatting numbers, dates, and messages in a way that is consistent with the Internationalization standards. It provides components, API and locale data for handling localization in a seamless way.
</details>
<br />

<details>
<summary>What are the main features of React Intl ?</summary>
React-Intl is an open-source library for internationalizing React applications. Some of the main features of React-Intl include:

- Message formatting
- Number and date formatting
- Pluralization
- Localization data
- Components
- Context API
- Ease to use API
- Built-in support for handling React Suspense
</details>
<br />

<details>
<summary>Can you force a component to re-render without calling setState ?</summary>
Yes, it is possible to force a component to re-render in React without calling setState. One way to do this is by passing a prop with a unique key to the component. React uses the key to determine whether or not to re-render the component, so by passing a different key each time the component is rendered, React will think that it is a new component and re-render it. Another way is by calling the forceUpdate() method on the component instance. This will cause the component to re-render without updating the state or props. It should be used with caution, it can cause unexpected behavior if used improperly.
</details>
<br />

<details>
<summary>What is strict mode in React ?</summary>
Strict Mode is a feature in React that helps you to identify potential problems in your code. It is not a part of the production build, but it can help you during development. When a component is wrapped by StrictMode, it will perform extra checks and warnings for its descendants.
</details>
<br />

<details>
<summary>What are React Mixins ?</summary>
React Mixins were a way to share behavior among multiple components in React. It allows you to reuse component logic and is implemented by merging an object of methods into a component's prototype. React Mixins are now considered as an anti-pattern and not recommended because they can make code harder to understand and lead to problems such as name collisions or component state inconsistencies.
</details>
<br />

<details>
<summary>How to enable production mode in React ?</summary>
If you are using create-react-app, it will automatically set the environment variable to production when you run the `npm run build` command.
</details>
<br />

<details>
<summary>What is the lifecycle methods order in mounting ?</summary>
The order of lifecycle methods that are called when a component is being "mounted" (inserted into the DOM) in React are as follows:

- constructor()
- static getDerivedStateFromProps()
- render()
- componentDidMount()
</details>
<br />

<details>
<summary>What is React Fiber ?</summary>
React Fiber is a new reconciliation algorithm in React that improves the handling of complex UIs and high-frequency updates. It builds on top of the stack reconciliation algorithm used in previous versions of React, and is able to split rendering work into smaller chunks, allowing the browser to respond to user input more quickly and smoothly. React Fiber was introduced in React v16 and it's the foundation of upcoming features such as "concurrent mode"
</details>
<br />

<details>
<summary>What is the main goal of React Fiber ?</summary>
The main goal of React Fiber is to improve the performance and responsiveness of React applications, especially in situations where the UI needs to update frequently or handle complex user interactions. React Fiber provides a more efficient way of reconciling the virtual DOM, by breaking the work into smaller chunks and being able to pause, abort, or reuse work as needed. This allows React to prioritize updates and make better use of the browser's idle time, resulting in a smoother and more responsive user experience.
</details>
<br />

<details>
<summary>What is the difference between useMemo and useCallback ?</summary>
useMemo is a React Hook that is used to memoize a value and only re-compute it when one of its dependencies changes.

useCallback is similar to useMemo, but it is used to memoize a callback function, and only return a new function when one of its dependencies change.

In short, useMemo is used to optimize computation intensive value and useCallback is used to optimize function and events callbacks.

</details>
<br />

<details>
<summary>What is React state batching ?</summary>
React state batching is a feature of React that allows multiple state updates to be combined into a single update and processed as a single render pass. This reduces the number of times the component re-renders, resulting in better performance. React does this by collecting all state updates that occur during a single event loop and applying them together. This applies for both setState calls and state updates made by hooks
This feature makes React more efficient and faster by reducing unnecessary re-renders and updates to the DOM.
</details>
<br />

<details>
<summary>What is the difference between npx and npm ?</summary>
npx is a package runner that comes with npm (Node Package Manager) starting from version 5.2.0. npm is a package manager for JavaScript, it's used to install packages, manage and share packages.

npx allows you to easily run command-line tools and other executables hosted on the npm registry, without having to install them globally on your system.

npm on the other hand, is mainly used to install and manage dependencies for a project, and it's mostly used for managing the project's development and production environment.

</details>
<br />

<details>
<summary>How to validate Props in React ?</summary>
In React, you can use the built-in prop-types library to validate the props passed to a component. This can be done by adding a propTypes property to the component and specifying the expected type of each prop. To use prop-types, you need to import it and then use the validator functions such as PropTypes.string , PropTypes.number etc. to specify the type of the props, also you can use isRequired to make it mandatory props.

```jsx
import PropTypes from "prop-types";

function App(props) {
  return <div> {props.name}</div>;
}

App.propTypes = {
  name: PropTypes.string.isRequired,
  age: PropTypes.number,
};

export default App;
```

</details>
<br />

# React Interview Question and Answer

## `Level 0`

<details>
<summary>What is React?</summary>
React is an open-source front-end JavaScript library that is used for building user interfaces, especially for single-page applications. It is used for handling view layer for web and mobile apps. React was created by Jordan Walke, a software engineer working for Facebook. React was first deployed on Facebook's News Feed in 2011 and on Instagram in 2012.
</details>
<br>

<details>
<summary>What are the major features of React?</summary>
The major features of React are:

-   It uses VirtualDOM instead of RealDOM considering that RealDOM manipulations are expensive.
-   Supports server-side rendering.
-   Follows Unidirectional data flow or data binding.
-   Uses reusable/composable UI components to develop the view.
</details>
<br>

<details>
<summary>What is JSX?</summary>
JSX is a XML-like syntax extension to ECMAScript (the acronym stands for JavaScript XML). Basically it just provides syntactic sugar for the React.createElement() function, giving us expressiveness of JavaScript along with HTML like template syntax.

In the example below text inside `<h1>` tag is returned as JavaScript function to the render function.

```js
export default function App() {
    return (
        <div>
            <h1>{'Welcome to Happy Learning'}</h1>
        </div>
    );
}
```

</details>
<br>

<details>
<summary> Can web browsers read JSX directly? </summary>

-   Web browsers cannot read JSX directly. This is because they are built to only read regular JS objects and JSX is not a regular JavaScript object

-   For a web browser to read a JSX file, the file needs to be transformed into a regular JavaScript object. For this, we use Babel

</details>
<br>

<details>
<summary>What are the most crucial advantages of using React?</summary>
Following is a list of the most crucial advantages of using React:

-   ## React is easy to learn and use

    React comes with good availability of documentation, tutorials, and training resources. It is easy for any developer to switch from JavaScript background to React and easily understand and start creating web apps using React. Anyone with little knowledge of JavaScript can start building web applications using React.

-   ## React follows the MVC architecture.

    React is the V (view part) in the MVC (Model-View-Controller) architecture model and is referred to as "one of the JavaScript frameworks." It is not fully featured but has many advantages of the open-source JavaScript User Interface (UI) library, which helps execute the task in a better manner.

-   ## React uses Virtual DOM to improve efficiency.

    React uses virtual DOM to render the view. The virtual DOM is a virtual representation of the real DOM. Each time the data changes in a react app, a new virtual DOM gets created. Creating a virtual DOM is much faster than rendering the UI inside the browser. Therefore, with the use of virtual DOM, the efficiency of the app improves. That's why React provides great efficiency.

-   ## Creating dynamic web applications is easy.

    In React, creating a dynamic web application is much easier. It requires less coding and gives more functionality. It uses JSX (JavaScript Extension), which is a particular syntax letting HTML quotes and HTML tag syntax to render particular subcomponents.

-   ## React allows reusable components.

    React web applications are made up of multiple components where each component has its logic and controls. These components provide a small, reusable piece of HTML code as an output that can be reused wherever you need them. The code reusability helps developers to make their apps easier to develop and maintain. It also makes the nesting of the components easy and allows developers to build complex applications of simple building blocks. The reuse of components also increases the pace of development.

-   ## React has a rich set of libraries.
    React has a huge ecosystem of libraries and provides you the freedom to choose the tools, libraries, and architecture for developing the best application based on your requirement.

</details>
<br>

<details>
<summary>Why we use JSX?</summary>
-   It is faster than regular JavaScript because it performs optimization while translating the code to JavaScript.
-   Instead of separating technologies by putting markup and logic in separate files, React uses components that contain both.

-   It makes easier to create templates.
</details>
<br>

<details>
<summary></summary>
</details>
<br>

<details>
<summary></summary>
</details>
<br>

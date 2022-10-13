# React-basics
## 📖 Definition ##
React is **an open-source, front-end JavaScript library** built/maintained in 2013 by Facebook as well as a community of individual developers and companies.
It's purpose is to build user interfaces or UI components.

#### React uses ES6, and you should be familiar with some of the new features like: ####

- Classes
- Arrow Functions
- Variables (let, const, var)
- Array Methods like .map()
- Destructuring
- Modules
- Ternary Operator
- Spread Operator

React creates a VIRTUAL DOM in memory. Instead of manipulating the browser's DOM directly, React creates a virtual DOM in memory, 
where it does all the necessary manipulating, before making the changes in the browser DOM.

✅ JSX allows us to write HTML in React. 

**JSX allows us to write HTML elements in JavaScript and place them in the DOM without any createElement()  and/or appendChild() methods.**

## Setting up a React Environment ##

To use React in production, you need **npm which is included with Node.js.**


If you have npx and Node.js installed, you can create a React application by using create-react-app.

You can run the following command to see if it is already installed for your current npm version:

```
$ which npx
```
If it's not, you can install it like this:

```
$ npm install -g npx
```

To create a React application by using create-react-app: 

```
npx create-react-app my-react-app
```

The create-react-app will set up everything you need to run a React application.

Now you are ready to run your first real React application!

Run this command to move to the my-react-app directory:
```
cd my-react-app
```
Run this command to run the React application my-react-app:

```
npm start
```
A new browser window will pop up with your newly created React App! If not, open your browser and type localhost:3000 in the address bar.

**Within React there is a Hierarchy that occurs when building and scaling our applications.**

Typically in most apps, we have a Root Component called **App** this is where all other components end up reaching through the component tree.

Look in the my-react-app directory, and you will find a **src** folder. Inside the src folder there is a file called **App.js.**

You can add a child component (ex. Contacts) inside the App Component. 

When Components are contained within other Components higher up the tree, these are known as **Parent and Child relationships.** 

**❗️Worth Mentioning that all components can be parents or children of another component (except app, which only can be the parent).❗️**


## React component ##
**React component  is an independent and reusable piece of code.**


There are 2 types of React components:
- Functional components
- Class components

### Functional components are Javascript Functions. ###

They return JSX and this JSX is rendered in the browser as DOM. 

**Worth mentioning you can define the component using a function declaration or a function expression.**

```
function MyComponent() {
  // I can add any JS logic here! 👍 
  const myName = 'Bob';
  return (
   <div>
      <h1>I can write whatever I want here</h1>
      <p>Hello {myName}</p>
    </div>
 );
}
```

```
const MyComponent = () => {
  // Arrow function also work 👍 
  return (
    <div>
      <h1>I can write whatever I want here</h1>
    </div>
  );
};
```
### Class components come in a Javascript class and you need to explicitly define a render method to render JSX in the browser. ###

```
class MyComponent {
  render() {
    // don't forget to return some JSX ☝️
    return (
      <div>
        <h1>I can write whatever I want here</h1>
      </div>
    );
  }
}
```

**❗️ React Components (functional and class) should be named with PascalCase❗️**

Also,  React Components only should return one HTML tag, if you need to return multiple items, wrap all the items into a single container.

## PROPS ##

**“Props” is a special keyword in React, which stands for properties and they are used for passing data from one component to another.**

❗️ Props are passed from Parent components to Child components. ❗️

Properties and values are "packed" into an object to be sent to the child component. You can retrieve this object thanks to the first parameter of your component function.

```
const Contact = (props) => {
  console.log(props)
 // logs: { name: "Emmanuel", phone: "15525264", age: 22 }
 console.log(props.name)
 // logs: "Emmanuel"

 return (
    <div className="friend-item">
      <h3>Emmanuel</h3>
      <h4>
        📧emmanuel@email.com
        <br />
        📞234234234
      </h4>
      <button>Delete</button>
    </div>
  );
};

export const App = (
  <div>
    <h1 className="text-center">My contacts list 📱</h1>

    <div>
      <div>
        <Contact name="Emmanuel" phone="15525264" age={18 + 4} />
      </div>
   </div>
  </div>
);
``` 

- If you don't pass any props from the parent, the props object will be an empty object.
- Props are read-only.
- Props can be of any type string, function, number, etc.
- Props is an object with key-value pairs.


## Expressions and Statements within JSX ##

### An expression is something that returns a value. ###

```
const isOnline = true;
```

```
isOnline ? "User is Online" : "User is Offline"
```

```
const numbers = [1, 4, 9, 16];
/ pass a function to map
const numbersMultipliedBy2 = numbers.map(number => number * 2);
console.log(numbersMultipliedBy2);
// expected output: Array [2, 8, 18, 32]
```


### A statement is something that performs or controls one or more actions but it does not return a value. ###

The first example of a statement is a control structure such as a simple if / else.

```
const testScore = 60;
if(testScore > 50) {
 console.log('You have passed the test')
} else {
 console.log('You need to retake the test') }
 ```
 
**In React, you can conditionally render components by using:**
- if Statement
- Logical && Operator
- Ternary Operator.

Conditional rendering in React works the same way conditions work in JavaScript. 
Use JavaScript operators like if or the conditional operator to create elements representing the current state, 
and let React update the UI to match them.


The second example of a statement is a control structure such as a simple for loop.

```
for (i = 0; i < 5; i++) {
  console.log(`The current number in the loop is ${[i]}`)
}
```









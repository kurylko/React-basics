# React-basics
## 📖 Definition ##
React is **an open-source, front-end JavaScript library** built/maintained in 2013 by Facebook as well as a community of individual developers and companies.
It's purpose is to build user interfaces or UI components.

React creates a VIRTUAL DOM in memory. Instead of manipulating the browser's DOM directly, React creates a virtual DOM in memory, 
where it does all the necessary manipulating, before making the changes in the browser DOM.

✅ JSX allows us to write HTML in React. 

**JSX allows us to write HTML elements in JavaScript and place them in the DOM without any createElement()  and/or appendChild() methods.**

## Let's create first React project ##

To use React in production, you need **npm which is included with Node.js.**


If you have npx and Node.js installed, you can create a React application by using create-react-app.

```
npx create-react-app my-react-app
```

The create-react-app will set up everything you need to run a React application.

Run the React Application
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

Look in the my-react-app directory, and you will find a src folder. 
Inside the src folder there is a file called **App.js.**


## React component ##
**React component  is an independent and reusable piece of code.**


There are 2 types of React components:
- Functional components
- Class components

### Functional components are Javascript Functions. ###

They return JSX and this JSX is rendered in the browser as DOM. 

Worth mentioning you can define the component using a function declaration or a function expression.

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










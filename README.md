# React-basics
## 📖 Definition ##
React is **an open-source, front-end JavaScript library** built/maintained in 2013 by Facebook as well as a community of individual developers and companies.
It's purpose is to build user interfaces or UI components.

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









```react
export default function MyApp() {

return (

<div>

<h1>Welcome to my app</h1>

<MyButton />

</div>

);

}
```
Notice that <MyButton /> starts with a capital letter. That’s how you know it’s a React component. React component names must always start with a capital letter, while HTML tags must be lowercase.

JSX is stricter than HTML. You have to close tags like <br />. Your component also can’t return multiple JSX tags. You have to wrap them into a shared parent, like a <div>...</div> or an empty <>...</> wrapper:

Pull in Bootstrap’s source files into nearly any project with some of the most popular package managers.

U can only import the components which are present inside “src”

In react u will write all the JS code with in curly braces

JSX lets you put markup into JavaScript. Curly braces let you “escape back” into JavaScript so that you can embed some variable from your code and display it to the user. For example, this will display user.name:


```return (
  <h1>
    {user.name}
  </h1>
)
```
Responding to events

```function MyButton() {
  function handleClick() {
    alert('You clicked me!');
  }

  return (
    <button onClick={handleClick}>
      Click me
    </button>
  );
}
```
Notice how onClick={handleClick} has no parentheses at the end! Do not call the event handler function: you only need to pass it down. React will call your event handler when the user clicks the button

Conditional rendering

In React, there is no special syntax for writing conditions. Instead, you’ll use the same techniques as you use when writing regular JavaScript code. For example, you can use an if statement to conditionally include JSX:

```let content;
if (isLoggedIn) {
  content = <AdminPanel />;
} else {
  content = <LoginForm />;
}
return (
  <div>
    {content}
  </div>
);
```
If you prefer more compact code, you can use the conditional ? operator. Unlike if, it works inside JSX:

```
<div>
  {isLoggedIn ? (
    <AdminPanel />
  ) : (
    <LoginForm />
  )}
</div>
```
✅ Common Event Handlers in React:

|Event type|React Attribute|Example                  |
|:----------|:---------------:|----------------------:|
|Click|onClick             |<button onClick={fn}>|
|Change (inputs)|onChange  |<input onChange={fn} />|
|Submit|onSubmit           |<form onSubmit={fn}>|
|Mouse Over|onMouseOver    |<div onMouseOver={fn}>|
|Key Press|onKeyPress      |<input onKeyPress={fn} />|

Often, you’ll want your component to “remember” some information and display it. For example, maybe you want to count the number of times a button is clicked. To do this, add state to your component.

First, import useState from React:


import { useState } from 'react';

what is the use of tailwind css

Tailwind CSS is a utility-first CSS framework used to style your web applications quickly and consistently by applying pre-defined classes directly in your HTML or JSX.

Tailwind Class

Effect

bg-blue-500

Background color

text-white

Text color

p-2

Padding

rounded

Border radius (rounded corners)

shadow

Adds box shadow


#React Developer Tools 
React DevTools let you check the props and the state of your React components. You can find the React DevTools tab at the bottom of the browser section in CodeSandbox:
``Every module can have two different types of export, named export and default export. You can have multiple named exports per module but only one default export.``

```
// export features declared elsewhere
export { myFunction2, myVariable2 };

// export individual features (can export var, let,
// const, function, class)
export let myVariable = Math.sqrt(2);
export function myFunction() {
  // …
}
```
After the export keyword, you can use let, const, and var declarations, as well as function or class declarations. You can also use the export { name1, name2 } syntax to export a list of names declared elsewhere. Note that export {} does not export an empty object — it's a no-op declaration that exports nothing (an empty name list).


Named exports are useful when you need to export several values. When importing this module, named exports must be referred to by the exact same name (optionally renaming it with as), but the default export can be imported with any name. For example:
```
const k = 12;
export default k;
```
You can also rename named exports to avoid naming conflicts:
```
export { myFunction as function1, myVariable as variable };
```
There is also export * from "mod", although there's no import * from "mod". This re-exports all named exports from mod as the named exports of the current module, but the default export of mod is not re-exported. If there are two wildcard exports statements that implicitly re-export the same name, neither one is re-exported.
JSX is stricter than HTML. You have to close tags like <br />.
You have to wrap them into a shared parent, like a <div>...</div> or an empty <>...</> wrapper:
```
function AboutPage() {
  return (
    <>
      <h1>About</h1>
      <p>Hello there.<br />How do you do?</p>
    </>
  );
}
```
#Responding to events 
You can respond to events by declaring event handler functions inside your components:
```
function MyButton() {
  function handleClick() {
    alert('You clicked me!');
  }

  return (
    <button onClick={handleClick}>
      Click me
    </button>
  );
}
```
Notice how onClick={handleClick} has no parentheses at the end! Do not call the event handler function: you only need to pass it down. React will call your event handler when the user clicks the button.



# React Basics

## What the hell is React?
**React is a Javascipt library**
React's ultimate purpose is to show content to users and handle user interaction.

## What is JSX?
JSX looks like HTML and can be placed in Javascript code. It determines the content of the React app just like normal HTML.

## What is a react component?
Function or Class that produces HTML to show the user (JSX) and handle feedback from the user (event handler).

## React and React-DOM? What is the difference?
**React** knows what a component is and how to make components work together.

**React-DOM** knows how to make a component and make it show up in the DOM.

## Starting react
1. ```npm install -g create-react-app``` 

    npm(node packet manager), install -g(globally) create-react-app(name of package)

2. ```create-react-app projectName```

>alternate way: npx create-react-app projectName

## Project Directory
1. src (Folder for source code)
2. public (Folder to store static file)
3. node_modules (Folder that contains all of project dependencies)
4. package.json (Record project dependencies and configure them)
5. package-lock.json (Records exact version of package installed)
6. README.md
7. .gitignore

## Starting a react app
```npm start```

To stop:

```cntl + c```

## Common Errors
1. Port is in use

    Just use another port.
2. Local host 3000 not working

    Find On Your Network and copy paste URL.

## The index.js file
1. Import the React and ReactDOM libraries
```Javascript
import React from 'react';
import ReactDOM from 'react-dom';
```

2. Create a react component
```Javascript
const App = () => {
    return <div>Hi there!</div>;
};
```

3. Take the react component and show it on the screen
```Javascript
ReactDOM.render(
    <App />,
    document.querySelector('#root')
)
```
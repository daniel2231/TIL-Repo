# State

## Rules of State
- Only usable with class components (can be used with "hooks" system)
- You will confuse props with state
- 'State' is a JS object that contains data relevant to a singular component 
- Updating 'State' on a component causes the component to (almost) instantly rerender
- State must be initialized when a component is created
- **State can only be updated using the function 'setState'**

## Constructor
- First called when instance is created
- a way to initialize states
- super -> make sure components get called

## Example
```JavaScript
import React from 'react';
import ReactDOM from 'react-dom';

class App extends React.Component {
    constructor(props) {
        super(props);

        this.state = { lat: null };

        window.navigator.geolocation.getCurrentPosition(
            (position) => {
                this.setState({ lat: position.coords.latitude });
            },
            (err) => console.log(err)
        );
    }

    render() {
        return <div>Latitude: {this.state.lat}</div>
    }
}

ReactDOM.render(<App />, document.querySelector("#root"));
```
## Flow (Lifecycle)
1. JS file loaded by browser
2. Instance of App component is created
3. App components 'constructor' function gets called
4. State object is created and assigned to the 'this.state' property
5. We call geolocation service
6. React calls the components render method
7. App returns JSX, gets rendered to page as HTML
8. We get result of geolocation
9. We update our state object with a call to 'this.setState'
10. React sees that we updated the state of a component
11. React calls our 'render' method a second time
12. Render method returns some updated JSX
13. React takes that JSX and updates content on the screen

## Conditionally rendering content

We can use if statement to conditionally render content.

## Component Lifecycle methods
1. constuctor - good place to do one-time setup
2. render - avoid doing anything besides returning JSX
3. **content visible on screen**
4. componentDidMount - Good place to do data-loading
5. **sit and wait for updates**
6. componentDidUpdate - Good place to do more data loading when state/props change
7. **sit and wait until this component is not longer shown**
8. componentWillUnmount - Good place to do cleanup (especially for non-react stuff)

## Refactoring state
```Javascript
    constructor(props) {
        super(props);

        this.state = { lat: null };
```
Can be changed into:
```JavaScript
state = { lat: null };
```
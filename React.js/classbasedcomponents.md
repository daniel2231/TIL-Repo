# Class Based Components

## Functional Components vs Class Components
Functional Components are good for simple content.

Class Components are good for just about anything else.

## Benefits of Class Components

- Easier code organization
- Can use 'state', which makes it easier to handle user input
- Understands lifecycle events, easier to do things when the app first starts

## Handling Async operations with functional components
Lifecycle example (geolocation)
- Js file loaded by browser
- App component get created
- We call geolocation service
- App returns JSX, gets rendered to page HTML
- We get result of geolocation
- Tell the components to rerender itself with this new information

## Rules of CLass Components
- Must be a Javascript Class
- Must extend (subclass) React.Component
- Must define a 'render' method that returns some amount of JSX

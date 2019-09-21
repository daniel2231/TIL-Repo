# Components and Props

## Component Nesting

A component can be shown inside of another.

## Component Resuability

We want to make components that can be easily reused through out application.

## Component Configuration

We should be able to configure a component when it is created.

## Steps to make a component
1. Identify the JSX that appears to be duplicated
2. What is the purpose of that block of JSX? Think of a descriptive name for what it does.
3. Create a new file to house this new component - it should have the same name as the component
4. Create a new component in the new file - paste the JSX into it
5. Make the new component configurable by using React's 'props' system
6. Export the component and import it in index.js

## Props (Properties)

System for passing data from a parent component to a child component.

Goal is to customize or configure a child component.

```JavaScript
<ComponentName NameofProp = "Value" />
```

To pass props within component, do this:
```JavaScript
<ComponentName>{props.children}</ComponentName>
```
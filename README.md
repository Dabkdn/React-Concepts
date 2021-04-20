# React-Concepts

## DOM and Virtual DOM

| DOM  | Virtual DOM |
| ------------- | ------------- |
| It updates slow.  | It updates faster.  |
| Can directly update HTML.  | Can’t directly update HTML.  |
| Creates a new DOM if element updates. |  Updates the JSX if element updates. |
| Too much of memory wastage. | No memory wastage. |

A virtual DOM is a lightweight JavaScript object which originally is just the copy of the real DOM. It is a node tree that lists the elements, their attributes and content as Objects and their properties. React’s render function creates a node tree out of the React components.
This Virtual DOM works in three simple steps.

- Whenever any underlying data changes, the entire UI is re-rendered in Virtual DOM representation.
![image](/image/virtual_dom_1.png)
- Then the difference between the previous DOM representation and the new one is calculated.
![image](/image/virtual_dom_2.png)
- Once the calculations are done, the real DOM will be updated with only the things that have actually changed. 
![image](/image/virtual_dom_3.png)

## JSX

JSX is a shorthand for JavaScript XML. This is a type of file used by React which utilizes the expressiveness of JavaScript along with HTML like template syntax. This makes the HTML file really easy to understand. This file makes applications robust and boosts its performance.

Browsers can only read JavaScript objects but JSX in not a regular JavaScript object. Thus to enable a browser to read JSX, first, we need to transform JSX file into a JavaScript object using JSX transformers like Babel and then pass it to the browser.

## Props

Props is the shorthand for Properties in React. They are read-only components which must be kept pure i.e. immutable. They are always passed down from the parent to the child components throughout the application. A child component can never send a prop back to the parent component.

## State

States are the source of data and must be kept as simple as possible. Basically, states are the objects which determine components rendering and behavior. They are mutable unlike the props and create dynamic and interactive components. They are accessed via this.state().

## Life cycle

There are three different phases of React component’s lifecycle:

- Initial Rendering Phase: This is the phase when the component is about to start its life journey and make its way to the DOM.
- Updating Phase: Once the component gets added to the DOM, it can potentially update and re-render only when a prop or state change occurs. That happens only in this phase.
- Unmounting Phase: This is the final phase of a component’s life cycle in which the component is destroyed and removed from the DOM.

![image](/image/lifecycle.png)

## Refs

Following are the cases when refs should be used:

- When you need to manage focus, select text or media playback
- To trigger imperative animations
- Integrate with third-party DOM libraries

## HOC

Just think about it, it receive a component and return another component like this:
 ```javascript
 const secondComponent = HOCComponent(firstComponent)
 ```

 ```javascript
 import React from 'react';
const higherOrderComponent = (WrappedComponent) => {
  class HOC extends React.Component {
    render() {
      return <WrappedComponent />;
    }
  }
  return HOC;
};
```
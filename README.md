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

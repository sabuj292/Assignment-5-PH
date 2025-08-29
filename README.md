
####  Q1) What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?

Ans: 
- **getElementById** → Returns a single element with the given ID.  
- **getElementsByClassName** → Returns a live HTMLCollection of elements with the given class.  
- **querySelector** → Returns the **first** element matching a CSS selector.  
- **querySelectorAll** → Returns a static NodeList of **all** elements matching a CSS selector.

#### Q2) How do you create and insert a new element into the DOM?
Ans:
```js
let div = document.createElement("div");
div.textContent = "Hello World";
document.body.appendChild(div);
```

#### Q3) What is Event Bubbling and how does it work?
Ans:
- **Event Bubbling** is the process where an event starts from the **target element** and then moves upward through its parent, grandparent, and so on up to the root (document).  
- Example: If I click a button inside a `<div>`, the click event first triggers on the button, then on the div, then on the body, and finally on the document (unless stopped).

#### Q4) What is Event Delegation in JavaScript? Why is it useful?
Ans:
Event Delegation → Attaching an event listener to a parent element to handle events of its child elements via bubbling.
It is useful as It reduces the number of event listeners, which increases the performance. Again, it handles dynamically added child elements.


#### Q5) What is the difference between preventDefault() and stopPropagation() methods?
Ans:
preventDefault() → Stops the default browser behaviour, for example, it prevents form submission, stops link navigation, etc.
stopPropagation() → Stops the event from going (bubbling) up to parent elements.

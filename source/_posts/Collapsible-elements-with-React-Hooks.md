---
title: Collapsible elements with React Hooks
date: 2020-09-15 11:31:16
tags: react, hooks, frontend
---
Today, we're building this:

{% jsfiddle t27oL9cn %}

In React, we don't have access to the underlying DOM element. To gain access to the element, we have to utilize the special `ref` property. Usually this property er associated with the [`useRef`](https://reactjs.org/docs/hooks-reference.html#useref) hook. However, it is also possible to [pass a simple callback function](https://reactjs.org/docs/refs-and-the-dom.html#callback-refs) to the `ref` property, like this:

```jsx
const CallbackComponent = () => {
    function callback(divNode) {
        // Do something meaningful with the node here
    }

    return (
        <div ref={callback}></div>
    );
};
```
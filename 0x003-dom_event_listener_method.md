# Dom Event Listener Method

The <b>addEventListener() </b> method attaches an event handler to a specified element.

- Does not over-ride existing handlers.
- Takes 3 parameters.

1.  Type of event passed in as a string. EG: click, mousedown, mouseenter e.t.c.

2.  Function we want to call when the specified event occurs.

Example:

```js
const btn = document.getElementById("btn");

btn.addEventListener("click", function () {
  console.log("Button Clicked");
});
```




## Assignment: (Read on Event Propagation)

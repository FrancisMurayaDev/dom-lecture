# DOM Events

Event in DOM is action or occurrence in browser, the browser can respond to.

Events are a result of user interactions such as clicks, key presses or mouse movements.

## Some Popular DOM Events.

1. Onclick

- triggered when an element is clicked.

```js
const btn = document.getElementById("btn");
btn.onclick = function () {
  console.log("Button Clicked");
};
```

2. onmouseover

- when the mouse moves over an element.

3. onmouseout

- Triggered when the mouse pointer moves out of an element.

4. onkeydown

- when a key is pressed down.
- usually called on the document, i.e: document.onkeydown = function() {}

5. onkeyup

- Triggered when a key is released.
- Usually called on the document, i.e. document.onkeydown = function() {}

6. onload

- Triggered when the entire page has finished loading.

- Called on window i.e: window.onload = function() {}

7. onfocus

- Triggered when an element gains focus.

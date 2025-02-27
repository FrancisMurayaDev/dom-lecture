# Changing DOM Elements

- Changing the content, attributes and styling of DOM elements.

With the elements selected, we can manipulate html elements and do some magic.

## Changing HTML elements content
There are 3 Ways:
- innerHTML
- innerText
- textContent

### innerHTML

Sets or gets inner html content of an element.
- It preserves the html tags.

```js
<div id="my-div">
  <h1>Hello, world</h1>
  <p>JavaScript is awesome</p>
</div>
```

```js
const div = document.getElementById("my-div"); //start by getting the div
console.log(div.innerHTML); // getting the inner html of the div
div.innerHTML = `<h1>New content</h1>`; //setting the innerHTML of that div using the innerHTML property.
console.log(div.innerHTML);
```

### innerText

Sets or get the text content of an element not preserving the HTML TAGS.

```js
<div id="my-div">
  <h1>Hello, world</h1>
  <p>JavaScript is awesome</p>
</div>
```

```js
const div = document.getElementById("my-div");//get the div
console.log(div.innerText);//get innerText
div.innerText = "New content"; //change innerText
console.log(div.innerText);
```
- Even if we write the HTML elements when setting the innerText, the elements will appear as texts, it does not preserve the html elements.

### textContent

Sets or gets the text content of an element and its descendants without preserving the HTML tags.
- does the same thing what `.innerText` does.

- More consistent across browser compared to <i>innerText </i>

## How to Update a HTML Element without Distorting it. 

- We start by appending a child to a HTML element.

Lets say we have a div which we want to change its innerHTML without interfering with the current one:

```html
<div class="container-div">
    <p>Good Morning</p>
    <p>Hello World</p>
  </div>
  ```

  - Lets first select the `div` using `document.querySelector`.

  ```js
  let div = document.querySelector('.container-div');
  ```
  - Create the html element that you want to add using `document.createElement()`, give it an `innerText` then `appendChild` to the div.

  ```js
  const heading2 = document.createElement('h2'); // create the element.

  heading2.innerText = 'Programming is Fun'; //The inner text of the h2 created.

  div.appendChild(heading2); // specify the child to append.

  console.log(div.innerText);
  ```
  




## Changing the attribute of HTML elements.

We use `element.attribute = value`.

```js
<h1 class="title" id="title">
  Hello, world
</h1>
```

```js
const title = document.getElementById("title");
console.log(title); // <h1 class="title" id="title">Hello, world</h1>
title.id = "awesome-title";
console.log(title); // <h1 class="title" id="awesome-title">Hello, world</h1>
```

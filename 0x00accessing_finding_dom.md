# Accessing/Finding DOM Elements

To access any element in an HTML page, we start by accessing the <i>document </i> object.

The document object owns other page objects.

## Methods of Accessing DOM Elements.

### document.getElementById(elementID)

```js
<button id="my-button">Click Me</button>
```

```js
const button = document.getElementById("my-button");
console.log(button); // <button id="my-button">Click Me</button>
```

### document.getElementsByTagName(name)

Targets elements that match a tag name.
You can index the specific element in the Node List (HTML Collection) as in indexing in array.

```js
<p>Hello, World</p>
<p>JavaScript is awesome</p>
<p>JavaScript is great</p>
```

```js
const paragraphs = document.getElementsByTagName("p");
console.log(paragraphs); // [p, p, p]
```

### document.getElementByClassName(className)

Returns all elements with a similar class. Indexing is used to get specific element.

```js
<p class="text">Hello, World</p>
<p class="text">JavaScript is awesome</p>
<p>JavaScript is great</p>
```

```js
const texts = document.getElementsByClassName("text");
console.log(texts); // [p.text, p.text]
```

### document.querySelector(selector)

selects the first element with a specific CSS selector.

- You specify the selector the way you specify it in CSS.
  For example: the ID and Class.

```js
const firstText = document.querySelector(".text");
console.log(firstText);
```

### document.querySelectorAll(selector)

Selects all elements in the document that match specified class, id or tag name and returns a node list of them.

- It cannot be used with an ID since only one ID should correspond to one element.

```js
<p class="text">Hello, World</p>
<p class="text">JavaScript is awesome</p>
<p>JavaScript is great</p>
```

```js
const paragraphs = document.querySelectorAll("p");
console.log(paragraphs); // [p.text, p.text, p]
```

```js
const title = document.getElementById("title");
console.log(title); // <h1 class="title" id="title">Hello, world</h1>
title.id = "awesome-title";
console.log(title); // <h1 class="title" id="awesome-title">Hello, world</h1>
```

We can also select elements with a certain class.
For example:

```js
document.querySelectorAll("p.text");
//This will select all paragraphs with the class of Text
```

If you have a different element with the same class, it will not be selected.

We can also use <b> element.setAttribute ("attribute", "value")</b>

```js
<h1 class="title" id="title">
  Hello, world
</h1>
```

```js
const title = document.getElementById("title");
console.log(title); // <h1 class="title" id="title">Hello, world</h1>
title.setAttribute("id", "awesome-title");
console.log(title);
```

## Changing the styling of HTML Elements.

We can use <em>element.style.property = "value ."</em>

It is essential to input the value in double quotes even if it is a number.

```js
const title = document.getElementById("title");
title.style.border = "3px solid red";
title.style.fontSize = "48px";
title.style.borderRadius = "5px";
```

### Changing Styling in JavaScript using CSS classes.

- element.classList.add() : adds one or more class names to an element without removing the existing classes.

- Element.classList.toggle() : toggles the specified class, it is present, it is removed, if it is absent, it is added.

- element.classList.contains(): returns true if an element contains the specified classes(es), false otherwise.

- element.classList.replace() : replaces an existing class with a new one.

- element.style.setProperty() : sets a CSS property on an element (first parameter) and its value (second parameter).

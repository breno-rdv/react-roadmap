# Creating element in JS

Creating an element in Vanilla Javascript for Web Application is done by using the function `createElement()`, available in [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) document.

This function returns a new element, this element itself won't appear in the DOM unless you append it to an existing node in the [document](https://developer.mozilla.org/en-US/docs/Web/API/Document).

After creating this element, many properties can be added to it, e.g. after creating a button, a meaninful name can be giving to it.

````Javascript
const button = document.createElement('button');
button.textContent = 'Send message';
````
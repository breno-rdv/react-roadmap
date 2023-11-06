# JSX
JSX (Javascript XML) is a html-like syntax in Javascript, bringing an ergonomic way to write React code.

Browser only understands HTML and Javascript, not them mixed up.

The code below is not supported by the Browser.

```HTML
    <div className='container' {...props}/>
```

That's why Babel comes into play

[Babel](https://babeljs.io/)

Self-closing tags

Interpolation {} put any expression, in  declarative and deterministic way

Spread props

As Babel uses Object.assign to extend props, to override one of them, we have to put it right after the props declaration.

React projects come with a build process that transforms JSX code.

So for creating a React component, you need to follow to rules:
- Create a function that starts with uppercase character
- Return a JSX Element, that can be a 
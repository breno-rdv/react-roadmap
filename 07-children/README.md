# Children

The children prop is a built-in property in React components, everything put in between your component's declaration
is considered as a child component.

This allows to use Components composition for building reusable components.

## Use cases

Children is a special property of React component, but just including it like we are
doing in Title component below, is not enough. React needs to know where it should be rendered
in.

```Javascript
const Title = () => {
    return (
        <h1></h1>
    );
}

const Header = () => {
    return (
        <div>
            <Title>React is awesome</Title>
        </div>
    );
}
```

Yet, `props.children` you always exist event though you don't pass anything to a component.
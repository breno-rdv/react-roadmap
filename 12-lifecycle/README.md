# Component's lifecycle
Each React component has its own lifecycle, going through each of the following steps:

## Mounting
When an instance of a component is being created and inserted to the DOM.
The mounting phase has four lifecycle methods, being:

### constructor() {}
It will get called whenever a new component is created.
- Ideal for initializing state and binding the event handlers;
- Do not cause side-effects;
- super() has to be called as a component extends React.component;
- Directly overwrite this.state;

### static getDerivedStateFromProps(props, state) {}
It is a rarely used method.
- It's used when a component's state depends on changes in props over time;
- State can be set, as a static method, there is no access to `this`, an object
with the new state has to be returned, return null in case the method be declared;
- Do not cause side-effects;

### render() {}
The only required method.
- Read props and state and return JSX (pure function)
- Do not change state, interact with the DOM, or make AJAX calls;
- Child component's lifecycle methods are also executed;

### componentDidMount() {}
Invoked immediately after a component and all its children components have been
rendered to the DOM
- The right place to perform side-effects, i.e interact with the DOM, AJAX calls, etc.


## Updating
When a component is being re-rendered as a result of changes to props or state,
or a parent re-renders.

### static getDerivedStateFromProps(props, state) {}
Reminder: This method is called every time a component is re-rendered.
And has the same behavior as in mounting lifecycle.

#### shouldComponentUpdate(nextProps, nextState) {}
It dictates if the component should re-render or not.
- Ideal for perfomance optimization;
- Changing state should be avoided;
- Ajax calls should be avoided;

** If component re-rendering be not desired, null must be returned **

#### render() {}
Same behavior as in other lifecycles.

#### getSnapshotBeforeUpdate(prevProps, prevState) {}
It is called right before the changes from the Virtual DOM are to be reflected to the DOM.
- Capture some information from the DOM;
- Method will either return null or return a value;

** Returned value will be passed as the third parameter to `componentDidUpdateMethod`**

### componentDidUpdate(prevProps, prevState, snapshot) {}
It is called after the render finishes and can check if components and children have been rendered correctly.
- Cause side-effects;
- It runs only once after every re-render;

## Unmounting
When a component is being removed from the DOM.
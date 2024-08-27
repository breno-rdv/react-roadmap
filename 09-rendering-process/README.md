# Rendering process

React operates with deterministic algorithm by focusing on components creation, just defining how
component will look like, and then React takes care of how to mount it into the DOM.

In Vanilla JS, on the other hand, everything is performed imperativily, codes are written to
manipulate the DOM.

A component declared, return in fact, an object. This object is saved in something called VDOM (Virtual DOM),
when a component is re-rendered, a reconciliation occurs, basically is a comparison between the the old and new object to
be determine which parts need to be changed. And, React uses React Fiber algorithm to update the VDOM.

Where is our component data stored?

React creates a fiber tree and each component of this tree is a fiber, all of its data
is stored in memory.

A fiber is nothing more than an object, containing type, prop, position, state. So, the component doesn't hold
any data, the fiber does.

Three rules for component be re-rendered:
- If the component holds state that changes, it will be eventually re-rendered;
- If a parent component re-renders, the child components will be re-rendered as well;
- If it uses a context value that has just changed, also re-renders;
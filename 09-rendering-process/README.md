

React operates with deterministic algorithm

Where is our component data stored?

React creates a fiber tree and each component of this tree is a fiber, all of its data
is stored in memory.

A fiber is nothing more than an object, containing type, prop, position, state. So, the component doesn't hold
any data, the fiber does.

Three rules for component be re-rendered:
- If the component holds state that changes, it will be eventually re-rendered;
- If a parent component re-renders, the child components will be re-rendered as well;
- If it uses a context value that has just changed, also re-renders;
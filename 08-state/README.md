# State in React
It is a state variable added to a component

## Important details
 - useState is asynchronous so React batches state updates when it finds necessary;
 - Everytime an state is updated, the component re-renders;

## Caveats
As useState being a hook, it can only called at the top level of a component or in a customized hook.
It can not be called in loops or conditions.

The useState hook should not be used for every case, in some cases useRef can be used in order to get values from DOM elements.

If a state needs to be updated based on previous value, always use the function version of useSate setter

### Code examples

#### Using useRef instead of useState

````Javascript
const Login = () => {
  const emailRef = React.useRef(null);
  const passwordRef = React.useRef(null);

  const onSubmit = (e) => {
    e.preventDefault();
    console.log({
      email: emailRef.current.value,
      password: passwordRef.current.value
    })
  }

  return (
    <form onSubmit={onSubmit}>
      <input
        type="email"
        ref={emailRef}
      />
      <input
        type="password"
        ref={passwordRef}
      />
      <button type="submit">Login</button>
    </form>
  )
}
    
````
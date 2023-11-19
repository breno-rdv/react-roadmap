# Reconciliation

React creates a tree of elements, which are just plai Javascript objects, this tree
of elements is called Virtual DOM

Then, sync the Virtual DOM with the real DOM.

When there is a state change, for example, React creates a new tree of elements, and then compares
the two trees using a diffing algorithm to make changes to the DOM

The diffing algorithm:
Looks at component type and $key prop of a element

- Create a two elements and update their type

- Creating a two elements and update their attributes

> When updating a attribute of an element, React doesn't re-render the component

````Javascript
const Title = (props) => {
    return (
        <h1 className={props.highlighted ? 'highlighted' : ''}>React is awesome</h1>
    );
}

const App = () => {
    const [highlighted, setHighlighted] = React.useState(false);

    return <>
        <Title highlighted={highlighted} />
        <button onClick={() => setHighlighted(prev => !prev)}>Highlight Title</button>
    </>
}
````

- Creating a list of items and include one at the bottom, with no index
````Javascript
const List = (props) => {
    return (
        <ul>
            {props.list?.map(item => {
                return <li>{item.name}</li>
            })}
        </ul>
    );
}

const App = () => {
    const [people, setPeople] = React.useState([{ name: 'John' }, { name: 'Janesse' }]);
    const [person, setPerson] = React.useState('');

    return <>
        <List list={people} />
        <input value={person} onChange={(e) => setPerson(e.target.value)}/>
        <button onClick={() => setPeople(prev => {setPeople([...prev, { name: person }])})}>Add more</button>
    </>
}
````

- Create a list of items and include one at the top, with no index
- Create a list of elements and add one in any place, with index

Bear in mind that React doesn't take care of rendering, this is performed by another package, i.e React-DOM.

React-DOM calls only once its *x* method and React communicates with it via updater and dipatcher "functions".
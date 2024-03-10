# React Interview Questions

### Subjects

0.
1. [React basics #1](#lecture-1---react-basics-1)
2. [React basics #2](#lecture-2---react-basics-2)
3. [React Intermediate](#lecture-3---react-intermediate)
4. [React router](#lecture-4---react-router)
5. [Redux #1](#lecture-5---redux-1)
6. [Redux #2](#lecture-6---redux-2)
7. [React Advanced](#lecture-7---react-advanced)
8. [React Optimisation](#lecture-8---react-optimisation)
9. [External Libraries](#lecture-9---external-libraries)
10. [Typescript](#lecture-10---typescript)
11. [Testing, debugging, Agile](#lecture-11---testing-debugging-agile)

## Lecture #1 - React basics #1

[To top](#react-interview-questions)

1.  <details><summary>What is the React</summary>
    React is a JavaScript library that implement a component approach of WEB Applications development. It's uses a JSX extention that allows us to create a fully independed stateful or stateless components. Due to HTML-like code with JS code in the same file are 
    reaching the really standalone components.

    There is existing an additional libraries such as react-router that can be used to reach the Single-Page Application approach.
    </details>

2.  <details><summary>What is the JSX</summary>
    It's a JavaScript extension with full name as JavaScript XML. This extension uses to achieve HTML-like syntax in JavaScript code.

    However, HTML-like syntax have a little difference from the thruly HTML. The difference is in some attributes name such as className or htmlFor
    </details>


3.  <details><summary>What is the SPA</summary>
    Abbreviature SPA means a Single-Page Application that used for describing applications that can be used without any reloades between page changes.

    This behavior can be reached by using react-router library for example.
    </details>
    
4.  <details><summary>DOM</summary>
    Abbreviature that described as a Document Object Model. It's a tree-node data structure that used by browsers to serve the HTML document and interact with it.
    </details>
    
5.  <details><summary>Virtual DOM</summary>
    <b>The Virtual DOM</b> is the lightweight copy of the <u>original DOM</u> represented as a JavaScript object. React can reach the really fast changing speed due this representation instead of working with tree-like structure.
    </details>
        
6.  <details><summary>What's the difference between class and functional components?</summary>
    The class components comes from the OOP. This approach means that we're should use the required render() method to render some JSX. Also theese components have an access to lifecycle methods such as componentDidMount, componentDidUpdate, componentWillUnmount and some count of another methods to provide the component flexibility.

    Meanwhile, functional components are a simple functions that simply should return a JSX markup. There is hooks exists to reach the next level of component flexibility. 

    Each of them can contain any logic into them but the difference between them in the workflow with them.
    </details>
        
7.  <details><summary>What is the key?</summary>
    The key is a special prop in React that implicitly exist in any JSX entity. This prop helps React to identefy the changes into components. We must to use the key explicitly when we should to render some array of data as a list of components or JSX elements.
    </details> 

8.  <details><summary>What are hooks?</summary>
    Hooks are special conceptions in functional components provide us comfortable controls of data and components workflows. They allows the more expressive and understandable approach instead of class lifecycle methods and they can be use more flexible.
    
    Some of them can have a dependecies array that provide a light-understandable control of data or component dependencies.
    </details>

9. <details><summary>Component renders.</summary>
    When the component appears on the screen in first time or after unmounting it means that <b>initial render</b> was caused

    If some of reactive values of existed component were changed or the parent component was re-rendered it will calls <b>re-render</b> of component
    </details>


## Lecture #2 - React basics #2

[To top](#react-interview-questions)

1.  <details><summary>What is the State and how to use it?</summary>
    That is current state of a component or an application. Some data which our components working with. As I mentioned before, state can be for components, for the application or it parts as well.

    To reach the state manipulations and usage we can use lifecycle methods or hooks, such as useState, useReducer, useEffect and anothers or additional libraries such as Redux to achieve comfortable workflow with global state of application.
    </details>

2.  <details><summary>What are reactive and non-reactive values</summary>
    Reactive values are exact what React dealing with. Changes of reactive values will trigger the re-rendering of components. Due for it we can show an up-to-date data to user in each moment of working with application. The Reactive value can be created by the state management features such as useState hook.

    Opposite of reactive values are non-reactive values. The React re-render feature will not reflect on changes of these values and will not re-render components if some of these were changed. To create any non-reactive value we can use hook useRef or deal with common JS variables, constants or class fields.
    </details>

3.  <details><summary>useState and useReducer</summary>
    Hooks useState and useReducer uses to create and manipulate with state of components. 

    While useState uses to reach the control with some simple data such as JS primitives, arrays or a small objects the useReducer uses to work with more complicated data such as objects with many fields with nested object as an example.

    useState returns a value and a function to change this value. To reach the value changing we can provide new value or a function callback in returned function setter. Callback have an access to previous previous value and should return the new one.

    useReducer returns a value and a function reducer that we should provide in hook while created it. The reducer function should be a clear function that awaits for some action and always returns state with changes based on received action type.
    </details>

4.  <details><summary>Context and useContext?</summary>
    Context is a global application state or a part of it. It's providing us some values or a complex data structures in the different parts or components of application and it get us access to use and change theys.

    To use the context we should create it with the createContext function that awaits for value with initial state of context or null. Then to use this context we should to wrap the part of application by this context Provider and it will provide an access to the context.

    We can get this data using the useContext hook (that awaits for the value created with createContext function) in a parts of application that were wrapped by this context provider.
    </details>

5.  <details><summary>useRef</summary>
    One of the ways to create non-reactive value is a useRef hook. It's always an object with field current as result. This field is mutable and can contain any data such as some JS data types or HTML nodes.    
    </details>

6.  <details><summary>forwardRef and useImperativeHandle</summary>
    forwardRef is a function wrapper for component that awaits for ref. The component should me implemented as a function declaration or an arrow nameless function that firstly receive a props and secondary a ref as an arguments.

    If we wanna send ref to a child component from parrent using a common way and prop ref we'll should to wrap the child using forwardRef and then we'll have an access to this ref from parent.

    Using the useImperativeHandle that related uses with forwardRef we can reach more flexible manipulations with child component from the parent. This hook awaits for ref and callback that returns an object with fields that we'll can use in parent component later.
    </details>

## Lecture #3 - React Intermediate

[To top](#react-interview-questions)

1. <details><summary>Lifecycle of react components</summary>
    There are three stages. Mounting, updating and unmounting.

    Class and Functional components have itself flows to work with lifecycles. Each of them can manipulate it state based on current stage.
    </details>

1.  <details><summary>Class lifecycle methods</summary>
    They provide us with the opportunity to work with the state of a class component at different stages of its lifecycle. Due to them, we can manipulate data during component mounting, updating, or unmounting.

    The more commonly used lifecycle methods include componentDidMount, componentDidUpdate, and componentWillUnmount.

    There are also other methods such as shouldComponentUpdate, componentDidCatch, getSnapshotBeforeUpdate, or getDerivedStateFromProps.
    </details>
    
2.  <details><summary>useEffect</summary>
    This hook provide us a possibility to do some side-effects into functional components. Its sugnature is useEffect(callback, dependecnies). The callback of it will called in each initial render and each next re-render if we'll not provide a dependencies array.

    This hook have more flexible behavior than class lifecycle methods due dependencies array. Due to instant callback calling after component did mounted we achieved componentDidMount functionallity, if we'll not provide the dependencies array we'll reach the componentDidUpdate fucntionallity and due to return callback from the called callback we're reaching componentWillUnmount functionallity but not in useEffect context - not component.

    And there are more usefull cases based on an array of dependencies that will trigger callback each time when some of provided dependencies was changed. Or will trigger only ones if the dependencies array is empty.
    </details>
    
3.  <details><summary>useLayoutEffect</summary>
    This is a hook that fires before a browser repaints the screen. It's should be noted that the useLayoutEffect works synchroniously instead of synchronous work as works useEffect

    It's also awaits for callback that also can return a clean-up function and dependencies array and will call provided function based on component lifecycle and dependencies.
    </details>
    
4.  <details><summary>Dependencies</summary>
    Some of hooks awaits for array as a dependencies.

    Dependencies array it's an entity that will checked by any hook that awaits for it while something changes in state. If something from state was changed and it was as dependency in the array - it will trigger callback.
    </details>
    
6.  <details><summary>Custom hooks</summary>
    Based on provided built-in hooks we can create a custom hooks. Usually they're combinations of pair or more hooks. It's usefull when we want to create a short-hand of some repeatable logic based on hooks.
    </details>
    
7.  <details><summary>React render phases</summary>
    Before something will be rendered in browser, three render phases should be gone.

    Triggering, reconciling, commiting to DOM

    The triggering phase depends on two events. Initial render and state updating.

    Initial render calls when the component should be rendered first time on screen. And every next update or "re-creating" calls re-render.

    After the render triggering, React compares the current Virtual DOM with the previous one to determine what needs to be rendered. It may call initial render or re-render depends on component existing in Virtual DOM and it will calls react.root component if it was not existed or the function component that state was changed.

    And the next stage is a commiting that caused on initial rendering or if something was changed. React will make changes in DOM if there is a difference between redners. 
    During initial rendering React will calls appendChild() DOM API function to put DOM Nodes that should be rendered on screen.
    Meanwhile the re-rendering process will make only minimal neccessary operations to make the DOM up-to-date state.  
    </details>

## Lecture #4 - React router

[To top](#react-interview-questions)

1.  <details><summary>Router and SPA</summary>

    </details>

2.  <details><summary>Routes and Route</summary>

    </details>

3.  <details><summary>Nested routes</summary>

    </details>

4.  <details><summary>Route to 404 page</summary>

    </details>

5.  <details><summary>Protected routes</summary>

    </details>

6.  <details><summary>Outlet</summary>

    </details>

7.  <details><summary>useParams</summary>

    </details>

8.  <details><summary>History breaker - replace</summary>

    </details>

## Lecture #5 - Redux #1

[To top](#react-interview-questions)

1.  <details><summary>Redux</summary>

    </details>

1.  <details><summary>HOC connect()</summary>

    </details>

1.  <details><summary>Middlewares</summary>

    </details>

1.  <details><summary>Memoised selector</summary>

    </details>

1.  <details><summary>Normalized state</summary>

    </details>

1.  <details><summary>useSelector and useDispatch</summary>

    </details>

1.  <details><summary>Rules of Redux</summary>

    </details>

1.  <details><summary>Redux lifecycle</summary>

    </details>

## Lecture #6 - Redux #2

[To top](#react-interview-questions)

1.  <details><summary>RTK Query</summary>

    </details>

1.  <details><summary>createAsyncThunk</summary>

    </details>

1.  <details><summary>createApi</summary>

    </details>

1.  <details><summary></summary>

    </details>


## Lecture #7 - React Advanced

[To top](#react-interview-questions)

1.  <details><summary>React patterns</summary>

    </details>

1.  <details><summary>Key</summary>

    </details>

1.  <details><summary>Suspense</summary>

    </details>

1.  <details><summary>Fiber</summary>

    </details>

1.  <details><summary>Parallel processes in React</summary>

    </details>

## Lecture #8 - React Optimisation

[To top](#react-interview-questions)

1.  <details><summary>Motivation - general questions</summary>
    
    - Can we move the calculations from front to back?
  
    - Can we refactor code to simplify calculations?
  
    - Are we really should memoize it?
    </details>

2.  <details><summary>useMemo & useCallback</summary>

    </details>

3.  <details><summary>memo(component, arePropsEqual?)</summary>

    </details>

4.  <details><summary>PureComponent</summary>

    </details>

5.  <details><summary>lazy()</summary>

    </details>

6.  <details><summary>Virtualisation</summary>

    </details>

6.  <details><summary>Bundle optimisation</summary>

    </details>

6.  <details><summary>Web workers</summary>

    </details>
    
6.  <details><summary>Image optimisation</summary>

    </details>
    
6.  <details><summary>Reselect</summary>

    </details>


## Lecture #9 - External Libraries

[To top](#react-interview-questions)


1.  <details><summary></summary>

    </details>

1.  <details><summary></summary>

    </details>

## Lecture #10 - Typescript

[To top](#react-interview-questions)

1.  <details><summary></summary>

    </details>

1.  <details><summary></summary>

    </details>


## Lecture #11 - Testing, debugging, Agile

[To top](#react-interview-questions)

1.  <details><summary></summary>

    </details>

1.  <details><summary></summary>

    </details>


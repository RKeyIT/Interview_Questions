# React Interview Questions

### Subjects

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
12. [Random questions](#random-questions)

## Lecture #1 - React basics #1

[To top](#react-interview-questions)

1.  <details><summary>What is the React</summary>

    React is a JavaScript library that implement a component approach of WEB Applications development. It's uses a JSX extention that allows us to create a fully independed stateful or stateless components. Due to HTML-like code with JS code in the same file are
    reaching the really standalone components.

    There is existing an additional libraries such as react-router that can be used to reach the Single-Page Application approach.

    ***

    </details>

2.  <details><summary>What is the JSX</summary>

    It's a JavaScript extension with full name as JavaScript XML. This extension uses to achieve HTML-like syntax in JavaScript code.

    However, HTML-like syntax have a little difference from the thruly HTML. The difference is in some attributes name such as className or htmlFor

    ***

    </details>

3.  <details><summary>What is the SPA</summary>

    Abbreviature SPA means a Single-Page Application that used for describing applications that can be used without any reloades between page changes.

    This behavior can be reached by using react-router library for example.

    ***

    </details>

4.  <details><summary>DOM</summary>

    Abbreviature that described as a Document Object Model. It's a tree-node data structure that used by browsers to serve the HTML document and interact with it.

    ***

    </details>

5.  <details><summary>Virtual DOM</summary>

    <b>The Virtual DOM</b> is the lightweight copy of the <u>original DOM</u> represented as a JavaScript object. React can reach the really fast changing speed due this representation instead of working with tree-like structure.

    ***

    </details>

6.  <details><summary>React-DOM</summary>

    react-dom library is ...

    ***

    </details>

7.  <details><summary>What's the difference between class and functional components?</summary>

    The class components comes from the OOP. This approach means that we're should use the required render() method to render some JSX. Also theese components have an access to lifecycle methods such as componentDidMount, componentDidUpdate, componentWillUnmount and some count of another methods to provide the component flexibility.

    Meanwhile, functional components are a simple functions that simply should return a JSX markup. There is hooks exists to reach the next level of component flexibility.

    Each of them can contain any logic into them but the difference between them in the workflow with them.

    ***

    </details>

8.  <details><summary>What is the key?</summary>

    The key is a special prop in React that implicitly exist in any JSX entity. This prop helps React to identefy the changes into components. We must to use the key explicitly when we should to render some array of data as a list of components or JSX elements.

    ***

    </details>

9.  <details><summary>What are hooks?</summary>

    Hooks are special conceptions in functional components provide us comfortable controls of data and components workflows. They allows the more expressive and understandable approach instead of class lifecycle methods and they can be use more flexible.

    Some of them can have a dependecies array that provide a light-understandable control of data or component dependencies.

    ***

    </details>

10. <details><summary>Component renders.</summary>

    When the component appears on the screen in first time or after unmounting it means that <b>initial render</b> was caused

    If some of reactive values of existed component were changed or the parent component was re-rendered it will calls <b>re-render</b> of component

    ***

    </details>

## Lecture #2 - React basics #2

[To top](#react-interview-questions)

1.  <details><summary>What is the State and how to use it?</summary>
    That is current state of a component or an application. Some data which our components working with. As I mentioned before, state can be for components, for the application or it parts as well.

    To reach the state manipulations and usage we can use lifecycle methods or hooks, such as useState, useReducer, useEffect and anothers or additional libraries such as Redux to achieve comfortable workflow with global state of application.

    ***

    </details>

2.  <details><summary>What are reactive and non-reactive values</summary>
    Reactive values are exact what React dealing with. Changes of reactive values will trigger the re-rendering of components. Due for it we can show an up-to-date data to user in each moment of working with application. The Reactive value can be created by the state management features such as useState hook.

    Opposite of reactive values are non-reactive values. The React re-render feature will not reflect on changes of these values and will not re-render components if some of these were changed. To create any non-reactive value we can use hook useRef or deal with common JS variables, constants or class fields.

    ***

    </details>

3.  <details><summary>useState and useReducer</summary>
    Hooks useState and useReducer uses to create and manipulate with state of components.

    While useState uses to reach the control with some simple data such as JS primitives, arrays or a small objects the useReducer uses to work with more complicated data such as objects with many fields with nested object as an example.

    useState returns a value and a function to change this value. To reach the value changing we can provide new value or a function callback in returned function setter. Callback have an access to previous previous value and should return the new one.

    useReducer returns a value and a function reducer that we should provide in hook while created it. The reducer function should be a clear function that awaits for some action and always returns state with changes based on received action type.

    ***

    </details>

4.  <details><summary>Context and useContext?</summary>
    Context is a global application state or a part of it. It's providing us some values or a complex data structures in the different parts or components of application and it get us access to use and change theys.

    To use the context we should create it with the createContext function that awaits for value with initial state of context or null. Then to use this context we should to wrap the part of application by this context Provider and it will provide an access to the context.

    We can get this data using the useContext hook (that awaits for the value created with createContext function) in a parts of application that were wrapped by this context provider.

    ***

    </details>

5.  <details><summary>useRef</summary>
    One of the ways to create non-reactive value is a useRef hook. It's always an object with field current as result. This field is mutable and can contain any data such as some JS data types or HTML nodes.

    ***

    </details>

6.  <details><summary>forwardRef and useImperativeHandle</summary>
    forwardRef is a function wrapper for component that awaits for ref. The component should me implemented as a function declaration or an arrow nameless function that firstly receive a props and secondary a ref as an arguments.

    If we wanna send ref to a child component from parrent using a common way and prop ref we'll should to wrap the child using forwardRef and then we'll have an access to this ref from parent.

    Using the useImperativeHandle that related uses with forwardRef we can reach more flexible manipulations with child component from the parent. This hook awaits for ref and callback that returns an object with fields that we'll can use in parent component later.

    ***

    </details>

## Lecture #3 - React Intermediate

[To top](#react-interview-questions)

1. <details><summary>Lifecycle of react components</summary>
   There are three stages. Mounting, updating and unmounting.

   Class and Functional components have itself flows to work with lifecycles. Each of them can manipulate it state based on current stage.

   ***

   </details>

2. <details><summary>Class lifecycle methods</summary>
   They provide us with the opportunity to work with the state of a class component at different stages of its lifecycle. Due to them, we can manipulate data during component mounting, updating, or unmounting.

   The more commonly used lifecycle methods include componentDidMount, componentDidUpdate, and componentWillUnmount.

   There are also other methods such as shouldComponentUpdate, componentDidCatch, getSnapshotBeforeUpdate, or getDerivedStateFromProps.

   ***

   </details>

3. <details><summary>useEffect</summary>
   This hook provide us a possibility to do some side-effects into functional components. Its sugnature is useEffect(callback, dependecnies). The callback of it will called in each initial render and each next re-render if we'll not provide a dependencies array.

   This hook have more flexible behavior than class lifecycle methods due dependencies array. Due to instant callback calling after component did mounted we achieved componentDidMount functionallity, if we'll not provide the dependencies array we'll reach the componentDidUpdate fucntionallity and due to return callback from the called callback we're reaching componentWillUnmount functionallity but not in useEffect context - not component.

   And there are more usefull cases based on an array of dependencies that will trigger callback each time when some of provided dependencies was changed. Or will trigger only ones if the dependencies array is empty.

   ***

   </details>

4. <details><summary>useLayoutEffect</summary>
   This is a hook that fires before a browser repaints the screen. It's should be noted that the useLayoutEffect works synchroniously instead of synchronous work as works useEffect

   It's also awaits for callback that also can return a clean-up function and dependencies array and will call provided function based on component lifecycle and dependencies.

   ***

   </details>

5. <details><summary>Dependencies</summary>
   Some of hooks awaits for array as a dependencies.

   Dependencies array it's an entity that will checked by any hook that awaits for it while something changes in state. If something from state was changed and it was as dependency in the array - it will trigger callback.

   ***

   </details>

6. <details><summary>Custom hooks</summary>
   Based on provided built-in hooks we can create a custom hooks. Usually they're combinations of pair or more hooks. It's usefull when we want to create a short-hand of some repeatable logic based on hooks.

   ***

   </details>

7. <details><summary>React render phases</summary>
   Before something will be rendered in browser, three render phases should be gone.

   Triggering, reconciling, commiting to DOM

   The triggering phase depends on two events. Initial render and state updating.

   Initial render calls when the component should be rendered first time on screen. And every next update or "re-creating" calls re-render.

   After the render triggering, React compares the current Virtual DOM with the previous one to determine what needs to be rendered. It may call initial render or re-render depends on component existing in Virtual DOM and it will calls react.root component if it was not existed or the function component that state was changed.

   And the next stage is a commiting that caused on initial rendering or if something was changed. React will make changes in DOM if there is a difference between redners.
   During initial rendering React will calls appendChild() DOM API function to put DOM Nodes that should be rendered on screen.
   Meanwhile the re-rendering process will make only minimal neccessary operations to make the DOM up-to-date state.

   ***

   </details>

## Lecture #4 - React router

[To top](#react-interview-questions)

1.  <details><summary>Router and SPA</summary>
    To implement an application as a SPA we can use a router feature such as react-router. SPA allows us making redirects in our application without page reloading. Due to this conception we can create the 
    Single Page Application.

    To create the router with react-router we should chose one of available from:

    BrowserRouter, HashRouter, MemoryRouter, StaticRouter

    More often usable router is a BrowserRouter that can be created by using "createBrowserRouter(router)" that awaits for array with path objects that looks like:

        const router = {
            path: '/'
            component: <Root />
            loader: rootLoader,
            children: [
                {
                    path: '/user',
                    component: <User />,
                    loader: userLoader,
                    children: [...]
                }
            ]
        }

    And then we should use provider of this router

        <App>
            <Header />
                <RouterProvider router={router} />
            <Footer />
        </App>

    ***

    </details>

2.  <details><summary>Routes and Route</summary>
    Routes and Route are React components that implements routing functionallity within our application. We should provide a string as a route path into same-name "attribute" or prop of Route component.

    Routes is a wrapper under our Route components.

    We can nest the Route component in another one to reach the thin setup of routing. It's an alternate way to create flexible routing (instead of modern router object created with createBrowserRouter for example).

    ***

    </details>

3.  <details><summary>Nested routes</summary>
    To reach the flexible workflow with routes we can use nested routes that can be as a parameteres or separated folders

    ***

    </details>

4.  <details><summary>Route to 404 page</summary>
    To redirect on page 404 if user looks for some not existed page we can use route with '/*' characters. Router will use this way if no one another ways were not match.

    We can create some component that will show to user that he's on wrong way.

    Also we can handle it by using errorElement field:

        const router = {
            path: '/'
            component: <Root />
            loader: rootLoader,

            errorElement: <Page404 />,

            children: [
                {
                    path: '/user',
                    component: <User />,
                    loader: userLoader,
                    children: [...]
                }
            ]
        }

    ***

    </details>

5.  <details><summary>Protected routes</summary>
    That is conception that can helps us to protect or preporcess some routes depends on any logic. To reach this purpose we can create a wrapper component that will contain some logic and render some content depends on this logic.

    It's can be user access rights, login, time and any another logic.

    Protected route can be looked like:

        const RouterProtector = ({ children }) => {
            ... some logic ...

            return children
        }

        const User = () => {
            return <section>...some markup...</section>
        }

        const browserRouter = createBrowserRouter([
            {
                path: '/',
                component: '<Home />',
                children: [
                    {
                        path: '/user'
                        component: <RouterProtector><User /></RouterProtector>
                    }
                ]
            }
        ])

    ***

    </details>

6.  <details><summary>Outlet</summary>
    That is component that will place router depended components.

    An <Outlet> should be used in parent route elements to render their child route elements. This allows nested UI to show up when child routes are rendered. If the parent route matched exactly, it will render a child index route or nothing if there is no index route.

    ***

    </details>

7.  <details><summary>useParams</summary>
    That is hook that returns an object { key: value } that contains each of parameters in current URL.

    ***

    </details>

8.  <details><summary>History breaker - replace</summary>
    To reach the rerouting without possibility to returning back in any link or function as navigate() we can put additional object with field replace { replace: true }

        <Link to="/home" replace>Home</Link>

        navigate('/new-url', { replace: true });

        history.replace('/home', { replace: true });

    ***

    </details>

## Lecture #5 - Redux #1

[To top](#react-interview-questions)

1.  <details><summary>Redux</summary>

    Redux is one of the state management libraries that provide a comfortable workflow with the global state of application based on the Context API.

    The global state can be used as an application state or as a seperate part of it. We can wrap any part of app by the chosen "context" provider and use this state in any child of this component.

    In React applications we can use react-redux library that provides us more effective way to interact with global state by using react patterns such as hooks.

    ***

    </details>

2.  <details><summary>Rules of Redux</summary>

    There is main redux rules:

    - Single Source of Truth - means that should be existed only one global state and only it must be as a Source of Truth. The current application state must be received only from it.
    - State is immutable - means that the state is read-only. We can make some changes directly in state. Each changes should be make by reducers
    - Reducers is a pure functions that always return a new state based on previous state and received action.
    - One Way Data Flow - means that the data have only one way from components - through dispatch to store

    ***

    </details>

3.  <details><summary>HOC connect()</summary>

    This is react-redux High Ordered Function that returns received component that will connected with redux state. We should provide 2 functions that will handle our work with state.

    They're mapStateToProps and mapDispatchToProps.

    mapStateToProps will handle what exact part of state we'll receive, meanwhile mapDispatchToProps will handle state changes

    ***

    </details>

4.  <details><summary>Middlewares</summary>

    Middleware - is a general development concept of functions that work with data that we passed in them and can make some changes in the data.

    ***

    </details>

5.  <details><summary>Normalized state</summary>

    WORK IN PROGRESS

    ***

    </details>

6.  <details><summary>Reducers and Actions</summary>

    Reducer is a pure function that always receive a state and an action and then returns state. It's waiting for action with type field and based on this type should implement some logic of state handling. Usually it uses switch case operator to figuring out what the changes should be applied and anyway returns state.

    Action is an object that must contain a "type" property. It's can contain any fields to but usually one more field exists called as "payload". The type field may be a string with name of current action, meanwhile payload is an optional field that contains some data that should be stored.

        const reducer = (state, action) => {
            switch(action.type) {
                case "ADD_USER":
                    state.users = {
                        ...state.users,
                        action.payload
                    }
                default:
                    return state
            }
        }

        const ADD_USER_ACTION = { type: "ADD_USER", payload: userObject }

    ***

    </details>

7.  <details><summary>useSelector and useDispatch</summary>

    They're hooks to interact with redux state.

    The useSelector is selector for our state. We can get some piece of state with it.

        const userState = useSelector(state => state.users)

    useDispatch is a hook that returns a function to handle state changes. It sends an action to store and in store will be applied changes based on this action.

        const dispatch = useDispatch()

        dispatch({ type: 'ADD_USER', payload: newUser })

        or

        const ADD_USER_ACTION = { type: "ADD_USER", payload: userObject }
        dispatch(ADD_USER_ACTION)

    ***

    </details>

8.  <details><summary>Redux lifecycle</summary>

    Everything begins from UI. When we want to change something in state we'll handle some event by handler that should calls dispatch function and put in it some action based on current event.

    - The action starts it way to store through dispatcher and may be modified by middlewares.
    - Then the data goes through reducers and when some of them figure out received action type, they're returning a new state.
    - Next step is updated data going to UI

    ***

    </details>

9.  <details><summary>Memoised selector</summary>

    This selector will helps in cases when we want to save some part of data (as a list of some IDs) and do not re-render or re-calculate something.

    While a common selector will be called each time when component was rerendered, a memoised one will not. It will cash the date and return cashed value each time if an arguments were not changed.

    ***

    </details>

## Lecture #6 - Redux #2

[To top](#react-interview-questions)

1.  <details><summary>RTK Query</summary>
    Redux Toolkit Query is an extension over redux that provide for us another level of abstraction to free us from writting much boiler plate code.

    It's provide more comfortable new features such as configureStore, createSlice, createApi, redux devtools and much anothers to make our development experience much faster and effectively.

    ***

    </details>

2.  <details><summary>configureStore</summary>
    It's a comfortable way to setup store. configureStore is waiting for reducers that we can provide from slices or from fucntion combineReducers that may fit them all in one variable. It's may accept midlewares as well.

    ***

    </details>

3.  <details><summary>createSlice</summary>
    createSlice - is a function that awaits for settings object that should include name of slice, initial state, reducers, extraReducers and returns one same-named part of global state. That's why it's calls as slice.

    ***

    </details>

4.  <details><summary>extraReducers</summary>
    That is additional reducers that provides for us a feature to react when some of actions was comes from dispatch. We always have an access to current store and received action and can implement some logic based on them.

    ***

    </details>

5.  <details><summary>createAsyncThunk</summary>
    It is an action that works with asynchronous things such us data fetching. It's waiting for name of action that usually used as string, and asynchronous function that returns some date. It's works as an action and we can react on it with our extraReducers.

    ***

    </details>

6.  <details><summary>createApi</summary>
    It's a modern decision to implement more comfortable interaction with API. createApi is waiting for an object with settings such as reducerPath, baseQuery and endpoints.

    endpoints is a function that receive a builder object and should return an object with different methods based on current needs. It can be qurey to get something from server or mutation to send something to server.

    ***

    </details>

## Lecture #7 - React Advanced

[To top](#react-interview-questions)

1.  <details><summary>React patterns</summary>

    - Props destructuring
    - Conditional rendering
    - Array rendering
    - Children rendering
    - High Order Component

    ***

    </details>

2.  <details><summary>Key</summary>

    A key is a special prop that implicitly exist in any JSX entity in react. Due this prop react is figuring out what and where was changed.

    We should use the key explicitly when we're rendering an array of something as a list of JSX elements. The JSX element that we're returning from the map function should have explicitly setled key that must be a unique value.

    That means if we'll render a dynamic array, indexes of that array will not be optimal decision to set them as keys. Better variant - it's using IDs of iterable entities if theys exist, or pre-set IDs with using some library before mapping this data.

    ***

    </details>

3.  <details><summary>Suspense</summary>

    It's a special component that can provide some component instead of currently downloadable.

    Currently it's working with lazy components that we can create by lazy() function that will dinamycaly import specified component.

    ***

    </details>

4.  <details><summary>React Reconciliation</summary>

    It's a process of comparing the current tree with the work-in-progress tree, followed by an optimized way to commit the changes from the work-in-progress tree to the current tree. These changes are applied to the virtual DOM, resulting in the updated virtual DOM becoming the new current tree.

    ***

    </details>

5.  <details><summary>Fiber</summary>

    Fiber is a new conception since React 16 that provide a more effective way of reconciliation than earlier stack-based.

    It's includes:

    - Prioritisation
    - Pausing
    - Resuming
    - Aborting
    - Concurrency

    > [!WARNING]
    > The problematic of previous stack-based approach is a list of neccessary performance issues:
    >
    > - Lack of interruption
    > - Synchronous process
    > - Inefficient updates
    > - Limited prioritization

    > [!TIP]
    > We can think of a single fiber as a virtual stack frame. In simple terms, a fiber represents a unit of work with its own virtual stack.

    In the previous implementation of the reconciliation algorithm, React created a tree of objects (React elements) that are immutable and traversed the tree recursively.

    In the current implementation, React creates a tree of fiber nodes that can mutate. The fiber node effectively holds the component’s state, props, and underlying DOM element it renders to.

    ***

    </details>

6.  <details><summary>Parallel processes in React</summary>

    Due to new conception as Fiber the React have an option to make state changes asynchronously and in more effective way.

    This also will prevent unneccessary re-renders due to "batching" coception that will collect same tasks and will accept them in only one time

    ***

    </details>

## Lecture #8 - React Optimisation

[To top](#react-interview-questions)

1.  <details><summary>Motivation - general questions</summary>

    - Can we move the calculations from front to back?

    - Can we refactor code to simplify calculations?

    - Are we really should memoize it?

    ***

    </details>

2.  <details><summary>useMemo & useCallback</summary>

    They're 2 same hooks but useCallback is another layer of abstraction that was designed for functions to free us from using additional callback as a parameter of hook.

    They're hooks that memoize values or results of some statements and prevent recalculations during rerendering processes that may provide more performance to our applications.

    useMemo and useCallback also have a dependency array and while values in it will not change the memoized entities will not be recalculated. Even if the parent component will be rerendered, memoized entities will be with previous values if dependencies will not changed.

    ***

    </details>

3.  <details><summary>memo(component, arePropsEqual?)</summary>

    It's a HOC to functional component that will prevent uneccessary rerenders and will rerender component only if props was changed.

    It's another memoisation feature of react designed for components and the signature is a memo(component, compareFunction) when the compareFunction is a function to compare props between currents and previouses

    ***

    </details>

4.  <details><summary>PureComponent</summary>

    It's a class component extended from React.PureComponent instead of React.Component that shallowly compares props and state between currents and previouses and will rerender component only in case if the difference exists.

    PureComponent prevent unneccessary rerenders while setState was called but the state was not changed

    ***

    </details>

5.  <details><summary>Pure Function</summary>

    That is function without side-effects (as a changing values out of function scope) and with same parameters always returns same expected and predictable values.

    ***

    </details>

6.  <details><summary>lazy()</summary>

    It's React built-in function that provides dynamical loading of components. Using lazy() we can separate our application on chunks that will loaded only when it will be required.

    ***

    </details>

7.  <details><summary>Virtualisation</summary>

    It's a concept with same behavior to lazy() function that allows us to load dynamicaly list elements.

    To prevent displaying not loaded items we can create a buffer zone that will not be in user viewport, but will content some amount of loaded additionaly items.

    ***

    </details>

8.  <details><summary>Image optimisation</summary>

    s

    ***

    </details>

9.  <details><summary>Reselect</summary>

    s

    ***

    </details>

10. <details><summary>Web workers</summary>

    s

    ***

    </details>

11. <details><summary>Bundle optimisation</summary>

    s

    ***

    </details>

## Lecture #9 - External Libraries

[To top](#react-interview-questions)

1.  <details><summary></summary>

    s

    ***

    </details>

2.  <details><summary></summary>

    s

    ***

    </details>

## Lecture #10 - Typescript

[To top](#react-interview-questions)

1.  <details><summary></summary>

    s

    ***

    </details>

2.  <details><summary></summary>

    s

    ***

    </details>

## Lecture #11 - Testing, debugging, Agile

[To top](#react-interview-questions)

1.  <details><summary></summary>

    s

    ***

    </details>

2.  <details><summary></summary>

    s

    ***

    </details>

## Random questions

[To top](#react-interview-questions)

1.  <details><summary>Data types in JS</summary>

    - Boolean
    - String
    - Number
    - BigInt
    - undefined
    - null
    - Object
    - Symbol

    ***

    </details>

2.  <details><summary>Differences between primitives and object</summary>

    Primitives - they are simply values that can be assigned, changed, and replaced. They are not related to any other data with the same value and cannot be related.

    Meanwhile, an Object - is a reference type, and assigning it means assigning a reference to this type. Any manipulations with values in it will be reflected in any other reference to this object.

    Any different variables that contain the same primitive are comparable, while objects are not. Two different objects with the same fields and values will not be equal.

    ***

    </details>

3.  <details><summary>Array methods(5-6 examples)</summary>

    - forEach - It's apply callback to each value of an array and returns undefined
    - map - returns another array based on results of mapping one with received callback
    - filter - It's a method that returns a new array that contains elements that was checked as trully by received callback
    - sort - Returns modified array without creating another one sorted by received callback
    - concat - returns another array based on array that calls this method with elements of received arrays.
    - every - returns true if each element was chacked by callback as true
    - some - returns true if some of elements was trully checked by callback
    - fill - returns modified array that was filled by received values
    - isArray - returns true if the type of received object is array
    - pop - returns an element that was removed from the end of array that calls this method
    - shift - returns an element that was removed from the start of array that calls this method
    - push - returns modified array with added in the end received element
    - unshift - returns modified array with received element in start

    ***

    </details>

4.  <details><summary>Difference between forEach and Map</summary>

    Foreach is not modify array and returns nothing (undefined). It's only apply the function on each iteration with elements as arguments for this.

    Meanwhile, Map returns new array based on provided callback that will be applied to each element and returns result of callback instead of previous element as a new element for new array.

    ***

    </details>

5.  <details><summary>Difference between var and let. What problem solves let?</summary>

    - function scope vs block scope
    - var hoisted while let is not

    The problem that solves let is a hoisting and function scope together. The var can make a problems based on hoisting and rewrite some outer variable by undefined. There is unconsidering block scope.

    ***

    </details>

6.  <details><summary>Difference between arrow function and function declaration</summary>

    - this context
    - new operator
    - arguments
    - implicit return

    The arrow functions are have no their own this and considering that can not be used as a function constructors. Ofcourse it means that we can not call them by using new operator.

    Arrow function have no its own arguments object while function declaration have.

    Implicit return statement in arrow function if was not be used curly braces

    ***

    </details>

7.  <details><summary>Closure</summary>

    It's a combination of function and lexical environment within which it was declared. This technique allows us to save an access to outer scope variables in function even if outer function was stop they work.

    ***

    </details>

8.  <details><summary>How to iterate object keys</summary>

    - for in loop
    - for off if the object have implements iterator

    Then we can use Object methods to create an array based on object entries and iterate this array.

    - Object.keys()
    - Object.getOwnPropertyNames()
    - Object.entries()

    ***

    </details>

9.  <details><summary>Event Loop explanation</summary>

    In JavaScript, the event loop is a concept provided by the JavaScript runtime environment, such as browsers or Node.js, to handle asynchronous operations.

    While synchronous code runs directly in the main thread of the runtime, asynchronous code is managed by the event loop. The event loop sorts and executes operations based on their nature.

    The event loop operates together with other concepts, including the Call Stack, Microtask Queue, and Macrotask Queue.

    - When code is executed, each statement is pushed onto the Call Stack. Synchronous code is executed immediately, while asynchronous tasks are added to their respective queues and await execution.

    - When the Call Stack is empty, Event Loop begins processing tasks in the Microtask Queue.

    - Then the Event Loop goes to on one of Macrotasks and complete it. After that all of previous processes will be repeated

    ***

    </details>

10. <details><summary>Asynchronous, microtasks and macrotasks</summary>

    Asynchronous code is the code that will be completed outer from the main thread and will not block it.

    This code used when the statement may not be completed immediately. It's can be as any interactions with an outer API such as file system or database, timers and others.

    Microtasks are promises, mainly, but there are function QueueMicrotask() and MutationObserver conception and they're provide the ability to create the microtasks.

    Meanwhile, macrotasks are everything others such as I/O operations, ajax requests, timers/intervals and event listeners

    ***

    </details>

11. <details><summary>Why do we need to use React and for what purposes it was invented</summary>

    React was designed to simplify creating and maintaining UIs for web applications based on component approach.

    ***

    </details>

12. <details><summary>Where we can use React</summary>

    It's a multiplatform library that can be used in WEB, Mobile and Desktop development due to additional libraries or frameworks.

    Library: react-dom
    Framewroks: React Native, Electron

    ***

    </details>

13. <details><summary>How does JSX transform in JS</summary>

    - Parsing
    - Transformation
    - Code Generation

    Parsing JSX by parser that converts the JSX to an Abstract Syntax Tree (AST).

    Then the AST transofrms into equivalent JavaScript code that in the end converts the JSX elements to JavaScript functions.

    Finally, the transformed AST is converted back into JavaScript code.

    It's just converting from JSX syntax to JavaScript.

    ***

    </details>

14. <details><summary>Could we provide a callback inside SetState function in class component?(tricky)</summary>

    Yes, but as the second argument that will calls after state changing. It's provide an ability to create some side effects based on state

    ***

    </details>

15. <details><summary>Can we change props?</summary>

    No, props are immutable and can be changed by related setState function.

    ***

    </details>

16. <details><summary>Have we replace lifecycle methods from class components into function components?</summary>

    Not directly, but we can simulate behavior by using useEffect hook. But it has it's own lifecycle instead of component lifecycle and it depends on dependencies array.

    ***

    </details>

17. <details><summary>How much hooks do you know?</summary>

    React:

    - useState
    - useReducer
    - useEffect
    - useLayoutEffect
    - useRef
    - useImperativeHandle
    - useContext
    - useMemo
    - useCallback
    - useTransition
    - useDefferedValue
    - useId

    Redux and RTK Query:

    - useSelector
    - useDispatch
    - useNavigate
    - generated by createApi()

    ***

    </details>

18. <details><summary>What purposes for useRef?</summary>

    s

    ***

    </details>

19. <details><summary>Can we provide any data type into useRef?</summary>

    s

    ***

    </details>

20. <details><summary>Batching</summary>

    s

    ***

    </details>

21. <details><summary>Synthetic Event vs Browser Event</summary>

    s

    ***

    </details>

22. <details><summary>Context API. Which kind of problem it solves?</summary>

    s

    ***

    </details>

23. <details><summary>Everything you know about OOP</summary>

    s

    ***

    </details>

24. <details><summary>Browser getting URL, what's next?</summary>

    s

    ***

    </details>

25. <details><summary>Cookies, local and session storages</summary>

    s

    ***

    </details>

26. <details><summary>Everything you know about Fiber</summary>

    s

    ***

    </details>

27. <details><summary>Portals and propagation</summary>

    s

    ***

    </details>

28. <details><summary>Everyghing you know about Redux</summary>

    s

    ***

    </details>

29. <details><summary>What is a pure function</summary>

    s

    ***

    </details>

30. <details><summary>Is a function pure if it's logging something? </summary>

    s

    ***

    </details>

31. <details><summary>Which lifecycle methods may be replaced by useEffect</summary>

    s

    ***

    </details>

32. <details><summary>JS Cotext loses</summary>

    s

    ***

    </details>

33. <details><summary>Prototype inheritance and chaining</summary>

    s

    ***

    </details>

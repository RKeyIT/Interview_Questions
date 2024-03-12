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


## Random questions
- Data types in JS
- Differences between prymitives and object
- Array methods(5-6 examples)
- Difference between forEach and Map
- Difference between var and let. What problem solves let?
- Difference between arrow function and function declaration
- Closure
- How iterate object keys
- Event Loop
- Asyncronious and asyncronious difference + microtasks/macrotasks(which events in micro/macro)
- Why do we need to use React and for what puposes it was invented
- Where we can use React(tricky) - reactNative, desktop applications(teams, slack)
- React-Dom library(what does react-dom do)
- What do you know about JSX
- How does JSX transform in JS
- What types of components we have
- Did you have an experience writing class components? :D
- Could we provide a callback inside SetState function in class component?(tricky)
- What is a props
- Can we change props?
- Have we replace lifecycle methods from class components into function components?
- React hooks
- What hooks do you know?
- useEffect
- useRef
- What purposes for useRef?
- Can we provide any data type into useRef?
- useState (batching)
- (sandbox) useEffect with empty dependencies array, useEffect with some depend in the array, how can we sumulate componentWillUnmount in func comp, useEffect without second argument
- (sandbox) how useEffect work, when dependency changed
- Difference between React Synthetic event and browser native event
- Context API. Which kind of problem it solves?
- What kind of storages we have in browser?
- Difference between local and session storages?
- Cookie - what the main difference between storages and cookies


## Lecture #1 - React basics #1

[To top](#react-interview-questions)

1.  <details><summary>What is the React</summary>
    React is a JavaScript library that implement a component approach of WEB Applications development. It's uses a JSX extention that allows us to create a fully independed stateful or stateless components. Due to HTML-like code with JS code in the same file are 
    reaching the really standalone components.

    There is existing an additional libraries such as react-router that can be used to reach the Single-Page Application approach.
    
    ---
    </details>

2.  <details><summary>What is the JSX</summary>
    It's a JavaScript extension with full name as JavaScript XML. This extension uses to achieve HTML-like syntax in JavaScript code.

    However, HTML-like syntax have a little difference from the thruly HTML. The difference is in some attributes name such as className or htmlFor
    
    ---
    </details>


3.  <details><summary>What is the SPA</summary>
    Abbreviature SPA means a Single-Page Application that used for describing applications that can be used without any reloades between page changes.

    This behavior can be reached by using react-router library for example.
    
    ---
    </details>
    
4.  <details><summary>DOM</summary>
    Abbreviature that described as a Document Object Model. It's a tree-node data structure that used by browsers to serve the HTML document and interact with it.
    
    ---
    </details>
    
5.  <details><summary>Virtual DOM</summary>
    <b>The Virtual DOM</b> is the lightweight copy of the <u>original DOM</u> represented as a JavaScript object. React can reach the really fast changing speed due this representation instead of working with tree-like structure.
    
    ---
    </details>
        
6.  <details><summary>What's the difference between class and functional components?</summary>
    The class components comes from the OOP. This approach means that we're should use the required render() method to render some JSX. Also theese components have an access to lifecycle methods such as componentDidMount, componentDidUpdate, componentWillUnmount and some count of another methods to provide the component flexibility.

    Meanwhile, functional components are a simple functions that simply should return a JSX markup. There is hooks exists to reach the next level of component flexibility. 

    Each of them can contain any logic into them but the difference between them in the workflow with them.
    
    ---
    </details>
        
7.  <details><summary>What is the key?</summary>
    The key is a special prop in React that implicitly exist in any JSX entity. This prop helps React to identefy the changes into components. We must to use the key explicitly when we should to render some array of data as a list of components or JSX elements.
    
    ---
    </details> 

8.  <details><summary>What are hooks?</summary>
    Hooks are special conceptions in functional components provide us comfortable controls of data and components workflows. They allows the more expressive and understandable approach instead of class lifecycle methods and they can be use more flexible.
    
    Some of them can have a dependecies array that provide a light-understandable control of data or component dependencies.
    
    ---
    </details>

9. <details><summary>Component renders.</summary>
    When the component appears on the screen in first time or after unmounting it means that <b>initial render</b> was caused

    If some of reactive values of existed component were changed or the parent component was re-rendered it will calls <b>re-render</b> of component
    
    ---
    </details>


## Lecture #2 - React basics #2

[To top](#react-interview-questions)

1.  <details><summary>What is the State and how to use it?</summary>
    That is current state of a component or an application. Some data which our components working with. As I mentioned before, state can be for components, for the application or it parts as well.

    To reach the state manipulations and usage we can use lifecycle methods or hooks, such as useState, useReducer, useEffect and anothers or additional libraries such as Redux to achieve comfortable workflow with global state of application.
    
    ---
    </details>

2.  <details><summary>What are reactive and non-reactive values</summary>
    Reactive values are exact what React dealing with. Changes of reactive values will trigger the re-rendering of components. Due for it we can show an up-to-date data to user in each moment of working with application. The Reactive value can be created by the state management features such as useState hook.

    Opposite of reactive values are non-reactive values. The React re-render feature will not reflect on changes of these values and will not re-render components if some of these were changed. To create any non-reactive value we can use hook useRef or deal with common JS variables, constants or class fields.
    
    ---
    </details>

3.  <details><summary>useState and useReducer</summary>
    Hooks useState and useReducer uses to create and manipulate with state of components. 

    While useState uses to reach the control with some simple data such as JS primitives, arrays or a small objects the useReducer uses to work with more complicated data such as objects with many fields with nested object as an example.

    useState returns a value and a function to change this value. To reach the value changing we can provide new value or a function callback in returned function setter. Callback have an access to previous previous value and should return the new one.

    useReducer returns a value and a function reducer that we should provide in hook while created it. The reducer function should be a clear function that awaits for some action and always returns state with changes based on received action type.
    
    ---
    </details>

4.  <details><summary>Context and useContext?</summary>
    Context is a global application state or a part of it. It's providing us some values or a complex data structures in the different parts or components of application and it get us access to use and change theys.

    To use the context we should create it with the createContext function that awaits for value with initial state of context or null. Then to use this context we should to wrap the part of application by this context Provider and it will provide an access to the context.

    We can get this data using the useContext hook (that awaits for the value created with createContext function) in a parts of application that were wrapped by this context provider.
    
    ---
    </details>

5.  <details><summary>useRef</summary>
    One of the ways to create non-reactive value is a useRef hook. It's always an object with field current as result. This field is mutable and can contain any data such as some JS data types or HTML nodes.    
    
    ---
    </details>

6.  <details><summary>forwardRef and useImperativeHandle</summary>
    forwardRef is a function wrapper for component that awaits for ref. The component should me implemented as a function declaration or an arrow nameless function that firstly receive a props and secondary a ref as an arguments.

    If we wanna send ref to a child component from parrent using a common way and prop ref we'll should to wrap the child using forwardRef and then we'll have an access to this ref from parent.

    Using the useImperativeHandle that related uses with forwardRef we can reach more flexible manipulations with child component from the parent. This hook awaits for ref and callback that returns an object with fields that we'll can use in parent component later.
    
    ---
    </details>

## Lecture #3 - React Intermediate

[To top](#react-interview-questions)

1. <details><summary>Lifecycle of react components</summary>
    There are three stages. Mounting, updating and unmounting.

    Class and Functional components have itself flows to work with lifecycles. Each of them can manipulate it state based on current stage.
    
    ---
    </details>

2.  <details><summary>Class lifecycle methods</summary>
    They provide us with the opportunity to work with the state of a class component at different stages of its lifecycle. Due to them, we can manipulate data during component mounting, updating, or unmounting.

    The more commonly used lifecycle methods include componentDidMount, componentDidUpdate, and componentWillUnmount.

    There are also other methods such as shouldComponentUpdate, componentDidCatch, getSnapshotBeforeUpdate, or getDerivedStateFromProps.
    
    ---
    </details>
    
3.  <details><summary>useEffect</summary>
    This hook provide us a possibility to do some side-effects into functional components. Its sugnature is useEffect(callback, dependecnies). The callback of it will called in each initial render and each next re-render if we'll not provide a dependencies array.

    This hook have more flexible behavior than class lifecycle methods due dependencies array. Due to instant callback calling after component did mounted we achieved componentDidMount functionallity, if we'll not provide the dependencies array we'll reach the componentDidUpdate fucntionallity and due to return callback from the called callback we're reaching componentWillUnmount functionallity but not in useEffect context - not component.

    And there are more usefull cases based on an array of dependencies that will trigger callback each time when some of provided dependencies was changed. Or will trigger only ones if the dependencies array is empty.
    
    ---
    </details>
    
4.  <details><summary>useLayoutEffect</summary>
    This is a hook that fires before a browser repaints the screen. It's should be noted that the useLayoutEffect works synchroniously instead of synchronous work as works useEffect

    It's also awaits for callback that also can return a clean-up function and dependencies array and will call provided function based on component lifecycle and dependencies.
    
    ---
    </details>
    
5.  <details><summary>Dependencies</summary>
    Some of hooks awaits for array as a dependencies.

    Dependencies array it's an entity that will checked by any hook that awaits for it while something changes in state. If something from state was changed and it was as dependency in the array - it will trigger callback.
    
    ---
    </details>
    
6.  <details><summary>Custom hooks</summary>
    Based on provided built-in hooks we can create a custom hooks. Usually they're combinations of pair or more hooks. It's usefull when we want to create a short-hand of some repeatable logic based on hooks.
    
    ---
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
    
    ---
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

    ---
    </details>

2.  <details><summary>Routes and Route</summary>
    Routes and Route are React components that implements routing functionallity within our application. We should provide a string as a route path into same-name "attribute" or prop of Route component.

    Routes is a wrapper under our Route components.

    We can nest the Route component in another one to reach the thin setup of routing. It's an alternate way to create flexible routing (instead of modern router object created with createBrowserRouter for example).
    
    ---
    </details>

3.  <details><summary>Nested routes</summary>
    To reach the flexible workflow with routes we can use nested routes that can be as a parameteres or separated folders
    
    ---
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
    
    ---
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
    
    ---
    </details>

6.  <details><summary>Outlet</summary>
    That is component that will place router depended components.

    An <Outlet> should be used in parent route elements to render their child route elements. This allows nested UI to show up when child routes are rendered. If the parent route matched exactly, it will render a child index route or nothing if there is no index route.
    
    ---
    </details>

7.  <details><summary>useParams</summary>
    That is hook that returns an object { key: value } that contains each of parameters in current URL.
    
    ---
    </details>

8.  <details><summary>History breaker - replace</summary>
    To reach the rerouting without possibility to returning back in any link or function as navigate() we can put additional object with field replace { replace: true }
    
        <Link to="/home" replace>Home</Link>

        navigate('/new-url', { replace: true });

        history.replace('/home', { replace: true });



    ---
    </details>

## Lecture #5 - Redux #1

[To top](#react-interview-questions)

1.  <details><summary>Redux</summary>

    Redux is one of the state management libraries that provide a comfortable workflow with the global state of application based on the Context API.

    The global state can be used as an application state or as a seperate part of it. We can wrap any part of app by the chosen "context" provider and use this state in any child of this component.

    In React applications we can use react-redux library that provides us more effective way to interact with global state by using react patterns such as hooks.
    
    ---
    </details>

3.  <details><summary>Rules of Redux</summary>

    There is main redux rules:

    - Single Source of Truth - means that should be existed only one global state and only it must be as a Source of Truth. The current application state must be received only from it.
    - State is immutable - means that the state is read-only. We can make some changes directly in state. Each changes should be make by reducers
    - Reducers is a pure functions that always return a new state based on previous state and received action.
    - One Way Data Flow - means that the data have only one way from components - through  dispatch to store

    
    ---
    </details>

5.  <details><summary>HOC connect()</summary>

    This is react-redux High Ordered Function that returns received component that will connected with redux state. We should provide 2 functions that will handle our work with state.

    They're mapStateToProps and mapDispatchToProps.

    mapStateToProps will handle what exact part of state we'll receive, meanwhile mapDispatchToProps will handle state changes
    
    ---
    </details>

7.  <details><summary>Middlewares</summary>

    Middleware - is a general development concept of functions that work with data that we passed in them and can make some changes in the data.
    
    ---
    </details>

8.  <details><summary>Normalized state</summary>
 
    WORK IN PROGRESS
    
    ---
    </details>
    
9.  <details><summary>Reducers and Actions</summary>

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
    
    ---
    </details>

10. <details><summary>useSelector and useDispatch</summary>

    They're hooks to interact with redux state.
    
    The useSelector is selector for our state. We can get some piece of state with it.

        const userState = useSelector(state => state.users)
    
    useDispatch is a hook that returns a function to handle state changes. It sends an action to store and in store will be applied changes based on this action.

        const dispatch = useDispatch()

        dispatch({ type: 'ADD_USER', payload: newUser })

        or

        const ADD_USER_ACTION = { type: "ADD_USER", payload: userObject }
        dispatch(ADD_USER_ACTION)

    ---
    </details>

11. <details><summary>Redux lifecycle</summary>
 
    Everything begins from UI. When we want to change something in state we'll handle some event by handler that should calls dispatch function and put in it some action based on current event.

    - The action starts it way to store through dispatcher and may be modified by middlewares. 
    - Then the data goes through reducers and when some of them figure out received action type, they're returning a new state.
    - Next step is updated data going to UI
    
    ---
    </details>

12. <details><summary>Memoised selector</summary>
 
    This selector will helps in cases when we want to save some part of data (as a list of some IDs) and do not re-render or re-calculate something. 

    While a common selector will be called each time when component was rerendered, a memoised one will not. It will cash the date and return cashed value each time if an arguments were not changed.
    
    ---
    </details>

## Lecture #6 - Redux #2

[To top](#react-interview-questions)

1.  <details><summary>RTK Query</summary>
    Redux Toolkit Query is an extension over redux that provide for us another level of abstraction to free us from writting much boiler plate code.

    It's provide more comfortable new features such as configureStore, createSlice, createApi, redux devtools and much anothers to make our development experience much faster and effectively.
    
    ---
    </details>


2.  <details><summary>configureStore</summary>
    It's a comfortable way to setup store. configureStore is waiting for reducers that we can provide from slices or from fucntion combineReducers that may fit them all in one variable. It's may accept midlewares as well.

    ---
    </details>

3.  <details><summary>createSlice</summary>
    createSlice - is a function that awaits for settings object that should include name of slice, initial state, reducers, extraReducers and returns one same-named part of global state. That's why it's calls as slice.
    
    ---
    </details>


2.  <details><summary>extraReducers</summary>
    That is additional reducers that provides for us a feature to react when some of actions was comes from dispatch. We always have an access to current store and received action and can implement some logic based on them.

    ---
    </details>

3.  <details><summary>createAsyncThunk</summary>
    It is an action that works with asynchronous things such us data fetching. It's waiting for name of action that usually used as string, and asynchronous function that returns some date. It's works as an action and we can react on it with our extraReducers.
    
    ---
    </details>

4.  <details><summary>createApi</summary>
    It's a modern decision to implement more comfortable interaction with API. createApi is waiting for an object with settings such as reducerPath, baseQuery and endpoints.

    endpoints is a function that receive a builder object and should return an object with different methods based on current needs. It can be qurey to get something from server or mutation to send something to server.
    
    ---
    </details>


## Lecture #7 - React Advanced

[To top](#react-interview-questions)

1.  <details><summary>React patterns</summary>
  
    - Props destructuring
    - Conditional rendering
    - Array rendering
    - Children rendering
    - High Order Component
    
    ---
    </details>

2.  <details><summary>Key</summary>

    A key is a special prop that implicitly exist in any JSX entity in react. Due this prop react is figuring out what and where was changed.

    We should use the key explicitly when we're rendering an array of something as a list of JSX elements. The JSX element that we're returning from the map function should have explicitly setled key that must be a unique value.

    That means if we'll render a dynamic array, indexes of that array will not be optimal decision to set them as keys. Better variant - it's using IDs of iterable entities if theys exist, or pre-set IDs with using some library before mapping this data. 
    
    ---
    </details>

3.  <details><summary>Suspense</summary>

    It's a special component that can provide some component instead of currently downloadable. 

    Currently it's working with lazy components that we can create by lazy() function that will dinamycaly import specified component.
    
    ---
    </details>

3.  <details><summary>React Reconciliation</summary>

    It's a process of comparing the current tree with the work-in-progress tree, followed by an optimized way to commit the changes from the work-in-progress tree to the current tree. These changes are applied to the virtual DOM, resulting in the updated virtual DOM becoming the new current tree.
    
    ---
    </details>

4.  <details><summary>Fiber</summary>

    Fiber is a new conception since React 16 that provide a more effective way of reconciliation than earlier stack-based. 
    
    It's includes:
    - Prioritisation
    - Pausing
    - Resuming
    - Aborting
    - Concurrency

    > [!WARNING]
    > The problematic of previous stack-based approach is a list of neccessary performance issues:
    > - Lack of interruption
    > - Synchronous process
    > - Inefficient updates
    > - Limited prioritization

    > [!TIP]
    > We can think of a single fiber as a virtual stack frame. In simple terms, a fiber represents a unit of work with its own virtual stack. 
    
    In the previous implementation of the reconciliation algorithm, React created a tree of objects (React elements) that are immutable and traversed the tree recursively.

    In the current implementation, React creates a tree of fiber nodes that can mutate. The fiber node effectively holds the component’s state, props, and underlying DOM element it renders to.

    
    
    ---
    </details>

5.  <details><summary>Parallel processes in React</summary>

    Due to new conception as Fiber the React have an option to make state changes asynchronously and in more effective way.
    
    This also will prevent unneccessary re-renders due to "batching" coception that will collect same tasks and will accept them in only one time
    
    ---
    </details>

## Lecture #8 - React Optimisation

[To top](#react-interview-questions)

1.  <details><summary>Motivation - general questions</summary>
    
    - Can we move the calculations from front to back?
  
    - Can we refactor code to simplify calculations?
  
    - Are we really should memoize it?
    
    ---
    </details>

2.  <details><summary>useMemo & useCallback</summary>
   
    s
    
    ---
    </details>

3.  <details><summary>memo(component, arePropsEqual?)</summary>

    s
    
    ---
    </details>

4.  <details><summary>PureComponent</summary>

    s

    ---
    </details>

5.  <details><summary>lazy()</summary>

    s

    ---
    </details>

6.  <details><summary>Virtualisation</summary>

    s

    ---
    </details>

7.  <details><summary>Bundle optimisation</summary>

    s

    ---
    </details>

8.  <details><summary>Web workers</summary>

    s

    ---
    </details>
    
9.  <details><summary>Image optimisation</summary>

    s

    ---
    </details>
    
10. <details><summary>Reselect</summary>

    s

    ---
    </details>


## Lecture #9 - External Libraries

[To top](#react-interview-questions)


1.  <details><summary></summary>

    s

    ---
    </details>

1.  <details><summary></summary>

    s

    ---
    </details>

## Lecture #10 - Typescript

[To top](#react-interview-questions)

1.  <details><summary></summary>

    s

    ---
    </details>

1.  <details><summary></summary>

    s

    ---
    </details>


## Lecture #11 - Testing, debugging, Agile

[To top](#react-interview-questions)

1.  <details><summary></summary>

    s

    ---
    </details>

1.  <details><summary></summary>

    s
    
    ---
    </details>


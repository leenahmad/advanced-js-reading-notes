# Hook 

We know that components and top-down data flow help us organize a large UI into small, independent, reusable pieces. However, we often can’t break complex components down any further because the logic is stateful and can’t be extracted to a function or another component. Sometimes that’s what people mean when they say React doesn’t let them “separate concerns.”

These cases are very common and include animations, form handling, connecting to external data sources, and many other things we want to do from our components. When we try to solve these use cases with components alone, we usually end up with:

- Huge components that are hard to refactor and test.
- Duplicated logic between different components and lifecycle methods.
- Complex patterns like render props and higher-order components.

[read more about hook here](https://medium.com/@dan_abramov/making-sense-of-react-hooks-fdbde8803889) 🤏

-------------------

# Code State Hook

![state hook](https://miro.medium.com/proxy/1*xGHdt-0F2jtUUNSB93O3JQ.png)

[click me to see codes](https://reactjs.org/docs/hooks-state.html)🤏


-------------

# hooks api 


They let you use state and other React features without writing a class.

id , handleStatusChange ) ; } ; } ) ; if ( isOnline === null ) { return 'Loading...' ; } return isOnline ? '

isOnline ) ; } Hooks let you organize side effects in a component by what pieces are related (such as adding and removing a subscription), rather than forcing a split based on lifecycle methods.

Detailed Explanation You can learn more about useEffect on a dedicated page: Using the Effect Hook.

First, we’ll extract this logic into a custom Hook called useFriendStatus : import React , { useState , useEffect } from 'react' ; function useFriendStatus ( friendID ) { const [ isOnline , setIsOnline ] = useState ( null ) ; function handleStatusChange ( status ) { setIsOnline ( status .


![hook api](https://resources.infosecinstitute.com/wp-content/uploads/042214_1534_APIHooking2.png)

[hooks api](https://reactjs.org/docs/hooks-overview.html)

--------------

# hooks api reference

This page describes the APIs for the built-in Hooks in React.


1. Basic Hooks
   - useState
   ```
   const [state, setState] = useState(initialState);

   ```
   - useEffect
   ```
   useEffect(didUpdate);
   ```
   - useContext
   ```
   const value = useContext(MyContext);
   ```

2. Additional Hooks
   - useReducer
   ```
   const [state, dispatch] = useReducer(reducer, initialArg, init);
   ```
   - useCallback
   ```
   const memoizedCallback = useCallback(
      () => {
    doSomething(a, b);
     },
        [a, b],
    );
   ```
   - useMemo
   ```
   const memoizedValue = useMemo(() => computeExpensiveValue(a, b), [a, b]);
   ```
   - useRef
   ```
   const refContainer = useRef(initialValue);
   ```
   - useImperativeHandle
   ```
   useImperativeHandle(ref, createHandle, [deps])
   ```
   - useLayoutEffect
   ```
   ```
   - useDebugValue
   ```
   useDebugValue(value)
   ```
   - useDeferredValue
   ```
   const deferredValue = useDeferredValue(value);
   ```
   - useTransition
   ```
   const [isPending, startTransition] = useTransition();
   ```
   - useId
   ```
   const id = useId();
   ```

3. Library Hooks
   - useSyncExternalStore
   ```
   const state = useSyncExternalStore(subscribe, getSnapshot[, getServerSnapshot]);
   ```
   - useInsertionEffect
   ```
   useInsertionEffect(didUpdate);
   ```


[hooks api reference](https://reactjs.org/docs/hooks-reference.html)


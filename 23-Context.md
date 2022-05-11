# React Context


React Context is a way to manage state globally.

It can be used together with the useState Hook to share state between deeply nested components more easily than with useState alone.

In a typical React application, data is passed top-down (parent to child) via props, but such usage can be cumbersome for certain types of props (e.g. locale preference, UI theme) that are required by many components within an application. Context provides a way to share values like these between components without having to explicitly pass a prop through every level of the tree.



### When to Use Context

Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language.


### Before You Use Context

Context is primarily used when some data needs to be accessible by many components at different nesting levels. Apply it sparingly because it makes component reuse more difficult.

If you only want to avoid passing some props through many levels, component composition is often a simpler solution than context.




- API

    - React.createContext
    - Context.Provider
    - Class.contextType
    - Context.Consumer
    - Context.displayName


![react context](https://res.cloudinary.com/practicaldev/image/fetch/s--I_MQW9s2--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://blog.pagepro.co/wp-content/uploads/2019/12/pasted-image-0-1024x515.png)



[read more from here for more info](https://reactjs.org/docs/context.html#classcontexttype)

[hooks and context example](https://reactjs.org/docs/context.html#classcontexttype)

[react context links](https://github.com/diegohaz/awesome-react-context)



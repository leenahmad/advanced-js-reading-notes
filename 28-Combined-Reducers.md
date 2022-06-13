# Combined Reducers

On this page Using combineReducers The most common state shape for a Redux app is a plain Javascript object containing "slices" of domain-specific data at each top-level key.

See Beyond combineReducers for examples and suggestions.)

While Redux itself is not opinionated about how your state is organized, combineReducers enforces several rules to help users avoid common errors.

However, combineReducers has specific behavior that does work that way.

In order to assemble the new state tree, combineReducers will call each slice reducer with its current slice of state and the current action, giving the slice reducer a chance to respond and update its slice of state if needed.

So, in that sense, using combineReducers does "call all reducers", or at least all of the slice reducers it is wrapping.


On this page combineReducers(reducers) As your app grows more complex, you'll want to split your reducing function into separate functions, each managing independent parts of the state.

For example, you may call combineReducers({ todos: myTodosReducer, counter: myCounterReducer }) for the state shape to be { todos, counter } .

A popular convention is to name reducers after the state slices they manage, so you can use ES6 property shorthand notation: combineReducers({ counter, todos }) .

Earlier documentation suggested the use of the ES6 import * as reducers syntax to obtain the reducers object.

Any reducer passed to combineReducers must satisfy these rules: For any action that is not recognized, it must return the state given to it as the first argument.

export default function todos ( state = [ ] , action ) { switch ( action .


![img](https://miro.medium.com/max/1400/0*GbreE_PkjDuYaOdS.jpg)
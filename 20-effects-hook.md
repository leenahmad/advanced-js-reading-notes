# effects-hook 

![img](https://daveceddia.com/images/useEffect-hook.png)

The useEffect Hook allows you to perform side effects in your components.

Some examples of side effects are: fetching data, directly updating the DOM, and timers.

useEffect accepts two arguments. The second argument is optional.

useEffect(`<function>, <dependency>`)

useEffect runs on every render. That means that when the count changes, a render happens, which then triggers another effect.

This is not what we want. There are several ways to control when side effects run.

We should always include the second parameter which accepts an array. We can optionally pass dependencies to useEffect in this array.



--------------------------


Here’s how we might subscribe and display that status using a class: class FriendStatus extends React .

id , handleStatusChange ) ; return ( ) => { ChatAPI .

If you feel like you have a decent grasp on how the Effect Hook works, or if you feel overwhelmed, you can jump to the next page about Rules of Hooks now.

Our class reads friend.id from this.props , subscribes to the friend status after the component mounts, and unsubscribes during unmounting: componentDidMount ( ) { ChatAPI .

Note If you use this optimization, make sure the array includes all values from the component scope (such as props and state) that change over time and that are used by the effect.


####  We can optionally pass dependencies to useEffect in this array.

1. No dependency passed: useEffect(() => { //Runs on every render });
2. An empty array: useEffect(() => { //Runs only on the first render }, []);
3. Props or state values


![img](https://dmitripavlutin.com/533bea4c73b775e7cb1cad6d1d4acaf1/react-useeffect-callback-3.svg)

[read more from here](https://reactjs.org/docs/hooks-effect.html)


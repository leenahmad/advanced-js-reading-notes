# react hello world




The smallest React example looks like this: ReactDOM .

```
ReactDOM
  .createRoot(document.getElementById('root'))
  .render(<h1>Hello, world!</h1>);

```

## Knowledge Level Assumptions

React is a JavaScript library, and so we’ll assume you have a basic understanding of the JavaScript language. If you don’t feel very confident, we recommend going through a JavaScript tutorial to check your knowledge level and enable you to follow along this guide without getting lost. It might take you between 30 minutes and an hour, but as a result you won’t have to feel like you’re learning both React and JavaScript at the same time.



--------------

# Introducing JSX

Consider this variable declaration: const element = < h1 > Hello, world!

We will explore rendering them to the DOM in the next section.

React doesn’t require using JSX, but most people find it helpful as a visual aid when working with UI inside the JavaScript code.
With that out of the way, let’s get started!

In the example below, we embed the result of calling a JavaScript function, formatName(user) , into an
element.

potentiallyMaliciousInput ; const element = < h1 > { title } ; By default, React DOM escapes any values embedded in JSX before rendering them.

----------------------------

# Rendering Elements

Elements are the smallest building blocks of React apps.'

An element describes what you want to see on the screen: const element = < h1 > Hello, world ; Unlike browser DOM elements, React elements are plain objects, and are cheap to create.

Updating the Rendered Element React elements are immutable.

In the next sections we will learn how such code gets encapsulated into stateful components.

We recommend that you don’t skip topics because they build on each other.

You can verify by inspecting the last example with the browser tools: Even though we create an element describing the whole UI tree on every tick, only the text node whose contents have changed gets updated by React DOM.



[read more about react hello world](https://reactjs.org/docs/hello-world.html)

[read more about Introducing JSX](https://reactjs.org/docs/introducing-jsx.html)

[read more about Rendering Elements](https://reactjs.org/docs/rendering-elements.html)
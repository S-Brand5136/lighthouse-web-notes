# Notes

- What are the advantages of using React ?

  - Use of the virtual DOM to improve efficiency

    - Each time data changes in a react app, a new virtual DOM is created. Creating a virtual DOM is much faster than rendering UI in the browser
    - Because react is such a small framework its very easy to pick up quickly
    - SEO friendly
      - UI can be built to be easily navigated
    - Reusable components
      - component-based architecture, this increases the speed of development
    - Large amount of librarys to choose from

- What are props ?

  - Props are Immutable, have better performace, can be passed to child components

  - Every react component, accepts a single object argument called props (which stands for “properties”).
    These props can be passed to a component using HTML attributes and the component accepts these props as an argument.
    Using props, we can pass data from one component to another.

- What is state ?

  - State is Owned by its component, Locally scoped, Mutable, has setState method to modify properties, Changes to state can be asychronous, can only be passed as props

  - Every component in react has a built-in state object, which contains all the property values that belong to that component.

- What is a hook ?

  - Hooks are funcitons that let us "hook into" React state and lifecycle features from a functional component. React hooks CANNOT be used in class components. They let us write components without class.

- What is JSX ?

  - Stands for Javascript XML. It allows us to write HTML inside of javascript and place them in the DOM without using functions like appendChild() or createElement().

- What is the dif between func/class based components

  - Before the introduction of Hooks in React, functional components were called stateless components and were behind class components on feature basis. After the introduction of Hooks, functional components are equivalent to class components.

- What is the virtual dom

  - The virtualDOM is a concept where a virtual representation of the real DOM is kept inside the memory and is synced witht he real DOM by a library such as ReactDOM.

  - For every DOM object there is a corresponding DOM object. Which has the same properties.

- Different ways to style ?

  - Inline styling
  - Javascript objects
  - CSS stylesheets
  - CSS Modules

- What are keys ?

  - A key is a special string attribute that needs to be included when using lists of elements.

  - The index as the key should be avoided

- How to pass data ?

  - With the use of props we can pass data down to a child.

  - Through the use of callbacks we can pass data back up from the child to the parent

- What is prop drilling ?

  - Prop drilling is when we need to pass data from a component that is higher in the hierarchy to a component that is deeply nested. In order to do this we pass props from a source component and keep passing it until its reached the deeply nested component.

    - The disadvantage of this is components that shouldnt have access to the data, do.

- What are the different lifecycle methods in React?

  - Every component in React has lifecycle methods that we can tap into to trigger changes at a particular phase of the lifecycle

  - The three lifecycle methods are _Mounting_, _Updating_, and _Unmounting_

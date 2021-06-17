# Notes

## React class-based components

- A React component declared using an ES6 class must follow additional rules

  - Basic syntax

```js
import React, { Component } from 'react';

class Application extends Component {
  render() {
    return <div></div>;
  }
}
```

- The first and second rules of a react class based components

  - All class-based React components must extend the React.Component class.
  - All class-based React components must override the render method of the React.Component superclass that they extend.

- We are not required to override the constructor method, but if we do, then we must follow an important rule to ensure that our component works properly.

```js
import React, { Component } from 'react';

class Application extends Component {
  constructor(props) {
    /* If we add a constructor to our class, we must pass props to the super class */
    super(props);
  }

  render() {
    return <div></div>;
  }
}
```

### Version Managers

- Version managers are tools that allow us to easily download and switch between different versions of software, like node

- Ruby has its own package manager called RVM
  - There is alternatives to RVM like n, asdf, rbenv

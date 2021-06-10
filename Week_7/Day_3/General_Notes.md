# Notes

### Proxying API requests in Development

- Adding a proxy to package.json during development allows us to avoid CORS errors when making api requests.

- The development server will only attempt to send requests without text/html in its Accept header to the proxy.

- MDN about cors

  > For security reasons, browsers restrict cross-origin HTTP requests initiated from scripts. For example, XMLHttpRequest and the Fetch API follow the same-origin policy. This means that a web application using those APIs can only request resources from the same origin the application was loaded from unless the response from other origins includes the right CORS headers.

- Why is it important to leave the original version of our state unchanged when we are updating state ?
  - React compares the old values and the new values, it needs a way to faithfully make a comparison

## React useEffect Rules

- #1
  - Don't call Hooks inside loops, conditions or nested functions.
- #2
  - Only call hooks from inside React components
- #3

  - The effect method that we pass to useEffect must either return undefined or a function

- There are two classifications of side effects. Some require cleanup, and others do not. We can return a function from our effect that describes how to clean up the side effect. Timers, event listeners and socket connections are examples of side effects that require cleanup.

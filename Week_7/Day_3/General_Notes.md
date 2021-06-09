# Notes

### Proxying API requests in Development

- Adding a proxy to package.json during development allows us to avoid CORS errors when making api requests.

- The development server will only attempt to send requests without text/html in its Accept header to the proxy.

- MDN about cors
  > For security reasons, browsers restrict cross-origin HTTP requests initiated from scripts. For example, XMLHttpRequest and the Fetch API follow the same-origin policy. This means that a web application using those APIs can only request resources from the same origin the application was loaded from unless the response from other origins includes the right CORS headers.

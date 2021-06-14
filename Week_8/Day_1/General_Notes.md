# Notes

## Testing

- Adding the prop-types libray in react is a quick way to gain confidence that the correct prop-types are passed into the component

  - some other ways to achieve a similar result would be to use a superset of javascript like typeScript or flow

- A component and all of its children will be considered a unit during intergration tests

- Structure of an Intergration test

  - Initialize the component that we would like to test
  - Trigger the change that executes the unit
  - Verify that the unit produced the expected result.

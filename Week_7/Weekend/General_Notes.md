## Notes

# Testing

- Regression testing is the process of verifying that previously uncovered bugs have not returned in all subsequent versions of the software.

- Write tests. Certain types of testing should be automated.
- Not too many. We don't need 100% code coverage to have a high level of confidence.
- Mostly integration. These types of tests are more thorough and test how the different parts of the application work together.

- Four distinct categories of tests

  1.  static
  2.  Unit
  3.  Integration
  4.  End-to-End

- Static testing

  - examples of static testing is using tools like ESLint, prettier, or TypeScript to ensure common errors are identified. Such as type coericon

- Unit testing

  - With unit testing, the end goal is to test a function or component in isolation.
    Some frame works built for this kind of testing inculde Jest, and Mocha

- Integration Testing

  - Is the process of testing that 2 distinct units of code work together
  - The risk of writing a lot of integration tests is overlapping coverage. If we are testing these two units with an integration test, we may not want to maintain two additional unit tests as well.

- End-to-End Testing
  - Is the most expensive category of testing. The goal is to get as close to simulated user behavior as possible.

# Test Driven Development

- The goal of TDD is _Clean Code that works_. We follow two rules to achieve it

  - Write new Code only if an automated test has failed
  - Eliminate duplication

- Its a great technique for new developers beacuse it encourages the understanding of requirements before any code is written

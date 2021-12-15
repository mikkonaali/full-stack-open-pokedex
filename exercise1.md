# Continuous Integration in Python development

## Linting

When developing in any language one must configure a suitable CI setup for linting, testing and building before the actual deployment process. In Python ecosystem popular linting tools for developers are `pylint` and `flake8`. They check that source code conforms to common Python programming style norms. Developer can run linter manually in his/her code editor but it can also be automated for example with **Git hooks** to run before each commit. Automated linting can be executed in an external CI server.

## Testing

In our hypothetical scenario all the developers in a small team should write **unit tests** for their Python code to be run before each commit. Python standard library includes a `unittest` module but one popular 3rd party library for writing tests is `pytest`. Tests should be run automatically in the CI server during the CI/CD process even if the developer forgets to do it in the first place. This includes **integration tests** in addition to the forementioned unit testing. Note that when developing web applications with `Django`, it's good to know that Django provides a test runner for unit tests. To automate test execution our team could use for example `Travis CI` which is a framework for testing and deploying projects.

## Building

Because Python is an interpreted language, there is no need for actual compiling the source code in the build step. Building in Python development is then mainly concerned with **including all the required dependencies** that aren't in the standard library, and packaging all the code for deployment.

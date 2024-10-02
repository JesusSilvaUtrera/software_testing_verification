# Test Levels and Types

## Unit Testing
Testing every individual module (method or class) in the code, in isolation if possible, so it's easier to debug any failure.

Unit tests are really useful to help improve your code, make it more readable and simpler, as you will find that maybe you are overcomplicating it.

## Integration Testing
Testing a combination of modules, or even the entire program. It's the next level after unit testing, so you have assured before that the modules isolated work fine, and now you are testing the connections between modules.

It's useful to use **mocks** (also called `stub versions`) for certain modules to ease the testing process (for example, test without the actual hardware, just simulating what it would be like to use it).

## Automated Testing and Regression Testing
The testing process should be run automatically, not manually triggered by someone (it can be helpful to have both possibilities for specific scenearios).

Running all your tests after every change is called **Regression Testing**, so that we check that no new bug is being introduced when solving other or adding new features (this is called Regressing). You can create regression tests adding the fixes you made to the test suite.

Automated and Regression tests are almost always used together (Automated Regression Testing) and it is a good practice of moderns software engineering.

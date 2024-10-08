# Introduction

## Validation
Testing is an example of a more general process called validation. Its purpose is to uncover the problems in a program and increase the confidence in it.

Validation includes:
- Formal reasoning: usually called verification
- Code review: reviewing the code before merging it.
- Testing: running the programs with selected inputs and check the outputs are the expected ones.

## Test first programming
`Test First Driven Development` is a programming technique that involves writing automated tests before writing the code, so write the code accordignly to pass those tests.

You define some specifications first, and create the tests according to those specifications.

## Choose Tests by Partitioning
Divide the input space into subdomains, and choose one test case for every subdomain. This way we have a small enough test suite to run quickly, but large enough to cover all the pissible inputs.

This approach is much better than random testing, but it's slower to accomplish. It may be necessary to divide the output space too, but usually this is not the case.

It's important to consider special cases and boundaries in the test suites, because in those cases is where bugs can often occur. Depending on the specific case, you should be more or less exhaustive when choosing your test suite.

## Blackbox and Whitebox Testing

### Blackbox Testing
Choosing test cases only from the specification (the description of the function's behavior: types of parameters, type of return value, constraints and relationships). With this approach, there is no need to take a look at the implementation, the actual code of the function.

### Whitebox Testing
Choosing your test cases with knowledge of how the function is actually implemented. E.g: if the implementation uses different algorithms according to the input, you should divide according to that behavior. If there is some kind of memory of the previous inputs, you should test repeated inputs.

## Documenting the Testing Strategy
You should document the strategy followed to choose the test cases at the top of the test class, and describe on each test case what's being covered.

## Quality Assurance vs Quality Control
They are often used in the same environment, but they are 2 distinct processes taking place at different times. Both play a vital role for effective quality management.

Quality Assurance is a process-oriented approach. It focuses on preventing defects during the development phase by improving the processes used to develop a product and ensures those methods, techniques and processes are followed. QA is applied from the start until the end of the development lifecycle, being proactive. E.g: defining best practices, process documentation...

Quality Control is a product-oriented approach. It focuses on identifying and correcting defects in the developed product or service. It involves the inspection and testing of the final product to ensure it meets the required standards and specifications. QC is applied after the development, so it's a reactive approach. E.g: code reviews, bug fixing, all kinds of testing...

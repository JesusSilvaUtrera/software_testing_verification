# Test Metrics

## Coverage
One way to judge a test suite is to ask how thoroughly it exercises the program. This notion is called coverage . Here are three common kinds of coverage:
- **Statement coverage** : is every statement run by some test case?
- **Branch coverage** : for every if or while statement in the program, are both the true and the false direction taken by some test case?
- **Path coverage** : is every possible combination of branches — every path through the program — taken by some test case?

Path > Branch > Statement, and the stronger the coverage is, the more tests you need to achieve it. 100% Path Coverage is infeasible, and even 100% Branch Coverage is only achieved on safety-critical industries. Most of the times, we should just focus on the Statement Coverage.

Statement Coverage is usually measured by a Code Coverage Tool, showing you which lines are covered and which aren't, so you can add more tests focusing on the not covered ones until you reach your expected Statement Coverage.

### C++
For C++, the most used tools to check the code coverage are `gcov` (with the command line) and `lcov` (generates a HTML report):
1. Compile the code with the `-coverage` flag:

```
clang++ -O0 -coverage test.cpp && ./a.out
```

2. 2 additional files will be generated: `test.gcda` and `test.gcno`
3. Run the gcov command to check the coverage:

```
gcov test.cpp
```

4. For small projects, this will be enough msot of the times, but for larger projects, you would need to use `lcov`:

```
lcov --directory . --capture --output-file coverage.info
```

5. Finally, generate the HTML files:

```
genhtml --demangle-cpp -o coverage coverage.info
```

6. Open the resulting `coverage/index.html` on a briwser and check the results. It will tell you the coverage and which lines are not covered yet.

You can also integrate this into CMake or CI to make the process easier and automated.

### Python
The most used tool is `coverage.py`. It can be installed with pip.

1. Simply run the command you usually use for running your tests adding the coverage part (args are not required normally):

```
coverage run -m pytest arg1 arg2 arg3
```

2. Then use `coverage report` to report on the results
3. For a nicer presentation, you can create a HTML report using `coverage html` and then open the `htmlcov/index.html` on a browser.

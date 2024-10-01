# Test Metrics

## Coverage
One way to judge a test suite is to ask how thoroughly it exercises the program. This notion is called coverage . Here are three common kinds of coverage:
- **Statement coverage** : is every statement run by some test case?
- **Branch coverage** : for every if or while statement in the program, are both the true and the false direction taken by some test case?
- **Path coverage** : is every possible combination of branches — every path through the program — taken by some test case?

Path > Branch > Statement, and the stronger the coverage is, the more tests you need to achieve it. 100% Path Coverage is infeasible, and even 100% Branch Coverage is only achieved on safety-critical industries. Most of the times, we should just focus on the Statement Coverage.

<!-- TODO -->
Statement Coverage is usually measured by a Code Coverage Tool, showing you which lines are covered and which aren't, so you can add more tests focusing on the not covered ones until you reach your expected Statement Coverage.

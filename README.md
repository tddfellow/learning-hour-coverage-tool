# Learning Hour: Using Coverage Tool to Back-fill Tests for Legacy Code

_Reminder: This learning hour is screen recording friendly. If one of the team members can't join, 
you can record it, and they'll be able to watch later._

Test coverage tool is often used for the metric of quality of the test suite, however, it's not the
place where these tools shine the most. The most useful feature of the test coverage tool is to show
which lines and branches of the code are covered and which aren't. This is especially useful in the
development environment when you want to increase the coverage of the module, or add test coverage
that didn't exist before (e.g., in legacy code contexts).

Reading: (10 min) _(& asking any questions or clarification)_

## What coverage even means?

When the tool reports something as covered, that only means that it has been executed. Whether it was
correctly verified or not is up to developer to understand by reviewing the existing tests.

When combined with approval testing, and assuming that approval printer produces all relevant state &
changes that the executed code has changed and produced, then covered almost equivalent to tested.

## Coverage types

1. Line coverage - this line of code has been executed
2. Branch coverage - when `if` or other conditional type is encountered, the coverage tool can report
   whether this conditional is fully covered or only one of its paths

## How to deal with iteration and loops?

Even if you exercise the loop logic only with a single item, likely the coverage will show all green.
However, this isn't sufficient to properly test iteration. When you encounter the iteration, you should
trigger its zero, one and many cases.

## How to come up with scenarios when you don't know what they could be?

You can look at a particular code path that isn't covered, and think what conditions must be true for
this code path to be exercised by your tests. This will give you an idea of what kind of test you have
to write. Then, from the test setup and assertion, you have to think what scenario this test may be
representing. Additionally, you may encounter "weird" scenarios here - these are usually worth
discussing with business, product or domain expert.

You may find what you consider a bug. But because this bug was there for a while, customers may come to
expect it, and it has since became a feature. When adding the coverage to legacy code, don't try to fix
bugs. Instead, surface them to the business, product and domain experts for later discussion and 
investigation what to do with it.

## Coding Kata (Ensemble)

(45 min)

[SupermarketReceipt Refactoring Kata](https://github.com/emilybache/SupermarketReceipt-Refactoring-Kata/tree/main/typescript)

- Set up coverage tool in your IDE
- Practice identifying test cases and scenarios from missing coverage
- Try to get to 100% line and branch coverage

Use the code sharing tool of your choice (e.g., JB Code-With-Me or VS Code LiveShare).

Ensemble rules:

1. Driver rotates every 5 min 
2. Ensemble serves as a collective navigator 
3. Coach serves as a facilitator, keeping the ensemble productive

## Reflection

(5 min)

1. What did you learn today? 
2. What would you do differently starting tomorrow? 
3. What else do you want to learn deeper now (that you weren't aware before)?

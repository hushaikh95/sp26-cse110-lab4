# Part 1 Answers

## Q1
Line 9 prints: `values added: 20`.

## Q2
Line 13 prints: `final result: 20`.

`result` was declared with `var`, so it has function scope (not block scope) and is still accessible outside the `if` block.

## Q3
You should avoid `var` because it is function-scoped and can be accessed/overwritten outside the block where it is declared, which can cause bugs and naming conflicts. It is also hoisted in ways that can be confusing. `let` and `const` are safer and more predictable.

## Q4
Line 9 prints: `values added: 20`.

## Q5
Line 13 throws an error: `ReferenceError: result is not defined`.

With `let`, `result` is block-scoped to the `if (add) { ... }` block, so it cannot be used outside that block.

## Q6
Line 9 does not print because the code errors first at `result = num1 + num2`.

With `const`, reassignment is not allowed, so JavaScript throws `TypeError: Assignment to constant variable.` before line 9 executes.

## Q7
Line 13 is not printed because execution already stopped due to the `TypeError` from trying to reassign a `const`.


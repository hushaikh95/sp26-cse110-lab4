# Part 1 Answers

## Q1
Line 9 prints: `values added: 20`.

## Q2
Line 13 prints: `final result: 20`.

## Q3
You should avoid `var` because it is function-scoped and can be accessed outside the block where it is declared, which can cause bugs and naming conflicts.

## Q4
Line 9 prints: `values added: 20`.

## Q5
Line 13 throws an error: `ReferenceError: result is not defined`.

The variable was definied using `let` which is block-scoped to the `if` block, so it cannot be used outside that block. Meaning in line 13 when result is being accessed outside the `if` block the code fails cause there is no result variable outside the `if` block. 

## Q6
Line 9 does not print because the code errors first at `result = num1 + num2`.

The variable is definied as `const`, which means reassignment is not allowed, so JavaScript throws `TypeError: Assignment to constant variable.` before line 9 executes.

## Q7
Line 13 is not printed because execution already stopped due to the `TypeError` from trying to reassign a `const`.


# Part 2 Answers

## Q1
Line 12 prints `3`.

`i` is declared with `var`, so it is function-scoped (not block-scoped). After the loop finishes, `i` has value `3` (`prices.length`).

## Q2
Line 13 prints `150`.

`discountedPrice` is declared with `var`, so it is also function-scoped and still accessible after the loop. Its final assigned value is from the last iteration: `300 * 0.5 = 150`.

## Q3
Line 14 prints `150`.

`finalPrice` is declared in the function scope (`var finalPrice = 0`) and updated each loop iteration. After the last iteration, it is `150`.

## Q4
The function returns `[50, 100, 150]`.

Each item in `prices` is multiplied by `(1 - 0.5)` and rounded to 2 decimals, then pushed into `discounted`.

## Q5
Line 12 throws `ReferenceError: i is not defined`.

Here `i` is declared with `let` in the `for` loop, so it is block-scoped to that loop and cannot be accessed outside it.

## Q6
Line 13 throws `ReferenceError: discountedPrice is not defined`.

`discountedPrice` is declared with `let` inside the loop block, so it only exists inside that block.

## Q7
Line 14 prints `150`.

`finalPrice` is declared with `let` in the function body (outside the loop block), so it is accessible at line 14 and holds the last computed value.

## Q8
The function returns `[50, 100, 150]`.

No error occurs because the out-of-scope `console.log` lines are commented out, and the return value is the built `discounted` array.

## Q9
Line 11 throws `ReferenceError: i is not defined`.

`i` is declared with `let` inside the `for` loop, so it is block-scoped and unavailable outside the loop.

## Q10
Line 12 prints `3`.

`length` is declared as `const length = prices.length` in function scope, so it is accessible at line 12 and equals `3`.

## Q11
The function returns `[50, 100, 150]`.

`discounted` is a `const` array, which means the variable binding cannot be reassigned, but the array contents can still be modified with `push`.

## Q12
A. `student.name`

B. `student['Grad Year']`

C. `student.greeting()`

D. `student['Favorite Teacher'].name`

E. `student.courseLoad[0]`

## Q13 (Arithmetic)
A. `'3' + 2` -> `'32'`  
String concatenation happens because one operand is a string.

B. `'3' - 2` -> `1`  
`-` forces numeric conversion, so `'3'` becomes `3`.

C. `3 + null` -> `3`  
`null` converts to `0` in numeric addition.

D. `'3' + null` -> `'3null'`  
`+` with a string does concatenation, so `null` becomes `"null"`.

E. `true + 3` -> `4`  
`true` converts to `1`.

F. `false + null` -> `0`  
`false` converts to `0` and `null` converts to `0`.

G. `'3' + undefined` -> `'3undefined'`  
String concatenation converts `undefined` to `"undefined"`.

H. `'3' - undefined` -> `NaN`  
`-` tries numeric conversion; `undefined` becomes `NaN`.

## Q14 (Comparison)
A. `'2' > 1` -> `true`  
`'2'` is converted to number `2`, and `2 > 1`.

B. `'2' < '12'` -> `false`  
Both are strings, so lexicographic comparison is used (`'2'` > `'1'`).

C. `2 == '2'` -> `true`  
`==` performs type coercion, converting `'2'` to `2`.

D. `2 === '2'` -> `false`  
`===` requires same type and value; number vs string fails.

E. `true == 2` -> `false`  
`true` converts to `1`, and `1 == 2` is false.

F. `true === Boolean(2)` -> `true`  
`Boolean(2)` is `true`, and both sides are boolean `true`.

## Q15
`==` checks loose equality and allows type coercion before comparison.  
`===` checks strict equality and does not coerce types, so both type and value must match.

## Q17
`modifyArray([1,2,3], doSomething)` returns `[2,4,6]`.

Briefly: `modifyArray` iterates through each element and applies the callback (`doSomething`) to it.  
So `1 -> 2`, `2 -> 4`, and `3 -> 6`, producing the final array `[2,4,6]`.

## Q19
The output order is:
1. `1`
2. `4`
3. `3`
4. `2`

`1` and `4` are logged synchronously in the function call.  
The `setTimeout(..., 0)` callback (`3`) runs next from the event queue, and `setTimeout(..., 1000)` (`2`) runs about one second later.


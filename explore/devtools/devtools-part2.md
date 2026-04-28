## What was the bug?

`num1` and `num2` are read from input elements, so they are strings.  
In `calculateSum(num1, num2)`, using `num1 + num2` concatenates strings instead of adding numbers.

Example: `"2" + "3"` becomes `"23"` instead of `5`.

## How would you fix it?

Convert both values to numbers before adding.
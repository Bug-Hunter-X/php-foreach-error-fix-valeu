# PHP foreach() Error: Argument must be of type array|object, null given
This repository demonstrates a common error in PHP when using foreach loops: attempting to iterate over a variable that is not an array or object.  The code in `bug.php` shows the problematic code.  The solution, provided in `bugSolution.php`, demonstrates how to robustly handle potential null or non-iterable values.

## How to reproduce the bug:
1. Clone this repository.
2. Run `bug.php`.
3. Observe the fatal error.

## Solution:
The solution in `bugSolution.php` utilizes type checking and null coalescing to safely handle different potential return types from `someFunctionThatMightReturnAnything()`.  It provides a default empty array if the return value is not iterable, preventing the fatal error.
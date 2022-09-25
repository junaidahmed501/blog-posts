## ES6: How to distinguish between spread & rest operators?

> This tip is for those learners who already know what spread & rest operators are but sometimes are unclear when one is being used.

When we see `"..."` in the code, it is either rest parameters or the spread operator.

There’s an easy way to distinguish between them:

*   When `...` is at the end of function parameters, it’s “rest parameters” and gathers the rest of the list of arguments into an array. I also like it call it the receiving end.
*   When `...` occurs in a function call or alike, it’s called a “spread operator” and expands an array into a list.
# Built-in Methods

This is a related series of simulated technical interview questions, with guiding notes.

## Implement each()

Implement a function `each(list, action)` that applies the `action` on every item in `list`:

- `list` should be an array
- `action` should be a function

To test your implementation, pass in a function that console logs an item as the `action` argument, and pass in `[1, 2, 3]` as the `list` argument, as in: `each([1, 2, 3], function () { // ... })`. If your implementation is correct, you should see the numbers 1, 2, and 3 printed to Terminal sequentially.

Hint: This is similar to the built-in [`forEach()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach) method in JavaScript.

Note: This is designed to test if you understand how to pass in a function as a parameter of another function - also known as a callback pattern or callback function (referring to the function being passed in, not the one receiving the function).

## Further - implement reduce()

Using your implementation of `each()`, implement a function that reduces an array to a single value by repetitively invoking a `reducer` function on each item in the array, and returns the final value.

The function signature should be:

```js
reduce(list, reducer, accumulator);
```

It should be able to reduce an array of numbers into a single summed up number (one use case of reduce):

```js
const numbers = [1, 2, 3];
const sum = reduce(numbers, function(total, number){
  return total + number;
}, 0);

console.log(sum);
//=> 6
```

Hints: 

- What parameters should the `reducer()` callback function have?
- Does your implementation rely on `reducer()` returning a value?
- Where does your previously implemented `each()` function fit in this?
- Write pseudo-code to layout your approach generally first before coding

Note: This is designed to test how well you understand callbacks and how to make use of them to solve real problems.



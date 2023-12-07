# JS API

## Level 1

### String

- length: returns the length of the string
- indexOf: returns the first index of the target in a string
- lastIndexOf: returns the last index of the target
- slice: takes two parameters start and end, return a string where start index is inclusive and end ending exclusive. **substr is deprecated, use slice instead**
- substring: same as slice, but differs slightly

  | slice                                                                                                                                                                   | substring                                                    |
  | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------------------------------------------------------- |
  | if start > stop returns empty string                                                                                                                                    | if start > stop, swaps start and stop and returns the string |
  | if start is negative, it is treated as NaN and returns empty string, if stop is negative, sets stop to `str.length - Math.abs(stop)` in such case the stop is inclusive | if either of start and stop is negative it is treated as 0   |

- replace: takes two argument, target and replacement, returns a replaced string.
- split: returns an array, split function takes one argument that is the separator. ex:

  ```
  let str = "Hello Javascript API";

  console.log(str.split(" ")) // ['Hello', 'Javascript', 'API']

  ```

- trim: The trim() method removes whitespace from both sides of a string.

- toUpperCase: UPPERCASE the string;

- toLowerCase: lowercase the string;

### Number

- parseInt: parses string argument into integer
- parseFloat: parses string argument into floating number

### Arrays

- push: push element at the end of array
- pop: pop element from end
- shift: pop first element
- unshift: put element at first, and returns new length of array
- concat: concatenates two array into a single array.
- forEach: iterates over array element
- map: iterates over array element and returns a new array
- filter: filters an array based on condition, and returns a newly filtered array
- reduce: iterates over array and returns a single value. (value can be a string, single object)
- find:
- sort:
- toSorted:

## Level 2

### topics

- class
- dates
- objects
- JSON
- Math

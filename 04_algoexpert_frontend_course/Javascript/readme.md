# Javascript

###  Multi-Paradigm Language

1. Event Driven: Respond to events
2. Functional: Pure Functions, first-class functions 
   - Same result for a given set of arguments
3. Object-oriented: Custom objects with inheritance
4. Imperative: Specify logic and control flow
5. Declarative: specify desired output

###  Javacript Engine

  - Executes code in the browser
  - Just-in-time compilation (or interepted)


##  Basics

###  Primitive Types
1. Number
2. Bigint
3. Boolean
4. String
5. null
6. undefined
7. Symbol(): newly introduced

###  Functions
1. typeof
2. instanceof

###  Number Functions
1. Number(): returns a **number** or **NaN**
2. perseInt(): gives the number in the string
3. parseFloat(): gives the float in the string
4. Strict Equality (== vs ===)

###  String Functions
1. padStart(no. of chars, "chars to replace the spaces with")
   - e.g. str.padStart(10, "-") => ------abcd
2. padEnd()
3. trim(), trimStart(), trimEnd(): remove all white spaces on start and end

###  Object Functions
1. new Map(): keys could be of any type rather than *string* or *symbol*
  - map.set()
  - map.get()
  - map.size
2. new Set(): only the unique values are there, no **keys**
   - set.add(value)
   - set.has(value)
   - set.size

###  First Class Functions
- A function which is treated like other variables.  

###  Loops
1. Break works in for, while
2. do-while loop
  ```
    let i = 0
    do {
      console.log(i)
      i++
    }
    while (i < 4)
  ```

###  Error Handling
1. throw
2. throw new Error

###  Console logging
1. console.log()
2. console.error()
3. console.debug()
4. console.table()
5. console.count()
6. console.countReset()
7. console.time()
8. console.timeLog()
9. console.timeEnd()
10. console.trace()


## Variables and Scoping

1. let (BlockScope), const, var (Function Scope)
2. **Hoisting**: process by which js engines moves variable declarations on the top of their scope, allocating memory for them when declared in code

  ```
    console.log(varNum) // undefined
    console.log(letNum) // reference Error

    var varNum = 5
    let letNum = 10
  ```

## Arrays

1. How to create an array of 1 to 100
   
  ```
    const arr = new Array(100).fill(0).map((e,i) => i+1)
  ```

2. Find the answer
  ```
    const arr = [1,2,3]
    arr.length = 1
    console.log("Array: ", arr)  // [1]
  ```

  ```
    const arr = [1,2,3,4,5]
    arr.fill(9,2,4) // fill(value, start, end)
    console.log("Array: ", arr)  // [ 1, 2, 9, 9, 5 ]
  ```

  ```
    const arr = [1,2,3]
    arr.splice(1,0,'hello', 'world')
    console.log("Array: ", arr)  // [1, 'hello', 'world', 2, 3]
  ```

  ```
    const arr = [1,2,3]
    arr.forEach(function (value, index) {
      console.log(value, index, this)
    }, {num: 10})  // defines extra arg as this

    /*
      1 0 { num: 10 }
      2 1 { num: 10 }
      3 2 { num: 10 }
    */
  ```

  ```
    const arr = [5,7,3,0]
    arr.sort(compareNumbers)

    function compareNumbers(fisrtNumber, secondNumber) {
      return firstNumber - secondNumber // sort asc [0,3,5,7]
      return secondNumber - firstNumber // sort desc [7,5,3,0]

      if (firstNumber === 3) return -1
      if (secondNumber === 3) return 1
      return firstNumber - secondNumber // [3,0,5,7]
    }
  ```

3. [Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
  - **unshift** same as push but at the beginning
  - **shift** same as pop but at the beginning
  - splice(start, deleteCount, item1, item2, /* …, */ itemN) // remove/replace elements from array from the range
  - slice(start, end): returns the shallow copy of the array
  - every() vs some(): returns a boolean (T/F) if condition is passing
  - reduce(): if last arg not defined, it skips the first iteration
  - reduceRight(): iterate from right side

4. Compare Array
  ```
    arr intanceof Array
    Array.isArray(arr)
  ```


## Objects

### How to put a const as key in object

```
  const myKey = 'key'
  const website = {
    [myKey]: '1234'
  }
  console.log("Website: ", website) // {key: 1234}
```


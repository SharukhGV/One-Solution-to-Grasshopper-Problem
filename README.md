# One Solution to Grasshopper Problem
### Link https://www.codewars.com/kata/55d24f55d7dd296eb9000030



### QUESTION: 


Write a program that finds the summation of every number from 1 to num. The number will always be a positive integer greater than 0.


Here is the Solution:
```javascript
var summation = function (num) {


  let initialSum = 0
 for(let i=1;i<=num; i++){
   initialSum+=i;
  }
  return initialSum
  }
```
Here is the Explanation for the Solution:

The empty function is given to us and we have to fill in the details about it. We know that num is the final number that 1 has to go up to / increment to in this loop, and all the numbers between it (inclusive) have to be added together.

We are using a for loop because it is designed to take a number and increment it by a certain amount (whether one or two or whatever) given certain conditions. 

We choose the conditions to be from `1` to `num` inclusive (hence we used the `<=` instead of just `<`)

*From GOOGLE: The dictionary definition of inclusive is simply something that doesn't leave any person, part or group out.*

This means in our problem, we are including `1` and `num` in the summation loop.

The Loop above is going to start at `i` being `1`, then it will increment `i` each time until `i` becomes equal to `num`. 

```javascript

 for(let i=1;i<=num; i++)

 //i=1 is the starting point of the loop

 //i<=num is saying that num should be where the loop stops at when i is equal to num.

 //i++ means that i will increase until it reaches and becomes num
  
```

So if `num` is equal to `5`, then the values of `i` will increase by `1` to be:

- `1`      ---> `i=1` the loop starts off
- `2`      ---> `i<=5`, where here it is equal to `2`
- `3`      ---> `i<=5`, where here it is equal to `3`
- `4`      ---> `i<=5`, where here it is equal to `4`
- `5`      ---> `i<=5`, where here it is equal to `5`

...and if `num` is equal to `12`, then the values of `i` will increase by `1` to be:

- `1`      ---> `i=1`  the loop starts off
- `2`      --> `i<=12`, where here it is equal to `2`
- `3`      ---> `i<=12`, where here it is equal to `3`
- `4`      ---> `i<=12`, where here it is equal to `4`
- `5`      ---> `i<=12`, where here it is equal to `5`
- `6`      ---> `i<=12`, where here it is equal to `6`
- `7`     ---> `i<=12`, where here it is equal to `7`
- `8`      ---> `i<=12`, where here it is equal to `8`
- `9`     ---> `i<=12`, where here it is equal to `9`
- `10`     ---> `i<=12`, where here it is equal to `10`
- `11`     ---> `i<=12`, where here it is equal to `11`
- `12`     ---> `i<=12`, where here it is equal to `12`

```javascript
var summation = function (num) {


  let initialSum = 0
 for(let i=1;i<=num; i++){
   initialSum+=i;
  }
  return initialSum
  }
```
We can see in th solution above that we have our for loop written out... but why do we have `initialsum = 0`?

Well, we need to add i to something initially, and that something has to be an unchanging/constant value that will not effect the summation loop. If you were to put 1 here, you will basically start off at 1 and add 1 to it again, and then 2, and 3, and so on until you reach num. This summation loop will return a value that is one greater than what it is supposed to be.

If you were to put 2 here, you will basically start off at 2 and add 1 to it again, and then 2, and 3, and so on until you reach num. This summation loop will return a value that is two greater than what it is supposed to be.

So, the best option is to let the starting number that you will add all the values of i to be 0, because it will not effect the end result of the summation loop.

We will then add that initialSum, which is 0, to i, and set it equal to that new value, and repeat until i is equal to num. So, here we have:

if the value of num is 5:

`initialSum = initialSum+1`, where `initialSum` equals `0` to begin with.

So what will `initialSum` be equal to after the above resolves? It will equal `1`, because `0+1` is equal to `1`.

**So we notice that initialSum is being reassigned a new value each time. We use `let` keyword for `initialSum` here because `const` keyword cannot be reassigned a new value. The only option is `let` or `var`. You may use either, but be careful with scope properties of each of these two keywords.**

Then we have:
`initialSum = initialSum+2`, where `initialSum` is equal to 1.
After adding `1` to `2`, `initialSum` now becomes equal to `3`.

This continues until we add all the value up and get the summation of 0+1+2+3+4+5. The result is 15.

To return the final result, you must return initialSum outside the bracket of the for loop. This is because the loop will loop through everything and when it finishes it will go to the next line of code. If it were located in inside the for loop brackets, it will tryt o return a value each time the loop iterates. 

*From Google: iterate means to perform or utter repeatedly.*

Try to edit the function in the index.js file to see how the for loop works.

I hope this helps. 








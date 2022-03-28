Define a function isFive that will return true if a number is equal to 5 and false if it is not.

```javascript
function isFive(num) {
  if (num === 5) {
    return true;
  }
  // we don't have to wrap this in an `else` because if the above code did *not*
  // run then the number can't be 5 so we can just return false!
  return false

console.log(isFive(5)); // => true
console.log(isFive(13)); // => false
```
Write a function isOdd that takes in a number as an argument and returns
true if the number is odd and returns false otherwise. 

Write two versions of this function, one using conditionals (if) and one without using
conditionals.

```javascript
function isOdd(number) {
  return (number % 2 !== 0);
}
// !== means not equal to not equal

function isOddConditional(number) {
  if (number % 2 !== 0) {
    return true;
  } else {
    return false;
  }
}

console.log(isOdd(2)); // => false
console.log(isOdd(5)); // => true
console.log(isOdd(-17)); // => true
```

Define a function logBetween(lowNum, highNum) that will print
every number from lowNum to highNum, inclusive. Inclusive means that the
range includes lowNum and highNum. 

Hint: this function only needs to
print using console.log it does not need to return.

```javascript
function logBetween(lowNum, highNum) {
  for (let i = lowNum; i <= highNum; i += 1) {
    console.log(i);
  }
}
// <= high num is greater then or = to 1, +=1 because the data has an index of zero 

function logBetweenWhile(lowNum, highNum) {
  let i = lowNum;
  while (i <= highNum) {
    console.log(i);
    i++;
  }
}

logBetween(-1, 2); // prints out:
// -1
// 0
// 1
// 2

logBetween(14, 6); // => prints nothing

logBetween(4, 6); // prints out:
// 4
// 5
// 6
```

Write a function printFives(max) that prints out the multiples
of 5 that are less than the max.

Try to solve this in two ways, one using
a conditional (if), and one without using a conditional. 

```javascript 
function printFives1For(max) {
  for (let i = 0; i < max; i += 1) {
    if (i % 5 === 0) {
      console.log(i);
    }
  }
}

// i % 5 === 0 means that it has to be a multiple of 5 if it has any remainds it does not log 

function printFives1(max) {
  let i = 0;
  while (i < max) {
    if (i % 5 === 0) {
      console.log(i);
    }
    i++;
  }
}

// i < max logs the unmbers in order. zdont forget to log the i++ or it will be infanate 

function printFives2(max) {
  for (let i = 0; i < max; i += 5) {
    console.log(i);
  }
}

// just like the code from the other example but the i += 5 makes it divisasble by 5 

function printFives2While(max) {
  let i = 0;
  while (i < max) {
    console.log(i);
    i += 5;
  }
}


printFives(20) // prints out:
// 0
// 5
// 10
// 15
```

Write a function logBetweenStepper(min, max, step) that takes
in 3 numbers as parameters. The function should print out numbers between min
and max at step intervals. See the following examples. 

Hint: this
function only needs to print using console.log it does not need to return.

```javascript
function logBetweenStepperFor(min, max, step) {
  for (let i = min; i <= max; i += step) {
    console.log(i);
  }
}

function logBetweenStepper(min, max, step) {
  let i = min;
  while (i <= max) {
    console.log(i);
    i += step;
  }
}

logBetweenStepper(5, 9, 1); // prints out:
// 5
// 6
// 7
// 8
// 9


logBetweenStepper(-10, 15, 5)  // prints out:
// -10
// -5
// 0
// 5
// 10
// 15
```

Write a function threeOrSeven that takes in a number and
returns true if the number is divisible by either 3 or 7 and false
otherwise. 

Write two versions of this function, one using conditionals
(if), and one without using conditionals. 
```javascript
function threeOrSeven(number) {
  return (number % 7 === 0) || (number % 3 === 0);
}

// || is the or function ( only evaluate to false when both input values are false )

function threeOrSevenConditional(number) {
  if ((number % 7 === 0) || (number % 3 === 0)) {
    return true;
  } else {
    return false;
  }
}

console.log(threeOrSeven(3));   // => true
console.log(threeOrSeven(42));  // => true
console.log(threeOrSeven(8));   // => fals
```

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

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

Write a function sumArray(array) that takes in an array of numbers and returns the total sum of all the numbers.

```javascript
function sumArray(array) {
  let sum = 0;
  
  // letting 0 be the starting point 

  for (let i = 0; i < array.length; i += 1) {
    let num = array[i];
    sum += num;
  }

// 
  return sum;
}



console.log(sumArray([5, 6, 4])); // => 15
console.log(sumArray([7, 3, 9, 11])); // => 30
```

Write a function combineArray(array1, array2) that takes in two arrays of numbers and returns the two arrays combined into a single array. 

Hint: Use the Array.concat method but be aware that calling this method won't permanently change, also known as mutate, either array. 

```javascript
function combineArray(array1, array2) {
  let newArray = array1.concat(array2);
  return newArray;
}

// .concaat to aadd the two arrays together 

console.log(combineArray([1, 2], [3, 4])); // => [1, 2, 3, 4]
console.log(combineArray([17, 5], [6, 7]));  // => [17, 5, 6, 7]
```
Write a function doubler(numbers) that takes an array of numbers and returns a new array
where every element of the original array is multiplied by 2.

```javascript
function doubler(numbers) {
  let doubledNums = [];

  let i = 0;
  while (i < numbers.length) {
    let oldNum = numbers[i];
    let newNum = oldNum * 2;
    // this step is important because concat does NOT change the original array
    doubledNums = doubledNums.concat(newNum);

    i += 1;
  }

  return doubledNums;
}

console.log(doubler([1, 2, 3, 4])); // => [2, 4, 6, 8]
console.log(doubler([7, 1, 8])); // => [14, 2, 16]
```
___
## Vowel Counter
 Write a function, countVowels(word), that takes in a string
word and returns the number of vowels in the word. 
Vowels are the letters
"a", "e", "i", "o", "u". 

``` Javascript 
// 1. set a vowelCounter variable
// iterate through the incoming word
//checking weather the current letter is a vowel
//increment the vowelCounter vowel if the current letter is a vowel

function countVowels(word) {
    let vowelCounter = 0;
    let index = 0;

    while (index < word.length) {
        let letter = word[index];

        if (letter === "a" ||
            letter === "e" ||
            letter === "i" ||
            letter === "o" ||
            letter === "u") {
            vowelCounter += 1;
        }
        index++;

    }
    return vowelCounter
}

console.log(countVowels("bootcamp")); // => 3
console.log(countVowels("apple")); // => 2
console.log(countVowels("pizza")); // => 2
```

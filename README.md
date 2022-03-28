# Java Script 
This logs whatever text or number so you can see it:
```javascript 
console.log("Hello world")
```
___
### Numbers (subtraction. addition, etc)
```javascript 
+
-
/
-
% // Also reffered to as "Mod"
```
```javascript 
(22%5) 
//> 2 This is becuase 5 is only goes into 20 4 times and the remainder is 2
```
___
### Boolin Expressions 
* ! (not) - will reverse a boolean value
* && (and) - will take two boolean values and will only evaluate to true when both input values are true
* || (or) -  operator will take two boolean values and will only evaluate to false when both input values are false

```javascript 
console.log(!true); // => false
console.log(true && false); // => false
console.log(true || false); // => true
```
#### De Morgan's Law

!(A || B) is equivalent to !A && !B

!(A && B) is equivalent to !A || !B

___

### Initializing a variable

To initialize a variable in JavaScript we'll need two new pieces of syntax: 

##### let and =

```javascript
let bootcamp = "App Academy";
console.log(bootcamp); // 'App Academy'

let birthYear = 2012;
console.log(birthYear); // 2012
```

#### Assignment Shorthand
 
 
```javascript
let number = 0;
number += 10; // equivalent to number = number + 10
number -= 2; // equivalent to number = number - 2
number /= 4; // equivalent to number = number / 4
number *= 7; // equivalent to number = number * 7
console.log(number); // 14

let year = 3004;
year++;
console.log(year); // 3005
year--;
console.log(year); // 3004
```
___
## Functions
##### a set of code that will run when called

```javascript
// Function definition
function average(number1, number2) {
  return (number1 + number2) / 2;
}

// This function call passes the arguments 10 and 16.
average(10, 16)  // Returns 13

// Have to consol.log if you want it to print 
console.log(average(10,16))


function sayNumber(number) {
  console.log(number);
  return true;
}

sayNumber(1);   // Prints 1 and returns true
```

```javascript
function add(firstParameter, secondParameter) {
  console.log(firstParameter + secondParameter);
}

// the add function declares two parameters
> add(1, 2); //=> 3
```
Adding sapaces 

```javascript
function echo(string) {
  console.log(string.toUpperCase() + " ... " + string + " ... " + string.toLowerCase()) 
}

// The space after the "... " adds a space 

echo("Mom!"); // => prints "MOM! ... Mom! ... mom!"
echo("hey"); // => prints "HEY ... hey ... hey"
echo("JUMp"); // => prints "JUMP ... JUMp ... jump"
```
___
### Conditionals

* if 
* else if 
* else 
```javascript
function mathFun() {
  let x = 19;
  if (x === 3) {
    console.log("we have a 3");
}
//We can only use if once.    
    
    else if (x === 4) {
    console.log("we have a 4");
} 
// We can use else if as many times a we want. 
    else {
    console.log("I will return if everything above me is falsey!");
  }
};

//We can only use else once. 

//Pay attention to the syntax of the {}

mathFun(); // => "I will return if everything above me is falsey!"
```
___

### Loops 

#### While 

```javascript 
let index = 0;

// Index always has to be 0 

// this is the condition that will be checked every time this loop is run
while (index < 10) {
  console.log("The number is " + index);
  // this is common shorthand for index = index + 1
  index++;
// Have to add the index++ or it wont work if using an while statement 
```
#### For 

```javascript
for (<initial expression>;<condition>;<loopEnd expression>)
```
```javascript
let testString = "testing";

// We can use the testString's length as our condition!
// Since we know the testString's index starts at 0
// and our index starts at 0 we can access each letter:
for (let index = 0; index < testString.length; index += 1) {
  let letter = testString[index];
  console.log(letter);
}
``` 
___

### Array's

a data type that contains a list of in order values surrounded by square brackets []

array.length showds the arrays length 

* .concat - combines 2 arrays 

```javascript
console.log([1, 2, 3].concat([4, 5, 6])); // => [1, 2, 3, 4, 5, 6]
```
* Array.push(item) - Add
* Array.pop() - Removes 

```javascript
let arr = [1, 2, 3];
arr.push(4);
arr.push(5);
console.log(arr);   // => [1, 2, 3, 4, 5]
arr.pop();
console.log(arr);   // => [1, 2, 3, 4]
```

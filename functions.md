# Functions
**Functions** package up code so you can easily use (and reuse) a block of code. 
**Parameters** are variables that are used to store the data that's passed into a function for the function to use. 
**Arguments** are the actual data that's passed into a function when it is invoked:
```js 
! A function's return value can be stored in a variable or reused throughout your program as a function argument
```
## return & console.log
It’s important to understand that using **return** in a function is different from using **console.log.**
**console.log:**

```js
const sayHelloToConsole  = function (name) {
  console.log("Hello, " + name);
}
sayHelloToConsole('John'); ```
 						// It’s immediately outputs 'Hello, John' to the console.
```
**return:**
```js
const returnSayHello  = function (name) {
  return "Hello, " + name;
}
const greeting = returnSayHello('John’);	// Returns the string 'Hello, John' to a variable and nothing will get output to the console.
```
A **console.log** statement will result in some content being displayed in the console. 
A **return** statement will **not** output anything to the console. 
However, when a function returns a value, we can still console.log it later:
```js
const returnSayHello  = function (name) {
  return "Hello, " + name;
}
const greeting = returnSayHello('John');
console.log(greeting); ```
```
e.g
```js
								
function add(x, y) {				// x and y are parameters in this function declaration
 var sum = x + y;			        // function body (all inside {})
  return sum; 					// return statement
}
var sum = add(1, 2);			        //<—You invoke or call a function to have it do something (add(1,2))
						// 1 and 2 are passed into the function as arguments

```
e.g
```js
function sayHi(name) {
  var greeting = "Hello";
  console.log(greeting + " " + name);
}

sayHi("Julia");					//Output  Hello Julia
```

e.g
```js
function laugh(num) {
    var str = "";
    for(var i = 1; i <= num; i++) {
          str = str + "ha"; 
    }
    str = str + "!"; 
    return str;
}
console.log(laugh(3));  			// Output hahaha!

```
e.g
```js
function sayHello(name) {			//Declared the function with parameter - name
  console.log("Hello, " + name);
}

sayHello("Caliban");				// Call the function three times
sayHello("Miranda");
sayHello("Ferdinand");						
						//Output Caliban
							 Miranda
							 Ferdinand

```
### isEven function

**isEven** takes as its parameter a number and returns a Boolean value representing whether or not the number is even.
In the above isEven function, num can vary and therefore so will the result of num % 2 === 0. 
If num is even, the result of num % 2 is 0 and so the whole expression evaluates to *true*. 
The opposite happens when num is odd.

```js
const isEven  = function (num) {
  return num % 2 === 0;
}

console.log(isEven(10));			//*Output  True; False
console.log(isEven(11));							           
							
```

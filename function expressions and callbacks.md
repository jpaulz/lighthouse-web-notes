# Function Expressions and callbacks
In js you can store functions in variables.\
When a function is stored inside a variable it’s called a **function expression.**

```js
            var catSays = function(max) {
            var catMessage = "";
            for (var i = 0; i < max; i++) {
                catMessage += "meow ";
             }
                return catMessage;
            };
```

## anonymous function expression
The example of the function below has no name, it’s stored in a variable (favoriteMovie).\
This type of function is called **anonymous functions.** It’s stored in a variable and **to call it you need to use the variable’s name.**
```js
            var favoriteMovie = function() {	// Function has no name —> Anonymous function
	        return “The Fountain”;
            };

            favoriteMovie();    // Calling the function by using variable name, it will return “The Fountain”
```
## named function expression
This function has name (addOne) and this function is stored in a variable.
```js
            var doSomething = function addOne(y) {
                return y + 1;
            };

            doSomething(5);		// Calling the function by using variable name, and it returns 6
```
**! Remember, to call the function (for both cases function with name or anonymous function) by the name of variable, not the name of function.**

! All *function declarations* are hoisted and loaded before the script is actually run.\
 *Function expressions* are not hoisted, since they involve variable assignment, and only variable declarations are hoisted.

# Callback
Being able to store a function in a variable makes it really simple to pass the function into another function.\
A function that is passed into another function is called a **callback.** 

```js
            // function expression catSays
            var catSays = function(max) {
            var catMessage = "";
            for (var i = 0; i < max; i++) {
                catMessage += "meow ";
            }
            return catMessage;
            };

            // function declaration helloCat accepting a callback
            function helloCat(callbackFunc) {
            return "Hello " + callbackFunc(3);
            }

            // pass in catSays as a callback function
            helloCat(catSays);
```

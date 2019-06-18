# Array
An array stores multiple values into a single, organized data structure. \
You can define a new array by listing values separated with commas between square brackets [].\
In array can be stored strings, numbers, booleans… and really anything!

**Array of strings**
 ```js
            // creates a `donuts` array with three strings
            var donuts = ["glazed", "powdered", "jelly"];
```
**Array of mixed data**
```js
            // creates a `mixedData` array with mixed data types
            var mixedData = ["abcd", 1, true, undefined, null, "all the things"];
```
**Array of variables**
```js
            var captain = "Mal";
            var second = "Zoe";
            var pilot = "Wash";
            var companion = "Inara";
            var mercenary = "Jayne";
            var mechanic = "Kaylee";

            var crew = [captain, second, pilot, companion, mercenary, mechanic];
            console.log(crew);   // Output will be [ 'Mal', 'Zoe', 'Wash', 'Inara', 'Jayne', 'Kaylee' ]
```

**Nested array** - an array in an array 
```js
            // creates a `arraysInArrays` array with three arrays
            var arraysInArrays = [[1, 2, 3], ["Julia", "James"], [true, false, true, false]];
```

Nested arrays can be particularly hard to read, so it's common to write them on one line, using a newline after each comma:
```js
            var arraysInArrays = [
              [1, 2, 3], 
              ["Julia", "James"], 
              [true, false, true, false]
            ];
```
## Accessing Array Elements
Each element of the array can be accessed **by its index**.\
Elements in an array are indexed starting at the position 0.\
To access an element in an array, use the name of the array immediately followed by square brackets containing the index of the value you want to access.
```js
            var donuts = ["glazed", "powdered", "sprinkled"];
            console.log(donuts[0]); // "glazed" is the first element in the `donuts` array
```

! If you try to access an element at an index that does not exist, a value of undefined will be returned back.
```js
            console.log(donuts[3]); // the fourth element in `donuts` array does not exist! - it will printed out to console - undefined
```

## Changing the Value  of an Element in Array
To change the value of an element in array, you need to set it equal to a new value by index:
```js
            var donuts = ["glazed", "powdered", "sprinkled"];
            donuts[1] = "glazed cruller"; // changes the second element in the `donuts` array to "glazed cruller"
            console.log(donuts[1]); 
```

# Array properties and Methods
[List of all the available Array methods.](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)

## Array.length
Can be found by using array’s **length** property.\
To access the length property, type the name of the array, followed by a period . (you’ll also use the period to access other properties and methods), and the word length. \
The length property will then return the **number of elements** in the array.

```js
			var donuts = ["glazed", "powdered", "sprinkled"];
			console.log(donuts.length);	// Output - 3  		
```
## push() and pop() methods to modify an array
**Push**\
You can use **push()** method **to add elements to the end of an array**.\
Also, the push() method returns the length of the array after an element has been added.

```js
			var donuts = ["glazed", "chocolate frosted", "Boston creme", "glazed cruller", "cinnamon sugar", "sprinkled"];
			donuts.push("powdered");	// pushes "powdered" onto the end of the `donuts` array
			/* Output will be 7  (donuts array: ["glazed", "chocolate frosted", "Boston creme", "glazed cruller", "cinnamon 			sugar", "sprinkled", "powdered”])*/
```
**Pop**\
You can use the **pop()** method **to remove elements from the end of an array**.
With the pop() method you don’t need to pass a value; instead, **pop() will always remove the last element from the end** of the array.\
Also, pop() returns the element that has been removed in case you need to use it.

```js
			var donuts = ["glazed", "chocolate frosted", "Boston creme", "glazed cruller", "cinnamon sugar", "sprinkled", 				"powdered"];

			donuts.pop();	// pops "powdered" off the end of the `donuts` array
			donuts.pop();	// pops "sprinkled" off the end of the `donuts` array
			donuts.pop();	// pops "cinnamon sugar" off the end of the `donuts` array
			
			/* Output will be "cinnamon sugar"  - the last removed element 	and the array after that will be (donuts 				array: ["glazed", "chocolate frosted", "Boston creme", "glazed cruller”])*/
```
## Splice

splice() is another handy method that allows you to add and remove elements from anywhere within an array.\
While push() and pop() limit you to adding and removing elements from the end of an array,\
 **splice() lets you specify the index location to add new elements, as well as the number of elements you'd like to delete (if any)**.

- The first argument represents the starting index from where you want to change the array,\
- the second argument represents how many elements you want to remove,\
-  and the remaining arguments represent the elements you want to add.
```js
			var donuts = ["glazed", "chocolate frosted", "Boston creme", "glazed cruller"];
			donuts.splice(1, 1, "chocolate cruller", "creme de leche"); 
			// removes "chocolate frosted" at index 1 and adds "chocolate cruller" and "creme de leche" starting at index 1
			/*Output will be  ["chocolate frosted"]
			and the array after that will be donuts array: ["glazed", "chocolate cruller", "creme de leche", "Boston creme", 			"glazed cruller"]*/
```
**Splice with negative index number**
If there are splice with negative index number:\
- The first argument(negative number), which represents the starting of the array. You count  from right to left starting counting with -1 (not 0)\
- The second argument (number) represents how many elements you want to remove
- remaining arguments are elements you add on that spot

```js
			var donuts = ["cookies", "cinnamon sugar", "creme de leche"];

			donuts.splice(-2, 0, "chocolate frosted", "glazed");
			//and the array after that will be [“cookies", "chocolate frosted", "glazed”, ”cinnamon sugar", "creme de leche”];





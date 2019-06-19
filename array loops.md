# Array Loops
To loop through an array, you can use a variable to represent the index in the array,\
 and then loop over that index to perform whatever manipulations you want.
```js
			var donuts = ["jelly donut", "chocolate donut", "glazed donut"];

			// the variable `i` is used to step through each element in the array
			for (var i = 0; i < donuts.length; i++) {
			    donuts[i] += " hole";
    			    donuts[i] = donuts[i].toUpperCase();
			}
			// The result will be donuts array: ["JELLY DONUT HOLE", "CHOCOLATE DONUT HOLE", "GLAZED DONUT HOLE"]
```
In this example, the variable i is being used to represent the index of the array.\
As i is incremented, you are stepping over each element in the array starting from 0 until donuts.length - 1 (donuts.length is out of bounds).

## The forEach() loop
The forEach() method gives you an alternative way to iterate over an array, \
and manipulate each element in the array with an inline function expression.

```js
			var donuts = ["jelly donut", "chocolate donut", "glazed donut"];

			donuts.forEach(function(donut) {
  			donut += " hole";
  			donut = donut.toUpperCase();
  			console.log(donut);
			});			/* Output will be 
						JELLY DONUT HOLE
						CHOCOLATE DONUT HOLE
						GLAZED DONUT HOLE*/
```
That how it would be done with the for loop 
```js
			var donuts = ["jelly donut", "chocolate donut", "glazed donut"];

			for (var i = 0; i < donuts.length; i++) {
  			donuts[i] += " hole";
  			donuts[i] = donuts[i].toUpperCase();
  			console.log(donuts[i]);
			}
```

- The function that you pass to the forEach() method can take **up to three parameters** (element, index and all(the whole array)).
- The forEach() method will call this function once for each element in the array (hence the name forEach.) 
- Each time, it will call the function with different arguments. 
- The element parameter will get the *value* of the array element.
- The index parameter will get the *index* of the element (starting with zero).
-  The array parameter will get a reference to the whole array, which is handy if you want to modify the elements.
```js				  
				  0      1      2     //Indexes of elements
			words = ["cat", "in", "hat"];  // cat, in, hat - elements
			words.forEach(function(word, num, all) {
  			console.log("Word " + num + " in " + all.toString() + " is " + word);
			});
						/*Output will be Word 0 in cat,in,hat is cat 
								 Word 1 in cat,in,hat is in 														Word 2 in cat,in,hat is hat*/
```
## Map
With the map() method, you can take an array, perform some operation on each element of the array, and return a new array.
- The map() method accepts one argument, which has to be a function that will be used to manipulate each element in the array. The function can have up to three arguments (element, index, and the whole array).
- In the example below, used a function expression to pass that function into map(). 
- This function is taking in one argument, *donut* which corresponds to each element in the donuts array.
- You no longer need to iterate over the indices anymore. map() does all that work for you.
- Remeber to **return** 
```js
			var donuts = ["jelly donut", "chocolate donut", "glazed donut"];

			var improvedDonuts = donuts.map(function(donut) {
 			 donut += " hole";
 			 donut = donut.toUpperCase();
 			 return donut;
			});
				/*donuts array: ["jelly donut", "chocolate donut", "glazed donut"]
				improvedDonuts array: ["JELLY DONUT HOLE", "CHOCOLATE DONUT HOLE", "GLAZED DONUT HOLE"]*/
```
map() method examople
```js
			var bills = [50.23, 19.12, 34.01,100.11, 12.15, 9.90, 29.11, 12.99,10.00, 99.22, 102.20, 100.10, 6.77, 2.22];
   				 
    			var totals = bills.map(function(num) {
 			 num += num * 0.15;		//calculating 15% and adding it to num
 			 num = num.toFixed(2);		// num.toFixed() - rounding the values to a maximum of 2 decimal places
 		     	 num = Number(num);		//Number() - converting string to number
 		     	 return num;
            
			});
			console.log(totals); //Output [ 57.76,21.99, 39.11,...2.55 ]
  
 
  

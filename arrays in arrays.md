# Arrays in Arrays (Nested arrays)
Syntax:
```js
			var donutBox = [     // first array
  			["glazed", "chocolate glazed", "cinnamon"],  //second array
  			["powdered", "sprinkled", "glazed cruller"],
  			["chocolate cruller", "Boston creme", "creme de leche"]
			];

To loop over the donut box and display each donut (along with its position in the box!):
1. Start with writing a for loop to loop over each **row** of the box of donuts
2. Next need to set up an inner-loop to loop over each **cell** in the arrays.
```js			
            for (var row = 0; row < donutBox.length; row++) {   // for loop for each row
			/* here, donutBox[row].length refers to the length of 
                        the donut array currently being looped over*/
  
			for (var column = 0; column < donutBox[row].length; column++) {  //for loop for each cell
    			console.log(donutBox[row][column]);
  			}
			}
				/* Output   	"glazed"
						"chocolate glazed"
						"cinnamon"
						"powdered"
						"sprinkled"
						"glazed cruller"
						"chocolate cruller"
						"Boston creme"
						"creme de leche”*/
```
```js
			var numbers = [
  			[243, 12, 23, 12, 45, 45, 78, 66, 223, 3],
    			[34, 2, 1, 553, 23, 4, 66, 23, 4, 55],
    
			];

			for (var row = 0; row < numbers.length; row++) {   // for loop for each row
  
			for (var column = 0; column < numbers[column].length; column++) {    //for loop for each column

			if (numbers[row][column] % 2 === 0) {
    			numbers[row][column] = "even";    		// ! don't console.log (it will just print to console and not/ 				change the array), instead you need to replace the numbers with a string by assigning the value
			} else {
    			numbers[row][column] = "odd";     //replacing the numbers with a string
			}
			console.log(numbers[row][column]);
			}

			}
```

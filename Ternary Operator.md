# ternary operator
The ternary operator provides you with a shortcut alternative for writing lengthy **if...else** statements:

**conditional ? (if condition is true) : (if condition is false)**

To use the ternary operator:
 1. Provide a conditional statement on the left-side of the ?. 
 2. Then, between the ? and : write the code that would run if the condition is true.
 3. On the right-hand side of the : write the code that would run if the condition is false. 

e.g one
```js
	var isGoing = true;
	var color = isGoing ? "green" : "red";
		console.log(color);
                       			 // Output “green" 
                        
```

e.g two

```js
	var adult = true;
	var preorder = true;
		console.log("It costs $" + (adult ? "40.00" : "20.00") + " to attend the concert. Pick up your tickets at the " + (preorder ? "will call" : "gate") + ".";
					// Output - “It costs 40$ to attend the concert. Pick up your tickets at the will call.”
```
e.g three
```js
			  1	   2
	var eatsPlants = true;	  false
	var eatsAnimals = false;  true
	var category = eatsPlants ? (eatsAnimals ? "omnivore" : "herbivore") : (eatsAnimals ? "carnivore" : undefined);
		console.log(category); 
					 1 // Output “herbivore”
					 2// Output  “carnivore”




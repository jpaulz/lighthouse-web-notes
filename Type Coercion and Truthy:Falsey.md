# Double Equals, Triple Equals, and Type Coercion in js

## Operators to compare values
**===** operator to compare two values & the type of those values Ex. 23 === “23” will return **_False_** because of different values\
**==** operator will attempt to force the two values to be the same(it calls **_type coercion_**)\
Ex. 23 == “23” will return **_True_**

 ``! It's better to use triple equals **===** in almost every case, type coercion can sometimes produce unexpected results in your code.
``
## Not Equal
**!==** operator to check that two values are not equal\
**!=** operator will force type coercion the same as **==** before comparing the two values
  
 `` ! It's almost always better to use !== in order to avoid any accidental type coercion in your code``

## Truthy & Falsey
Comparing two values in JavaScript will return either true or false.\
But there are some exceptions in JavaScript, for ex. using ==, the correct response will be the opposite of expected.

E.g.  **0 == false**
( == will try to force a type coercion even though they are different type Boolean and Number.\
In JavaScript, everything has an inherent Boolean value, which is refered to as a **_Truthy or Falsey value_**.\
Even though 0 is a Number, it also holds a Falsey value.

In JavaScript most things are considered Truthy, except for the following:
```javascript
// All of the following are inherently falsey:

False         // False is False. Makes sense, right?
0             // 0 is the only falsey Number
""            // an empty string is falsey
null          // a null, or empty value, is falsey.
undefined     // an object that has not been defined is considered falsey.
NaN           // Not a Number. You'll learn more about NaN as we go on. ```

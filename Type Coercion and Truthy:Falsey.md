#Double Equals, Triple Equals, and Type Coercion in js

##Operators to compare values
**===** - operator to compare two values & the type of those values Ex. 23 === “23” will return **_False because of different values_**

**==** -  operator will attempt to force the two values to be the same(it calls **_type coercion_**)
Ex. 23 == “23” will return **_True_**

! It's better to use triple equals **===** in almost every case, type coercion can sometimes produce unexpected results in your code.
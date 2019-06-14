# Switch Statement
A **switch statement** is an another way to chain multiple **else if** statements that are based on the same value without using conditional statements. Instead, you just switch which piece of code is executed based on a value.

The **break statement** can be used to terminate a switch statement and transfer control to the code following the terminated statement.\ By adding a break to each case clause, you fix the issue of the switch statement falling-through to other case clauses.

E.g
```js
var education = "a Doctoral degree";
var salary = "$84,396";

switch (education) {
    case "no high school diploma":
        salary = "$25,636";
      console.log("In 2015, a person with " + education + " earned an average of " + salary.toLocaleString("en-US") + "/year.");
    break;
    case "a high school diploma":
        salary = "$35,256";
      console.log("In 2015, a person with " + education + " earned an average of " + salary.toLocaleString("en-US") + "/year.");
    break;
    case "an Associate's degree":
        salary = "$41,496";
        console.log("In 2015, a person with " + education + " earned an average of " + salary.toLocaleString("en-US") + "/year.");
    break;
    case "a Bachelor's degree":
        salary = "$59,124";
        console.log("In 2015, a person with " + education + " earned an average of " + salary.toLocaleString("en-US") + "/year.");
    break;
    case "a Master's degree":
        salary = "$69,732";
        console.log("In 2015, a person with " + education + " earned an average of " + salary.toLocaleString("en-US") + "/year.");
    break;
    case "a Professional degree":
         salary = "$89,960";
        console.log("In 2015, a person with " + education + " earned an average of " + salary.toLocaleString("en-US") + "/year.");
    break;
    case "a Doctoral degree":
        salary = "$84,396";
        console.log("In 2015, a person with " + education + " earned an average of " + salary.toLocaleString("en-US") + "/year.");
}
    
   //  or to make code shorter take console.log outside the code (outside curly brackets)


var education = "a Doctoral degree";
var salary = "$84,396";

switch (education) {
    case "no high school diploma":
        salary = "$25,636";
    break;
    case "a high school diploma":
        salary = "$35,256";
    break;
    case "an Associate's degree":
        salary = "$41,496";
    break;
    case "a Bachelor's degree":
        salary = "$59,124";
    break;
    case "a Master's degree":
        salary = "$69,732";
    break;
    case "a Professional degree":
         salary = "$89,960";
    break;
    case "a Doctoral degree":
        salary = "$84,396";
}
    console.log("In 2015, a person with " + education + " earned an average of " + salary.toLocaleString("en-US") + "/year.");
    
    
    

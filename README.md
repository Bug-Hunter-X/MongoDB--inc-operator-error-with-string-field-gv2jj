# MongoDB $inc operator error with string field

This repository demonstrates an example of an uncommon error in MongoDB related to the incorrect usage of the `$inc` operator. The `$inc` operator is used to increment numeric fields, but attempting to increment a string field leads to an error.

## Bug
The `bug.js` file contains code that attempts to increment a string field using the `$inc` operator. This results in a MongoDB error because the `$inc` operator only works with numeric fields. 

## Solution
The `bugSolution.js` file provides a corrected version of the code. It first converts the string field to a number and then uses the `$inc` operator to increment the numerical value.  Alternatively, if the field is intended to remain a string, a different update strategy (like appending to the string) should be used instead of $inc.
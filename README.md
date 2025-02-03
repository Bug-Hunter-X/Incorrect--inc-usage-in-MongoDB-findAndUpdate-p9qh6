# MongoDB findAndUpdate with $inc operator
This repository demonstrates an uncommon error when using the `$inc` operator within a MongoDB `findOneAndUpdate` operation. The error arises from providing a string value instead of a number to the `$inc` operator, leading to unexpected behavior.

## Bug
The original code attempts to increment the `count` field by '1', a string. This results in an incorrect update or an error, depending on the MongoDB version.

## Solution
The solution involves correcting the data type provided to the `$inc` operator. The value should be a number (e.g., 1).
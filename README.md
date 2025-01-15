# MongoDB $inc Operator Bug
This repository demonstrates a common error when using the `$inc` operator in MongoDB update queries.  The `$inc` operator is used to increment a numeric field by a specified value.  However, providing a string value instead of a number will lead to unexpected results and potential data corruption.

## Bug Description
The bug arises from using a string ('1') instead of a number (1) with the `$inc` operator in a MongoDB update query. This will cause the update operation to fail silently or produce an unintended result.

## Solution
The solution involves ensuring the value passed to `$inc` is always a valid number.
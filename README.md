# MongoDB updateOne: Silent Data Corruption with Type Mismatch in $set

This repository demonstrates a potential issue with MongoDB's `updateOne` method when using the `$set` operator and encountering type mismatches.  The bug arises when attempting to update a field with a value of a different datatype than expected.  This can lead to either an error or, more insidiously, a silent failure, resulting in data corruption.

The `bug.js` file contains the problematic code, while `bugSolution.js` offers a solution to prevent this kind of issue. This silent failure is hard to debug unless you meticulously check for every data type.
# Array Operators

JS has built in array operators. Allows you to modify and operate on the data.

## forEach
the `forEach` operator allows you to do something to each item in the array.
Takes in a callback function.

```
let numbers = [1,2,3,4,5];
numbers.forEach((item, index, array)=>{
	console.log(item) // 1, 2, 3, 4, 5
	console.log(index) // 0, 1, 2, 3, 4
	console.log(array) //[1,2,3,4,5], [1,2,3,4,5], [1,2,3,4,5], [1,2,3,4,5], [1,2,3,4,5]
	})


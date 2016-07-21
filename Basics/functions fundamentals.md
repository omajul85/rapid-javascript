### Functions fundamentals

* The code below shows a function declaration and execution:

```js
function printOrder() {
	console.log(‘Printing order.’);
};

printOrder(); //Prints 'Printing order.'
```
* You can call functions that are defined after (hoisting):

```js
printOrder(‘9002’);
	function printOrder(orderId) {

console.log(‘Printing order: ’ + orderId);
};
```

* Use the `return` keyword to get information out of a function:

```js
function calcTotalPrice(quantity, price){
	return quantity * price;
};

var totalPrice = calcTotalPrice(2, 4.00);
console.log(totalPrice); // 8
```

* If a function does not return a value, by default it assigns `undefined`.

* JS accepts functions expressions (very common usage):

```js
var activateOrder = function() {
	console.log(‘Order activated.’);
};

console.log(typeof activateOrder); // function
activateOrder(); // Order activated.
```

* 
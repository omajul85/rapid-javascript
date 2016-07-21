### Conditions and Loops

* if:

```js
var total = 99.99;
var freeShipping;
var savings;
if (total >= 100.00) {
	freeShipping = true;
	savings = 29.99;
}
else {
	freeShipping = false;
	savings = 0;
}

console.log(savings); // O
```

* switch

```js
var orderType = 'business';
var shipMethod;

switch (orderType) {
	case 'business':
		shipMethod = 'FedEx';
		break;
	case 'personal':
		shipMethod = 'UPS Ground';
		break;
	default:
		shipMethod = 'USPS';
}

console.log(shipMethod); // FedEx
```

* The example below is unique to JS:

```js
var orderTotal = 99.99;
var discount;
switch (true) {
	case orderTotal >= 50 && orderTotal < 75:
		discount = 10;
		break;
	case orderTotal >= 75 && orderTotal < 100:
		discount = 20;
		break;
	case orderTotal >= 100:
		discount = 30;
		break;
	default:
		discount = 0;
}

console.log(discount); // 20
```

* for

```js
var lineItemCount = 5;
for (var i = 0; i < lineItemCount; i++) {
	console.log(i);
	if (i == 1)
		break;
}

// Prints 0 1
```

```js
var lineItemCount = 5;
for (var i = 0; i < lineItemCount; i++) {
	if (i == 1)
		continue;   // This skips 1
	console.log(i);
}

// Prints 0 2 3 4
```

* for in syntax:

```js
var lineItem = {
	product: "Widget 1",
	quantity: 4,
	price: 9.50
};

for (var field in lineItem)
	console.log(field + " : " + lineItem[field]);

// product : Widget 1
// quantity : 4
// price : 9.50
```
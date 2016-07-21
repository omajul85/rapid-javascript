### if and switch

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
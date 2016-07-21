### Variables

* In JS the variables are dynamically typed (not recommended to do so):

```js
var orderId = "ORD-9001";
orderId = 1201;
console.log(orderId);
```

* `strict mode;` was created to handle the bug of JS creating global variables for us. We need to type *var* in order to define a variable; otherwise (in strict mode), there will be a RUNTIME ERROR.

* JS sees both 4 and 4.0 as a `number`. You can check the type using:

```js
var orderId = 9001.01;
console.log(typeof orderId);
```

* The type of an uninitialized variable is `undefined`.

* The type of an array is `object`. 

* The type of avariable initialized to `null` is `object`. It can be seen as an object with no methods nor attributes.

* There is a type called function (for functions).


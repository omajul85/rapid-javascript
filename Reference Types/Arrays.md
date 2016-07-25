### Arrays

* Creating an array using `new`:

```js
var entries = new Array('Trains', 'Plains', 'Automobiles');
console.log(entries instanceof Array); // true
```

* It is totally valid to use different types within an array:

```js
var entries = new Array('Trains', 1, true, 'Automobiles');
console.log(entries instanceof Array); // true
```

* Creating an array using `[]`:

```js
var entries = ['Trains', 'Plains',
'Automobiles'];
console.log(entries instanceof Array); // true
```

* We can predefine the size of the array:

```js
ary = Array(5) //[undefined × 5]
```

* The length of an empty array is 0.

* We can modify the size of the array by changing its property length:

```js
var entries = ['Planes', 'Trains'];
entries.length = 10;
console.log(entries.length); // 10 (the other 8 elements are undefined)
```

* JS expands the size of the array if we define an element outside its boundaries:

```js
var entries = ['Planes', 'Trains',
'Automobiles'];
entries[42] = 'Cars';
console.log(entries[42]); // 'Cars'
console.log(entries.length); // 43
```
* Create a comma separated list from an array using `toString()`:

```js
var entries = ['Planes', 'Trains',
'Automobiles'];
console.log(entries.toString()); // 'Planes,Trains,Automobiles'
```

### Array features

* Use an array as **stack**:

```js
var ratings = [];
ratings.push(5);
ratings.push(2, 4);
console.log(ratings.length); // 3
console.log(ratings.pop()); // 4
```

* You can get the first element out of an array using `shift()`
* `unshift()` adds an element at the beginning of the array and returns the new size
* You can sum arrays using `concat()`
* You can slice arrays using slice(index). The new array will start at the index until the end 	
* Takes the last 2 entries of the array:

```js
var ratings = [1,2,3,4];
ratings.slice(-2); // [3,4]
```

* With `splice()` the original array is modified.

```js
var ratings = [1, 2, 3, 4];
ratings.splice(1, 2);
console.log(ratings.toString()); // '1,4'
```

* We can insert elements in an array at a particular position using `splice()`:

```js
var ratings = [1, 2, 3, 4];
ratings.splice(2, 0, 99);
console.log(ratings.toString()); // '1,2,99,3,4'
```
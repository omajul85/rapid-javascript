### Storage

* In primitive types, variables such as numbers, strings and booleans are stored in memory locations and are immutables:

```js
var a = 42;
var b = a; // Copy the value from var a (42) into b
b = 5; // b is now 5 but a is still 42
```

* For reference types (objects), the values are not stored directly in a memory location. The memory location will contain a pointer (reference) to an unknown memory location.

```js
var o = {
	name: "Jill"
};

var o2 = o; // Both o and o2 points to the same memory location.
o2[name] = "Bob";

console.log(o); //Object {name: "Bob"}
```

### Common Reference Types

* Objects
* Arrays
* Dates
* RegExp's
* Functions
* Primitives (via wrappers)


### Examples

* Functions can modify Referenced Types:

```js
var blog = {
	name: 'Ski Utah'
};

function changeBlogName(localBlog) {
	localBlog.name = 'no name';
}

changeBlogName(blog);
console.log(blog.name); // 'no name'
```
* With arrays:

```js
var a1 = [1, 2, 3];
var a2 = a1; // This line is just copying a pointer to the array values (not the content itself)
a1[0] = 99;
console.log(a2[0]); // 99
```

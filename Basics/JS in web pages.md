### JavaScript in web pages

* The preferred place for the `<script>` tag is the very end of the body tag, so the page can be loaded while the js script is parsed and executed.

```js
<!DOCTYPE html>
<html>
<head>
</head>
<body>
	<h1>Our Page</h1>
	<script src="js/app.js"></script>
</body>
</html>
```

* If you use the `src` attribute in the script tag in order to load a JS file, the browser will ignore the content inside the script tag and ONLY executes the content of the file.

* The code below is a JS bug that triggers the error `unexpected end of file`. This might work on some browsers but is not recommended:

```js 
<script src="js/app.js" />
```

* JS scripts included using the `src` attribute are processed in order.

* The `defer` attribute is used to postpone the script to the end, once the others are already executed (and change order of execution).

* The `<noscript>` tag defines an alternate content for users that have disabled scripts in their browser or have a browser that doesn't support script.

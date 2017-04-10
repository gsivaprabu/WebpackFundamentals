# Basic Builds with Webpack - Building Multiple Files


- Add multiple files

```javascript
module.exports = {
	entry: ["./utils","./app.js"],
	output: {
		filename: "bundle.js"
	}
}
```
# Basic Builds with Webpack - Using Pre Loaders

- Preloaders concepts deprecated

so use the below config file

```javascript
module.exports = {
    entry: ["./utils", "./app.js"],
    output: {
        filename: "bundle.js"
    },
    watch: true,

    module: {
        loaders: [
            {
                test: /\.es6$/,
                exclude: /node_modules/,
                loader: "babel-loader"
            },
            {
                test: /\.js$/,
                exclude: /node_modules/,
                loader: "jshint-loader",
                enforce: 'pre'
            }
        ]
    },
    resolve: {
        extensions: ['.js','.es6']
    }
}
```
# Basic Builds with Webpack - Production Vs Development Builds

- Differences between production and development  of webpack.
- Not minified
- In development phase need to debug so we need source map.
- **webpack -p** is production ***-p*** means production you got **minified js**
- Install **npm install strip-loader --save-dev** Removed the **console.log()**
- Create new file **webpack-production.config.js** add production based configurations only.

```javascript

var WebpackStrip = require('strip-loader');

var devConfig = require('./webpack.config.js');

var stripLoader = {
    test: [/\.js$/, /\.es6$/],
    exclude: /node_modules/,
    loader: WebpackStrip.loader('console.log')
}

devConfig.module.loaders.push(stripLoader);

module.exports = devConfig;

```

- Install http-server **npm install http-server -g**
- Run http-server  **> http-server**

- Now you open in browser using below details

Starting up http-server, serving

Available on:

  http://192.168.1.100:8081

  http://127.0.0.1:8081

- Open the Developer tool and check the logs and all
# webpack5-starter-template

Webpack 5 Starter Template

1.  Project initialization: create a "package.json" file
    ```bash
    $ mkdir ./webpack5-starter-template && cd ./webpack5-starter-template
    $ npm init
    ```
2.  Install "webpack" and "webpack-cli" as development dependencies
    ```bash
    $ npm install webpack webpack-cli --save-dev
    ```
3.  Create project files
    ```bash
    $ mkdir ./src && cd ./src
    $ mkdir -p ./styles/{libraries,modules,variables} ./modules ./fonts ./images
    $ touch ./index.js ./index.html ./styles/style.css ./modules/module.js
    $ cd ..
    $ touch ./webpack.config.js
    ```
4.  Install "webpack-dev-server" as development dependency
    ```bash
    $ npm install webpack-dev-server --save-dev
    ```
5.  Add these lines to "package.json" file to configure npm scripts
    ```json
    "scripts": {
        "serve": "export NODE_ENV=development && webpack serve",
        "build:dev": "export NODE_ENV=development && webpack",
        "build:prod": "export NODE_ENV=production && webpack",
        "clean": "rm -rf ./dist"
    },
    ```
6.  Install "html-webpack-plugin" as development dependency
    ```bash
    $ npm install html-webpack-plugin --save-dev
    ```
7.  Configure "html-webpack-plugin"

8.  Install "html-loader"
    ```bash
    $ npm install html-loader
    ```
9.  Install "css-loader" and "style-loader" as development dependencies to load your styles from css and js files
    ```bash
    $ nmp install css-loader style-loader --save-dev
    ```
10. Install "mini-css-extract-plugin" as development dependency
    ```bash
    $ npm install mini-css-extract-plugin
    ```
11. Install "sass" and "sass-loader" as development dependencies
    ```bash
    $ npm install sass sass-loader --save-dev
    mv ./src/styles/style.css ./src/styles/style.scss
    ```
13. Install "postcss" "postcss-loader" "postcss-preset-env" as development dependencies
    ```bash
    npm install postcss postcss-loader postcss-preset-env --save-dev
    ```
14. Add these lines to "webpack.config.js" file to configure "webpack-dev-server"
    ```javascript
    module.exports = {
        devServer: {
        port: 9000,
        open: false,
        hot: true,
        },
    },
    ```
15. Install "babel-loader" "@babel/core" "@babel/preset-env"
    ```bash
    $ npm install babel-loader @babel/core @babel/preset-env as development dependencies
    ```
16. Add these lines to "wbpack.config.js" file to configure "babel-loader"
    ```javascript
    module: {
        rules: [
            {
                test: /\.m?js$/,
                exclude: /(node_modules|bower_components)/,
                use: {
                    loader: 'babel-loader',
                    options: {
                        presets: ['@babel/preset-env']
                    }
                }
            }
        ]
    }
    ```
17. Add these lines to webpack.config.js to configure fonts
    ```javascript
    module: {
        rules: [
            {
                test: /\.(eot|woff2?|[to]tf)$/i,
                type: 'asset/resource',
                generator: {
                    filename: 'fonts/[name][ext]'
                }
            }
        ]
    }
    ```
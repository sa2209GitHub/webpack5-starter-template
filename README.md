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

    $ npm install html-webpack-plugin --save-dev

7.  Configure "html-webpack-plugin"
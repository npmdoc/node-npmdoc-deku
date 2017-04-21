# npmdoc-deku

#### api documentation for  deku (v2.0.0-rc16)  [![npm package](https://img.shields.io/npm/v/npmdoc-deku.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-deku) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-deku.svg)](https://travis-ci.org/npmdoc/node-npmdoc-deku)

#### Render interfaces using pure functions and virtual DOM

[![NPM](https://nodei.co/npm/deku.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/deku)

- [https://npmdoc.github.io/node-npmdoc-deku/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-deku/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-deku/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-deku/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-deku/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-deku/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "deku",
    "version": "2.0.0-rc16",
    "license": "MIT",
    "repository": "dekujs/deku",
    "description": "Render interfaces using pure functions and virtual DOM",
    "main": "lib/index.js",
    "jsnext:main": "src/index.js",
    "scripts": {
        "clean": "rimraf lib _book",
        "build": "babel src --out-dir lib",
        "test": "hihat test/index.js -- --debug -t babelify -p tap-dev-tool",
        "test:headless": "browserify test/index.js -t babelify | tape-run",
        "test:browsers": "zuul -- ./test/index.js",
        "test:lint": "standard src/*.js test/*.js | snazzy",
        "docs:install": "gitbook install",
        "docs:build": "npm run docs:install && gitbook build",
        "docs:serve": "npm run docs:install && gitbook serve",
        "docs:deploy": "npm run docs:build && gh-pages -d _book",
        "prepublish": "npm run clean && npm run build",
        "preversion": "npm run clean && npm run test:lint",
        "version": "npm run build",
        "postversion": "git push && git push --tags && npm run clean",
        "standalone": "browserify src/index.js -s deku -t babelify -o dist/deku.js",
        "example:basic": "budo examples/basic/index.js -- -t babelify"
    },
    "devDependencies": {
        "babel-cli": "6.3.17",
        "babel-plugin-transform-react-jsx": "6.1.18",
        "babel-polyfill": "6.1.19",
        "babel-preset-es2015": "6.1.18",
        "babel-preset-stage-2": "6.1.18",
        "babelify": "7.2.0",
        "browserify": "13.0.0",
        "browserify-hmr": "^0.3.1",
        "budo": "7.1.0",
        "gh-pages": "0.8.0",
        "gitbook": "2.6.6",
        "hihat": "2.6.4",
        "is-dom": "1.0.5",
        "rimraf": "2.5.0",
        "snazzy": "2.0.1",
        "standard": "5.4.1",
        "tap-dev-tool": "1.3.0",
        "tape": "4.2.2",
        "tape-run": "2.1.0",
        "trigger-event": "1.0.0",
        "zuul": "3.9.0"
    },
    "dependencies": {
        "dift": "0.1.12",
        "index-of": "0.2.0",
        "is-svg-element": "1.0.1",
        "setify": "1.0.3",
        "svg-attribute-namespace": "2.1.0",
        "uid": "0.0.2",
        "union-type": "0.1.6"
    },
    "keywords": [
        "deku",
        "functional",
        "react",
        "virtual",
        "dom",
        "elm",
        "redux"
    ],
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

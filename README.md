# npmdoc-then-request

#### api documentation for  then-request (v2.2.0)  [![npm package](https://img.shields.io/npm/v/npmdoc-then-request.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-then-request) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-then-request.svg)](https://travis-ci.org/npmdoc/node-npmdoc-then-request)

#### A request library that returns promises, inspired by request

[![NPM](https://nodei.co/npm/then-request.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/then-request)

- [https://npmdoc.github.io/node-npmdoc-then-request/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-then-request/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-then-request/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-then-request/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-then-request/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-then-request/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "then-request",
    "version": "2.2.0",
    "description": "A request library that returns promises, inspired by request",
    "keywords": [],
    "browser": "./browser.js",
    "dependencies": {
        "caseless": "~0.11.0",
        "concat-stream": "^1.4.7",
        "http-basic": "^2.5.1",
        "http-response-object": "^1.1.0",
        "promise": "^7.1.1",
        "qs": "^6.1.0"
    },
    "devDependencies": {
        "browserify": "^8.1.1",
        "exorcist": "^0.1.6",
        "istanbul": "^0.3.5",
        "minifyify": "^6.0.0",
        "mkdirp": "^0.5.0",
        "rimraf": "^2.2.8",
        "testit": "^1.2.0"
    },
    "scripts": {
        "test": "node test/index.js && istanbul cover test/index.js",
        "prebuild": "rimraf dist && mkdirp dist",
        "prepublish": "npm run build",
        "build": "npm run build:full && npm run build:min",
        "build:full": "browserify -d --standalone request browser.js | exorcist -u request.js.map dist/request.js.map > dist/request.js",
        "build:min": "browserify -d --standalone request browser.js -p [minifyify --compressPath . --map request.min.js.map --output dist/request.min.js.map] > dist/request.min.js"
    },
    "repository": {
        "type": "git",
        "url": "https://github.com/then/then-request.git"
    },
    "author": "ForbesLindesay",
    "license": "MIT"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

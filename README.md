# npmdoc-aphrodite

#### basic api documentation for  [aphrodite (v1.2.0)](https://github.com/Khan/aphrodite)  [![npm package](https://img.shields.io/npm/v/npmdoc-aphrodite.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-aphrodite) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-aphrodite.svg)](https://travis-ci.org/npmdoc/node-npmdoc-aphrodite)

#### Inline styles in JS that just work (TM)

[![NPM](https://nodei.co/npm/aphrodite.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/aphrodite)

- [https://npmdoc.github.io/node-npmdoc-aphrodite/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-aphrodite/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-aphrodite/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-aphrodite/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-aphrodite/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-aphrodite/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Jamie Wong"
    },
    "bugs": {
        "url": "https://github.com/Khan/aphrodite/issues"
    },
    "dependencies": {
        "asap": "^2.0.3",
        "inline-style-prefixer": "^3.0.1",
        "string-hash": "^1.1.3"
    },
    "description": "Inline styles in JS that just work (TM)",
    "devDependencies": {
        "babel": "^5.8.23",
        "babel-core": "^5.8.25",
        "babel-loader": "^5.3.2",
        "caniuse-api": "^1.5.3",
        "chai": "^3.3.0",
        "es6-shim": "^0.35.3",
        "eslint": "^3.7.1",
        "eslint-config-standard-react": "^4.2.0",
        "eslint-plugin-react": "^6.3.0",
        "flow-bin": "^0.34.0",
        "jsdom": "^6.5.1",
        "mkdirp": "^0.5.1",
        "mocha": "^2.3.3",
        "npm-run-all": "^1.7.0",
        "nyc": "^6.4.4",
        "rimraf": "^2.5.2",
        "webpack": "^1.12.2"
    },
    "directories": {},
    "dist": {
        "shasum": "c2f30bd1cdf6a550f4a29a0f1cf22ed10e825764",
        "tarball": "https://registry.npmjs.org/aphrodite/-/aphrodite-1.2.0.tgz"
    },
    "gitHead": "413d20db4ffe7bf3492b9cc1c011f2fc3c28c5db",
    "homepage": "https://github.com/Khan/aphrodite",
    "keywords": [
        "css",
        "react",
        "inline-styles"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "jlfwong"
        },
        {
            "name": "khanacademy"
        },
        {
            "name": "xymostech"
        }
    ],
    "name": "aphrodite",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/Khan/aphrodite.git"
    },
    "scripts": {
        "build": "npm-run-all --parallel build:*",
        "build:commonjs": "webpack --output-library-target commonjs2 --output-filename aphrodite.js",
        "build:main": "babel -d lib/ src",
        "build:prefixes": "tools/generate_prefixer_data.js",
        "build:umd": "webpack --output-library-target umd --output-library aphrodite --output-filename aphrodite.umd.js --devtool source-map",
        "build:umdmin": "webpack --output-library-target umd --output-library aphrodite --output-filename aphrodite.umd.min.js -p --devtool source-map",
        "coverage": "nyc --check-coverage --lines 100 --branches 100 npm run tests",
        "lint": "eslint --fix --cache . && flow check",
        "posttest": "npm run lint",
        "prebuild": "rimraf dist/* lib/*",
        "pretest": "npm run build:prefixes",
        "preversion": "npm test",
        "test": "npm run coverage",
        "tests": "mocha --compilers js:babel/register tests",
        "tests:watch": "mocha --watch --compilers js:babel/register tests",
        "version": "npm run build && git add dist",
        "watch:build": "npm-run-all --parallel watch:build:*",
        "watch:build:commonjs": "npm run build:commonjs -- --watch",
        "watch:build:main": "npm run build:main -- --watch",
        "watch:build:umd": "npm run build:umd -- --watch",
        "watch:build:umdmin": "npm run build:umdmin -- --watch"
    },
    "tonicExampleFilename": "examples/runkit.js",
    "version": "1.2.0",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

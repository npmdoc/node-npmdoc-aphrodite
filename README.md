# api documentation for  [aphrodite (v1.2.0)](https://github.com/Khan/aphrodite)  [![npm package](https://img.shields.io/npm/v/npmdoc-aphrodite.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-aphrodite) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-aphrodite.svg)](https://travis-ci.org/npmdoc/node-npmdoc-aphrodite)
#### Inline styles in JS that just work (TM)

[![NPM](https://nodei.co/npm/aphrodite.png?downloads=true)](https://www.npmjs.com/package/aphrodite)

[![apidoc](https://npmdoc.github.io/node-npmdoc-aphrodite/build/screenCapture.buildNpmdoc.browser.%2Fhome%2Ftravis%2Fbuild%2Fnpmdoc%2Fnode-npmdoc-aphrodite%2Ftmp%2Fbuild%2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-aphrodite/build/apidoc.html)

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
            "name": "jlfwong",
            "email": "jamie.lf.wong@gmail.com"
        },
        {
            "name": "khanacademy",
            "email": "opensource+npm@khanacademy.org"
        },
        {
            "name": "xymostech",
            "email": "xymostech@gmail.com"
        }
    ],
    "name": "aphrodite",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
    "version": "1.2.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module aphrodite](#apidoc.module.aphrodite)
1.  [function <span class="apidocSignatureSpan">aphrodite.</span>css ()](#apidoc.element.aphrodite.css)
1.  [function <span class="apidocSignatureSpan">aphrodite.</span>ordered_elements ()](#apidoc.element.aphrodite.ordered_elements)
1.  object <span class="apidocSignatureSpan">aphrodite.</span>StyleSheet
1.  object <span class="apidocSignatureSpan">aphrodite.</span>StyleSheetServer
1.  object <span class="apidocSignatureSpan">aphrodite.</span>StyleSheetTestUtils
1.  object <span class="apidocSignatureSpan">aphrodite.</span>generate
1.  object <span class="apidocSignatureSpan">aphrodite.</span>inject
1.  object <span class="apidocSignatureSpan">aphrodite.</span>no_important
1.  object <span class="apidocSignatureSpan">aphrodite.</span>util

#### [module aphrodite.StyleSheet](#apidoc.module.aphrodite.StyleSheet)
1.  [function <span class="apidocSignatureSpan">aphrodite.StyleSheet.</span>create (sheetDefinition)](#apidoc.element.aphrodite.StyleSheet.create)
1.  [function <span class="apidocSignatureSpan">aphrodite.StyleSheet.</span>extend (extensions)](#apidoc.element.aphrodite.StyleSheet.extend)
1.  [function <span class="apidocSignatureSpan">aphrodite.StyleSheet.</span>rehydrate ()](#apidoc.element.aphrodite.StyleSheet.rehydrate)

#### [module aphrodite.StyleSheetServer](#apidoc.module.aphrodite.StyleSheetServer)
1.  [function <span class="apidocSignatureSpan">aphrodite.StyleSheetServer.</span>renderStatic (renderFunc)](#apidoc.element.aphrodite.StyleSheetServer.renderStatic)

#### [module aphrodite.StyleSheetTestUtils](#apidoc.module.aphrodite.StyleSheetTestUtils)
1.  [function <span class="apidocSignatureSpan">aphrodite.StyleSheetTestUtils.</span>clearBufferAndResumeStyleInjection ()](#apidoc.element.aphrodite.StyleSheetTestUtils.clearBufferAndResumeStyleInjection)
1.  [function <span class="apidocSignatureSpan">aphrodite.StyleSheetTestUtils.</span>suppressStyleInjection ()](#apidoc.element.aphrodite.StyleSheetTestUtils.suppressStyleInjection)

#### [module aphrodite.generate](#apidoc.module.aphrodite.generate)
1.  [function <span class="apidocSignatureSpan">aphrodite.generate.</span>generateCSS (selector, styleTypes, selectorHandlers, stringHandlers, useImportant )](#apidoc.element.aphrodite.generate.generateCSS)
1.  [function <span class="apidocSignatureSpan">aphrodite.generate.</span>generateCSSRuleset (selector, declarations, stringHandlers, useImportant, selectorHandlers )](#apidoc.element.aphrodite.generate.generateCSSRuleset)
1.  object <span class="apidocSignatureSpan">aphrodite.generate.</span>defaultSelectorHandlers

#### [module aphrodite.inject](#apidoc.module.aphrodite.inject)
1.  [function <span class="apidocSignatureSpan">aphrodite.inject.</span>addRenderedClassNames (classNames)](#apidoc.element.aphrodite.inject.addRenderedClassNames)
1.  [function <span class="apidocSignatureSpan">aphrodite.inject.</span>flushToString ()](#apidoc.element.aphrodite.inject.flushToString)
1.  [function <span class="apidocSignatureSpan">aphrodite.inject.</span>flushToStyleTag ()](#apidoc.element.aphrodite.inject.flushToStyleTag)
1.  [function <span class="apidocSignatureSpan">aphrodite.inject.</span>getRenderedClassNames ()](#apidoc.element.aphrodite.inject.getRenderedClassNames)
1.  [function <span class="apidocSignatureSpan">aphrodite.inject.</span>injectAndGetClassName (useImportant, styleDefinitions, selectorHandlers )](#apidoc.element.aphrodite.inject.injectAndGetClassName)
1.  [function <span class="apidocSignatureSpan">aphrodite.inject.</span>injectStyleOnce (key, selector, definitions, useImportant )](#apidoc.element.aphrodite.inject.injectStyleOnce)
1.  [function <span class="apidocSignatureSpan">aphrodite.inject.</span>reset ()](#apidoc.element.aphrodite.inject.reset)
1.  [function <span class="apidocSignatureSpan">aphrodite.inject.</span>startBuffering ()](#apidoc.element.aphrodite.inject.startBuffering)

#### [module aphrodite.no_important](#apidoc.module.aphrodite.no_important)
1.  [function <span class="apidocSignatureSpan">aphrodite.no_important.</span>css ()](#apidoc.element.aphrodite.no_important.css)
1.  object <span class="apidocSignatureSpan">aphrodite.no_important.</span>StyleSheet
1.  object <span class="apidocSignatureSpan">aphrodite.no_important.</span>StyleSheetServer
1.  object <span class="apidocSignatureSpan">aphrodite.no_important.</span>StyleSheetTestUtils

#### [module aphrodite.ordered_elements](#apidoc.module.aphrodite.ordered_elements)
1.  [function <span class="apidocSignatureSpan">aphrodite.</span>ordered_elements ()](#apidoc.element.aphrodite.ordered_elements.ordered_elements)
1.  [function <span class="apidocSignatureSpan">aphrodite.ordered_elements.</span>from (obj)](#apidoc.element.aphrodite.ordered_elements.from)
1.  [function <span class="apidocSignatureSpan">aphrodite.ordered_elements.</span>fromMap (map)](#apidoc.element.aphrodite.ordered_elements.fromMap)
1.  [function <span class="apidocSignatureSpan">aphrodite.ordered_elements.</span>fromObject (obj)](#apidoc.element.aphrodite.ordered_elements.fromObject)

#### [module aphrodite.util](#apidoc.module.aphrodite.util)
1.  [function <span class="apidocSignatureSpan">aphrodite.util.</span>flatten (list)](#apidoc.element.aphrodite.util.flatten)
1.  [function <span class="apidocSignatureSpan">aphrodite.util.</span>flattenDeep (list)](#apidoc.element.aphrodite.util.flattenDeep)
1.  [function <span class="apidocSignatureSpan">aphrodite.util.</span>hashObject (object)](#apidoc.element.aphrodite.util.hashObject)
1.  [function <span class="apidocSignatureSpan">aphrodite.util.</span>importantify (string)](#apidoc.element.aphrodite.util.importantify)
1.  [function <span class="apidocSignatureSpan">aphrodite.util.</span>kebabifyStyleName (string)](#apidoc.element.aphrodite.util.kebabifyStyleName)
1.  [function <span class="apidocSignatureSpan">aphrodite.util.</span>mapObj (obj, fn )](#apidoc.element.aphrodite.util.mapObj)
1.  [function <span class="apidocSignatureSpan">aphrodite.util.</span>objectToPairs (obj)](#apidoc.element.aphrodite.util.objectToPairs)
1.  [function <span class="apidocSignatureSpan">aphrodite.util.</span>recursiveMerge (a, b )](#apidoc.element.aphrodite.util.recursiveMerge)
1.  [function <span class="apidocSignatureSpan">aphrodite.util.</span>stringifyValue (key, prop )](#apidoc.element.aphrodite.util.stringifyValue)



# <a name="apidoc.module.aphrodite"></a>[module aphrodite](#apidoc.module.aphrodite)

#### <a name="apidoc.element.aphrodite.css"></a>[function <span class="apidocSignatureSpan">aphrodite.</span>css ()](#apidoc.element.aphrodite.css)
- description and source-code
```javascript
function css() /* : MaybeSheetDefinition[] */{
    for (var _len = arguments.length, styleDefinitions = Array(_len), _key = 0; _key < _len; _key++) {
        styleDefinitions[_key] = arguments[_key];
    }

    return (0, _inject.injectAndGetClassName)(useImportant, styleDefinitions, selectorHandlers);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.aphrodite.ordered_elements"></a>[function <span class="apidocSignatureSpan">aphrodite.</span>ordered_elements ()](#apidoc.element.aphrodite.ordered_elements)
- description and source-code
```javascript
function OrderedElements() {
    var elements /* : {[string]: any} */ = arguments.length <= 0 || arguments[0] === undefined ? {} : arguments[0];
    var keyOrder /* : string[] */ = arguments.length <= 1 || arguments[1] === undefined ? [] : arguments[1];

    _classCallCheck(this, OrderedElements);

    this.elements = elements;
    this.keyOrder = keyOrder;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.aphrodite.StyleSheet"></a>[module aphrodite.StyleSheet](#apidoc.module.aphrodite.StyleSheet)

#### <a name="apidoc.element.aphrodite.StyleSheet.create"></a>[function <span class="apidocSignatureSpan">aphrodite.StyleSheet.</span>create (sheetDefinition)](#apidoc.element.aphrodite.StyleSheet.create)
- description and source-code
```javascript
function create(sheetDefinition) {
    return (0, _util.mapObj)(sheetDefinition, function (_ref) {
        var _ref2 = _slicedToArray(_ref, 2);

        var key = _ref2[0];
        var val = _ref2[1];

        return [key, {
            // TODO(emily): Make a 'production' mode which doesn't prepend
            // the class name here, to make the generated CSS smaller.
            _name: key + '_' + (0, _util.hashObject)(val),
            _definition: val
        }];
    });
}
```
- example usage
```shell
...
            This is blue and turns red when the browser is less than
            600px width.
        </span>
    </div>;
}
}

const styles = StyleSheet.create({
red: {
    backgroundColor: 'red'
},

blue: {
    backgroundColor: 'blue'
},
...
```

#### <a name="apidoc.element.aphrodite.StyleSheet.extend"></a>[function <span class="apidocSignatureSpan">aphrodite.StyleSheet.</span>extend (extensions)](#apidoc.element.aphrodite.StyleSheet.extend)
- description and source-code
```javascript
function extend(extensions) {
    var extensionSelectorHandlers = extensions
    // Pull out extensions with a selectorHandler property
    .map(function (extension) {
        return extension.selectorHandler;
    })
    // Remove nulls (i.e. extensions without a selectorHandler
    // property).
    .filter(function (handler) {
        return handler;
    });

    return makeExports(useImportant, selectorHandlers.concat(extensionSelectorHandlers));
}
```
- example usage
```shell
...
Aphrodite ('css', 'StyleSheet', etc.) which will have your extensions included.
For example:

'''js
// my-aphrodite.js
import {StyleSheet} from "aphrodite";

export default StyleSheet.extend([extension1, extension2]);

// styled.js
import {StyleSheet, css} from "my-aphrodite.js";

const styles = StyleSheet.create({
    ...
});
...
```

#### <a name="apidoc.element.aphrodite.StyleSheet.rehydrate"></a>[function <span class="apidocSignatureSpan">aphrodite.StyleSheet.</span>rehydrate ()](#apidoc.element.aphrodite.StyleSheet.rehydrate)
- description and source-code
```javascript
function rehydrate() {
    var renderedClassNames /* : string[] */ = arguments.length <= 0 || arguments[0] === undefined ? [] : arguments[0];

    (0, _inject.addRenderedClassNames)(renderedClassNames);
}
```
- example usage
```shell
...
        <head>
            <style data-aphrodite>${css.content}</style>
        </head>
        <body>
            <div id='root'>${html}</div>
            <script src="./bundle.js"></script>
            <script>
                StyleSheet.rehydrate(${JSON.stringify(css.renderedClassNames)});
                ReactDOM.render(<App/>, document.getElementById('root'));
            </script>
        </body>
    </html>
';
'''
...
```



# <a name="apidoc.module.aphrodite.StyleSheetServer"></a>[module aphrodite.StyleSheetServer](#apidoc.module.aphrodite.StyleSheetServer)

#### <a name="apidoc.element.aphrodite.StyleSheetServer.renderStatic"></a>[function <span class="apidocSignatureSpan">aphrodite.StyleSheetServer.</span>renderStatic (renderFunc)](#apidoc.element.aphrodite.StyleSheetServer.renderStatic)
- description and source-code
```javascript
function renderStatic(renderFunc) {
    (0, _inject.reset)();
    (0, _inject.startBuffering)();
    var html = renderFunc();
    var cssContent = (0, _inject.flushToString)();

    return {
        html: html,
        css: {
            content: cssContent,
            renderedClassNames: (0, _inject.getRenderedClassNames)()
        }
    };
}
```
- example usage
```shell
...
As an example:

'''js
import { StyleSheetServer } from 'aphrodite';

// Contains the generated html, as well as the generated css and some
// rehydration data.
var {html, css} = StyleSheetServer.renderStatic(() => {
return ReactDOMServer.renderToString(<App/>);
});

// Return the base HTML, which contains your rendered HTML as well as a
// simple rehydration script.
return '
<html>
...
```



# <a name="apidoc.module.aphrodite.StyleSheetTestUtils"></a>[module aphrodite.StyleSheetTestUtils](#apidoc.module.aphrodite.StyleSheetTestUtils)

#### <a name="apidoc.element.aphrodite.StyleSheetTestUtils.clearBufferAndResumeStyleInjection"></a>[function <span class="apidocSignatureSpan">aphrodite.StyleSheetTestUtils.</span>clearBufferAndResumeStyleInjection ()](#apidoc.element.aphrodite.StyleSheetTestUtils.clearBufferAndResumeStyleInjection)
- description and source-code
```javascript
function clearBufferAndResumeStyleInjection() {
    (0, _inject.reset)();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.aphrodite.StyleSheetTestUtils.suppressStyleInjection"></a>[function <span class="apidocSignatureSpan">aphrodite.StyleSheetTestUtils.</span>suppressStyleInjection ()](#apidoc.element.aphrodite.StyleSheetTestUtils.suppressStyleInjection)
- description and source-code
```javascript
function suppressStyleInjection() {
    (0, _inject.reset)();
    (0, _inject.startBuffering)();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.aphrodite.generate"></a>[module aphrodite.generate](#apidoc.module.aphrodite.generate)

#### <a name="apidoc.element.aphrodite.generate.generateCSS"></a>[function <span class="apidocSignatureSpan">aphrodite.generate.</span>generateCSS (selector, styleTypes, selectorHandlers, stringHandlers, useImportant )](#apidoc.element.aphrodite.generate.generateCSS)
- description and source-code
```javascript
function generateCSS(selector, styleTypes, selectorHandlers, stringHandlers, useImportant ) /* : string */{
    var merged /* : OrderedElements */ = styleTypes.reduce(_util.recursiveMerge, new _orderedElements2['default']());

    var plainDeclarations = new _orderedElements2['default']();
    var generatedStyles = "";

    // TODO(emily): benchmark this to see if a plain for loop would be faster.
    merged.forEach(function (key, val) {
        // For each key, see if one of the selector handlers will handle these
        // styles.
        var foundHandler = selectorHandlers.some(function (handler) {
            var result = handler(key, selector, function (newSelector) {
                return generateCSS(newSelector, [val], selectorHandlers, stringHandlers, useImportant);
            });
            if (result != null) {
                // If the handler returned something, add it to the generated
                // CSS and stop looking for another handler.
                generatedStyles += result;
                return true;
            }
        });
        // If none of the handlers handled it, add it to the list of plain
        // style declarations.
        if (!foundHandler) {
            plainDeclarations.set(key, val);
        }
    });

    return generateCSSRuleset(selector, plainDeclarations, stringHandlers, useImportant, selectorHandlers) + generatedStyles;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.aphrodite.generate.generateCSSRuleset"></a>[function <span class="apidocSignatureSpan">aphrodite.generate.</span>generateCSSRuleset (selector, declarations, stringHandlers, useImportant, selectorHandlers )](#apidoc.element.aphrodite.generate.generateCSSRuleset)
- description and source-code
```javascript
function generateCSSRuleset(selector, declarations, stringHandlers, useImportant, selectorHandlers ) /* : string */{
    var handledDeclarations /* : OrderedElements */ = runStringHandlers(declarations, stringHandlers, selectorHandlers);

    var originalElements = _extends({}, handledDeclarations.elements);

    // NOTE(emily): This mutates handledDeclarations.elements.
    var prefixedDeclarations = prefixAll(handledDeclarations.elements);

    var prefixedRules = (0, _util.flatten)((0, _util.objectToPairs)(prefixedDeclarations).map(function (_ref) {
        var _ref2 = _slicedToArray(_ref, 2);

        var key = _ref2[0];
        var value = _ref2[1];

        if (Array.isArray(value)) {
            // inline-style-prefixer returns an array when there should be
            // multiple rules for the same key. Here we flatten to multiple
            // pairs with the same key.
            return value.map(function (v) {
                return [key, v];
            });
        }
        return [[key, value]];
    }));

    // Calculate the order that we want to each element in 'prefixedRules' to
    // be in, based on its index in the original key ordering.
    var sortOrder = {};
    for (var i = 0; i < handledDeclarations.keyOrder.length; i++) {
        var key = handledDeclarations.keyOrder[i];
        sortOrder[key] = i;

        // In order to keep most prefixed versions of keys in about the same
        // order that the original keys were in but placed before the
        // unprefixed version, we generate the prefixed forms of the keys and
        // set their order to the same as the original key minus a little bit.
        var capitalizedKey = '' + key[0].toUpperCase() + key.slice(1);
        var prefixedKeys = ['Webkit' + capitalizedKey, 'Moz' + capitalizedKey, 'ms' + capitalizedKey];
        for (var j = 0; j < prefixedKeys.length; ++j) {
            if (!originalElements.hasOwnProperty(prefixedKeys[j])) {
                sortOrder[prefixedKeys[j]] = i - 0.5;
                originalElements[prefixedKeys[j]] = originalElements[key];
            }
        }
    }

    // Calculate the sort order of a given property.
    function sortOrderForProperty(_ref3) {
        var _ref32 = _slicedToArray(_ref3, 2);

        var key = _ref32[0];
        var value = _ref32[1];

        if (sortOrder.hasOwnProperty(key)) {
            if (originalElements.hasOwnProperty(key) && originalElements[key] !== value) {
                // The value is prefixed. Sort this just before the key with
                // the unprefixed value.
                return sortOrder[key] - 0.25;
            } else {
                // Either the key and value are unprefixed here, or this is a
                // prefixed key. Either way, this is handled by the sortOrder
                // calculation above.
                return sortOrder[key];
            }
        } else {
            // If the property isn't in the sort order, it wasn't in the
            // original set of unprefixed keys, so it must be a prefixed key.
            // Sort at order -1 to put it at the top of the set of styles.
            return -1;
        }
    }

    // Actually sort the rules according to the sort order.
    prefixedRules.sort(function (a, b) {
        return sortOrderForProperty(a) - sortOrderForProperty(b);
    });

    var transformValue = useImportant === false ? _util.stringifyValue : function (key, value) {
        return (0, _util.importantify)((0, _util.stringifyValue)(key, value));
    };

    var rules = prefixedRules.map(function (_ref4) {
        var _ref42 = _slicedToArray(_ref4, 2);

        var key = _ref42[0];
        var value = _ref42[1];
        return (0, _util.kebabifyStyleName)(key) + ':' + transformValue(key, value) + ';';
    }).join("");

    if (rules) {
        return selector + '{' + rules + '}';
    } else {
        return "";
    }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.aphrodite.inject"></a>[module aphrodite.inject](#apidoc.module.aphrodite.inject)

#### <a name="apidoc.element.aphrodite.inject.addRenderedClassNames"></a>[function <span class="apidocSignatureSpan">aphrodite.inject.</span>addRenderedClassNames (classNames)](#apidoc.element.aphrodite.inject.addRenderedClassNames)
- description and source-code
```javascript
function addRenderedClassNames(classNames) {
    classNames.forEach(function (className) {
        alreadyInjected[className] = true;
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.aphrodite.inject.flushToString"></a>[function <span class="apidocSignatureSpan">aphrodite.inject.</span>flushToString ()](#apidoc.element.aphrodite.inject.flushToString)
- description and source-code
```javascript
function flushToString() {
    isBuffering = false;
    var ret = injectionBuffer;
    injectionBuffer = "";
    return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.aphrodite.inject.flushToStyleTag"></a>[function <span class="apidocSignatureSpan">aphrodite.inject.</span>flushToStyleTag ()](#apidoc.element.aphrodite.inject.flushToStyleTag)
- description and source-code
```javascript
function flushToStyleTag() {
    var cssContent = flushToString();
    if (cssContent.length > 0) {
        injectStyleTag(cssContent);
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.aphrodite.inject.getRenderedClassNames"></a>[function <span class="apidocSignatureSpan">aphrodite.inject.</span>getRenderedClassNames ()](#apidoc.element.aphrodite.inject.getRenderedClassNames)
- description and source-code
```javascript
function getRenderedClassNames() {
    return Object.keys(alreadyInjected);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.aphrodite.inject.injectAndGetClassName"></a>[function <span class="apidocSignatureSpan">aphrodite.inject.</span>injectAndGetClassName (useImportant, styleDefinitions, selectorHandlers )](#apidoc.element.aphrodite.inject.injectAndGetClassName)
- description and source-code
```javascript
function injectAndGetClassName(useImportant, styleDefinitions, selectorHandlers ) /* : string */{
    styleDefinitions = (0, _util.flattenDeep)(styleDefinitions);

    var classNameBits = [];
    var definitionBits = [];
    for (var i = 0; i < styleDefinitions.length; i += 1) {
        // Filter out falsy values from the input, to allow for
        // 'css(a, test && c)'
        if (styleDefinitions[i]) {
            classNameBits.push(styleDefinitions[i]._name);
            definitionBits.push(styleDefinitions[i]._definition);
        }
    }
    // Break if there aren't any valid styles.
    if (classNameBits.length === 0) {
        return "";
    }
    var className = classNameBits.join("-o_O-");

    injectStyleOnce(className, '.' + className, definitionBits, useImportant, selectorHandlers);

    return className;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.aphrodite.inject.injectStyleOnce"></a>[function <span class="apidocSignatureSpan">aphrodite.inject.</span>injectStyleOnce (key, selector, definitions, useImportant )](#apidoc.element.aphrodite.inject.injectStyleOnce)
- description and source-code
```javascript
function injectStyleOnce(key, selector, definitions, useImportant ) {
    var selectorHandlers /* : SelectorHandler[] */ = arguments.length <= 4 || arguments[4] === undefined ? [] : arguments[4];

    if (!alreadyInjected[key]) {
        var generated = (0, _generate.generateCSS)(selector, definitions, selectorHandlers, stringHandlers, useImportant);

        injectGeneratedCSSOnce(key, generated);
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.aphrodite.inject.reset"></a>[function <span class="apidocSignatureSpan">aphrodite.inject.</span>reset ()](#apidoc.element.aphrodite.inject.reset)
- description and source-code
```javascript
function reset() {
    injectionBuffer = "";
    alreadyInjected = {};
    isBuffering = false;
    styleTag = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.aphrodite.inject.startBuffering"></a>[function <span class="apidocSignatureSpan">aphrodite.inject.</span>startBuffering ()](#apidoc.element.aphrodite.inject.startBuffering)
- description and source-code
```javascript
function startBuffering() {
    if (isBuffering) {
        throw new Error("Cannot buffer while already buffering");
    }
    isBuffering = true;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.aphrodite.no_important"></a>[module aphrodite.no_important](#apidoc.module.aphrodite.no_important)

#### <a name="apidoc.element.aphrodite.no_important.css"></a>[function <span class="apidocSignatureSpan">aphrodite.no_important.</span>css ()](#apidoc.element.aphrodite.no_important.css)
- description and source-code
```javascript
function css() /* : MaybeSheetDefinition[] */{
    for (var _len = arguments.length, styleDefinitions = Array(_len), _key = 0; _key < _len; _key++) {
        styleDefinitions[_key] = arguments[_key];
    }

    return (0, _inject.injectAndGetClassName)(useImportant, styleDefinitions, selectorHandlers);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.aphrodite.ordered_elements"></a>[module aphrodite.ordered_elements](#apidoc.module.aphrodite.ordered_elements)

#### <a name="apidoc.element.aphrodite.ordered_elements.ordered_elements"></a>[function <span class="apidocSignatureSpan">aphrodite.</span>ordered_elements ()](#apidoc.element.aphrodite.ordered_elements.ordered_elements)
- description and source-code
```javascript
function OrderedElements() {
    var elements /* : {[string]: any} */ = arguments.length <= 0 || arguments[0] === undefined ? {} : arguments[0];
    var keyOrder /* : string[] */ = arguments.length <= 1 || arguments[1] === undefined ? [] : arguments[1];

    _classCallCheck(this, OrderedElements);

    this.elements = elements;
    this.keyOrder = keyOrder;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.aphrodite.ordered_elements.from"></a>[function <span class="apidocSignatureSpan">aphrodite.ordered_elements.</span>from (obj)](#apidoc.element.aphrodite.ordered_elements.from)
- description and source-code
```javascript
from = function (obj) {
    if (obj instanceof OrderedElements) {
        // NOTE(emily): This makes a shallow copy of the previous elements, so
        // if the elements are deeply modified it will affect all copies.
        return new OrderedElements(_extends({}, obj.elements), obj.keyOrder.slice());
    } else if (
    // For some reason, flow complains about a plain
    // 'typeof Map !== "undefined"' check. Casting 'Map' to 'any' solves
    // the problem.
    typeof /*::(*/Map /*: any)*/ !== "undefined" && obj instanceof Map) {
        return OrderedElements.fromMap(obj);
    } else {
        return OrderedElements.fromObject(obj);
    }
}
```
- example usage
```shell
...
b /* : ObjectMap | Map<string,any> */
) /* : OrderedElements | any */{
// TODO(jlfwong): Handle malformed input where a and b are not the same
// type.

if (!isPlainObject(a) || !isPlainObject(b)) {
    if (isPlainObject(b)) {
        return _orderedElements2['default'].from(b);
    } else {
        return b;
    }
}

var ret = _orderedElements2['default'].from(a);
var right = _orderedElements2['default'].from(b);
...
```

#### <a name="apidoc.element.aphrodite.ordered_elements.fromMap"></a>[function <span class="apidocSignatureSpan">aphrodite.ordered_elements.</span>fromMap (map)](#apidoc.element.aphrodite.ordered_elements.fromMap)
- description and source-code
```javascript
fromMap = function (map) {
    var ret = new OrderedElements();
    map.forEach(function (val, key) {
        ret.set(key, val);
    });
    return ret;
}
```
- example usage
```shell
...
        // if the elements are deeply modified it will affect all copies.
        return new OrderedElements(_extends({}, obj.elements), obj.keyOrder.slice());
    } else if (
    // For some reason, flow complains about a plain
    // 'typeof Map !== "undefined"' check. Casting 'Map' to 'any' solves
    // the problem.
    typeof /*::(*/Map /*: any)*/ !== "undefined" && obj instanceof Map) {
        return OrderedElements.fromMap(obj);
    } else {
        return OrderedElements.fromObject(obj);
    }
};
module.exports = exports["default"];
...
```

#### <a name="apidoc.element.aphrodite.ordered_elements.fromObject"></a>[function <span class="apidocSignatureSpan">aphrodite.ordered_elements.</span>fromObject (obj)](#apidoc.element.aphrodite.ordered_elements.fromObject)
- description and source-code
```javascript
fromObject = function (obj) {
    return new OrderedElements(obj, Object.keys(obj));
}
```
- example usage
```shell
...
    } else if (
    // For some reason, flow complains about a plain
    // 'typeof Map !== "undefined"' check. Casting 'Map' to 'any' solves
    // the problem.
    typeof /*::(*/Map /*: any)*/ !== "undefined" && obj instanceof Map) {
        return OrderedElements.fromMap(obj);
    } else {
        return OrderedElements.fromObject(obj);
    }
};
module.exports = exports["default"];
...
```



# <a name="apidoc.module.aphrodite.util"></a>[module aphrodite.util](#apidoc.module.aphrodite.util)

#### <a name="apidoc.element.aphrodite.util.flatten"></a>[function <span class="apidocSignatureSpan">aphrodite.util.</span>flatten (list)](#apidoc.element.aphrodite.util.flatten)
- description and source-code
```javascript
function flatten(list) {
    return (/* : any[] */list.reduce(function (memo, x) {
            return memo.concat(x);
        }, [])
    );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.aphrodite.util.flattenDeep"></a>[function <span class="apidocSignatureSpan">aphrodite.util.</span>flattenDeep (list)](#apidoc.element.aphrodite.util.flattenDeep)
- description and source-code
```javascript
function flattenDeep(list) {
    return (/* : any[] */list.reduce(function (memo, x) {
            return memo.concat(Array.isArray(x) ? flattenDeep(x) : x);
        }, [])
    );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.aphrodite.util.hashObject"></a>[function <span class="apidocSignatureSpan">aphrodite.util.</span>hashObject (object)](#apidoc.element.aphrodite.util.hashObject)
- description and source-code
```javascript
function hashObject(object) {
    return (/* : string */(0, _stringHash2['default'])(JSON.stringify(object)).toString(36)
    );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.aphrodite.util.importantify"></a>[function <span class="apidocSignatureSpan">aphrodite.util.</span>importantify (string)](#apidoc.element.aphrodite.util.importantify)
- description and source-code
```javascript
function importantify(string) {
    return (<span class="apidocCodeCommentSpan">/* : string */
</span>        // Bracket string character access is very fast, and in the default case we
        // normally don't expect there to be "!important" at the end of the string
        // so we can use this simple check to take an optimized path. If there
        // happens to be a "!" in this position, we follow up with a more thorough
        // check.
        string[string.length - 10] === '!' && string.slice(-11) === ' !important' ? string : string + ' !important'
    );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.aphrodite.util.kebabifyStyleName"></a>[function <span class="apidocSignatureSpan">aphrodite.util.</span>kebabifyStyleName (string)](#apidoc.element.aphrodite.util.kebabifyStyleName)
- description and source-code
```javascript
function kebabifyStyleName(string) /* : string */{
    var result = string.replace(UPPERCASE_RE, UPPERCASE_RE_TO_KEBAB);
    if (result[0] === 'm' && result[1] === 's' && result[2] === '-') {
        return '-' + result;
    }
    return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.aphrodite.util.mapObj"></a>[function <span class="apidocSignatureSpan">aphrodite.util.</span>mapObj (obj, fn )](#apidoc.element.aphrodite.util.mapObj)
- description and source-code
```javascript
function mapObj(obj, fn ) /* : ObjectMap */{
    var keys = Object.keys(obj);
    var mappedObj = {};
    for (var i = 0; i < keys.length; i += 1) {
        var _fn = fn([keys[i], obj[keys[i]]]);

        var _fn2 = _slicedToArray(_fn, 2);

        var newKey = _fn2[0];
        var newValue = _fn2[1];

        mappedObj[newKey] = newValue;
    }
    return mappedObj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.aphrodite.util.objectToPairs"></a>[function <span class="apidocSignatureSpan">aphrodite.util.</span>objectToPairs (obj)](#apidoc.element.aphrodite.util.objectToPairs)
- description and source-code
```javascript
function objectToPairs(obj) {
    return (/* : Pairs */Object.keys(obj).map(function (key) {
            return [key, obj[key]];
        })
    );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.aphrodite.util.recursiveMerge"></a>[function <span class="apidocSignatureSpan">aphrodite.util.</span>recursiveMerge (a, b )](#apidoc.element.aphrodite.util.recursiveMerge)
- description and source-code
```javascript
function recursiveMerge(a, b ) /* : OrderedElements | any */{
    // TODO(jlfwong): Handle malformed input where a and b are not the same
    // type.

    if (!isPlainObject(a) || !isPlainObject(b)) {
        if (isPlainObject(b)) {
            return _orderedElements2['default'].from(b);
        } else {
            return b;
        }
    }

    var ret = _orderedElements2['default'].from(a);
    var right = _orderedElements2['default'].from(b);

    right.forEach(function (key, val) {
        if (ret.has(key)) {
            ret.set(key, recursiveMerge(ret.get(key), val));
        } else {
            ret.set(key, val);
        }
    });

    return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.aphrodite.util.stringifyValue"></a>[function <span class="apidocSignatureSpan">aphrodite.util.</span>stringifyValue (key, prop )](#apidoc.element.aphrodite.util.stringifyValue)
- description and source-code
```javascript
function stringifyValue(key, prop ) /* : string */{
    if (typeof prop === "number") {
        if (isUnitlessNumber[key]) {
            return "" + prop;
        } else {
            return prop + "px";
        }
    } else {
        return '' + prop;
    }
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

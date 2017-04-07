# api documentation for  [isparta (v4.0.0)](http://github.com/douglasduteil/isparta)  [![npm package](https://img.shields.io/npm/v/npmdoc-isparta.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-isparta) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-isparta.svg)](https://travis-ci.org/npmdoc/node-npmdoc-isparta)
#### A code coverage tool for ES6 (babel)

[![NPM](https://nodei.co/npm/isparta.png?downloads=true)](https://www.npmjs.com/package/isparta)

[![apidoc](https://npmdoc.github.io/node-npmdoc-isparta/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-isparta_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-isparta/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-isparta/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-isparta/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Douglas Duteil",
        "email": "douglasduteil@gmail.com"
    },
    "bin": {
        "isparta": "./bin/isparta"
    },
    "bugs": {
        "url": "http://github.com/douglasduteil/isparta/issues"
    },
    "dependencies": {
        "babel-core": "^6.1.4",
        "escodegen": "^1.6.1",
        "esprima": "^2.1.0",
        "istanbul": "^0.4.0",
        "mkdirp": "^0.5.0",
        "nomnomnomnom": "^2.0.0",
        "object-assign": "^4.0.1",
        "source-map": "^0.5.0",
        "which": "^1.0.9"
    },
    "description": "A code coverage tool for ES6 (babel)",
    "devDependencies": {
        "babel-cli": "^6.1.4",
        "babel-plugin-transform-object-rest-spread": "^6.1.4",
        "babel-polyfill": "^6.1.4",
        "babel-preset-es2015": "^6.1.4",
        "chai": "^3.2.0",
        "douglasduteil...shelltest": "^2.0.0",
        "hide-stack-frames-from": "^1.0.0",
        "mocha": "^2.2.1",
        "nth": "^0.1.2",
        "sinon": "^1.17.2",
        "sinon-chai": "^2.8.0"
    },
    "directories": {
        "lib": "./lib"
    },
    "dist": {
        "shasum": "1de91996f480b22dcb1aca8510255bae1574446e",
        "tarball": "https://registry.npmjs.org/isparta/-/isparta-4.0.0.tgz"
    },
    "files": [
        "bin/",
        "lib/"
    ],
    "gitHead": "749862a7d1810dd25b8c62c9e613720b57d36da1",
    "homepage": "http://github.com/douglasduteil/isparta",
    "keywords": [
        "karma",
        "karma-coverage",
        "karma-traceur-preprocessor",
        "istanbul",
        "6to5",
        "babel",
        "es6",
        "harmony"
    ],
    "license": "WTFPL",
    "main": "./lib/isparta",
    "maintainers": [
        {
            "name": "douglasduteil",
            "email": "douglasduteil@gmail.com"
        }
    ],
    "name": "isparta",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/douglasduteil/isparta.git"
    },
    "scripts": {
        "dist": "babel src --out-dir lib",
        "prepublish": "npm run dist",
        "test": "mocha",
        "watch": "npm run dist -- -w"
    },
    "version": "4.0.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module isparta](#apidoc.module.isparta)
1.  [function <span class="apidocSignatureSpan">isparta.</span>Collector (options)](#apidoc.element.isparta.Collector)
1.  [function <span class="apidocSignatureSpan">isparta.</span>ContentWriter ()](#apidoc.element.isparta.ContentWriter)
1.  [function <span class="apidocSignatureSpan">isparta.</span>FileWriter (sync)](#apidoc.element.isparta.FileWriter)
1.  [function <span class="apidocSignatureSpan">isparta.</span>Instrumenter ()](#apidoc.element.isparta.Instrumenter)
1.  [function <span class="apidocSignatureSpan">isparta.</span>Report ()](#apidoc.element.isparta.Report)
1.  [function <span class="apidocSignatureSpan">isparta.</span>Reporter (cfg, dir)](#apidoc.element.isparta.Reporter)
1.  [function <span class="apidocSignatureSpan">isparta.</span>Store ()](#apidoc.element.isparta.Store)
1.  [function <span class="apidocSignatureSpan">isparta.</span>TreeSummarizer ()](#apidoc.element.isparta.TreeSummarizer)
1.  [function <span class="apidocSignatureSpan">isparta.</span>Writer ()](#apidoc.element.isparta.Writer)
1.  [function <span class="apidocSignatureSpan">isparta.</span>_yuiLoadHook (matchFn, transformFn, verbose)](#apidoc.element.isparta._yuiLoadHook)
1.  [function <span class="apidocSignatureSpan">isparta.</span>matcherFor (options, callback)](#apidoc.element.isparta.matcherFor)
1.  object <span class="apidocSignatureSpan">isparta.</span>Collector.prototype
1.  object <span class="apidocSignatureSpan">isparta.</span>ContentWriter.prototype
1.  object <span class="apidocSignatureSpan">isparta.</span>FileWriter.prototype
1.  object <span class="apidocSignatureSpan">isparta.</span>Report.prototype
1.  object <span class="apidocSignatureSpan">isparta.</span>Reporter.prototype
1.  object <span class="apidocSignatureSpan">isparta.</span>Store.prototype
1.  object <span class="apidocSignatureSpan">isparta.</span>TreeSummarizer.prototype
1.  object <span class="apidocSignatureSpan">isparta.</span>Writer.prototype
1.  object <span class="apidocSignatureSpan">isparta.</span>config
1.  object <span class="apidocSignatureSpan">isparta.</span>hook
1.  object <span class="apidocSignatureSpan">isparta.</span>instrumenter
1.  object <span class="apidocSignatureSpan">isparta.</span>utils
1.  string <span class="apidocSignatureSpan">isparta.</span>assetsDir

#### [module isparta.Collector](#apidoc.module.isparta.Collector)
1.  [function <span class="apidocSignatureSpan">isparta.</span>Collector (options)](#apidoc.element.isparta.Collector.Collector)

#### [module isparta.Collector.prototype](#apidoc.module.isparta.Collector.prototype)
1.  [function <span class="apidocSignatureSpan">isparta.Collector.prototype.</span>add (coverage)](#apidoc.element.isparta.Collector.prototype.add)
1.  [function <span class="apidocSignatureSpan">isparta.Collector.prototype.</span>dispose ()](#apidoc.element.isparta.Collector.prototype.dispose)
1.  [function <span class="apidocSignatureSpan">isparta.Collector.prototype.</span>fileCoverageFor (fileName)](#apidoc.element.isparta.Collector.prototype.fileCoverageFor)
1.  [function <span class="apidocSignatureSpan">isparta.Collector.prototype.</span>files ()](#apidoc.element.isparta.Collector.prototype.files)
1.  [function <span class="apidocSignatureSpan">isparta.Collector.prototype.</span>getFinalCoverage ()](#apidoc.element.isparta.Collector.prototype.getFinalCoverage)

#### [module isparta.ContentWriter](#apidoc.module.isparta.ContentWriter)
1.  [function <span class="apidocSignatureSpan">isparta.</span>ContentWriter ()](#apidoc.element.isparta.ContentWriter.ContentWriter)

#### [module isparta.ContentWriter.prototype](#apidoc.module.isparta.ContentWriter.prototype)
1.  [function <span class="apidocSignatureSpan">isparta.ContentWriter.prototype.</span>println (str)](#apidoc.element.isparta.ContentWriter.prototype.println)
1.  [function <span class="apidocSignatureSpan">isparta.ContentWriter.prototype.</span>write ()](#apidoc.element.isparta.ContentWriter.prototype.write)

#### [module isparta.FileWriter](#apidoc.module.isparta.FileWriter)
1.  [function <span class="apidocSignatureSpan">isparta.</span>FileWriter (sync)](#apidoc.element.isparta.FileWriter.FileWriter)
1.  [function <span class="apidocSignatureSpan">isparta.FileWriter.</span>super_ ()](#apidoc.element.isparta.FileWriter.super_)

#### [module isparta.FileWriter.prototype](#apidoc.module.isparta.FileWriter.prototype)
1.  [function <span class="apidocSignatureSpan">isparta.FileWriter.prototype.</span>copyFile (source, dest)](#apidoc.element.isparta.FileWriter.prototype.copyFile)
1.  [function <span class="apidocSignatureSpan">isparta.FileWriter.prototype.</span>done ()](#apidoc.element.isparta.FileWriter.prototype.done)
1.  [function <span class="apidocSignatureSpan">isparta.FileWriter.prototype.</span>writeFile (file, callback)](#apidoc.element.isparta.FileWriter.prototype.writeFile)

#### [module isparta.Report](#apidoc.module.isparta.Report)
1.  [function <span class="apidocSignatureSpan">isparta.</span>Report ()](#apidoc.element.isparta.Report.Report)
1.  [function <span class="apidocSignatureSpan">isparta.Report.</span>create ()](#apidoc.element.isparta.Report.create)
1.  [function <span class="apidocSignatureSpan">isparta.Report.</span>getReportList ()](#apidoc.element.isparta.Report.getReportList)
1.  [function <span class="apidocSignatureSpan">isparta.Report.</span>loadAll ()](#apidoc.element.isparta.Report.loadAll)
1.  [function <span class="apidocSignatureSpan">isparta.Report.</span>mix (cons, proto)](#apidoc.element.isparta.Report.mix)
1.  [function <span class="apidocSignatureSpan">isparta.Report.</span>register ()](#apidoc.element.isparta.Report.register)
1.  [function <span class="apidocSignatureSpan">isparta.Report.</span>super_ ()](#apidoc.element.isparta.Report.super_)

#### [module isparta.Report.prototype](#apidoc.module.isparta.Report.prototype)
1.  [function <span class="apidocSignatureSpan">isparta.Report.prototype.</span>getDefaultConfig ()](#apidoc.element.isparta.Report.prototype.getDefaultConfig)
1.  [function <span class="apidocSignatureSpan">isparta.Report.prototype.</span>synopsis ()](#apidoc.element.isparta.Report.prototype.synopsis)
1.  [function <span class="apidocSignatureSpan">isparta.Report.prototype.</span>writeReport ()](#apidoc.element.isparta.Report.prototype.writeReport)

#### [module isparta.Reporter](#apidoc.module.isparta.Reporter)
1.  [function <span class="apidocSignatureSpan">isparta.</span>Reporter (cfg, dir)](#apidoc.element.isparta.Reporter.Reporter)

#### [module isparta.Reporter.prototype](#apidoc.module.isparta.Reporter.prototype)
1.  [function <span class="apidocSignatureSpan">isparta.Reporter.prototype.</span>add (fmt)](#apidoc.element.isparta.Reporter.prototype.add)
1.  [function <span class="apidocSignatureSpan">isparta.Reporter.prototype.</span>addAll (fmts)](#apidoc.element.isparta.Reporter.prototype.addAll)
1.  [function <span class="apidocSignatureSpan">isparta.Reporter.prototype.</span>handleDone (callback)](#apidoc.element.isparta.Reporter.prototype.handleDone)
1.  [function <span class="apidocSignatureSpan">isparta.Reporter.prototype.</span>write (collector, sync, callback)](#apidoc.element.isparta.Reporter.prototype.write)

#### [module isparta.Store](#apidoc.module.isparta.Store)
1.  [function <span class="apidocSignatureSpan">isparta.</span>Store ()](#apidoc.element.isparta.Store.Store)
1.  [function <span class="apidocSignatureSpan">isparta.Store.</span>create ()](#apidoc.element.isparta.Store.create)
1.  [function <span class="apidocSignatureSpan">isparta.Store.</span>getStoreList ()](#apidoc.element.isparta.Store.getStoreList)
1.  [function <span class="apidocSignatureSpan">isparta.Store.</span>loadAll ()](#apidoc.element.isparta.Store.loadAll)
1.  [function <span class="apidocSignatureSpan">isparta.Store.</span>mix (cons, proto)](#apidoc.element.isparta.Store.mix)
1.  [function <span class="apidocSignatureSpan">isparta.Store.</span>register ()](#apidoc.element.isparta.Store.register)

#### [module isparta.Store.prototype](#apidoc.module.isparta.Store.prototype)
1.  [function <span class="apidocSignatureSpan">isparta.Store.prototype.</span>dispose ()](#apidoc.element.isparta.Store.prototype.dispose)
1.  [function <span class="apidocSignatureSpan">isparta.Store.prototype.</span>get ()](#apidoc.element.isparta.Store.prototype.get)
1.  [function <span class="apidocSignatureSpan">isparta.Store.prototype.</span>getObject (key)](#apidoc.element.isparta.Store.prototype.getObject)
1.  [function <span class="apidocSignatureSpan">isparta.Store.prototype.</span>hasKey ()](#apidoc.element.isparta.Store.prototype.hasKey)
1.  [function <span class="apidocSignatureSpan">isparta.Store.prototype.</span>keys ()](#apidoc.element.isparta.Store.prototype.keys)
1.  [function <span class="apidocSignatureSpan">isparta.Store.prototype.</span>set ()](#apidoc.element.isparta.Store.prototype.set)
1.  [function <span class="apidocSignatureSpan">isparta.Store.prototype.</span>setObject (key, object)](#apidoc.element.isparta.Store.prototype.setObject)

#### [module isparta.TreeSummarizer](#apidoc.module.isparta.TreeSummarizer)
1.  [function <span class="apidocSignatureSpan">isparta.</span>TreeSummarizer ()](#apidoc.element.isparta.TreeSummarizer.TreeSummarizer)

#### [module isparta.TreeSummarizer.prototype](#apidoc.module.isparta.TreeSummarizer.prototype)
1.  [function <span class="apidocSignatureSpan">isparta.TreeSummarizer.prototype.</span>addFileCoverageSummary (filePath, metrics)](#apidoc.element.isparta.TreeSummarizer.prototype.addFileCoverageSummary)
1.  [function <span class="apidocSignatureSpan">isparta.TreeSummarizer.prototype.</span>getTreeSummary ()](#apidoc.element.isparta.TreeSummarizer.prototype.getTreeSummary)

#### [module isparta.Writer](#apidoc.module.isparta.Writer)
1.  [function <span class="apidocSignatureSpan">isparta.</span>Writer ()](#apidoc.element.isparta.Writer.Writer)
1.  [function <span class="apidocSignatureSpan">isparta.Writer.</span>super_ ()](#apidoc.element.isparta.Writer.super_)

#### [module isparta.Writer.prototype](#apidoc.module.isparta.Writer.prototype)
1.  [function <span class="apidocSignatureSpan">isparta.Writer.prototype.</span>copyFile ()](#apidoc.element.isparta.Writer.prototype.copyFile)
1.  [function <span class="apidocSignatureSpan">isparta.Writer.prototype.</span>done ()](#apidoc.element.isparta.Writer.prototype.done)
1.  [function <span class="apidocSignatureSpan">isparta.Writer.prototype.</span>writeFile ()](#apidoc.element.isparta.Writer.prototype.writeFile)

#### [module isparta.config](#apidoc.module.isparta.config)
1.  [function <span class="apidocSignatureSpan">isparta.config.</span>defaultConfig (includeBackCompatAttrs)](#apidoc.element.isparta.config.defaultConfig)
1.  [function <span class="apidocSignatureSpan">isparta.config.</span>loadFile (file, overrides)](#apidoc.element.isparta.config.loadFile)
1.  [function <span class="apidocSignatureSpan">isparta.config.</span>loadObject (obj, overrides)](#apidoc.element.isparta.config.loadObject)

#### [module isparta.hook](#apidoc.module.isparta.hook)
1.  [function <span class="apidocSignatureSpan">isparta.hook.</span>hookCreateScript (matcher, transformer, opts)](#apidoc.element.isparta.hook.hookCreateScript)
1.  [function <span class="apidocSignatureSpan">isparta.hook.</span>hookRequire (matcher, transformer, options)](#apidoc.element.isparta.hook.hookRequire)
1.  [function <span class="apidocSignatureSpan">isparta.hook.</span>hookRunInThisContext (matcher, transformer, opts)](#apidoc.element.isparta.hook.hookRunInThisContext)
1.  [function <span class="apidocSignatureSpan">isparta.hook.</span>unhookCreateScript ()](#apidoc.element.isparta.hook.unhookCreateScript)
1.  [function <span class="apidocSignatureSpan">isparta.hook.</span>unhookRequire ()](#apidoc.element.isparta.hook.unhookRequire)
1.  [function <span class="apidocSignatureSpan">isparta.hook.</span>unhookRunInThisContext ()](#apidoc.element.isparta.hook.unhookRunInThisContext)
1.  [function <span class="apidocSignatureSpan">isparta.hook.</span>unloadRequireCache (matcher)](#apidoc.element.isparta.hook.unloadRequireCache)

#### [module isparta.instrumenter](#apidoc.module.isparta.instrumenter)
1.  [function <span class="apidocSignatureSpan">isparta.instrumenter.</span>Instrumenter ()](#apidoc.element.isparta.instrumenter.Instrumenter)

#### [module isparta.utils](#apidoc.module.isparta.utils)
1.  [function <span class="apidocSignatureSpan">isparta.utils.</span>addDerivedInfo (coverage)](#apidoc.element.isparta.utils.addDerivedInfo)
1.  [function <span class="apidocSignatureSpan">isparta.utils.</span>addDerivedInfoForFile (fileCoverage)](#apidoc.element.isparta.utils.addDerivedInfoForFile)
1.  [function <span class="apidocSignatureSpan">isparta.utils.</span>blankSummary ()](#apidoc.element.isparta.utils.blankSummary)
1.  [function <span class="apidocSignatureSpan">isparta.utils.</span>incrementIgnoredTotals (cov)](#apidoc.element.isparta.utils.incrementIgnoredTotals)
1.  [function <span class="apidocSignatureSpan">isparta.utils.</span>mergeFileCoverage (first, second)](#apidoc.element.isparta.utils.mergeFileCoverage)
1.  [function <span class="apidocSignatureSpan">isparta.utils.</span>mergeSummaryObjects ()](#apidoc.element.isparta.utils.mergeSummaryObjects)
1.  [function <span class="apidocSignatureSpan">isparta.utils.</span>removeDerivedInfo (coverage)](#apidoc.element.isparta.utils.removeDerivedInfo)
1.  [function <span class="apidocSignatureSpan">isparta.utils.</span>summarizeCoverage (coverage)](#apidoc.element.isparta.utils.summarizeCoverage)
1.  [function <span class="apidocSignatureSpan">isparta.utils.</span>summarizeFileCoverage (fileCoverage)](#apidoc.element.isparta.utils.summarizeFileCoverage)
1.  [function <span class="apidocSignatureSpan">isparta.utils.</span>toYUICoverage (coverage)](#apidoc.element.isparta.utils.toYUICoverage)



# <a name="apidoc.module.isparta"></a>[module isparta](#apidoc.module.isparta)

#### <a name="apidoc.element.isparta.Collector"></a>[function <span class="apidocSignatureSpan">isparta.</span>Collector (options)](#apidoc.element.isparta.Collector)
- description and source-code
```javascript
function Collector(options) {
    options = options || {};
    this.store = options.store || new MemoryStore();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.ContentWriter"></a>[function <span class="apidocSignatureSpan">isparta.</span>ContentWriter ()](#apidoc.element.isparta.ContentWriter)
- description and source-code
```javascript
function ContentWriter() {
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.FileWriter"></a>[function <span class="apidocSignatureSpan">isparta.</span>FileWriter (sync)](#apidoc.element.isparta.FileWriter)
- description and source-code
```javascript
function FileWriter(sync) {
    Writer.call(this);
    var that = this;
    this.delegate = sync ? new SyncFileWriter() : new AsyncFileWriter();
    this.delegate.on('error', function (err) { that.emit('error', err); });
    this.delegate.on('done', function () { that.emit('done'); });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Instrumenter"></a>[function <span class="apidocSignatureSpan">isparta.</span>Instrumenter ()](#apidoc.element.isparta.Instrumenter)
- description and source-code
```javascript
function Instrumenter() {
  var options = arguments.length <= 0 || arguments[0] === undefined ? {} : arguments[0];

  _classCallCheck(this, Instrumenter);

  var _this = _possibleConstructorReturn(this, Object.getPrototypeOf(Instrumenter).call(this));

  _istanbul2.default.Instrumenter.call(_this, options);

  _this.babelOptions = _extends({
    sourceMap: true
  }, options && options.babel || {});
  return _this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Report"></a>[function <span class="apidocSignatureSpan">isparta.</span>Report ()](#apidoc.element.isparta.Report)
- description and source-code
```javascript
function Report() {
    EventEmitter.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Reporter"></a>[function <span class="apidocSignatureSpan">isparta.</span>Reporter (cfg, dir)](#apidoc.element.isparta.Reporter)
- description and source-code
```javascript
function Reporter(cfg, dir) {
    this.config = cfg || configuration.loadFile();
    this.dir = dir || this.config.reporting.dir();
    this.reports = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Store"></a>[function <span class="apidocSignatureSpan">isparta.</span>Store ()](#apidoc.element.isparta.Store)
- description and source-code
```javascript
function Store() {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.TreeSummarizer"></a>[function <span class="apidocSignatureSpan">isparta.</span>TreeSummarizer ()](#apidoc.element.isparta.TreeSummarizer)
- description and source-code
```javascript
function TreeSummarizer() {
    this.summaryMap = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Writer"></a>[function <span class="apidocSignatureSpan">isparta.</span>Writer ()](#apidoc.element.isparta.Writer)
- description and source-code
```javascript
function Writer() {
    EventEmitter.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta._yuiLoadHook"></a>[function <span class="apidocSignatureSpan">isparta.</span>_yuiLoadHook (matchFn, transformFn, verbose)](#apidoc.element.isparta._yuiLoadHook)
- description and source-code
```javascript
_yuiLoadHook = function (matchFn, transformFn, verbose) {
    return function (file) {
        if (!file.match(yuiRegexp)) {
            return;
        }
        var YMain = require(file),
            YUI,
            loaderFn,
            origGet;

        if (YMain.YUI) {
            YUI = YMain.YUI;
            loaderFn = YUI.Env && YUI.Env.mods && YUI.Env.mods['loader-base'] ? YUI.Env.mods['loader-base'].fn : null;
            if (!loaderFn) { return; }
            if (verbose) { console.log('Applying YUI load post-hook'); }
            YUI.Env.mods['loader-base'].fn = function (Y) {
                loaderFn.call(null, Y);
                origGet = Y.Get._exec;
                Y.Get._exec = function (data, url, cb) {
                    if (matchFn(url) || matchFn(path.resolve(url))) { //allow for relative paths as well
                        if (verbose) {
                            console.log('Transforming [' + url + ']');
                        }
                        try {
                            data = transformFn(data, url);
                        } catch (ex) {
                            console.error('Error transforming: ' + url + ' return original code');
                            console.error(ex.message || ex);
                            if (ex.stack) { console.error(ex.stack); }
                        }
                    }
                    return origGet.call(Y, data, url, cb);
                };
                return Y;
            };
        }
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.matcherFor"></a>[function <span class="apidocSignatureSpan">isparta.</span>matcherFor (options, callback)](#apidoc.element.isparta.matcherFor)
- description and source-code
```javascript
function matcherFor(options, callback) {

    if (!callback && typeof options === 'function') {
        callback = options;
        options = null;
    }
    options = options || {};
    options.relative = false; //force absolute paths
    options.realpath = true; //force real paths (to match Node.js module paths)

    filesFor(options, function (err, files) {
        var fileMap = {},
            matchFn;
        if (err) { return callback(err); }
        files.forEach(function (file) { fileMap[file] = true; });

        matchFn = function (file) { return fileMap[file]; };
        matchFn.files = Object.keys(fileMap);
        return callback(null, matchFn);
    });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.isparta.Collector"></a>[module isparta.Collector](#apidoc.module.isparta.Collector)

#### <a name="apidoc.element.isparta.Collector.Collector"></a>[function <span class="apidocSignatureSpan">isparta.</span>Collector (options)](#apidoc.element.isparta.Collector.Collector)
- description and source-code
```javascript
function Collector(options) {
    options = options || {};
    this.store = options.store || new MemoryStore();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.isparta.Collector.prototype"></a>[module isparta.Collector.prototype](#apidoc.module.isparta.Collector.prototype)

#### <a name="apidoc.element.isparta.Collector.prototype.add"></a>[function <span class="apidocSignatureSpan">isparta.Collector.prototype.</span>add (coverage)](#apidoc.element.isparta.Collector.prototype.add)
- description and source-code
```javascript
add = function (coverage) {
    var store = this.store;
    Object.keys(coverage).forEach(function (key) {
        var fileCoverage = coverage[key];
        if (store.hasKey(key)) {
            store.setObject(key, utils.mergeFileCoverage(fileCoverage, store.getObject(key)));
        } else {
            store.setObject(key, fileCoverage);
        }
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Collector.prototype.dispose"></a>[function <span class="apidocSignatureSpan">isparta.Collector.prototype.</span>dispose ()](#apidoc.element.isparta.Collector.prototype.dispose)
- description and source-code
```javascript
dispose = function () {
    this.store.dispose();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Collector.prototype.fileCoverageFor"></a>[function <span class="apidocSignatureSpan">isparta.Collector.prototype.</span>fileCoverageFor (fileName)](#apidoc.element.isparta.Collector.prototype.fileCoverageFor)
- description and source-code
```javascript
fileCoverageFor = function (fileName) {
    var ret = this.store.getObject(fileName);
    utils.addDerivedInfoForFile(ret);
    return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Collector.prototype.files"></a>[function <span class="apidocSignatureSpan">isparta.Collector.prototype.</span>files ()](#apidoc.element.isparta.Collector.prototype.files)
- description and source-code
```javascript
files = function () {
    return this.store.keys();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Collector.prototype.getFinalCoverage"></a>[function <span class="apidocSignatureSpan">isparta.Collector.prototype.</span>getFinalCoverage ()](#apidoc.element.isparta.Collector.prototype.getFinalCoverage)
- description and source-code
```javascript
getFinalCoverage = function () {
    var ret = {},
        that = this;
    this.files().forEach(function (file) {
        ret[file] = that.fileCoverageFor(file);
    });
    return ret;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.isparta.ContentWriter"></a>[module isparta.ContentWriter](#apidoc.module.isparta.ContentWriter)

#### <a name="apidoc.element.isparta.ContentWriter.ContentWriter"></a>[function <span class="apidocSignatureSpan">isparta.</span>ContentWriter ()](#apidoc.element.isparta.ContentWriter.ContentWriter)
- description and source-code
```javascript
function ContentWriter() {
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.isparta.ContentWriter.prototype"></a>[module isparta.ContentWriter.prototype](#apidoc.module.isparta.ContentWriter.prototype)

#### <a name="apidoc.element.isparta.ContentWriter.prototype.println"></a>[function <span class="apidocSignatureSpan">isparta.ContentWriter.prototype.</span>println (str)](#apidoc.element.isparta.ContentWriter.prototype.println)
- description and source-code
```javascript
println = function (str) { this.write(str + '\n'); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.ContentWriter.prototype.write"></a>[function <span class="apidocSignatureSpan">isparta.ContentWriter.prototype.</span>write ()](#apidoc.element.isparta.ContentWriter.prototype.write)
- description and source-code
```javascript
write = function () {
    throw new Error('write: must be overridden');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.isparta.FileWriter"></a>[module isparta.FileWriter](#apidoc.module.isparta.FileWriter)

#### <a name="apidoc.element.isparta.FileWriter.FileWriter"></a>[function <span class="apidocSignatureSpan">isparta.</span>FileWriter (sync)](#apidoc.element.isparta.FileWriter.FileWriter)
- description and source-code
```javascript
function FileWriter(sync) {
    Writer.call(this);
    var that = this;
    this.delegate = sync ? new SyncFileWriter() : new AsyncFileWriter();
    this.delegate.on('error', function (err) { that.emit('error', err); });
    this.delegate.on('done', function () { that.emit('done'); });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.FileWriter.super_"></a>[function <span class="apidocSignatureSpan">isparta.FileWriter.</span>super_ ()](#apidoc.element.isparta.FileWriter.super_)
- description and source-code
```javascript
function Writer() {
    EventEmitter.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.isparta.FileWriter.prototype"></a>[module isparta.FileWriter.prototype](#apidoc.module.isparta.FileWriter.prototype)

#### <a name="apidoc.element.isparta.FileWriter.prototype.copyFile"></a>[function <span class="apidocSignatureSpan">isparta.FileWriter.prototype.</span>copyFile (source, dest)](#apidoc.element.isparta.FileWriter.prototype.copyFile)
- description and source-code
```javascript
copyFile = function (source, dest) {
    mkdirp.sync(path.dirname(dest));
    fs.writeFileSync(dest, fs.readFileSync(source));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.FileWriter.prototype.done"></a>[function <span class="apidocSignatureSpan">isparta.FileWriter.prototype.</span>done ()](#apidoc.element.isparta.FileWriter.prototype.done)
- description and source-code
```javascript
done = function () {
    this.delegate.done();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.FileWriter.prototype.writeFile"></a>[function <span class="apidocSignatureSpan">isparta.FileWriter.prototype.</span>writeFile (file, callback)](#apidoc.element.isparta.FileWriter.prototype.writeFile)
- description and source-code
```javascript
writeFile = function (file, callback) {
    this.delegate.writeFile(file, callback);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.isparta.Report"></a>[module isparta.Report](#apidoc.module.isparta.Report)

#### <a name="apidoc.element.isparta.Report.Report"></a>[function <span class="apidocSignatureSpan">isparta.</span>Report ()](#apidoc.element.isparta.Report.Report)
- description and source-code
```javascript
function Report() {
    EventEmitter.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Report.create"></a>[function <span class="apidocSignatureSpan">isparta.Report.</span>create ()](#apidoc.element.isparta.Report.create)
- description and source-code
```javascript
create = function () { [native code] }
```
- example usage
```shell
...

function _interopRequireDefault(obj) { return obj && obj.__esModule ? obj : { default: obj }; }

function _classCallCheck(instance, Constructor) { if (!(instance instanceof Constructor)) { throw new TypeError("Cannot call a class
 as a function"); } }

function _possibleConstructorReturn(self, call) { if (!self) { throw new ReferenceError("this hasn't been initialised - super()
hasn't been called"); } return call && (typeof call === "object" || typeof call === "function") ? call : self; }

function _inherits(subClass, superClass) { if (typeof superClass !== "function" && superClass !== null) { throw new TypeError("Super
 expression must either be null or a function, not " + typeof superClass); } subClass.prototype = Object.create(superClass && superClass
.prototype, { constructor: { value: subClass, enumerable: false, writable: true, configurable: true } }); if (superClass) Object
.setPrototypeOf ? Object.setPrototypeOf(subClass, superClass) : subClass.__proto__ = superClass; } //

var POSITIONS = ['start', 'end'];

var Instrumenter = exports.Instrumenter = (function (_istanbul$Instrumente) {
_inherits(Instrumenter, _istanbul$Instrumente);

function Instrumenter() {
...
```

#### <a name="apidoc.element.isparta.Report.getReportList"></a>[function <span class="apidocSignatureSpan">isparta.Report.</span>getReportList ()](#apidoc.element.isparta.Report.getReportList)
- description and source-code
```javascript
getReportList = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Report.loadAll"></a>[function <span class="apidocSignatureSpan">isparta.Report.</span>loadAll ()](#apidoc.element.isparta.Report.loadAll)
- description and source-code
```javascript
loadAll = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Report.mix"></a>[function <span class="apidocSignatureSpan">isparta.Report.</span>mix (cons, proto)](#apidoc.element.isparta.Report.mix)
- description and source-code
```javascript
mix = function (cons, proto) {
    Object.keys(proto).forEach(function (key) {
        cons.prototype[key] = proto[key];
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Report.register"></a>[function <span class="apidocSignatureSpan">isparta.Report.</span>register ()](#apidoc.element.isparta.Report.register)
- description and source-code
```javascript
register = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Report.super_"></a>[function <span class="apidocSignatureSpan">isparta.Report.</span>super_ ()](#apidoc.element.isparta.Report.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.isparta.Report.prototype"></a>[module isparta.Report.prototype](#apidoc.module.isparta.Report.prototype)

#### <a name="apidoc.element.isparta.Report.prototype.getDefaultConfig"></a>[function <span class="apidocSignatureSpan">isparta.Report.prototype.</span>getDefaultConfig ()](#apidoc.element.isparta.Report.prototype.getDefaultConfig)
- description and source-code
```javascript
getDefaultConfig = function () {
    return null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Report.prototype.synopsis"></a>[function <span class="apidocSignatureSpan">isparta.Report.prototype.</span>synopsis ()](#apidoc.element.isparta.Report.prototype.synopsis)
- description and source-code
```javascript
synopsis = function () {
    throw new Error('synopsis must be overridden');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Report.prototype.writeReport"></a>[function <span class="apidocSignatureSpan">isparta.Report.prototype.</span>writeReport ()](#apidoc.element.isparta.Report.prototype.writeReport)
- description and source-code
```javascript
writeReport = function () {
    throw new Error('writeReport: must be overridden');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.isparta.Reporter"></a>[module isparta.Reporter](#apidoc.module.isparta.Reporter)

#### <a name="apidoc.element.isparta.Reporter.Reporter"></a>[function <span class="apidocSignatureSpan">isparta.</span>Reporter (cfg, dir)](#apidoc.element.isparta.Reporter.Reporter)
- description and source-code
```javascript
function Reporter(cfg, dir) {
    this.config = cfg || configuration.loadFile();
    this.dir = dir || this.config.reporting.dir();
    this.reports = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.isparta.Reporter.prototype"></a>[module isparta.Reporter.prototype](#apidoc.module.isparta.Reporter.prototype)

#### <a name="apidoc.element.isparta.Reporter.prototype.add"></a>[function <span class="apidocSignatureSpan">isparta.Reporter.prototype.</span>add (fmt)](#apidoc.element.isparta.Reporter.prototype.add)
- description and source-code
```javascript
add = function (fmt) {
    if (this.reports[fmt]) { // already added
        return;
    }
    var config = this.config,
        rptConfig = config.reporting.reportConfig()[fmt] || {};
    rptConfig.verbose = config.verbose;
    rptConfig.dir = this.dir;
    rptConfig.watermarks = config.reporting.watermarks();
    try {
        this.reports[fmt] = Report.create(fmt, rptConfig);
    } catch (ex) {
        throw inputError.create('Invalid report format [' + fmt + ']');
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Reporter.prototype.addAll"></a>[function <span class="apidocSignatureSpan">isparta.Reporter.prototype.</span>addAll (fmts)](#apidoc.element.isparta.Reporter.prototype.addAll)
- description and source-code
```javascript
addAll = function (fmts) {
    var that = this;
    fmts.forEach(function (f) {
        that.add(f);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Reporter.prototype.handleDone"></a>[function <span class="apidocSignatureSpan">isparta.Reporter.prototype.</span>handleDone (callback)](#apidoc.element.isparta.Reporter.prototype.handleDone)
- description and source-code
```javascript
handleDone = function (callback) {
    this.inProgress -= 1;
    if (this.inProgress === 0) {
        return callback();
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Reporter.prototype.write"></a>[function <span class="apidocSignatureSpan">isparta.Reporter.prototype.</span>write (collector, sync, callback)](#apidoc.element.isparta.Reporter.prototype.write)
- description and source-code
```javascript
write = function (collector, sync, callback) {
    var reports = this.reports,
        verbose = this.config.verbose,
        handler = this.handleDone.bind(this, callback);

    this.inProgress = Object.keys(reports).length;

    Object.keys(reports).forEach(function (name) {
        var report = reports[name];
        if (verbose) {
            console.error('Write report: ' + name);
        }
        report.on('done', handler);
        report.writeReport(collector, sync);
    });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.isparta.Store"></a>[module isparta.Store](#apidoc.module.isparta.Store)

#### <a name="apidoc.element.isparta.Store.Store"></a>[function <span class="apidocSignatureSpan">isparta.</span>Store ()](#apidoc.element.isparta.Store.Store)
- description and source-code
```javascript
function Store() {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Store.create"></a>[function <span class="apidocSignatureSpan">isparta.Store.</span>create ()](#apidoc.element.isparta.Store.create)
- description and source-code
```javascript
create = function () { [native code] }
```
- example usage
```shell
...

function _interopRequireDefault(obj) { return obj && obj.__esModule ? obj : { default: obj }; }

function _classCallCheck(instance, Constructor) { if (!(instance instanceof Constructor)) { throw new TypeError("Cannot call a class
 as a function"); } }

function _possibleConstructorReturn(self, call) { if (!self) { throw new ReferenceError("this hasn't been initialised - super()
hasn't been called"); } return call && (typeof call === "object" || typeof call === "function") ? call : self; }

function _inherits(subClass, superClass) { if (typeof superClass !== "function" && superClass !== null) { throw new TypeError("Super
 expression must either be null or a function, not " + typeof superClass); } subClass.prototype = Object.create(superClass && superClass
.prototype, { constructor: { value: subClass, enumerable: false, writable: true, configurable: true } }); if (superClass) Object
.setPrototypeOf ? Object.setPrototypeOf(subClass, superClass) : subClass.__proto__ = superClass; } //

var POSITIONS = ['start', 'end'];

var Instrumenter = exports.Instrumenter = (function (_istanbul$Instrumente) {
_inherits(Instrumenter, _istanbul$Instrumente);

function Instrumenter() {
...
```

#### <a name="apidoc.element.isparta.Store.getStoreList"></a>[function <span class="apidocSignatureSpan">isparta.Store.</span>getStoreList ()](#apidoc.element.isparta.Store.getStoreList)
- description and source-code
```javascript
getStoreList = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Store.loadAll"></a>[function <span class="apidocSignatureSpan">isparta.Store.</span>loadAll ()](#apidoc.element.isparta.Store.loadAll)
- description and source-code
```javascript
loadAll = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Store.mix"></a>[function <span class="apidocSignatureSpan">isparta.Store.</span>mix (cons, proto)](#apidoc.element.isparta.Store.mix)
- description and source-code
```javascript
mix = function (cons, proto) {
    Object.keys(proto).forEach(function (key) {
        cons.prototype[key] = proto[key];
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Store.register"></a>[function <span class="apidocSignatureSpan">isparta.Store.</span>register ()](#apidoc.element.isparta.Store.register)
- description and source-code
```javascript
register = function () { [native code] }
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.isparta.Store.prototype"></a>[module isparta.Store.prototype](#apidoc.module.isparta.Store.prototype)

#### <a name="apidoc.element.isparta.Store.prototype.dispose"></a>[function <span class="apidocSignatureSpan">isparta.Store.prototype.</span>dispose ()](#apidoc.element.isparta.Store.prototype.dispose)
- description and source-code
```javascript
dispose = function () {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Store.prototype.get"></a>[function <span class="apidocSignatureSpan">isparta.Store.prototype.</span>get ()](#apidoc.element.isparta.Store.prototype.get)
- description and source-code
```javascript
get = function () { throw new Error("get: must be overridden"); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Store.prototype.getObject"></a>[function <span class="apidocSignatureSpan">isparta.Store.prototype.</span>getObject (key)](#apidoc.element.isparta.Store.prototype.getObject)
- description and source-code
```javascript
getObject = function (key) {
    return JSON.parse(this.get(key));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Store.prototype.hasKey"></a>[function <span class="apidocSignatureSpan">isparta.Store.prototype.</span>hasKey ()](#apidoc.element.isparta.Store.prototype.hasKey)
- description and source-code
```javascript
hasKey = function () { throw new Error("hasKey: must be overridden"); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Store.prototype.keys"></a>[function <span class="apidocSignatureSpan">isparta.Store.prototype.</span>keys ()](#apidoc.element.isparta.Store.prototype.keys)
- description and source-code
```javascript
keys = function () { throw new Error("keys: must be overridden"); }
```
- example usage
```shell
...
    ////

  }, {
    key: '_statementMapTransformer',
    value: function _statementMapTransformer(metrics) {
      var _this3 = this;

      return Object.keys(metrics).map(function (index) {
return metrics[index];
      }).map(function (statementMeta) {
var _getMetricOriginalLoc = _this3._getMetricOriginalLocations([statementMeta]);

var _getMetricOriginalLoc2 = _slicedToArray(_getMetricOriginalLoc, 1);

var location = _getMetricOriginalLoc2[0];
...
```

#### <a name="apidoc.element.isparta.Store.prototype.set"></a>[function <span class="apidocSignatureSpan">isparta.Store.prototype.</span>set ()](#apidoc.element.isparta.Store.prototype.set)
- description and source-code
```javascript
set = function () { throw new Error("set: must be overridden"); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Store.prototype.setObject"></a>[function <span class="apidocSignatureSpan">isparta.Store.prototype.</span>setObject (key, object)](#apidoc.element.isparta.Store.prototype.setObject)
- description and source-code
```javascript
setObject = function (key, object) {
    return this.set(key, JSON.stringify(object));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.isparta.TreeSummarizer"></a>[module isparta.TreeSummarizer](#apidoc.module.isparta.TreeSummarizer)

#### <a name="apidoc.element.isparta.TreeSummarizer.TreeSummarizer"></a>[function <span class="apidocSignatureSpan">isparta.</span>TreeSummarizer ()](#apidoc.element.isparta.TreeSummarizer.TreeSummarizer)
- description and source-code
```javascript
function TreeSummarizer() {
    this.summaryMap = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.isparta.TreeSummarizer.prototype"></a>[module isparta.TreeSummarizer.prototype](#apidoc.module.isparta.TreeSummarizer.prototype)

#### <a name="apidoc.element.isparta.TreeSummarizer.prototype.addFileCoverageSummary"></a>[function <span class="apidocSignatureSpan">isparta.TreeSummarizer.prototype.</span>addFileCoverageSummary (filePath, metrics)](#apidoc.element.isparta.TreeSummarizer.prototype.addFileCoverageSummary)
- description and source-code
```javascript
addFileCoverageSummary = function (filePath, metrics) {
    this.summaryMap[filePath] = metrics;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.TreeSummarizer.prototype.getTreeSummary"></a>[function <span class="apidocSignatureSpan">isparta.TreeSummarizer.prototype.</span>getTreeSummary ()](#apidoc.element.isparta.TreeSummarizer.prototype.getTreeSummary)
- description and source-code
```javascript
getTreeSummary = function () {
    var commonArrayPrefix = findCommonArrayPrefix(Object.keys(this.summaryMap));
    return new TreeSummary(this.summaryMap, commonArrayPrefix);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.isparta.Writer"></a>[module isparta.Writer](#apidoc.module.isparta.Writer)

#### <a name="apidoc.element.isparta.Writer.Writer"></a>[function <span class="apidocSignatureSpan">isparta.</span>Writer ()](#apidoc.element.isparta.Writer.Writer)
- description and source-code
```javascript
function Writer() {
    EventEmitter.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Writer.super_"></a>[function <span class="apidocSignatureSpan">isparta.Writer.</span>super_ ()](#apidoc.element.isparta.Writer.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.isparta.Writer.prototype"></a>[module isparta.Writer.prototype](#apidoc.module.isparta.Writer.prototype)

#### <a name="apidoc.element.isparta.Writer.prototype.copyFile"></a>[function <span class="apidocSignatureSpan">isparta.Writer.prototype.</span>copyFile ()](#apidoc.element.isparta.Writer.prototype.copyFile)
- description and source-code
```javascript
copyFile = function () {
    throw new Error('copyFile: must be overridden');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Writer.prototype.done"></a>[function <span class="apidocSignatureSpan">isparta.Writer.prototype.</span>done ()](#apidoc.element.isparta.Writer.prototype.done)
- description and source-code
```javascript
done = function () {
    throw new Error('done: must be overridden');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.Writer.prototype.writeFile"></a>[function <span class="apidocSignatureSpan">isparta.Writer.prototype.</span>writeFile ()](#apidoc.element.isparta.Writer.prototype.writeFile)
- description and source-code
```javascript
writeFile = function () {
    throw new Error('writeFile: must be overridden');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.isparta.config"></a>[module isparta.config](#apidoc.module.isparta.config)

#### <a name="apidoc.element.isparta.config.defaultConfig"></a>[function <span class="apidocSignatureSpan">isparta.config.</span>defaultConfig (includeBackCompatAttrs)](#apidoc.element.isparta.config.defaultConfig)
- description and source-code
```javascript
function defaultConfig(includeBackCompatAttrs) {
    var ret = {
        verbose: false,
        instrumentation: {
            root: '.',
            extensions: ['.js'],
            'default-excludes': true,
            excludes: [],
            'embed-source': false,
            variable: '__coverage__',
            compact: true,
            'preserve-comments': false,
            'complete-copy': false,
            'save-baseline': false,
            'baseline-file': './coverage/coverage-baseline.json',
            'include-all-sources': false,
            'include-pid': false,
            'es-modules': false
        },
        reporting: {
            print: 'summary',
            reports: [ 'lcov' ],
            dir: './coverage'
        },
        hooks: {
            'hook-run-in-context': false,
            'post-require-hook': null,
            'handle-sigint': false
        },
        check: {
            global: {
                statements: 0,
                lines: 0,
                branches: 0,
                functions: 0,
                excludes: [] // Currently list of files (root + path). For future, extend to patterns.
            },
            each: {
                statements: 0,
                lines: 0,
                branches: 0,
                functions: 0,
                excludes: []
            }
        }
    };
    ret.reporting.watermarks = defaults.watermarks();
    ret.reporting['report-config'] = defaults.defaultReportConfig();

    if (includeBackCompatAttrs) {
        ret.instrumentation['preload-sources'] = false;
    }

    return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.config.loadFile"></a>[function <span class="apidocSignatureSpan">isparta.config.</span>loadFile (file, overrides)](#apidoc.element.isparta.config.loadFile)
- description and source-code
```javascript
function loadFile(file, overrides) {
    var defaultConfigFile = path.resolve('.istanbul.yml'),
        configObject;

    if (file) {
        if (!existsSync(file)) {
            throw new Error('Invalid configuration file specified:' + file);
        }
    } else {
        if (existsSync(defaultConfigFile)) {
            file = defaultConfigFile;
        }
    }

    if (file) {
        if (overrides && overrides.verbose === true) {
            console.error('Loading config: ' + file);
        }
        configObject = file.match(YML_PATTERN) ?
            yaml.safeLoad(fs.readFileSync(file, 'utf8'), { filename: file }) :
            require(path.resolve(file));
    }

    return new Configuration(configObject, overrides);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.config.loadObject"></a>[function <span class="apidocSignatureSpan">isparta.config.</span>loadObject (obj, overrides)](#apidoc.element.isparta.config.loadObject)
- description and source-code
```javascript
function loadObject(obj, overrides) {
    return new Configuration(obj, overrides);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.isparta.hook"></a>[module isparta.hook](#apidoc.module.isparta.hook)

#### <a name="apidoc.element.isparta.hook.hookCreateScript"></a>[function <span class="apidocSignatureSpan">isparta.hook.</span>hookCreateScript (matcher, transformer, opts)](#apidoc.element.isparta.hook.hookCreateScript)
- description and source-code
```javascript
function hookCreateScript(matcher, transformer, opts) {
    opts = opts || {};
    var fn = transformFn(matcher, transformer, opts.verbose);
    vm.createScript = function (code, file) {
        var ret = fn(code, file);
        return originalCreateScript(ret.code, file);
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.hook.hookRequire"></a>[function <span class="apidocSignatureSpan">isparta.hook.</span>hookRequire (matcher, transformer, options)](#apidoc.element.isparta.hook.hookRequire)
- description and source-code
```javascript
function hookRequire(matcher, transformer, options) {
    options = options || {};
    var extensions,
        fn = transformFn(matcher, transformer, options.verbose),
        postLoadHook = options.postLoadHook &&
            typeof options.postLoadHook === 'function' ? options.postLoadHook : null;

    extensions = options.extensions || ['.js'];

    extensions.forEach(function(ext){
        if (!(ext in originalLoaders)) {
            originalLoaders[ext] = Module._extensions[ext] || Module._extensions['.js'];
        }
        Module._extensions[ext] = function (module, filename) {
            var ret = fn(fs.readFileSync(filename, 'utf8'), filename);
            if (ret.changed) {
                module._compile(ret.code, filename);
            } else {
                originalLoaders[ext](module, filename);
            }
            if (postLoadHook) {
                postLoadHook(filename);
            }
        };
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.hook.hookRunInThisContext"></a>[function <span class="apidocSignatureSpan">isparta.hook.</span>hookRunInThisContext (matcher, transformer, opts)](#apidoc.element.isparta.hook.hookRunInThisContext)
- description and source-code
```javascript
function hookRunInThisContext(matcher, transformer, opts) {
    opts = opts || {};
    var fn = transformFn(matcher, transformer, opts.verbose);
    vm.runInThisContext = function (code, file) {
        var ret = fn(code, file);
        return originalRunInThisContext(ret.code, file);
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.hook.unhookCreateScript"></a>[function <span class="apidocSignatureSpan">isparta.hook.</span>unhookCreateScript ()](#apidoc.element.isparta.hook.unhookCreateScript)
- description and source-code
```javascript
function unhookCreateScript() {
    vm.createScript = originalCreateScript;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.hook.unhookRequire"></a>[function <span class="apidocSignatureSpan">isparta.hook.</span>unhookRequire ()](#apidoc.element.isparta.hook.unhookRequire)
- description and source-code
```javascript
function unhookRequire() {
    Object.keys(originalLoaders).forEach(function(ext) {
        Module._extensions[ext] = originalLoaders[ext];
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.hook.unhookRunInThisContext"></a>[function <span class="apidocSignatureSpan">isparta.hook.</span>unhookRunInThisContext ()](#apidoc.element.isparta.hook.unhookRunInThisContext)
- description and source-code
```javascript
function unhookRunInThisContext() {
    vm.runInThisContext = originalRunInThisContext;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.hook.unloadRequireCache"></a>[function <span class="apidocSignatureSpan">isparta.hook.</span>unloadRequireCache (matcher)](#apidoc.element.isparta.hook.unloadRequireCache)
- description and source-code
```javascript
function unloadRequireCache(matcher) {
    if (matcher && typeof require !== 'undefined' && require && require.cache) {
        Object.keys(require.cache).forEach(function (filename) {
            if (matcher(filename)) {
                delete require.cache[filename];
            }
        });
    }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.isparta.instrumenter"></a>[module isparta.instrumenter](#apidoc.module.isparta.instrumenter)

#### <a name="apidoc.element.isparta.instrumenter.Instrumenter"></a>[function <span class="apidocSignatureSpan">isparta.instrumenter.</span>Instrumenter ()](#apidoc.element.isparta.instrumenter.Instrumenter)
- description and source-code
```javascript
function Instrumenter() {
  var options = arguments.length <= 0 || arguments[0] === undefined ? {} : arguments[0];

  _classCallCheck(this, Instrumenter);

  var _this = _possibleConstructorReturn(this, Object.getPrototypeOf(Instrumenter).call(this));

  _istanbul2.default.Instrumenter.call(_this, options);

  _this.babelOptions = _extends({
    sourceMap: true
  }, options && options.babel || {});
  return _this;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.isparta.utils"></a>[module isparta.utils](#apidoc.module.isparta.utils)

#### <a name="apidoc.element.isparta.utils.addDerivedInfo"></a>[function <span class="apidocSignatureSpan">isparta.utils.</span>addDerivedInfo (coverage)](#apidoc.element.isparta.utils.addDerivedInfo)
- description and source-code
```javascript
function addDerivedInfo(coverage) {
    Object.keys(coverage).forEach(function (k) {
        addDerivedInfoForFile(coverage[k]);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.utils.addDerivedInfoForFile"></a>[function <span class="apidocSignatureSpan">isparta.utils.</span>addDerivedInfoForFile (fileCoverage)](#apidoc.element.isparta.utils.addDerivedInfoForFile)
- description and source-code
```javascript
function addDerivedInfoForFile(fileCoverage) {
    var statementMap = fileCoverage.statementMap,
        statements = fileCoverage.s,
        lineMap;

    if (!fileCoverage.l) {
        fileCoverage.l = lineMap = {};
        Object.keys(statements).forEach(function (st) {
            var line = statementMap[st].start.line,
                count = statements[st],
                prevVal = lineMap[line];
            if (count === 0 && statementMap[st].skip) { count = 1; }
            if (typeof prevVal === 'undefined' || prevVal < count) {
                lineMap[line] = count;
            }
        });
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.utils.blankSummary"></a>[function <span class="apidocSignatureSpan">isparta.utils.</span>blankSummary ()](#apidoc.element.isparta.utils.blankSummary)
- description and source-code
```javascript
function blankSummary() {
    return {
        lines: {
            total: 0,
            covered: 0,
            skipped: 0,
            pct: 'Unknown'
        },
        statements: {
            total: 0,
            covered: 0,
            skipped: 0,
            pct: 'Unknown'
        },
        functions: {
            total: 0,
            covered: 0,
            skipped: 0,
            pct: 'Unknown'
        },
        branches: {
            total: 0,
            covered: 0,
            skipped: 0,
            pct: 'Unknown'
        },
        linesCovered: {}
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.utils.incrementIgnoredTotals"></a>[function <span class="apidocSignatureSpan">isparta.utils.</span>incrementIgnoredTotals (cov)](#apidoc.element.isparta.utils.incrementIgnoredTotals)
- description and source-code
```javascript
function incrementIgnoredTotals(cov) {
    //TODO: This may be slow in the browser and may break in older browsers
    //      Look into using a library that works in Node and the browser
    var fileCoverage = JSON.parse(JSON.stringify(cov));

    [
        {mapKey: 'statementMap', hitsKey: 's'},
        {mapKey: 'branchMap', hitsKey: 'b'},
        {mapKey: 'fnMap', hitsKey: 'f'}
    ].forEach(function (keys) {
        Object.keys(fileCoverage[keys.mapKey])
            .forEach(function (key) {
                var map = fileCoverage[keys.mapKey][key];
                var hits = fileCoverage[keys.hitsKey];

                if (keys.mapKey === 'branchMap') {
                    var locations = map.locations;

                    locations.forEach(function (location, index) {
                        if (hits[key][index] === 0 && location.skip) {
                            hits[key][index] = 1;
                        }
                    });

                    return;
                }

                if (hits[key] === 0 && map.skip) {
                    hits[key] = 1;
                }
            });
        });

    return fileCoverage;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.utils.mergeFileCoverage"></a>[function <span class="apidocSignatureSpan">isparta.utils.</span>mergeFileCoverage (first, second)](#apidoc.element.isparta.utils.mergeFileCoverage)
- description and source-code
```javascript
function mergeFileCoverage(first, second) {
    var ret = JSON.parse(JSON.stringify(first)),
        i;

    delete ret.l; //remove derived info

    Object.keys(second.s).forEach(function (k) {
        ret.s[k] += second.s[k];
    });
    Object.keys(second.f).forEach(function (k) {
        ret.f[k] += second.f[k];
    });
    Object.keys(second.b).forEach(function (k) {
        var retArray = ret.b[k],
            secondArray = second.b[k];
        for (i = 0; i < retArray.length; i += 1) {
            retArray[i] += secondArray[i];
        }
    });

    return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.utils.mergeSummaryObjects"></a>[function <span class="apidocSignatureSpan">isparta.utils.</span>mergeSummaryObjects ()](#apidoc.element.isparta.utils.mergeSummaryObjects)
- description and source-code
```javascript
function mergeSummaryObjects() {
    var ret = blankSummary(),
        args = Array.prototype.slice.call(arguments),
        keys = ['lines', 'statements', 'branches', 'functions'],
        increment = function (obj) {
            if (obj) {
                keys.forEach(function (key) {
                    ret[key].total += obj[key].total;
                    ret[key].covered += obj[key].covered;
                    ret[key].skipped += obj[key].skipped;
                });

                // keep track of all lines we have coverage for.
                Object.keys(obj.linesCovered).forEach(function (key) {
                    if (!ret.linesCovered[key]) {
                        ret.linesCovered[key] = obj.linesCovered[key];
                    } else {
                        ret.linesCovered[key] += obj.linesCovered[key];
                    }
                });
            }
        };
    args.forEach(function (arg) {
        increment(arg);
    });
    keys.forEach(function (key) {
        ret[key].pct = percent(ret[key].covered, ret[key].total);
    });

    return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.utils.removeDerivedInfo"></a>[function <span class="apidocSignatureSpan">isparta.utils.</span>removeDerivedInfo (coverage)](#apidoc.element.isparta.utils.removeDerivedInfo)
- description and source-code
```javascript
function removeDerivedInfo(coverage) {
    Object.keys(coverage).forEach(function (k) {
        delete coverage[k].l;
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.utils.summarizeCoverage"></a>[function <span class="apidocSignatureSpan">isparta.utils.</span>summarizeCoverage (coverage)](#apidoc.element.isparta.utils.summarizeCoverage)
- description and source-code
```javascript
function summarizeCoverage(coverage) {
    var fileSummary = [];
    Object.keys(coverage).forEach(function (key) {
        fileSummary.push(summarizeFileCoverage(coverage[key]));
    });
    return mergeSummaryObjects.apply(null, fileSummary);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.utils.summarizeFileCoverage"></a>[function <span class="apidocSignatureSpan">isparta.utils.</span>summarizeFileCoverage (fileCoverage)](#apidoc.element.isparta.utils.summarizeFileCoverage)
- description and source-code
```javascript
function summarizeFileCoverage(fileCoverage) {
    var ret = blankSummary();
    addDerivedInfoForFile(fileCoverage);
    ret.lines = computeSimpleTotals(fileCoverage, 'l');
    ret.functions = computeSimpleTotals(fileCoverage, 'f', 'fnMap');
    ret.statements = computeSimpleTotals(fileCoverage, 's', 'statementMap');
    ret.branches = computeBranchTotals(fileCoverage);
    ret.linesCovered = fileCoverage.l;
    return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.isparta.utils.toYUICoverage"></a>[function <span class="apidocSignatureSpan">isparta.utils.</span>toYUICoverage (coverage)](#apidoc.element.isparta.utils.toYUICoverage)
- description and source-code
```javascript
function toYUICoverage(coverage) {
    var ret = {};

    addDerivedInfo(coverage);

    Object.keys(coverage).forEach(function (k) {
        var fileCoverage = coverage[k],
            lines = fileCoverage.l,
            functions = fileCoverage.f,
            fnMap = fileCoverage.fnMap,
            o;

        o = ret[k] = {
            lines: {},
            calledLines: 0,
            coveredLines: 0,
            functions: {},
            calledFunctions: 0,
            coveredFunctions: 0
        };
        Object.keys(lines).forEach(function (k) {
            o.lines[k] = lines[k];
            o.coveredLines += 1;
            if (lines[k] > 0) {
                o.calledLines += 1;
            }
        });
        Object.keys(functions).forEach(function (k) {
            var name = fnMap[k].name + ':' + fnMap[k].line;
            o.functions[name] = functions[k];
            o.coveredFunctions += 1;
            if (functions[k] > 0) {
                o.calledFunctions += 1;
            }
        });
    });
    return ret;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

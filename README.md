# npmtest-tldr

#### basic test coverage for  [tldr (v2.0.0)](http://tldr-pages.github.io)  [![npm package](https://img.shields.io/npm/v/npmtest-tldr.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-tldr) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-tldr.svg)](https://travis-ci.org/npmtest/node-npmtest-tldr)

#### Simplified and community-driven man pages

[![NPM](https://nodei.co/npm/tldr.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/tldr)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-tldr/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-tldr/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-tldr/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-tldr/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-tldr/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-tldr/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-tldr/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-tldr/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-tldr/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-tldr/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-tldr/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-tldr/build/test-report.html](https://npmtest.github.io/node-npmtest-tldr/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-tldr/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-tldr/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-tldr/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-tldr/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-tldr/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-tldr/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-tldr/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-tldr/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "tldr",
    "version": "2.0.0",
    "description": "Simplified and community-driven man pages",
    "author": "Romain Prieto",
    "license": "MIT",
    "repository": "tldr-pages/tldr-node-client",
    "keywords": [
        "man",
        "unix",
        "linux",
        "osx",
        "commands",
        "command-line",
        "shell",
        "bash",
        "zsh"
    ],
    "homepage": "http://tldr-pages.github.io",
    "engines": {
        "node": ">=4.7"
    },
    "main": "bin/tldr",
    "files": [
        "bin",
        "config.json",
        "lib",
        "LICENSE.md"
    ],
    "bin": {
        "tldr": "./bin/tldr"
    },
    "preferGlobal": true,
    "directories": {
        "test": "test"
    },
    "scripts": {
        "precommit": "npm run lint && npm run test:quiet",
        "prepush": "npm run test:quiet",
        "start": "node ./bin/tldr",
        "example": "node ./bin/tldr tar",
        "test": "mocha test --require=env-test",
        "test:quiet": "npm test --reporter=dot",
        "lint": "eslint lib test bin/tldr",
        "watch": "mocha test --require=env-test --reporter=min --watch --growl",
        "test:functional": "bash test/functional-test.sh",
        "test:all": "npm run lint && npm test && npm run test:functional"
    },
    "dependencies": {
        "chalk": "~1.1.1",
        "commander": "~2.9.0",
        "fs-extra": "^0.30.0",
        "lodash.defaults": "~4.2.0",
        "lodash.get": "~4.4.2",
        "lodash.identity": "~3.0.0",
        "lodash.isempty": "~4.4.0",
        "lodash.sample": "~4.2.1",
        "lodash.unescape": "~4.0.0",
        "marked": "~0.3.6",
        "ms": "~0.7.1",
        "os-homedir": "~1.0.1",
        "request": "~2.75.0",
        "unzip2": "~0.2.5"
    },
    "devDependencies": {
        "env-test": "*",
        "eslint": "*",
        "husky": "*",
        "mocha": "*",
        "should": "*",
        "sinon": "*"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

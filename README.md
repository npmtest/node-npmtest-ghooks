# npmtest-ghooks

#### basic test coverage for  [ghooks (v2.0.0)](https://github.com/gtramontina/ghooks)  [![npm package](https://img.shields.io/npm/v/npmtest-ghooks.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-ghooks) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-ghooks.svg)](https://travis-ci.org/npmtest/node-npmtest-ghooks)

#### Simple git hooks

[![NPM](https://nodei.co/npm/ghooks.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/ghooks)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-ghooks/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-ghooks/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-ghooks/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-ghooks/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-ghooks/build/test-report.html)|
| test-server-github : | [![github.com test-server](https://npmtest.github.io/node-npmtest-ghooks/GitHub-Mark-32px.png)](https://npmtest.github.io/node-npmtest-ghooks/build/app/index.html) | | build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-ghooks/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-ghooks/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-ghooks/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-ghooks/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-ghooks/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-ghooks/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-ghooks/build/test-report.html](https://npmtest.github.io/node-npmtest-ghooks/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-ghooks/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-ghooks/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-ghooks/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-ghooks/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-ghooks/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-ghooks/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-ghooks/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-ghooks/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Guilherme Tramontina"
    },
    "babel": {
        "presets": [
            "es2015"
        ]
    },
    "bugs": {
        "url": "https://github.com/gtramontina/ghooks/issues"
    },
    "config": {
        "ghooks": {
            "pre-commit": "opt --in pre-commit --exec \"npm run validate\"",
            "commit-msg": "opt --in commit-msg --exec validate-commit-msg"
        },
        "commitizen": {
            "path": "node_modules/cz-conventional-changelog"
        }
    },
    "dependencies": {
        "execa": "^0.4.0",
        "findup": "0.1.5",
        "lodash.clone": "4.3.2",
        "manage-path": "2.0.0",
        "opt-cli": "1.5.1",
        "path-exists": "^2.0.0",
        "spawn-command": "0.0.2"
    },
    "deprecated": "Use npmjs.com/husky instead, see https://github.com/gtramontina/ghooks/issues/166",
    "description": "Simple git hooks",
    "devDependencies": {
        "babel-cli": "^6.6.5",
        "babel-preset-es2015": "^6.3.13",
        "babel-register": "^6.4.3",
        "chai": "^3.0.0",
        "chai-string": "1.2.0",
        "codecov": "^1.0.1",
        "commitizen": "2.8.1",
        "cz-conventional-changelog": "1.2.0",
        "eslint": "^2.10.2",
        "eslint-config-kentcdodds": "^6.2.1",
        "eslint-plugin-import": "^1.8.0",
        "eslint-plugin-mocha": "^4.3.0",
        "ghooks": "*",
        "mocha": "^3.0.0",
        "mock-fs": "^3.0.0",
        "nyc": "^7.0.0",
        "proxyquire": "^1.3.1",
        "semantic-release": "^4.3.5",
        "sinon": "^1.12.2",
        "sinon-chai": "^2.7.0",
        "travis-after-all": "^1.4.4",
        "validate-commit-msg": "2.6.1"
    },
    "directories": {},
    "dist": {
        "shasum": "affd83a36e8b8fbdded9b851457c48ac74c8eab8",
        "tarball": "https://registry.npmjs.org/ghooks/-/ghooks-2.0.0.tgz"
    },
    "gitHead": "59b3aa3507baeaacfd8bfd228930f0ba55d3af8a",
    "homepage": "https://github.com/gtramontina/ghooks",
    "keywords": [
        "git",
        "hooks",
        "hook"
    ],
    "license": "MIT",
    "main": "./dist/runner.js",
    "maintainers": [
        {
            "name": "gtramontina"
        },
        {
            "name": "kentcdodds"
        }
    ],
    "name": "ghooks",
    "nyc": {
        "extension": [
            ".raw"
        ],
        "include": [
            "lib/**"
        ]
    },
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/gtramontina/ghooks.git"
    },
    "scripts": {
        "build": "babel lib --out-dir dist && babel lib/hook.template.raw --out-file dist/hook.template.raw",
        "check-coverage": "nyc check-coverage --statements 100 --branches 100 --functions 100 --lines 100",
        "commit": "git-cz",
        "coverage": "nyc --require babel-register --reporter=lcov --reporter=text mocha",
        "install": "node ./bin/module-install",
        "lint": "eslint bin/* lib/* test/",
        "prebuild": "rm -rf dist && mkdir dist",
        "report-coverage": "cat ./coverage/lcov.info | node_modules/.bin/codecov",
        "semantic-release": "semantic-release pre && npm publish && semantic-release post",
        "test": "npm run lint && npm run coverage",
        "test:unit": "mocha --compilers js:babel-register",
        "validate": "npm t && npm run check-coverage"
    },
    "version": "2.0.0",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

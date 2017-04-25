# npmdoc-jenkins

#### basic api documentation for  [jenkins (v0.20.0)](https://github.com/silas/node-jenkins#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-jenkins.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-jenkins) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-jenkins.svg)](https://travis-ci.org/npmdoc/node-npmdoc-jenkins)

#### Jenkins client

[![NPM](https://nodei.co/npm/jenkins.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/jenkins)

- [https://npmdoc.github.io/node-npmdoc-jenkins/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-jenkins/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-jenkins/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-jenkins/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-jenkins/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-jenkins/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Silas Sewell"
    },
    "bugs": {
        "url": "https://github.com/silas/node-jenkins/issues"
    },
    "dependencies": {
        "papi": "^0.26.0"
    },
    "description": "Jenkins client",
    "devDependencies": {
        "async": "^0.9.0",
        "bluebird": "^3.1.1",
        "fixturefiles": "^0.1.0",
        "istanbul": "^0.3.6",
        "jscs": "^1.5.8",
        "jshint": "^2.5.2",
        "lodash": "^3.3.1",
        "mocha": "^2.0.1",
        "nock": "^1.4.0",
        "node-uuid": "^1.4.1",
        "should": "^10.0.0",
        "sinon": "^1.17.2"
    },
    "directories": {},
    "dist": {
        "shasum": "9778d289508c04666ae5b8f557d9917c89c41ca2",
        "tarball": "https://registry.npmjs.org/jenkins/-/jenkins-0.20.0.tgz"
    },
    "gitHead": "7128502ae69e83320472e0a200be49e97bcdf2dd",
    "homepage": "https://github.com/silas/node-jenkins#readme",
    "keywords": [
        "jenkins"
    ],
    "license": "MIT",
    "main": "./lib",
    "maintainers": [
        {
            "name": "silas"
        }
    ],
    "name": "jenkins",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/silas/node-jenkins.git"
    },
    "scripts": {
        "cover": "istanbul cover ./node_modules/.bin/_mocha -- --recursive --check-leaks --timeout 15000 && open coverage/lcov-report/index.html",
        "test": "jshint lib test && ./node_modules/.bin/jscs lib test && ./node_modules/.bin/istanbul cover ./node_modules/.bin/_mocha -- --recursive --check-leaks --timeout 15000"
    },
    "version": "0.20.0",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

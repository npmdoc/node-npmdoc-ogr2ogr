# npmdoc-ogr2ogr

#### api documentation for  [ogr2ogr (v1.0.1)](http://github.com/wavded/ogr2ogr)  [![npm package](https://img.shields.io/npm/v/npmdoc-ogr2ogr.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-ogr2ogr) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-ogr2ogr.svg)](https://travis-ci.org/npmdoc/node-npmdoc-ogr2ogr)

#### ogr2ogr wrapper w/ multiple format support

[![NPM](https://nodei.co/npm/ogr2ogr.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/ogr2ogr)

- [https://npmdoc.github.io/node-npmdoc-ogr2ogr/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-ogr2ogr/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-ogr2ogr/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-ogr2ogr/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-ogr2ogr/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-ogr2ogr/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Marc Harter"
    },
    "bugs": {
        "url": "https://github.com/wavded/ogr2ogr/issues"
    },
    "dependencies": {
        "archiver": "^1.1.0",
        "comma-separated-values": "^3.6.0",
        "decompress-zip": "^0.3.0",
        "findit": "^2.0.0",
        "rimraf": "^2.2.8"
    },
    "description": "ogr2ogr wrapper w/ multiple format support",
    "devDependencies": {
        "istanbul": "^0.4.5",
        "tape": "^4.6.0"
    },
    "directories": {},
    "dist": {
        "shasum": "26f0151f2669150815b837fa3a4531e06d501c05",
        "tarball": "https://registry.npmjs.org/ogr2ogr/-/ogr2ogr-1.0.1.tgz"
    },
    "engines": {
        "node": "*"
    },
    "gitHead": "4d31d26e27143a3de0205161636370a1f5a59bf1",
    "homepage": "http://github.com/wavded/ogr2ogr",
    "keywords": [
        "ogr2ogr",
        "stream",
        "proj4",
        "gdal"
    ],
    "main": "./index.js",
    "maintainers": [
        {
            "name": "wavded"
        }
    ],
    "name": "ogr2ogr",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/wavded/ogr2ogr.git"
    },
    "scripts": {
        "docker-build": "docker build --rm -t wavded/ogre .",
        "docker-dev": "docker run -i -t -v 'pwd':/src -w /src wavded/ogre /bin/bash",
        "docker-test": "docker run -t -v 'pwd':/src -w /src wavded/ogre npm test",
        "test": "istanbul cover tape \"test/*-test.js\""
    },
    "version": "1.0.1"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

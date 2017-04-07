# api documentation for  [ogr2ogr (v1.0.1)](http://github.com/wavded/ogr2ogr)  [![npm package](https://img.shields.io/npm/v/npmdoc-ogr2ogr.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-ogr2ogr) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-ogr2ogr.svg)](https://travis-ci.org/npmdoc/node-npmdoc-ogr2ogr)
#### ogr2ogr wrapper w/ multiple format support

[![NPM](https://nodei.co/npm/ogr2ogr.png?downloads=true)](https://www.npmjs.com/package/ogr2ogr)

[![apidoc](https://npmdoc.github.io/node-npmdoc-ogr2ogr/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-ogr2ogr_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-ogr2ogr/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-ogr2ogr/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-ogr2ogr/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Marc Harter",
        "email": "wavded@gmail.com"
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
            "name": "wavded",
            "email": "wavded@gmail.com"
        }
    ],
    "name": "ogr2ogr",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module ogr2ogr](#apidoc.module.ogr2ogr)
1.  object <span class="apidocSignatureSpan">ogr2ogr.</span>csv
1.  object <span class="apidocSignatureSpan">ogr2ogr.</span>util
1.  object <span class="apidocSignatureSpan">ogr2ogr.</span>zip

#### [module ogr2ogr.csv](#apidoc.module.ogr2ogr.csv)
1.  [function <span class="apidocSignatureSpan">ogr2ogr.csv.</span>makeVrt (fpath, cb)](#apidoc.element.ogr2ogr.csv.makeVrt)

#### [module ogr2ogr.util](#apidoc.module.ogr2ogr.util)
1.  [function <span class="apidocSignatureSpan">ogr2ogr.util.</span>allCallback (cb)](#apidoc.element.ogr2ogr.util.allCallback)
1.  [function <span class="apidocSignatureSpan">ogr2ogr.util.</span>genTmpPath ()](#apidoc.element.ogr2ogr.util.genTmpPath)
1.  [function <span class="apidocSignatureSpan">ogr2ogr.util.</span>getDriver (fmt)](#apidoc.element.ogr2ogr.util.getDriver)
1.  [function <span class="apidocSignatureSpan">ogr2ogr.util.</span>oneCallback (cb)](#apidoc.element.ogr2ogr.util.oneCallback)
1.  [function <span class="apidocSignatureSpan">ogr2ogr.util.</span>rmDir (dpath, cb)](#apidoc.element.ogr2ogr.util.rmDir)
1.  [function <span class="apidocSignatureSpan">ogr2ogr.util.</span>rmFile (fpath, cb)](#apidoc.element.ogr2ogr.util.rmFile)
1.  [function <span class="apidocSignatureSpan">ogr2ogr.util.</span>rmParentDir (fpath, cb)](#apidoc.element.ogr2ogr.util.rmParentDir)
1.  [function <span class="apidocSignatureSpan">ogr2ogr.util.</span>tmpl (tmpl, data)](#apidoc.element.ogr2ogr.util.tmpl)
1.  [function <span class="apidocSignatureSpan">ogr2ogr.util.</span>writeGeoJSON (obj, cb)](#apidoc.element.ogr2ogr.util.writeGeoJSON)
1.  [function <span class="apidocSignatureSpan">ogr2ogr.util.</span>writeStream (ins, ext, cb)](#apidoc.element.ogr2ogr.util.writeStream)

#### [module ogr2ogr.zip](#apidoc.module.ogr2ogr.zip)
1.  [function <span class="apidocSignatureSpan">ogr2ogr.zip.</span>createZipStream (dpath)](#apidoc.element.ogr2ogr.zip.createZipStream)
1.  [function <span class="apidocSignatureSpan">ogr2ogr.zip.</span>extract (fpath, cb)](#apidoc.element.ogr2ogr.zip.extract)
1.  [function <span class="apidocSignatureSpan">ogr2ogr.zip.</span>findOgrFile (dpath, cb)](#apidoc.element.ogr2ogr.zip.findOgrFile)



# <a name="apidoc.module.ogr2ogr"></a>[module ogr2ogr](#apidoc.module.ogr2ogr)



# <a name="apidoc.module.ogr2ogr.csv"></a>[module ogr2ogr.csv](#apidoc.module.ogr2ogr.csv)

#### <a name="apidoc.element.ogr2ogr.csv.makeVrt"></a>[function <span class="apidocSignatureSpan">ogr2ogr.csv.</span>makeVrt (fpath, cb)](#apidoc.element.ogr2ogr.csv.makeVrt)
- description and source-code
```javascript
makeVrt = function (fpath, cb) {
  extractHead(fpath, function(er, headers) {
    if (er) return cb(er)

    var geo = {}
    headers.forEach(function(header) {
      var ht = (header + '').trim()
      switch (true) {
      case /\b(lon|longitude|lng|x)\b/i.test(ht):
        geo.x = header
        break
      case /\b(lat|latitude|y)\b/i.test(ht):
        geo.y = header
        break
      case /\b(the_geom|geom)\b/i.test(ht):
        geo.geom = header
        break
      default:
      }
    })

    if (!geo.geom && !geo.x) return cb(null, fpath) // no geometry fields, parse attributes

    var vrtData = util.tmpl(BASE_VRT, {
      file: fpath,
      name: path.basename(fpath, '.csv'),
      enc: geo.geom ? 'WKT' : 'PointFromColumns',
      encopt: geo.geom
                ? 'field="' + geo.geom + '"'
                : 'x="' + geo.x + '" y="' + geo.y + '"',
    })

    var vrtPath = util.genTmpPath() + '.vrt'
    return fs.writeFile(vrtPath, vrtData, function(er) {
      cb(er, vrtPath)
    })
  })
}
```
- example usage
```shell
...
if (ogr2ogr._isZipIn) {
  zip.extract(fpath, function(er2, fpath2) {
    if (er2) return one(er2)
    zip.findOgrFile(fpath2, one)
  })
}
else if (ogr2ogr._isCsvIn) {
  csv.makeVrt(fpath, function(err, vrt) {
    if (vrt && /\.vrt$/.test(vrt)) {
      // always set a source srs
      if (!ogr2ogr._sourceSrs) ogr2ogr._sourceSrs = ogr2ogr._targetSrs
    } else {
      // no geo data so no target srs
      delete ogr2ogr._targetSrs
    }
...
```



# <a name="apidoc.module.ogr2ogr.util"></a>[module ogr2ogr.util](#apidoc.module.ogr2ogr.util)

#### <a name="apidoc.element.ogr2ogr.util.allCallback"></a>[function <span class="apidocSignatureSpan">ogr2ogr.util.</span>allCallback (cb)](#apidoc.element.ogr2ogr.util.allCallback)
- description and source-code
```javascript
allCallback = function (cb) {
  var one = exports.oneCallback(cb)
  var expect = 0
  var total = 0

  setImmediate(function() { if (expect == 0) one(null, total) })

  return function() {
    expect++, total++
    return function(er) {
      if (er) return one(er)
      if (--expect == 0) one(null, total)
    }
  }
}
```
- example usage
```shell
...
  zs.pipe(ostream)
}

return ostream
}

Ogr2ogr.prototype._clean = function() {
var all = util.allCallback(this._testClean)

if (this._inStream && this._driver.output == 'zip') {
  util.rmDir(this._inPath, all())
}
else if (this._inStream || this._inGeoJSON) {
  util.rmFile(this._inPath, all())
}
...
```

#### <a name="apidoc.element.ogr2ogr.util.genTmpPath"></a>[function <span class="apidocSignatureSpan">ogr2ogr.util.</span>genTmpPath ()](#apidoc.element.ogr2ogr.util.genTmpPath)
- description and source-code
```javascript
genTmpPath = function () {
  return path.join(tmpdir, 'ogr_' + (genInc++).toString(14))
}
```
- example usage
```shell
...

ogr2ogr._inPath = fpath

ogr2ogr._isZipIn = /zip|kmz/.test(path.extname(fpath)) && !/^\/vsizip\//.test(fpath)
ogr2ogr._isCsvIn = /csv/.test(path.extname(fpath))
ogr2ogr._isZipOut = ogr2ogr._driver.output == 'zip'

ogr2ogr._ogrOutPath = ogr2ogr._isZipOut ? util.genTmpPath() : '/vsistdout/'

if (ogr2ogr._isZipIn) {
  zip.extract(fpath, function(er2, fpath2) {
    if (er2) return one(er2)
    zip.findOgrFile(fpath2, one)
  })
}
...
```

#### <a name="apidoc.element.ogr2ogr.util.getDriver"></a>[function <span class="apidocSignatureSpan">ogr2ogr.util.</span>getDriver (fmt)](#apidoc.element.ogr2ogr.util.getDriver)
- description and source-code
```javascript
getDriver = function (fmt) {
  for (var i = 0; i < drivers.length; i++) {
    if (drivers[i].format == fmt || drivers[i].aliases.indexOf(fmt) > -1) return drivers[i]
  }
  return {}
}
```
- example usage
```shell
...
if (!(this instanceof Ogr2ogr)) return new Ogr2ogr(mixed, fmt)

if (!mixed) {
  throw new Error('A file path, stream, or GeoJSON object is required')
}

if (mixed instanceof stream) {
  var driver = util.getDriver(fmt || path.extname(mixed.path).replace('.',''))
  if (!driver) throw new Error('Streams require a valid input format')
  this._inStream = mixed
  this._inDriver = driver
}
else if (typeof mixed == 'object') {
  this._inGeoJSON = mixed
}
...
```

#### <a name="apidoc.element.ogr2ogr.util.oneCallback"></a>[function <span class="apidocSignatureSpan">ogr2ogr.util.</span>oneCallback (cb)](#apidoc.element.ogr2ogr.util.oneCallback)
- description and source-code
```javascript
oneCallback = function (cb) {
  var called = false
  return function(er, data) {
    if (called) return
    called = true
    cb(er, data)
  }
}
```
- example usage
```shell
...
if (src) this._sourceSrs = src
return this
}

Ogr2ogr.prototype.exec = function(cb) {
var ogr2ogr = this
var buf = []
var one = util.oneCallback(cb)

this.stream()
  .on('data', function(chunk) { buf.push(chunk) })
  .on('error', one)
  .on('close', function() {
    var data = Buffer.concat(buf)
    if (ogr2ogr._format == 'GeoJSON') {
...
```

#### <a name="apidoc.element.ogr2ogr.util.rmDir"></a>[function <span class="apidocSignatureSpan">ogr2ogr.util.</span>rmDir (dpath, cb)](#apidoc.element.ogr2ogr.util.rmDir)
- description and source-code
```javascript
rmDir = function (dpath, cb) { rimraf(dpath, cb) }
```
- example usage
```shell
...
return ostream
}

Ogr2ogr.prototype._clean = function() {
var all = util.allCallback(this._testClean)

if (this._inStream && this._driver.output == 'zip') {
  util.rmDir(this._inPath, all())
}
else if (this._inStream || this._inGeoJSON) {
  util.rmFile(this._inPath, all())
}

if (this._isZipIn && this._ogrInPath) {
  util.rmParentDir(this._ogrInPath, all())
...
```

#### <a name="apidoc.element.ogr2ogr.util.rmFile"></a>[function <span class="apidocSignatureSpan">ogr2ogr.util.</span>rmFile (fpath, cb)](#apidoc.element.ogr2ogr.util.rmFile)
- description and source-code
```javascript
rmFile = function (fpath, cb) { fs.unlink(fpath, cb) }
```
- example usage
```shell
...
Ogr2ogr.prototype._clean = function() {
var all = util.allCallback(this._testClean)

if (this._inStream && this._driver.output == 'zip') {
  util.rmDir(this._inPath, all())
}
else if (this._inStream || this._inGeoJSON) {
  util.rmFile(this._inPath, all())
}

if (this._isZipIn && this._ogrInPath) {
  util.rmParentDir(this._ogrInPath, all())
}
if (this._isCsvIn && /vrt/.test(this._ogrInPath)) {
  util.rmFile(this._ogrInPath, all())
...
```

#### <a name="apidoc.element.ogr2ogr.util.rmParentDir"></a>[function <span class="apidocSignatureSpan">ogr2ogr.util.</span>rmParentDir (fpath, cb)](#apidoc.element.ogr2ogr.util.rmParentDir)
- description and source-code
```javascript
rmParentDir = function (fpath, cb) { rimraf(path.dirname(fpath), cb) }
```
- example usage
```shell
...
  util.rmDir(this._inPath, all())
}
else if (this._inStream || this._inGeoJSON) {
  util.rmFile(this._inPath, all())
}

if (this._isZipIn && this._ogrInPath) {
  util.rmParentDir(this._ogrInPath, all())
}
if (this._isCsvIn && /vrt/.test(this._ogrInPath)) {
  util.rmFile(this._ogrInPath, all())
}
if (this._isZipOut) {
  util.rmDir(this._ogrOutPath, all())
}
...
```

#### <a name="apidoc.element.ogr2ogr.util.tmpl"></a>[function <span class="apidocSignatureSpan">ogr2ogr.util.</span>tmpl (tmpl, data)](#apidoc.element.ogr2ogr.util.tmpl)
- description and source-code
```javascript
tmpl = function (tmpl, data) {
  for (var label in data) {
    tmpl = tmpl.replace('{{' + label + '}}', data[label])
  }
  return tmpl
}
```
- example usage
```shell
...
    break
  default:
  }
})

if (!geo.geom && !geo.x) return cb(null, fpath) // no geometry fields, parse attributes

var vrtData = util.tmpl(BASE_VRT, {
  file: fpath,
  name: path.basename(fpath, '.csv'),
  enc: geo.geom ? 'WKT' : 'PointFromColumns',
  encopt: geo.geom
            ? 'field="' + geo.geom + '"'
            : 'x="' + geo.x + '" y="' + geo.y + '"',
})
...
```

#### <a name="apidoc.element.ogr2ogr.util.writeGeoJSON"></a>[function <span class="apidocSignatureSpan">ogr2ogr.util.</span>writeGeoJSON (obj, cb)](#apidoc.element.ogr2ogr.util.writeGeoJSON)
- description and source-code
```javascript
writeGeoJSON = function (obj, cb) {
  var fpath = genTmpPath() + '.json'
  fs.writeFile(fpath, JSON.stringify(obj), function(er) {
    cb(er, fpath)
  })
}
```
- example usage
```shell
...
var ogr2ogr = this
var one = util.oneCallback(cb)

if (this._inStream) {
  util.writeStream(this._inStream, this._inDriver.output, getInFilePath)
}
else if (this._inGeoJSON) {
  util.writeGeoJSON(this._inGeoJSON, getInFilePath)
}
else {
  getInFilePath(null, this._inPath)
}

function getInFilePath(er, fpath) {
  if (er) return one(er)
...
```

#### <a name="apidoc.element.ogr2ogr.util.writeStream"></a>[function <span class="apidocSignatureSpan">ogr2ogr.util.</span>writeStream (ins, ext, cb)](#apidoc.element.ogr2ogr.util.writeStream)
- description and source-code
```javascript
writeStream = function (ins, ext, cb) {
  var fpath = genTmpPath() + '.' + ext
  var ws = fs.createWriteStream(fpath)
  var one = exports.oneCallback(cb)

  ins.pipe(ws)
    .on('error', one)
    .on('finish', function() {
      one(null, fpath)
    })
}
```
- example usage
```shell
...
}

Ogr2ogr.prototype._getOrgInPath = function(cb) {
var ogr2ogr = this
var one = util.oneCallback(cb)

if (this._inStream) {
  util.writeStream(this._inStream, this._inDriver.output, getInFilePath)
}
else if (this._inGeoJSON) {
  util.writeGeoJSON(this._inGeoJSON, getInFilePath)
}
else {
  getInFilePath(null, this._inPath)
}
...
```



# <a name="apidoc.module.ogr2ogr.zip"></a>[module ogr2ogr.zip](#apidoc.module.ogr2ogr.zip)

#### <a name="apidoc.element.ogr2ogr.zip.createZipStream"></a>[function <span class="apidocSignatureSpan">ogr2ogr.zip.</span>createZipStream (dpath)](#apidoc.element.ogr2ogr.zip.createZipStream)
- description and source-code
```javascript
createZipStream = function (dpath) {
  var zs = archiver('zip')

  fs.readdir(dpath, function(er, files) {
    if (er) return zs.emit('error', er)

    files.forEach(function(file) {
      var f = fs.createReadStream(path.join(dpath, file))
      zs.append(f, {name: file})
    })
    zs.finalize(function(er) {
      if (er) zs.emit('error', er)
    })
  })

  return zs
}
```
- example usage
```shell
...
    }
    if (!ogr2ogr._isZipOut) {
      ostream.emit('end')
      ostream.emit('close')
      return ogr2ogr._clean()
    }

    var zs = zip.createZipStream(ogr2ogr._ogrOutPath)
    zs.on('error', function(er2) { ostream.emit('error', er2) })
    zs.on('end', function() { ostream.emit('close'); ogr2ogr._clean() })
    zs.pipe(ostream)
  }

  return ostream
}
...
```

#### <a name="apidoc.element.ogr2ogr.zip.extract"></a>[function <span class="apidocSignatureSpan">ogr2ogr.zip.</span>extract (fpath, cb)](#apidoc.element.ogr2ogr.zip.extract)
- description and source-code
```javascript
extract = function (fpath, cb) {
  var zip = new DecompressZip(fpath)
  var zipPath = util.genTmpPath()
  var one = util.oneCallback(cb)

  zip
    .on('extract', function() {
      one(null, zipPath)
    })
    .on('error', one)
    .extract({path: zipPath})
}
```
- example usage
```shell
...
ogr2ogr._isZipIn = /zip|kmz/.test(path.extname(fpath)) && !/^\/vsizip\//.test(fpath)
ogr2ogr._isCsvIn = /csv/.test(path.extname(fpath))
ogr2ogr._isZipOut = ogr2ogr._driver.output == 'zip'

ogr2ogr._ogrOutPath = ogr2ogr._isZipOut ? util.genTmpPath() : '/vsistdout/'

if (ogr2ogr._isZipIn) {
  zip.extract(fpath, function(er2, fpath2) {
    if (er2) return one(er2)
    zip.findOgrFile(fpath2, one)
  })
}
else if (ogr2ogr._isCsvIn) {
  csv.makeVrt(fpath, function(err, vrt) {
    if (vrt && /\.vrt$/.test(vrt)) {
...
```

#### <a name="apidoc.element.ogr2ogr.zip.findOgrFile"></a>[function <span class="apidocSignatureSpan">ogr2ogr.zip.</span>findOgrFile (dpath, cb)](#apidoc.element.ogr2ogr.zip.findOgrFile)
- description and source-code
```javascript
findOgrFile = function (dpath, cb) {
  var finder = findit(dpath)
  var found

  finder.on('file', function(file, stat) {
    if (validOgrRe.test(path.extname(file))) found = file
  })
  finder.on('error', function(er) {
    cb(er)
    finder.stop() // prevent multiple callbacks, stop at first error
  })
  finder.on('end', function() {
    if (!found) return cb(new Error('No valid files found'))
    cb(null, found)
  })
}
```
- example usage
```shell
...
ogr2ogr._isZipOut = ogr2ogr._driver.output == 'zip'

ogr2ogr._ogrOutPath = ogr2ogr._isZipOut ? util.genTmpPath() : '/vsistdout/'

if (ogr2ogr._isZipIn) {
  zip.extract(fpath, function(er2, fpath2) {
    if (er2) return one(er2)
    zip.findOgrFile(fpath2, one)
  })
}
else if (ogr2ogr._isCsvIn) {
  csv.makeVrt(fpath, function(err, vrt) {
    if (vrt && /\.vrt$/.test(vrt)) {
      // always set a source srs
      if (!ogr2ogr._sourceSrs) ogr2ogr._sourceSrs = ogr2ogr._targetSrs
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

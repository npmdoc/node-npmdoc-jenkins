# api documentation for  [jenkins (v0.20.0)](https://github.com/silas/node-jenkins#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-jenkins.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-jenkins) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-jenkins.svg)](https://travis-ci.org/npmdoc/node-npmdoc-jenkins)
#### Jenkins client

[![NPM](https://nodei.co/npm/jenkins.png?downloads=true)](https://www.npmjs.com/package/jenkins)

[![apidoc](https://npmdoc.github.io/node-npmdoc-jenkins/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-jenkins_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-jenkins/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-jenkins/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-jenkins/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Silas Sewell",
        "email": "silas@sewell.org"
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
            "name": "silas",
            "email": "silas@sewell.org"
        }
    ],
    "name": "jenkins",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/silas/node-jenkins.git"
    },
    "scripts": {
        "cover": "istanbul cover ./node_modules/.bin/_mocha -- --recursive --check-leaks --timeout 15000 && open coverage/lcov-report/index.html",
        "test": "jshint lib test && ./node_modules/.bin/jscs lib test && ./node_modules/.bin/istanbul cover ./node_modules/.bin/_mocha -- --recursive --check-leaks --timeout 15000"
    },
    "version": "0.20.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module jenkins](#apidoc.module.jenkins)
1.  [function <span class="apidocSignatureSpan">jenkins.</span>Jenkins (opts)](#apidoc.element.jenkins.Jenkins)
1.  [function <span class="apidocSignatureSpan">jenkins.</span>Jenkins.Build (jenkins)](#apidoc.element.jenkins.Jenkins.Build)
1.  [function <span class="apidocSignatureSpan">jenkins.</span>Jenkins.CrumbIssuer (jenkins)](#apidoc.element.jenkins.Jenkins.CrumbIssuer)
1.  [function <span class="apidocSignatureSpan">jenkins.</span>Jenkins.Job (jenkins)](#apidoc.element.jenkins.Jenkins.Job)
1.  [function <span class="apidocSignatureSpan">jenkins.</span>Jenkins.Node (jenkins)](#apidoc.element.jenkins.Jenkins.Node)
1.  [function <span class="apidocSignatureSpan">jenkins.</span>Jenkins.Queue (jenkins)](#apidoc.element.jenkins.Jenkins.Queue)
1.  [function <span class="apidocSignatureSpan">jenkins.</span>Jenkins.View (jenkins)](#apidoc.element.jenkins.Jenkins.View)
1.  [function <span class="apidocSignatureSpan">jenkins.</span>Jenkins.super_ (opts)](#apidoc.element.jenkins.Jenkins.super_)
1.  object <span class="apidocSignatureSpan"></span>jenkins
1.  object <span class="apidocSignatureSpan">jenkins.</span>Jenkins.Build.prototype
1.  object <span class="apidocSignatureSpan">jenkins.</span>Jenkins.CrumbIssuer.prototype
1.  object <span class="apidocSignatureSpan">jenkins.</span>Jenkins.Job.prototype
1.  object <span class="apidocSignatureSpan">jenkins.</span>Jenkins.Node.prototype
1.  object <span class="apidocSignatureSpan">jenkins.</span>Jenkins.Queue.prototype
1.  object <span class="apidocSignatureSpan">jenkins.</span>Jenkins.View.prototype
1.  object <span class="apidocSignatureSpan">jenkins.</span>Jenkins.prototype
1.  object <span class="apidocSignatureSpan">jenkins.</span>Jenkins.super_.prototype
1.  object <span class="apidocSignatureSpan">jenkins.</span>crumb_issuer
1.  object <span class="apidocSignatureSpan">jenkins.</span>job
1.  object <span class="apidocSignatureSpan">jenkins.</span>middleware
1.  object <span class="apidocSignatureSpan">jenkins.</span>node
1.  object <span class="apidocSignatureSpan">jenkins.</span>queue
1.  object <span class="apidocSignatureSpan">jenkins.</span>utils
1.  object <span class="apidocSignatureSpan">jenkins.</span>view

#### [module jenkins.Jenkins](#apidoc.module.jenkins.Jenkins)
1.  [function <span class="apidocSignatureSpan">jenkins.</span>Jenkins (opts)](#apidoc.element.jenkins.Jenkins.Jenkins)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>Build (jenkins)](#apidoc.element.jenkins.Jenkins.Build)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>CrumbIssuer (jenkins)](#apidoc.element.jenkins.Jenkins.CrumbIssuer)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>Job (jenkins)](#apidoc.element.jenkins.Jenkins.Job)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>Node (jenkins)](#apidoc.element.jenkins.Jenkins.Node)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>Queue (jenkins)](#apidoc.element.jenkins.Jenkins.Queue)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>View (jenkins)](#apidoc.element.jenkins.Jenkins.View)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>super_ (opts)](#apidoc.element.jenkins.Jenkins.super_)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>walk ()](#apidoc.element.jenkins.Jenkins.walk)
1.  object <span class="apidocSignatureSpan">jenkins.Jenkins.</span>meta

#### [module jenkins.Jenkins.Build](#apidoc.module.jenkins.Jenkins.Build)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>Build (jenkins)](#apidoc.element.jenkins.Jenkins.Build.Build)
1.  object <span class="apidocSignatureSpan">jenkins.Jenkins.Build.</span>meta

#### [module jenkins.Jenkins.Build.prototype](#apidoc.module.jenkins.Jenkins.Build.prototype)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Build.prototype.</span>get (opts, callback)](#apidoc.element.jenkins.Jenkins.Build.prototype.get)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Build.prototype.</span>log (opts, callback)](#apidoc.element.jenkins.Jenkins.Build.prototype.log)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Build.prototype.</span>logStream (opts)](#apidoc.element.jenkins.Jenkins.Build.prototype.logStream)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Build.prototype.</span>stop (opts, callback)](#apidoc.element.jenkins.Jenkins.Build.prototype.stop)

#### [module jenkins.Jenkins.CrumbIssuer](#apidoc.module.jenkins.Jenkins.CrumbIssuer)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>CrumbIssuer (jenkins)](#apidoc.element.jenkins.Jenkins.CrumbIssuer.CrumbIssuer)
1.  object <span class="apidocSignatureSpan">jenkins.Jenkins.CrumbIssuer.</span>meta

#### [module jenkins.Jenkins.CrumbIssuer.prototype](#apidoc.module.jenkins.Jenkins.CrumbIssuer.prototype)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.CrumbIssuer.prototype.</span>get (opts, callback)](#apidoc.element.jenkins.Jenkins.CrumbIssuer.prototype.get)

#### [module jenkins.Jenkins.Job](#apidoc.module.jenkins.Jenkins.Job)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>Job (jenkins)](#apidoc.element.jenkins.Jenkins.Job.Job)
1.  object <span class="apidocSignatureSpan">jenkins.Jenkins.Job.</span>meta

#### [module jenkins.Jenkins.Job.prototype](#apidoc.module.jenkins.Jenkins.Job.prototype)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>build (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.build)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>config (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.config)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>copy (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.copy)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>create (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.create)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>delete (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.delete)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>destroy (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>disable (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.disable)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>enable (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.enable)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>exists (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.exists)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>get (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.get)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>list (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.list)

#### [module jenkins.Jenkins.Node](#apidoc.module.jenkins.Jenkins.Node)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>Node (jenkins)](#apidoc.element.jenkins.Jenkins.Node.Node)
1.  object <span class="apidocSignatureSpan">jenkins.Jenkins.Node.</span>meta

#### [module jenkins.Jenkins.Node.prototype](#apidoc.module.jenkins.Jenkins.Node.prototype)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>changeOfflineCause (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.changeOfflineCause)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>config (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.config)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>create (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.create)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>delete (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.delete)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>destroy (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>disable (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.disable)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>disconnect (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.disconnect)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>doDisconnect (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.doDisconnect)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>enable (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.enable)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>exists (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.exists)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>get (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.get)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>list (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.list)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>toggleOffline (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.toggleOffline)

#### [module jenkins.Jenkins.Queue](#apidoc.module.jenkins.Jenkins.Queue)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>Queue (jenkins)](#apidoc.element.jenkins.Jenkins.Queue.Queue)

#### [module jenkins.Jenkins.Queue.prototype](#apidoc.module.jenkins.Jenkins.Queue.prototype)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Queue.prototype.</span>cancel (opts, callback)](#apidoc.element.jenkins.Jenkins.Queue.prototype.cancel)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Queue.prototype.</span>get (opts, callback)](#apidoc.element.jenkins.Jenkins.Queue.prototype.get)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Queue.prototype.</span>item (opts, callback)](#apidoc.element.jenkins.Jenkins.Queue.prototype.item)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.Queue.prototype.</span>list (opts, callback)](#apidoc.element.jenkins.Jenkins.Queue.prototype.list)

#### [module jenkins.Jenkins.View](#apidoc.module.jenkins.Jenkins.View)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>View (jenkins)](#apidoc.element.jenkins.Jenkins.View.View)
1.  object <span class="apidocSignatureSpan">jenkins.Jenkins.View.</span>meta

#### [module jenkins.Jenkins.View.prototype](#apidoc.module.jenkins.Jenkins.View.prototype)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.View.prototype.</span>add (opts, callback)](#apidoc.element.jenkins.Jenkins.View.prototype.add)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.View.prototype.</span>config (opts, callback)](#apidoc.element.jenkins.Jenkins.View.prototype.config)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.View.prototype.</span>create (opts, callback)](#apidoc.element.jenkins.Jenkins.View.prototype.create)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.View.prototype.</span>delete (opts, callback)](#apidoc.element.jenkins.Jenkins.View.prototype.delete)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.View.prototype.</span>destroy (opts, callback)](#apidoc.element.jenkins.Jenkins.View.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.View.prototype.</span>exists (opts, callback)](#apidoc.element.jenkins.Jenkins.View.prototype.exists)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.View.prototype.</span>get (opts, callback)](#apidoc.element.jenkins.Jenkins.View.prototype.get)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.View.prototype.</span>list (opts, callback)](#apidoc.element.jenkins.Jenkins.View.prototype.list)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.View.prototype.</span>remove (opts, callback)](#apidoc.element.jenkins.Jenkins.View.prototype.remove)

#### [module jenkins.Jenkins.prototype](#apidoc.module.jenkins.Jenkins.prototype)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.prototype.</span>_onCreate (ctx, next)](#apidoc.element.jenkins.Jenkins.prototype._onCreate)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.prototype.</span>_onResponse (ctx, next)](#apidoc.element.jenkins.Jenkins.prototype._onResponse)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.prototype.</span>get (opts, callback)](#apidoc.element.jenkins.Jenkins.prototype.get)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.prototype.</span>info (opts, callback)](#apidoc.element.jenkins.Jenkins.prototype.info)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.prototype.</span>walk ()](#apidoc.element.jenkins.Jenkins.prototype.walk)

#### [module jenkins.Jenkins.super_](#apidoc.module.jenkins.Jenkins.super_)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>super_ ()](#apidoc.element.jenkins.Jenkins.super_.super_)

#### [module jenkins.Jenkins.super_.prototype](#apidoc.module.jenkins.Jenkins.super_.prototype)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>__create (request, next)](#apidoc.element.jenkins.Jenkins.super_.prototype.__create)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>__execute (request, next)](#apidoc.element.jenkins.Jenkins.super_.prototype.__execute)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>__push (request, name)](#apidoc.element.jenkins.Jenkins.super_.prototype.__push)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_decode (mime, value)](#apidoc.element.jenkins.Jenkins.super_.prototype._decode)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_delete (opts)](#apidoc.element.jenkins.Jenkins.super_.prototype._delete)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_encode (mime, value)](#apidoc.element.jenkins.Jenkins.super_.prototype._encode)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_err (err, opts)](#apidoc.element.jenkins.Jenkins.super_.prototype._err)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_ext (eventName, callback)](#apidoc.element.jenkins.Jenkins.super_.prototype._ext)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_get (opts)](#apidoc.element.jenkins.Jenkins.super_.prototype._get)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_head (opts)](#apidoc.element.jenkins.Jenkins.super_.prototype._head)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_log (tags, data)](#apidoc.element.jenkins.Jenkins.super_.prototype._log)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_options (opts)](#apidoc.element.jenkins.Jenkins.super_.prototype._options)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_patch (opts)](#apidoc.element.jenkins.Jenkins.super_.prototype._patch)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_plugin (plugin, options)](#apidoc.element.jenkins.Jenkins.super_.prototype._plugin)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_post (opts)](#apidoc.element.jenkins.Jenkins.super_.prototype._post)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_put (opts)](#apidoc.element.jenkins.Jenkins.super_.prototype._put)
1.  [function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_request (opts)](#apidoc.element.jenkins.Jenkins.super_.prototype._request)

#### [module jenkins.crumb_issuer](#apidoc.module.jenkins.crumb_issuer)
1.  [function <span class="apidocSignatureSpan">jenkins.crumb_issuer.</span>CrumbIssuer (jenkins)](#apidoc.element.jenkins.crumb_issuer.CrumbIssuer)

#### [module jenkins.jenkins](#apidoc.module.jenkins.jenkins)
1.  [function <span class="apidocSignatureSpan">jenkins.jenkins.</span>Jenkins (opts)](#apidoc.element.jenkins.jenkins.Jenkins)

#### [module jenkins.job](#apidoc.module.jenkins.job)
1.  [function <span class="apidocSignatureSpan">jenkins.job.</span>Job (jenkins)](#apidoc.element.jenkins.job.Job)

#### [module jenkins.middleware](#apidoc.module.jenkins.middleware)
1.  [function <span class="apidocSignatureSpan">jenkins.middleware.</span>body (ctx, next)](#apidoc.element.jenkins.middleware.body)
1.  [function <span class="apidocSignatureSpan">jenkins.middleware.</span>bodyItem (key)](#apidoc.element.jenkins.middleware.bodyItem)
1.  [function <span class="apidocSignatureSpan">jenkins.middleware.</span>empty (ctx, next)](#apidoc.element.jenkins.middleware.empty)
1.  [function <span class="apidocSignatureSpan">jenkins.middleware.</span>exists (ctx, next)](#apidoc.element.jenkins.middleware.exists)
1.  [function <span class="apidocSignatureSpan">jenkins.middleware.</span>notFound (value)](#apidoc.element.jenkins.middleware.notFound)
1.  [function <span class="apidocSignatureSpan">jenkins.middleware.</span>queueLocation (ctx, next)](#apidoc.element.jenkins.middleware.queueLocation)
1.  [function <span class="apidocSignatureSpan">jenkins.middleware.</span>require302 (message)](#apidoc.element.jenkins.middleware.require302)

#### [module jenkins.node](#apidoc.module.jenkins.node)
1.  [function <span class="apidocSignatureSpan">jenkins.node.</span>Node (jenkins)](#apidoc.element.jenkins.node.Node)

#### [module jenkins.queue](#apidoc.module.jenkins.queue)
1.  [function <span class="apidocSignatureSpan">jenkins.queue.</span>Queue (jenkins)](#apidoc.element.jenkins.queue.Queue)

#### [module jenkins.utils](#apidoc.module.jenkins.utils)
1.  [function <span class="apidocSignatureSpan">jenkins.utils.</span>FolderPath (value)](#apidoc.element.jenkins.utils.FolderPath)
1.  [function <span class="apidocSignatureSpan">jenkins.utils.</span>crumbIssuer (jenkins, callback)](#apidoc.element.jenkins.utils.crumbIssuer)
1.  [function <span class="apidocSignatureSpan">jenkins.utils.</span>options (req, opts)](#apidoc.element.jenkins.utils.options)

#### [module jenkins.view](#apidoc.module.jenkins.view)
1.  [function <span class="apidocSignatureSpan">jenkins.view.</span>View (jenkins)](#apidoc.element.jenkins.view.View)



# <a name="apidoc.module.jenkins"></a>[module jenkins](#apidoc.module.jenkins)

#### <a name="apidoc.element.jenkins.Jenkins"></a>[function <span class="apidocSignatureSpan">jenkins.</span>Jenkins (opts)](#apidoc.element.jenkins.Jenkins)
- description and source-code
```javascript
function Jenkins(opts) {
  if (!(this instanceof Jenkins)) {
    return new Jenkins(opts);
  }

  if (typeof opts === 'string') {
    opts = { baseUrl: opts };
  } else {
    opts = opts || {};
  }

  if (!opts.baseUrl) {
    if (opts.url) {
      opts.baseUrl = opts.url;
      delete opts.url;
    } else {
      throw new Error('baseUrl required');
    }
  }

  if (!opts.headers) {
    opts.headers = {};
  }
  if (!opts.headers.referer) {
    opts.headers.referer = opts.baseUrl + '/';
  }

  if (opts.request) {
    throw new Error('request not longer supported');
  }

  opts.name = 'jenkins';

  if (typeof opts.crumbIssuer === 'function') {
    this._crumbIssuer = opts.crumbIssuer;
  } else if (opts.crumbIssuer === true) {
    this._crumbIssuer = utils.crumbIssuer;
  }

  papi.Client.call(this, opts);

  this._ext('onCreate', this._onCreate);
  this._ext('onResponse', this._onResponse);

  this.build = new Jenkins.Build(this);
  this.crumbIssuer = new Jenkins.CrumbIssuer(this);
  this.job = new Jenkins.Job(this);
  this.node = new Jenkins.Node(this);
  this.queue = new Jenkins.Queue(this);
  this.view = new Jenkins.View(this);

  try {
    if (opts.promisify) {
      if (typeof opts.promisify === 'function') {
        papi.tools.promisify(this, opts.promisify);
      } else {
        papi.tools.promisify(this);
      }
    }
  } catch (err) {
    err.message = 'promisify: ' + err.message;
    throw err;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.Build"></a>[function <span class="apidocSignatureSpan">jenkins.</span>Jenkins.Build (jenkins)](#apidoc.element.jenkins.Jenkins.Build)
- description and source-code
```javascript
function Build(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.CrumbIssuer"></a>[function <span class="apidocSignatureSpan">jenkins.</span>Jenkins.CrumbIssuer (jenkins)](#apidoc.element.jenkins.Jenkins.CrumbIssuer)
- description and source-code
```javascript
function CrumbIssuer(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.Job"></a>[function <span class="apidocSignatureSpan">jenkins.</span>Jenkins.Job (jenkins)](#apidoc.element.jenkins.Jenkins.Job)
- description and source-code
```javascript
function Job(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.Node"></a>[function <span class="apidocSignatureSpan">jenkins.</span>Jenkins.Node (jenkins)](#apidoc.element.jenkins.Jenkins.Node)
- description and source-code
```javascript
function Node(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.Queue"></a>[function <span class="apidocSignatureSpan">jenkins.</span>Jenkins.Queue (jenkins)](#apidoc.element.jenkins.Jenkins.Queue)
- description and source-code
```javascript
function Queue(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.View"></a>[function <span class="apidocSignatureSpan">jenkins.</span>Jenkins.View (jenkins)](#apidoc.element.jenkins.Jenkins.View)
- description and source-code
```javascript
function View(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.super_"></a>[function <span class="apidocSignatureSpan">jenkins.</span>Jenkins.super_ (opts)](#apidoc.element.jenkins.Jenkins.super_)
- description and source-code
```javascript
function Client(opts) {
  if (!(this instanceof Client)) {
    return new Client(opts);
  }

  events.EventEmitter.call(this);

  opts = opts || {};

  if (typeof opts === 'string') {
    opts = { baseUrl: opts };
  }

  if (!opts.baseUrl) {
    throw errors.Validation('baseUrl required');
  }

  if (!(opts.baseUrl instanceof url.Url)) {
    if (typeof opts.baseUrl !== 'string') {
      throw errors.Validation('baseUrl must be a string: ' + opts.baseUrl);
    }

    opts.baseUrl = url.parse(opts.baseUrl);
  }

  opts.baseUrl.path = opts.baseUrl.pathname;
  opts.baseUrl = utils.pick(opts.baseUrl,
    'auth', 'hostname', 'path', 'port', 'protocol');

  if (opts.baseUrl.path === '/') {
    opts.baseUrl.path = '';
  } else if (opts.baseUrl.path[opts.baseUrl.path.length - 1] === '/') {
    throw errors.Validation('baseUrl must not end with a forward slash');
  }

  opts.headers = utils.mergeHeaders(opts.headers);
  opts.tags = opts.tags || [];

  if (opts.name && !~opts.tags.indexOf(opts.name)) {
    opts.tags = opts.tags.concat(opts.name);
  }

  opts.encoders = utils.merge(constants.ENCODERS, opts.encoders);
  opts.decoders = utils.merge(constants.DECODERS, opts.decoders);

  this._opts = opts;
  this._exts = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jenkins.Jenkins"></a>[module jenkins.Jenkins](#apidoc.module.jenkins.Jenkins)

#### <a name="apidoc.element.jenkins.Jenkins.Jenkins"></a>[function <span class="apidocSignatureSpan">jenkins.</span>Jenkins (opts)](#apidoc.element.jenkins.Jenkins.Jenkins)
- description and source-code
```javascript
function Jenkins(opts) {
  if (!(this instanceof Jenkins)) {
    return new Jenkins(opts);
  }

  if (typeof opts === 'string') {
    opts = { baseUrl: opts };
  } else {
    opts = opts || {};
  }

  if (!opts.baseUrl) {
    if (opts.url) {
      opts.baseUrl = opts.url;
      delete opts.url;
    } else {
      throw new Error('baseUrl required');
    }
  }

  if (!opts.headers) {
    opts.headers = {};
  }
  if (!opts.headers.referer) {
    opts.headers.referer = opts.baseUrl + '/';
  }

  if (opts.request) {
    throw new Error('request not longer supported');
  }

  opts.name = 'jenkins';

  if (typeof opts.crumbIssuer === 'function') {
    this._crumbIssuer = opts.crumbIssuer;
  } else if (opts.crumbIssuer === true) {
    this._crumbIssuer = utils.crumbIssuer;
  }

  papi.Client.call(this, opts);

  this._ext('onCreate', this._onCreate);
  this._ext('onResponse', this._onResponse);

  this.build = new Jenkins.Build(this);
  this.crumbIssuer = new Jenkins.CrumbIssuer(this);
  this.job = new Jenkins.Job(this);
  this.node = new Jenkins.Node(this);
  this.queue = new Jenkins.Queue(this);
  this.view = new Jenkins.View(this);

  try {
    if (opts.promisify) {
      if (typeof opts.promisify === 'function') {
        papi.tools.promisify(this, opts.promisify);
      } else {
        papi.tools.promisify(this);
      }
    }
  } catch (err) {
    err.message = 'promisify: ' + err.message;
    throw err;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.Build"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>Build (jenkins)](#apidoc.element.jenkins.Jenkins.Build)
- description and source-code
```javascript
function Build(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
...
}

papi.Client.call(this, opts);

this._ext('onCreate', this._onCreate);
this._ext('onResponse', this._onResponse);

this.build = new Jenkins.Build(this);
this.crumbIssuer = new Jenkins.CrumbIssuer(this);
this.job = new Jenkins.Job(this);
this.node = new Jenkins.Node(this);
this.queue = new Jenkins.Queue(this);
this.view = new Jenkins.View(this);

try {
...
```

#### <a name="apidoc.element.jenkins.Jenkins.CrumbIssuer"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>CrumbIssuer (jenkins)](#apidoc.element.jenkins.Jenkins.CrumbIssuer)
- description and source-code
```javascript
function CrumbIssuer(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
...

papi.Client.call(this, opts);

this._ext('onCreate', this._onCreate);
this._ext('onResponse', this._onResponse);

this.build = new Jenkins.Build(this);
this.crumbIssuer = new Jenkins.CrumbIssuer(this);
this.job = new Jenkins.Job(this);
this.node = new Jenkins.Node(this);
this.queue = new Jenkins.Queue(this);
this.view = new Jenkins.View(this);

try {
  if (opts.promisify) {
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Job"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>Job (jenkins)](#apidoc.element.jenkins.Jenkins.Job)
- description and source-code
```javascript
function Job(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
...
papi.Client.call(this, opts);

this._ext('onCreate', this._onCreate);
this._ext('onResponse', this._onResponse);

this.build = new Jenkins.Build(this);
this.crumbIssuer = new Jenkins.CrumbIssuer(this);
this.job = new Jenkins.Job(this);
this.node = new Jenkins.Node(this);
this.queue = new Jenkins.Queue(this);
this.view = new Jenkins.View(this);

try {
  if (opts.promisify) {
    if (typeof opts.promisify === 'function') {
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Node"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>Node (jenkins)](#apidoc.element.jenkins.Jenkins.Node)
- description and source-code
```javascript
function Node(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
...

this._ext('onCreate', this._onCreate);
this._ext('onResponse', this._onResponse);

this.build = new Jenkins.Build(this);
this.crumbIssuer = new Jenkins.CrumbIssuer(this);
this.job = new Jenkins.Job(this);
this.node = new Jenkins.Node(this);
this.queue = new Jenkins.Queue(this);
this.view = new Jenkins.View(this);

try {
  if (opts.promisify) {
    if (typeof opts.promisify === 'function') {
      papi.tools.promisify(this, opts.promisify);
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Queue"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>Queue (jenkins)](#apidoc.element.jenkins.Jenkins.Queue)
- description and source-code
```javascript
function Queue(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
...
this._ext('onCreate', this._onCreate);
this._ext('onResponse', this._onResponse);

this.build = new Jenkins.Build(this);
this.crumbIssuer = new Jenkins.CrumbIssuer(this);
this.job = new Jenkins.Job(this);
this.node = new Jenkins.Node(this);
this.queue = new Jenkins.Queue(this);
this.view = new Jenkins.View(this);

try {
  if (opts.promisify) {
    if (typeof opts.promisify === 'function') {
      papi.tools.promisify(this, opts.promisify);
    } else {
...
```

#### <a name="apidoc.element.jenkins.Jenkins.View"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>View (jenkins)](#apidoc.element.jenkins.Jenkins.View)
- description and source-code
```javascript
function View(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
...
this._ext('onResponse', this._onResponse);

this.build = new Jenkins.Build(this);
this.crumbIssuer = new Jenkins.CrumbIssuer(this);
this.job = new Jenkins.Job(this);
this.node = new Jenkins.Node(this);
this.queue = new Jenkins.Queue(this);
this.view = new Jenkins.View(this);

try {
  if (opts.promisify) {
    if (typeof opts.promisify === 'function') {
      papi.tools.promisify(this, opts.promisify);
    } else {
      papi.tools.promisify(this);
...
```

#### <a name="apidoc.element.jenkins.Jenkins.super_"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>super_ (opts)](#apidoc.element.jenkins.Jenkins.super_)
- description and source-code
```javascript
function Client(opts) {
  if (!(this instanceof Client)) {
    return new Client(opts);
  }

  events.EventEmitter.call(this);

  opts = opts || {};

  if (typeof opts === 'string') {
    opts = { baseUrl: opts };
  }

  if (!opts.baseUrl) {
    throw errors.Validation('baseUrl required');
  }

  if (!(opts.baseUrl instanceof url.Url)) {
    if (typeof opts.baseUrl !== 'string') {
      throw errors.Validation('baseUrl must be a string: ' + opts.baseUrl);
    }

    opts.baseUrl = url.parse(opts.baseUrl);
  }

  opts.baseUrl.path = opts.baseUrl.pathname;
  opts.baseUrl = utils.pick(opts.baseUrl,
    'auth', 'hostname', 'path', 'port', 'protocol');

  if (opts.baseUrl.path === '/') {
    opts.baseUrl.path = '';
  } else if (opts.baseUrl.path[opts.baseUrl.path.length - 1] === '/') {
    throw errors.Validation('baseUrl must not end with a forward slash');
  }

  opts.headers = utils.mergeHeaders(opts.headers);
  opts.tags = opts.tags || [];

  if (opts.name && !~opts.tags.indexOf(opts.name)) {
    opts.tags = opts.tags.concat(opts.name);
  }

  opts.encoders = utils.merge(constants.ENCODERS, opts.encoders);
  opts.decoders = utils.merge(constants.DECODERS, opts.decoders);

  this._opts = opts;
  this._exts = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.walk"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>walk ()](#apidoc.element.jenkins.Jenkins.walk)
- description and source-code
```javascript
walk = function () {
  return papi.tools.walk(Jenkins);
}
```
- example usage
```shell
...
/**
 * Walk methods
 */

Jenkins.meta.walk = { type: 'sync' };

Jenkins.walk = Jenkins.prototype.walk = function() {
  return papi.tools.walk(Jenkins);
};

/**
 * Module exports.
 */

exports.Jenkins = Jenkins;
...
```



# <a name="apidoc.module.jenkins.Jenkins.Build"></a>[module jenkins.Jenkins.Build](#apidoc.module.jenkins.Jenkins.Build)

#### <a name="apidoc.element.jenkins.Jenkins.Build.Build"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>Build (jenkins)](#apidoc.element.jenkins.Jenkins.Build.Build)
- description and source-code
```javascript
function Build(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
...
}

papi.Client.call(this, opts);

this._ext('onCreate', this._onCreate);
this._ext('onResponse', this._onResponse);

this.build = new Jenkins.Build(this);
this.crumbIssuer = new Jenkins.CrumbIssuer(this);
this.job = new Jenkins.Job(this);
this.node = new Jenkins.Node(this);
this.queue = new Jenkins.Queue(this);
this.view = new Jenkins.View(this);

try {
...
```



# <a name="apidoc.module.jenkins.Jenkins.Build.prototype"></a>[module jenkins.Jenkins.Build.prototype](#apidoc.module.jenkins.Jenkins.Build.prototype)

#### <a name="apidoc.element.jenkins.Jenkins.Build.prototype.get"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Build.prototype.</span>get (opts, callback)](#apidoc.element.jenkins.Jenkins.Build.prototype.get)
- description and source-code
```javascript
get = function (opts, callback) {
  var arg0 = typeof arguments[0];
  var arg1 = typeof arguments[1];
  var arg2 = typeof arguments[2];
  var arg3 = typeof arguments[3];

  if (arg0 === 'string' && (arg1 === 'string' || arg1 === 'number')) {
    if (arg2 === 'object') {
      opts = arguments[2];
      callback = arg3 === 'function' ? arguments[3] : undefined;
    } else {
      opts = {};
      callback = arg2 === 'function' ? arguments[2] : undefined;
    }

    opts.name = arguments[0];
    opts.number = arguments[1];
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'build', 'get'], opts);

  var req = { name: 'build.get' };

  utils.options(req, opts);

  try {
    var folder = utils.FolderPath(opts.name);

    if (folder.isEmpty()) throw new Error('name required');
    if (!opts.number) throw new Error('number required');

    req.path = '{folder}/{number}/api/json';
    req.params = {
      folder: folder.path(),
      number: opts.number,
    };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._get(
    req,
    middleware.notFound(opts.name + ' ' + opts.number),
    middleware.body,
    callback
  );
}
```
- example usage
```shell
...
     "url": "http://localhost:8080/"
   }
 ]
}
'''

<a name="build-get"></a>
### jenkins.build.get(options, callback)

Get build information.

Options

* name (String): job name
* number (Integer): build number
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Build.prototype.log"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Build.prototype.</span>log (opts, callback)](#apidoc.element.jenkins.Jenkins.Build.prototype.log)
- description and source-code
```javascript
log = function (opts, callback) {
  var arg0 = typeof arguments[0];
  var arg1 = typeof arguments[1];
  var arg2 = typeof arguments[2];
  var arg3 = typeof arguments[3];

  if (arg0 === 'string' && (arg1 === 'string' || arg1 === 'number')) {
    if (arg2 === 'object') {
      opts = arguments[2];
      callback = arg3 === 'function' ? arguments[3] : undefined;
    } else {
      opts = {};
      callback = arg2 === 'function' ? arguments[2] : undefined;
    }

    opts.name = arguments[0];
    opts.number = arguments[1];
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'build', 'log'], opts);

  var req = { name: 'build.log' };

  utils.options(req, opts);

  try {
    var folder = utils.FolderPath(opts.name);

    if (folder.isEmpty()) throw new Error('name required');
    if (!opts.number) throw new Error('number required');

    req.path = '{folder}/{number}/logText/progressive{type}';
    req.params = {
      folder: folder.path(),
      number: opts.number,
      type: opts.type === 'html' ? 'Html' : 'Text',
    };
    req.type = 'form';
    req.body = {};
    if (opts.hasOwnProperty('start')) req.body.start = opts.start;
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(
    req,
    middleware.notFound(opts.name + ' ' + opts.number),
    function(ctx, next) {
      if (ctx.err) return next(ctx.err);
      if (!opts.meta) return next(false, null, ctx.res.body);

      var data = {
        text: ctx.res.body,
        more: ctx.res.headers['x-more-data'] === 'true',
      };

      if (ctx.res.headers['x-text-size']) {
        data.size = ctx.res.headers['x-text-size'];
      }

      next(false, null, data);
    },
    callback
  );
}
```
- example usage
```shell
...

Usage

''' javascript
jenkins.info(function(err, data) {
  if (err) throw err;

  console.log('info', data);
});
'''

Result

''' json
{
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Build.prototype.logStream"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Build.prototype.</span>logStream (opts)](#apidoc.element.jenkins.Jenkins.Build.prototype.logStream)
- description and source-code
```javascript
logStream = function (opts) {
  var arg0 = typeof arguments[0];
  var arg1 = typeof arguments[1];
  var arg2 = typeof arguments[2];

  if (arg0 === 'string' && (arg1 === 'string' || arg1 === 'number')) {
    if (arg2 === 'object') {
      opts = arguments[2];
    } else {
      opts = {};
    }

    opts.name = arguments[0];
    opts.number = arguments[1];
  } else {
    opts = opts || {};
  }

  return new LogStream(this.jenkins, opts);
}
```
- example usage
```shell
...
  if (err) throw err;

  console.log('log', data);
});
'''

<a name="build-log-stream"></a>
### jenkins.build.logStream(options, callback)

Get build log stream.

Options

* name (String): job name
* number (Integer): build number
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Build.prototype.stop"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Build.prototype.</span>stop (opts, callback)](#apidoc.element.jenkins.Jenkins.Build.prototype.stop)
- description and source-code
```javascript
stop = function (opts, callback) {
  var arg0 = typeof arguments[0];
  var arg1 = typeof arguments[1];

  if (arg0 === 'string' && (arg1 === 'string' || arg1 === 'number')) {
    opts = {
      name: arguments[0],
      number: arguments[1],
    };
    callback = arguments[2];
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'build', 'stop'], opts);

  var req = { name: 'build.stop' };

  utils.options(req, opts);

  try {
    var folder = utils.FolderPath(opts.name);

    if (folder.isEmpty()) throw new Error('name required');
    if (!opts.number) throw new Error('number required');

    req.path = '{folder}/{number}/stop';
    req.params = {
      folder: folder.path(),
      number: opts.number,
    };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(
    req,
    middleware.notFound(opts.name + ' ' + opts.number),
    middleware.require302('failed to stop: ' + opts.name),
    middleware.empty,
    callback
  );
}
```
- example usage
```shell
...

log.on('end', function() {
 console.log('end');
});
'''

<a name="build-stop"></a>
### jenkins.build.stop(options, callback)

Stop build.

Options

* name (String): job name
* number (Integer): build number
...
```



# <a name="apidoc.module.jenkins.Jenkins.CrumbIssuer"></a>[module jenkins.Jenkins.CrumbIssuer](#apidoc.module.jenkins.Jenkins.CrumbIssuer)

#### <a name="apidoc.element.jenkins.Jenkins.CrumbIssuer.CrumbIssuer"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>CrumbIssuer (jenkins)](#apidoc.element.jenkins.Jenkins.CrumbIssuer.CrumbIssuer)
- description and source-code
```javascript
function CrumbIssuer(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
...

papi.Client.call(this, opts);

this._ext('onCreate', this._onCreate);
this._ext('onResponse', this._onResponse);

this.build = new Jenkins.Build(this);
this.crumbIssuer = new Jenkins.CrumbIssuer(this);
this.job = new Jenkins.Job(this);
this.node = new Jenkins.Node(this);
this.queue = new Jenkins.Queue(this);
this.view = new Jenkins.View(this);

try {
  if (opts.promisify) {
...
```



# <a name="apidoc.module.jenkins.Jenkins.CrumbIssuer.prototype"></a>[module jenkins.Jenkins.CrumbIssuer.prototype](#apidoc.module.jenkins.Jenkins.CrumbIssuer.prototype)

#### <a name="apidoc.element.jenkins.Jenkins.CrumbIssuer.prototype.get"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.CrumbIssuer.prototype.</span>get (opts, callback)](#apidoc.element.jenkins.Jenkins.CrumbIssuer.prototype.get)
- description and source-code
```javascript
get = function (opts, callback) {
  if (typeof opts === 'function') {
    callback = opts;
    opts = {};
  }

  this.jenkins._log(['debug', 'crumbIssuer', 'get'], opts);

  var req = {
    name: 'crumbIssuer.get',
    path: '/crumbIssuer/api/json',
  };

  utils.options(req, opts);

  return this.jenkins._get(req, middleware.body, callback);
}
```
- example usage
```shell
...
     "url": "http://localhost:8080/"
   }
 ]
}
'''

<a name="build-get"></a>
### jenkins.build.get(options, callback)

Get build information.

Options

* name (String): job name
* number (Integer): build number
...
```



# <a name="apidoc.module.jenkins.Jenkins.Job"></a>[module jenkins.Jenkins.Job](#apidoc.module.jenkins.Jenkins.Job)

#### <a name="apidoc.element.jenkins.Jenkins.Job.Job"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>Job (jenkins)](#apidoc.element.jenkins.Jenkins.Job.Job)
- description and source-code
```javascript
function Job(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
...
papi.Client.call(this, opts);

this._ext('onCreate', this._onCreate);
this._ext('onResponse', this._onResponse);

this.build = new Jenkins.Build(this);
this.crumbIssuer = new Jenkins.CrumbIssuer(this);
this.job = new Jenkins.Job(this);
this.node = new Jenkins.Node(this);
this.queue = new Jenkins.Queue(this);
this.view = new Jenkins.View(this);

try {
  if (opts.promisify) {
    if (typeof opts.promisify === 'function') {
...
```



# <a name="apidoc.module.jenkins.Jenkins.Job.prototype"></a>[module jenkins.Jenkins.Job.prototype](#apidoc.module.jenkins.Jenkins.Job.prototype)

#### <a name="apidoc.element.jenkins.Jenkins.Job.prototype.build"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>build (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.build)
- description and source-code
```javascript
build = function (opts, callback) {
  var arg0 = typeof arguments[0];
  var arg1 = typeof arguments[1];
  var arg2 = typeof arguments[2];

  if (arg0 === 'string') {
    if (arg1 === 'object') {
      opts = arguments[1];
      callback = arg2 === 'function' ? arguments[2] : undefined;
    } else {
      opts = {};
      callback = arg1 === 'function' ? arguments[1] : undefined;
    }
    opts.name = arguments[0];
  }

  opts = opts || {};

  this.jenkins._log(['debug', 'job', 'build'], opts);

  var req = { name: 'job.build' };

  utils.options(req, opts);

  try {
    var folder = utils.FolderPath(opts.name);

    if (folder.isEmpty()) throw new Error('name required');

    req.path = '{folder}/build';
    req.params = { folder: folder.path() };

    if (opts.parameters) {
      req.path += 'WithParameters';
      req.query = opts.parameters;
    }

    if (opts.token) req.query.token = opts.token;
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(
    req,
    middleware.notFound(opts.name),
    middleware.queueLocation,
    callback
  );
}
```
- example usage
```shell
...
''' javascript
jenkins.build.stop('example', 1, function(err) {
 if (err) throw err;
});
'''

<a name="job-build"></a>
### jenkins.job.build(options, callback)

Trigger build.

Options

* name (String): job name
* parameters (Object, optional): build parameters
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Job.prototype.config"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>config (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.config)
- description and source-code
```javascript
config = function (opts, callback) {
  var arg0 = typeof arguments[0];
  var arg1 = typeof arguments[1];
  var arg2 = typeof arguments[2];

  if (arg0 === 'string') {
    opts = { name: arguments[0] };
    if (arg1 === 'string') {
      opts.xml = arguments[1];
      callback = arg2 === 'function' ? arguments[2] : undefined;
    } else {
      callback = arg1 === 'function' ? arguments[1] : undefined;
    }
  }

  opts = opts || {};

  this.jenkins._log(['debug', 'job', 'config'], opts);

  var req = { name: 'job.config' };

  utils.options(req, opts);

  try {
    var folder = utils.FolderPath(opts.name);

    if (folder.isEmpty()) throw new Error('name required');

    req.path = '{folder}/config.xml';
    req.params = { folder: folder.path() };

    if (opts.xml) {
      req.method = 'POST';
      req.headers = { 'content-type': 'text/xml' };
      req.body = new Buffer(opts.xml);
    } else {
      req.method = 'GET';
    }
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._request(
    req,
    middleware.notFound('job ' + opts.name),
    function(ctx, next) {
      if (ctx.err || opts.xml) return middleware.empty(ctx, next);

      next(false, null, ctx.res.body.toString('utf8'));
    },
    callback
  );
}
```
- example usage
```shell
...
''' javascript
jenkins.job.build({ name: 'example': parameters: { name: 'value' } }, function(err) {
 if (err) throw err;
});
'''

<a name="job-config-get"></a>
### jenkins.job.config(options, callback)

Get job XML configuration.

Options

* name (String): job name
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Job.prototype.copy"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>copy (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.copy)
- description and source-code
```javascript
copy = function (opts, callback) {
  var arg0 = typeof arguments[0];
  var arg1 = typeof arguments[1];
  var arg2 = typeof arguments[2];

  if (arg0 === 'string' && arg1 === 'string') {
    opts = {
      from: arguments[0],
      name: arguments[1],
    };
    callback = arg2 === 'function' ? arguments[2] : undefined;
  }

  opts = opts || {};

  this.jenkins._log(['debug', 'job', 'copy'], opts);

  var req = { name: 'job.copy' };

  utils.options(req, opts);

  try {
    var folder = utils.FolderPath(opts.name);

    if (folder.isEmpty()) throw new Error('name required');
    if (!opts.from) throw new Error('from required');

    req.path = '{dir}/createItem';
    req.headers = { 'content-type': 'text/xml' };
    req.params = { dir: folder.dir() };
    req.query.name = folder.name();
    req.query.from = opts.from;
    req.query.mode = 'copy';
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(
    req,
    middleware.require302('failed to create: ' + opts.name),
    middleware.empty,
    callback
  );
}
```
- example usage
```shell
...
''' javascript
jenkins.job.config('example', xml, function(err) {
 if (err) throw err;
});
'''

<a name="job-config-copy"></a>
### jenkins.job.copy(options, callback)

Create job by copying existing job.

Options

* name (String): new job name
* from (String): source job name
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Job.prototype.create"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>create (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.create)
- description and source-code
```javascript
create = function (opts, callback) {
  var arg0 = typeof arguments[0];
  var arg1 = typeof arguments[1];
  var arg2 = typeof arguments[2];

  if (arg0 === 'string' && arg1 === 'string') {
    opts = {
      name: arguments[0],
      xml: arguments[1],
    };
    callback = arg2 === 'function' ? arguments[2] : undefined;
  }

  opts = opts || {};

  this.jenkins._log(['debug', 'job', 'create'], opts);

  var req = { name: 'job.create' };

  utils.options(req, opts);

  try {
    var folder = utils.FolderPath(opts.name);

    if (folder.isEmpty()) throw new Error('name required');
    if (!opts.xml) throw new Error('xml required');

    req.path = '{dir}/createItem';
    req.headers = { 'content-type': 'text/xml' };
    req.params = { dir: folder.dir() };
    req.query.name = folder.name();
    req.body = new Buffer(opts.xml);
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(req, middleware.empty, callback);
}
```
- example usage
```shell
...
''' javascript
jenkins.job.copy('fromJob', 'example', function(err) {
 if (err) throw err;
});
'''

<a name="job-create"></a>
### jenkins.job.create(options, callback)

Create job from scratch.

Options

* name (String): job name
* xml (String): configuration XML
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Job.prototype.delete"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>delete (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.delete)
- description and source-code
```javascript
delete = function (opts, callback) {
  if (typeof opts === 'string') {
    opts = { name: opts };
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'job', 'destroy'], opts);

  var req = { name: 'job.destroy' };

  utils.options(req, opts);

  try {
    var folder = utils.FolderPath(opts.name);

    if (folder.isEmpty()) throw new Error('name required');

    req.path = '{folder}/doDelete';
    req.params = { folder: folder.path() };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(
    req,
    middleware.notFound(opts.name),
    middleware.require302('failed to delete: ' + opts.name),
    middleware.empty,
    callback
  );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.Job.prototype.destroy"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>destroy (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.destroy)
- description and source-code
```javascript
destroy = function (opts, callback) {
  if (typeof opts === 'string') {
    opts = { name: opts };
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'job', 'destroy'], opts);

  var req = { name: 'job.destroy' };

  utils.options(req, opts);

  try {
    var folder = utils.FolderPath(opts.name);

    if (folder.isEmpty()) throw new Error('name required');

    req.path = '{folder}/doDelete';
    req.params = { folder: folder.path() };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(
    req,
    middleware.notFound(opts.name),
    middleware.require302('failed to delete: ' + opts.name),
    middleware.empty,
    callback
  );
}
```
- example usage
```shell
...
''' javascript
jenkins.job.create('example', xml, function(err) {
 if (err) throw err;
});
'''

<a name="job-destroy"></a>
### jenkins.job.destroy(options, callback)

Delete job.

Options

* name (String): job name
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Job.prototype.disable"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>disable (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.disable)
- description and source-code
```javascript
disable = function (opts, callback) {
  if (typeof opts === 'string') {
    opts = { name: opts };
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'job', 'disable'], opts);

  var req = { name: 'job.disable' };

  utils.options(req, opts);

  try {
    var folder = utils.FolderPath(opts.name);

    if (folder.isEmpty()) throw new Error('name required');

    req.path = '{folder}/disable';
    req.params = { folder: folder.path() };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(
    req,
    middleware.notFound(opts.name),
    middleware.require302('failed to disable: ' + opts.name),
    middleware.empty,
    callback
  );
}
```
- example usage
```shell
...
''' javascript
jenkins.job.destroy('example', function(err) {
 if (err) throw err;
});
'''

<a name="job-disable"></a>
### jenkins.job.disable(options, callback)

Disable job.

Options

* name (String): job name
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Job.prototype.enable"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>enable (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.enable)
- description and source-code
```javascript
enable = function (opts, callback) {
  if (typeof opts === 'string') {
    opts = { name: opts };
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'job', 'enable'], opts);

  var req = { name: 'job.enable' };

  utils.options(req, opts);

  try {
    var folder = utils.FolderPath(opts.name);

    if (folder.isEmpty()) throw new Error('name required');

    req.path = '{folder}/enable';
    req.params = { folder: folder.path() };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(
    req,
    middleware.notFound(opts.name),
    middleware.require302('failed to enable: ' + opts.name),
    middleware.empty,
    callback
  );
}
```
- example usage
```shell
...
''' javascript
jenkins.job.disable('example', function(err) {
 if (err) throw err;
});
'''

<a name="job-enable"></a>
### jenkins.job.enable(options, callback)

Enable job.

Options

* name (String): job name
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Job.prototype.exists"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>exists (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.exists)
- description and source-code
```javascript
exists = function (opts, callback) {
  if (typeof opts === 'string') {
    opts = { name: opts };
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'job', 'exists'], opts);

  var req = { name: 'job.exists' };

  utils.options(req, opts);

  try {
    var folder = utils.FolderPath(opts.name);

    if (folder.isEmpty()) throw new Error('name required');

    req.path = '{folder}/api/json';
    req.params = { folder: folder.path() };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._head(req, middleware.exists, callback);
}
```
- example usage
```shell
...
''' javascript
jenkins.job.enable('example', function(err) {
 if (err) throw err;
});
'''

<a name="job-exists"></a>
### jenkins.job.exists(options, callback)

Check job exists.

Options

* name (String): job name
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Job.prototype.get"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>get (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.get)
- description and source-code
```javascript
get = function (opts, callback) {
  var arg0 = typeof arguments[0];
  var arg1 = typeof arguments[1];
  var arg2 = typeof arguments[2];

  if (arg0 === 'string') {
    if (arg1 === 'object') {
      opts = arguments[1];
      callback = arg2 === 'function' ? arguments[2] : undefined;
    } else {
      opts = {};
      callback = arg1 === 'function' ? arguments[1] : undefined;
    }
    opts.name = arguments[0];
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'job', 'get'], opts);

  var req = { name: 'job.get' };

  utils.options(req, opts);

  try {
    var folder = utils.FolderPath(opts.name);

    if (folder.isEmpty()) throw new Error('name required');

    req.path = '{folder}/api/json';
    req.params = { folder: folder.path() };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._get(
    req,
    middleware.notFound(opts.name),
    middleware.body,
    callback
  );
}
```
- example usage
```shell
...
     "url": "http://localhost:8080/"
   }
 ]
}
'''

<a name="build-get"></a>
### jenkins.build.get(options, callback)

Get build information.

Options

* name (String): job name
* number (Integer): build number
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Job.prototype.list"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Job.prototype.</span>list (opts, callback)](#apidoc.element.jenkins.Jenkins.Job.prototype.list)
- description and source-code
```javascript
list = function (opts, callback) {
  if (typeof opts === 'function') {
    callback = opts;
    opts = {};
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'job', 'list'], opts);

  var req = {
    name: 'job.list',
    path: '/api/json',
  };

  utils.options(req, opts);

  return this.jenkins._get(
    req,
    function(ctx, next) {
      if (ctx.err) return next();

      if (!ctx.res.body || !Array.isArray(ctx.res.body.jobs)) {
        ctx.err = new Error('returned bad data');
      }

      next();
    },
    middleware.bodyItem('jobs'),
    callback
  );
}
```
- example usage
```shell
...
  "scm": {},
  "upstreamProjects": [],
  "url": "http://localhost:8080/job/example/"
}
'''

<a name="job-list"></a>
### jenkins.job.list(callback)

List all jobs.

Usage

''' javascript
jenkins.job.list(function(err, data) {
...
```



# <a name="apidoc.module.jenkins.Jenkins.Node"></a>[module jenkins.Jenkins.Node](#apidoc.module.jenkins.Jenkins.Node)

#### <a name="apidoc.element.jenkins.Jenkins.Node.Node"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>Node (jenkins)](#apidoc.element.jenkins.Jenkins.Node.Node)
- description and source-code
```javascript
function Node(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
...

this._ext('onCreate', this._onCreate);
this._ext('onResponse', this._onResponse);

this.build = new Jenkins.Build(this);
this.crumbIssuer = new Jenkins.CrumbIssuer(this);
this.job = new Jenkins.Job(this);
this.node = new Jenkins.Node(this);
this.queue = new Jenkins.Queue(this);
this.view = new Jenkins.View(this);

try {
  if (opts.promisify) {
    if (typeof opts.promisify === 'function') {
      papi.tools.promisify(this, opts.promisify);
...
```



# <a name="apidoc.module.jenkins.Jenkins.Node.prototype"></a>[module jenkins.Jenkins.Node.prototype](#apidoc.module.jenkins.Jenkins.Node.prototype)

#### <a name="apidoc.element.jenkins.Jenkins.Node.prototype.changeOfflineCause"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>changeOfflineCause (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.changeOfflineCause)
- description and source-code
```javascript
changeOfflineCause = function (opts, callback) {
  opts = opts || {};

  opts.message = opts.message || '';

  this.jenkins._log(['debug', 'node', 'changeOfflineCause'], opts);

  var req = { name: 'node.changeOfflineCause' };

  utils.options(req, opts);

  try {
    if (!opts.name) throw new Error('name required');

    req.path = '/computer/{name}/changeOfflineCause';
    req.params = { name: opts.name };
    req.type = 'form';
    req.body = {
      offlineMessage: opts.message,
      json: JSON.stringify({
        offlineMessage: opts.message,
      }),
      Submit: 'Update reason',
    };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(
    req,
    middleware.notFound(opts.name),
    middleware.require302('failed to update offline message: ' + opts.name),
    middleware.empty,
    callback
  );
}
```
- example usage
```shell
...
  }

  self.get(opts.name, function(err, node) {
if (err) return callback(err);

if (node && node.temporarilyOffline) {
  if (node.offlineCauseReason !== opts.message) {
    return self.changeOfflineCause({
      name: opts.name,
      message: opts.message,
    }, callback);
  }

  return callback();
}
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Node.prototype.config"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>config (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.config)
- description and source-code
```javascript
config = function (opts, callback) {
  var arg0 = typeof arguments[0];
  var arg1 = typeof arguments[1];
  var arg2 = typeof arguments[2];

  if (arg0 === 'string') {
    opts = { name: arguments[0] };
    if (arg1 === 'string') {
      opts.xml = arguments[1];
      callback = arg2 === 'function' ? arguments[2] : undefined;
    } else {
      callback = arg1 === 'function' ? arguments[1] : undefined;
    }
  }

  opts = opts || {};

  this.jenkins._log(['debug', 'node', 'config'], opts);

  var req = { name: 'node.config' };

  utils.options(req, opts);

  try {
    if (!opts.name) throw new Error('name required');

    req.path = '/computer/{name}/config.xml';
    req.params = {
      name: opts.name === 'master' ? '(master)' : opts.name,
    };

    if (opts.xml) {
      if (opts.name === 'master') {
        throw new Error('master not supported');
      }

      req.method = 'POST';
      req.headers = { 'content-type': 'text/xml' };
      req.body = new Buffer(opts.xml);
    } else {
      req.method = 'GET';
    }
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._request(
    req,
    middleware.notFound('node ' + opts.name),
    function(ctx, next) {
      if (ctx.err || opts.xml) return middleware.empty(ctx, next);

      next(false, null, ctx.res.body.toString('utf8'));
    },
    callback
  );
}
```
- example usage
```shell
...
''' javascript
jenkins.job.build({ name: 'example': parameters: { name: 'value' } }, function(err) {
 if (err) throw err;
});
'''

<a name="job-config-get"></a>
### jenkins.job.config(options, callback)

Get job XML configuration.

Options

* name (String): job name
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Node.prototype.create"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>create (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.create)
- description and source-code
```javascript
create = function (opts, callback) {
  var arg0 = typeof arguments[0];
  var arg1 = typeof arguments[1];
  var arg2 = typeof arguments[2];

  if (arg0 === 'string') {
    if (arg1 === 'object') {
      opts = arguments[1];
      callback = arg2 === 'function' ? arguments[2] : undefined;
    } else {
      opts = {};
      callback = arg1 === 'function' ? arguments[1] : undefined;
    }
    opts.name = arguments[0];
  } else {
    opts = opts || {};
  }

  opts.type = opts.type || 'hudson.slaves.DumbSlave$DescriptorImpl';
  opts.retentionStrategy = opts.retentionStrategy ||
    { 'stapler-class': 'hudson.slaves.RetentionStrategy$Always' };
  opts.nodeProperties = opts.nodeProperties || { 'stapler-class-bag': 'true' };
  opts.launcher = opts.launcher ||
    { 'stapler-class': 'hudson.slaves.JNLPLauncher' };
  opts.numExecutors = opts.hasOwnProperty('numExecutors') ?
    opts.numExecutors : 2;
  opts.remoteFS = opts.remoteFS || '/var/lib/jenkins';
  opts.mode = opts.mode || (opts.exclusive ? 'EXCLUSIVE' : 'NORMAL');

  this.jenkins._log(['debug', 'node', 'create'], opts);

  var req = { name: 'node.create' };

  utils.options(req, opts);

  try {
    if (!opts.name) throw new Error('name required');

    req.path = '/computer/doCreateItem';
    req.query.name = opts.name;
    req.query.type = opts.type;
    req.query.json = JSON.stringify({
      name: opts.name,
      nodeDescription: opts.nodeDescription,
      numExecutors: opts.numExecutors,
      remoteFS: opts.remoteFS,
      labelString: opts.labelString,
      mode: opts.mode,
      type: opts.type,
      retentionStrategy: opts.retentionStrategy,
      nodeProperties: opts.nodeProperties,
      launcher: opts.launcher,
    });
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(
    req,
    middleware.require302('failed to create: ' + opts.name),
    middleware.empty,
    callback
  );
}
```
- example usage
```shell
...
''' javascript
jenkins.job.copy('fromJob', 'example', function(err) {
 if (err) throw err;
});
'''

<a name="job-create"></a>
### jenkins.job.create(options, callback)

Create job from scratch.

Options

* name (String): job name
* xml (String): configuration XML
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Node.prototype.delete"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>delete (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.delete)
- description and source-code
```javascript
delete = function (opts, callback) {
  if (typeof opts === 'string') {
    opts = { name: opts };
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'node', 'destroy'], opts);

  var req = { name: 'node.destroy' };

  utils.options(req, opts);

  try {
    if (!opts.name) throw new Error('name required');

    req.path = '/computer/{name}/doDelete';
    req.params = { name: opts.name };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(
    req,
    middleware.notFound(opts.name),
    middleware.require302('failed to delete: ' + opts.name),
    middleware.empty,
    callback
  );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.Node.prototype.destroy"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>destroy (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.destroy)
- description and source-code
```javascript
destroy = function (opts, callback) {
  if (typeof opts === 'string') {
    opts = { name: opts };
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'node', 'destroy'], opts);

  var req = { name: 'node.destroy' };

  utils.options(req, opts);

  try {
    if (!opts.name) throw new Error('name required');

    req.path = '/computer/{name}/doDelete';
    req.params = { name: opts.name };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(
    req,
    middleware.notFound(opts.name),
    middleware.require302('failed to delete: ' + opts.name),
    middleware.empty,
    callback
  );
}
```
- example usage
```shell
...
''' javascript
jenkins.job.create('example', xml, function(err) {
 if (err) throw err;
});
'''

<a name="job-destroy"></a>
### jenkins.job.destroy(options, callback)

Delete job.

Options

* name (String): job name
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Node.prototype.disable"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>disable (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.disable)
- description and source-code
```javascript
disable = function (opts, callback) {
  var self = this;

  var arg0 = typeof arguments[0];
  var arg1 = typeof arguments[1];

  if (arg0 === 'string' && arg1 === 'string') {
    opts = {
      name: arguments[0],
      message: arguments[1],
    };
    callback = arguments[2];
  } else if (typeof opts === 'string') {
    opts = { name: opts };
  } else {
    opts = opts || {};
  }

  self.jenkins._log(['debug', 'node', 'disable'], opts);

  if (!opts.name) {
    return callback(this.jenkins._err('name required', { name: 'node.disable' }));
  }

  self.get(opts.name, function(err, node) {
    if (err) return callback(err);

    if (node && node.temporarilyOffline) {
      if (node.offlineCauseReason !== opts.message) {
        return self.changeOfflineCause({
          name: opts.name,
          message: opts.message,
        }, callback);
      }

      return callback();
    }

    self.toggleOffline({ name: opts.name, message: opts.message }, function(err) {
      if (err) return callback(err);

      callback();
    });
  });
}
```
- example usage
```shell
...
''' javascript
jenkins.job.destroy('example', function(err) {
 if (err) throw err;
});
'''

<a name="job-disable"></a>
### jenkins.job.disable(options, callback)

Disable job.

Options

* name (String): job name
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Node.prototype.disconnect"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>disconnect (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.disconnect)
- description and source-code
```javascript
disconnect = function (opts, callback) {
  var self = this;

  var arg0 = typeof arguments[0];
  var arg1 = typeof arguments[1];

  if (arg0 === 'string' && arg1 === 'string') {
    opts = {
      name: arguments[0],
      message: arguments[1],
    };
    callback = arguments[2];
  } else if (typeof opts === 'string') {
    opts = { name: opts };
  } else {
    opts = opts || {};
  }

  self.jenkins._log(['debug', 'node', 'disconnect'], opts);

  if (!opts.name) {
    return callback(this.jenkins._err('name required', { name: 'node.disconnect' }));
  }

  self.get(opts.name, function(err, node) {
    if (err) return callback(err);

    if (node && node.offline) {
      return self.toggleOffline({ name: opts.name, message: opts.message }, function(err) {
        if (err) return callback(err);

        callback();
      });
    }

    self.doDisconnect({ name: opts.name, message: opts.message }, function(err) {
      if (err) return callback(err);

      callback();
    });
  });
}
```
- example usage
```shell
...
''' javascript
jenkins.node.destroy('slave', function(err) {
 if (err) throw err;
});
'''

<a name="node-disconnect"></a>
### jenkins.node.disconnect(options, callback)

Disconnect node.

Options

* name (String): node name
* message (String, optional): reason for being disconnected
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Node.prototype.doDisconnect"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>doDisconnect (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.doDisconnect)
- description and source-code
```javascript
doDisconnect = function (opts, callback) {
  opts = opts || {};

  this.jenkins._log(['debug', 'node', 'doDisconnect'], opts);

  var req = { name: 'node.doDisconnect' };

  utils.options(req, opts);

  try {
    if (!opts.name) throw new Error('name required');

    req.path = '/computer/{name}/doDisconnect';
    req.params = { name: opts.name };
    req.query.offlineMessage = opts.message || '';
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(
      req,
      middleware.notFound(opts.name),
      middleware.require302('failed to disconnect: ' + opts.name),
      middleware.empty,
      callback
  );
}
```
- example usage
```shell
...
      return self.toggleOffline({ name: opts.name, message: opts.message }, function(err) {
        if (err) return callback(err);

        callback();
      });
    }

    self.doDisconnect({ name: opts.name, message: opts.message }, function(err) {
      if (err) return callback(err);

      callback();
    });
  });
};
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Node.prototype.enable"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>enable (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.enable)
- description and source-code
```javascript
enable = function (opts, callback) {
  var self = this;

  if (typeof opts === 'string') {
    opts = { name: opts };
  } else {
    opts = opts || {};
  }

  self.jenkins._log(['debug', 'node', 'enable'], opts);

  if (!opts.name) {
    return callback(this.jenkins._err('name required', { name: 'node.enable' }));
  }

  self.get(opts.name, function(err, node) {
    if (err) return callback(err);

    if (!node.temporarilyOffline) return callback();

    self.toggleOffline({ name: opts.name, message: '' }, function(err) {
      if (err) callback(err);

      callback();
    });
  });
}
```
- example usage
```shell
...
''' javascript
jenkins.job.disable('example', function(err) {
 if (err) throw err;
});
'''

<a name="job-enable"></a>
### jenkins.job.enable(options, callback)

Enable job.

Options

* name (String): job name
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Node.prototype.exists"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>exists (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.exists)
- description and source-code
```javascript
exists = function (opts, callback) {
  if (typeof opts === 'string') {
    opts = { name: opts };
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'build', 'exists'], opts);

  var req = { name: 'node.exists' };

  utils.options(req, opts);

  try {
    if (!opts.name) throw new Error('name required');

    req.path = '/computer/{name}/api/json';
    req.params = {
      name: opts.name === 'master' ? '(master)' : opts.name,
    };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._head(req, middleware.exists, callback);
}
```
- example usage
```shell
...
''' javascript
jenkins.job.enable('example', function(err) {
 if (err) throw err;
});
'''

<a name="job-exists"></a>
### jenkins.job.exists(options, callback)

Check job exists.

Options

* name (String): job name
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Node.prototype.get"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>get (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.get)
- description and source-code
```javascript
get = function (opts, callback) {
  if (typeof opts === 'string') {
    opts = { name: opts };
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'node', 'get'], opts);

  var req = { name: 'node.get' };

  utils.options(req, opts);

  try {
    if (!opts.name) throw new Error('name required');

    req.path = '/computer/{name}/api/json';
    req.params = {
      name: opts.name === 'master' ? '(master)' : opts.name,
    };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._get(
    req,
    middleware.notFound(opts.name),
    middleware.body,
    callback
  );
}
```
- example usage
```shell
...
     "url": "http://localhost:8080/"
   }
 ]
}
'''

<a name="build-get"></a>
### jenkins.build.get(options, callback)

Get build information.

Options

* name (String): job name
* number (Integer): build number
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Node.prototype.list"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>list (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.list)
- description and source-code
```javascript
list = function (opts, callback) {
  if (typeof opts === 'function') {
    callback = opts;
    opts = {};
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'node', 'list'], opts);

  var req = {
    name: 'node.list',
    path: '/computer/api/json',
  };

  utils.options(req, opts);

  if (opts.full === true) {
    return this.jenkins._get(
      req,
      middleware.body,
      callback
    );
  } else {
    return this.jenkins._get(
      req,
      middleware.bodyItem('computer'),
      callback
    );
  }
}
```
- example usage
```shell
...
  "scm": {},
  "upstreamProjects": [],
  "url": "http://localhost:8080/job/example/"
}
'''

<a name="job-list"></a>
### jenkins.job.list(callback)

List all jobs.

Usage

''' javascript
jenkins.job.list(function(err, data) {
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Node.prototype.toggleOffline"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Node.prototype.</span>toggleOffline (opts, callback)](#apidoc.element.jenkins.Jenkins.Node.prototype.toggleOffline)
- description and source-code
```javascript
toggleOffline = function (opts, callback) {
  opts = opts || {};

  this.jenkins._log(['debug', 'node', 'toggleOffline'], opts);

  var req = { name: 'node.toggleOffline' };

  utils.options(req, opts);

  try {
    if (!opts.name) throw new Error('name required');

    req.path = '/computer/{name}/toggleOffline';
    req.params = { name: opts.name };
    req.query.offlineMessage = opts.message || '';
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(
    req,
    middleware.notFound(opts.name),
    middleware.require302('failed to toggle offline: ' + opts.name),
    middleware.empty,
    callback
  );
}
```
- example usage
```shell
...
return callback(this.jenkins._err('name required', { name: 'node.disconnect' }));
  }

  self.get(opts.name, function(err, node) {
if (err) return callback(err);

if (node && node.offline) {
  return self.toggleOffline({ name: opts.name, message: opts.message }, function(err) {
    if (err) return callback(err);

    callback();
  });
}

self.doDisconnect({ name: opts.name, message: opts.message }, function(err) {
...
```



# <a name="apidoc.module.jenkins.Jenkins.Queue"></a>[module jenkins.Jenkins.Queue](#apidoc.module.jenkins.Jenkins.Queue)

#### <a name="apidoc.element.jenkins.Jenkins.Queue.Queue"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>Queue (jenkins)](#apidoc.element.jenkins.Jenkins.Queue.Queue)
- description and source-code
```javascript
function Queue(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
...
this._ext('onCreate', this._onCreate);
this._ext('onResponse', this._onResponse);

this.build = new Jenkins.Build(this);
this.crumbIssuer = new Jenkins.CrumbIssuer(this);
this.job = new Jenkins.Job(this);
this.node = new Jenkins.Node(this);
this.queue = new Jenkins.Queue(this);
this.view = new Jenkins.View(this);

try {
  if (opts.promisify) {
    if (typeof opts.promisify === 'function') {
      papi.tools.promisify(this, opts.promisify);
    } else {
...
```



# <a name="apidoc.module.jenkins.Jenkins.Queue.prototype"></a>[module jenkins.Jenkins.Queue.prototype](#apidoc.module.jenkins.Jenkins.Queue.prototype)

#### <a name="apidoc.element.jenkins.Jenkins.Queue.prototype.cancel"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Queue.prototype.</span>cancel (opts, callback)](#apidoc.element.jenkins.Jenkins.Queue.prototype.cancel)
- description and source-code
```javascript
cancel = function (opts, callback) {
  if (typeof opts !== 'object') {
    opts = { number: opts };
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'queue', 'cancel'], opts);

  var req = { name: 'queue.cancel' };

  utils.options(req, opts);

  try {
    if (!opts.number) throw new Error('number required');

    req.path = '/queue/item/{number}/cancelQueue';
    req.params = { number: opts.number };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(
    req,
    middleware.require302('failed to cancel: ' + opts.number),
    middleware.empty,
    callback
  );
}
```
- example usage
```shell
...
 }
}
'''



<a name="queue-cancel"></a>
### jenkins.queue.cancel(options, callback)

Cancel build in queue.

Options

* number (Integer): queue item id
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Queue.prototype.get"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Queue.prototype.</span>get (opts, callback)](#apidoc.element.jenkins.Jenkins.Queue.prototype.get)
- description and source-code
```javascript
get = function (opts, callback) {
  if (typeof opts === 'function') {
    callback = opts;
    opts = {};
  } else {
    opts = opts || {};
  }

  this.list(opts, function(err, data) {
    if (err) return callback(err);

    callback(err, { items: data });
  });
}
```
- example usage
```shell
...
     "url": "http://localhost:8080/"
   }
 ]
}
'''

<a name="build-get"></a>
### jenkins.build.get(options, callback)

Get build information.

Options

* name (String): job name
* number (Integer): build number
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Queue.prototype.item"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Queue.prototype.</span>item (opts, callback)](#apidoc.element.jenkins.Jenkins.Queue.prototype.item)
- description and source-code
```javascript
item = function (opts, callback) {
  var arg0 = typeof arguments[0];

  if (arg0 === 'function') {
    callback = opts;
    opts = {};
  } else {
    if (arg0 === 'string' || arg0 === 'number') {
      opts = {
        number: opts
      };
    }
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'queue', 'item'], opts);

  var req = {
    name: 'queue.item',
    path: '/queue/item/{number}/api/json',
    params: {
      number: opts.number
    }
  };

  utils.options(req, opts);

  if (!opts.number) {
    return callback(this.jenkins._err(new Error('number required'), req));
  }

  return this.jenkins._get(req, middleware.body, callback);
}
```
- example usage
```shell
...
     "why": "Build #2 is already in progress (ETA:N/A)"
   }
 ]
}
'''

<a name="queue-item"></a>
### jenkins.queue.item(options, callback)

Lookup a queue item.

Options

* number (Integer): queue item number
...
```

#### <a name="apidoc.element.jenkins.Jenkins.Queue.prototype.list"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.Queue.prototype.</span>list (opts, callback)](#apidoc.element.jenkins.Jenkins.Queue.prototype.list)
- description and source-code
```javascript
list = function (opts, callback) {
  if (typeof opts === 'function') {
    callback = opts;
    opts = {};
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'queue', 'list'], opts);

  var req = {
    name: 'queue.list',
    path: '/queue/api/json',
  };

  utils.options(req, opts);

  return this.jenkins._get(req, middleware.bodyItem('items'), callback);
}
```
- example usage
```shell
...
  "scm": {},
  "upstreamProjects": [],
  "url": "http://localhost:8080/job/example/"
}
'''

<a name="job-list"></a>
### jenkins.job.list(callback)

List all jobs.

Usage

''' javascript
jenkins.job.list(function(err, data) {
...
```



# <a name="apidoc.module.jenkins.Jenkins.View"></a>[module jenkins.Jenkins.View](#apidoc.module.jenkins.Jenkins.View)

#### <a name="apidoc.element.jenkins.Jenkins.View.View"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>View (jenkins)](#apidoc.element.jenkins.Jenkins.View.View)
- description and source-code
```javascript
function View(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
...
this._ext('onResponse', this._onResponse);

this.build = new Jenkins.Build(this);
this.crumbIssuer = new Jenkins.CrumbIssuer(this);
this.job = new Jenkins.Job(this);
this.node = new Jenkins.Node(this);
this.queue = new Jenkins.Queue(this);
this.view = new Jenkins.View(this);

try {
  if (opts.promisify) {
    if (typeof opts.promisify === 'function') {
      papi.tools.promisify(this, opts.promisify);
    } else {
      papi.tools.promisify(this);
...
```



# <a name="apidoc.module.jenkins.Jenkins.View.prototype"></a>[module jenkins.Jenkins.View.prototype](#apidoc.module.jenkins.Jenkins.View.prototype)

#### <a name="apidoc.element.jenkins.Jenkins.View.prototype.add"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.View.prototype.</span>add (opts, callback)](#apidoc.element.jenkins.Jenkins.View.prototype.add)
- description and source-code
```javascript
add = function (opts, callback) {
  var arg0 = typeof arguments[0];
  var arg1 = typeof arguments[1];
  var arg2 = typeof arguments[2];

  if (arg0 === 'string' && arg1 === 'string') {
    opts = {
      name: arguments[0],
      job: arguments[1],
    };
    callback = arg2 === 'function' ? arguments[2] : undefined;
  }

  opts = opts || {};

  this.jenkins._log(['debug', 'view', 'add'], opts);

  var req = {
    path: '{dir}/view/{name}/addJobToView',
    query: { name: opts.job },
    type: 'form',
    name: 'view.add',
    body: {},
  };

  utils.options(req, opts);

  try {
    var folder = utils.FolderPath(opts.name);

    if (folder.isEmpty()) throw new Error('name required');
    if (!opts.job) throw new Error('job required');

    req.params = { dir: folder.dir(), name: folder.name() };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(
    req,
    middleware.empty,
    callback
  );
}
```
- example usage
```shell
...
   }
 ],
 "overallLoad": {}
}
'''

<a name="view-add"></a>
### jenkins.view.add(options, callback)

Add job to view.

Options

* name (String): view name
* job (String): job name
...
```

#### <a name="apidoc.element.jenkins.Jenkins.View.prototype.config"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.View.prototype.</span>config (opts, callback)](#apidoc.element.jenkins.Jenkins.View.prototype.config)
- description and source-code
```javascript
config = function (opts, callback) {
  var arg0 = typeof arguments[0];
  var arg1 = typeof arguments[1];
  var arg2 = typeof arguments[2];

  if (arg0 === 'string') {
    opts = { name: arguments[0] };
    if (arg1 === 'string') {
      opts.xml = arguments[1];
      callback = arg2 === 'function' ? arguments[2] : undefined;
    } else {
      callback = arg1 === 'function' ? arguments[1] : undefined;
    }
  }

  opts = opts || {};

  this.jenkins._log(['debug', 'view', 'config'], opts);

  var req = {
    path: '{dir}/view/{name}/config.xml',
    name: 'view.config',
  };

  utils.options(req, opts);

  try {
    var folder = utils.FolderPath(opts.name);

    if (folder.isEmpty()) throw new Error('name required');

    req.params = { dir: folder.dir(), name: folder.name() };

    if (opts.xml) {
      req.method = 'POST';
      req.headers = { 'content-type': 'text/xml' };
      req.body = new Buffer(opts.xml);
    } else {
      req.method = 'GET';
    }
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._request(
    req,
    middleware.notFound('view ' + opts.name),
    function(ctx, next) {
      if (ctx.err || opts.xml) return middleware.empty(ctx, next);

      next(false, null, ctx.res.body.toString('utf8'));
    },
    callback
  );
}
```
- example usage
```shell
...
''' javascript
jenkins.job.build({ name: 'example': parameters: { name: 'value' } }, function(err) {
 if (err) throw err;
});
'''

<a name="job-config-get"></a>
### jenkins.job.config(options, callback)

Get job XML configuration.

Options

* name (String): job name
...
```

#### <a name="apidoc.element.jenkins.Jenkins.View.prototype.create"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.View.prototype.</span>create (opts, callback)](#apidoc.element.jenkins.Jenkins.View.prototype.create)
- description and source-code
```javascript
create = function (opts, callback) {
  var arg0 = typeof arguments[0];
  var arg1 = typeof arguments[1];
  var arg2 = typeof arguments[2];

  if (arg0 === 'string' && arg1 === 'string') {
    opts = {
      name: arguments[0],
      type: arguments[1],
    };
    callback = arg2 === 'function' ? arguments[2] : undefined;
  } else if (arg0 === 'string') {
    opts = {
      name: arguments[0],
      type: 'list',
    };
  }

  opts = opts || {};

  this.jenkins._log(['debug', 'view', 'create'], opts);

  var req = { name: 'view.create' };

  utils.options(req, opts);

  var shortcuts = {
    list: 'hudson.model.ListView',
    my: 'hudson.model.MyView',
  };

  try {
    var folder = utils.FolderPath(opts.name);
    var mode = shortcuts[opts.type] || opts.type;

    if (folder.isEmpty()) throw new Error('name required');
    if (!opts.type) throw new Error('type required');

    req.path = '{dir}/createView';
    req.type = 'form';
    req.params = { dir: folder.dir() };
    req.body = {
      name: folder.name(),
      mode: mode,
      json: JSON.stringify({
        name: folder.name(),
        mode: mode,
      }),
    };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(
    req,
    middleware.require302('failed to create: ' + opts.name),
    middleware.empty,
    callback
  );
}
```
- example usage
```shell
...
''' javascript
jenkins.job.copy('fromJob', 'example', function(err) {
 if (err) throw err;
});
'''

<a name="job-create"></a>
### jenkins.job.create(options, callback)

Create job from scratch.

Options

* name (String): job name
* xml (String): configuration XML
...
```

#### <a name="apidoc.element.jenkins.Jenkins.View.prototype.delete"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.View.prototype.</span>delete (opts, callback)](#apidoc.element.jenkins.Jenkins.View.prototype.delete)
- description and source-code
```javascript
delete = function (opts, callback) {
  if (typeof opts === 'string') {
    opts = { name: opts };
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'view', 'destroy'], opts);

  var req = { name: 'view.destroy' };

  utils.options(req, opts);

  try {
    var folder = utils.FolderPath(opts.name);

    if (folder.isEmpty()) throw new Error('name required');

    req.path = '{dir}/view/{name}/doDelete';
    req.params = { dir: folder.dir(), name: folder.name() };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(
    req,
    middleware.notFound(opts.name),
    middleware.require302('failed to delete: ' + opts.name),
    middleware.empty,
    callback
  );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.View.prototype.destroy"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.View.prototype.</span>destroy (opts, callback)](#apidoc.element.jenkins.Jenkins.View.prototype.destroy)
- description and source-code
```javascript
destroy = function (opts, callback) {
  if (typeof opts === 'string') {
    opts = { name: opts };
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'view', 'destroy'], opts);

  var req = { name: 'view.destroy' };

  utils.options(req, opts);

  try {
    var folder = utils.FolderPath(opts.name);

    if (folder.isEmpty()) throw new Error('name required');

    req.path = '{dir}/view/{name}/doDelete';
    req.params = { dir: folder.dir(), name: folder.name() };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(
    req,
    middleware.notFound(opts.name),
    middleware.require302('failed to delete: ' + opts.name),
    middleware.empty,
    callback
  );
}
```
- example usage
```shell
...
''' javascript
jenkins.job.create('example', xml, function(err) {
 if (err) throw err;
});
'''

<a name="job-destroy"></a>
### jenkins.job.destroy(options, callback)

Delete job.

Options

* name (String): job name
...
```

#### <a name="apidoc.element.jenkins.Jenkins.View.prototype.exists"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.View.prototype.</span>exists (opts, callback)](#apidoc.element.jenkins.Jenkins.View.prototype.exists)
- description and source-code
```javascript
exists = function (opts, callback) {
  if (typeof opts === 'string') {
    opts = { name: opts };
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'view', 'exists'], opts);

  var req = { name: 'view.exists' };

  utils.options(req, opts);

  try {
    var folder = utils.FolderPath(opts.name);

    if (folder.isEmpty()) throw new Error('name required');

    req.path = '{dir}/view/{name}/api/json';
    req.params = { dir: folder.dir(), name: folder.name() };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._head(req, middleware.exists, callback);
}
```
- example usage
```shell
...
''' javascript
jenkins.job.enable('example', function(err) {
 if (err) throw err;
});
'''

<a name="job-exists"></a>
### jenkins.job.exists(options, callback)

Check job exists.

Options

* name (String): job name
...
```

#### <a name="apidoc.element.jenkins.Jenkins.View.prototype.get"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.View.prototype.</span>get (opts, callback)](#apidoc.element.jenkins.Jenkins.View.prototype.get)
- description and source-code
```javascript
get = function (opts, callback) {
  var arg0 = typeof arguments[0];
  var arg1 = typeof arguments[1];
  var arg2 = typeof arguments[2];

  if (arg0 === 'string') {
    if (arg1 === 'object') {
      opts = arguments[1];
      callback = arg2 === 'function' ? arguments[2] : undefined;
    } else {
      opts = {};
      callback = arg1 === 'function' ? arguments[1] : undefined;
    }
    opts.name = arguments[0];
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'view', 'get'], opts);

  var req = { name: 'view.get' };

  utils.options(req, opts);

  try {
    var folder = utils.FolderPath(opts.name);

    if (folder.isEmpty()) throw new Error('name required');

    req.path = '{dir}/view/{name}/api/json';
    req.params = { dir: folder.dir(), name: folder.name() };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._get(
    req,
    middleware.notFound(opts.name),
    middleware.body,
    callback
  );
}
```
- example usage
```shell
...
     "url": "http://localhost:8080/"
   }
 ]
}
'''

<a name="build-get"></a>
### jenkins.build.get(options, callback)

Get build information.

Options

* name (String): job name
* number (Integer): build number
...
```

#### <a name="apidoc.element.jenkins.Jenkins.View.prototype.list"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.View.prototype.</span>list (opts, callback)](#apidoc.element.jenkins.Jenkins.View.prototype.list)
- description and source-code
```javascript
list = function (opts, callback) {
  if (typeof opts === 'function') {
    callback = opts;
    opts = {};
  } else if (typeof opts === 'string') {
    opts = { name: opts };
  } else {
    opts = opts || {};
  }

  this.jenkins._log(['debug', 'view', 'list'], opts);

  var req = {
    name: 'view.list',
    path: '{folder}/api/json',
  };

  try {
    var folder = utils.FolderPath(opts.name);

    req.params = { folder: folder.path() };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  utils.options(req, opts);

  return this.jenkins._get(
    req,
    function(ctx, next) {
      if (ctx.err) return next();

      if (!ctx.res.body || !Array.isArray(ctx.res.body.views)) {
        ctx.err = new Error('returned bad data');
      }

      next();
    },
    middleware.bodyItem('views'),
    callback
  );
}
```
- example usage
```shell
...
  "scm": {},
  "upstreamProjects": [],
  "url": "http://localhost:8080/job/example/"
}
'''

<a name="job-list"></a>
### jenkins.job.list(callback)

List all jobs.

Usage

''' javascript
jenkins.job.list(function(err, data) {
...
```

#### <a name="apidoc.element.jenkins.Jenkins.View.prototype.remove"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.View.prototype.</span>remove (opts, callback)](#apidoc.element.jenkins.Jenkins.View.prototype.remove)
- description and source-code
```javascript
remove = function (opts, callback) {
  var arg0 = typeof arguments[0];
  var arg1 = typeof arguments[1];
  var arg2 = typeof arguments[2];

  if (arg0 === 'string' && arg1 === 'string') {
    opts = {
      name: arguments[0],
      job: arguments[1],
    };
    callback = arg2 === 'function' ? arguments[2] : undefined;
  }

  opts = opts || {};

  this.jenkins._log(['debug', 'view', 'remove'], opts);

  var req = {
    path: '{dir}/view/{name}/removeJobFromView',
    query: { name: opts.job },
    type: 'form',
    name: 'view.remove',
    body: {},
  };

  utils.options(req, opts);

  try {
    var folder = utils.FolderPath(opts.name);

    if (folder.isEmpty()) throw new Error('name required');
    if (!opts.job) throw new Error('job required');

    req.params = { dir: folder.dir(), name: folder.name() };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(
    req,
    middleware.empty,
    callback
  );
}
```
- example usage
```shell
...
''' javascript
jenkins.view.add('example', 'jobExample', function(err) {
 if (err) throw err;
});
'''

<a name="view-remove"></a>
### jenkins.view.remove(options, callback)

Remove job from view.

Options

* name (String): view name
* job (String): job name
...
```



# <a name="apidoc.module.jenkins.Jenkins.prototype"></a>[module jenkins.Jenkins.prototype](#apidoc.module.jenkins.Jenkins.prototype)

#### <a name="apidoc.element.jenkins.Jenkins.prototype._onCreate"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.prototype.</span>_onCreate (ctx, next)](#apidoc.element.jenkins.Jenkins.prototype._onCreate)
- description and source-code
```javascript
_onCreate = function (ctx, next) {
  if (!this._crumbIssuer || ctx.opts.method !== 'POST') return next();

  this._crumbIssuer(this, function(err, data) {
    if (err) return next(err);

    if (data.headerName && data.headerValue) {
      if (!ctx.opts.headers) ctx.opts.headers = {};
      ctx.opts.headers[data.headerName] = data.headerValue;
    }

    next();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.prototype._onResponse"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.prototype.</span>_onResponse (ctx, next)](#apidoc.element.jenkins.Jenkins.prototype._onResponse)
- description and source-code
```javascript
_onResponse = function (ctx, next) {
  if (ctx.err) {
    if (ctx.res && ctx.res.headers && ctx.res.headers['x-error']) {
      ctx.err.message = ctx.res.headers['x-error'].replace(/\?/g, '"');
    }
    ctx.err.res = ctx.res;
  }

  next();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.prototype.get"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.prototype.</span>get (opts, callback)](#apidoc.element.jenkins.Jenkins.prototype.get)
- description and source-code
```javascript
get = function (opts, callback) {
  if (typeof opts === 'function') {
    callback = opts;
    opts = {};
  }

  this._log(['debug', 'info'], opts);

  var req = {
    name: 'info',
    path: '/api/json',
  };

  utils.options(req, opts);

  return this._get(req, middleware.body, callback);
}
```
- example usage
```shell
...
     "url": "http://localhost:8080/"
   }
 ]
}
'''

<a name="build-get"></a>
### jenkins.build.get(options, callback)

Get build information.

Options

* name (String): job name
* number (Integer): build number
...
```

#### <a name="apidoc.element.jenkins.Jenkins.prototype.info"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.prototype.</span>info (opts, callback)](#apidoc.element.jenkins.Jenkins.prototype.info)
- description and source-code
```javascript
info = function (opts, callback) {
  if (typeof opts === 'function') {
    callback = opts;
    opts = {};
  }

  this._log(['debug', 'info'], opts);

  var req = {
    name: 'info',
    path: '/api/json',
  };

  utils.options(req, opts);

  return this._get(req, middleware.body, callback);
}
```
- example usage
```shell
...
Usage

''' javascript
var jenkins = require('jenkins')({ baseUrl: 'http://user:pass@localhost:8080', crumbIssuer: true });
'''

<a name="info"></a>
### jenkins.info(callback)

Get server information.

Usage

''' javascript
jenkins.info(function(err, data) {
...
```

#### <a name="apidoc.element.jenkins.Jenkins.prototype.walk"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.prototype.</span>walk ()](#apidoc.element.jenkins.Jenkins.prototype.walk)
- description and source-code
```javascript
walk = function () {
  return papi.tools.walk(Jenkins);
}
```
- example usage
```shell
...
/**
 * Walk methods
 */

Jenkins.meta.walk = { type: 'sync' };

Jenkins.walk = Jenkins.prototype.walk = function() {
  return papi.tools.walk(Jenkins);
};

/**
 * Module exports.
 */

exports.Jenkins = Jenkins;
...
```



# <a name="apidoc.module.jenkins.Jenkins.super_"></a>[module jenkins.Jenkins.super_](#apidoc.module.jenkins.Jenkins.super_)

#### <a name="apidoc.element.jenkins.Jenkins.super_.super_"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.</span>super_ ()](#apidoc.element.jenkins.Jenkins.super_.super_)
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



# <a name="apidoc.module.jenkins.Jenkins.super_.prototype"></a>[module jenkins.Jenkins.super_.prototype](#apidoc.module.jenkins.Jenkins.super_.prototype)

#### <a name="apidoc.element.jenkins.Jenkins.super_.prototype.__create"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>__create (request, next)](#apidoc.element.jenkins.Jenkins.super_.prototype.__create)
- description and source-code
```javascript
__create = function (request, next) {
  var self = this;

  var opts = request.opts;
  var path = opts.path;

  if (typeof path !== 'string') {
    return next(errors.Validation('path required'));
  }

  var headers = utils.mergeHeaders(self._opts.headers, opts.headers);

  // path
  try {
    path = path.replace(/\{(\w+)\}/g, function(src, dst) {
      if (!opts.params.hasOwnProperty(dst)) {
        throw errors.Validation('missing param: ' + dst);
      }

      var part = opts.params[dst] || '';

      // optionally disable param encoding
      return part.encode === false && part.toString ?
        part.toString() : encodeURIComponent(part);
    });
  } catch (err) {
    return next(err);
  }

  // query
  if (!utils.isEmpty(opts.query)) {
    try {
      path += '?' + self._encode('application/x-www-form-urlencoded',
                                 opts.query).toString();
    } catch (err) {
      return next(err);
    }
  }

  // body
  if (opts.body !== undefined) {
    var mime = constants.MIME_ALIAS[opts.type] ||
      headers['content-type'] ||
      constants.MIME_ALIAS[self._opts.type];

    var isFunction = typeof opts.body === 'function';

    if (isFunction) {
      try {
        request.body = opts.body();
      } catch (err) {
        return next(err);
      }
    } else {
      request.body = opts.body;
    }

    var isBuffer = Buffer.isBuffer(request.body);
    var isStream = utils.isReadableStream(request.body);

    if (!isBuffer && !isStream && !mime) {
      return next(errors.Validation('type required'));
    }

    if (!isBuffer && !isStream) {
      if (self._opts.encoders[mime]) {
        try {
          request.body = this._encode(mime, request.body);
        } catch (err) {
          return next(err);
        }
      } else {
        return next(errors.Codec('type is unknown: ' + mime));
      }
    }

    if (!headers['content-type'] && mime) {
      headers['content-type'] = mime + '; charset=' + constants.CHARSET;
    }

    if (isStream) {
      if (!isFunction) request._retryable = false;
    } else {
      headers['content-length'] = request.body.length;
    }
  } else if (!~constants.EXCLUDE_CONTENT_LENGTH.indexOf(opts.method)) {
    headers['content-length'] = 0;
  }

  // response pipe
  if (opts.pipe) {
    var isPipeFunction = typeof opts.pipe === 'function';

    if (isPipeFunction) {
      try {
        request.pipe = opts.pipe();
      } catch (err) {
        return next(err);
      }
    } else {
      request.pipe = opts.pipe;

      request._retryable = false;
    }

    if (!utils.isWritableStream(request.pipe)) {
      return next(errors.Validation('pipe must be a writable stream'));
    }
  }

  // build http.request options
  request.req = utils.merge(
    utils.pick(self._opts, constants.CLIENT_OPTIONS),
    utils.pick(self._opts.baseUrl, 'auth', 'hostname', 'port', 'path'),
    utils.pick(opts, constants.REQUEST_OPTIONS),
    { headers: headers }
  );

  // append request path to baseUrl
  request.req.path += path;

  // pick http transport
  if (self._opts.baseUrl.protocol === 'https:') {
    request.transport = https;
    if (!request.req.port) request.req.port = 443;
  } else {
    request.transport = http;
    if (!request.req.port) request.req.port = 80;
  }

  if (request.req.auth === null) delete request.req.auth;

  next();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.super_.prototype.__execute"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>__execute (request, next)](#apidoc.element.jenkins.Jenkins.super_.prototype.__execute)
- description and source-code
```javascript
__execute = function (request, next) {
  var self = this;

  if (request.ctx) {
    if (request.ctx.canceled === true) {
      return next(errors.Validation('ctx already canceled'));
    } else if (request.ctx.finished === true) {
      return next(errors.Validation('ctx already finished'));
    }
  }

  var done = false;

  var opts = request.opts;

  var abort;
  var timeoutId;
  var timeout = opts.hasOwnProperty('timeout') ?
    opts.timeout : self._opts.timeout;

  self._log(['papi', 'request'].concat(opts.tags), request.req);

  var req = request.transport.request(request.req);

  var userAgent = req.getHeader('user-agent');

  if (userAgent === undefined) {
    req.setHeader('user-agent', 'papi/' + meta.version);
  } else if (userAgent === null) {
    req.removeHeader('user-agent');
  }

  req.on('error', function(err) {
    self._log(['papi', 'request', 'error'].concat(opts.tags), err);

    if (done) return;
    done = true;

    if (abort) request.ctx.removeListener('cancel', abort);
    if (timeoutId) clearTimeout(timeoutId);

    request.err = err;
    next();
  });

  if (request.ctx) {
    abort = function() {
      req.abort();
      req.emit('error', errors.Abort('request aborted'));
    };

    request.ctx.once('cancel', abort);
  }

  // set request and absolute timeout
  if (timeout && timeout > 0) {
    timeoutId = setTimeout(function() {
      req.emit('timeout');
      req.abort();
    }, timeout);

    req.setTimeout(timeout);
  }

  req.on('timeout', function(err) {
    self._log(['papi', 'request', 'error', 'timeout'].concat(opts.tags));
    if (err) {
      err = errors.Timeout(err);
    } else {
      err = errors.Timeout('request timed out (' + timeout + 'ms)');
    }
    req.emit('error', err);
  });

  req.on('response', function(res) {
    var chunks = [];
    var bodyLength = 0;

    self._log(['papi', 'response'].concat(opts.tags), {
      method: opts.method,
      path: req.path,
      statusCode: res.statusCode,
      headers: res.headers,
      remoteAddress: res.connection.remoteAddress,
      remotePort: res.connection.remotePort,
    });

    request.res = res;

    if (request.pipe) {
      res.pipe(request.pipe);
    } else {
      res.on('data', function(chunk) {
        chunks.push(chunk);
        bodyLength += chunk.length;
      });
    }

    res.on('end', function() {
      if (done) return;
      done = true;

      if (abort) request.ctx.removeListener('cancel', abort);
      if (timeoutId) clearTimeout(timeoutId);

      // body content mime
      var mime;

      // decode body
      if (bodyLength) {
        res.body = Buffer.concat(chunks, bodyLength);

        // don't decode if user explicitly asks for buffer
        if (!opts.buffer) {
          mime = (res.headers['content-type'] || '').split(';')[0].trim();

          if (self._opts.decoders[mime]) {
            try {
              res.body = self._decode(mime, res.body);
            } catch (err) {
              request.err = err;
              return next();
            }
          }
        }
      }

      // any non-200 is consider an error
      if (Math.floor(res.statusCode / 100) !== 2) {
        var err = errors.Response();

        if (res.body && mime === 'text/plain' && res.body.length < 80) {
          err.message = res.body;
        }

        if (!err.message) {
          if (http.STATUS_CODES[res.statusCode]) {
            err.message = http.STATUS_CODES[res.statusCode].toLowerCase();
          } else {
            err.message = 'request failed: ' + res.statusCode;
          }
        }

        err.statusCode = res.statusCode;

        request.err = err;
      }

      next();
    });
  });

  if (utils.isReadableStream(request.body)) {
    request.body.pipe(req);
  } else {
    req.end(request.body);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.super_.prototype.__push"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>__push (request, name)](#apidoc.element.jenkins.Jenkins.super_.prototype.__push)
- description and source-code
```javascript
__push = function (request, name) {
  if (this._exts[name]) {
    request._stack.push.apply(request._stack, this._exts[name]);
  }

  if (request.opts && request.opts.exts && request.opts.exts[name]) {
    if (Array.isArray(request.opts.exts[name])) {
      request._stack.push.apply(request._stack, request.opts.exts[name]);
    } else {
      request._stack.push(request.opts.exts[name]);
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.super_.prototype._decode"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_decode (mime, value)](#apidoc.element.jenkins.Jenkins.super_.prototype._decode)
- description and source-code
```javascript
_decode = function (mime, value) {
  if (!this._opts.decoders[mime]) {
    throw errors.Codec('unknown decoder: ' + mime);
  }

  try {
    return this._opts.decoders[mime](value);
  } catch (err) {
    err.message = 'decode (' + mime + ') failed: ' + err.message;
    throw errors.Codec(err);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.super_.prototype._delete"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_delete (opts)](#apidoc.element.jenkins.Jenkins.super_.prototype._delete)
- description and source-code
```javascript
_delete = function (opts) {
  var args;

  if (typeof opts === 'string') {
    opts = { path: opts, method: reqMethod };

    args = Array.prototype.slice.call(arguments);
    args[0] = opts;

    return this._request.apply(this, args);
  } else if (!opts) {
    args = Array.prototype.slice.call(arguments);
    args[0] = {};

    return this._request.apply(this, args);
  }

  opts.method = reqMethod;

  return this._request.apply(this, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.super_.prototype._encode"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_encode (mime, value)](#apidoc.element.jenkins.Jenkins.super_.prototype._encode)
- description and source-code
```javascript
_encode = function (mime, value) {
  if (!this._opts.encoders[mime]) {
    throw errors.Codec('unknown encoder: ' + mime);
  }

  try {
    return this._opts.encoders[mime](value);
  } catch (err) {
    err.message = 'encode (' + mime + ') failed: ' + err.message;
    throw errors.Codec(err);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.super_.prototype._err"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_err (err, opts)](#apidoc.element.jenkins.Jenkins.super_.prototype._err)
- description and source-code
```javascript
_err = function (err, opts) {
  if (!err) return err;

  if (!(err instanceof Error)) err = new Error(err);

  if (opts && opts.name) {
    err.message = util.format('%s: %s', opts.name, err.message);
  }

  if (this._opts.name) {
    err.message = util.format('%s: %s', this._opts.name, err.message);
  }

  return err;
}
```
- example usage
```shell
...
  if (opts.parameters) {
    req.path += 'WithParameters';
    req.query = opts.parameters;
  }

  if (opts.token) req.query.token = opts.token;
} catch (err) {
  return callback(this.jenkins._err(err, req));
}

return this.jenkins._post(
  req,
  middleware.notFound(opts.name),
  middleware.queueLocation,
  callback
...
```

#### <a name="apidoc.element.jenkins.Jenkins.super_.prototype._ext"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_ext (eventName, callback)](#apidoc.element.jenkins.Jenkins.super_.prototype._ext)
- description and source-code
```javascript
_ext = function (eventName, callback) {
  if (!eventName || typeof eventName !== 'string') {
    throw this._err(errors.Validation('extension eventName required'));
  }

  if (typeof callback !== 'function') {
    throw this._err(errors.Validation('extension callback required'));
  }

  if (!this._exts[eventName]) this._exts[eventName] = [];

  this._exts[eventName].push(callback);
}
```
- example usage
```shell
...
  this._crumbIssuer = opts.crumbIssuer;
} else if (opts.crumbIssuer === true) {
  this._crumbIssuer = utils.crumbIssuer;
}

papi.Client.call(this, opts);

this._ext('onCreate', this._onCreate);
this._ext('onResponse', this._onResponse);

this.build = new Jenkins.Build(this);
this.crumbIssuer = new Jenkins.CrumbIssuer(this);
this.job = new Jenkins.Job(this);
this.node = new Jenkins.Node(this);
this.queue = new Jenkins.Queue(this);
...
```

#### <a name="apidoc.element.jenkins.Jenkins.super_.prototype._get"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_get (opts)](#apidoc.element.jenkins.Jenkins.super_.prototype._get)
- description and source-code
```javascript
_get = function (opts) {
  var args;

  if (typeof opts === 'string') {
    opts = { path: opts, method: reqMethod };

    args = Array.prototype.slice.call(arguments);
    args[0] = opts;

    return this._request.apply(this, args);
  } else if (!opts) {
    args = Array.prototype.slice.call(arguments);
    args[0] = {};

    return this._request.apply(this, args);
  }

  opts.method = reqMethod;

  return this._request.apply(this, arguments);
}
```
- example usage
```shell
...
  var req = {
    name: 'crumbIssuer.get',
    path: '/crumbIssuer/api/json',
  };

  utils.options(req, opts);

  return this.jenkins._get(req, middleware.body, callback);
};

/**
 * Module exports.
 */

exports.CrumbIssuer = CrumbIssuer;
...
```

#### <a name="apidoc.element.jenkins.Jenkins.super_.prototype._head"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_head (opts)](#apidoc.element.jenkins.Jenkins.super_.prototype._head)
- description and source-code
```javascript
_head = function (opts) {
  var args;

  if (typeof opts === 'string') {
    opts = { path: opts, method: reqMethod };

    args = Array.prototype.slice.call(arguments);
    args[0] = opts;

    return this._request.apply(this, args);
  } else if (!opts) {
    args = Array.prototype.slice.call(arguments);
    args[0] = {};

    return this._request.apply(this, args);
  }

  opts.method = reqMethod;

  return this._request.apply(this, arguments);
}
```
- example usage
```shell
...

    req.path = '{folder}/api/json';
    req.params = { folder: folder.path() };
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._head(req, middleware.exists, callback);
};

/**
 * Job details
 */

Job.prototype.get = function(opts, callback) {
...
```

#### <a name="apidoc.element.jenkins.Jenkins.super_.prototype._log"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_log (tags, data)](#apidoc.element.jenkins.Jenkins.super_.prototype._log)
- description and source-code
```javascript
_log = function (tags, data) {
  return this.emit('log', tags, data);
}
```
- example usage
```shell
...

CrumbIssuer.prototype.get = function(opts, callback) {
if (typeof opts === 'function') {
  callback = opts;
  opts = {};
}

this.jenkins._log(['debug', 'crumbIssuer', 'get'], opts);

var req = {
  name: 'crumbIssuer.get',
  path: '/crumbIssuer/api/json',
};

utils.options(req, opts);
...
```

#### <a name="apidoc.element.jenkins.Jenkins.super_.prototype._options"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_options (opts)](#apidoc.element.jenkins.Jenkins.super_.prototype._options)
- description and source-code
```javascript
_options = function (opts) {
  var args;

  if (typeof opts === 'string') {
    opts = { path: opts, method: reqMethod };

    args = Array.prototype.slice.call(arguments);
    args[0] = opts;

    return this._request.apply(this, args);
  } else if (!opts) {
    args = Array.prototype.slice.call(arguments);
    args[0] = {};

    return this._request.apply(this, args);
  }

  opts.method = reqMethod;

  return this._request.apply(this, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.super_.prototype._patch"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_patch (opts)](#apidoc.element.jenkins.Jenkins.super_.prototype._patch)
- description and source-code
```javascript
_patch = function (opts) {
  var args;

  if (typeof opts === 'string') {
    opts = { path: opts, method: reqMethod };

    args = Array.prototype.slice.call(arguments);
    args[0] = opts;

    return this._request.apply(this, args);
  } else if (!opts) {
    args = Array.prototype.slice.call(arguments);
    args[0] = {};

    return this._request.apply(this, args);
  }

  opts.method = reqMethod;

  return this._request.apply(this, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.super_.prototype._plugin"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_plugin (plugin, options)](#apidoc.element.jenkins.Jenkins.super_.prototype._plugin)
- description and source-code
```javascript
_plugin = function (plugin, options) {
  if (!plugin) {
    throw this._err(errors.Validation('plugin required'));
  }

  if (typeof plugin.register !== 'function') {
    throw this._err(errors.Validation('plugin must have register function'));
  }

  var attributes = plugin.register.attributes;

  if (!attributes) {
    throw this._err(errors.Validation('plugin attributes required'));
  }

  if (!attributes.name) {
    throw this._err(errors.Validation('plugin attributes name required'));
  }

  if (!attributes.version) {
    throw this._err(errors.Validation('plugin attributes version required'));
  }

  return plugin.register(this, options || {});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.super_.prototype._post"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_post (opts)](#apidoc.element.jenkins.Jenkins.super_.prototype._post)
- description and source-code
```javascript
_post = function (opts) {
  var args;

  if (typeof opts === 'string') {
    opts = { path: opts, method: reqMethod };

    args = Array.prototype.slice.call(arguments);
    args[0] = opts;

    return this._request.apply(this, args);
  } else if (!opts) {
    args = Array.prototype.slice.call(arguments);
    args[0] = {};

    return this._request.apply(this, args);
  }

  opts.method = reqMethod;

  return this._request.apply(this, arguments);
}
```
- example usage
```shell
...
    }

    if (opts.token) req.query.token = opts.token;
  } catch (err) {
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._post(
    req,
    middleware.notFound(opts.name),
    middleware.queueLocation,
    callback
  );
};
...
```

#### <a name="apidoc.element.jenkins.Jenkins.super_.prototype._put"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_put (opts)](#apidoc.element.jenkins.Jenkins.super_.prototype._put)
- description and source-code
```javascript
_put = function (opts) {
  var args;

  if (typeof opts === 'string') {
    opts = { path: opts, method: reqMethod };

    args = Array.prototype.slice.call(arguments);
    args[0] = opts;

    return this._request.apply(this, args);
  } else if (!opts) {
    args = Array.prototype.slice.call(arguments);
    args[0] = {};

    return this._request.apply(this, args);
  }

  opts.method = reqMethod;

  return this._request.apply(this, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.Jenkins.super_.prototype._request"></a>[function <span class="apidocSignatureSpan">jenkins.Jenkins.super_.prototype.</span>_request (opts)](#apidoc.element.jenkins.Jenkins.super_.prototype._request)
- description and source-code
```javascript
_request = function (opts) {
  var self = this;

  var request;

  if (this.__request) {
    request = this.__request;
    opts = request.opts;
    self = request._client;
  } else {
    request = {
      _args: Array.prototype.slice.call(arguments),
      _client: this,
      opts: opts,
      state: {},
    };

    if (!opts) opts = request.opts = {};

    if (request._args.length > 1) {
      request._callback = request._args[request._args.length - 1];
    } else {
      return self.emit('error', self._err(
        errors.Validation('callback required'), opts));
    }

    // if ctx is an event emitter we use it to abort requests when done is
    // emitted
    if (opts.ctx instanceof events.EventEmitter) {
      request.ctx = opts.ctx;
    }

    // combine global and request tags
    opts.tags = (opts.tags || []).concat(self._opts.tags);

    // inject request name into tags if not already defined
    if (opts.name && !~opts.tags.indexOf(opts.name)) {
      opts.tags.push(opts.name);
    }

    if (!opts.headers) opts.headers = {};
    if (!opts.params) opts.params = {};
    if (!opts.query) opts.query = {};

    // restart request
    request.retry = function() {
      if (request._retryable === false) {
        throw errors.Validation('request is not retryable');
      }

      self._log(['papi', 'request', 'retry'].concat(request.opts.tags));

      delete request.body;
      delete request.err;
      delete request.req;
      delete request.res;
      delete request.transport;

      self._request.call({ __request: request });
    };

    request._stack = [];

    self.__push(request, 'onCreate');

    request._stack.push(self.__create);

    self.__push(request, 'onRequest');

    request._stack.push(self.__execute);

    self.__push(request, 'onResponse');

    request._stack.push.apply(
      request._stack,
      request._args.slice(1, request._args.length - 1)
    );
  }

  var i = 0;
  function next(err) {
    if (err) return request._callback(self._err(err, opts));

    // middlware can call next(false, args...) to stop middleware
    if (err === false) {
      return request._callback.apply(null,
        Array.prototype.slice.call(arguments, 1));
    }

    var fn = request._stack[i++];
    if (fn) {
      fn.call(self, request, next);
    } else {
      request._callback.call(self, self._err(request.err, opts), request.res);
    }
  }

  next();
}
```
- example usage
```shell
...
} else {
  req.method = 'GET';
}
  } catch (err) {
return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._request(
req,
middleware.notFound('job ' + opts.name),
function(ctx, next) {
  if (ctx.err || opts.xml) return middleware.empty(ctx, next);

  next(false, null, ctx.res.body.toString('utf8'));
},
...
```



# <a name="apidoc.module.jenkins.crumb_issuer"></a>[module jenkins.crumb_issuer](#apidoc.module.jenkins.crumb_issuer)

#### <a name="apidoc.element.jenkins.crumb_issuer.CrumbIssuer"></a>[function <span class="apidocSignatureSpan">jenkins.crumb_issuer.</span>CrumbIssuer (jenkins)](#apidoc.element.jenkins.crumb_issuer.CrumbIssuer)
- description and source-code
```javascript
function CrumbIssuer(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
...

papi.Client.call(this, opts);

this._ext('onCreate', this._onCreate);
this._ext('onResponse', this._onResponse);

this.build = new Jenkins.Build(this);
this.crumbIssuer = new Jenkins.CrumbIssuer(this);
this.job = new Jenkins.Job(this);
this.node = new Jenkins.Node(this);
this.queue = new Jenkins.Queue(this);
this.view = new Jenkins.View(this);

try {
  if (opts.promisify) {
...
```



# <a name="apidoc.module.jenkins.jenkins"></a>[module jenkins.jenkins](#apidoc.module.jenkins.jenkins)

#### <a name="apidoc.element.jenkins.jenkins.Jenkins"></a>[function <span class="apidocSignatureSpan">jenkins.jenkins.</span>Jenkins (opts)](#apidoc.element.jenkins.jenkins.Jenkins)
- description and source-code
```javascript
function Jenkins(opts) {
  if (!(this instanceof Jenkins)) {
    return new Jenkins(opts);
  }

  if (typeof opts === 'string') {
    opts = { baseUrl: opts };
  } else {
    opts = opts || {};
  }

  if (!opts.baseUrl) {
    if (opts.url) {
      opts.baseUrl = opts.url;
      delete opts.url;
    } else {
      throw new Error('baseUrl required');
    }
  }

  if (!opts.headers) {
    opts.headers = {};
  }
  if (!opts.headers.referer) {
    opts.headers.referer = opts.baseUrl + '/';
  }

  if (opts.request) {
    throw new Error('request not longer supported');
  }

  opts.name = 'jenkins';

  if (typeof opts.crumbIssuer === 'function') {
    this._crumbIssuer = opts.crumbIssuer;
  } else if (opts.crumbIssuer === true) {
    this._crumbIssuer = utils.crumbIssuer;
  }

  papi.Client.call(this, opts);

  this._ext('onCreate', this._onCreate);
  this._ext('onResponse', this._onResponse);

  this.build = new Jenkins.Build(this);
  this.crumbIssuer = new Jenkins.CrumbIssuer(this);
  this.job = new Jenkins.Job(this);
  this.node = new Jenkins.Node(this);
  this.queue = new Jenkins.Queue(this);
  this.view = new Jenkins.View(this);

  try {
    if (opts.promisify) {
      if (typeof opts.promisify === 'function') {
        papi.tools.promisify(this, opts.promisify);
      } else {
        papi.tools.promisify(this);
      }
    }
  } catch (err) {
    err.message = 'promisify: ' + err.message;
    throw err;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jenkins.job"></a>[module jenkins.job](#apidoc.module.jenkins.job)

#### <a name="apidoc.element.jenkins.job.Job"></a>[function <span class="apidocSignatureSpan">jenkins.job.</span>Job (jenkins)](#apidoc.element.jenkins.job.Job)
- description and source-code
```javascript
function Job(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
...
papi.Client.call(this, opts);

this._ext('onCreate', this._onCreate);
this._ext('onResponse', this._onResponse);

this.build = new Jenkins.Build(this);
this.crumbIssuer = new Jenkins.CrumbIssuer(this);
this.job = new Jenkins.Job(this);
this.node = new Jenkins.Node(this);
this.queue = new Jenkins.Queue(this);
this.view = new Jenkins.View(this);

try {
  if (opts.promisify) {
    if (typeof opts.promisify === 'function') {
...
```



# <a name="apidoc.module.jenkins.middleware"></a>[module jenkins.middleware](#apidoc.module.jenkins.middleware)

#### <a name="apidoc.element.jenkins.middleware.body"></a>[function <span class="apidocSignatureSpan">jenkins.middleware.</span>body (ctx, next)](#apidoc.element.jenkins.middleware.body)
- description and source-code
```javascript
function body(ctx, next) {
  if (ctx.err) return next(ctx.err);

  next(false, null, ctx.res.body);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.middleware.bodyItem"></a>[function <span class="apidocSignatureSpan">jenkins.middleware.</span>bodyItem (key)](#apidoc.element.jenkins.middleware.bodyItem)
- description and source-code
```javascript
function bodyItem(key) {
  return function(ctx, next) {
    if (ctx.err) return next(ctx.err);

    next(false, null, ctx.res.body[key]);
  };
}
```
- example usage
```shell
...

     if (!ctx.res.body || !Array.isArray(ctx.res.body.jobs)) {
       ctx.err = new Error('returned bad data');
     }

     next();
   },
   middleware.bodyItem('jobs'),
   callback
 );
};

/**
* Module exports.
*/
...
```

#### <a name="apidoc.element.jenkins.middleware.empty"></a>[function <span class="apidocSignatureSpan">jenkins.middleware.</span>empty (ctx, next)](#apidoc.element.jenkins.middleware.empty)
- description and source-code
```javascript
function empty(ctx, next) {
  if (ctx.err) return next(ctx.err);

  next(false);
}
```
- example usage
```shell
...
    return callback(this.jenkins._err(err, req));
  }

  return this.jenkins._request(
    req,
    middleware.notFound('job ' + opts.name),
    function(ctx, next) {
      if (ctx.err || opts.xml) return middleware.empty(ctx, next);

      next(false, null, ctx.res.body.toString('utf8'));
    },
    callback
  );
};
...
```

#### <a name="apidoc.element.jenkins.middleware.exists"></a>[function <span class="apidocSignatureSpan">jenkins.middleware.</span>exists (ctx, next)](#apidoc.element.jenkins.middleware.exists)
- description and source-code
```javascript
function exists(ctx, next) {
  if (ctx.res && ctx.res.statusCode === 404) {
    return next(false, null, false);
  }

  if (ctx.err) return next(ctx.err);

  next(false, null, true);
}
```
- example usage
```shell
...
''' javascript
jenkins.job.enable('example', function(err) {
 if (err) throw err;
});
'''

<a name="job-exists"></a>
### jenkins.job.exists(options, callback)

Check job exists.

Options

* name (String): job name
...
```

#### <a name="apidoc.element.jenkins.middleware.notFound"></a>[function <span class="apidocSignatureSpan">jenkins.middleware.</span>notFound (value)](#apidoc.element.jenkins.middleware.notFound)
- description and source-code
```javascript
function notFound(value) {
  return function(ctx, next) {
    if (ctx.res && ctx.res.statusCode === 404) {
      var err = new Error(value + ' not found');
      err.notFound = true;

      return next(err);
    }

    next();
  };
}
```
- example usage
```shell
...
   if (opts.token) req.query.token = opts.token;
 } catch (err) {
   return callback(this.jenkins._err(err, req));
 }

 return this.jenkins._post(
   req,
   middleware.notFound(opts.name),
   middleware.queueLocation,
   callback
 );
};

/**
* Get or update config
...
```

#### <a name="apidoc.element.jenkins.middleware.queueLocation"></a>[function <span class="apidocSignatureSpan">jenkins.middleware.</span>queueLocation (ctx, next)](#apidoc.element.jenkins.middleware.queueLocation)
- description and source-code
```javascript
function queueLocation(ctx, next) {
  if (ctx.err) return next(ctx.err);

  try {
    // Get queue number from location header
    var parts = ctx.res.headers.location.split('/');

    return next(false, null, parseInt(parts[parts.length - 2], 10));
  } catch (err) {
    // ignore errors
  }

  next();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.middleware.require302"></a>[function <span class="apidocSignatureSpan">jenkins.middleware.</span>require302 (message)](#apidoc.element.jenkins.middleware.require302)
- description and source-code
```javascript
function require302(message) {
  return function(ctx, next) {
    if (ctx.res && ctx.res.statusCode === 302) {
      return next(false);
    } else if (ctx.res) {
      if (ctx.err) {
        if (!ctx.res.headers['x-error']) ctx.err.message = message;
      } else {
        ctx.err = new Error(message);
      }

      return next(ctx.err);
    }

    next();
  };
}
```
- example usage
```shell
...
   req.query.mode = 'copy';
 } catch (err) {
   return callback(this.jenkins._err(err, req));
 }

 return this.jenkins._post(
   req,
   middleware.require302('failed to create: ' + opts.name),
   middleware.empty,
   callback
 );
};

/**
* Create new job from xml
...
```



# <a name="apidoc.module.jenkins.node"></a>[module jenkins.node](#apidoc.module.jenkins.node)

#### <a name="apidoc.element.jenkins.node.Node"></a>[function <span class="apidocSignatureSpan">jenkins.node.</span>Node (jenkins)](#apidoc.element.jenkins.node.Node)
- description and source-code
```javascript
function Node(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
...

this._ext('onCreate', this._onCreate);
this._ext('onResponse', this._onResponse);

this.build = new Jenkins.Build(this);
this.crumbIssuer = new Jenkins.CrumbIssuer(this);
this.job = new Jenkins.Job(this);
this.node = new Jenkins.Node(this);
this.queue = new Jenkins.Queue(this);
this.view = new Jenkins.View(this);

try {
  if (opts.promisify) {
    if (typeof opts.promisify === 'function') {
      papi.tools.promisify(this, opts.promisify);
...
```



# <a name="apidoc.module.jenkins.queue"></a>[module jenkins.queue](#apidoc.module.jenkins.queue)

#### <a name="apidoc.element.jenkins.queue.Queue"></a>[function <span class="apidocSignatureSpan">jenkins.queue.</span>Queue (jenkins)](#apidoc.element.jenkins.queue.Queue)
- description and source-code
```javascript
function Queue(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
...
this._ext('onCreate', this._onCreate);
this._ext('onResponse', this._onResponse);

this.build = new Jenkins.Build(this);
this.crumbIssuer = new Jenkins.CrumbIssuer(this);
this.job = new Jenkins.Job(this);
this.node = new Jenkins.Node(this);
this.queue = new Jenkins.Queue(this);
this.view = new Jenkins.View(this);

try {
  if (opts.promisify) {
    if (typeof opts.promisify === 'function') {
      papi.tools.promisify(this, opts.promisify);
    } else {
...
```



# <a name="apidoc.module.jenkins.utils"></a>[module jenkins.utils](#apidoc.module.jenkins.utils)

#### <a name="apidoc.element.jenkins.utils.FolderPath"></a>[function <span class="apidocSignatureSpan">jenkins.utils.</span>FolderPath (value)](#apidoc.element.jenkins.utils.FolderPath)
- description and source-code
```javascript
function FolderPath(value) {
  if (!(this instanceof FolderPath)) {
    return new FolderPath(value);
  }
  if (Array.isArray(value)) {
    this.value = value;
  } else if (typeof value === 'string') {
    if (value.match('^https?:\/\/')) {
      this.value = parseName(value);
    } else {
      this.value = value.split('/').filter(Boolean);
    }
  } else {
    this.value = [];
  }
}
```
- example usage
```shell
...
  this.jenkins._log(['debug', 'job', 'build'], opts);

  var req = { name: 'job.build' };

  utils.options(req, opts);

  try {
var folder = utils.FolderPath(opts.name);

if (folder.isEmpty()) throw new Error('name required');

req.path = '{folder}/build';
req.params = { folder: folder.path() };

if (opts.parameters) {
...
```

#### <a name="apidoc.element.jenkins.utils.crumbIssuer"></a>[function <span class="apidocSignatureSpan">jenkins.utils.</span>crumbIssuer (jenkins, callback)](#apidoc.element.jenkins.utils.crumbIssuer)
- description and source-code
```javascript
function crumbIssuer(jenkins, callback) {
  jenkins.crumbIssuer.get(function(err, data) {
    if (err) return callback(err);
    if (!data || !data.crumbRequestField || !data.crumb) {
      return callback(new Error('Failed to get crumb'));
    }

    callback(null, {
      headerName: data.crumbRequestField,
      headerValue: data.crumb,
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jenkins.utils.options"></a>[function <span class="apidocSignatureSpan">jenkins.utils.</span>options (req, opts)](#apidoc.element.jenkins.utils.options)
- description and source-code
```javascript
function options(req, opts) {
  if (!req.query) req.query = {};

  if (typeof opts.depth === 'number') {
    req.query.depth = opts.depth;
  }

  if (typeof opts.tree === 'string') {
    req.query.tree = opts.tree;
  }

  return opts;
}
```
- example usage
```shell
...
 this.jenkins._log(['debug', 'crumbIssuer', 'get'], opts);

 var req = {
   name: 'crumbIssuer.get',
   path: '/crumbIssuer/api/json',
 };

 utils.options(req, opts);

 return this.jenkins._get(req, middleware.body, callback);
};

/**
* Module exports.
*/
...
```



# <a name="apidoc.module.jenkins.view"></a>[module jenkins.view](#apidoc.module.jenkins.view)

#### <a name="apidoc.element.jenkins.view.View"></a>[function <span class="apidocSignatureSpan">jenkins.view.</span>View (jenkins)](#apidoc.element.jenkins.view.View)
- description and source-code
```javascript
function View(jenkins) {
  this.jenkins = jenkins;
}
```
- example usage
```shell
...
this._ext('onResponse', this._onResponse);

this.build = new Jenkins.Build(this);
this.crumbIssuer = new Jenkins.CrumbIssuer(this);
this.job = new Jenkins.Job(this);
this.node = new Jenkins.Node(this);
this.queue = new Jenkins.Queue(this);
this.view = new Jenkins.View(this);

try {
  if (opts.promisify) {
    if (typeof opts.promisify === 'function') {
      papi.tools.promisify(this, opts.promisify);
    } else {
      papi.tools.promisify(this);
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

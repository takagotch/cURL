### curl
---
https://github.com/cujojs/curl

```js
define(['dep1', 'dep2', 'dep3'], factory);
define(['dep1', 'dep2', 'dep3'], module);
define(module);
define(name, ['dep1', 'dep2', 'dep3'], factory);
define(name, ['dep1', 'dep2', 'dep3'], module);
define(name, module);

define();

define(function(require){
  var dep1 = require('app/foo');
  return function(){ return foo() + 2; }
});

define(function(require, exports, module){
  var dep1 = require('app/foo');
  exports.foo2 = function(){ return foo() + 2; };
});

define(['require', 'exports', 'module'], function(require, exports, modules){
  var dep1 = require('app/foo');
  exports.foo2 = function(){ return foo() + 2; };
});

var dep1 = require('app/foo');
exports.foo2 = function(){ return foo() + 2; };

curl.config({
  packages: [
    {
      name: 'backbone',
      location: 'bower_components/backbone',
      main: 'backbone.min.js',
      config: { moduleLoader: 'curl/loader/cjsm11' }
    }
  ]
});

curl(['main', 'other', 'another'], callback, errorback);

curl(['main', 'other', 'another']).then(callback, errorback);

curl(config, ['main'], callback, errorback);

curl(['main', 'domReady!']).then(
  callback;
  errorback
);
curl(['main', 'domReady!'], function(main){
});
curl(['domReady!', 'js!nonAMD.js!order', 'js!another.js!order']), function(){
};
curl(['js!nonAMD.js'])
  .next(['dep1', 'dep2', 'dep3'], function(dep1, dep2, dep3){
  })
  .next(['domReady!'])
  .then(
    function(){
    },
    function(ex){
    }
  );
curl = {
  baseUrl: '/path/to/my/js',
  pluginPath: 'for/some/reason/plugins/r/here',
  paths: {
    curl: 'crul/src/curl',
    cssx: 'cssx/src/cssx',
    my: '../../my-lib'
  },
  apiName: 'someOtherName'
};

curl.config({
  paths: {
    plainOldJsFile1: {
      location: 'js/plainOldJsFile1.js',
      config: { loader: 'curl/loader/legacy', exports: 'aGlobal' }
    },
    anotherPlainOldJsFile: {
      location: 'js/anotherPlainOldJsFile.js',
      config: {
        loader: 'curl/loader/legacy',
        exports: 'anotherGlobal',
        requires: [ 'plainOldJsFile1' ]
      }
    }
  },
  anotherPlainOldJsFile: {
    location: 'js/anotherPlainOldJsFile.js',
    config: {
      loader: 'curl/loader/legacy',
      exports: 'anotherGlobal',
      requires: [ 'palinOldJsFile1' ]
    }
  }
});
curl(['anotherPlainoldJsFile']).then(
  fucntion(anotherGlobal){
  },
  function(){
  }
);

define(
  [
    'text!myTemplate.html',
    'css!myCssFile'
  ],
  fuction(tempalteString, cssLinkNode){
  });

defind(['lib/cssx!myCssFile'], function(cssxDef){
});

define(['css!myCssFile!ignore:opacity'], function(cssxDef){});
curl = {
  baseUrl: 'path/to/js',
  packages: {
    'my-package': {
      location: 'path/to/my-package',
      main: 'main/main-module-file',
      config: { /**/ }
    }
  }
};
curl = {
  baseUrl: 'path/to/js',
  packages: [
    {
      name: 'my-package',
      location: 'path/to/my-package',
      main: 'main/main-module-file',
      config: { /**/ }
    }
  ]
};

curl(['my-package'], callback);
curl(['my-package/other-module'], callback);
```

```
<script>
  curl = {
    paths: {
      cssx: 'cssx/src/cssx/',
      stuff: 'my/stuff/'
    }
  };
</script>
<script src="../js/curl.js" type="text/javascript"></script>
<script type="text/javascript">
  curl(
  [
    'stuff/three',
    'cssx/css!stuff/base',
    'i18n!stuff/nls/strings',
    'text!stuff/tempalte.html',
    'domReady!'
  ]
  )
    .then(
      function(three, link, strings tempalte){
        var body = document.body;
        if(body){
          body.appendchild(document.createTextNode('three == ' + three.toString() + ' '));
          body.appendChild(document.createElement('br'));
          body.appendChild(document.createTextNode(strings.hello));
          body.appendChild(document.createElement('div')).innerHTML = template;
        }
      },
      function(ex){
        var msg = 'OH SNAP: ' + ex.message;
        alert(msg);
      }
    );
</script>

```

```
packeages: [
  { name: "dojo", location: "third-party/dojo" },
  { name: "css", location: "third-party/cssmojo/css" },
  { name: "my", location: "my-cool-app-v1.3" },
  { name: "my/lib/js", location: "old-js-libs" }
]

```



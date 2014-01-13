# bower organize sources

Get Bower dependency source files, in order, listed by file extension.

``` js
var organizeSources = require('organize-bower-sources');
// bowerJSON is output bower list --json
var bowerSources = organizeSources( bowerJSON );
// returns:
{
  '.js': [ 'js-dep1/js-dep1.js', 'js-dep2/js-dep2.js', ... ],
  '.css': [ 'css-dep1/css-dep1.css', 'css-dep2/css-dep2.css', ... ],
}
```

See it [in use in grunt-fizzy-docs](https://github.com/metafizzy/grunt-fizzy-docs/blob/master/tasks/int-bower.js)

To limit the sources to just files for one package, pass in second argument with the package name.

``` js
var masonrySources = organizeSources( bowerJSON, 'masonry' );
```

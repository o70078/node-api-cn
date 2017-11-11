<!-- YAML
added: v1.0.0
-->

使用 `v8.setFlagsFromString()` 方法可以以编程方式设置v8命令行参数. 这个方法需要谨慎使用,更改参数有可能导致一些不可预知的情况!

The V8 options available for a version of Node.js may be determined by running
`node --v8-options`.  An unofficial, community-maintained list of options
and their effects is available [here][].

Usage:

```js
// Print GC events to stdout for one minute.
const v8 = require('v8');
v8.setFlagsFromString('--trace_gc');
setTimeout(function() { v8.setFlagsFromString('--notrace_gc'); }, 60e3);
```


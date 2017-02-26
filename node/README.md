# node相关知识点
* 1.[nodejs2016十大文章](http://www.jcodecraeer.com/a/javascript/2017/0113/7008.html)

# node 的模块机制
```
function require() {
  var module = {exports: {}}
  ((module, exports) => {
    // Your module code here. In this example, define a function.
    function some_fun (){}
    exports = some_fun
    // At this point, exports is no longer a shortcut to module.exports, and
    // this module will still export an empty default object.
    module.exports = some_func
    // At this point, the module will now export some_func, instead of the
    // default object.
  })(module, module.exports)

  return module.exports 
}
```
# 如果 a.js require 了 b.js, 那么在 b 中定义全局变量 t = 111 能否在 a 中直接打印出来?
[nodejs模块问题](https://github.com/ElemeFE/node-interview/blob/master/sections/module.md#q-loop)

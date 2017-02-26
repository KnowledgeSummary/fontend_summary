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

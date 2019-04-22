# 模块化

commonJS： 服务器端
AMD/CMD/UMD： ADM 浏览器端
ES6 module


命名空间
没有模块化时： 库名.类别名.方法名


## commonJS
一个文件为一块模块，通过module.esports 暴露模块接口
通过require引入模块
同步执行（本地加载）
```js
var req = require('./request')
const app = {
    //
}

export = module.exports = app
```

### AMD Async Module Definition
使用define定义模块，使用require加载
RequireJS是基于AMD的一个库
依赖前置，提前执行
```js
define(
    // 模块名
    "alpha",
    // 依赖
    ["require", "exports", "beta"],
    // 模块输出
    function(require, exports, beta) {
        exports.verb = function() {
            return beat.verb()
            // or
            return require ("beta").verb()
        }
    }
)

//
define(
    ["a", "b", "c", "d"],
    function(a, b, c, d) {
        // 等于在最前面申明并初始化了要用到的所有模块
        if(false) {
            // 即便没用到某个模块b，但b还是提前执行力
            b.foo()
        }
    }
)
```

### CMD Common Module Definition
一个文件一个模块
使用define定义一个模块
通过require加载一个模块
SeaJS
尽可能懒执行

```js
// 所有模块通过define定义
define(function(require, exports, module) {
    // 通过require引入依赖
    var $ = require("jquery")
    var Spining = require('./spining')

    // 通过exports 提供接口
    exports.doSomething = ...
    // 或者通过module.exports提高整个接口
    module.exports = 。。。
})
```

### UMD 通用模块定义
是否支持ADM
是否支持CMD
否则定义全局变量


### ES Module
一个文件一个模块
exports/import
```js
import Vue from 'vue'
import { named!, named2 } from 'src/mylib'

import { named1 as myNamede1, named2 } from 'src/mylib'

import * as mylib from 'src/mylib'

import 'src/lib'

```
```js
export var myVar1 = ''
export function () {

}

export class Myclass {}

export default function {

}
export default 123

export * from 'src/others'
```


### webpack支持
AMD(RequireJS)/ES module/CommonJS
推荐ES Module




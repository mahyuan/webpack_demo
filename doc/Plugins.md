# Plugins

- 参与整个打包过程
- 打包优化和压缩
- 配置编译时的变量
```js
const webpack = require('webpack');

module.exports = {
    plugins: [
        new webpack.optimize.UglifyJsPlugin()
    ]
}

```
## 常用的
webpack4 之后有很多插件功能集成在了webpack中


## 名词
Chunk 代码块
Bundle 一束，一捆
Module 模块
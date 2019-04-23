# Output

打包成的文件（bundle）
一个或多个
自定义规则
自定义CDN

```js
// 单输出
nmodule.exports = {
    entry: 'index.js',
    ounput: {
        filename: 'index.min.js'
    }
}

// 多输出
module.exports = {
    entry: {
        index: 'index.js',
        vender: 'verder.js'
    },
    output: {
        // 自定义规则, name是entry中的key
        filename: '[name].min.[hash:5].js'
    }
}

```

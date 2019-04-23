# Entry

代码的入口
单一入口


```js
module.exports = {
    entry: 'src/index.js'
}
```
多入口
```js
// 数组形式
module.exports = {
    entry: ['src/index.js', 'vender.js']
}
// 多选形式, 每个入口有key，便于拓展
module.exports = {
    entry: {
        index: ['index.js', 'app.js'],
        verder: 'verder.js'
    }
}
```

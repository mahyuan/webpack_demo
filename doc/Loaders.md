# Loaders

处理文件
转化为js可以处理的模块

```js
module.exports = {
    module: {
        rules: [
            {
                test: /\.css$/,
                use: 'css-loader'
            }
        ]
    }
}

```

## 常用的loaders:
- 编译相关
babel-loader, ts-loader
- 样式相关
style-loader, css-loader, less-loader, postcss-loader
- 文件相关
file-loader, url-loader



# Webpack


## 基础介绍


`webpack`、`webpack-cli`


默认只对js文件打包


### webpack
```yaml
webpack:
    serve: # 启动开发服务器

webpack-cli:

```


#### webpack.config.js
```yaml
:
    entry: # 入口文件（默认index.js）
    devServer: # 开发服务器
        open:
        port:
        static:
    mode: # 开发模式
        development:
    module:
        rules:
            test: # 文件匹配
            exclude:
            use: # loader 默认 从右往左
                loader:
                options:
                ---
                babel-loader:
                    presets:
                        @babel-preset-env:
                css-loader:
                less-loader:
                style-loader:
            type:
                asset:
                    resource:
            generator:
                filename:
                    name:
                    hash:
                    ext:
    output: # 输出文件（默认dist/main.js）
        path:
    plugins:
        HtmlWebpackPlugin:
            template: # html模板
```



## 核心内容


### Loader

#### css-loader

css加载器

#### style-loader

将css插入到DOM中


#### less-loader

将less编译成css文件



#### babel-loader

js语法兼容转换


### Plugin

#### HtmlWebpackPlugin

生成HTML文件




### Dev Server



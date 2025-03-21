# Webpack


## 基础介绍


默认只对js文件打包
- `webpack`
- `webpack-cli`
- `webpack-dev-server`




### webpack
```yaml
webpack:
    serve: # 启动开发服务器
        --mode:

webpack-cli:

```


#### webpack.config.js
```yaml
webpack.config.js:
    entry: # 入口文件（默认index.js）
    devServer: # 开发服务器
        compress: # 压缩
        contentBase: # 静态内容目录
        open:
        port:
        static:
    mode: # 开发模式
        development:
    module: # 模块解析（loader）
        rules: # 模块匹配规则
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
        filename: # 输出文件名
        path:
    plugins: # 插件
        HtmlWebpackPlugin:
            template: # html模板
```



## 核心内容


### Loader
```yaml
this:
    loader:
    module:
    resource:
    resourcePath:
    resourceQuery:
    query:
    async():
    cacheable():
    emitError():
    emitWarning():
```

#### Custom Loader
```jsx
module.exports = function (source) {
  // `source` 是加载的文件内容（原始内容）
  // 这里我们将文件内容转换成大写
  return source.toUpperCase();
};
```

自定义Loader
主要用于文件的转换和处理，使得Webpack能够理解非JavaScript文件并将其处理成可以作为模块使用的格式



#### css-loader

css加载器

#### style-loader

将css插入到DOM中


#### less-loader

将less编译成css文件



#### babel-loader

js语法兼容转换


### Plugin
```yaml
compiler: # webpack实例
    cache: # 这个属性提供了对缓存的访问。缓存用于提高构建性能
    compilation:
    context: # 返回 Webpack 的当前上下文（工作目录）
    entryPoints:
    environment:
    hooks: # 生命周期
        afterCompile: # 在模块编译完成后触发
        compilation:
        done: # Webpack 完成构建时触发
        emit: # 在 Webpack 打包完成之后生成输出文件时触发
            tapAsync():
        failed: 
        invalid:
        normalModuleFactory: # 在 Webpack 创建新的模块时触发
        run: # 当 Webpack 开始编译时触发
        watchRun: # 在 Webpack 检测到文件变化并开始编译时触发
    inputFileSystem: # 通过此对象访问文件系统并读取文件
    modifiedFiles: # 这个属性返回一个包含修改过的文件的集合
    options: # Webpack 配置对象中的所有配置信息
    outputFileSystem:
    outputOptions:
    watchFileSystem:
    watchMode:
    getCache():
    getInfrastructureLogger():
    run():
    watch():
```

#### Custom Plugin
```js
class MyCustomPlugin {
  constructor(options) {
    // 插件的构造函数，可以接受配置项
    this.options = options;
  }

  apply(compiler) {
    // 这个方法会在 Webpack 编译时被调用
    compiler.hooks.emit.tapAsync('MyCustomPlugin', (compilation, callback) => {
      console.log('自定义插件运行中...');
      // 在这里可以修改编译结果，做任何自定义操作

      // 假设我们想在每次构建后输出一条信息：
      console.log('构建完成，输出文件：', compilation.assets);

      // 最后必须调用 callback 来告知 Webpack 完成此钩子的执行
      callback();
    });
  }
}

module.exports = MyCustomPlugin;
```
自定义Plugin、实现apply方法
Plugin在Webpack的生命周期中执行特定的操作，可以访问 Webpack的编译上下文（compiler），并在不同的阶段进行修改和处理



#### HtmlWebpackPlugin

生成HTML文件




### Dev Server



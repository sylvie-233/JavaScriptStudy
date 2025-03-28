# Webpack

`Webpack 5教程：P12`

## 基础介绍


核心概念：
- Entry入口
- Output出口
- Loader加载器
- Plugin插件
- Mode模式
- Module模块
- Dependency Graph依赖图


默认只对js文件打包
- `webpack`
- `webpack-cli`
- `webpack-dev-server`




### webpack
```yaml
webpack:
    -o:
    --config:
    --mode:
    --output-path:
    serve: # 启动开发服务器
```


#### webpack.config.js
```yaml
webpack.config.js:
    entry: # 入口文件（默认src/index.js）
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
        HtmlWebpackPlugin: # 生成HTML文件，并在HTML中加载所有打包资源，可设置Context上下文变量，在模板中传递，ejs语法，htmlWebpackPlugin.options.xxx 
            filename:
            minify:
            template: # html模板
            title:
        MiniCssExtractPlugin: # 抽离css到单独的文件
            filename: # [name]、
            loader:
        StyleLintPlugin: # CSS代码格式校验
            files:
```



## 核心内容
```yaml

```

### Loader
```yaml
Loader:
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

处理非js的加载
loader执行从右往左






#### custom loader
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

css加载器，css转换为js


#### style-loader

将css插入到DOM中（`<style>`）


#### less-loader

将less编译成css文件


#### postcss-loader

css转换，添加前缀
依赖autoprefixer插件、postcss.config.js配置



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

#### custom plugin
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



#### html-webpack-plugin

生成HTML文件，并在HTML中加载所有打包资源
内嵌ejs模板，支持模板变量


#### mini-css-extract-plugin

抽离css到单独的文件


#### optimize-css-assets-webpack-plugin


CSS压缩



#### stylelint-webpack-plugin

css代码格式校验



### Dev Server





### Mode

模式，区分开发环境
- development
- production
- none




### Module

一切皆模块



### Dependency Graph

依赖图


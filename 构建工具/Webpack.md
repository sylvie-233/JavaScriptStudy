# Webpack

``

## 基础介绍


核心概念：
- Entry入口
- Output出口
- Loader加载器
- Plugin插件
- Mode模式
- Module模块
- Dependency Graph依赖图


默认只对js文件打包，默认最终也是生成js代码
- `webpack`
- `webpack-cli`
- `webpack-dev-server`





### webpack
```yaml
webpack:
    -o:
    --config: # 配置文件
    --env: # 开发环境profile
    --mode:
    --output-path:
    serve: # 启动开发服务器
```


#### webpack.config.js
```yaml
webpack.config.js:
    entry: # 入口文件（默认src/index.js），支持多入口文件
    externals: # 指定排除打包
    devServer: # 开发服务器
        compress: # 压缩gzip
        contentBase: # 静态内容目录，output
        liveReload: # 热更新
        open:
        port: # 端口
        proxy: # 代理
            pathRewrite:
            target:
        static:
        target:
    devtool: # source-map映射模式
        source-map:
    mode: # 开发模式
        development:
    module: # 模块解析（loader）
        rules: # 模块匹配规则
            exclude: # 目录排除
            generator: # 内置asset资源模块文件生成
                filename: 
            parser: # 内置asset资源模块解析规则
            test: # 文件匹配
            type: # 使用内置asset资源模块处理
                asset:
            use: # loader 默认 从右往左
                loader:
                options: # loader配置
                ---
                babel-loader:
                    cacheDirectory:
                    presets:
                        @babel-preset-env:
                css-loader:
                file-loader:
                    name:
                html-loader:
                    esModule:
                less-loader:
                style-loader:
                url-loader:
                    esModule:
                    limit:
                    name:
                MiniCssExtractPlugin.loader:
                    publicPath:
            type:
                asset:
                    resource:
            generator:
                filename:
                    name:
                    hash:
                    ext:
    optimization: # 优化策略
        minimize:
        minimizer: # 压缩器
        sideEffects: # 指定哪些模块有副作用，不删除
        splitChunks:
            chunks:
                all:
        usedExports: # 标记未使用的代码
    output: # 输出文件（默认dist/main.js）
        filename: # 输出文件名
        path:
    plugins: # 插件
        CleanWebpackPlugin: # 生成文件清理
        CopyWebpackPlugin: # 文件直接拷贝输出目录
            patterns:
                from:
                to:
        EslintPlugin: # js代码格式
            fix:
        HtmlWebpackPlugin: # 生成HTML文件，并在HTML中加载所有打包资源，可设置Context上下文变量，在模板中传递，ejs语法，htmlWebpackPlugin.options.xxx 
            chunks: # 不同的页面加载各自的bundle js文件，指定页面需要的chunk
            filename:
            minify:
            template: # html模板
            title:
        MiniCssExtractPlugin: # 抽离css到单独的文件
            filename: # [name]、
            loader:
        StyleLintPlugin: # CSS代码格式校验
            files:
    resolve: # 模块解析规则
        alias: # 路径别名
        extensions: # 模块后缀名
        modules: # 模块默认加载路径
```

支持函数式配置，接收env、argv
webpack-merge支持多环境profile配置合并



## 核心内容
```yaml
webpack:
    DefinePlugin: # 内置定义全局变量插件
```

### Loader
```yaml
loader:
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
loader-utils:
    getOptions(): # 读取loader配置
```

处理非js的加载，模块解析
loader执行从右往左，内部管道
loader本质上就是一个转换函数






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


#### babel-loader

js语法兼容转换
- preset-env: 转译基础语法
- polyfill: 转译所有js新语法

#### css-loader

css加载器，css转换为js


#### file-loader

图片复制到输出目录
支持字体打包


#### html-loader

html导入为字符串

#### less-loader

将less编译成css文件


#### postcss-loader

css转换，添加前缀
依赖autoprefixer插件、postcss.config.js配置

#### style-loader

将css插入到DOM中（`<style>`）

#### url-loader

file-loader升级版



### Assets

内置资源模块



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
                compilation:
                    assets: # 所有模块资源
                        size(): # 模块资源内容大小
                        source(): # 模块资源内容
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


#### clean-webpack-plugin

生成文件清理


#### copy-webpack-plugin

文件直接拷贝到输出目录


#### eslint-webpack-plugin

js代码格式检查




#### html-webpack-plugin

生成HTML文件，并在HTML中加载所有打包资源
内嵌ejs模板，支持模板变量
一个plugin实例生成一个html文件


#### mini-css-extract-plugin

抽离css到单独的文件


#### optimize-css-assets-webpack-plugin


CSS压缩



#### stylelint-webpack-plugin

css代码格式校验



#### terser-webpack-plugin

删除未使用的代码


### Dev Server





### Mode

模式，区分开发环境
- development
- production
- none


### Dependency Graph

依赖图


### Module

一切皆模块


代码分离解决方案：
- 多入口打包
- 提取公用模块
- 动态导入


#### Dynamic Import
```js
import(/* webpackChunkName: 'xxx', webpackPrefetch: false */ "/xxx").then()
```
动态导入，支持代码分隔
webpackChunkName定义chunk名称，webpackPrefetch预加载chunk


#### Source Map


`.map`源代码与构建代码映射
浏览器原生支持 Source Maps
```js
// 最后一行map文件标记
//# sourceMappingURL=app.js.map
```


#### Tree Shaking

树摇，移除未使用代码






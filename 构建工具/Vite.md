# Vite


`Vite世界指南：P1`
`Vite官方中文文档：https://vitejs.cn/vite3-cn/`
``



## 基础介绍


前端项目开发、构建工具
- 开发服务器
- 依赖预构建
- 模块热更新
- 构建打包

Rollup封装、esbuild构建、支持插件系统、nodejs服务ssr渲染
开发环境使用esbuild、生成环境使用Rollup




### vite
```yaml
vite:
    --config: # 配置文件
    --model: # 指定开发模式
    build: # 打包
    preview: # 启动开发服务器
```

#### vite.config.js
```yaml
vite.config.js:
    assetsInclude:
    base:
    build: # 配置构建行为
        assetsDir: # 静态资源目录
        cssCodeSplit:
        manifest: # 构建生成资源清单文件（html，js、css）
        minify:
        outDir: # 输出目录
        rollupOptions: # rollup配置
        sourcemap:
        target:
    cacheDir:
    clearScreen:
    css: # 对CSS的行为进行配置
        module: # module模块化配置
        preprocessorOptions: # 预处理器配置
        devSourcemap:  #css的sourceMap文件索引
        postcss: # PostCss配置相关
    define:
    envDir:
    esbuild: # EsBuild工具配置
        jsxInject:
    json:
        namedExports:
    logLevel:
    mode:
    optimizeDeps: # 控制依赖预构建的行为
        entries:
        exclude:
        include:
    plugins: # 插件配置
    publicDir:
    resolve: # 文件导入解析
        alias: # 路径别名
        conditions:
        dedupe:
        extensions:
        mainFields:
    root:
    server: # 开发服务器配置
        cors:
        hmr:
        host:
        https:
        open:
        port:
        proxy:
        watch:
    ssr:
        external:
```

#### tsconfig.js

typescript配置

#### postcss.config.js
```yaml
postcss.config.js:
    plugins:
```

原生支持postcss样式转换


#### .eslintrc.js
```yaml
.eslintrc.js:
    extend: # 配置继承
    globals:
        postMessage:
    rules: # 代码规范规则
```

代码格式检测


#### .prettier
```yaml
.prettier:
    semi: # 分号 
```

代码自动格式化工具



## 核心内容
```yaml
import.meta:
    hot: # 热更新
        data:
            cache:
        accept():
            newModule:
        decline():
        dispose():
        invalidate():
    glob(): # 多文件匹配
    globEager():

vite:
    Plugin:
        enforce:
        name:
        buildStart():
        config():
        configResolved():
        configureServer():
        handleHotUpdate():
        load():
        resolveId():
        transformIndexHtml():
    createServer():
        server:
            middlewareMode:
    defineConfig():
    
@vitejs:
    plugin-react-refresh:
    plugin-vue:
        vue():
    plugin-vue-jsx:
        vueJsx():

vite-plugin-vue2:
    createVuePlugin():
```




### 插件
```yaml
Plugin Hooks:
    config(): # 修改 Vite 配置
    transform(): # 转换文件内容
    load(): # 自定义资源加载
    handleHotUpdate(): # 热更新处理
    configureServer(): # 配置开发服务器等,扩展 Vite 的开发服务器，加入额外的中间件
```

生命周期：
1. pre:
2. normal:
3. post:









## 工作原理

### 开发服务器

依赖预构建：
- 解析node_modules依赖，使用esbuild进行预构建
- 将CommonJS/UMD依赖转换为ESM格式，加速import加载

基于connect中间件框架创建web服务器
- 浏览器基于ES Module，每次import会发起一次请求
- 拦截import请求、解析TS、Vue、React等文件

模块热替换：监听文件变动（fs.watch）、仅重新编译变更的模块，并通知浏览器更新

Vite的插件系统基于Rollup插件 API，但做了一些扩展
依赖中间件，请求来的时候依次调用Plugin插件的各个Hook钩子


#### resolveConfig

配置文件解析、收集所有插件



#### PluginContainer 

插件容器、持有所有Plugin
遍历所有的Plugin，调用其Hook进行解析



#### HMR

基于websocket通知浏览器哪些模块需要重新请求
- update
- css-update
- full-reloa
- connected
- custom


#### Dependency Graph

依赖图、高效地进行增量构建和热更新
- 模块解析和加载：当一个模块被导入时，Vite会根据依赖图确定如何加载该模块的依赖。
- 增量构建：Vite通过依赖图跟踪每个模块的变化，仅重新构建发生变化的部分，而不是重新构建整个项目。
- 热更新（HMR）：依赖图有助于快速准确地进行模块热替换，当某个模块发生变化时，Vite 可以根据依赖图判断需要替换哪些模块，避免不必要的更新。

每个模块就是一个节点、import产生边



### 构建打包

- 源代码优化与转换：在构建过程中，Vite会对所有源代码进行处理和优化，这包括使用esbuild将 TypeScript、JSX、JS等转换为浏览器能够理解的JavaScript代码
- 资源处理与打包：Vite会将所有静态资源（如图片、CSS、JS）打包并生成对应的输出文件
- 代码拆分与压缩：在最终打包阶段，Vite会使用rollup对代码进行拆分和压缩，生成最终的产物

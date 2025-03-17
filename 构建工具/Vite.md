# Vite


`Vite世界指南：P1`
`Vite官方中文文档：https://vitejs.cn/vite3-cn/`
`Vite.js快速入门到精通：P48`



## 基础介绍


前端项目开发、构建工具

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
    optimizeDeps: # 包依赖编译优化
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

生命周期：
1. pre:
2. normal:
3. post:
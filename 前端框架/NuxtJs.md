# NuxtJs

>
> `#TODO Nuxt官方文档：https://nuxt.com/docs/getting-started/routing`
>

## 基础介绍

Vue.js SSR

基于文件的路由




### 项目结构
```yaml
NuxtJs:
    /.nuxt:
        /schema:
        /types:
        app.config.mjs:
        components.d.ts:
        imports.d.ts:
        nuxt.d.ts:
        tsconfig.json:
        tsconfig.server.json:
    /.output:
    /assets: # 资源文件
    /components: # 自定义组件
    /layouts: # 页面布局
        default.vue: 
    /pages: # 页面路由
        index.vue:
    /public: # 静态访问资源
        favicon.ico:
        robots.txt:
    /server:
        /plugins:
        tsconfig.json:
    app.vue:
    nuxt.config.ts:
    package.json:
    tsconfig.json:
```

#### nuxt.config.ts
```yaml
NuxtConfig:
    $production: # 生产环境配置
    app:
        head:
            link:
    css:
    devtools:
    hooks:
    nitro:
    postcss:
    runtimeConfig: # 服务端可读属性
        public: # 客户端可读属性
    vite:
    vue:
    webpack:
```

#### app.config.ts
```yaml

```

### nuxt
```yaml
nuxt:
    build:
    dev:
    generate:
    prepare:
    preview:
```

#### nuxi
```yaml
nuxi:
    init: # 初始化项目
```




## 核心内容
```yaml
nuxt:
    NuxtPage: # pages页面显示
    useAppConfig():
    useHead():
    useRuntimeConfig(): # 读取配置属性
```
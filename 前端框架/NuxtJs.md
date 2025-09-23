# NuxtJs

>
> ``
>

## 基础介绍

Vue.js SSR

- 服务端渲染（SSR）：优化 SEO，提升首屏速度
- 静态生成（SSG）：生成静态 HTML，部署方便
- 文件路由：pages 目录自动生成路由




### 项目结构
```yaml
NuxtJs:
    /.nuxt: # 构建目录
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
    /composables: # 可复用的逻辑函数
    /layouts: # 页面布局
        default.vue: 
    /middleware: # 中间件
    /pages: # 页面路由
        index.vue:
    /plugins: # 插件
    /public: # 静态访问资源
        favicon.ico:
        robots.txt:
    /server: # 服务端 API
        /plugins:
        tsconfig.json:
    app.vue:
    nuxt.config.ts: # 配置文件
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

nuxt项目配置文件



### nuxt
```yaml
nuxt:
    build:
    dev:
    generate:
    prepare:
    preview:
```

nuxt构建命令



#### nuxi
```yaml
nuxi:
    init: # 初始化项目
```

nuxt项目脚手架命令




## 核心内容
```yaml
vue:
vue-router:
pinia:
    defineStore():
nuxt:
    config:
        defineNuxtConfig():
            css:
            modules:
    NuxtLayout: # 渲染布局
    NuxtLink: # 路由跳转
    NuxtPage: # 渲染页面内容（路由视图）
    $fetch(): # 类似 axios/fetch 的封装
    definePageMeta(): # 定义页面元信息（layout、auth等）
    defineNuxtPlugin(): # 
    defineNuxtRouteMiddleware(): # 定义路由中间件
    navigateTo(): # 路由跳转（编程式）
    useAppConfig():
    useAsyncData(): # 获取异步数据，支持 SSR
    useCookie():
    useFetch(): # 类似 useAsyncData，自动处理 fetch
    useHead():
    useNuxtApp(): # 使用nuxt app
    useRuntimeConfig(): # 读取配置属性
    useState():
h3: # 服务端API
    createError():
    defineEventHandler(): # 定义 API 处理函数
    readBody(): # 
```


### Plugin
```ts
import { createPinia } from 'pinia'
export default defineNuxtPlugin(nuxtApp => {
  nuxtApp.vueApp.use(createPinia())
})
```

nuxt插件
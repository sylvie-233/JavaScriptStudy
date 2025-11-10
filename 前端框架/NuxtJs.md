# NuxtJs

>
> ``
>

## 基础介绍

Vue.js SSR

- 服务端渲染（SSR）：优化 SEO，提升首屏速度
- 静态生成（SSG）：生成静态 HTML，部署方便
- 文件路由：pages 目录自动生成路由


- NuxtPage基于文件系统的路由视图组件
- NuxtLayout声明使用的布局组件

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
    /app: # 客户端
        /assets: # 资源文件
        /components: # 组件（自动注册）
        /composables: # Hooks 钩子函数
        /layouts: # 布局
            default.vue: # 主布局组件（默认）
        /middleware: # 中间件
            main.global.js:
                defineNuxtRouteMiddleware(): # 定义全局路由中间件
                    abortNavigation():
                    navigateTo():
        /pages: # 页面
            [...path].vue: # 路由捕获
            [param].vue: # 动态路由
                $route: # 路由信息
                    meta:
                    params:
                $style: # 模块样式
                $fetch(): # 数据获取
                definePageMeta():
                    title:
                    layout: # 使用的布局组件
                    middleware: # 使用的中间件
                ref():
                setPageLayout(): # 修改页面布局组件
                useHead(): # HTML 元信息
                    title:
                    meta:
                    link:
                useNuxtApp(): # 获取app实例
                useRoute():
                useRouter(): # 编程式路由
                useSeoMeta():
                useToast():
                useUserSession():
                    clear():
        /plugins: # 插件函数
            index.js:
                defineNuxtPlugin(): # 定义插件
                    nuxtApp:
                        provide():
        /stores: # 全局状态函数
        /utils: # 工具函数
        app.vue:
        error.vue: # 全局异常页面
    /node_modules:
    /public:
    /server: # 服务端
        /api:
            index.get.js:
                defineEventHandler():
                    event:
                    createError():
                        statusCode:
                        statusMessage:
                    readBody(): # 获取请求体
                    setUserSession():
        /middleware:
        /routes:
        /utils:
    nuxt.config.ts: # 配置文件
    package.json:
    tsconfig.json:
```

#### app.vue
```vue
<template>
    <NuxtLayout>
        <NuxtRouteAnnouncer />
        <NuxtWelcome />
        <NuxtPage /> 
    </NuxtLayout>
</template>
```

应用程序入口页面



#### nuxt.config.ts
```yaml
NuxtConfig:
    $production: # 生产环境配置
    app: # 应用配置
        head:
            link:
    components: # 组件注册
    css: # css文件
    devtools: # 开发工具
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
    build: # 构建
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

### Components

内置组件


#### ClientOnly

#### NuxtLayout
#### NuxtLink

链接

#### NuxtPage




### Middleware

中间件
全局中间件 -> 命名中间件 -> 本地中间件


### Plugin
```ts
import { createPinia } from 'pinia'
export default defineNuxtPlugin(nuxtApp => {
  nuxtApp.vueApp.use(createPinia())
})
```

nuxt插件



### Nitro


SSR 引擎



### Module

第三方模块


#### @nuxt/ui
#### nuxt-auth-utils
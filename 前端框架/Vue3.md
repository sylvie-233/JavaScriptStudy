# Vue3

>
> `# TODO 尚硅谷Vue3入门到实战，最新版vue3+TypeScript前端开发教程`
>


## 基础介绍

vue-cli基于webpack脚手架、vue3建议使用vite构建

### 项目结构

```
:
    /public:
        favicon.ico:
    /src:
        /assets:
        /components:
        App.vue:
        main.ts:
    env.d.ts:
    index.html:
    package.json:
    tsconfig.app.json:
    tsconfig.json:
    tsconfig.node.json:
    vite.config.json:
```



## 核心内容

```yaml
vue:
    App:
        mount(): 挂载
        use(): 使用中间件
    RefImpl:
        value: 代理数据
    createApp(): 创建应用
    reactive(): 响应式数据
    ref(): 响应式数据
```

setup函数可以返回一个渲染函数，setup相对于Vue2中的生命周期是最早的


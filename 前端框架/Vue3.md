# Vue3

>
> 
>


## 基础介绍

vue-cli基于webpack脚手架、vue3建议使用vite构建

### 项目结构
```yaml
目录结构:
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
        config:
            globalProperties:
        component():
        directive(): # 自定义指令
        mount(): # 挂载
        use(): # 使用中间件
    RefImpl:
        value: 代理数据
    computed(): # 计算属性
    createApp(): # 创建应用
    customRef(): # 自定义ref（传入回调函数，返回对象重写get、set，），(get调用track, set调用trigger)
    defineEmits():
    defineExpose(): # 组件ref导出定义
    defineProps(): # 定义组件属性
    inject:
    markRaw(): 标记不会变成响应式对象
    provide:
    reactive(): # 响应式数据
    readonly(): # 响应式转只读数据
    ref(): # 响应式数据
    shallowReactive(): 浅层reactive响应式
    shallowReadonly():
    shallowRef(): 浅层ref响应式
    toRaw(): 响应式数据转原始对象
    toRef():
    toRefs():
    watch():
    watchEffect(): # 监视变化

vue-router:
    RouterLink:
    RouterView:
    createRouter():
    creatWebHashHistory():
    createWebHistory():
    useRoute():
        params:
        query:
    useRouter():
        push():
        replace():

pinia:
    createPinia():
    defineStore():
        $state:
        $patch(): # 修改state
        $reset(): # 重置state
        $subscribe(): # 订阅（变化监听）
    mapState():
    storeToRefs():
```

setup函数可以返回一个渲染函数，setup相对于Vue2中的生命周期是最早的

v-model双向绑定

computed计算属性：给响应式数据提供了一个处理过程

### 生命周期
- setup():
- onBeforeMount():
- onMounted():
- onBeforeUpdate():
- onUpdated():
- onBeforeUnmount():
- onUnmounted():



### 组件通信

- props属性传递
- 自定义事件event
- 事件总线bus
- v-model:
- $attr:
- $refs/$parent:



### 页面插槽

```HTML

<slot>默认内容</slot>


<template v-slot:xxx>插入内容</template>
<slot name="xxx">默认内容</slot>


<template #xxx="{prop}">插入内容</template>
<slot name="xxx" :prop="xxx">默认内容</slot>

```

- 默认插槽
- 具名插槽
- 作用域插槽：插槽引用子组件传递的变量/数据


`<slot>`定义插槽、`<template>`插入插槽




### 内置组件

#### Teleport
```html
<Teleport on="css选择器">
    传送内容
</Teleport>
```

传送组件





#### Suspense
```html
<Suspense>
    <template v-slot:default>
        延迟显示内容
    </template>
    <template v-slot:fallback>
        兜底显示内容
    </template>
</Suspense>
```

延时组件




### HOOKS

响应式数据、修改方法




### 页面路由

```yaml
router-link:
    active-class:
    params:
    to:
        name:
        path:
        query:


router-view:

```


嵌套路由






### 状态管理



#### Pinia

```javascript
import { defineStore } from "pinia"

const store = defineStore("storeId", {
    state: () => {
        return {
            状态值
        }
    },
    getters: {
        getter函数：计算属性（传入state）
    },
    actions: {
        this引用，修改state的方法
    }
})
```


定义store，每个store为一个Hooks函数



## 项目实战







# Vue3

>
> `# TODO 尚硅谷Vue3入门到实战，最新版vue3+TypeScript前端开发教程 P61`
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
    computed(): 计算属性
    createApp(): 创建应用
    defineEmits():
    defineExpose(): 组件ref导出定义
    defineProps(): 定义组件属性
    inject:
    provide:
    reactive(): 响应式数据
    ref(): 响应式数据
    toRef():
    toRefs():
    watch():
    watchEffect(): 监视变化

vue-router:
    RouterLink:
    RouterView:
    createRouter():
    creatWebHashHistory():
    createWebHistory():
    useRoute():
        :
            params:
            query:
    useRouter():
        :
            push():
            replace():

pinia:
    createPinia():
        :
    defineStore():
        :
            $state:
            $patch(): 修改state
            $reset(): 重置state
            $subscribe(): 订阅（变化监听）
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






### 内置组件


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





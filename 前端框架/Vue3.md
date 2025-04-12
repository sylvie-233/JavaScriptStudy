# Vue3

>
> `https://cn.vuejs.org/guide/components/props.html`
>


## 基础介绍


支持选项式API（对象）、组合式API（函数）两种风格
单文件组件 (简称 SFC)


vue-cli基于webpack脚手架、vue3建议使用vite构建
- data
- methods
- props
- computed
- watch
- hooks
- components
- event/emit
- slot

![Vue生命周期钩子](../assets/Vue生命周期钩子.png)



当根组件没有设置template选项时，Vue将自动使用容器的innerHTML作为模板
createApp()可创建多次，一个页面可共存多个app对象


### 项目结构
```yaml
项目结构:
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
        config: # 应用配置
            errorHandler: # (err) 组件异常处理
            globalProperties: # 全局属性配置
        component(): # 组件注册
        directive(): # 自定义指令
            bindings: # 绑定对象
                instance: # 组件实例
                value: # 当前绑定值
                oldValue: # 上一个绑定值
                arg: # 参数（如 v-my-dir:foo）
                modifiers: # 修饰符（如 v-my-dir.foo.bar）
                dir: # 指令定义对象本身
            el: # DOM对象
        mount(): # 挂载，可接收DOM对象或字符串
        use(): # 使用中间件
    ComputedRef: # 计算属性ref
    DefineComponent: # 组件定义类型
    InjectionKey: # 依赖注入key
    PropType: # 属性类型
    Ref: # 引用类型
    RefImpl:
        value: # 代理数据
    VNode: # 虚拟 DOM 节点
    VNodeTypes:
    computed(): # 计算属性，返回ref对象，支持可写计算属性(setter、getter)
    createApp(): # 创建应用App，传入一个组件创建应用对象app
    createVNode(): # 创建虚拟节点
    customRef(): # 自定义ref（传入回调函数，返回对象重写get、set，），(get调用track, set调用trigger)
    defineComponent(): # 自定义组件
        $attr: # 内置属性传值
            class:
        $emit: # 内置信号触发
        components: # 组件注册
        emits: # 自定义事件
        directives: # 自定义指令
        props: # 组件属性
          required:
          type:
        setup: # 选项式api,(props, ctx)
          ctx:
          props:
        template: # 组件模板，可直接使用字符串，或引用dom元素
        data(): # 组件状态，选项式
        setup(): # 专门用于组合式 API设置
    defineEmits(): # 自定义事件，返回emit()触发函数
    defineExpose(): # 显式定义导出
    defineProps(): # 定义组件属性props
    expose():
    h(): # dom渲染函数
    inject():
    isRef():
    isReactive():
    isReadonly():
    isProxy():
    markRaw(): # 标记不会变成响应式对象
    nextTick(): # 等待dom刷新，用于默认异步的状态更新
    onActivated():
    onBeforeMount():
    onBeforeUnmount():
    onBeforeUpdate():
    onDeactivated():
    onErrorCaptured():
    onMounted(): # DOM挂载时，生命周期钩子
    onRenderTracked():
    onRenderTriggered():
    onUnmounted():
    onUpdated():
	onWatcherCleanup(): # 上一次watch清理
    provide():
    reactive(): # 响应式数据， 返回的是一个原始对象的 Proxy
    readonly(): # 响应式转只读数据
    ref(): # 基础响应式数据，也可用于引用DOM
        value: # js中需通过修改value来实现响应式
    shallowReactive(): # 浅层reactive响应式
    shallowReadonly():
    shallowRef(): # 浅层ref响应式
    toRaw(): # 响应式数据转原始对象
    toRef():
    toRefs():
    unref():
    useAttrs():
    useModel():
    useSlots():
	useTemplateRef(): # 原生dom引用，支持引用多个
    watch(): # 响应式数据监听(new, old, onCleanup)，支持单值响应式数据、getter()函数、多数据源数组，返回取消监听函数
		deep: # 深度监听
		flush: # 值刷新执行时期
			post:
			sync:
		immediate: # 初始化立即执行
		once: # 仅执行一次
    watchEffect(): # 监视变化(onCleanup)，自动监听回调方法中所有的响应式数据变化
    watchPostEffect(): # 后置监视变化， 在 Vue 更新后执行
    watchSyncEffect(): # 前置监视变化，在 VUe 更新之前执行
    withDefaults():

vue-router:
    RouterLink:
    RouterView:
    createRouter():
        history: # 路由模式
        routes: # 路由表
            path:
            component:
            children:
    creatWebHashHistory():
    createWebHistory():
    useRoute(): # 获取当前路由信息
        params:
        query:
    useRouter(): # 获取路由器
        push():
            path:
            name:
            query:
        replace():

pinia:
    createPinia():
    defineStore():
        $state:
        $patch(): # 修改state
        $reset(): # 重置state
        $subscribe(): # 订阅（变化监听）
        state:
        actions:
        getters:
    mapState():
    storeToRefs(): # 转换为vue的ref变量
```

setup函数可以返回一个渲染函数，setup相对于Vue2中的生命周期是最早的

v-model双向绑定

computed计算属性：给响应式数据提供了一个处理过程



### 模板语法
```yaml
Template:
    {{}}: # 文本插值，支持js表达式
    v-bind: # 属性绑定，支持同名简写es6、动态绑定多个值(直接绑定对象)、动态参数:[xxx]
    v-for: # 列表渲染，可遍历对象，整数
    v-html: # 原始 HTML显示
    v-if ... v-else-if ... v-else ...: # 条件渲染
    v-model: # props.modelValue、$emit("update:modelValue")，双向绑定，支持多个元素绑定到同一个数组
		false-value:
		true-value:
		lazy: # input变更位change事件
		number: # 字符串转数字
		trim:
		<input>:
		<textarea>:
		<select>:
		<radio>:
		<checkbox>:
    v-on: # $event，事件绑定@，支持内联事件处理，方法事件处理
        $event: # 内联事件处理中访问原生dom事件
			preventDefault():
			stopPropagation():
		capture:
		click: # 点击事件
			left:
			middle:
			right:
		keyup: # 按键监听
			alt:
			ctrl:
			down:
			enter:
			esc:
			exact:
			delete:
			left:
			meta:
			right:
			shift:
			space:
			tab:
			up:
		once:
		passive:
        prevent: # 阻止默认行为
		self: # event.target触发对象是自身时才会执行
		stop: # 停止事件冒泡
    v-show: # 条件渲染
    v-slot: # 插槽

Component:
    Component: # 动态组件 
        is:
    Teleport: # 传送组件
    Transition: # 动画过渡组件
        name:
    TransitionGroup: # 动画过渡组组件
        name:
        tag:
```

v-on、v-bind可实现动态参数绑定：`v-bind:[attr]`

v-for可遍历对象属性

class样式绑定、style样式绑定



#### 页面插槽
```jsx
// 匿名插槽
<template>
  <div class="card">
    <slot></slot>
  </div>
</template>


// 具名插槽
<template>
  <header><slot name="header" /></header>
  <main><slot /></main>
</template>

// 父组件具名插入
<template v-slot:header>
    <h1>标题</h1>
</template> 


// 作用域插槽，子组件向插槽传递值，父组件可以接收这些值并使用
// 子组件传递值
<template>
  <slot :user="user" />
</template>

// 父组件接收值
<UserCard>
  <template v-slot="{ user }">
    <p>姓名：{{ user.name }}</p>
    <p>年龄：{{ user.age }}</p>
  </template>
</UserCard>
```

- 默认插槽
- 具名插槽
- 作用域插槽：插槽引用子组件传递的变量/数据


`<slot>`定义插槽、`<template>`插入插槽
slot可以反向传值给template


#### 自定义指令
```jsx
<div id="app">
  <input v-focus />
</div>

<script>
    const app = Vue.createApp({
        directives: {
            // 自定义 v-focus 指令
            focus: {
                mounted(el) {
                    el.focus();
                }
            }
        }
    });
    app.mount('#app');
</script>
```

指令绑定生命周期：
- created()：	指令绑定到元素上时
- beforeMount()：	元素准备挂载到DOM之前
- mounted()：	元素已经挂载到 DOM
- beforeUpdate()： 更新前
- updated()：更新后
- beforeUnmount()：卸载前
- unmounted()：元素已经被卸载

#### 事件处理

v-on
受控组件、非受控组件


#### 样式绑定

v-bind class、style



### 内置组件
#### component
```jsx
<component :is="currentComponent"></component>
```

动态组件，用于根据绑定的is属性动态切换组件


#### keep-alive
```jsx
<keep-alive>
  <component :is="currentTabComponent"></component>
</keep-alive>
```

`<keep-alive>`是一个特殊的包装组件，用于缓存动态组件实例。


#### suspense
```html
<suspense>
    <template v-slot:default>
        延迟显示内容
    </template>
    <template v-slot:fallback>
        兜底显示内容
    </template>
</suspense>
```

异步加载组件



#### teleport
```html
<teleport to="body">
  <div class="modal">我是弹窗</div>
</teleport>
```

传送组件







#### transition
```jsx
<transition name="fade">
  <p v-if="show">Hello</p>
</transition>
```

为单个元素或组件添加进入 / 离开过渡效果


#### transition-group
```jsx
<transition-group name="list" tag="ul">
  <li v-for="item in items" :key="item.id">{{ item.text }}</li>
</transition-group>
```

用于给多个元素添加过渡效果，常用于列表的进入/离开动画











### 生命周期

- setup():
    - onBeforeCreate():
    - onCreated():
    - onBeforeMount():
    - onMounted():
    - onBeforeUpdate():
    - onUpdated():
    - onBeforeUnmount():
    - onUnmounted():
    - onErrorCaptured():
- beforeCreate():
- created():
- beforeMount():
- mounted():
- beforeUpdate():
- updated():
- activated():
- deactivated():
- beforeDestroy():
- destroyed():
- errorCaptured():



#### setup

支持组合式api的生命周期
在所有生命周期之前执行





### 组件通信

- props属性传递
- 自定义事件event
- 事件总线bus
- v-model:
- $attr:
- $refs/$parent:


#### props

属性传递


#### v-model
```jsx
// 自定义组件使用v-model
<MyInput v-model="value" />

// 等价于modelValue属性 + 自定义update事件
<MyInput :modelValue="value" @update:modelValue="value = $event" />

// 自定义处理v-model
// MyInput.vue
<template>
  <input :value="modelValue" @input="$emit('update:modelValue', $event.target.value)" />
</template>

<script>
export default {
  props: ['modelValue']
}
</script>
```

组件value双向绑定



#### event

defineEmits()、


#### inject


provide()、inject()









### HOOKS

- 响应式系统 (ref/reactive etc.)
- 侦听变化 (watch/watchEffect)  
- 生命周期 (onMounted 等)   
- 注入/提供 (provide/inject) 
- 组件上下文 (attrs, slots)  
- 其他工具 (nextTick, computed)



#### ref


#### reacttive



#### watch
```jsx
const count = ref(0);

// 使用 watch 监听 count 的变化
watch(count, (newValue, oldValue) => {
    console.log(`count changed from ${oldValue} to ${newValue}`);
});
```

属性变化监听



#### watchEffect
```jsx
const count = ref(0)

watchEffect(() => {
  // 任何响应式数据变化时都会触发
  console.log('Count has changed:', count.value)
})

count.value++  // 当 count 变化时，watchEffect 会触发
```


与 watch 不同，watchEffect 不需要显式地指定需要观察的数据源，它会自动追踪你在函数中使用的响应式数据


#### onMounted



#### nextTick





### 扩展机制


#### Plugin
```jsx
// 自定义函数式插件
const myPlugin = (app, options) => {
  app.config.globalProperties.$myPlugin = options
}

// 全局注册插件
const app = createApp(App)
app.use(myPlugin, { name: 'My Custom Plugin' })
app.mount('#app')
```


app.use()会将插件安装到Vue应用实例中。Vue会调用插件的install方法（如果插件是一个对象且实现了install方法

插件会做一些全局的配置（比如添加全局组件、指令、挂载全局方法或配置等


自定义插件支持对象式(install)、函数式插件


### 页面路由
```jsx
// router.js 路由定义
const routes = [
  { path: '/', component: Home },
  { path: '/about', component: About },
]

const router = createRouter({
  history: createWebHistory(), // 使用 HTML5 模式
  routes
})


// main.js 注册路由
app.use(router)

// App.vue路由布局
<template>
  <nav>
    <router-link to="/">首页</router-link>
    <router-link to="/about">关于</router-link>
  </nav>
  <router-view /> 
  {/* router-view可在组件内部嵌套，实现嵌套路由出口 */}
</template>
```


嵌套路由






### 状态管理



#### Pinia
```jsx
// store.js
import { defineStore } from 'pinia'

export const useCounterStore = defineStore('counter', {
  state: () => ({
    count: 0,
    name: 'pinia'
  }),
  getters: {
    doubleCount: (state) => state.count * 2
  },
  actions: {
    increment() {
      this.count++
    }
  }
})

// main.js中注册
app.use(pinia)

// 组件中使用 store
const counter = useCounterStore()
```


定义store，每个store为一个Hooks函数










# uni-app


## 基础介绍

使用Vue语法开发多端程序


多page -> component




### 目录结构
```yaml
目录结构:
    /components:
    /mixins:
    /node_modules:
    /pages:
    /static:
    /store:
    /subpkg:
    App.vue:
    main.js:
    manifest.json:
    pages.json:
    uni.scss:
```

#### manifest.json
```yaml
:
    mp-weixin:
        appid:
        setting:
            urlCheck:
```

项目配置




#### pages.json
```yaml
:
    globalStyle:
        backgroundColor:
        navigationBarTextStyle:
    pages:
        page:
        style:
    subPackages: # 分包
        pages:
        root:
        style:
    tabBar:
        list:
            iconPath:
            pagePath:
            selectedIconPath:
            text:
        selectedColor:
```

声明式路由配置





## 核心内容
```yaml
vue2:
    data:
    methods:
    onLoad():

vue3:


vuex:
    Store:
        modules:
            getters:
            mutations:
            namespaced:
            state:
    mapGetters():
    mapMutations():
    mapState():
    
uni:
    chooseAddress():
    getStorageSync():
    getSystemInfoSync():
        model:
        screenHeight:
        screenWidth:
    hideLoading():
    navigateTo():
    openSetting():
    previewImage():
    setStorageSync():
    setTabBarBadge():
    showLoading():
    showModal():
    showToast():
        duration:
        icon:
        title:
    switchTab():
```


### 内置组件
```yaml
内置组件:
    <block>: # 空白标签
    <image>:
        src:
    <navigator>:
        url:
    <radio>:
    <scroll-view>:
        scroll-top:
    <swiper>:
        autoplay:
        circular:
        duration:
        indicator-dots:
        interval:
    <swiper-item>:
    <template>:
    <text>:
    <view>:
```


### 模板语法


使用Vue模板语法


### 页面路由

`uni.navagateTo()`


### 状态管理


Vuex




### Page
```yaml
Page:
    computed:
    data: # 数据定义
    methods: # 方法定义
    mixins:
    onLoad():
    onReachBottom():
    $emit(): # 触发自定义事件
```






页面Vue组件





### Component
```yaml
Component:
    computed:
    data:
    filters:
    method:
    mixins:
    props:
        default:
        type:
    watch:
    $emit():
```





## uni-app x


Vue3组合式API



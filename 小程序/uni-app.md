# uni-app


## 基础介绍

使用Vue语法开发多端程序




### 目录结构
```yaml
目录结构:
    /components:
    /pages:
    /static:
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
uni:
    hideLoading():
    showLoading():
    showToast():
        duration:
        icon:
        title:
    switchTab():
```


### 内置组件
```yaml
内置组件:
    <image>:
        src:
    <navigator>:
        url:
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



### 状态管理


Vuex




### Page
```yaml
Page:
   data: # 数据定义
   methods: # 方法定义
   onLoad():
```






页面Vue组件





### Component





## uni-app x


Vue3组合式API



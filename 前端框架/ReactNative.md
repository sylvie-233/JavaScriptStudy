# ReactNative

`react native入门到实战：P21`

## 基础介绍

React移动端解决方案

`create-expo-app`expo项目脚手架

### 目录结构
```yaml
expo项目:
    /app:
    /assets:
    /components:
    /constants:
    /hooks:
    /node_modules:
    /scripts:
    app.json:
    babel.config.js:
    metro.config.js:
    package.json:
    tailwind.config.js:
    tsconfig.json:
```







#### app.json
```yaml
app.json:
    expo:
        android: # 安卓平台配置
            adaptiveIcon:
                backgroundColor:
                foregroundImage:
            package: # 主包名
            permissions: # 手机权限
                CAMERA:
                LOCATION:
            versionCode:
        assetBundlePatterns: # 资源文件打包
        extra: # 额外参数（环境变量）,可通过expo-constants获取
            apiBaseUrl: # 常配置api url
        icon: # 应用图标
        ios: # ios平台配置
        name: # 应用名称
        orientation: # 应用方向
            portrait: # 竖向
        scheme: # 自定义deeplink（URL Scheme）
        splash: # 启动画面、首屏广告
            backgroundColor:
            image:
            resizeMode:
        slug:
        updates: # 远程更新
            fallbackToCacheTimeout:
        userInterfaceStyle: # 深色/浅色模式
            automatic:
        version: # 版本
        web: # WEB平台配置
```


打包构建配置
控制应用的名称、图标、权限、依赖项


#### app.config.js

app.json的js配置版本


#### metro.config.js




#### eas.json
```yaml
eas.json:
    build: # 构建配置（多环境Profile）
        development:
        preview:
        production: # 生产环境
            android: # 安卓打包配置
                apk:
                app-bundle:
            distribution:
            ios:
    cli:
        version:
    submit:
        production:
            android:
                serviceAccountKeyPath:
```

eas服务配置



### expo
```yaml
expo:
    build:
        --profile: # 指定配置环境Profile 
        android:
            -t: # apk
    init: # 初始化项目、脚手架
    install: # expo组件安装
    prebuild: # 预构建、生成原生项目
    publish: # 项目发布到expo
    start: # 开发服务器启动
        --android:
        --ios:
        a: # 安卓启动
        i: # ios启动
        w: # web启动
        e: # expo go启动
```


开发命令工具



#### eas
```yaml
eas:
    build: # 远程构建
        --platform:
        configure: # 生成 eas.json远程项目配置文件
    doctor: # 项目环境检测
    login: # 登录expo
```

打包命令工具



## 核心内容
```yaml
react:
    Component: # 类组件
react-native:
    ActiveIndicator: # 加载指示器
        animating:
        color:
        size:
    Alert: # 提示框
        alert(): # 可设置多个item
            onPress: # 点击事件
            style:
            text:
    Animated: # 动画
    AppRegistry:
        registerComponent(): # 主页面组件注册
    Button: # 按钮
        title:
        onPress:
    Dimensions: # 动态尺寸、媒体查询 
        addEventListener():
            change:
        get():
            screen:
            window:
                height:
                width:
    FlatList: # 高性能列表、列表渲染
        data: # 数据列表
        horizontal: # 水平方向
        initialNumberToRender:
        initialScrollIndex:
        ItemSeparatorComponent:
        ListEmptyComponent:
        ListFooterComponent:
        ListHeaderComponent:
        numColumns:
        keyExtractor: # key生成
        onEndReached:
        onRefresh:
        renderItem: # 渲染函数
    Image: # 图片
        source:
    ImageBackground:
    KeyboardAvoidingView:
    Modal: # 模态组件
        animationType:
            fade:
            slide:
        onRequestClose:
        presentationStyle:
            pageSheet:
        visible:
    NativeModules:
    Platform: # 平台，媒体查询
        OS: # 操作系统
        select():
            android:
            ios:
    Pressable:
        onLongPress:
        onPress:
        onPressIn:
        onPressOut:
    SafeAreaView: # 安全界面视图
    ScrollView: # 滚动视图
        contentContainerStyle:
        horizontal:
    SectionList: # 分组列表、支持下拉刷新、上拉加载
        ItemSeparatorComponent:
        keyExtractor:
        ListEmptyComponent:
        ListHeaderComponent:
        onEndReached:
        onEndReachedThreshold:
        onRefresh:
        renderItem: # 渲染函数
        renderSectionHeader:
        sections: # 列表数据
    Switch: # 开关按钮
        onValueChange:
        trackColor: # 背景色
        thumbColor: # 前景色
        value:
    StatusBar: # 状态栏
        backgroundColor: # 背景色
        barStyle: # 预设样式
        hidden: # 隐藏状态条
    StyleSheet: # css样式
        create():
    Text: # <p>
        style:
    TextInput: # 输入框
        keyboardType:
        multline: # 多行输入框
        numberOfLines:
        onChangeText: # 输入文本事件
        placeholder:
        secureTextEntry:
        value:
    TouchalbeHighlight:
    TouchalbeOpacity:
    TouchalbeWithoutFeedback:
    View: # <div>
        style:
    alert():
    useWindowDimensions():
@react-navigation
    bottom-tabs:
        createBottomTabNavigator():
            Navigator:
            Screen:
    drawer:
        createDrawerNavigator():
            Navigator:
            Screen:
    material-top-tabs:
    native:
        DartTheme:
        DefaultTheme:
        NavigationContainer:
        ThemeProvider:
        useNavigation(): # 编程式导航
            navigate():
    native-stack:
        createNativeStackNavigator():
            Navigator:
            Screen:
                component:
                name:
                navigation: # 自动注入
                    navigate(): # 路由切换
                options:
                    headerStyle:
                    title:
                route:
                    params:
    stack:
        createStackNavigator():
```







### 组件



- 函数式组件
- 类组件

- 条件渲染：if
- 列表渲染：map、FlatList


#### 事件机制
```yaml
Event:
    onPress: # 点击事件
```

#### 生命周期

##### componentDidMount

##### componentDidUpdate

##### componentWillUnmount



#### 组件样式


##### StyleSheet

样式组件，不能直接使用CSS
组件样式不具有继承性、可传递多个对象


##### Animated








### Hook

#### useState

状态管理

#### useEffect

副作用钩子，挂载、数据监听




### 组件通信



#### Props



#### Context



### 状态管理

#### Zustand


#### Redux



#### Mobx









### 组件路由
```jsx
import { NavigationContainer } from '@react-navigation/native';
import { createStackNavigator } from '@react-navigation/stack';

const Stack = createStackNavigator();

// 配置路由
const App = () => (
  <NavigationContainer>
    <Stack.Navigator>
      <Stack.Screen name="Home" component={HomeScreen} options={{ title: '首页' }} />
      <Stack.Screen name="Detail" component={DetailScreen} options={{ title: '详情页' }} />
    </Stack.Navigator>
  </NavigationContainer>
);
```


#### NavigationContainer

路由容器

#### Navigator

##### Screen

NavigationContainer -> Navigator -> Screen(可嵌套Navigator)



### 原生模块


#### NativeModules



## Expo
```yaml
expo:
    metro-config:
        getDefaultConfig():
expo-av:
expo-background-fetch:
expo-camera:
expo-constants:
expo-contacts:
expo-device:
expo-file-system: # 文件访问
expo-font:
expo-gl:
expo-google-maps:
expo-image-picker:
expo-linking:
expo-location:
expo-media-library:
expo-notifications:
expo-permissions:
expo-router: # 基于文件结构的约定式路由
    Link:
    Slot: # layout子组件插槽
    Stack: # 路由视图容器
        Screen: # 视图页面定义
            name:
            options: 
    router:
    useRouter():
        params:
        pathname:
        query:
        back():
        push():
expo-secure-store:
expo-sensors:
expo-sharing:
expo-sms:
expo-splash-screen:
    SplashScreen:
expo-sqlite: # sqlite数据库访问
expo-status-bar:
    StatusBar:
expo-task-manager:
```

### expo-av

音频播放


### expo-camera

相机访问

### expo-notifications

消息通知

### expo-permissions

动态权限

### expo-router
```yaml
Component: # 视图组件配置
    navigationOptions:
```

基于文件目录结构的路由，类似nextjs的路由管理
支持动态路由、_layout布局


# ReactNative

`react native入门到实战：P5`

## 基础介绍

React移动端解决方案



### 目录结构
```yaml
expo项目:

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
expo-constants:
expo-status-bar:
    StatusBar:

react-native:
    ActiveIndicator:
        animating:
        size:
    Alert: # 提示框
        alert():
            onPress:
            text:
    Animated: # 动画组件
    Button: # 按钮组件
        title:
        onPress:
    Dimensions: # 动态尺寸
        addEventListener():
            change:
        get():
            screen:
            window:
                height:
                width:
    FlatList: # 列表渲染
        data:
        ItemSeparatorComponent:
        ListEmptyComponent:
        ListFooterComponent:
        ListHeaderComponent:
        keyExtractor:
        renderItem:
    Image: # 图像
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
    Platform: # 平台查询
        OS:
        select():
            android:
            ios:
    Pressable:
        onLongPress:
        onPress:
        onPressIn:
        onPressOut:
    SafeAreaView:
    ScrollView: # 滚动视图
    SectionList:
        renderItem:
        renderSectionHeader:
        sections:
    Switch:
        onValueChange:
        value:
    StatusBar: # 状态栏
        backgroundColor:
        barStyle:
        hidden:
    StyleSheet:
        create():
    Text:
        style:
    TextInput:
        multlineText:
        onChange:
        value:
    View:
        style:
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
    native:
        NavigationContainer:
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
```yaml

```

- 条件渲染：if
- 列表渲染：map、FlatList


#### 事件机制
```yaml
Event:
    onPress:
```

#### 生命周期

##### componentDidMount

##### componentDidUpdate

##### componentWillUnmount



#### 组件样式


##### StyleSheet

样式组件，不能直接使用CSS


#### 自定义组件







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
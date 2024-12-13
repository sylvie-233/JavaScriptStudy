# React


## 基础介绍


### react-scripts
```yaml
react-scripts:

```


## 核心内容
```yaml
react:
    createContext(): # 上下文通信
        Provider:
            value:
    useContext(): # 使用上下文
    useEffect():
    useState():

react-dom:
    render():

react-router-dom:
    BrowserRouter:
    Link:
        to:
    NavLink:
        activeClassName:
        to:
    Redirect:
        to:
    Route:
        exact:
        path:
    Switch:
    useLocation(): # 路由导航信息
        pathname:

mobx:
    @action: # 定义响应式数据操作方法
        bound:
    @computed: # 定义计算属性
        observe():
    @observable: # 定义响应式数据
    makeObservable():

mobx-react:
    @observer: # 使组件可观测(响应状态变化更新)

react-native:
    ActiveIndicator:
        animating:
        size:
    Alert: # 提示框
        alert():
            onPress:
            text:
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
    Image: # 图像
        source:
    ImageBackground:
    Modal: # 模态组件
        animationType:
            fade:
            slide:
        onRequestClose:
        presentationStyle:
            pageSheet:
        visible:
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
    StatusBar: # 状态栏
        backgroundColor:
        barStyle:
        hidden:
    StyleSheet:
        create():
    Text:
        style:
    View:
        style:
    useWindowDimensions():

expo-status-bar:
    StatusBar:
```


### 组件路由



### 组件通信


### 状态管理

#### mobx
```js

```


基础集成；
- 响应组件
- 状态
- 修改状态的方法




## React Native

### 目录结构
```yaml
:

```

#### app.json
```yaml
app.json:
    expo:
        name:
        orientation:
        splash:
```



### expo
```yaml
expo:
    start:
```



### StyleSheet



### 自定义组件


### 组件渲染






条件渲染、列表渲染


### 组件通信


### 组件路由




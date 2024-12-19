# React

`react项目实战：P21`


## 基础介绍


### react-scripts
```yaml
react-scripts:

```


## 核心内容
```yaml
react:
    ReactNode:
    StrictMode:
    createContext(): # 上下文通信
        Provider:
            value:
    useContext(): # 使用上下文
    useEffect():
    useRef(): # ref引用DOM
        current:
    useState():

react-dom:
    client:
        ReactDOM:
            createRoot():
                reander():
    render():

react-router-dom:
    BrowserRouter:
        basename:
    Link:
        to:
    Navigate:
    NavLink:
        activeClassName:
        to:
    Outlet: # router-view，子路由显示入口
    Redirect:
        to:
    Route:
        element:
        exact:
        loader:
        path:
    RouterProvider: # 总route显示
        router:
    Routes:
    Switch:
    createBrowserRouter():
        _options:
            basename:
        path:
        element:
        children:
    createRoutesFromElements():
    useLocation(): # 路由导航信息
        pathname:
    useNavigate():


redux:
@reduxjs/toolkit: # 定义store
    configureStore():
        reducer:
    createSlice(): # reducer：data、action
        name:
        initialState:
        reducers:
        ---
        actions:
        reducer:
react-redux: # 使用store
    Provider:
        store:
    useDispatch(): # 获取store方法
    useSelector(): # 获取store状态



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

expo-status-bar:
    StatusBar:

@react-navigation/native:
    NavigationContainer:
    useNavigation():
        navigate():
@react-navigation/native-stack:
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
@react-navigation/bottom-tabs:
    createBottomTabNavigator:
        Navigator:
        Screen:
@react-navigation/drawer:
    createDrawerNavigator():
        Navigator:
        Screen:
```


### 组件路由

React Router

```yaml
<BrowserRouter>:
    <Routes>:
        <Route>:
```


### 组件通信


### 状态管理


#### redux

reducer、



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


- 条件渲染：if
- 列表渲染：map、FlatList


### 组件通信


### 组件路由


NavigationContainer -> Navigator -> Screen(可嵌套Navigator)




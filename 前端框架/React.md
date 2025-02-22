# React

`react官方文档：https://react.dev/learn`
`React入门到实战：P60`


## 基础介绍



Javascript 前端UI框架

基于JSX（声明式UI）语法、组件化


核心库：
- react
- react-dom
- react-scripts



`create-react-app`：react项目脚手架

`{ xxx }`：JSX模板语法（支持js表达式）
组件必须有一个根节点

可利用表达式实现：条件渲染（三元运算符、&&）、列表渲染（map()）

组件样式clasName：行内样式、类名样式、module css、

组件事件绑定：`onXxx`


### 项目结构
```yaml
项目结构:
    /public:
        favicon.ico:
        index.html: # 项目主页面
        robots.txt: 
    /src:
        App.js: # 项目主应用
        App.css:
        index.js: # 项目入口文件
        index.css:
    package.json:
```


### react-scripts
```yaml
react-scripts:
    build: # 项目打包
    eject:
    start: # 开发运行
    test:
```

React打包命令





## 核心内容
```yaml
react: # react核心包
    Component: # 组件基类
    ReactNode:
    StrictMode: # 严格模式
    act():
    cache():
    createContext(): # 创建上下文
        Consumer: # 上下文消费者组件
        Provider: # 上下文提供者组件
            value:
    createElement(): # 创建DOM元素 (name, attrs, children)
    createRef(): # 原始DOM引用
        current:
    lazy():
    memo():
    startTransition():
    use():
    useActionState():
    useCallback():
    useContext(): # 使用上下文
    useDebugValue():
    useDeferredValue():
    useEffect():
    useId():
    useImperativeHandle():
    useInsertionEffect():
    useLayoutEffect():
    useMemo():
    useOptimistic():
    useReducer():
    useRef(): # ref引用DOM
        current:
    useState():
    useSyncExternalStore():
    useTransition():
react-dom:
    client:
        ReactDOM: # React Dom 操作工具类（创建、渲染）
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
mobx:
    @action: # 定义响应式数据操作方法
        bound:
    @computed: # 定义计算属性
        observe():
    @observable: # 定义响应式数据
    makeObservable():
mobx-react:
    @observer: # 使组件可观测(响应状态变化更新)


redux:
    configureStore(): # 定义store
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
```


### 内置组件

- <Fragment>：`<>`空节点
- <Profiler>
- <StrictMode>
- <Suspense>


#### 自定义组件
```jsx
// 自定义类组件
class MyComp extends React.Component {
    // 初始化状态，this.setState()修改状态
    state = { 
        name: "xxx"
    }
    render() {
        return <div>Sylvie233</div>
    }
}
```


函数组件、类组件

受控组件、非受控组件




##### 事件绑定
```yaml
事件绑定:
    onChange:
    onClick:
        nativeEvent:
        target:
        type:
        preventDefault():
```


##### 组件Props
```yaml
props:
    children:
```


props类型限定：`Xxx.propTypes`
props默认值：`Xxx.defaultProps`
（static静态属性）


##### 生命周期
```yaml
挂载阶段:
    constructor():
    render():
    componentDidMount():
更新阶段:
    render():
    componentDidUpdate():
销毁阶段:
    componentWillUnmount():
```

![React类组件生命周期](../assets/React类组件生命周期.png)



### Hook
```yaml
```



#### useState

创建状态属性



#### useEffect

实现生命周期、属性监听



#### useRef

原始DOM引用





### 组件通信


#### Props

属性传递、子传父通过传递方法实现
兄弟组件通信、状态提升


#### Context
```jsx
// 创建上下文
const {Provider, Consumer} = createContext():

// 提供者提供数据
<Provider value="xxx">

    {/* 消费者消费数据 */}
    <Consumer>
        {value => xxx}
    </Consumer>
<Provider>
```

可实现多级传递



### 组件路由
```yaml
<BrowserRouter>:
    <Routes>:
        <Route>:
```


React Router





### 状态管理

#### mobx
```js

```


基础集成；
- 响应组件
- 状态
- 修改状态的方法



#### redux

reducer、





## React Native
```yaml
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

### 内置组件

- 条件渲染：if
- 列表渲染：map、FlatList

#### 自定义组件






### 组件样式






### 组件通信





### 组件路由


NavigationContainer -> Navigator -> Screen(可嵌套Navigator)




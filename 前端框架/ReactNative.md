# ReactNative


## 基础介绍

React移动端解决方案



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



## 核心内容
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

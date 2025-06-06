# Flutter

`Flutter官方文档：https://docs.flutter.dev/`
`flutter从零到实战: P5`


## 基础介绍

基于Dart的跨平台GUI框架

依赖JDK、Android SDK(配置ANDROID_HOME)、Flutter SDK、Android模拟器
Flutter SDK中包含了Dart SDK


资源镜像：
- PUB_HOSTED_URL:
- FLUTTER_STORAGE_BASE_URL:


### 项目结构
```yaml
flutter:
    /.dart_tool:
        package_config.json: # 记录第三方包实际路径（本地）
    /.idea:
    /android:
    /build:
    /ios:
    /lib: # flutter主目录
        main.dart:
    /test: # 测试
    .metadata:
    analyasis_options.yaml:
    xxx.iml:
    pubspec.lock:
    pubspec.yaml:
```

#### 安装目录
```yaml
flutter:
    /.pub-cache: # 下载的公共模块
        /bin:
    /bin:
        /cache:
            /dart-sdk: # dart运行sdk
                /bin:
                    /resources:
                    /snapshots:
                    /utils:
                    dart:
                /include:
                /lib:
                /pkg:
        /internal:
        /mingit:
        dart:
        flutter:
    /dev:
    /docs:
    /engine:
    /examples:
    /packages:
```


#### pubspec.yaml
```yaml
pubspec.yaml:
    dependencies:
        flutter:
            sdk:
    description:
    dev_dependencies:
    name:
    version:
```




### flutter
```yaml
flutter:
    -h:
    --version:
    channel: # 版本管理
        beta:
    create: # 创建项目
    doctor: # 环境检测
    driver:
    emulator:
        --launch:
    emulators: # 所有模拟器
        --create:
        --launch:
    run: # 运行项目
        R: # 热重载
        c:
        d:
        h:
        q:
        r:
    upgrade:
```


## 核心内容
```yaml
dart:
    ui:
        ColorFilter:
        FontWeight: # 字体粗细
        TextAlign:
        TextDecoration:
flutter:
    animation: # 动画库
        Animation:
        AnimationController: # 动画控制器
            duration:
            addListener():
            addStatusListener():
            forward(): # 执行
            reverse():
        AnimationStatus:
        ColorTween:
        Tween:
    cupertinto:
    foundation:
        debugPrint():
    gestures:
    material: # 组件库
        ActionChip: # 徽章
            onPress:
        AlertDialog: # 警告 弹出框
        AppBar: # 标题栏
            title: # 标题
            bottom:
        BottomAppBar: # 底部滑动窗口
        BottomNavigationBar: # 底部导航条
        ButtonBar: # 按钮组
        Card: # 卡片
        Checkbox: # 复选框
            onChanged:
            value:
        CheckboxListTile: # 复选框 标签
        Chip: # 徽章
            label:
        ChoiceChip: # 徽章
        CircleAvatar: # 圆形头像
        Colors:
        DataCell: # 数据单元格
        DataColumn: # 数据列
        DataRow: # 数据行
            cells:
        DataTable: # 数据表
        DataTableSource: # 数据表 数据源
            getRow():
        DefaultTabController:
        Divider: # 分隔线
        Drawer:
        DrawerHeader:
        ElevatedButton: # 阴影 按钮
        ExpansionPanel: # 收缩面板
            body:
            headerBuilder:
            isExpanded:
        ExpansionPanelList: # 收缩面板列表
            expansionCallback:
        FilterChip: # 徽章
        FloatingActionButton: # 浮动按钮
        IconButton:
        Icons:
        InkWell:
        InputBorder:
        InputDecoration: # 装饰 输入框
            border:
            hintText:
            icon:
            labelText:
        ListTile: # 列表项
            leading:
            subtitle:
            title:
        Material: # Material样式
        MaterialApp: # 主应用，核心组件，携带路由
            debugShowCheckedModeBanner:
            home: # 应用主页
            initialRoute:
            onGenerateRoute: # 动态路由生成
            onUnknownRoute:
            routes:
            theme: # 样式主题
            title: # 标题
        MaterialPageRoute: # 路由页面
        OutlinedButton: # 边框 按钮
        PaginatedDataTable: # 分页 数据表
        PopupMenuButton: # 弹出菜单 按钮
            itemBuilder:
            onSelected:
        PopupMenuItem: # 弹出菜单项
        Radio: # 单选按钮
            groupValue:
        RadioListTile:
        Scaffold: # 脚手架组件，带底部导航，标题栏
            appBar: # 顶部导航条
            body: # 页面主体
            bottomNavigationBar: # 底部导航条
            drawer: # 左侧抽屉
            endDrawer:
            floatingActionButton: # 浮动按钮
            of():
            showSnakeBar():
        ScaffoldState:
            showBottomSheet(): # 底部滑动窗口
        SimpleDialog: # 简单弹出框
        SimpleDialogOption: # 弹出框选项
        Slider: # 滑动选择
            onChanged:
        SnackBar: # 底部消息提示
        SnackBarAction:
        Step: # 具体步骤
            content:
            isActive:
            subtitle:
            title:
        Stepper: # 步骤
            onStepCancel:
            onStepContinue:
            onStepTapped:
            steps:
        Switch: # 开关按钮
        SwitchListTile:
        Tab:
        TabBarView:
        TextButton: # 文本 按钮
        TextField: # 文本 输入框
            onChanged:
            onSubmitted:
        TextFormField: # 表单 输入框
            onSaved:
            validator: # 表单 校验
        Theme: # 主题  
            data:
            copyWith():
            of(): # 根据context上下文获取当前theme主题
        ThemeData: # 主题数据
            primarySwatch:
        UserAccountsDrawerHeader:
        showDatePicker(): # 日期选择
        showDialog(): # 对话框
            builder:
        showModalBottomSheet(): # 底部滑动窗口
        showTimePicker(): # 日期选择
    painting: # 样式库
        Alignment: # 对齐
        AssetImage:
        Border: # 边框
        BorderRadius: # 边框圆角
        BorderSide:
        BoxDecoration: # 盒子装饰
        BoxFit:
        BoxShadow: # 盒子阴影
        BoxShape: # 盒子形状
        DecorationImage: # 装饰图片
        EdgeInsets:
        ImageRepeat:
        NetworkImage:
        RadialGradient: # 径向渐变
        StadiumBorder: # 椭圆边框
        TextOverflow: # 文字溢出
        TextSpan:
        TextStyle: # 文字样式
            color:
            fontSize:    
    physics:
    rendering:
        MainAxisAlignment:
    scheduler:
    semantics:
    services:
    widgets: # 控件库（默认导入）
        Align:
        AnimatedWidget:
        AspectRatio: # 宽高比
        BottomNavigationBarItem:
        BuildContext: # 控件构建上下文
        Center: # 居中排列
            child:
        Column: # 垂直排列
        ConstrainedBox: # 约束盒子
        Container: # 容器
        CustomScrollView: # 自定义 滚动视图
        Divider:
        Expanded: # 填充剩余
            flex: # 填充占比
        Flexible:
        Form: # 表单
        FormState: # 表单状态
            save(): # 触发 保存
            validate(): # 触发 校验
        FutureBuilder: # Suspense
        GlobalKey: # 全局key
            currentState:
        GridView: # 网格视图
            build():
        Icon: # 图标
        IconData: # 图标数据
        Image: # 图片
        InheritedWidget: # Provider状态继承 控件基类
        ListView: # 列表视图
            build():
                itemBuilder:
                itemCount:
        Navigator: # 路由器、路由插槽
            of():
            pop():
            pushNamed():
            pushReplacementNamed():
        PageController: # PageView控制器 
        PageView: # 滚动页面视图
            onPageChanged:
        Positioned:
        RichText: # 富文本
        Row: # 水平排列
            mainAxisAlignment: # 主轴排列
        ScrollView: # 滚动视图
        SizedBox: # 固定大小盒子
        SliverAppBar:
        SliverGrid: # 复杂滚动、嵌套滚动网格
            delegate: # 动态生成
            gridDelegate: # 网格属性
        SliverPadding:
        SliverSafeArea:
        Stack:
        State: # 状态，携带生命周期
            build(): # 控件渲染 钩子
            deactivate(): # 控件失活 钩子
            didUpdateWidget(): # 状态更新 钩子
            dispose(): # 状态销毁 钩子
            initState(): # 状态初始化 钩子
            setState(): # 修改状态
        StatefulWidget: # 有状态组件基类
            createState(): # 创建状态
        StatelessWidget: # 无状态组件基类
            build():
        StreamBuilder: # 流式 构造器
        Text: # 文本
            style:
            textDirection:
        TextEditingController:
            addListener():
        Widget: # 控件基类
            createElement():
        Wrap:
        runApp(): # 主程序运行
```


### 组件

- MaterialApp -> Scaffold
- Row -> Container -> Alignment -> Decoration
- ListView、ScrollView、GridView、PageView、CustomScrollView(SliverGrid)
- ConstrainedBox、SizedBox
- Stack、Positioned、Flexible



通过key引用组件State，类似useRef


#### StatelessWidget

无状态组件


#### StatefulWidget

自定义状态组件
分2步创建、和Vue2的data()方法要求返回一个新对象是同一个原理



### 组件样式


Theme 会在应用的 Widget 树中向下传播，这意味着它不仅影响到全局的样式，也能在特定的局部区域中应用不同的主题。Theme向下传递


#### Animation

##### AnimationController
##### AnimationStatus


### 组件通信


#### Prop

构造函数参数传递


#### Provider



### 组件路由

MaterialApp -> Navigator(嵌套) 实现多级路由

#### Navigator



### 状态管理


#### Provider
```javascript
// 定义状态
class CounterModel extends ChangeNotifier {
  int _count = 0;

  int get count => _count; // 公开 getter

  void increment() {
    _count++; // 修改状态
    notifyListeners(); // 通知 UI 更新
  }
}

// 全局注入状态
void main() {
  runApp(
    ChangeNotifierProvider(
      create: (context) => CounterModel(),
      child: MyApp(),
    ),
  );
}

// 使用状态
class CounterScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    final counter = context.watch<CounterModel>(); // 监听状态

    return Scaffold(
      appBar: AppBar(title: Text("Provider 计数器")),
      body: Center(
        child: Text("计数: ${counter.count}", style: TextStyle(fontSize: 24)),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: () => context.read<CounterModel>().increment(), // 触发修改
        child: Icon(Icons.add),
      ),
    );
  }
}
```



# Layui

``

## 基础介绍

开源 Web UI 组件库
- layui.js: 核心模块库
- layui.css: 核心样式库

Layui采用模块化加载，需要layui.use()进行初始化
```js
let layer, form, $, table;

// 初始化模块
layui.use(['layer', 'form', 'jquery', 'table'], function(){
    layer = layui.layer;
    form = layui.form;
    $ = layui.jquery;
    table = layui.table;

    // 你可以在这里初始化页面逻辑
    layer.msg('Layui 模块已加载完毕');
});
```





## 核心内容
```yaml
layui:
    $: # jQuery
    cache:  # 获得 UI 的一些配置及临时缓存信息
    carousel: # 轮播图
        render():
    colorpicker: # 颜色选择器
        render():
            done():
    element: # 选项卡、进度条
    flow: # 无线加载
    form: # 表单
        on():
            submit(filter):
                field: # 表单项    
        render():
    jquery: # jQuery
    laydate: # 日期选择器
        render():
            elem:
            format: # 格式
            type: # 类型
                datetime: # 日期时间
            value: # 默认值    
    layer: # 弹出框
        alert():
        close(): # 关闭，基于inde
        confirm():
        getChildFrame(): # 获取弹出层
        msg(): # 消息弹窗
        open(): # 自定义弹出框
            content:
            end: # 弹出层关闭回调
            title:
            type:
    laypage: # 分页组件（所需外部数据：数据总数、当前页、页大小）
        render():
            count: # 数据总数
            curr: # 
            elem: 
            limit: # 每页显示的条数
            limits: # 可供选择的条数
    laytpl: # 模板引擎
        (template, options): # 模板渲染
            tagStyle:
                modern:
        compile():
        config():
        extendVars():
            include: # 实现引入模板文件
            toDataString:
        render(): # 支持回调，获取渲染后的HTML
    table: # 表格
        checkStatus(): # 基于id，获取表格选中状态
        on(): # 表格事件绑定，基于lay-filter进行元素筛选，lay-event标注事件id
            tool(filter): # 单元格事件
                data: # 行数据
                event: # 事件id
            toolbar(filter): # 工具栏事件，
                config:
                    id: # 表格 id
                event:
        reload(): # 重新加载数据，基于table id 
        render():
            cols: # 表格列定义
                field: # 数据列
                templet: # 自定义列显示（模板语法）
                title: # 标题
            data: # 表格数据
            elem:
            fixed:
            page: # 分页
                groups:
                limit:
                limits:
                prev:
                next:
            parseData: # 解析(转换) url 响应
                code:
                msg:
                count:
                data:
            request: # url 请求参数
                pageName:
                limitName:
            sort:
            toolbar: # 工具栏
            type:
                checkbox:    
            url: # 数据请求url
    tree: # 树形
        render():
    upload: # 文件上传
        render():
            elem:
            url: # 上传url
            done():
    config(): # 全局配置
        base: # 设置用于扩展模块的基础路径
        debug:
        dir:
        version:
    component(): # 创建组件
        config:
        CONST:
        name:
        beforeInit():
        beforeRender():
        extendsInstance():
        events():
        render():
        ---
        cache:
        Class:
        config:
        CONST:
            MOD_NAME: # 组件名称
        index:
        getInst():
        on():
        reload():
        removeInst():
        render(): # 组件渲染，依赖原生dom实例
            elem:
            id:
            show:
        set():
    data(): # localStorage
        key:
        remove:
        value:
    debounce(): # 防抖，函数按指定毫秒延时执行
    define(): # 定义模块
    device(): # 获取浏览器信息
        mobile:
        os:
    disuse():
    each(): # 对象（Array、Object、DOM 对象等）遍历，可用于取代 for 语句
    event(): # 执行自定义模块事件，搭配 onevent 使用
    extend(): # 扩展模块
    factory(): # 用于获取模块对应的 layui.define() 的回调函数
    getStyle(): # 获得一个原始 DOM 节点的 style 属性值
    hint():
    img(): # 图片预加载
    isArray():
    link(): # 动态加载css
    off(): # 用于移除模块相关事件
    onevent(): # 增加自定义模块事件，一般在内置组件中使用。
    sessionData(): # sessionStorage 
    stope(): # 阻止事件冒泡
    throttle(): # 节流，限制函数在指定毫秒内不重复执行
    type(): # 获取基本数据类型和各类常见引用类型
    url(): # url解析对象
        hash:
            href:
            path:
            search:
        pathname:
        search:
    use(): # 加载模块

layui.css:
    layui-bg-red: # 背景颜色
        layui-bg-blue:
    layui-btn: # 按钮
        layui-btn-danger:
        layui-btn-disabled: # 禁用按钮
        layui-btn-normal:
        layui-btn-fluid: # 按钮大小占满整个宽度
        layui-btn-lg: # 按钮大小
        layui-btn-sm:
    layui-carousel:
    layui-container: # 容器，两边带留白
    layui-fluid: # 容器，两边没有留白
    layui-form: # 表单
        layui-form-item: # 表单项 
            layui-form-label: # 表单标签
    layui-icon: # 字体图标
        layui-icon-clear: # 删除图标
        layui-icon-heart-fill: # 心形图标
    layui-inline: # 行内样式
    layui-input: # 输入框
        layui-input-block:
        layui-input-inline:
    layui-layout: # 框体
        layui-layout-admin:
            layui-body:
            layui-footer:
            layui-header:
                layui-logo:
                layui-nav:
            layui-side:
    layui-row: # 栅格布局(12) 行，默认占满整行
        layui-col-space15: # 列之间间隙（1-32），给col中的内容加的（不是col本身）
        layui-col-xs3: # 栅格布局 列 < 768px
        layui-col-sm3:
        layui-col-md3: # >= 992px
        layui-col-lg3: 
        layui-col-xl3: # >=1400px
        layui-col-md-offset4: # 列偏移
    layui-show:
    layui-tab: # 选项卡
        layui-tab-content:
        layui-tab-item:
        layui-tab-title:
    layui-table: # 表格
        lay-even: # 隔行变色
    layui-this:
```

### 模块
```js
/** demo.js **/
layui.define(function(exports){
  // do something
  // 输出 demo 模块
  exports('demo', {
    msg: 'Hello Demo'
  });
});

// 若该模块需要依赖别的模块，则在 `mods` 参数中声明即可：
layui.define(['layer', 'form'], callback);
```

模块系统
- layui.define([mods], callback): 定义模块
    - mods: （可选）用于声明该模块所依赖的模块
    - callback: 即为模块加载完毕的回调函数，它返回一个 exports 参数，用于输出该模块的接口
- layui.use([mods], callback): 使用模块
- layui.extend(settings): 扩展模块
    - settings: 扩展模块的相关配置，如模块名、模块路径等
- layui.disuse()

Layui 定义的模块将会被绑定在 layui 对象下，如：var demo = layui.demo;
每个模块都有一个特定命名，且无法被占用，所以你无需担心模块的命名空间被污染，除非通过 layui.disuse([mods]) 方法弃用已定义的模块


### 组件





### 布局


#### 框体


自带的admin后台布局，侧边栏、头部、身体、尾部


#### 栅格

分为12等分


### 通用

#### 颜色

#### 按钮

#### 图标

#### 动画




### 表单

#### 表单组件

#### 输入框

#### 选择框

#### 复选框

#### 单选框



### 展示

#### 表格

#### 分页

#### 树形表格

#### 导航菜单

#### 基础菜单

#### 选项卡

#### 徽章


### 交互


#### 弹出层


#### 日期与时间选择



#### 上传



### 模板引擎
```yaml
laytpl:
    {{ }}: # js语句
    {{# }}: # 注释标签
    {{= }}: # 转义输出
    {{- }}: # 原文输出。即不对 HTML 字符进行转义
        include: # 引入子模板
```

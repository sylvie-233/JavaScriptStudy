# Layui



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
    cache:  # 获得 UI 的一些配置及临时缓存信息
    carousel:
        render():
    colorpicker:
        render():
            done():
    element: # 选项卡、进度条
    flow: # 无线加载
    form: # 表单
        on():
    jquery:
    laydate: # 日期选择器
        render():
            elem:
    layer: # 弹窗
        alert():
        close():
        confirm():
        msg(): # 消息弹窗
    table: # 表格
        render():
            cols:
            data:
            elem:
    tree:
        render():
    upload: # 文件上传
        render():
            elem:
            url:
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
    layui-carousel:
    layui-container:
    layui-btn: # 按钮
        layui-btn-danger:
        layui-btn-normal:
    layui-form: # 表单
        layui-form-item:
        layui-form-label:
    layui-input: # 输入框
        layui-input-block:
    layui-layout:
        layui-layout-admin:
            layui-body:
            layui-footer:
            layui-header:
                layui-logo:
                layui-nav:
            layui-side:
    layui-row: # 栅格布局
        layui-col-xs3:
    layui-show:
    layui-tab: # 选项卡
        layui-tab-content:
        layui-tab-item:
        layui-tab-title:
    layui-table: # 表格
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


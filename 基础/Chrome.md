# Chrome


## 基础介绍

谷歌浏览器
- 浏览器进程
- 渲染进程
- GPU进程
- 插件进程
- 网络进程


Chrome 采用的是“多渲染进程”架构，即每个标签页（Tab）都可能是一个独立的渲染进程，避免单个网页崩溃影响整个浏览器。


## 核心内容
```yaml
chrome:
    action: # 插件图标、弹出框
        onClicked:
            addListener():
        setBadgeBackgroundColor():
        setBadgeText():
        setIcon():
    alarms: # 定时任务
        onAlarm:
            addListener():
        create():
    bookmarks: # 书签
        create():
        getTree():
        remove():
    clipboard: # 剪切板
    commands: # 命令
        onCommand:
            addListener():
    contextMenus: # 右键菜单
        create():
    devtools: # 开发者工具
        panels:
            create():
    downloads: # 下载
        onChanged:
        download():
    fileSystem: # 文件系统
        chooseEntry():
    history: # 历史
        addUrl():
        deleteUrl():
        search():
    identity: # Google 账号身份验证
        getAuthToken():
        getProfileUserInfo():
    notifications: # 桌面通知
        create():
    permissions: # 权限
        remove():
        request():
    runtime: # 运行时，生命周期、事件
        getManifest():
        onInstalled: 
        onMessage():
            addListener():
    scripting: # 脚本执行
        executeScript():
    storage: # 本地存储
        local:
        sync:
            get():
            set():
    tabs: # 标签页
        captureVisibleTab(): # 截图当前标签页
        create(): # 新建标签
        remove():
        query():
    tts:
    webRequest: # 网络请求
        onBeforeRequest:
            addListener():
    windows: # 窗口
        create():
        getAll():
        update():
```



### JS事件循环

浏览器的事件循环有两个队列：
1. 宏任务队列（Task Queue）：（定时器、动画帧、IO）
    - setTimeout
    - setInterval
    - setImmediate（仅 IE 兼容）
    - requestAnimationFrame
    - I/O 事件
2. 微任务队列（Microtask Queue）：(异步Promise)
    - Promise.then
    - MutationObserver
    - queueMicrotask

执行顺序：
1. 执行主线程任务（同步代码）
2. 执行微任务（Microtasks）
3. 执行一个宏任务（Macrotask）
4. 重复步骤 2 和 3



同步任务 -> 微任务 -> 宏任务

JavaScript 是单线程运行的，采用 事件循环（Event Loop） 处理异步任务：
1. 同步任务 直接执行。
2. 异步任务（如 setTimeout、Promise、网络请求） 进入任务队列。
3. 主线程执行完同步任务后，从 微任务队列 取出执行（如 Promise）。
4. 微任务完成后，执行 宏任务队列（如 setTimeout）。



### V8引擎



### 插件
```yaml
插件目录:
    /icons: # 插件图标
    background.js: # 后台脚本（可选）
    content.js: # 注入网页的脚本（可选）
    manifest.json: # 插件的配置文件（必需）
    options.html: # 配置页面（可选）
    popup.html: # 插件弹出窗口（可选）
```


#### manifest.json
```yaml
manifest.json:
    action:
        default_icon: # 插件图标
        default_popup: # 插件弹出窗口
    background: # background.js后台脚本
        service_worker:
    commands: # CMD命令
    content_scripts: # content.js网页注入脚本
        js:
        matches:
    description:
    manifest_version:
    name:
    permissions:
        activeTab:
        scripting:
        storage:
    version:
```









# Electron

`electron官方文档：https://www.electronjs.org/docs/latest/`
`Electron: P4`


## 基础介绍


入口文件：`main.js`
项目脚手架：`npx create-electron-app`

app -> window -> process
ipcMain -> contextBridge(preload) -> ipcRenderer

- 在preload.js中利用contextBridge暴露的方法操作ipcRenderer与main.js中的ipcMain通信



### electron
```yaml
electron:

```

### electron-build
```yaml
electron-build:
    
```

#### bulid.config
```yaml
package.json:build:
    afterPack:
    appId: # appId
    artifactBuildCompleted:
    asar:
    directories: # 目录
        output: # dist输出目录
    extraFiles:
        from:
        to:
    files:
    nsis:
        oneClick:
    productName:
    win: # windows平台配置
        icon:
        target: 
            nsis:
```




### electron-forge
```yaml
electron-forge:
    import:
    make: # 编译,在 package 的基础上，进一步调用 maker 插件（比如 @electron-forge/maker-squirrel、@electron-forge/maker-zip 等），生成真正可分发给用户的安装包/压缩包
    package: # 打包,项目打包成一个 未安装的应用程序目录，不生成安装程序
    publish:
    start:
```

electron打包工具


#### forge.config.js
```yaml:
forge.config.js:
    packagerConfig: # 打包配置
        asar: # 启用 asar 压缩
        icon: # 应用图标
        ignore: # 忽略文件
        name:
        osxSign:
        osxNotarize:
        overwrite: # 每次打包覆盖旧文件
    rebuildConfig: # 配置 rebuild 原生模块（C++ Addon）的行为
        onlyModules:
    makers: # 生成的安装包类型，每个 maker 是一个插件
        name:
            @electron-forge/maker-squirrel: # .exe 安装包
            @electron-forge/maker-zip: # zip包
        config:
            name: # 安装程序名称
            setupIcon: # 安装程序图标
            loadingGif: # 
    publishers: # 定义 发布渠道
        name:
        config:
            repository:
    buildIdentifier:
    plugins: # 插件（构建工具vite、webpack）
        @electron-forge/plugin-webpack:
            mainConfig:
            renderer:
                config:
                entryPoints:
    hooks: # 钩子函数
        generateAssets: # 打包前生成资源
        prePackage: # 调用 package 前
        postPackage: # package 后
        preMake:
        postMake:
        prePublish:
        postPublish:
```

electron打包配置
package.json 中的 "config.forge" 字段



### electron-fiddle

electron官方编辑器



### electron-updater

electron程序更新





## 核心内容
```yaml
electron:
    common: # 
        nativeImage:
            createFromDataURL():
    main: # 主进程
        BrowserWindow: # 浏览器窗口
            width:
            height:
            webPreferences:
                preload: # 预加载js
            ---
            webContents:
                navigationHistory:
                    goBack():
                    goForward():
                session:
                    on():
                        select-usb-device:
                        usb-device-added:
                        usb-device-removed:
                on():
                    before-input-event:
                openDevTools(): # 打开开发者工具
                postMessage():  
            getAllWindows():
            loadFile():
            loadURL():
            setProgressBar():
        Menu: # 菜单    
            append():
            buildFromTemplate():
            setApplicationMenu():
        MenuItem: # 菜单项
        Tray: # 托盘菜单
        app: # 主应用程序
            addRecentDocument():
            getPath(): # 获取路径
                userData: # 专门给应用存储数据的目录（推荐）
                documents: # 用户文档目录
                downloads: # 下载目录
            on():
                activate:
                ready():
                window-all-closed:
            quit(): # 退出程序
            whenReady(): # 应用程序准备完毕
        dialog: # 弹框
            showOpenDialog():   
        globalShortcut: # 快捷键
            register():
        ipcMain: # 主进程
            handle():
            on():
        nativeTheme: # 主题
            themeSource:
    BaseWindow: # 窗口
        contentView:
            addChildView():
    MessageChannelMain:
        port1:
        port2:
            on():
                message:
            postMessage():
    MessagePortMain: # 通信channel内的port端口
    Notification: # 通知框
        show():
    WebContentsView: # 内容视图
        webContents:
            loadURL():
        setBounds():
    autoUpdater:
    clipboard: # 剪切板
        readText():
        writeText():
    contentTracing:
        startRecording():
        stopRecording():
    contextBridge: # 进程桥
        exposeInMainWorld(): # 暴露接口在浏览器环境中（ipcRenderer -> ipcMain）
    crashReporter:
        start():
    desktopCapturer: # 屏幕截图
    inAppPurchase:
    ipcRenderer: # 渲染进程
        invoke(): # 
        send():
    nativeImage:
    nativeTheme:
    net:
        request():
    netLog:
    parentPort:
    process:
    safeStorage:
    session:
        defaultSession:
        setDisplayMediaRequestHandler():
    webUtils:

electron-updater:
    autoupdater:
        autoDownload:
        checkForUpdates(): # 检查更新
    AppUpdater:
```



### Processes

- main process: 本地运行(node)
- render process：浏览器运行(browser)

Context Isolation: 上下文隔离

contextBridge: `preload.js`，负责编写两个进程的通信API`invoke()/handle()`

ipcRenderer -> contextBridge -> ipcMain

#### ipcMain

主进程nodejs

#### ipcRenderer

渲染进程浏览器


#### contextBridge


### MessageChannelMain

跨进程通信（IPC）双工通信，性能比传统的 ipcMain / ipcRenderer 更高效

#### MessagePortMain


### BrowserWindow

渲染窗口


### Menu

窗口菜单


#### MenuItem
#### Tray

托盘菜单



### Dialog

弹出框

### Notification

通知


### Clipboard 

剪切板


### Shortcut

快捷键


### Net

网络


### Device

设备访问


### Theme

主题

### MultiThreading

多线程worker





### Extension

#### ASAR
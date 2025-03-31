# Electron

`electron官方文档：https://www.electronjs.org/docs/latest/`

## 基础介绍


入口文件：`main.js`


app -> window -> process
ipcMain -> contextBridge(preload) -> ipcRenderer


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
    make:
    package:
    publish:
    start:
```

#### forge.config.js

```yaml:
:
    buildIdentifier:
    hooks:
    makers: [
        {

        }
    ],
    packagerConfig: {
        asar:
        name:
        osxSign:
        osxNotarize: {
            tool:
        }
    },
    plugins:
    publishers:
    rebuildConfig:
```


### electron-fiddle

electron官方编辑器



### electron-updater

electron程序更新





## 核心内容
```yaml
electron:
    BaseWindow: # 窗口
        contentView:
            addChildView():
    BrowserWindow: # 浏览器窗口
        loadFile():
        loadURL():
    Menu: # 菜单    
    MessageChannelMain:
    MessagePortMain:
    Notification:
    WebContentsView: # 内容视图
        webContents:
            loadURL():
        setBounds():
    app:
        on():
            window-all-closed:
        whenReady():
    autoUpdater:
    clipboard: # 剪切板
        writeText():
    contentTracing:
        startRecording():
        stopRecording():
    contextBridge:
        exposeInMainWorld():
    crashReporter:
        start():
    desktopCapturer: # 屏幕截图
    dialog: # 弹框
        showOpenDialog():
    globalShortcut: # 快捷键
        register():
    inAppPurchase:
    ipcMain: # 主进程
        handle():
        on():
    ipcRenderer:
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






### Package

打包



#### electron-updater

electron程序更新




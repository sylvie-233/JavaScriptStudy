# Electron

## 基础介绍


入口文件：`main.js`







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

```javascript
module.export = {
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
}
```


### electron-fiddle

electron官方编辑器



### electron-updater

electron程序更新





## 核心内容

```yaml
electron:
    main:
        app:
            on(): 
                activate:
                window-all-closed:
            quit(): # 应用退出
            whenReady():
        BrowserWindow: 
            height:
            webContents:
                openDevTools():
                send(): # 主进程向渲染进程通信
            webPreferences:
                contextIsolation:
                nodeIntegration:
                preload: # 窗口预加载脚本（Bridge）
            width:
            close():
            getAllWindows(): # 获取所有窗口
            loadFile():
            loadUrl():
            maximize():
            on():
                close:
                hide:
                ready-to-show:
            setMenu(): # 设置菜单栏
        globalShortcut: # 全局快捷键
            register():
        ipcMain:
            handle():
            on():
        Menu: # 菜单
            click:
            label:
            submenu:
                role:
                type:
                    separator:
            popup():
            setApplicationMenu(): # 设置窗口主菜单
    net:
        request():
    renderer:
        contextBridge:
            exposeInMainWorld(): # 定义全局变量（window 可在renderer进程中使用）
        ipcRenderer:
            invoke():
            once():
            removeListener():
            send():
            sendSync():
    dialog:
        showMessageBox():
    shell:
        openExternal():

electron-updater:
    autoupdater:
        autoDownload:
        checkForUpdates(): # 检查更新
    AppUpdater:

window: # 渲染进程全局对象
    document: # DOM
    localStorage:
    sessionStorage:
        setItem():
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




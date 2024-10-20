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

```
:
    afterPack:
    appId:
    artifactBuildCompleted:
    asar:
    directories:
        output:
    extraFiles: [
        {
            from:
            to:
        }
    ],
    files: [],
    nsis:
        oneClick:
    productName:
    win:
        icon:
        target: [
            {
                target: "nsis"
            }
        ]
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



## 核心内容

```yaml
electron:
    main:
        app:
            on(): "activate|window-all-closed"
            whenReady():
        BrowserWindow:
            "close|hide|ready-to-show"
            height:
            webContents:
                openDevTools():
                send():
            webPreferences:
                contextIsolation:
                nodeIntegration:
                preload: 窗口预加载脚本
            width:
            close():
            getAllWindows():
            loadFile():
            loadUrl():
            maximize():
            setMenu():
        ipcMain:
            handle():
    renderer:
        contextBridge:
            exposeInMainWorld(): 定义全局变量
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

```

### Processes

- main process: 本地运行
- render process：浏览器运行

Context Isolation: 上下文隔离










### Package



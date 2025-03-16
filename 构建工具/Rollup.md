# Rollup


## 基础介绍

javascript构建工具
目标构建ESM


### rollup
```yaml
rollup:
    -i:
    -v:
    --config:
    --dir:
    --environment:
    --file:
    --format:
    --help:
    --plugin:
    --watch:
```

#### rollup.config.js
```yaml
rollup.config.js:
    external:
    input:
    output:
        banner:
        file:
        format:
        name:
        plugins:
    plugins:
```


## 核心内容
```yaml
rollup:
    PartialResolveId:
    Plugin: # 核心插件对象
        name:
        buildEnd():
        buildStart(): # HOOK 插件初始化配置
        closeWatcher():
        generateBundle():
        load():
        moduleParsed():
        options(): # HOOK 配置预处理
        renderChunk():
        renderEnd():
        renderStart():
        resolveId(): # HOOK 插件解析核心逻辑
        resolveDynamicImport():
        transform():
        watchChange():
        writeBundle():

@rollup:
    plugin-alias:
        alias:
            entries:
    plugin-commonjs:
    plugin-json:
        json():
    plugin-node-resolve:
        resolve():
    plugin-replace:

rollup-plugin-terser: # 代码压缩
    terser:
```



### 插件
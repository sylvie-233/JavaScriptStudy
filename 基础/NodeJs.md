# NodeJs





## 基础介绍


### node
```yaml
node:
    -v: 版本
```


### npm
```yaml
npm:
    -v: 版本
    init: 初始化项目
    install: 安装
        -g: 全局安装
        --registry: 仓库
```

### package.json
```
{

}
```



## 核心内容


## 标准库

```
std:
    builtin:
        __dirname: 目录名
        __filename: 文件名
        console:
        module: 模块
            exports: 模块导出对象
        process: 进程对象
            env: 环境变量
            cwd(): 当前工作目录
        Buffer: 二进制对象
            toString(): 转换为字符串
        Error: 错误对象
        JSON:
            stringify(): json字符串序列化
        Object:
            assign(): 对象赋值
        clearInterval(): 清除定时器
        require(): 导入函数
        setInterval(): 间隔定时器
        setTimeout(): 定时器
    crypto: 加密包
    events: 事件
        EventEmitter:
            emit(): 触发事件
            on(): 监听事件
            once(): 
    fs:
        createReadStrem(): 创建读取流
        readFileSync(): 读取文件
        writeFileSync(): 写入文件
    http:
        Server: 服务
        createServer(): 创建服务
    net:
        Server: 服务
    path:
        resolve(): 路径合并
    util: 工具包
    zlib: 压缩包
        createGzip():
```


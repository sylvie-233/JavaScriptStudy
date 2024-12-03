# NodeJs

`尚硅谷Node.js零基础视频教程: P14`

## 基础介绍

![NodeJs运行机制](../assets/NodeJs运行机制.png)


### node
```yaml
node:
    -v: 版本
```

nodejs命令行工具


### npm
```yaml
npm:
    -v: # 版本
    init: # 初始化项目
    install: # 安装
        -g: # 全局安装
        --registry: # 仓库
```

nodejs包管理器




#### package.json
```yaml
```

nodejs包配置文件




### nvm

nodejs版本管理器




## 核心内容
```yaml
node:
    _builtin:
        __dirname: 目录名
        __filename: 文件名
        console: # 控制台对象
            log:
        global: # 全局对象
        globalThis:
        module: # 模块对象
            children:
            exports: # 模块导出对象
            filename:
            id:
            loaded:
            parent:
            path:
            paths:
        process: # 进程对象
            argv:
            channel:
            env: # 环境变量
            stderr:
            stdin: # 标准输入
            stdout: # 标准输出
            exit(): # 进程结束
            nextTick():
        Buffer: # 二进制对象（大小固定）
            length:
            alloc(): # 直接分配内存创建Buffer
            allocUnsafe(): # 未初始归零分配
            concat():
            from(): # 由String创建Buffer
            slice():
            toString(): # 转换为字符串
            write(): 
        Error: # 错误对象
        JSON:
            parse():
            stringify(): # json字符串序列化
        Object: # 基类对象
            assign(): # 对象赋值
        Promise:
            all():
        Proxy:
            get():    
            set():
        clearInterval(): # 清除定时器
        require(): # 导入函数
        setInterval(): # 间隔定时器
        setTimeout(): # 定时器
    assert:
    buffer:
    child_process: # 子进程
    cluster:
    crypto: # 加密包
    dgram:
    dns:
    domain:
    events: # 事件
        EventEmitter:
            emit(): 触发事件
            listeners():
            on(): 监听事件
            once(): 
    fs: # 文件操作
        promises:
        appendFile():
        close():
        createReadStream(): 创建读取流
        createWriteStream():
        existsSync(): # 文件存在
        open():
        readFile():
        readFileSync(): 读取文件
        writeFile():
        writeFileSync(): 写入文件
    http:
        Server: 服务
            listen():
        createServer(): 创建服务
    https:
    net:
        Server: 服务
    os: # 操作系统
    path: # 路径操作
        resolve(): 路径合并
    process: # 进程对象
    querystring:
    readline:
        Interface:
            close():
            on():
                _close:
                _line: # 输入一行
            prompt(): # 输出提示信息
            question():
            setPrompt():
        createInterface():
            input:
            output:
    stream:
        pipeline:
        Readable:
            on():
                data:
                end:
                readable:
            pipe():
        Transform:
            _flush():
            _transform():
        Writeable:     
    string_decoder:
    timers:
    tls:
    tty:
    url:
    util: # 工具包
    worker_threads: # 工作线程
        workerData:
        parentPort:
            PostMessage():
    zlib: # 压缩包
        createGzip():
        
```

### 异步模块

![Nodejs异步模块](../assets/Nodejs异步模块.png)


promise、async

- 定时器
- I/O操作
- Node内置


<br />
<br />



### 事件循环

事件循环：
![NodeJS事件循环](../assets/NodeJS事件循环.png)



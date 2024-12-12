# NodeJs

`尚硅谷Node.js零基础视频教程: P55`

## 基础介绍

![NodeJs运行机制](../assets/NodeJs运行机制.png)

- %NODE_PATH%：nodejs主目录
- %NODE_PATH%/node_cache
- %NODE_PATH%/node_global
- %NODE_PATH%/node_modules:



### node
```yaml
node:
    -v: 版本
    --env-file:
    --test:
```

nodejs命令行工具


### npm
```yaml
npm:
    -v: # 版本
    config:
        edit:
        get:
        list:
        set:
            cache:
            prefix:
            registry:
    init: # 初始化项目
        -y:
    install: # 安装
        -g: # 全局安装
        --no-save:
        --registry: # 仓库
    uninstall:
```

nodejs包管理器




#### package.json
```yaml
package.json:
    
```

nodejs包配置文件


#### npx



### nvm
```yaml
nvm:

```

nodejs版本管理器




## 核心内容
```yaml
node:
    _builtin:
        __dirname: # 目录名
        __filename: # 文件名
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
            memoryUsage():  # 内存使用情况
            nextTick():
            on(): # 监听进程信号signal
            once():
                SIGINT:
                SIGTERM:
                uncaughtException:
                unhandledRejection:
        Array:
            forEach():
            push():
        Buffer: # 二进制对象（大小固定）
            length: # 长度
            alloc(): # 直接分配内存创建Buffer
            allocUnsafe(): # 未初始归零分配
            concat():
            from(): # 由String创建Buffer
            slice():
            toString(): # 转换为字符串
            write(): 
        Date: # 日期
            now():
        Error: # 错误对象
        JSON:
            parse():
            stringify(): # json字符串序列化
        Number:
        Object: # 基类对象
            assign(): # 对象赋值
            defineProperty():
                configurable:
                enumerable:
                get():
            getPrototypeOf():
            setPrototypeOf():
        Promise:
            all():
            resolve():
        Proxy:
            get():    
            set():
        String:
            split():
        URL:
            pathname:
            searchParams:
        clearInterval(): # 清除定时器
        require(): # 导入函数
        setInterval(): # 间隔定时器
        setTimeout(): # 定时器
    assert:
        assert():
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
        ReadStream: # 读入流
            on():
                _close:
                _data:
                _end:
            pipe(): # 管道传输
        WriteStream: # 写出流
            end():
            write():
        appendFile(): # 追加内容
        close():
        createReadStream(): # 创建读取流
        createWriteStream():
        existsSync(): # 文件存在
        mkdir(): # 创建文件夹
            _options:
                recursive: # 递归创建
        open():
        readdir(): # 读取目录
        readFile(): # 读取文件
        readFileSync(): # 读取文件（同步）
        rename(): # 文件重命名
        rm():
        rmdir():
            _options:
                recursive:
        stat(): # 文件信息
            atime:
            ctime:
            isDirectory():
            isFile():
        unlink(): # 删除文件
        writeFile(): # 写入文件
            _options:
                flag:
                    a: # 追加
        writeFileSync(): # 写入文件(同步)
    http:
        Request:
            headers:
            httpVersion:
            method:
            pathname:
            query:
            url:
            on():
                data:
                end:
        Response:
            statusCode: # 响应状态码
            statusMessage:
            end():
            setHeader(): # 设置响应头
            write(): # 响应体
        Server: # http服务
            listen():
        createServer(): # 创建http服务
    https:
    worker_threads: # 工作线程
        workerData:
        parentPort:
            PostMessage():
    net:
        Server: # 服务
            listen():
            on():
                _connection:
                _data:
                _error:
            
        Socket:
            setEncoding:
            connect(): # socket连接
            destroy():
            end():
            on():
                _data:
                _error:
            write():
        createServer():
    os: # 操作系统
    path: # 路径操作
        sep:
        basename:
        extname():
        dirname():
        join():
        parse():
            base:
            name:
            root:
        resolve(): # 路径合并
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
            on():
            write(): 
    string_decoder:
    test:
        describe():
        it():
    timers:
    tls:
    tty:
    url:
        Url:
        parse(): # 解析url
    util: # 工具包
        inspect():
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



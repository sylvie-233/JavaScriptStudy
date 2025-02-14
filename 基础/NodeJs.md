# NodeJs

`Nodejs官方文档：https://nodejs.org/en/learn/getting-started/introduction-to-nodejs`

`尚硅谷Node.js零基础视频教程: P55`
`小满Node.js：P43`

## 基础介绍

![NodeJs运行机制](../assets/NodeJs运行机制.png)

- %NODE_PATH%：nodejs主目录
- %NODE_PATH%/node_cache：
- %NODE_PATH%/node_global：
- %NODE_PATH%/node_modules：



### node
```yaml
node:
    -v: # 版本信息
    --env-file:
    --experimental-strip-types:
    --test:
    --watch:
```

nodejs命令行工具



#### package.json
```yaml
package.json:
    author:
    description:
    dependencies: # 项目依赖
    devDependencies: # 开发依赖
    license:
    main: # 入口文件
    module:
    peerDependencies: # 对等依赖
    name: # 包名
    repository:
        type:
            git:
        url:
    scripts: # 运行脚本
        pos_:
        pre_:
        clean:
        dev:
        start:
        test:
    version:
```

nodejs包配置文件


### npm
```yaml
npm:
    -v: # 版本
    add: # 添加本地路径映射（包）
    config:
        edit:
        get:
            registry:
        list: # 查看所有配置项
        set:
            cache: # 缓存路径
            prefix: # 全局软件下载路径
            registry:
    homepage:
    init: # 初始化项目
        -y:
    install: # 安装第三方包
        -D:
        -g: # 全局安装
        --no-save:
        --registry: # 仓库
        --save: # 包依赖
        --save-dev: # 开发依赖
    link:
    list:
        -g:
    publish: # 发布包
    run: # 运行脚本
    uninstall: # 卸载第三方包
```

nodejs包管理器

需要手动安装

npm私服




#### .npmrc

局部npm配置文件


#### npx
#### nvm
```yaml
nvm:
    alias:
    install:
    list:
        avaliable:
    uninstall:
    use:
```

nodejs版本管理器




## 核心内容
```yaml
node:
    _builtin:
        __dirname: # 目录名
        __filename: # 文件名
        console: # 控制台对象
            log():
        global: # 全局对象（windows）
        globalThis: # 兼容浏览器的全局对象
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
            argv: # 进程运行参数
            channel:
            env: # 环境变量
            stderr:
            stdin: # 标准输入
            stdout: # 标准输出
            cwd(): # 进程运行目录
            exit(): # 进程结束
            memoryUsage():  # 内存使用情况
            nextTick():
            on(): # 监听进程信号signal
            once():
                exit:
                SIGINT:
                SIGTERM:
                uncaughtException:
                unhandledRejection:
        Array:
            forEach():
            push():
        Blob:
            text():
        BroadcastChannel:
            onmessage:
            postMessage():
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
        Math:
            PI:
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
            repeat():
            split():
        URL:
            pathname:
            searchParams:
        clearInterval(): # 清除定时器
        fetch():
        require(): # 导入函数
        setInterval(): # 间隔定时器
        setTimeout(): # 定时器
    assert:
        assert():
        deepEqual():
        deepStrictEqual():
        doesNotMatch():
        doesNotReject():
        doesNotThrow():
        ok():
    buffer:
        isUtf8():
        transcode():
    child_process: # 子进程(执行子命令)
        exec(): # 执行命令行
        execFile(): # 执行文件
        execSync():
        fork(): # 运行js模块（返回js进程）
            send():
        spawn():
        spawnSync():
            cwd:
    cluster:
    crypto: # 加密包
        Cipher:
            final():
            update():
        Decipher:
            final():
            update():
        Hash:
            copy():
            digest():
            update(): 
        createCipheriv():
        createDecipheriv():
        createHash():
        generateKeyPairSync():
        hash():
        privateDecrypt(): # 私钥解密
        publicEncrypt(): # 公钥加密 
        randomBytes():
    dgram: # UDP
        Socket:
        createSocket():
    dns:
    domain:
    events: # 事件
        EventEmitter:
            emit(): # 触发事件
            listeners():
            off():
            on(): # 监听事件
            once(): 
            setMaxListeners():
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
            on():
                finish:
            write():
        appendFile(): # 追加内容
        close():
        createReadStream(): # 创建读取流
        createWriteStream():
        existsSync(): # 文件存在
        link():
            
        mkdir(): # 创建文件夹
            recursive: # 递归创建
        open():
        readdir(): # 读取目录
        readFile(): # 读取文件
            encoding:
                utf-8:
            flag:
                r:
        readFileSync(): # 读取文件（同步）
        rename(): # 文件重命名
        rm():
        rmdir():
            _options:
                recursive:
        rmSync():
            recursive:
        stat(): # 文件信息
            atime:
            ctime:
            isDirectory():
            isFile():
        symlink():
        unlink(): # 删除文件
        watch(): # 监听文件变化
        writeFile(): # 写入文件
            flag:
                a: # 追加
        writeFileSync(): # 写入文件(同步)
    http:
        Request:
            headers:
            httpVersion:
            method: # 请求方法
            pathname:
            query: # query param
            url: # request url
            on():
                data:
                end:
        Response:
            statusCode: # 响应状态码
            statusMessage:
            end():
            setHeader(): # 设置响应头
            write(): # 响应体
            writeHead():
        Server: # http服务
            listen():
        createServer(): # 创建http服务
    https:
    net:
        BlockList:
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
        SocketAddress:
        connect():
        createConnection():
        createServer():
        isIP():
    os: # 操作系统
        arch():
        cpus():
            model:
            speed:
            times:
        homedir(): # 用户主目录
        networkInterfaces(): # 网络信息
        platform():
        release():
        type():
        version():
    path: # 路径操作
        posix:
        win32:
        sep:
        basename(): # 基础文件名
        extname(): # 文件扩展名
        dirname(): # 目录名
        format(): # 合成路径 
        join(): # 路径合并
        parse(): # 解析路径
            base:
            dir:
            ext:
            name:
            root:
        resolve(): # 路径解析（返回绝对路径）
    process: # 进程对象（全局）
        arch:
        argv: # 进程参数
        env: # 环境变量
            NODE_ENV:
        pid:
        platform:
        cwd(): # 进程运行路径
        exit():
        kill():
        memoryUsage():
        on(): # 监听进程事件
            exit:
            message():
    querystring: # url query解析
        decode():
        encode():
        parse():
        stringify():
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
        web:
            ReadableStream:
                start():
                    close():
                    enqueue():
            TransformStream:
                transform():
            WritableStream:
                write():
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
            pathname:
        parse(): # 解析url
    util: # 工具包
        type:
        callbackify():
        format(): # 格式化字符串
        inspect():
        promisify(): # 回调函数转promise函数
    worker_threads: # 工作线程
        workerData:
        parentPort:
            PostMessage():
    ws:
        Websocket:
            on():
                close:
                message:
                open:
            send():
    zlib: # 压缩包
        createDeflate():
        createGunzip():
        createGzip():
        createInflate():
        deflateSync():
        gzipSync():
```


### 数据类型
```yaml
DataTypes:
    Array:
    BigInt:
    Boolean:
    Function:
    Null:
    Number: # 数值
    Object:
    String:
    Symbol:
    Undefined:
```



### 控制流程



### 面向对象


### 模块

CommonJs、Module

require()支持引入json



### 异步

![Nodejs异步模块](../assets/Nodejs异步模块.png)


promise、async

- 定时器
- I/O操作
- Node内置


<br />
<br />


### 运行机制

#### 事件循环

事件循环：
![NodeJS事件循环](../assets/NodeJS事件循环.png)



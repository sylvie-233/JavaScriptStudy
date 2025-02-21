# NodeJs

`Nodejs官方文档：https://nodejs.org/en/learn/getting-started/introduction-to-nodejs`
`npm包官网：https://www.npmjs.com/`

`尚硅谷Node.js零基础视频教程: P193`
``

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
    --env-file: # 指定加载.env文件
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
    scripts: # 自定义运行脚本
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
            registry: # 镜像仓库url
    homepage:
    init: # 初始化项目
        -y:
    install: # 安装第三方包
        -g: # 全局安装
        -D: # 开发依赖
        -S: # 项目依赖
        --no-save:
        --registry: # 指定下载镜像仓库
        --save: # 包依赖
        --save-dev: # 开发依赖
    link:
    list: # 列出已安装包
        -g:
    login: # 登录npmjs官网
    publish: # 发布包
    remove: # 删除包
    root: # 查看项目node_modules路径
        -g: # 全局node_modules路径
    run: # 运行脚本
    search: # 搜索包
    uninstall: # 卸载第三方包
    unpublish:
```

nodejs包管理器

需要手动安装

npm私服




#### .npmrc

配置文件：
- `安装目录/node_modules/npm/npmrc`：安装配置文件
- `~/.npmrc`：用户配置文件
- `.npmrc`：项目配置文件

npm配置文件


#### npx
#### nvm
```yaml
nvm:
    alias: # 版本别名
    install:
        latest:
    list:
        avaliable:
    uninstall:
    use: # 使用版本
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
            arguments: # module底层执行包裹函数 function(exports, require, module, __filename, __dirname)
                callee:
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
            sort(): # 排序（可传入比较函数实现自定义排序）
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
            cause: # 错误原因
            code: # 错误码
            message: # 错误信息
            stack: # 错误函数栈
        JSON:
            parse():
            stringify(): # json字符串序列化
        Math: # 数学运算
            E:
            PI:
            abs():
            max():
            min():
            pow():
            random():
            round():
            sqrt():
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
            slice(): # 字符串截取
            split():
        URL: # url对象
            pathname: # url 路径
            searchParams:
        URLSearchParams: # 
        clearInterval(): # 清除定时器
        fetch(): # ajax请求 promise风格
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
        spawn(): # 启动子进程（返回进程对象）
            stderr:
                on():
                    data:
            stdout:
                on():
                    data:
            on():
                close:
        spawnSync():
            cwd:
    cluster: # 集群（多核系统中创建多个nodejs进程）
        isPrimary: # 主进程判断
        fork(): # 创建子进程
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
    errors: # 错误/异常
        Error: # 异常基类
        SyntaxError: # 语法错误
        SystemError:
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
        Request: # http 请求
            headers:
            httpVersion:
            method: # 请求方法
            pathname:
            query: # query param
            url: # request url 请求url
            on():
                data:
                end:
        Response: # 响应
            statusCode: # 响应状态码
            statusMessage:
            end(): # 结束响应
            setHeader(): # 设置响应头
            write(): # 响应体
            writeHead():
        Server: # http服务
            listen():
            on():
                request:
        createServer(): # 创建http服务
            options: # 服务配置
            requestListener: # 处理回调函数
                req:
                res:
    https:
    net:
        BlockList:
        Server: # 服务
            listen(): # 监听端口
            on():
                connection:
                data:
                error:
            
        Socket:
            setEncoding:
            connect(): # socket连接
            destroy():
            end():
            on():
                data: # 接收消息
                error:
            write(): # 发送消息
        SocketAddress:
        connect():
        createConnection(): # 创建socket客户端
            host:
            port:
        createServer(): # 创建socket服务端
            socket:
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
    Error:
    Function:
    Map:
    Null:
    Number: # 数值
    Object:
    Set:
    String:
    Symbol:
    Undefined:
```

#### String

字符串


### 控制流程
```yaml
Control Flow:
    if ... else if ... else ...:
```

#### 异常处理
```javascript
// 捕获异常
try {
    ...
} catch (e) {
    ...
} finallly {
    ...
}

// 抛出异常
thorw new Error("xxx")
```


### 面向对象
```javascirpt

```


### 模块
```javascript
// 导入模块
const xxx = require("xxx")

// 导出模块
module.exports = {
    xxxx
}
exp
```

CommonJs、ES Module

防止命名冲突、高复用性、高维护性

require() 导入缓存、只会执行一次

require()支持引入`js`、`json`、`.node`扩展
js文件优先级高
require()中的相对路径是相对文件本身、不会受到工作目录影响

require()导入文件夹、会导入文件夹下的package.json中main属性指向的文件，否则导入index.js文件



### 异步

![Nodejs异步模块](../assets/Nodejs异步模块.png)


promise、async

- 定时器
- I/O操作
- Node内置


<br />
<br />


### 事件循环

libuv库

事件循环：
![事件循环](../assets/事件循环.png)
![NodeJS事件循环](../assets/NodeJS事件循环.png)

回调函数执行顺序问题

宏任务、微任务
微任务：`process.nextTick()`、`Promise`



## node-gyp
```yaml
node-gyp:
    configure:
```

使用C++编写nodejs扩展：`.node`，动态库

`NAPI`、`NODE_API_MODULE()`

### binding.gyp
```yaml
binding.gyp:
    targets:
        include_dirs:
        source:
        target_name:
```
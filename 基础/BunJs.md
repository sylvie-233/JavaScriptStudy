# Bun


## 基础介绍

现代的JavaScript运行时、原生TypeScript支持、内置打包工具、内置的 HTTP 服务器
Zig 语言编写的 JavaScript 全栈工具链
- 运行时 (Runtime)
- 打包器 (Bundler)
- 测试框架 (Test Runner)
- 包管理器 (Package Manager)


- 自动加载.env文件





### 项目结构
```yaml
bun:
    /node_modules:
        /bun-types:
            package.json:
            README.md:
            tsconfig.json:
            types.d.ts:
    .gitignore:
    bun.lockb: # bunjs版本锁
    index.ts:
    package.json:
    README.md:
    tsconfig.json:
```

### bun
```yaml
bun:
    --hot: # 热更新
    --version: # 版本
    --watch: # 热重载
    add: # 添加依赖
        --dev:
        --save:
    build: # 构建打包
        --entrypoints:
        --minify:
        --outdir:
        --sourcemap:
        --target:
    create: # 使用模板创建项目
    init: # 初始化项目
    install: # 安装依赖
        -w: # 指定workspace工作空间
    link:
    remove: # 移除依赖
    run: # 运行
        --filter:
        --hot:
    test: # 测试
    unlink:
    upgrade: # 升级bun
bunx:
```






## 核心内容
```yaml
bun:
    _Globals:
        AbortController:
        AbortSignal:
        ArrayBuffer:
        Blob:
        CloseEvent:
        Crypto:
        Event:
        File:
        FormData:
        TextDecoder:
        TextEncoder:
        Uint8Array:
        URL:
        URLSearchParams:
        fetch():
    ffi:
    jsc:
    sqlite: # sqlite3
        Database: # 数据库
            exec():
            query():
        Statement:
            all():
    test: # 测试
        beforeEach():
        describe(): # 分组
        expect(): # 断言
            toBe():
        test(): # 测试
    Bun: # 内建模块
        build:
        env: # 环境变量
        file():
    BunFile:
    serve():
        port:
        error():
        fetch():
        ---
    sleep(): # 睡眠
node: # nodejs兼容
    assert:
    async_hooks:
    buffer:
    child_process:
    cluster:
    crypto:
    dgram:
    diagnostics_channel:
    dns:
        promises:
    events:
    fs:
        promises:
    http:
    http2:
    https:
    inspector:
        promises:
    module:
    net:
    os:
    path:
    perf_hooks:
    punycode:
    querystring:
    readline:
        promise:
    stream:
        consumers:
        promises:
        web:
    string_decoder:
    test:
        reporters:
    timers:
        promises:
    tls:
    trace_events:
    tty:
    url:
    util:
        types:
    v8:
    vm:
    wasi:
    worker_threads:
    zlib:
```
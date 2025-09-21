# Bun


## 基础介绍

现代的JavaScript运行时、原生TypeScript支持、内置打包工具、内置的 HTTP 服务器



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
    bun.lockb:
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
    build:
    create: # 使用模板创建项目
    init: # 初始化项目
    install:
    link:
    remove:
    run: # 运行
        --hot:
    test:
    unlink:
    upgrade: # 升级bun
bunx:
```






## 核心内容
```yaml
bun:
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
    
```
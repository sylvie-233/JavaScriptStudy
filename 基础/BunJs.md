# Bun


## 基础介绍

现代的JavaScript运行时、原生TypeScript支持、内置打包工具、内置的 HTTP 服务器

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
    --version:
    --watch: # 热重载
    add:
    build:
    create: # 使用模板创建项目
    init: # 初始化项目
    install:
    link:
    unlink:
    remove:
    run: # 运行
        --hot:
    test:
bunx:
```






## 核心内容
```yaml
bun:
    Bun: # 内建模块
        build:
        file():
    test:
        describe():
        expect():
        test():
    BunFile:
    serve():
        port:
        error():
        fetch():
        ---
node: # nodejs兼容
    
```
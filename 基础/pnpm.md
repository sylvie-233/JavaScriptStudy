# pnpm

## 基础介绍

优化版npm
pnpm使用硬链接和符号链接来共享依赖库，避免重复的依赖安装，从而大大减少了项目的磁盘占用
- 支持非扁平的node_modules目录


### pnpm
```yaml
pnpm:
    --version:
    add: # 添加依赖
        --dev:
        --peer: 
        --workspace-root:
    alias:
    env: 
    exec: # 直接运行npm脚本
    init: # 初始化、生成package.json
    init-workspace: # 初始化工作区
    install: # 安装依赖
    list: # 列出已安装依赖
    patch:
    publish: # 发布包
    remove: # 移除依赖
        --dev:
    run: # 运行npm脚本
        --filte:
    set: # 修改配置
        registry:   
    store:
        path: # 查看缓存的路径
        prune: # 清理store空间
        status:
    update: # 更新依赖
```


#### pnpm-workspace.yaml
```yaml
pnpm-workspace.yaml:
    packages: # 多个项目路径
```


## 核心内容


### monorepo

npm版Maven多项目管理工具

Monorepo（单一代码库）是一种软件开发策略，将多个项目或模块存储在同一个代码库中，而不是为每个项目单独创建代码库。

工作区可以减少重复的依赖安装，并优化版本控制

# Verdaccio


## 基础介绍

npm私服

默认4873端口


`VERDACCIO_STORAGE_PATH`：配置存储位置
`.verdaccio-db`：JSON数据库

支持nodejs直接调用运行


### verdaccio
```yaml
verdaccio:
    --config: # 配置文件
    --info: # 打印本地环境信息
    --listen: # 端口监听
    --version:
```

运行命令行工具


#### verdaccio.yaml
```yaml
verdaccio.yaml:
    auth:
    https:
    listen:
    log:
    packages: # 控制软件包的访问方式
    plugins: # 插件
    security:
    server:
    storage: # 存储
    uplinks: # 上行链路
    web:
```

配置文件


## 核心内容


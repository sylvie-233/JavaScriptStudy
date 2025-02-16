# nacos

## 基础介绍

操作nacos注册中心


## 核心内容
```yaml
nacos:
    NacosConfigClient:
        serverAddr:
        ---
        getConfig():
        publishSingle():
        remove(): 
        subscribe():
    NacosNamingClient:
        namespace:
        serverList:
        ---
        ready():
        registerInstance(): # 注册服务
```
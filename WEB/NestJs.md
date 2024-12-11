# NestJs

``

nodejs 服务端框架

## 基础介绍

- `@nestjs/core`
- `@nestjs/common`
- `rxjs`
- `reflect-metadata`



module -> imports     ->
       -> controllers(控制器)
       -> providers   -> services(服务实现)





### 项目结构
```yaml
project:
    src:
        app.controller.spec.ts:
        app.controller.ts:
        app.module.ts:
        app.service.ts:
        main.ts:
```

### nest
```yaml
nest:
    new: # 新建项目
```


## 核心内容
```yaml
@nestjs/common:
    @Get: # http get 请求
    @Controller: # 控制器
    @Injectable: # 依赖注入
    @Mudule: # 模块
    INestApplication: # nest主应用类
        listen(): # 监听端口

@nestjs/core:
    NestFactoroy:
        create(): # 创建应用实例(根据Module)

@nestjs/testing:
    Test:
    TestingModule:
```


### Controller


### Provider


### Module


### Middleware


### Exception Filter


### Pipe


### Guard


### Interceptors


### Custom Decorator
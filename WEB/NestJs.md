# NestJs

``

nodejs 服务端框架

## 基础介绍

- `@nestjs/core`
- `@nestjs/common`
- `rxjs`
- `reflect-metadata`



module -> imports(导入其它模块)
       -> controllers(控制器)
       -> providers   -> services(服务实现)

一个项目project 可以有多个 模块module




### 项目结构
```yaml
project:
    /src:
        app.controller.spec.ts:
        app.controller.ts:
        app.module.ts:
        app.service.ts:
        main.ts:
    /test:
    nest-cli.json:
    package.json:
    tsconfig.json:
```

### nest
```yaml
nest:
    build:
    g: # 生成文件
        module:
    new: # 新建项目
    start:
        --watch:
```


## 核心内容
```yaml
@nestjs/common:
    @Body: # request body
    @Catch:
    @Delete:
    @Get: # http get 请求
    @Controller: # 控制器
    @Ip:
    @Injectable: # 依赖注入
    @Mudule: # 模块
        controllers:
        exports:
        providers:
            provider:
            useClass: # Guard
    @Param: # path param
    @Patch:
    @Post:
    @Query: # query param
    ConsoleLogger:
    HttpException:
    HttpStatus:
    INestApplication: # nest主应用类
        enableCors():
        get(): # 手动获取依赖
        listen(): # 监听端口
        setGlobalPrefix():
        useGlobalFilters():
        useLogger():
    NotFindException:
    OnModuleInit:
    ParseIntPipe:
    ValidationPipe:

@nestjs/core:
    APP_GUARD:
    BaseExceptionFilter: # 异常捕获
    NestFactoroy:
        create(): # 创建应用实例(根据Module)
            logger:

@nestjs/mapped-types:
    PartialType():

@nestjs/testing:
    Test:
    TestingModule:

@nestjs/throttler: # 速率限制
    @SkipThrottle:
    @Throttle:
    ThrottlerGuard:
    ThrottlerModule:
        forRoot():
            limit:
            ttl:

@prisma/client: # orm
    Prisma:
        _modelCreateArgs:
    PrismaClient:
        _model:
            create():
                data:
            delete():
            findMany():
                where:
            findUnique():
            update():
        $connect:

class-validator: # 数据验证(DTO)
    @IsEmail:
    @IsEnum:
        message:
    @IsNotEmpty:
    @IsString:

express:
    Request:
    Response:
```


### Controller


### Provider

依赖注入对象





### Module


### Middleware


### Exception Filter


### Pipe

数据处理通道，类似中间件

数据转换、数据验证



### Guard


### Interceptors


### Custom Decorator
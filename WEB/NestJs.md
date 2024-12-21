# NestJs

`Nest.js官方文档：https://docs.nestjs.com/pipes`

nodejs 服务端框架

## 基础介绍

- `@nestjs/core`
- `@nestjs/common`
- `rxjs`
- `reflect-metadata`
- `@nestjs/platform-express`
- `@nestjs/platform-fastify`




module -> imports(导入其它模块)
       -> controllers(控制器)
       -> providers   -> services(服务实现)

一个项目project 可以有多个 模块module，模块module之间可以相互依赖嵌套




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
    g: # 生成代码文件
        controller: # 控制器
        module: # 模块
        resource:
        service: # CRUD resource router
    new: # 新建项目
    start:
        --watch:
```


## 核心内容
```yaml
@nestjs/common:
    @All: # all request method
    @Body: # request body
    @Catch: # 异常捕获过滤器
    @Delete:
    @Get: # http get 请求
    @Global: # 全局模块
    @Controller: # 控制器
        host:
    @Header: # 设置响应头
    @Headers:
    @HostParam: # controller host param
    @HttpCode: # 响应状态码
    @Ip:
    @Injectable: # 依赖注入
    @Mudule: # 模块
        controllers:
        exports: # 导出provider、module
        imports:
        providers:
            provide: # 自定义注册（不使用@Injectable）
                APP_FILTER:
                APP_GUARD:
            useClass: # 
    @Next:
    @Optional:
    @Param: # path param
    @Patch:
    @Post: # post request
    @Query: # query param
    @Redirect: # 响应重定向
        url:
        statusCode:
    @Req: # 请求对象
    @Res: # 响应对象
        passthrough:
    @Session:
    @UseFilters: # 使用异常处理过滤器
    @UseGuards: # 使用请求守卫
    @UseInterceptors:
    @UsePipes: # 使用数据管道
    ArgumentMetadata:
    ArgumentsHost:
        switchToHttp():
            getResponse():
            getRequest():
    CanActivate: # 请求拦截
        canActivate():
            context:
    ConsoleLogger:
    DynamicModule: # 动态配置模块(forRoot)
    ExceptionFilter: # 异常处理过滤器基类
        catch():
            exception:
            host:
    ExecutionContext: # 路由守卫执行上下文
        getHandler(): # 获取处理函数
    HttpException: # HTTP异常基类
        getStatus():
    HttpStatus: # HTTP状态码
    INestApplication: # nest主应用类
        enableCors():
        get(): # 手动获取依赖
        listen(): # 监听端口
        setGlobalPrefix():
        use(): # 注册全局中间件
        useGlobalFilters(): # 全局异常处理过滤器
        useGlobalPipes(): # 全局数据管道
        useLogger():
    MiddlewareConsumer:
        apply(): # 应用中间件
        exclude(): # 排除应用中间件的路由
        forRoutes(): # 指定应用中间件的路由
            method:
            path:
    NestInterceptor: # 拦截器
    NestMiddleware: # 中间件
        use():
    NestModule: # 模块
        configure():
            consumer:
    NotFindException:
    OnModuleInit:
    ParseIntPipe:
    PipeTransform: # Pipe管道基类
        transform():
            value:
            metadata:
    RequestMethod:
        GET:
    ValidationPipe:

@nestjs/core:
    APP_GUARD:
    BaseExceptionFilter: # 异常捕获
    NestFactoroy:
        create(): # 创建应用实例(根据Module)
            logger:
    Reflector:
        createDecorator():
        get():

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

class-transformer: # 数据转换
    plainToInstance():
class-validator: # 数据验证(DTO)
    @IsEmail:
    @IsEnum:
        message:
    @IsNotEmpty:
    @IsString:
    validate(): # 数据校验

express: # nestjs内置集成http库
    NextFunction: # next函数
    Request: # 请求对象
    Response: # 响应对象
        json():
        send():
        status():
zod: # 数据验证
    z:
        infer(): # 创建数据验证类型(Dto)
        number():
        object():
            require():
        string():
    ZodSchema:
```


### Controller


### Provider

依赖注入对象、@Injectable、





### Module


模块、一个项目可以拆分成多个模块（根据路由、功能）

动态模块、forRoot静态方法动态生成模块信息(module、providers、exports)


### Middleware

```ts
import { Injectable, NestMiddleware } from '@nestjs/common';
import { Request, Response, NextFunction } from 'express';

@Injectable()
export class LoggerMiddleware implements NestMiddleware {
  use(req: Request, res: Response, next: NextFunction) {
    console.log('Request...');
    next();
  }
}
```

支持Express的函数式中间件（不支持依赖注入功能）



### Exception Filter

异常过滤链

自定义异常继承HttpException 




### Pipe

数据处理通道，类似中间件

数据转换、数据验证



### Guard

请求守卫（拦截）


### Interceptors

拦截器、类似中间件


### Custom Decorator



## 项目实战


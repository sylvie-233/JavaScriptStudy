# NestJs

`Nest.js官方文档：https://docs.nestjs.com/`
``


## 基础介绍

- `@nestjs/core`
- `@nestjs/common`
- `rxjs`
- `reflect-metadata`
- `@nestjs/platform-express`
- `@nestjs/platform-fastify`


nodejs 服务端框架、支持依赖注入

Middleware、Interceptor、Guard三个组件功能相似


全局->
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
    --help:
    add: # a
    build: # 打包
    generate: # g 生成代码文件
        controller: # 控制器
        module: # 模块
        resource:
        service: # CRUD resource router
    info: # i
    new: # n 新建项目
    start: # 运行项目
        --debug:
        --watch:
    update: # u
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
            inject: # 工厂函数参数注入
                optional:
                token:
            provide: # 自定义注册（不使用@Injectable）
                APP_FILTER:
                APP_GUARD:
                APP_INTERCEPTOR:
                APP_PIPE:
            useClass: # 使用类
            useExisting: # 创建已有注入的别名
            useFactory: # 使用工厂函数
            useValue: # 使用常量对象
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
        --- # req请求对象实例
        body:
        params:
        query:
    @Res: # 响应对象
        passthrough:
        --- # res响应对象实例
        download(): # 响应下载内容
        send(): # 发生响应内容
        type(): # 响应类型
    @Session:
    @SetMetadata: # 设置元信息（常配合Guard使用）
    @UseFilters: # 使用异常处理过滤器
    @UseGuards: # 使用请求守卫
    @UseInterceptors: # 使用拦截器（AOP）
    @UsePipes: # 使用数据管道(数据验证、数据转换)
    @Version: # api版本控制
    ArgumentMetadata: # 方法参数元数据
        data:
        metatype: # 元类信息
        type:
            body:
            custom:
            param:
            query:
    ArgumentsHost:
        switchToHttp():
            getResponse():
            getRequest():
    BadRequestException:
    CallHandler():
    CanActivate: # 请求守卫（）
        canActivate():
            context: # 执行上下文
    ConsoleLogger:
    DynamicModule: # 动态配置模块(forRoot)
    ExceptionFilter: # 异常处理过滤器基类
        catch():
            exception:
            host:
    ExecutionContext: # 路由守卫执行上下文
        getHandler(): # 获取处理函数
        switchToHttp():
            getRequest():
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
        useGlobalGuards(): # 全局请求守卫注册
        useGlobalInterceptors(): # 全局拦截器注册
        useGlobalPipes(): # 全局数据管道注册
        useLogger():
        useStaticAssets(): # 静态目录挂载
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
        errorHttpStatusCode:
    PipeTransform: # Pipe管道基类
        transform():
            value:
            metadata:
    RequestMethod:
        GET:
    ValidationPipe:
        validateCustomDecorators:
    applyDecorators(): # 复合装饰器（组合多个装饰器）
    createDecorator(): # 创建装饰器
    createParamDecorator(): # 创建参数装饰器

@nestjs/core:
    APP_GUARD:
    BaseExceptionFilter: # 异常捕获
    NestFactoroy:
        create(): # 创建应用实例(根据Module)
            logger:
    Reflector: # 反射工具（获取元信息）
        createDecorator(): # 自定义装饰器
        get(): # 获取装饰器中的值

@nestjs/mapped-types:
    PartialType():

@nestjs/platform-express:
    MulterModule:
        register():

@nestjs/swagger:
    @ApiBearerAuth:
    @ApiOperation:
    @ApiParam:
    @ApiQuery:
    @ApiResponse:
    @ApiTags:
    DocumentBuilder:
    SwaggerModule:

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
@nestjs/typeorm:
    @InjectRepository: # 注入dao
    TypeOrmModule:
        forFeature():
        forRoot():
            database:
            entities:
            host:
            password:
            port:
            synchronize:
            type:
            username:

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
    plainToInstance(): # 根据数据和元信息转换为校验对象
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
express-session: # 使用session中间件
    ():
        cookie:
            maxAge:
        name: # cookie名
        rolling:
        secret:
rxjx:
    operators:
        catchError():
        map():
        of():
        timeout():
    Observable:
    throwError():
zod: # 数据验证
    z:
        infer(): # 创建数据验证类型(Dto)
        number():
        object():
            require():
        string():
    ZodSchema:
        parse(): # 数据验证（失败抛出异常）
```


### Controller


控制器、视图处理函数


### Provider

依赖注入对象、@Injectable、

控制反转、构造方法注入

Factory providers工厂注入





### Module


模块、子工程、一个项目可以拆分成多个模块（根据路由、功能）

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

中间件
支持Express的函数式中间件（不支持依赖注入功能）



### Exception Filter
```ts

import { ExceptionFilter, Catch, ArgumentsHost, HttpException } from '@nestjs/common';
import { Request, Response } from 'express';

@Catch(HttpException)
export class HttpExceptionFilter implements ExceptionFilter {
  catch(exception: HttpException, host: ArgumentsHost) {
    const ctx = host.switchToHttp();
    const response = ctx.getResponse<Response>();
    const request = ctx.getRequest<Request>();
    const status = exception.getStatus();

    response
      .status(status)
      .json({
        statusCode: status,
        timestamp: new Date().toISOString(),
        path: request.url,
      });
  }
}
```

异常处理、异常过滤链

自定义异常继承HttpException 




### Pipe
```ts
@Get(':id')
async findOne(@Param('id', ParseIntPipe) id: number) {
  return this.catsService.findOne(id);
}

```

数据转换、数据验证
数据处理通道，类似中间件
内置ValidationPipe可实现大部分数据校验了
常配合`class-validator`、`class-transform`两个库使用自定义Pipe



在方法上使用数据验证、数据Pipe：`@UsePipes()`
在方法参数上使用数据转换Pipe：`@Param()`、`@Query()`、`@Body()`



内置Pipe：
- ValidationPipe
- ParseIntPipe
- DefaultValuePipe
- ParseFilePipe

使用`zod`：定义式数据验证
使用`class-validator`：声明式装饰器数据验证



#### Custom Pipe
```ts
import { PipeTransform, Injectable, ArgumentMetadata } from '@nestjs/common';

@Injectable()
export class ValidationPipe implements PipeTransform {
  transform(value: any, metadata: ArgumentMetadata) {
    // 方法内进行数据验证、数据转换
    return value;
  }
}
```




### Guard
```ts
@Injectable()
export class RolesGuard implements CanActivate {
  canActivate(
    context: ExecutionContext,
  ): boolean | Promise<boolean> | Observable<boolean> {
    return true;
  }
}
```


请求守卫（拦截）

Guard在所有Middleware之后执行、在所有Interceptor之前执行


### Interceptors
```ts
import { Injectable, NestInterceptor, ExecutionContext, CallHandler } from '@nestjs/common';
import { Observable } from 'rxjs';
import { tap } from 'rxjs/operators';

@Injectable()
export class LoggingInterceptor implements NestInterceptor {
  intercept(context: ExecutionContext, next: CallHandler): Observable<any> {
    console.log('Before...');

    const now = Date.now();
    return next
      .handle() // 处理函数调用
      .pipe(
        tap(() => console.log(`After... ${Date.now() - now}ms`)),
      );
  }
}
```


拦截器、类似中间件，主要用于实现AOP功能
- 在函数执行之前/之后绑定额外的逻辑
- 转换从函数返回的结果
- 转换从函数抛出的异常
- 扩展基本函数行为



### Custom Decorator

自定义装饰器

通常和Pipe结合一块使用



## 项目实战

### ORM

#### Prisma


#### TypeORM


### Templatie Engine

#### EJS



### Common Middlewares

#### express-session

session支持中间件


#### multer

文件上传


### Data Validation


#### Zod



### Deployment

#### PM2
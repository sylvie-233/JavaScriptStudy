# NestJs

`Nest.js官方文档：https://docs.nestjs.com/`
`2025最新版 Nest.js 零基础入门到精通教程: P11`


## 基础介绍

- `@nestjs/core`
- `@nestjs/common`
- `rxjs`
- `reflect-metadata`
- `@nestjs/platform-express`
- `@nestjs/platform-fastify`


Express + Decorator


nodejs 服务端框架、支持依赖注入
- Module:
- Controller:
- Provider: 注入式服务或依赖




全局->
module -> imports(导入其它模块)
       -> controllers(控制器)
       -> providers   -> services(服务实现)

一个项目project 可以有多个 模块module，模块module之间可以相互依赖嵌套




Middleware、Interceptor、Guard三个组件功能相似


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
        --watch: # 热更新
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
        controllers: # 控制器
        exports: # 导出provider、module
        imports: # 导入其它模块
        providers: # 功能依赖组件
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
    ArgumentsHost: # 上下文Context
        switchToHttp(): # 
    BadRequestException:
    CallHandler:
        handle(): # 使用rxjs Observable进行流式处理
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
    HttpArgumentHost: # 上下文Context
        getResponse():
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

@nestjs/config:
    ConfigModule:
        forRoot():
            isGlobal:

@nestjs/core:
    APP_GUARD:
    BaseExceptionFilter: # 异常捕获
    NestApplication: # nest应用
    NestFactoroy: # 应用模块工厂
        create(): # 创建应用实例(根据Module)
            logger:
    Reflector: # 反射工具（获取元信息）
        createDecorator(): # 自定义装饰器
        get(): # 获取装饰器中的值

@nestjs/jwt:        
    JwtModule:
        register():
            secret:
            signOptions:

@nestjs/mapped-types:
    PartialType():

@nestjs/passport:
    AuthGuard:
    PassportModule:
    PassportStrategy:

@nestjs/platform-express: # 底层express框架适配器
    MulterModule:
        register():

@nestjs/swagger:
    @ApiBearerAuth:
    @ApiOperation:
    @ApiParam:
    @ApiQuery:
    @ApiResponse:
    @ApiTags:
    DocumentBuilder: # 
        addBearerAuth():
        build():
        setDescription():
        setTitle():
        setVersion():
    SwaggerModule: # swagger模块
        createDocument(): # 创建文档对象
        setup(): # 启动swagger文档在指定url上面

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
    @MinLength:
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
passport-jwt:
    ExtractJwt:
    Strategy:
reflect-metadata: # 元编程库，提供元数据反射API，增强Reflect的Metadata功能
rxjs:
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
- @Controller
    - @Get:
    - @Post


### Provider

依赖注入对象、@Injectable、
控制反转、构造方法注入
任何可以被注入的东西都是 Provider，比如服务（Service）、工厂（Factory）、仓库（Repository）等


Factory providers工厂注入


#### Service

封装业务逻辑
一般作为 Provider 提供，被 Controller 注入调用，专注处理核心逻辑




### Module

模块、子工程、一个项目可以拆分成多个模块（根据路由、功能）
每个模块是一个功能区域（Feature Area），可以导入其他模块，提供自己的服务（Providers）给其他模块使用
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

异常处理、异常过滤链：统一管理异常响应，比如返回标准化错误信息
自定义异常继承HttpException 


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


请求守卫（拦截）,决定某个请求是否可以继续被处理
适合做权限控制、角色校验
Guard在所有Middleware之后执行、在所有Interceptor之前执行


### Pipe
```ts
@Get(':id')
async findOne(@Param('id', ParseIntPipe) id: number) {
  return this.catsService.findOne(id);
}

```

数据转换、数据验证：可以在进入 Controller 之前对参数做校验、转换
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
在请求处理前后扩展行为，在请求处理前后扩展行为
- 在函数执行之前/之后绑定额外的逻辑
- 转换从函数返回的结果
- 转换从函数抛出的异常
- 扩展基本函数行为



### Custom Decorator

自定义装饰器

通常和Pipe结合一块使用



## NestJS 生态

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



### Document

#### Swagger

### Deployment

#### PM2



## NestJs 原理


1. 应用启动Application：
依赖根模块创建应用对象NestApplication，内部初始化一个巨大的 IoC 容器

2. 扫描、注册模块Module：
Nest 会递归扫描 imports、controllers、providers。
所有模块、控制器、服务等元数据（用装饰器 @Module、@Injectable、@Controller 收集的）都会被提取出来。
生成模块之间的依赖图（dependency graph）

3. 创建、注入Provider
扫描到的 Provider（Service、Factory、Repository 等）：
- 被注册到容器里。
- 按需 实例化。
- 遇到需要依赖注入的地方，容器负责解析依赖树，自动注入

4. 绑定中间件（Middleware）
如果在模块中定义了中间件（比如日志、鉴权中间件）：
- Nest 调用 configure() 方法。
- 注册 Express（默认）或 Fastify 的中间件

5. 注册控制器路由（Controller）
- 扫描每个 Controller 上的路由装饰器，比如 @Get(), @Post()。
- 把这些路由绑定到底层的 HTTP 服务器（Express/Fastify）

6. 安装管道（Pipes）、守卫（Guards）、拦截器（Interceptors）、异常过滤器（Filters）
全局或者局部的 Pipes / Guards / Interceptors / Filters 都会在这一阶段挂载。
这些机制会形成一套请求处理链（类似于 AOP 切面编程）：
请求进来 → 中间件 → 守卫 → 管道 → 控制器 → 拦截器（前） → 业务逻辑 → 拦截器（后） → 返回响应

7. 启动 HTTP 服务器并监听端口
app.listen(3000) 会启动底层的 Express/Fastify。
等待接收外部请求

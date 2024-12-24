# express

``



## 基础介绍


一个project可以有多个router







### express-generator
```yaml
express:
    -h:
    --css:
    --ejs:
    --no-view:
    --view:
```

express脚手架



## 核心内容
```yaml
express:
    Express: # express Application
        locals: # app 本地变量(可用于模板渲染)
        mountpath: # route path
        response:
        router: # app 内置 router
        all(): # all request method handler
        delete():
        disable():
        engine(): # 设置模板引擎
        get():
        listen():
        on(): # 事件监听
            mount: # 路由挂载钩子
        param(): # 自定义path param处理
        path():
        post():
        put():
        route():
        set():
            view:
            view engine: # 模板引擎
            views: # 模板视图文件夹
        use():
    Multer:
        File:
            fieldname:
            originalname:
    Request:
        app:
        baseUrl:
        body: # 请求体
        cookies:
        err:
        file:
        files:
        host:
        hostname:
        headers:
        ip:
        ips:
        method:
        originalUrl:
        params:
        path:
        query:
        xhr:
        on():
            _data:
        pipe():
    Response:
        attachment(): # 附件下载
        cookie():
        clearCookie():
        download():
        end():
        json(): # 返回json数据
        jsonp():
        location():
        redirect(): # 重定向
        render(): # 渲染模板
        send(): # 响应内容
        sendFile(): # 响应文件
        sendStatus(): # 响应状态码
        set():
        status(): # 响应状态码
    Router: # 子路由
        _options:
            mergeParams:
        delete():
        get(): # http get请求
        param(): # 自定义path param处理
        post():
        put():
        use(): # 注册中间件
    response:
    json(): # json 请求体中间件
    Router(): # 子路由
    static(): # 静态目录挂载(中间件)
    urlencoded(): # urlencoded 请求中间件

cookie-parser:
cors:
body-parser:
express-validator: 
    body():
        isLength():
        withMessage():
    validationResult():
        _errors:
            array():
            isEmpty():
multer:
    _options:
        fileFilter:
        limits:
            fileSize:
        storage:
            config:
            destination:
    diskStorage: # 磁盘存储
        destination: # (req, file, cb)
        filename: # (req, file, cb)
    array():
    single(): # 单文件上传中间件
pug:
```


### Route


路由path可使用正则表达式

路由参数：`/path/:arg`

路由处理函数：`(req, resp, next)`
可一次性传入多个处理函数

子路由：`Router`


### Middleware

中间件
- 应用级别
- 路由级别
- 异常处理
- 内置中间件
- 第三方中间件



#### data validation




#### File Upload

multer库

```js

```


### Error Handler

异常处理：`(err, req, resp, next)`



### Template Engine

模板引擎

`art-template`

#### art-template



### Log



#### morgan


### ORM


#### sequelize


#### mongoose


### Test


### Third-party

#### Mail Sender
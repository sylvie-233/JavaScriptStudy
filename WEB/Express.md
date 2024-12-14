# express

``



## 基础介绍

### express-generator
```yaml
express:
    -h:
    --css:
    --ejs:
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
        json():
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
        get():
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

multer:
    _options:
        limits:
        storage:
    diskStorage: # 磁盘存储
        destination: # (req, file, cb)
        filename: # (req, file, cb)
    array():
    single():

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


#### File Upload

multer库

```js

```


### Error Handler

异常处理：`(err, req, resp, next)`



### Template Engine

模板引擎

`art-template`




### Third-party
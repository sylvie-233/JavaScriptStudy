# express

`Express官方教程：https://expressjs.com/en/guide/error-handling.html`



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
    Express:
        response:
        all():
        delete():
        engine(): # 设置模板引擎
        get():
        listen():
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
        body: # 请求体
        cookies:
        err:
        file:
        files:
        headers:
        originalUrl:
        method:
        params:
        on():
            _data:
        pipe():
    Response:
        download():
        end():
        json():
        jsonp():
        redirect(): # 重定向
        render(): # 渲染模板
        send(): # 响应内容
        sendFile(): # 响应文件
        sendStatus(): # 响应状态码
        status(): # 响应状态码
    Router: # 子路由
        _options:
            mergeParams:
        delete():
        get():
        post():
        put():
        use():
    response:
    json(): # json 请求体中间件
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




### Third-party
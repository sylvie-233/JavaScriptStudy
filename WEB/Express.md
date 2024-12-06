# express

`Express官方教程：https://expressjs.com/en/guide/writing-middleware.html`



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
        all():
        delete():
        get():
        listen():
        post():
        put():
        route():
        use():
    Request:
        body:
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
        send(): # 响应内容
        sendFile(): # 响应文件
        sendStatus(): # 响应状态码
    Router: # 子路由
        _options:
            mergeParams:
        delete():
        get():
        post():
        put():
        use():
    json(): # json中间件
    static(): # 静态目录挂载(中间件)
```


### Route


路由path可使用正则表达式

路由参数：`/path/:arg`

路由处理函数：`(req, resp, next)`
可一次性传入多个处理函数

子路由：`Router`
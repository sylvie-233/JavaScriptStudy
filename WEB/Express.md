# express

`Express官方教程：https://expressjs.com/en/guide/routing.html`



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
        delete():
        get():
        listen():
        post():
        put():
        use():
    Request:
        body:
        params:
        on():
            _data:
        pipe():
    Response:
        send(): # 响应内容
    json(): # json中间件
    static(): # 静态目录挂载(中间件)
```
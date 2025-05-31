# Hono


## 基础介绍


Web开发框架


Hono脚手架项目
`bun create hono my-app`



## 核心内容
```yaml
hono:
    adapter:
        env():
    cache:
        cache():
    client:
        hc():
    http-exception:
        HTTPException:
    logger: # 日志中间件
        logger():
    streaming: # 流式响应
        stream():
        streamSSE():
        streamText():
    testing:
        testClient:
    vercel:
        handle():
    Context: # http 上下文
        req:
        body():
        header():
        html():
        json():
        notFound():
        redirect():
        status():
        text():
    Hono: # 主应用
        basePath():
        delete():
        fetch():
        fire(): # 添加全局fetch事件
        get():
        group():
        mount():
        onError(): # 全局异常处理
        post():
        put():
        request(): # 请求转发
        route(): # 子路由组
        use(): # 使用中间件 (ctx, next)
    HonoRequest: # http 请求
        arrayBuffer(): # body 二进制
        header():
        json(): # body application/json
        param(): # path 路径参数
        parseBody():
        query(): # query 请求参数
        text(): # body text/plain
        valid(): # 使用zValidator校验器
    MiddlewareHandler: # (ctx, next)
    Response: # http 响应
        headers:
            append():
        get():
        set():
@hono: # 第三方集成
    node-server: # node 服务
        HttpBindings:
        serve():
            fetch:
            port: 
    swagger:
    zod-validator: # zod字段校验器
        zValidator():
```



### Request

请求



#### Context



### Route


路由

#### RouteGroup
```ts
// 为 "/api" 路由组应用中间件
app.route('/api', (r) => {
  r.use(cors()) // 只对/api路由组应用CORS中间件
  r.use(bodyParser()) // 只对/api路由组应用请求体解析中间件

  r.get('/user', (c) => {
    return c.json({ id: 1, name: 'John Doe' })
  })

  r.post('/login', (c) => {
    const { username, password } = c.req.body
    return c.json({ username, password })
  })
})
```

路由组


### Middleware 

中间件




### Exception


异常处理


### Validation

字段校验


#### Zod


### Security


#### Jwt




### Template

模板引擎



### ORM




### Logger

日志


### Swagger

OpenAPI文档



### Websocket
# tRPC


## 基础介绍

typescript RPC框架
- @trpc/server 
- @trpc/client 
- @trpc/react-query

## 核心内容
```yaml
@trpc:
    client: # 客户端
        createTRPCProxyClient():
        httpBatchLink():
    server: # 服务端
        adapters:
            express:
                createExpressMiddleware(): # 创建express中间件
                    createContext:
                    router:
        initTRPC():
            create():
                procedure:
                    input():
                    mutation(): # 修改
                    query(): # 查询
                router(): # 路由定义
```
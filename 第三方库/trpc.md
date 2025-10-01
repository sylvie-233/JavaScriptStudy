# tRPC


## 基础介绍

typescript RPC框架（基于http协议，没有单独新开端口）
- @trpc/server 
- @trpc/client 
- @trpc/react-query

- 可集成在express中
- graphql升级版


## 核心内容
```yaml
@trpc:
    client: # 客户端
        createTRPCProxyClient():
        httpBatchLink():
    server: # 服务端
        adapters: # 后端适配器
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
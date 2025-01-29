# http-proxy-middleware

## 基础介绍

node反向代理中间件

### proxy.config.js
```yaml
:
    serve:
        proxy:
            /xxx:
                changeOrigin:
                rewrite:
                target:
```


## 核心内容
```yaml
http-proxy-middleware:
    createProxyMiddeware():
```
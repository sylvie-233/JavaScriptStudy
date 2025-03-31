# Remix

## 基础介绍

基于React的服务端渲染框架


`npx create-remix@latest`


### 项目结构
```yaml
项目结构:
    /app:
        /routes: # 路由文件
            _index.tsx:
                action(): # api处理
                clientAction(): # 前端 api
                clientLoader():
                handle():
                headers():
                links():
                    href:
                    rel:
                loader(): # 页面数据加载
                meta(): # 页面元信息
                shouldRevalidate():
                Component(): # 自定义组件
                ErrorBoundary(): # 错误边界
                HydrateFallback(): # Suspence加载状态
        entry.client.tsx: # 客户端入口
        entry.server.tsx: # 服务端入口
            handleDataRequest():
            handleError():
        root.tsx:
        tailwind.css:
    /node_modules:
    /public:
    .eslintrc.cjs:
    package.json:
        @remix-run/node:
        @remix-run/react:
        @remix-run/serve:
        react:
        react-dom:
    postcss.config.js:
    remix.config.js:
    tailwind.config.ts:
    tsconfig.json:
    vite.config.ts:
```

#### remix.config.js
```yaml
remix.config.js:

```


### remix
```yaml
remix:
    vite:
        build:
```



## 核心内容
```yaml
react:
    FunctionComponent:
@remix-run/dev:
@remix-run/express:
    createRequestHandler():
@remix-run/node:
    ActionFunctionArgs:
        request:
            formData():
    LinksFunction:
    LoaderFunctionArgs:
    json():
    redirect(): # 重定向
@remix-run/react:
    Form: # 表单
    Link: # 链接
        to:
    Links: # 链接出口
    Meta: # 元信息出口
    NavLink:
    Outlet: # 路由出口
    RemixBrowser:
    Scripts: # 脚本出口
    screen:
    render():
    useLoaderData(): # 使用loader加载数据
    useNavigate():
    useNavigation():
@remix-run/serve:
```


### File Conventions





### Route Module




### Components



### Hooks


### Utilities

### Styling
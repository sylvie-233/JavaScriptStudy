# Remix

`remix官方文档：https://remix.run/docs/en/main/start/tutorial#creating-contacts`


## 基础介绍

基于React的SSR服务端渲染框架、集成React-Router
基于文件系统约定式路由，`.`代表了路由路径`/`


创建remix脚手架
`npx create-remix@latest --template`





### 项目结构
```yaml
项目结构:
    /app:
        /routes: # 路由文件
            _index.tsx:
                action(): # 服务端，api请求处理
                clientAction(): # 前端 api
                clientLoader():
                handle():
                headers():
                links(): # css link链接，可多个
                    href:
                    rel:
                loader(): # 服务端，页面数据加载、参数校验定义、配合客户端的useLoaderData()使用
                    params: # 页面 parh params路径参数
                meta(): # 页面元信息
                shouldRevalidate():
                Component(): # 自定义组件
                ErrorBoundary(): # 错误边界
                HydrateFallback(): # Suspence加载状态
            $xxx.tsx: # 动态路由页面
        entry.client.tsx: # 客户端入口，底层
        entry.server.tsx: # 服务端入口，底层
            handleDataRequest():
            handleError():
        root.tsx: # 客户端加载 root根页面
        tailwind.css:
    /build: # 构建目录
        /client:
        /server:
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


#### vite.config.ts
```yaml

```


### remix
```yaml
remix:
    reveal: # 生成entry.client.tsx、entry.server.tsx底层控制文件
    vite:
        build: # 构建打包
```


#### remix-serve
```yaml
remix-serve: # remix服务运行
```

基于express实现的服务器



## 核心内容
```yaml
react:
    FunctionComponent: # 函数式组件
react-dom:
@remix-run/dev:
    vitePlugin: # vite remix打包插件
@remix-run/express:
    createRequestHandler():
@remix-run/node:
    ActionFunctionArgs:
        request:
            formData():
    LinksFunction: # 
    LoaderFunctionArgs: # loader 函数参数类型
    json():
    redirect(): # 重定向
@remix-run/react:
    Form: # 表单
        action: # url
        encType:
    Link: # 链接
        to:
    Links: # 链接出口
    Meta: # 元信息出口
    NavLink:
    Outlet: # 路由出口
    RemixBrowser:
    Scripts: # 脚本出口
    ScrollRestoration:
    screen:
    render():
    useLoaderData(): # 使用定义的loader加载数据
    useNavigate():
    useNavigation():
@remix-run/serve:
@remix-run/testing:
```


### File Conventions





### Route Module




### Components



### Hooks


### Utilities

### Styling
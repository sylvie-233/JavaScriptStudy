# Next.js

>
>`Next.js官方文档：https://nextjs.org/docs`
>
>
>
>``
>

## 基础介绍


React服务端实现


`page.tsx`、`route.tsx`


- page：显示的页面Page
- route: 后端控制器Controller
- action：后端服务方法Service





- SSG: 静态站点生成
- ISR: 增量静态生成


核心功能：
- Routing
- API routes
- Rendering
- Data fetching
- Styling
- Optimization
- Dev and prod build system


- 基于文件的路由系统，所有路由文件都必须放入app文件夹中
- 路由页面：`page.tsx`
- 布局页面：`layout.tsx`
- 模板页面：`template.tsx`
- 默认页面：`default.tsx`
- 404页面：`not-found.tsx`
- 加载页面：`loading.tsx`
- 异常处理：`error.tsx`
- API Handler：`route.tsx`
- 中间件：`middleware.ts`

![Next组件结构](../assets/Next组件结构.png)


路径别名：根目录`@/xxx`


自动图象、字体优化


### next

```yaml
next:
    build:
    dev:
    lint:
    start:
```


#### create-next-app
```yaml
create-next-app: # next脚手架
    --typescript:
```

next脚手架




### 项目结构
```yaml
项目结构:
    /.next:
        /cache:
        /server:
        /static:
        /types:
        package.json:
    /public: # 静态资源目录
    /src:
        /app: # 前端路由页面
            /xxx:
            /(xxx): # 路由分组 无实际url
            /_xxx: # 私有文件夹
            /api:
                /xxx:
                route.tsx:
                    Response:
                        json:
                    GET():
            default.tsx: # 默认插槽页面
            error.tsx: # 异常页面
                error:
                    message:
                reset():
            favicon.ico:
            globals.css: # 全局CSS
            layout.tsx: # 主布局页面
                metadata: # 页面元信息
                ---
                children: # 子组件渲染
            loading.tsx: # 加载页面
            page.tsx: # 入口页面
                dynamic: # 动态页面配置
                revalidate: # 页面重新验证刷新时间
                generateMetadata(): # 动态生成页面元信息
                ---
                params: # 页面参数
                searchParams:
                fetch(): # 异步获取数据
        /components:
        /lib:
        middleware.tsx: # 中间件定义
            config:
                matcher: # 中间件匹配器
            middleware():
    .eslintrc:
    next-env.d.ts:
    next.config.js:
    package.json:
    postcss.config.json:
    tailwind.config.ts:
    tsconfig.json:
```

## 核心内容

```yaml
next:
    font:
        google:
            Inter:
    headers:
        cookies(): # 请求头中的Cookie
        headers():
    image:
        Image: # 图片组件
            alt:
            src:
    link:
        Link: # 页面跳转组件
            href:
            replace:
    navigation:
        notFound(): # 跳转到404页面
        redirect(): # 重定向响应
        userPathname(): # 获取url path（仅客户端组件）
        useRouter(): # 路由器、路由跳转（仅客户端组件）
            ---
            back():
            forward():
            push():
            refresh():
            replace(): 
        useSearchParams():
        useServerInsertedHTML():
    server:
        NextRequest:
            cookies:
            headers:
            nextUrl:
                pathname:
                searchParams:
            url:
        NextResponse:
            cookies:
            headers:
            next():
            redirect(): # 重定向
            rewrite():
    Headers:
    Request:
        json():
    Response:
        json():
    Metadata: # 页面源信息
        title: # 页面标题
            absolute:
            default:
            template: # 多级metadata嵌套模板字符串
        description: # 页面描述
    NextConfig: # next项目配置
        compiler:
            styledComponents:
        images:
            remotePatterns:
        sassOptions:
            additionalData:
react: # React全局对象
    FormEvent:
    ReactNode: # jsx组件
    Suspense:
        fallback:
    startTransition():
    use(): # 使用异步参数
    useState():
react-dom:
    useFormStatus():
        pending:



next-auth:
    NextAuth:
        adapter: # 集成数据库
        providers: # 集成OAuth第三方 
        ---
        auth():
        handlers():
        signIn():
        signOut():
    Session:
next-safe-action: # next api 自调用
    createSafeActionClient():
    useAction():
        onSuccess():
        ---
        status:
        execute():
react-hook-form:
```


### Routing

- `[id]`：动态路由匹配
- `[...id]`：多级匹配、匹配所有
- `(id)`：排除名称、路由分组（文件夹名不包含在路由内）
- `_id`：私有文件夹
- `@id`：layout插槽文件夹
- `(.)id`/`(..)id`/`(...)id`: 路由拦截文件夹


path params 通过函数参数传递进来



`page.tsx`：默认页面

`layout.tsx`：默认布局页面

当前及其子级的page.tsx文件都 会被放入layout.tsx文件中

layout插槽：`default.tsx`插槽默认页面

路由拦截：


#### Dynamic Route







#### Private Route


#### Route Group

#### 404


#### Loading


#### Error Handling

error.tsx必须是客户端组件


### Rendering

默认服务端组件

`use client`使用客户端组件

客户端渲染组件CSC、服务端渲染组件RSC

服务端组件不能使用state

客户端渲染组件的子级也是客户端渲染组件，尽量在叶子节点的组件上使用客户端组件


组件渲染顺序
- layout.js
- template.js
- error.js (React error boundary)
- loading.js (React suspense boundary)
- not-found.js (React error boundary)
- page.js or nested layout.js




#### Inner Component
```yaml
内置组件:
    Image:
    Link:
        href:
    Suspense:
```


METADATA动态生成

Link链接

Suspense占位组件：可实现延迟加载


#### Layout

实现内部React-Router效果

layout.tsx可嵌套


#### Template




#### Styling

支持`.module.css`模块CSS、全局CSS






### API Handler

```javascript
// route.tsx
export async function GET() {
    return new Response("xxx")
}

export async function POST(req: Request) {
    const data = await request.json()
    return new Response("xxx")
}

```  
page.tsx与route.ts存在冲突，优先显示route.tsx

route.ts的路由规则和page.tsx的规则一样

中间件Middleware

form表单的action可直接绑定API处理函数





#### Data Fetching

fetct()

ORM





#### Middleware

```javascript
// 中间件处理函数
export function middleware(req: NextRequest) {
    return NextResponse.redirect("/xxx")
}

// 中间件配置
export const config = {
    matcher: "/xxx"
}

```

#### Caching


#### Authentication


`next-auth`



### Comfiguring

#### Optimizing



### Testing


### Deploy








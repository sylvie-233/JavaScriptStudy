# Next.js

>
>`Next.js官方文档：https://nextjs.org/docs/app/getting-started/images-and-fonts`
>

## 基础介绍

React服务端实现


`page.tsx`、`route.tsx`


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


路径别名：根目录`@/xxx`



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





### 项目结构

```yaml
:
    /public:
    /src:
        /app: # 前端路由页面
            /_xxx: # 私有文件夹
            /xxx:
            /api:
                route.tsx:
            default.tsx: # 默认插槽页面
            error.tsx:
            favicon.ico:
            globals.css:
            layout.tsx: # 主布局页面
                children: # 子组件渲染
            loading.tsx:
            page.tsx: # 入口页面
        /components:
        /lib:
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
        cookies():
        headers():
    image:
        Image:
    link:
        Link: # 页面跳转组件
            href:
            replace:
    navigation:
        notFound():
        redirect(): # 重定向
        userPathname():
        useRouter(): # 路由器（路由跳转）
            :
            back():
            forward():
            push():
            refresh():
            replace(): 
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
            redirect():
            rewrite():
    Headers:
    Request:
        json():
    Response:
        json():
    Metadata:
        title:
        description:
    NextConfig:

React:
    FormEvent:
    ReactNode:
    Suspense:
        fallback:
    useState():

```


### Routing

- `[id]`：
- `[...id]`：多级匹配
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




### Rendering

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




#### 内置组件


METADATA动态生成

Link链接

Suspense占位组件：可实现延迟加载







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

#### Data Fetching





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


#### Testing








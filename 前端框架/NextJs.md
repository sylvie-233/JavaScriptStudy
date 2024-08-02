# Next.js

>
>`# TODO Next.js 14 Tutorial P41`
>

## 基础介绍

React服务端实现


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
- 404页面：`not-found.tsx`
- 加载页面：`loading.tsx`
- 异常处理：`error.tsx`
- API Handler：`route.tsx`


### next

```yaml
next:
    build:
    dev:
    lint:
    start:
```






### 项目结构

```yaml
:
    /public:
    /src:
        /app:
            favicon.ico:
            globals.css:
            layout.tsx:
            page.tsx:
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
    link:
        Link:
            href:
            replace:
    navigation:
        redirect(): 重定向
        userPathname():
        useRouter():
            :
                back():
                forward():
                push():
                refresh():
                replace():
    server:
        NextRequest:
            nextUrl:
                searchParams:
    Request:
        json():
    Response:
        json():
    Metadata:
        title:
        description:
    NextConfig:

React:
    ReactNode:
    useState():

```

### 内置组件

`use client`使用客户端组件



METADATA动态生成

Link链接






### 动态路由

- `[id]`：
- `[...id]`：多级匹配
- `(id)`：排除名称
- `_id`：私有文件夹
- `@id`：layout插槽文件夹
- `(.)id`/`(..)id`/`(...)id`: 路由拦截文件夹



`page.tsx`：默认页面

`layout.tsx`：默认布局页面

当前及其子级的page.tsx文件都 会被放入layout.tsx文件中

layout插槽：`default.tsx`插槽默认页面

路由拦截：


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





# TailwindCSS

`TailwinCSS官方文档：https://tailwindcss.com/docs/aspect-ratio`

## 基础介绍


预定义css类样式库




引入tailwindcss
```css
/* 旧方法，已被移除 */
@tailwind base;
@tailwind components;
@tailwind utilities;

/* 新方法 */
@import "tailwindcss";
/*
内部定义、引入：
@layer theme, base, components, utilities;

@import "tailwindcss/theme.css" layer(theme);
@import "tailwindcss/preflight.css" layer(base);
@import "tailwindcss/utilities.css" layer(utilities);

*/
```

`@layer`：自定义样式
`@apply`：应用自定义样式



### tailwindcss
```yaml
tailwindcss:
    --watch: 监听（实时编译）
    init: 初始化
```





#### tailwind.config.js
```yaml
tailwind.config.js:
    content:
    plugins:
    theme:
        extend:
```









## 核心内容
```yaml
tailwindcss:
    Config:
        content:
        theme:
            extend:
        plugins:

utility-class:
    variants: # 前缀条件状态查询
        @lg:
        @md: # 容器宽度条件 @container标注容器
        active:
        after: # ::after伪元素
        before: # ::before伪元素
        checked:
        dark:
        data-*: # 自定义data属性状态条件
        disabled:
        disabled:
        empty:
        file: # ::file
        first: # first-child
        first-line: # ::first-line
        first-letter: # ::first-letter
        first-of-type:
        focus:
        group-*: # 父类状态条件
        group-[selector]: # 选择器父类状态条件
        group-*/{name}: # 命名父类状态条件
        has-*:
        hover: # :hover状态
        in-*: # 级联状态
        invalid:
        last: # last-child
        lg: # 
        marker: # ::marker
        max-*:
        md:
        not-*:
        nth-*:
        nth-last-*:
        nth-last-of-type-*:
        nth-of-type-*:
        only-child:
        peer-*: # 同类状态条件
        peer-[selector]:
        peer-*/{name}:
        placeholder: # ::placeholder
        required:
        selection: # ::selection
        sm:
    @container: # 标注容器
```



### Layout

```yaml
:
    absolute:
    container:
        "width: 100%;"
        container-sm:
    box-border:
    box-content:
    block:
    clear-both:
    clear-left:
    fixed:
    inline-block:
    inline:
    object-contain:
    object-fill:
    overflow-auto:
    overscroll-auto:
    relative:
    static:
    sticky:
    top-0:
    visible:
    z-0:
```

### Flexbox & Grid

```yaml
:
    flex-1:
    grid-cols-1:
    items-center:
    justify-center:
    justify-end:
```

### Spacing

```yaml
:
    m-0:
        "margin: 0px;"
        mx-0:
            "margin-left: 0px;margin-right: 0px;"
    p-0:
        "padding: 0px;"
        px-4:
        py-4:
    space-x-0:
```

### Sizing

```yaml
:
    h-44:
    min-w-0:
    size-0:
    w-0:
```

### Typography

```yaml
:
    align-top:
    break-words:
    font-bold:
    text-6xl:
    text-black:
    text-center:
    text-sm:
    text-wrap:
    underline:
```


### Backgrounds

```yaml
:
    bg-black:
    bg-center:
    bg-clip-border:
    bg-fixed:
```

### Borders

```yaml
:
    border:
    rounded:
```

### Effects

```yaml
:
    opacity-0:
    shadow:
    
```

### Filters

```yaml
:
    blue:
```

### Tables

```yaml
:
    border-collapse:
```

### Transitions & Animation

```yaml
:
    transition:
```

### Transforms

```yaml
:
    scale-0:
```

### Interactivity

```yaml
:
   cursor-pointer: 
   scroll-auto:
```


## 核心概念

### CSS Directive

TailwinCSS@指令




#### @apply
```css
.select2-dropdown {
  @apply rounded-b-lg shadow-md;
}
```

在自定义css中引用tailwincss工具类


#### @custom-variant
```css
@custom-variant pointer-coarse (@media (pointer: coarse));

/* 使用：pointer-coarse:size-48 */
```
自定义条件状态查询
自定义前缀变量


#### @import

导入css文件

#### @reference
```vue
<template>
  <h1>Hello world!</h1>
</template>

<style>
  @reference "../../app.css";
  h1 {
    @apply text-2xl font-bold text-red-500;
  }
</style>
```


引用框架css文件、以便可以在前端框架的`<style>`块中使用`@apply`、`@variant`等tailwincss指令



#### @layer


过时指令、用于在特定功能模块自定义属性


#### @source

显式声明可被tailwindcss检测的源码文件


#### @theme
```css
@theme {
  --font-display: "Satoshi", "sans-serif";
  --breakpoint-3xl: 1920px;
  --color-avocado-100: oklch(0.99 0 0);
  --ease-snappy: cubic-bezier(0.2, 0, 0, 1);
}
```

自定义css变量，用于修改默认行为


#### @utility
```css
@utility tab-4 {
  tab-size: 4;
}
```

添加自定义工具类、能关联系统自带条件前缀


#### @variant
```css
@variant dark {
    background: black;
}
```


在自定义css中使用条件状态查询
多条件状态使用嵌套@variant



### State Condition

样式前缀约束

样式状态支持父类查询group、同类查询peer


#### Custom Breakpoints
```css
@import "tailwindcss";
@theme {
  --breakpoint-xs: 30rem;
  --breakpoint-2xl: 100rem;
  --breakpoint-3xl: 120rem;
}
```

自定义媒体宽度



#### Dark Mode










## Components
# TailwindCSS

## 基础介绍



`@layer`、`@apply`：自定义样式




```css
@tailwind base;
@tailwind components;
@tailwind utilities;


```

### tailwindcss

```yaml
tailwindcss:
    --watch: 监听（实时编译）
    init: 初始化
```





### tailwind.config.js

```javascript
module.exports = {
    content:
    theme: {
        extend:
    },
    plugins:
}
```









## 核心内容

```yaml
tailwindcss:
    Config:
        content:
        theme:
            extend:
        plugins:

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

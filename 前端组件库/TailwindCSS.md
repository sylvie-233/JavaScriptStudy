# TailwindCSS

`TailwinCSS官方文档：https://tailwindcss.com/docs/aspect-ratio`

## 基础介绍


预定义css类样式库




引入tailwindcss
```js
/* 旧方法，已被移除 */
/* 基础样式 (Normalize & Reset) */
@tailwind base; 
/* 组件样式 (可复用的 CSS 类) */
@tailwind components; 
/* 工具类 (margin, padding, flex, grid 等) */
@tailwind utilities;
/* (Tailwind v3.4+) 变体样式（动态生成） */
@tailwind variants;

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



tailwindcss断点前缀：
- sm: (≥640px)
- md: (≥768px)
- lg: (≥1024px)
- xl: (≥1280px)
- 2xl: (≥1536px)



### tailwindcss
```yaml
tailwindcss:
    -i: # 输入文件（先根据配置文件进行扫描）
    -o: # 输出文件
    --minify:
    --watch: # 监听、实时编译
    init: # 生成配置文件
```


tailwindcss扫描编译器





#### tailwind.config.js
```yaml
tailwind.config.js:
    content: # 扫描使用tailwindcss的文件
    corePlugins: # 
    dartMode: # 黑暗模式
        class: # 手动加dark类
        media: # 根据用户系统主题切换
    plugins: # 插件
    presets: # 预设配置
    theme: # 主题，允许你扩展 Tailwind 的默认设计系统，比如颜色、间距、字体大小等
        extend: # 自定义样式扩展
            borderRadius:
            color:
            colors:
            fontFamily:
            spacing:
        screens:
            sm:
            xs:
    variants: # 变体配置
        extend:
            backgroundColor:
```

tailwincss配置文件





## 核心内容
```yaml
tailwindcss:
    variants: # 变体、前缀条件状态查询
        @lg:
        @md: # 容器宽度条件 @container标注容器
        active: # 激活状态
        after: # ::after伪元素
        before: # ::before伪元素
        checked:
        dark: # 暗黑模式
        data-*: # 自定义data属性状态条件
        disabled: # 禁用状态
        empty:
        file: # ::file
        first: # first-child
        first-line: # ::first-line
        first-letter: # ::first-letter
        first-of-type:
        focus: # 焦点状态
        group-*: # 父类状态条件
            hover:
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
            checked:
        peer-[selector]:
        peer-*/{name}:
        placeholder: # ::placeholder
        required:
        selection: # ::selection
        sm:
    @container: # 标注容器
    align: # 垂直对齐
        baseline: # vertical-align: baseline;
        middle:
        top:
    animate: # 动画
        bounce: # 弹跳
        spin: # 旋转
    aspect:
        ratio:
        square: # 宽高比 1:1
    bg:
        gradient: # 背景渐变
        red: # 背景颜色，background-color: var(--color-red);
            [x]:
        opacity: # 背景透明度
    block: # 块级元素，display: block;
    blur: # 模糊
    border:
        red: # 边框颜色
            [x]:
    box:
        border: # 边框盒子模型，box-sizing: border-box
    brightness: # 亮度
    btn: # 按钮
        primary:
        secondary:
    col:
        span: # 列偏移
    columns:
    container:
    contrast: # 对比度
    divide: # 分割线
        y: # 
    duration: # 过渡持续时间
    flex: # 弹性布局
        col:
    font: # 字体
        [value]: # font-family: <value>;
        bold: # 字体加粗
        light: # 字体宽度，font-weight: 300;
        mono: # mono字体，font-family: var(--font-mono);
    gap: # 间距
        [x]:
    grayscale: # 灰度
    grid: # 网格布局
        cols: # 网格列
            [x]: # 指定列网格布局
        rows: # 网格行
    h:
        screen:
    hidden:
    inline:
        flex:
    items:
        center:
    list: # 列表
        none: # 移除默认样式
    justify:
        center:
    m: # 外边距
        [x]:
    min:
        h:
    ml:
    mx:
        auto: # 水平居中
    no-underline: # 取消文本装饰，text-decoration-line: none;
    p:
        [x]: # 内边距
    px:
    py:
    object: # 
        cover: # 图片等比例填充
    outline: # 轮廓
        none: # 无轮廓
    overflow: # 溢出
        auto: # 自动滚动
        hidden: # 隐藏溢出内容
    placeholder:
        gray: # 占位符颜色
    rotate: # 旋转
    rounded: # 圆角
        full:
        lg:
    row:
        span: # 行偏移
    scale:
    scroll:
        smooth: # 平滑滚动
    sepia:
    shadow: # 盒子阴影
        lg:
    space:
        x:
            [x]:
    text: # 文本
        lg: # 字体大小
        center: # 文本对齐，居中，text-align: center;
        while: # 文本颜色，color: var(--color-white);
        wrap: # 文本换行，text-wrap: wrap;
        xl: # 字体大小，font-size: var(--text-xl); line-height: var(--text-xl--line-height);
    transition: # 过渡
    translate: # 平移
        x:
    underline: # 文本下划线，text-decoration-line: underline;
    w: # 宽度
        [number]: # width: calc(var(--spacing) * <number>);
        1/2: # 一半宽度
        full:
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

基础布局


### Flexbox & Grid
```yaml
:
    flex-1:
    grid-cols-1:
    items-center:
    justify-center:
    justify-end:
```

弹性布局、网格布局




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

间距


### Sizing
```yaml
:
    h-44:
    min-w-0:
    size-0:
    w-0:
```

大小




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

文本段落



### Backgrounds
```yaml
:
    bg-black:
    bg-center:
    bg-clip-border:
    bg-fixed:
```

背景



### Borders
```yaml
:
    border:
    rounded:
```

边框


### Effects
```yaml
:
    opacity-0:
    shadow:
    
```

特殊效果



### Filters
```yaml
:
    blue:
```

滤镜


### Tables
```yaml
:
    border-collapse:
```

表格



### Transitions & Animation
```yaml
:
    transition:
```

过渡、动画




### Transforms
```yaml
:
    scale-0:
```

变换



### Interactivity
```yaml
:
   cursor-pointer: 
   scroll-auto:
```

交互性




### SVG

矢量图




## 核心概念
```yaml
tailwindcss/plugin:
    plugin():
        addBase(): # 添加基础css类
        addComponents(): # 添加组件类
        addUtilities(): # 添加工具类
        addVariant(): # 添加变体
        theme(): # 获取theme配置
```


### Directive

TailwinCSS@指令




#### @apply
```css
.select2-dropdown {
  @apply rounded-b-lg shadow-md;
}
```

在自定义css中引用tailwincss工具类
允许你在 CSS 中直接使用 Tailwind 的工具类



#### @config
```css
@config "./tailwind.config.js";
```

允许你直接在 CSS 文件中指定 Tailwind 配置文件路径




#### @custom-variant
```css
@custom-variant pointer-coarse (@media (pointer: coarse));

/* 使用：pointer-coarse:size-48 */
```
自定义条件状态查询
自定义前缀变量


#### @import

导入css文件




#### @layer
```css
@layer components {
  .btn-primary {
    @apply py-2 px-4 bg-blue-500 text-white rounded hover:bg-blue-700;
  }
}
```

过时指令、用于在特定功能模块自定义属性
- @layer base：扩展基础样式，修改 HTML 标签的默认样式。
- @layer components：定义可复用的组件类，如 .btn。
- @layer utilities：扩展实用工具类，如 .content-auto。


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



#### @screen
```css
@screen md {
  .custom-btn {
    @apply bg-blue-500 text-white;
  }
}
```

手动创建响应式规则、类似@media媒体查询
根据 Tailwind 断点定义响应式样式


#### @source

显式声明可被tailwindcss检测的源码文件


#### @tailwind
```css
@layer base {
  h1 {
    @apply text-2xl font-bold;
  }
}

@layer components {
  .btn {
    @apply px-4 py-2 bg-blue-500 text-white rounded;
  }
}

@layer utilities {
  .content-auto {
    content-visibility: auto;
  }
}
```



用于引入 Tailwind 的不同层级样式


#### @theme
```css
@theme {
  --font-display: "Satoshi", "sans-serif";
  --breakpoint-3xl: 1920px;
  --color-avocado-100: oklch(0.99 0 0);
  --ease-snappy: cubic-bezier(0.2, 0, 0, 1);
}
```

自定义css主题变量，用于修改默认行为


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



### Variants

样式前缀约束、内置class查询，实现原生css伪类的效果
样式状态支持父类查询group、同类查询peer
支持组合变体、伪类变体

#### Group
```jsx
<div class="group p-4 border">
  <p class="group-hover:text-red-500">鼠标悬停时，我会变红！</p>
</div>

/**
 * group 放在父元素（div）。
 * group-hover:text-red-500 让 子元素 在 父元素 hover 时 变红。
 */
```

group允许父元素的状态（如hover、focus）影响子元素的样式
- group-active:
- group-focus:
- group-hover:


#### Peer
```jsx
<input type="checkbox" id="toggle" class="peer hidden">
<label for="toggle" class="peer-checked:bg-green-500 p-2">点击我</label>
```

兄弟元素状态
- peer-checked:

#### Has

- first:
- last:
- odd:
- even:


#### Status

- active:
- focus:
- focus-visible:
- focus-within:
- hover:


#### Data
```jsx
<button data-state="active" class="data-[state=active]:bg-green-500 p-4">
  状态按钮
</button>
```

利用HTML data-*属性，Tailwind提供`data-[...]`选择器

#### Responsive

响应式
- sm: ≥ 640px
- md: ≥ 768px
- lg: ≥ 1024px
- xl: ≥ 1280px
- 2xl: ≥ 1536px


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




### Plugin

自定义插件Plugin

#### addBase

添加基础样式


#### addComponents

添加组件类

#### addUtilities

添加工具类

#### addVariant
```jsx
// 应用插件
module.exports = {
  plugins: [
    plugin(function ({ addVariant }) {
      addVariant("disabled", "&:disabled");
    }),
  ],
};

// 使用变体
<button class="disabled:bg-gray-400" disabled>
  禁用按钮
</button>
```
添加变体



### Theme

#### Variable
```yaml
theme variable:
    --color:
    --text:
```

主题变量
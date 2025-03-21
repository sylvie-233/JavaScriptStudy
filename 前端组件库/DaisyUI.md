# DaisyUI


## 基础介绍

TailwindCss组件样式库

### tailwind.config.js
```yaml
tailwind.config.js:
    daisyui:
        themes:
            dark:
            light:
    plugins: 
        require("daisyui"):
```


## 核心内容
```yaml

```


### Theme
```jsx
// 配置主题
module.exports = {
  daisyui: {
    themes: [
      {
        mytheme: {
          "primary": "#ff0000",
          "secondary": "#00ff00",
          "accent": "#0000ff",
          "neutral": "#3d4451",
          "base-100": "#ffffff",
        },
      },
    ],
  },
};

// 应用主题
<html data-theme="dark">
  <button class="btn btn-primary">按钮</button>
</html>
```


主题
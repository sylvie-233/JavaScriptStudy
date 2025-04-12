# fullpage.js


## 基础介绍


js全屏滚动库

基础使用：
```jsx
<div id="fullpage">
    <div class="section">Section 1</div>
    <div class="section">Section 2</div>
    <div class="section">Section 3</div>
    <div class="section">Section 4</div>
</div>

<script>
    new fullpage('#fullpage', {
        // 配置选项
        autoScrolling: true,
        scrollHorizontally: true
    });
</script>
```



## 核心内容
```yaml
fullpage.js:
    fullpage:
        options: # 配置
            anchors: # 配置每个 section 的锚点，用于页面跳转
            autoScrolling: # 是否启用自动滚动（默认启用）
            navigation: # 是否启用导航栏，提供页面导航的按钮和指示器
            navigationTooltips:
            sectionsColor: # 设置每个 section 的背景色
            scrollHorizontally: # 是否启用横向滚动（默认禁用）
            afterLoad():
            onLeave():
```
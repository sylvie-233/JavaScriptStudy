# mockjs


## 基础介绍

Mock假数据生成
预设占位符


## 核心内容
```yaml
mockjs:
    Mock:
        Random:
            integer():
        mock(): # 生成假数据
            list:
```


### Mock
```js
// 生成mock数据
const data = Mock.mock({
  // 生成 5-10 个元素
  'list|5-10': [{
    'id|+1': 1,          // 自增 ID
    'name': '@cname',    // 中文姓名
    'age|18-60': 1,      // 18-60 岁
    'gender|1': ['男', '女'], // 性别
    'email': '@email',   // 邮箱
    'address': '@county(true)' // 地址
  }]
})

// 
```


### 占位符
```yaml
占位符:

```
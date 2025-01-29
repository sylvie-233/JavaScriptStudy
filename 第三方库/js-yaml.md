# js-yaml

## 基础介绍

js yaml配置解析


## 核心内容
```yaml
js-yaml:
    load():
```


### yaml
```yaml
# 对象
key: value
key: {k1:v1, k2:v2}
obj:
    k1: v1
    k2: v2


# 序列
key:
    - v1
    - v2
key: [v1, v2]
array:
-
    k1: v1
    k2: v2

# 锚点（&：建立锚点；*：引用锚点；<<：配置合并）
default: &case1
    k1: v1:

test:
    <<: *case1


# 复合key
?
    k1
    k2
:
    v
```
Yet Another Markup Language

数据类型：object、array、scalar
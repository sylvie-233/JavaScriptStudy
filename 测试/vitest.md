# vitest

`vitest官方文档：https://vitest.dev/guide/features.html#mocking`


## 基础介绍

js、ts测试框架，vite同作者

测试文件`.test.ts、.spec.ts`、测试套件`describe()`、测试用例`it()、test()`、断言`expect()`、模拟`mock()`



### vitest
```yaml
vitest: # 默认监听
    --config: # 指定配置文件
    --help:
    --standalone:
    run: # 运行测试（默认不监听文件）
        --coverage: 
        --https:
        --port:
    watch:
```


#### vitest.config.ts
```yaml
vitest.config.ts:
    test:

```


## 核心内容
```yaml
vitest:
    config:
        defineConfig(): # 定义vitest配置
        defineWorkspace(): # 定义工作空间配置
        mergeConfig(): # 合并配置文件
    assert:
        equal():       
    describe():
        concurrent():
    expect(): # 值判断
        toBe(): # 相等判断
        toMatchSnapshot():
    it():
        concurrent(): # 并发运行测试
    test(): # 测试用例
```


### Test Filtering


测试过滤、分组


### Workspace
```yaml
vitest.workspace.ts:
    test:
        environment:
        name:
        root:
        setupFiles:
```

`vitest.workspace.ts`: 工作空间配置文件
工作空间
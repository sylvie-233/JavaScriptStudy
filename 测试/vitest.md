# vitest

`vitest官方文档：https://vitest.dev/guide/features.html#mocking`


## 基础介绍

js、ts测试框架，vite同作者

测试文件`.test.ts、.spec.ts`、测试套件`describe()`、测试用例`it()、test()`、断言`expect()`、模拟`mock()`

对于路径别名、tsconfig.json、vitest.config.ts中都要配置和包含


vscode中调试vitest：launch.json
```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "type": "node",
            "request": "launch",
            "name": "Debug Vitest",
            "runtimeExecutable": "vitest",
            "console": "integratedTerminal",
          }
    ]
}
```


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
        alias: # 路径别名
        environment: # 测试环境配置
        globals: # 使用全局测试方法
        include: # 测试文件包含
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
    describe(): # 测试模块分组
        concurrent():
    expect(): # 测试断言
        toBe(): # 相等判断
        toMatchSnapshot():
    it(): # 测试用例
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
# Jest

`jest官方文档：https://jestjs.io/docs/getting-started`

## 基础介绍


javascript测试库

`ts-jest`：支持typescript测试


测试文件`.test.js`、测试套件`describe()`、测试用例`it()、test()`、断言`expect()`、模拟`mock()`

`.test.js`测试文件


### Jest
```yaml
jest:
    --coverage: # 测试覆盖率
    --watch: # 监听文件变化
```


#### jest.config.js
```yaml
jest.config.js:
    globals:
    preset: # 环境预设
        ts-jest:
    testEnvironment: # 测试环境
        node:
    transform: # 文件转换，Jest默认只支持js，支持ts（'^.+\\.ts$': 'ts-jest'）
```


## 核心内容
```yaml
jest:
    globals: # jest全局函数 @jest/globals
        jest:
            mock():
        afterAll():
        afterEach():
        beforeAll():
        beforeEach():
        describe(): # 测试模块
            each():
        expect(): # 测试断言、测试值传递
            not: # 否定
            rejects:
            resolves:
            toBe():
            toBeCloseTo():
            toBeFalsy():
            toBeGreaterThen():
            toBeNull():
            toBeTruthy():
            toBeUndefined():
            toContain(): # 数组包含
            toEqual(): # 判断值相等
            toHaveBeenCalled():
            toHaveBeenCalledTimes():
            toHaveBeenCalledWith():
            toMatch():
            toStrictEqual():
        test(): # 测试函数
            each():
    Config:
        automock:
    fn():
        mock:
            calls:
            results:
        mockResolvedValueOnce():
```
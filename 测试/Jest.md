# Jest

`jest官方文档：https://jestjs.io/docs/getting-started`

## 基础介绍


javascript测试库

测试文件`.test.js`、测试套件`describe()`、测试用例`it()、test()`、断言`expect()`、模拟`mock()`

`.test.js`测试文件


### Jest
```yaml
jest:
    --watch: # 监听文件变化
```


## 核心内容
```yaml
jest:
    globals: # @jest/globals
        jest:
        afterAll():
        afterEach():
        beforeAll():
        beforeEach():
        describe():
            each():
        expect():
            not:
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
        test():
            each():
    Config:
        automock:
    fn():
```
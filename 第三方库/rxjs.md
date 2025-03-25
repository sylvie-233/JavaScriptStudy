# rxjs


## 基础介绍

javascript 响应式、异步编程库
基于观察者模式，通过创建和操作 observable（可观察对象）来处理异步操作、事件、异步请求等
- Observable（可观察对象）
- Observer（观察者）
- Operator（操作符）
- Subscription（订阅）

## 核心内容
```yaml
rxjs:
    index:
    operators: # 流式操作符
        catchError():
        debounceTime():
        distinctUntilChanged():
        filter(): # 过滤
        findIndex():
        map(): # 数值转换
        merge(): # 合并流
        observeOn():
        reduce():
        retry():
        scan(): # 迭代
        switchMap():
        tap():
        take():
        takeUntil():
    testing:
        TestScheduler:
    Observable: # 核心类 可观测对象
        subscribe: # 数据生成
            complete(): # 结束响应
            next(): # 传递值
        ---
        forEach():
        lift():
        pipe(): # 管道流，应用操作符
        subscribe(): # 数据订阅
            complete():
            error(): # 
            next(): # 处理数据
            ---
            unsubscribe(): 取消订阅
    Subject: # 类似Observable，用于一值多播
    asyncScheduler():
    from(): # 普通对象 创建Observable
    fromEvent(): # 根据DOM事件 创建Observable
    interval(): # 定时器 创建Observable
    of(): # 字面量 创建Observable
    timer():

```



### Observable
```js
const observable = new Observable(subscriber => {
  subscriber.next(1);
  subscriber.next(2);
  subscriber.next(3);
  setTimeout(() => {
    subscriber.next(4);
    subscriber.complete();
  }, 1000);
})
```

可观测对象、数据流


### Observer
```js
// 创建观察者
const observer = {
  next: x => console.log('Observer得到值: ' + x),
  error: err => console.error('Observer得到错误: ' + err),
  complete: () => console.log('Observer完成')
};

// 观察者订阅
const subscription = observable.subscribe(observer);

// 取消订阅
subscription.unsubscribe();
```
观测者对象


### Operator
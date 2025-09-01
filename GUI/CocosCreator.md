# Cocos Creator

``

## 基础介绍

国产2D游戏开发引擎

Scene -> Node -> Component
Canvas -> UI


- Node节点是一个物体的基础属性
- Component组件的事件最终都会挂载到它所属的 Node 上


### 安装目录
```yaml
CocosDashboard:
    /resources:
        app.asar:
        cocos.asar:
        dashboard.json:
        default_app.asar:
```

CocosDashboard是用Electron框架写的界面


#### 项目结构
```yaml
Cocos Creator:
    /assets:
        /prefabs:
        /resources:
        /scenes:
        /scripts:
        /sounds:
    /library:
    /settings:
    /temp:
    /extensions:
    package.json:
    tsconfig.json:
```


## 核心内容
```yaml
cc:
    _decorator: # 装饰器
        @ccclass: # 类
        @disallowMultiple:
        @property: # 属性
    animation:
        AnimationController: # 动画控制器
    assetManager: # 资源管理器
        loadBundle(): # 加载Bundle资源
    director: # 场景管理
        getCollisionManager():
        getScene():
        loadScene(): # 加载场景 
        preloadScene(): # 预加载场景
    game: # 全局对象
        addPersistRootNode(): # 添加持久化节点
        removePersistRootNode(): # 添加持久化节点
    geometry: # 几何
        AABB:
        Plane:
    input: # 输入系统
        on(): # 输入事件监听
    loader: # 资源加载
        loadRes():
        loadResDir():
    math: # 数学
        Vec2: # 二维向量
    macro:
        KEY: # 键盘按键
    native: # 原生平台
        fileUtils: # 文件操作工具
            getStringFromFile():
            getWritablePath():
            isFileExist():
            writeStringToFile(): # 本地文件写入
    physics: # 物理系统
        CharacterController: # 人物控制器
            BoxCharacterController:
        Collider: # 3D碰撞体
            BoxCollider: # 盒型碰撞体
            CapsuleCollider:
            CircleCollider:
        PhysicsMaterial: # 物理材质
        RigidBody: # 刚体
    renderer: # 渲染
        scene: # 
            Camera: # 相机
    resources: # 资源
        load(): # 资源加载 /assets/resources
        release():
    sp:
        spine:
            Animation:
    sys:
        isNative:
        localStorage: # 本地数据存储
            getItem():
            removeItem():
            setItem():
    systemEvent: # 系统事件（键盘、鼠标、触摸）
        on():
    tween: # 补间动画
        by(): # 相对变化
        call(): # 在补间中插入回调
        delay(): # 延迟一段时间
        repeat(): # 重复执行
        repeatForever(): # 无限循环
        sequence(): # 串联多个补间
        start():
        to(): # 在指定时间内过渡到某个属性值
    Animation: # 动画
        play():
    Animator: # 动画状态机
        setTrigger():
        setValue():
    AssetManager: # 资源管理器
    Atlas: # 图集资源
    Camera: # 摄像机
        clearFlags: # 清除标记
        projection: # 投影方式
    CCObject:
        Asset: # 资源
            AnimationClip:
            AudioClip:
            Mesh: # 贴图
            Prefab: # 预制体
            SpriteAtlas: # 精灵图集
                getSpriteFrame():
            SpriteFrame:
        Component: # 组件
            enable: # 组件启用
            node: # 获取当前组件挂载的节点
            getComponent():
            onCollisionEnter():
            onCollisionExit():
            onCollisionStay():
            schedule(): # 定时器
            start():
            ---
            Animation: # 动画
            AudioSource: # 音频
                loop:
                pause():
                play():
                playOneShot():
                stop():
            Button: # 按钮
            Collider2D: # 2D碰撞体

                on(): # 事件监听
                ----
                BoxCollider2D:
                CircleCollider2D:
                PolygonCollider2D: # 2D 多边形碰撞体
            Layout: # 布局
            Light: # 灯光
            ProgressBar: # 滚动条
            Renderer:
                UIRenderer: # UI
                    Label: # 标签
                    Sprite: # 精灵图
                        sizeMode:
                        spriteFrame: # 图片
                        type: # 类型
            RigidBody2D: # 2D刚体
                linearVelocity: # 线性速度
            RenderRoot2D:
                Canvas: # 画布
            SafeArea: # 安全区域
            TiledMap: # 瓦片地图
            UITransform: # 
            ViewGroup: # 视图组
                ScrollView: # 滚动视图
                    PageView:   
            VideoPlayer: # 视频播放器
                pause():
                play():
                stop():
            Widget: # 控件
        Node: # 节点
            active: # 激活节点
            anchorX:
            children: # 子节点
            color:
            parent: # 父节点
            position: # 位置
            ratation:
            scala:
            x:
            y:
            addComponent(): # 添加组件
            emit(): # 发送自定义事件
            destroy():
            dispatchEvent(): # 分发事件
            getChildByName():
            getParent(): # 父节点
            on(): # 节点事件监听
            removeAllChildren():
            removeChild():
            removeFromParent():
            runAction(): # （已被Tween代替）
            setPosition(): # 设置位置
            stopAction():
            ---
            Scene: # 场景
            EventType: # 事件类型
                MOUSE_DOWN:
                MOUSE_MOVE:
                MOUSE_UP:
                TOUCH_CANCEL:
                TOUCH_END:
                TOUCH_MOVE:
                TOUCH_START:
    Color:
    Contact2DType: # 
        BEGIN_CONTACT:
    Director:
    ERaycast2DType:
    Event: # 事件
        EventCustom: # 自定义事件
        EventMouse: # 鼠标事件
            BUTTON_LEFT:
    EventHandler: # 事件处理
    EventKeyboard:
    EventTarget: # 自定义事件对象
        emit():
        off():
        on():
    ICollisionEvent: # 碰撞事件
        otherCollider:
    Input: # 输入系统
        EventType: # 输入事件类型
            KEY_DOWN:
    IPhysics2DContact:
    KeyCode: # 
    Layers: # 图层
    RaycastResult2D: # 射线结果
        collider:
        normal:
        point:
    Renderer: # 渲染
        ModelRenderer: # 模型渲染
            ParticleSystem: # 粒子系统
    System:
        PhysicsSystem2D: # 2D物理系统
            raycast(): # 射线
        View:
    SystemEvent:
    Tween: # 补间动画
    UI:
    find(): # Node节点查找（绝对路径）
    instantiate(): # 实例化预制体
    moveTo():
    v2(): # Vec2
```



### Script

JavaScript & TypeScript 脚本

脚本以组件的形式挂载到Node节点上 


#### LifeCycle

生命周期
- onLoad(): 初始化加载
- onEnable():
- start():
- update(): 更新
- lateUpdate():
- onDisable():
- onDestroy():



### Node

支持事件监听机制




#### Scene

场景

#### Camera

摄像机


#### Event

事件


##### EventTarget

自定义事件



### Component


#### TiledMap

瓦片地图

#### Lighting





### Asset

#### Prefab

预制体

#### Audio


##### AudioSource

音频播放器

##### AudioClip

#### Video

##### VideoPlayer

视频播放器


### Input


#### SystemEvent

系统输入事件


### UI

#### Canvas

画布


#### Layout

布局

#### Widget

锚点定位


#### ViewGroup

##### ScrollView

滚动视图

##### PageView


##### SafeArea 

安全区域





#### Button

按钮

#### ToggleContainer

开关容器

##### Toggle

开关

#### EditBox

输入框

#### Sprite

精灵图

#### Label

标签



### Animation


#### Animator

动画状态机



#### Tween

补间动画












### Physics

物理系统 = 刚体(重力、速度) + 碰撞体(碰撞检测)

物理系统事件
- onBeginContact / onCollisionEnter ： 碰撞开始
- onEndContact / onCollisionExit ： 碰撞结束
- onPreSolve / onCollisionStay ： 碰撞持续
- onPostSolve ： 碰撞结果
- onTriggerEnter ：触发器模式 碰撞开始


#### RigidBody

刚体

##### RigidBody2D

2D刚体

#### Collider

碰撞体


##### BoxCollider2D

盒型碰撞体

##### CircleCollider2D 

圆形碰撞体

##### PolygonCollider2D

多边形碰撞体


### Particle


#### ParticleSystem

粒子系统


### Shader


### Network

- HTTP：fetch()
- WebSocket：Socket.io
- Socket：
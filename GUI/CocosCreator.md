# Cocos Creator

`Cocos Creator零基础小白超神教程: P43`

## 基础介绍

国产2D游戏开发引擎

Node -> Component


- Node节点是一个物体的基础属性


## 核心内容
```yaml
cc:
    _decorator: # 装饰器
        @ccclass: # 类
        @disallowMultiple:
        @property: # 属性
    animation:
        AnimationController: # 动画控制器
    director: # 场景
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
    loader: # 资源加载
        loadRes():
        loadResDir():
    math: # 数学
        Vec2: # 二维向量
    macro:
        KEY: # 键盘按键
    physics: # 物理系统
        CharacterController: # 人物控制器
            BoxCharacterController:
        Collider: # 碰撞体
            BoxCollider: # 盒型碰撞体
            CapsuleCollider:
            CircleCollider:
        PhysicsMaterial: # 物理材质
        RigidBody: # 刚体
    renderer: # 渲染
        scene: # 
            Camera: # 相机
    sp:
        spine:
            Animation:
    Atlas: # 图集资源
    CCObject:
        Asset: # 资源
            AnimationClip:
            AudioClip:
            Mesh: # 贴图
            Prefab: # 预制体
            SpriteAtlas: # 精灵图集
                getSpriteFrame():
            SpriteFrame:
        Collider2D:
            PolygonCollider2D: # 2D 多边形碰撞体
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
            AudioSource:
            Button: # 按钮
            Layout: # 布局
            Light: # 灯光
            Renderer:
                UIRenderer: # UI
                    Label: # 标签
                    Sprite: # 精灵图
                        sizeMode:
                        spriteFrame: # 图片
                        type: # 类型
            RenderRoot2D:
                Canvas: # 画布
            ViewGroup: # 视图组
            VideoPlayer: # 视频播放器
            Widget: # 控件
        Node: # 节点
            active: # 激活节点
            anchorX:
            children: # 子节点
            color:
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
            on(): # 事件监听
            removeAllChildren():
            removeChild():
            removeFromParent():
            setPosition():
            ---
            Scene: # 场景
            EventType: # 事件类型
                MOUSE_DOWN:
    Color:
    Event: # 事件
        EventCustom: # 自定义事件
        EventMouse: # 鼠标事件
            BUTTON_LEFT:
    EventHandler: # 事件处理
    Input: # 输入系统
    Layers: # 图层
    UI:
    System:
        View:
    Tween: # 补间动画
    systemEvent: # 系统事件
        on():
    find(): # Node节点查找（绝对路径）
    instantiate(): # 实例化预制体
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

#### Event

事件

#### Camera

摄像机


### Component




#### Lighting





### Asset

#### Prefab

#### Audio

#### Video


### Input


### UI


#### Layout

布局


#### ViewGroup



##### View


#### Widget


#### Canvas

画布


#### Button

按钮

#### Sprite

精灵图

#### Label

标签



### Animation



### Tween

补间动画












### Physics


#### RigidBody

刚体



#### Collider


碰撞体



### Particle





### Shader


### Network
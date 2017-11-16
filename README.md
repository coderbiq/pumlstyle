通过对 [PlantUML](http://plantuml.com/) 的风格扩展定义一套用于开发领域驱动设计（DDD）的设计语言。



## 安装

在 [PlantUMl](http://plantuml.com/) 设计图中通过 `!includeurl https://elvis-bi.github.io/pumlstyle/ddd.puml` 指令加载风格扩展文件：

```
@startuml
!includeurl https://elvis-bi.github.io/pumlstyle/ddd.puml

...
@enduml
```



## 使用

通过下面提供的这些命令方法即可以创建出指定的领域模型。



**当前支持的模型创建方法**

| 方法                                       | 用途      |
| ---------------------------------------- | ------- |
| dddRoot(name, label = null, type = class) | 创建聚合根模型 |
| dddValueObject(name, label = null, type = class) | 创建值对象模型 |
| dddEntity(name, label = null, type = class) | 创建实体模型  |
| dddRepository(name, label = null, type = interface) | 创建仓库模型  |
| dddEvent(name, label = null, type = class) | 创建事件模型  |
| dddService(name, label = null, type = class) | 创建服务模型  |
| dddFactory(name, label = null, type = class) | 创建工厂模型  |



**例如：标记聚合根模型**

```
@startuml
!includeurl https://elvis-bi.github.io/pumlstyle/ddd.puml


' 创建聚合根模型
dddRoot(root1)

' 创建聚合根并指定显示名称和内部结构
dddRoot(root2, "我是聚合根") {
    String name
}

' 创建值对象模型
dddValueObject(valueObject)

' 创建实体模型
dddEntity(我是实体)

' 创建仓库模型
dddRepository(repository)

' 创建领域事件模型
dddEvent(event)

' 创建领域服务模型
dddService(领域服务)

' 创建工厂模型
dddFactory(工厂)

root1 --> valueObject
root1 -> 我是实体
repository -> root1

@enduml
```


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

目前主要提供通过类图的 "<<" 和 ">>" 关键字来标识出 DDD 中的模型类型，后期还会针对每种模型类型增加自定义的显示风格。



**当前支持的模型类型**

| 类型          | 显示值  |
| ----------- | ---- |
| Root        | 聚合根  |
| ValueObject | 值对象  |
| Entity      | 实体   |
| Repository  | 仓库   |
| Event       | 事件   |
| Service     | 服务   |
| Factory     | 工厂   |



**例如：标记聚合根模型**

```
@startuml
!includeurl https://elvis-bi.github.io/pumlstyle/ddd.puml

' 通过 <<Root>> 标识当前创建的 class 是一个 DDD 中的聚合根模型
' 在图形渲染的时候这个 class 会被标识为"聚合根"
class Abc <<Root>>
@enduml
```


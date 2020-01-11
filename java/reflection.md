# 反射 Reflectin
每加载一种`class` 就生成一个 `Class`类型的实例 来进行关联。`Class`实例由JVM内部创建，由于JVM为每个加载的`class`创建了对应的`Class`实例，并在实例中保存了该`class`的所有信息，包括类名、包名、父类、实现的接口、所有方法、字段等，因此，如果获取了某个`Class`实例，我们就可以通过这个`Class`实例获取到该实例对应的`class`的所有信息。  

这种通过`Class`实例获取`class`信息的方法称为反射（Reflection）。

* 通过 `==`来精确判断一个类型是不是`class`实例。
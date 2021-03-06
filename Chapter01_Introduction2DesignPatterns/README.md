[TOC]

## 第一章 设计模式简介
### 1.1 课程目标
* 理解松耦合设计思想
* 掌握面向对象设计原则
* 掌握重构技法改善设计
* 掌握GOF核心设计模式

### 1.2 什么是设计模式
> "每一个模式描述了一个在我们周围不断重复发生的问题以及该问题的解决方案核心。这样你就能一次又一次的使用该方案而不必做重复劳动"。——Christopher Alexand
* 不需要重复造轮子

### 1.3 GOF 设计模式
* 《设计模式：**可复用**面向对象软件设计基础》
    * 目标是**可复用**
    * 面向对象是方法
    * 书中介绍了23种经典的面向对象设计模式
    * GOF：Gang of Four (四人组)
    * 确立了模式在软件设计中的地位
    <br>
* 通常所说的设计模式隐含的表示为面向对象的设计模式
    * 但是设计模式**并不等于"面向对象设计模式"**
    * 有非面向对象的设计模式，如：
        * 架构模式
        * 数据库领域数据库模式 

### 1.4 从面向对象谈起
> 底层思维 <-> 程序员 <-> 抽象思维

#### 1.4.1 底层思维：向下，如何把握机器底层
* 语言构造
* 编译转换
* 内存模型
* 运行时机制
    * 异常处理
    * 垃圾回收

#### 1.4.2 抽象思维：向上，如何将我们的周围世界抽象为程序代码
> 世界抽象为程序代码
* 面向对象
* 组件封装
* 设计模式
* 架构模式

#### 1.4.3 抽象思维和底层思维关系
* 两者都很重要
* 没有底层思维，写出的代码质量不高，性能不好
* 抽象思维可以很好地帮助管理代码复杂度
* 设计模式课程更偏向抽象思维的学习与理解

### 1.5 深入理解面向对象
#### 1.5.1 向下:深入理解三大面向对象机制(底层思维)
* 封装:隐藏内部实现
* 继承:复用现有代码
* 多态:改写对象行为

#### 1.5.2 向上:深刻把握面向对象机制的抽象意义(抽象思维)
* 理解如何使用这些机制来表达现实世界
* 掌握什么是"好的面向对象设计"

### 1.6 软件设计固有的复杂性
#### 1.6.1 软件设计复杂的根本原因
* 变化
    * 客户需求变化
    * 技术平台变化
    * 开发团队变化
    * 市场环境变化
    * ...
 
#### 1.6.2 如何解决复杂性
##### 分解
* 人们面对复杂性有一个常见的作法:**分而治之**
##### 抽象
* 更高层次来讲,人们处理复杂性有个通用的技术,即**抽象**
* 由于不能掌握全部的复杂对象,我们选择忽视它的非本质细节,而去处理泛化和理想化的模型
##### 分析Point画线段,矩形,圆的示例代码
* 该示例程序显示抽象较分解模式更加能够适应用户需求变化

### 1.7 软件设计的目标
* 什么是好的软件设计?软件设计的金科玉律: **复用性**

### 1.8 GOF-23 模式分类

#### 1.8.1 从目的来看

* **创建型（Creational）模式**
    > 将对象的部分创建工作延迟到子类或者其他对象，从而应对需求变化为对象创建时具体类型实现引来的冲击。
  
* **结构型（Structual）模式**
    > 通过类继承或者对象组合获得更灵活的结构，从而应对需求变化为对象的结构带来的冲击。

* **行为型（Behavioral）模式**
    > 通过类继承或者对象组合来划分类与对象间的职责，从而应对需求变化为多个交互的对象带来的冲击。

#### 1.8.2 从范围来看

* **类模式处理类与子类的静态关系**
    > 更倾向于继承方案
* **对象模式处理对象间的动态关系**
    > 更倾向于组合方案，一个类包含另外一个类的对象或引用（指针）

### 1.9 李建忠分类方案
#### 1.9.1 组件协作
> 主要解决类间协作问题
> 现代软件专业分工之后的第一个结果是“框架与应用程序的划分”，**“组织协作”模式通过晚绑定，来实现框架与应用程序间的松耦合**，是二者之间协作的常用模式。
* Template Method
* Strategy
* Observer / Event
    <br>
#### 1.9.2 单一职责
> 主要解决类间责任划分问题
> 在软件组件的设计中，如果责任划分的不清晰，使用继承得到的结果往往是随着需求的变化，子类急剧膨胀，同时充斥着重复代码，这时候的关键是划清责任。
* **Decorator**
* **Bridge**
    <br>
#### 1.9.3 对象创建
> 主要解决对象创建过程依赖关系问题
* **Factory Method**
* **Abstract Factory**
* **Prototype**
* **Builder**
    <br>

#### 1.9.4 对象性能
> **主要解决性能问题**
* **Singleton**
* **Flyweight**
    <br>

#### 1.9.5 接口隔离
* **Facade**
* **Proxy**
* **Mediator**
* **Adapter**
    <br>

#### 1.9.6 状态变化
* **Memento**
* **State**
    <br>

#### 1.9.7 数据结构
* **Composite**
* **Iterator**
* **Chain of Responsibility**
    <br>

#### 1.9.8 行为变化
* **Command**
* **Visitor**
    <br>

#### 1.9.9 领域问题
* **Interpreter**

### 1.10 重构获得模式 Refactoring to Patterns
* 面向对象设计模式是“好的面向对象设计”，所谓“好的面向对象设计”指是那些可以满足 “**应对变化，提高复用**”的设计 。
    <br>
* 现代软件设计的特征是“需求的频繁变化”。设计模式的要点是“**寻找变化点，然后在变化点处应用设计模式**，从而来更好地应对需求的变化”.“**什么时候、什么地点应用设计模式**”比“理解设计模式结构本身”更为重要。
    <br>

* **设计模式的应用不宜先入为主，一上来就使用设计模式是对设计模式的最大误用**。没有一步到位的设计模式。敏捷软件开发实践提倡的“Refactoring to Patterns”（迭代修正得到模式）是目前普遍公认的最好的使用设计模式的方法。  

### 1.11 推荐图书
* 《重构——改善既有代码的设计》
    > 《Refactoring Improving the Design of Exsting Code》
* 《重构与模式》
    > 《Refactoring to Patterns》

### 1.12 重构关键技法
* **静态** -> **动态**
* **早绑定** -> **晚绑定**
* **继承** -> **组合**
* **编译时依赖** -> **运行时依赖**
* **紧耦合** -> **松耦合**
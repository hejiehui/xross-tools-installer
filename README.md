# 简介
xross-tools-installer将安装X-Series工具集。X-Series是一套轻量级的框架。包含好几个工具，各自解决不同场景的共性问题。每个工具都拥有基于Eclipse的图形化编辑器和基于标准maven依赖的运行时引擎。他们具有以下特点：
* 易于使用。基于图形化界面，操作直观，容易理解
* 易于集成。基于maven依赖，可以直接引入到项目
* 易于测试。相关组件的接口经过精心设计，基本上都是函数式接口。组件之间的交互清晰，方便单元测试。部分工具可以直接生成单元测试代码
* 最合适的。所有的功能都经过精心挑选，没有一丝多余的功能。尽可能做到专注和精简。

X-Series试图解决大规模软件开发难题，包括：
* 沟通。如何准确有效的描述系统的静态和动态
* 文档。如何保障文档始终反应系统最新的状态
* 学习曲线。新手如何快速理解系统

X-Series能够达到的效果：
* 降低开发成本。减少90%的系统设计开发工作；分离模型与代码，大幅降低系统复杂度和维护成本
* 提高开发效率。组件化设计，流水线式开发；与开发环境高度集成
* 保障软件质量。把高内聚，低耦合落到实处

### 更多说明
[解锁进入千万级代码系统的正确姿势](https://v.qq.com/x/page/c0340vrpod1.html)

X-Series 精简版介绍[X-Series V2.pptx](https://github.com/hejiehui/xross-tools-installer/blob/master/doc/X-series%20V2.pptx)

X-Series 详细版介绍[x-series中文.pptx](https://github.com/hejiehui/xross-tools-installer/blob/master/doc/X-Series%20-%20%E4%B8%AD%E6%96%87.pptx)

X-Series 详细版介绍[x-series中文.pdf](https://github.com/hejiehui/xross-tools-installer/blob/master/doc/X-Series%20-%20%E4%B8%AD%E6%96%87.pdf)

[X-Series企业级开发实践](https://zhuanlan.zhihu.com/p/27289061)

[用xstate实现金服业务流程动态化 ](http://mp.weixin.qq.com/s/neptecSgeceSHXwDSWQ3FQ)

[提高系统开发效率的“银弹”——X-series可视化大规模应用开发工具集 ](http://blog.csdn.net/ctrip_tech/article/details/53337622)

### 发布历史
[Release Notes](https://github.com/hejiehui/xross-tools-installer/wiki/Release-Notes)

### xUnit
Xross unit可以用来：

* 开发和具体服务无关的通用处理流程，比如接收到请求后的通用处理，例如，平台特定请求到领域模型的映射，用户身份认证，处理转发，统一输出处理等
* 组织系统顶层服务。在处理转发下层，按照业务需求创建的多个具体业务处理。

具体模型即可用放在同一个文件；也可以分开放置，如果放在一起整体显得太大的话

[xunit](https://github.com/hejiehui/xUnit)

![xunit](https://static.oschina.net/uploads/img/201707/03184917_7GR5.png)

Xross unit同时还支持IDEA版本

![xunit](https://oscimg.oschina.net/oscnet/up-c3ae7017420fd4551452f03e911a6ef89ab.png)

### xDecision
Xross Decision是商业智能领域常用的决策工具

利用树形模型表达复杂的决策制定过程。

相对于传统的if/else的多层嵌套结构，xdecision可以用非常小的屏幕空间有效的描述复杂的逻辑判断，同时保持最优的可理解性

在决策因子定义没有变化的情况下，通过修改决策树模型，可以很方便快捷的修改系统决策行为，无需做代码的任何改动。无论是开发还是维护都完胜代码方式

[xdecision](https://github.com/hejiehui/xDecision)

![xdecison](https://static.oschina.net/uploads/img/201707/03184929_NSfV.png)

Xross Decision同时还支持IDEA版本

![xdecison](https://oscimg.oschina.net/oscnet/up-ba0b9c8c0df9778cb4d02e6a6f12dafa6f2.png)

### xState
Xross State是状态机编辑器。用于对状态的变迁与控制建模。

注意如果希望实现为工作流建模，请使用xstate，而不是xunit。因为：

* xunit的图比较严格。扇出节点和扇入节点都是严格对应的。工作流一般比较随意，从任意节点可以连接任意的其他节点。
* 工作流接收到一个请求后，会推动模型从当前状态/任务节点走到下个状态/任务节点。xunit是一个请求走完特定路径上的所有节点。两者用法差别很大用法

[xstate](https://github.com/hejiehui/xState)
![xstate](https://oscimg.oschina.net/oscnet/up-77a64e69d1d009af7b0731da86f5957c5c5.png)

### xeda
基于actor模型的微服务框架。目前还在开发中

预览
![xeda](https://static.oschina.net/uploads/img/201707/03184941_IoPy.png)

# 安装步骤
## IDEA
在Setting--Plugin里面搜索产品名称即可

Xross Unit Editor
Xross Decision Tree Edtitor
Xross State Machine Edtitor

如果无法从IDEA里面安装，可以访问如下网址下载：

[Xross Unit Editor](https://plugins.jetbrains.com/plugin/21413-xross-unit-editor）
[Xross Decision Tree Edtitor](https://plugins.jetbrains.com/plugin/21527-xross-decision-tree-edtitor）
[Xross State Machine Edtitor](https://plugins.jetbrains.com/plugin/21557-xross-state-machine-edtitor）
注：Xross State Machine Edtitor目前还在审核，可能无法访问

## Eclipse
安装环境要求
推荐Eclipse版本高于：
Version: Kepler Service Release 2
Build id: 20140224-0627

JDK 1.7或以上


## 下载安装包
[XrossTools.zip](https://github.com/hejiehui/xross-tools-installer/raw/master/installer/XrossTools.zip)

或者

![1](https://static.oschina.net/uploads/img/201707/03184945_60V3.png)

## 在Eclipse里面install
![1](https://static.oschina.net/uploads/img/201707/03184948_UKWG.png)

## 定位安装包
![1](https://static.oschina.net/uploads/img/201707/03184952_pPmp.png)

## 安装
记得选项要象下面一样，否则可能无法显示产品或者耗时很长去搜索其它update site
![1](https://static.oschina.net/uploads/img/201707/03184959_nfKe.png)

## 安装成功
![1](https://static.oschina.net/uploads/img/201707/03185001_kBML.png)

# 卸载步骤
如果不想继续使用Xross Tools或者要升级Xross Tools，则需要进行卸载操作
## 点击Help-->About Eclipse
![1](https://oscimg.oschina.net/oscnet/up-e7cda455205da052928d5a1d76cfd922530.png)

## 点击Installation Detail
![1](https://oscimg.oschina.net/oscnet/up-3f993a3a013fc85f15bbfea4cebf09bf9b7.png)

## Uninstall Xross Tools
![1](https://oscimg.oschina.net/oscnet/up-8725f2fc65a9f257fc5b5d4769f9cae450a.png)

# 技术支持
QQ x-series支持群：146746429

![Tech Support](https://static001.geekbang.org/infoq/0f/0f13df5473cd9dbb337df07910a8ce5d.png)

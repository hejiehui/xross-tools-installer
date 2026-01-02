# 技术支持
QQ x-series支持群：146746429

![Tech Support](https://static001.geekbang.org/infoq/0f/0f13df5473cd9dbb337df07910a8ce5d.png)

# 简介
X-Series是一套基于可视化模型的轻量级的后端开发框架。支持基于IDEA和Eclipse的可视化编辑器和基于AI的模型生成扩展。特点包括：
* 功能齐全。支持流程图[Xross Unit](https://github.com/hejiehui/xUnit)，决策树[Xross Decision](https://github.com/hejiehui/xDecision)，状态机[Xross State](https://github.com/hejiehui/xState)，行为树[Xross Behavior](https://github.com/hejiehui/xBehavior)，工作流[Xross Flow](https://github.com/hejiehui/xFlow)
* 直观易懂。可视化模型容易理解，交流，操作直观
* 安装简便。可直接从IDEA插件市场下载安装。引擎通过maven导入
* 易于开发。引擎负责调度，研发只需实现最简单的功能接口，从设计上保障高内聚，低耦合。支持工厂类代码生成
* 易于测试。大部分工具可生成单元测试代码框架，仅需简单填空
* 功能精简。所有的功能都经过精心挑选，没有一丝多余的功能。尽可能做到专注和精简。

X-Series试图解决大规模软件开发难题，包括：
* 沟通。如何准确有效的描述系统的静态和动态
* 文档。如何保障文档始终反映系统最新的状态
* 学习曲线。新手如何快速理解系统

X-Series能够达到的效果：
* 降低开发成本。减少90%的系统设计开发工作；分离模型与代码，大幅降低系统复杂度和维护成本
* 提高开发效率。组件化设计，流水线式开发；与开发环境高度集成
* 保障软件质量。把高内聚，低耦合落到实处

### 更多说明
小红书号：42941729994

[B站视频：低代码框架x-series介绍及应用案例](https://www.bilibili.com/video/BV1R64y127QZ/)

[腾讯视频：解锁进入千万级代码系统的正确姿势](https://v.qq.com/x/page/c0340vrpod1.html)

[B站合集·面向后端低代码工具集X-Series](https://space.bilibili.com/472310927/lists/3326246?type=season)

[知乎个人主页](https://www.zhihu.com/people/hejiehui-73/posts)

[掘金个人主页](https://juejin.cn/user/1163731741704600/posts)

[InfoQ个人主页](https://www.infoq.cn/profile/9DEED95B45AB57/publish)

ArchSummit分享：[低代码框架x-series介绍与实践.pptx](https://github.com/hejiehui/xross-tools-installer/blob/master/doc/%E4%BD%8E%E4%BB%A3%E7%A0%81%E6%A1%86%E6%9E%B6x-series%E4%BB%8B%E7%BB%8D%E4%B8%8E%E5%AE%9E%E8%B7%B5-ArchSummit.pptx)

K+峰会分享：[软件研发困境与x-series落地实践.pptx](https://github.com/hejiehui/xross-tools-installer/blob/master/doc/%E8%BD%AF%E4%BB%B6%E7%A0%94%E5%8F%91%E5%9B%B0%E5%A2%83%E4%B8%8Ex-series%E8%90%BD%E5%9C%B0%E5%AE%9E%E8%B7%B5-K%2B%E5%B3%B0%E4%BC%9A.pptx)

[单元测试落地指北.pptx](https://github.com/hejiehui/xross-tools-installer/blob/master/doc/%E5%8D%95%E5%85%83%E6%B5%8B%E8%AF%95%E8%90%BD%E5%9C%B0%E6%8C%87%E5%8C%97.pptx)

[后端低代码工具X-Series线下培训介绍](https://juejin.cn/post/7350971151131344959)

X-Series 精简版介绍[X-Series V2.pptx](https://github.com/hejiehui/xross-tools-installer/blob/master/doc/X-series%20V2.pptx)

X-Series 详细版介绍[x-series中文.pptx](https://github.com/hejiehui/xross-tools-installer/blob/master/doc/X-Series%20-%20%E4%B8%AD%E6%96%87.pptx)

X-Series 详细版介绍[x-series中文.pdf](https://github.com/hejiehui/xross-tools-installer/blob/master/doc/X-Series%20-%20%E4%B8%AD%E6%96%87.pdf)

[X-Series企业级开发实践](https://zhuanlan.zhihu.com/p/27289061)

[用xstate实现金服业务流程动态化 ](http://mp.weixin.qq.com/s/neptecSgeceSHXwDSWQ3FQ)

[提高系统开发效率的“银弹”——X-series可视化大规模应用开发工具集 ](http://blog.csdn.net/ctrip_tech/article/details/53337622)

### Xross Unit
Xross Unit是流程图编辑器。简称xUnit。可以用来：

* 构建包含多个步骤的后端服务处理流程，例如接收到Facade层请求后，将通用格式转换为业务对象，然后进行具体的操作并输出
* 构建系统顶层通用处理流程，再利用模型的跨文件引用功能，将请求定位并转发到具体服务流程

如果希望使用工作流建模，请使用下面的xflow，而不是xunit。因为：

* 工作流在执行过程中可能会停留在需要等待或输入的节点，而流程图是接收请求后一次走完执行路径上的所有节点，不会暂停
* 流程图扇出节点和扇入节点都是严格对应，而工作流节点连接限制不严格，两者从拓扑角度来说是不一样的图形

[xUnit](https://github.com/hejiehui/xUnit)

![xUnit](https://static.oschina.net/uploads/img/201707/03184917_7GR5.png)

Xross unit同时还支持IDEA版本

![xunit](https://oscimg.oschina.net/oscnet/up-c3ae7017420fd4551452f03e911a6ef89ab.png)

### Xross Decision
Xross Decision是商业智能领域常用的决策工具。简称xDecision

利用树形模型表达复杂的决策制定过程。

相对于传统的if/else的多层嵌套结构，xdecision可以用非常小的屏幕空间有效的描述复杂的逻辑判断，同时保持最优的可理解性

在决策因子定义没有变化的情况下，通过修改决策树模型，可以很方便快捷的修改系统决策行为，无需做代码的任何改动。无论是开发还是维护都完胜代码方式

[xDecision](https://github.com/hejiehui/xDecision)

![xDecison](https://static.oschina.net/uploads/img/201707/03184929_NSfV.png)

Xross Decision同时还支持IDEA版本

![xdecison](https://oscimg.oschina.net/oscnet/up-ba0b9c8c0df9778cb4d02e6a6f12dafa6f2.png)

### Xross State
Xross State是状态机编辑器。简称xState

[xState](https://github.com/hejiehui/xState)

![xState](https://oscimg.oschina.net/oscnet/up-77a64e69d1d009af7b0731da86f5957c5c5.png)

Xross State同时还支持IDEA版本

![xstate](https://oscimg.oschina.net/oscnet/up-5414ffb4dd9461984b5fca4c13154ddccc8.png)

### Xross Behavior
Xross Behavior是行为树编辑器，简称xBehavior

[xBehavior](https://github.com/hejiehui/xBehavior)

![xBehavior](https://github.com/user-attachments/assets/ab3a8346-7335-469d-89c0-dc2e4f79c142)

Xross Behavior目前不支持Eclipse编辑器

### Xross Flow
Xross Flow是工作流编辑器。简称xFlow

[xFlow](https://github.com/hejiehui/xFlow)

![xFlow](https://github.com/user-attachments/assets/ab3686c2-00fd-417c-a8b5-d4621b486d0e)

### Xross Extension
Xross Extension是付费的插件。用于对其他编辑器进行功能增强，例如基于AI的模型生成与修改等

[xExtension](https://github.com/hejiehui/xExtension)

[xExtension视频演示](https://www.bilibili.com/video/BV1kt1WBnEr7/)

# 安装步骤
## IDEA
在Setting--Plugin里面搜索产品名称即可。比如输入Xross，在自动显示的相关产品选择要安装的

或直接访问插件页面下载：

[Xross Unit Editor](https://plugins.jetbrains.com/plugin/21413-xross-unit-editor)

[Xross Decision Tree Edtitor](https://plugins.jetbrains.com/plugin/21527-xross-decision-tree-edtitor)

[Xross State Machine Edtitor](https://plugins.jetbrains.com/plugin/21557-xross-state-machine-edtitor)

[Xross Behavior Tree Editor](https://plugins.jetbrains.com/plugin/25520-xross-behavior-tree-edtitor)

[Xross Workflow Editor](https://plugins.jetbrains.com/plugin/28043-xross-workflow-editor)

## Eclipse
注意，Eclipse版本现在处于维护阶段，目前xUnit，xState和xDecision支持Eclipse，其他暂不支持。有需要请微信，QQ或邮件联系我

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

# 联系方式
微信：hejiehui76

e-mail 常用: he_jiehui@163.com

e-mail 不常用: jerry_he_7667@hotmail.com


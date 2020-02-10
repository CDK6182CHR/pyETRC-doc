# pyETRC列车运行图系统

本文档是`pyETRC`列车运行图系统的简要用户手册。

## 概述

本项目是基于Python语言和PyQt5的非官方性质、简易的中国铁路列车运行图系统。本代码的发布遵循`GPLv3`协议。在协议允许范围内，作者保留一切权利和最终解释权。

作者联系方式：mxy0268@qq.com

本项目在Windows 10 操作系统下开发和测试。

### 与`ETRC`的联系

#### 渊源

`pyETRC`项目的最初灵感来源和很多功能设置都来自由LGuo等前辈基于java语言开发的`ETRC`列车运行图系统。为致敬开发`ETRC`项目的前辈，本项目定名为**`pyETRC`列车运行图系统**，简称为`pyETRC`。

#### 交互支持

本系统支持读取和导出`ETRC`列车运行图系统的运行图文件（`*.trc`）。但由于两软件支持的功能有差异，读取和导出过程可能造成一定的信息损失。

本系统与`ETRC`列车运行图系统的实现各有侧重。相比本系统，`ETRC`列车运行图系统有如下的特色比较突出：

* **动态运行图**。本系统不支持此功能。
* 对于精确到客运时刻的需求，**自带较完善的线路数据库和车次时刻数据库**。而本系统的线路和车次数据库依赖外部文件，且目前很不完整。
* 较完善的车次切片功能。
* 更简洁的操作和数据，或者说需要用户提供的数据更少。

相比`ETRC`列车运行图系统，本系统主要有如下的特色：

* 更准确、完整的数据支持，包括精确到秒的时刻和精确到三位小数的里程，允许上下行分设不同站点，标尺，天窗，交路等。
* 做了一定的效率优化，对较大运行图的执行效果相对更好。
* 提供了一些运行图快速微调工具和分析工具，例如调整某一站名（同时修改所有列车数据中引用的改站名），对比两运行图等。
* 在`3.0.0`版本以后，提供了路网级的数据库管理模块，可以在更高层面上管理，更方便地查看、导出区段运行图。

两系统各有长短。因此我们建议，如果有需求，可以两套系统结合使用。

## 文档注记

此文档自2020年2月9日开始维护，基于`3.0.0`及以上的版本。旧版中可能有一些地方不符合，以实际软件为准。另外，我们建议，保持使用最新版本的软件，以尽量避免各种问题。



[powered by docsify](https://docsify.js.org/)
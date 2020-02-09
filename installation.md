[返回首页](README.md)

# 安装运行指南

目前`pyETRC`列车运行图系统提供三种运行方式。

1. 使用源代码直接运行。
2. 使用egg版本发行版。
3. 使用win64发行版。

对于有一定开发基础的用户，我们建议**采用源代码方式运行**，这样可以从github上快速获得软件更新；其次推荐采用egg发行版。请注意**win64版本暂不支持使用路网管理模块**。

## 使用源代码运行

使用**源代码**方式运行本项目，需要具有以下环境。

1. `Python` 3.7及以上的版本。开发所用的版本是3.7.4.

   > 注：本项目使用了大量的`f-string`语法，该语法在`Python ` 3.6以后的版本才被支持。一些较新的代码中利用了`Python` 3.7中`dict`键值对顺序与添加顺序一致的特性。如果使用3.6.*版本，这部分代码可能出现一些问题。如果使用3.6以下版本，则会报错。

2. 下列的`Python`第三方库，都可以用`pip`安装。

   * `PyQt5`。必须。推荐使用`5.10.1`版本。
   * `xlwt`。可选。在涉及输出`.xls`的操作中需要用到。
   * `xlrd`。可选。在涉及读取.`xls`的操作中需要用到。
   * `xpinyin`。可选。在本系统`2.3.0`版本之前的线路数据库排序中用到。
   * `NetworkX`。可选。在`3.0.0`版本引入的路网数据管理中，用于以图论算法计算经由给出的路径。

3. 作者开发的另一支持库`Timetable_new`。该库需要使用github上的源代码安装。

### 第三方库安装

在安装第三方库之前，需要配置好`python`环境，并将安装目录添加到`PATH`环境变量中，安装好`pip`库。相关教程可借助搜索引擎找到。

在shell中依次执行以下命令，无报错即可。

```powershell
pip install PyQt5==5.10.1
pip install xlwt
pip install xlrd
pip install xpinyin
pip install networkx
```

### `Timetable_new`的安装

依次执行：

```powershell
git clone https://github.com/CDK6182CHR/Timetable_new
cd Timetable_new
.\install.bat
```

如果不用`git`，也可以在[链接](https://github.com/CDK6182CHR/Timetable_new)中下载并解压源代码，双击执行`install.bat`。

> 注：`install.bat`文件适合windows操作系统。如果是其他操作系统，请自行更改相关代码。

`install.bat`的代码如下。

```powershell
python setup.py build
python setup.py sdist
python setup.py install
pause
```

### 运行

运行`main.py`文件即可。

```powershell
python main.py
```

## 使用egg发行版

> egg包是可执行Python文件的打包，其作用类似于java语言中的`*.jar`文件。

使用egg发行版需安装Python环境和第三方库，但无需直接接触源代码，也无需手动安装`Timetable_new`支持库。

### 环境安装

Python环境和第三方库的安装请参阅上一节中有关内容。

### 运行

egg发行版中提供了`run.cmd`文件，运行该脚本即可。
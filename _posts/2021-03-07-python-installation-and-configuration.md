---
layout:      post
title:      ".py | 在 Windows 10 上配置 python 开发环境"
keywords:   "md"
excerpt:    "截图截到哭……"
date:        2021-03-07
categories:  post
milestoneID: 34
---

我的 python 版本之前一直停留在 3.7，目前最新已经到了 3.9。最近研究上要用一段别人写的 python 的代码，原作要求 3.6 版本的 python，所以卸载了 3.7 版本，重新安装了 3.9 和 3.6 两个版本的 python。

煽动爸妈学编程很久了，欠他们一篇教程。不论是打算不断精进者的第一门编程语言，还是浅尝辄止者打算学的唯一一门语言，python 都是一个很不错的选择。所以即便爸妈对编程可以说是毫无兴趣，我也还是把这篇教程写完了，希望能帮到其他人。因为是面向纯新手的，所以基于 Windows 10 操作系统。因为这套设置我自己也要用，处于个人偏好，所以没有直接使用 `conda`。

## ~~别看你今天闹得欢~~ 先拉个清单
- python
    - 在官网下载 `python` 解释器
    - 安装 `python` 解释器
- 虚拟环境
    - 设置环境变量
    - 用 `pip` 安装 `virtualenv` 
    - 用 `pip` 安装 `virtualenvwrapper`
    - 创建一个虚拟环境，安装 `jupyter`
- 编辑器
    - 在官网下载 `vscode`
    - 安装 `vscode` 和相关插件
    - 测试一下效果

## 教程本体

### 在官网下载 `python` 解释器

在 python 的官网上 ([https://www.python.org/downloads/](https://www.python.org/downloads/)) 下载

{% maincolumn "assets/photos/2021-03-07-python-official-website.png" "" %}

### 安装 `python` 解释器

执行下载的文件，可以看到如下图所示的界面，点击红框中的选项，因为我想更改安装路径。此处似乎也可以勾选最下面的 "Add Python 3.9 to PATH"，我安装的时候没有选，后面才发现还要手动完成这一工作。

{% maincolumn "assets/photos/2021-03-07-python-install.png" "" %}

接下来的界面里每个选项都勾选，next。

{% maincolumn "assets/photos/2021-03-07-python-next.png" "" %}

在接下来出现的界面中，选择 "Install for all users"，然后选择一个自己喜欢的安装路径。我之所以选择 `C:\Python39` 这个位置，是因为:
1. C 盘是系统盘，而且是固态硬盘，比较快；
2. 默认路径在个人文件夹里，非常难找
3. `C:\Program Files` 需要管理员权限，用 `pip` 做软件包管理不方便。

{% maincolumn "assets/photos/2021-03-07-python-install-path.png" "" %}

安装完成后进入命令提示符，输入 `py`，应该可以看到一串 python 版本信息，然后命令提示符变成 `>>>` 字样，此时就已经进入了 python 环境，可以按行运行 python 命令。输入 `exit()` 就可以退出 python。

### 设置环境变量

在 windows 的搜索框里输入 "environment variables"，没等你输完，应该就可以看到下图中的联想结果：

{% maincolumn "assets/photos/2021-03-07-environment-variable-search.png" "" %}

再按照下图，依次点击按钮，一共要做两件事:
1. 给 `Path` 变量添加 `C:\Python39` 和 `C:\Python39\Scripts` 两个新值。
2. 新建一个文件夹，用于存放 python 的虚拟环境（比如 `C:\PythonEnvs`）。创建一个名为 `WORKON_HOME` 的新变量，并将其值设为 `C:\PythonEnvs`.

{% maincolumn "assets/photos/2021-03-07-environment-variable-box.png" "" %}

### 用 `pip` 安装 `virtualenv` 和 `virtualenvwrapper`

按照刚才的步骤，此时 `pip` 应该已经安装，此时在命令行输入途中的命令，应该可以看到类似的返回信息：

{% maincolumn "assets/photos/2021-03-07-pip-check.png" "" %}

如果命令行说没找到 `pip`，可能需要按照[这个链接](https://pip.pypa.io/en/stable/installing/#installing-with-get-pip-py)里的方法重新安装。

在命令行中输入 `py -m pip install virtualenv`， 安装虚拟环境管理器：

{% maincolumn "assets/photos/2021-03-07-virtualenv-install.png" "" %}

显示安装成功之后，在命令行输入 `py -m pip install virtualenvwrapper-win`，结果应该和上图差不多，忘了截图。

### 创建一个虚拟环境，安装 `jupyter`

`virtualenv` 和 `virtualenvwrapper` 安装完成之后，在命令行中输入 `mkvirtualenv base`，新建一个名为 base 的虚拟环境。

然后输入 `workon base`，此时命令提示符的行首应该会多出一个 `(base)` 字样，这说明我们已经工作在了 base 这个虚拟环境里。此时 `pip --version` 的结果说明我们的 python 的地址已经和之前不同了。

{% maincolumn "assets/photos/2021-03-07-virtualenvwrapper-check.png" "" %}

在这个环境之下，安装 jupyter，输入命令 `pip install jupyter`，安装 jupyter。这一步不是必须的，但是这样我们将来安装 vscode 之后，可以获得和 conda 自带的 spyder 类似的体验，菜鸟逐行调试的时候非常方便。

### 下载和安装 `vscode`

从 vscode 的官网下载安装包（[链接在此](https://code.visualstudio.com/)），可以看到大大的下载按钮：

{% maincolumn "assets/photos/2021-03-07-vscode-download.png" "" %}

下在之后的安装过程就和一般的程序安装一样（安装很久了，没有截图）。

然后在你想开始写代码的文件夹里，鼠标右键单击，选择 "Open with Code":

{% maincolumn "assets/photos/2021-03-07-vscode-folder-open.png" "" %}

然后在 vscode 的界面，在文件树上单击红框中的按钮，新建一个文件，命名为 `*.py`，这里随便写了个 "hello".

{% maincolumn "assets/photos/2021-03-07-vscode-new-file.png" "" %}

在随后打开的文档编辑区输入 `print("Hello World")`，将光标停留在这一行，按 `Shift`+`Enter` 执行这一行：

{% maincolumn "assets/photos/2021-03-07-vscode-run.png" "" %}

因为是第一次执行，又因为安装了 `jupyter`，这时候 vscode 的右下角应该会出现一个提示框，询问是否用 jupyter interactive window 执行代码。然后关掉下方的这个 terminal (下半区右上角的叉号)。重新按 `Shift`+`Enter` 执行，此时的结果应该如下图，点击红圈中的变量浏览器，这就几乎和 spyder 的体验一样了。

{% maincolumn "assets/photos/2021-03-07-vscode-interactive.png" "" %}

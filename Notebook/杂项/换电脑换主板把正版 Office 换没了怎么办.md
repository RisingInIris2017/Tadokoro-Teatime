# 换电脑换主板把正版 Office 换没了怎么办？

## 前言

本文是 [简单的 Windows 10 重装指南](https://github.com/RisingInIris2017/Tadokoro-Teatime/blob/master/Notebook/%E6%9D%82%E9%A1%B9/%E7%AE%80%E5%8D%95%E7%9A%84%20Windows%2010%20%E9%87%8D%E8%A3%85%E6%8C%87%E5%8D%97.md) 的补充教程，同样来源于我在写作本文前不到 10 小时，发生的真实经历。

## 问题描述

我更换了电脑的主板以后，丢失了正版 Office 的激活信息。

众所周知，买电脑送的 Office 是“家庭与学生版”，这个许可证只能激活一台电脑。

于是，现在当我打开任何一款 Office 组件，包括但不限于 Word, PowerPoint, Excel，软件都会提示“**您的许可证已达到最大安装数量**”。

不管如何再尝试激活，都会这样提示。

**本教程专门适用遇到这种情况的 Office 用户，其他激活问题请另找教程**。

除了更换主板外，假如你换的新电脑没有预装 Office，

你打算从以前的品牌机上把正版 Office 薅过来用的话，那么更换新电脑也会发生这种情况。

## 解决流程

### 重装

这一节的步骤可能是可选的，因为我不能确定需不需要重新安装 Office 才能解决问题。

你不妨尝试跳过本节的全部步骤，直接从下一节的第一步开始操作，如果尝试成功，请发 Issue 告知我，非常感谢。

1. 在 [微软账户管理界面](https://account.microsoft.com/) 的顶部找到“设备”和“服务与订阅”，都打开，或点击下面的链接。
2. 打开“[设备](https://account.microsoft.com/devices)”，找到你的旧电脑，将其删除。
3. 如果你是换主板遇到了这个问题，下载 [这个工具](https://wwd.lanzoui.com/ioj6Tz0k65g) 选择你电脑上那个出问题的 Office 版本，进行卸载。这里的工具是微软官方的，有人将其上传到蓝奏云供大家下载而已，安全无毒，可以放心使用。卸载完毕后，请打开“[服务与订阅](https://account.microsoft.com/services)”，找到你想迁移到新电脑的那个 Office 版本，点“安装”。
4. 此时你会开始下载安装程序，下载完成后直接运行完成重装。

### 激活

这一步是最关键的环节。你不就是要那个许可证吗？

1. 打开你现在用不了的任意一款 Office 软件，Word，PPT，Excel，都行。进入其“开始”菜单，找到“账户”，在里面应当有个“许可证”的按钮。点进去找到“电话验证”，这时会显示一个窗口，里面有一长串数字，这个东西就是安装 ID。开着这个窗口别关，找一张纸一支笔备用。
2. 下载 [Skype 网络电话软件](https://www.skype.com/en/get-skype/)（这里包含电脑客户端和手机客户端的下载，你也可以直接用电脑打这个电话）。如果你愿意支付打越洋电话到英国的话费，也可以跳过这一步骤。
3. 打电话给这个英国号码：`+44 8000188354`

当电话接通，你会听到一口标准的 *英语*。如果在英语听力方面有一定困难，可以找家里的学生来听电话里的语音，完成下面的步骤。

> 语音：欢迎来到微软产品激活中心，为了安全起见，请输入三位数字验证码：

听到语音播报的三个数字之后，输入进去即可。

> 语音：要激活 Windows ，请按 1；要激活 Office 和 Mac，请按 2。

不管它，只按 1。

> 语音：要激活 Windows 10 ，请按 1；要激活其他产品，请按 2 。

不管它，只按 2。

> 语音：若您已准备好安装 ID ，请按 1；未准备好，请按 2 。

按 1，一听到“please”，就把安装 ID 的第一段输入进去，输完等一下，等语音开始唧唧呱呱说话了，就输下一段。

如果某一段输错了，语音会让你把刚才输错的这一段重新输一遍，不会导致从头再来，不用太担心。

输完之后等待一会，如果没有问题，语音就会开始播报一串很长的数字，这个数字就是确认 ID。

听写这一段数字，如果听错了或者听漏了，后面有让你按数字重听的机会，不用太紧张，不是四六级。

然后把这段数字输入到第一步打开的窗口中，即可激活成功。

—— 本段引用自镜像之家文章《[Win10 Office 2019电话激活全过程](https://www.win10com.com/wzjc/soft/28428.html)》

## 额外的问题描述

这一段是给像我一样不作死就不会死的人准备的。

在发现正版 Office 丢失以后，我病急乱投医尝试了很多激活码，

导致电脑上出现了许多个无效的 Office 许可证，什么专业增强版、什么预览版之类的。

这些无效的许可证会阻止你接下来使用完成激活的“家庭与学生版”！

哪怕你激活完成，Office 仍然会把所有的功能锁定，等待你激活这些你不可能激活的无效许可证。

### 解决方案

1. 用管理员权限打开命令提示符。其中一种方法是，先打开任务管理器（Windows 10 下快捷键为 Ctrl+Shift+Esc），左上角“文件”-“运行新任务”-输入 `cmd`-勾选下面的“以系统管理权限创建此任务”。
2. 根据你的 Windows 操作系统位数和 Office 软件位数，从下面三条命令中选择正确的一条输入命令提示符。

Office 64 位 和 Windows 64 位

`cscript “C:\Program Files\Microsoft Office\Office16\ospp.vbs” /dstatus`

Office 32 位 和 Windows 64 位

`cscript “C:\Program Files (x86)\Microsoft Office\Office16\ospp.vbs” /dstatus`

Office 32 位 和 Windows 32 位

`cscript “C:\Program Files\Microsoft Office\Office16\ospp.vbs” /dstatus`

在我自己的 Office 2019 这里测试，命令当中的 `Office16` 也不用更改，应该是和 Office 具体版本无关的。

输入正确的命令后，命令提示符会打印所有你电脑上的 Office 许可证信息，有效的和无效的都会打印。

接下来依据你的 Office 软件位数，从下面两条命令中选择正确的一条输入命令提示符，输完先不要按回车。

Office 64 位

`cscript “C:\Program Files\Microsoft Office\Office16\ospp.vbs” /unpkey:`

office 32 位

`cscript “C:\Program Files (x86)\Microsoft Office\Office16\ospp.vbs” /unpkey:`

查看一下刚才打印出来的所有许可证信息，大致是这样：

> PRODUCT ID: xxxxx
> SKU ID: xxxxx
> LICENSE NAME: xxxxx
> LICENSE DESCRIPTION: xxxxx
> BETA EXPIRATION: xxxxx
> LICENSE STATUS: xxxxx
> Last 5 characters of installed product key: 五位数字/字母

LICENSE STATUS 如果是 Licensed，就是有效的，其他都是不需要的。

把不需要的许可证信息最后一行那五位数字和字母，输入到命令的最后，按下回车即可删除这条许可证信息。

如果你想看到删除后的效果，那么依据你的 Office 软件位数，从下面两条命令中选择正确的一条输入命令提示符。

Office 64 位

`cscript “C:\Program Files\Microsoft Office\Office16\ospp.vbs” /remhst`

Office 32 位

`cscript “C:\Program Files (x86)\Microsoft Office\Office16\ospp.vbs” /remhst`

等你看到电脑上只剩下 LICENSE STATUS 是 Licensed 的有效许可证，就可以了。

把这些问题解决完，你的 Office 应该就可以恢复正常使用了。

## 某个未经验证的神奇方案

[这条发布于 2016 年的帖子](https://www.jumin.cc/T-248093-1-1.html) 描述了一种无需打电话的激活方案，

是我在解决问题之后，最近搜索到的，没有经过验证，假如仍然可用，可以发 Issue 告诉我。

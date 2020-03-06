# 如何在服务器上使用你心爱的多世界模组
## 本文目录
## 前言
有不少 MOD 服服主喜欢使用地形生成模组，例如广受大家喜爱的 [\[BOP\] 超多生物群系](https://www.mcbbs.net/thread-817372-1-1.html)，
[\[RTG\] 真实地形生成](https://www.mcbbs.net/thread-681294-1-1.html)，

甚至冷门一些的，适用于 1.7.10 的 [高地](https://www.curseforge.com/minecraft/mc-mods/highlands)。

总而言之，这些有趣的模组极大地改造了 Minecraft 世界的地形地貌，为玩家的生存世界带来了别致的风景。

然而在服务器上使用时，服主们常常遇到以下四个问题：

1. 我要怎样使用某某 MOD 生成主世界？

2. 在安装了多世界插件，例如 MV 的情况下，如何使用某某 MOD 生成新的世界？

3. 已有旧的地图情况下，可以加地形 MOD 吗？有用吗？

4. 当我不想要地形 MOD 了，该怎么处理？

本文将一一解答以上的问题，帮助你开起拥有美丽世界的 MOD 服。

## 如何使用某某 MOD 生成主世界

启用 MOD 的地形生成器的关键，就在于这些 MOD 的地形生成器名称。

BOP 超多生物群系:`BIOMESOP`

RTG 真实地形生成：`RTG`

知道了地形生成器的名称，我们只需打开 `server.properties` 文件，

找到

`generator-settings=`

在等号后面填入地形生成器的名称，保存，重启服务器就可以了。

## 如何使用某某 MOD 生成多世界插件的世界
### 准备工具
这里涉及到使用 NBTExplorer 修改 level.dat 的内容，

因此我们首先给出 NBTExplorer 工具的下载地址：https://github.com/jaquadro/NBTExplorer/releases/latest

msi 格式是安装包，zip 格式是免安装的，解压就可以使用，推荐下载后者。
### 操作步骤
我们以 Multiverse-Core 插件（MV 多世界）为例，介绍生成 MOD 世界的方法。

1. 在服务器使用命令

`/mv create <世界名> normal`

生成一个世界，生成完毕之后，立即关闭服务器，或使用。

`/mv unload <世界名>`

将世界卸载，备用。

2. 将生成好的世界文件夹打开，默认位于 `服务端根目录/world/<世界名>文件夹` 下。

删除 `region` 文件夹，并找到 level.dat 文件。

3.双击“灌木”图标的 NBTExplorer.exe 运行，将 level.dat 文件拖入已经打开的 NBTExplorer 窗口中。

打开之后是这样。
![3LtWCR.png](https://s2.ax1x.com/2020/03/06/3LtWCR.png)

点击 Data 左边的小按钮，展开 Data 目录。

向下滚动鼠标滚轮，找到红圈圈住的 `generatorName` 项，双击打开。

在跳出的文本框中输入世界生成器名称，例如 `RTG`。

填好后点击“OK”按钮，并按 Ctrl+S 快捷键保存更改。

更改完后是这样。
![3Lt259.png](https://s2.ax1x.com/2020/03/06/3Lt259.png)

4. 启动服务器，或使用

`/mv load <世界名>`

载入世界，现在新生成的区块都会使用 RTG 提供的地形生成器来加载了，

你可以看到高大的树木、起伏的山岭，我们就成功了。

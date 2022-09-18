# 植魔作者Vazkii：我是这样制作整合包的

作于 2022 年 9 月 16 日。

## 作者自序

在开始讨论这个话题之前，请允许我做一个自我介绍，并对一些事情简要做个说明。

我是 Vazkii，若干 Minecraft MOD 与整合包的作者。在这篇博文中，我会针对我最近的两个“原版+”风格整合包：[Crucial 2](https://www.curseforge.com/minecraft/modpacks/crucial-2) 和 [Bliss](https://www.curseforge.com/minecraft/modpacks/bliss) ，就我设计整合包的方法论体系展开讨论。

这篇博文会讲述 *我* 是怎么设计整合包的。我曾多次接到邀请，让我写点这种东西，让刚刚接触整合包制作的创作者们了解一下我是怎么做整合包的。但是这篇博文不是教你怎么设计你自己的整合包的完整教程，更不是设计任何整合包的标准方法：这只是 *我自己* 的方法。如果你是做整合包的新手，我觉得你可以从我的想法当中学到相当多的东西；但是我建议，你的整合包和我的整合包风格差距越大，你对我的观点就越要慎重考虑。

本文的其余文段将大量地用我的整合包来举例。所以，我建议你稍微了解一点整合包的运行原理，免得你由于缺少相关背景知识看不懂这篇文章。如果你没玩过我的这两个整合包的话，可以先看一下 *Mischief of Mice* 的视频（Youtube）：

[Crucial 2 整合包](https://www.youtube.com/watch?v=FQkCc4UO-jg)

[Bliss 整合包](https://www.youtube.com/watch?v=FXFdRJPNrM4)

好的，说完这些，我们就开始设计整合包了。

## 💡 创意

创意是整合包项目的种子，从这里开始你的整合包生根、发芽、开花。种子有很多品种，但最重要的是，你要从中选择独一无二的、带有你在其他的种子上找不到的特质的。

我们都站在巨人的肩膀上。我们所站的巨人，则站在数量更多的巨人的肩膀上，以此类推。找一个你喜欢的巨人，然后站在他的肩膀上。

这种文学性的说法，说白了就是，如果你想做个整合包，它必须做出一点新东西来。不是说你非得做出翻天覆地的改变，你只是必须有一些别人没有的。可能是游戏机制的微小改动，可能是换个 MOD，可能是对游戏平衡的不同理解，或者类似的这种东西。

我们以 *Crucial 2* 和 *Bliss* 为例：

- *Crucial 2* 本质上是个直截了当的“原版+”整合包，但是它的改动在于，它利用 JEI 的条目与指南书中的“闲话”章节，建立了它独有的整合包说明机制。它的关键词是“探索”。即使去掉这个创造了和“传统”的“原版+”整合包不同的游戏体验的新机制，这个整合包也是合格的、好玩的，但是你是不可能看到我做这样的整合包的。
- 在 *Crucial 2* 的基础上，*Bliss* 同样采用了上述的设计理念。同时，它引入了类似于和平包（可以在和平难度下玩的整合包）的元素。同样，即使去掉这种元素，*Bliss* 仍然是相当合格的整合包，但同样地，你是不可能看到我做这样的整合包的。

你可以像这样构思你的创意：“可以这样，但是...”，或者甚至是，“可以这样，再那样，但是...”——任何东西都是一步一步推导出来的。通过这种方式，你可以找到你喜欢的那种东西，然后把整合包魔改成那样。

实操这种思路的一种有趣的方式，是从游戏里去掉某些东西。*Bliss* 实际上就是这种整合包。你把一些东西从游戏里拿掉之后，游戏内容就出现了一个空缺，你就可以想办法把它补上。很多时候，如果你设计得当，这样做完之后你就得到了一个具有完全不同的游戏体验的整合包。

我写到这里的时候突然想到个创意，在这里白送给各位读者：

- 一个经典的科技包。但是，你没有任何办法存储能量。这会迫使你随着游戏推进不断扩大发电量，同时迫使你搭建一个信号/控制系统。

理解你的思路推导会对游戏体验带来什么样的改变，以及想清楚你要怎么利用这些改变，去创造新的东西。这至关重要。下面的文段中，凡是我从我的整合包中拿出来，用来佐证我的观点的例子，我会用引用块来表示，像下面这样：

> 在 *Bliss* 中，你不招惹怪物，怪物就不打你。从而，我可以在地图上生成苦力怕的刷怪笼。通常情况下这种东西是不能存在的，因为刷出来的苦力怕会炸掉刷怪笼本身。

说到这里，你可能不得不接受两个生活的真相：

- 好的创意不常有，而且
- 你一开始觉得好的创意通常不怎么样

所以我做整合包要花很长时间。我不会纯粹地为了做包而做包，而且我还经常把我想出来的大部分点子否决掉。花点时间，看看其他的内容，从它们身上找找灵感，让创意的源泉充分涌流。但要注意，你的创意源泉不是拧开就有的水龙头，也不是整天都有的自来水。如果你一时想不出来，就不要强求。

如果你很难找到好创意，试试带着分析的眼光去玩游戏。找个你还没玩过，但是你觉得自己可能会喜欢的整合包，检阅一下这个包 *做* 了什么东西。阻止自己随波逐流，质疑每一个决定的依据。为什么这个配方要这样改？为什么要加这个 MOD？看看你喜欢什么，不喜欢什么。通过提出这些问题，你就会代入到整合包设计者（策划）的角色中，你就会自然而然地开始问你自己“但假如我这样的话...，那么...”。

这里的“假如”就会变成前面的“但是”。这些问题就会变成种子，它们就可能成长为一个整合包项目。

总的来说，花点时间，找到一颗好的种子。生命的循环不是在一天之内发生的。

> 从 *Crucial 2: Refresh* 的更新发布，到我开始做任何 *Bliss* 的设计规划之前，中间间隔了大概 7 个月。

## 🛍️ MOD 的选择

一旦你想好了要做什么，你就要开始挑选内容的组成部分了。我挑选 MOD 的流程可以划分为几个不同的阶段。

### 核心 MOD 的选择

每当你想做包的时候，脑海里一定会出现几个你 *想要* 加进去的 MOD。这些 MOD 要么是你相信契合整合包主题的 MOD，要么它们 *就是* 整合包的主题 MOD。

> *Crucial 2* 的核心 MOD 是一套简单、传统的“原版+” MOD，也就是 Quark（夸克），Supplementaries 和 Abnormals Mods 全家桶。
*Bliss* 是从“和平包”的概念出发而设计的，用到了 *Apathy* 这个 MOD。

有时你可能一个核心 MOD 都挑不出来，没关系的，跳过这一步就是了。

如果挑出来了，打开你喜欢的整合包制作工具（我个人使用 CurseForge 的客户端，虽然它可能很糟糕）, 创建一个新整合包实例，然后把你这些核心 MOD 加进去。

警惕加一大堆核心 MOD 的做法。一个核心 MOD 是你的整合包的一条公理，它负责建立你的整合包当中最最基本的东西。你加的核心 MOD 越多，所有的东西都会变得越不方便。通常情况下，你可以从你想要做的内容当中提炼出最重要的部分，而其他的一切内容都围绕着它。那么我们就从这个“最重要的部分”开始。

有的时候你想要的核心 MOD 有可能不存在。你的整合包创意需要的那个核心 MOD，有可能过时了、弃坑了，甚至还没有人开发出来过。你要是会开发 MOD，你可以自己把这个坑填上；你要是不会，你可以考虑找个人帮你把这事情办了。

### 挑选候选 MOD

进入这个阶段，我就会打开 CurseForge 的 MOD 列表，去找我要找的任何游戏版本，然后把 *每一页* 都浏览一遍，寻找可能适合整合包主题的 MOD。我基本上会点开任何看起来起码有一半靠谱的 MOD，而且也不会立即以“超出整合包的范围”为理由否决一个 MOD（例如在做“原版+”整合包的时候看到了一个高科技题材的 MOD）。

我会粗略看一下这些 MOD 的主页，并把任何看起来有趣的东西放进浏览器收藏夹。没必要在时候做得非常精确，反正我们稍后要作一番删减。

把这个流程做完以后，我通常已经收藏了几百个 MOD；我会对它们做个梳理，它们中的绝大多数是不会出现在最终的整合包成品当中的。

这套方法也可以，而且通常会，用在确定整合包核心 MOD 的时候。任何你完全确定非加不可的 MOD 都可以直接加进去，接下来你还可以用这个办法去砍掉不必要的 MOD。

如果到完成了这一步你还没有找到核心 MOD，那这时候你要好好地考虑一下你的想法是否可行。你肯定是需要一些基本的东西作为地基来搭建你的整合包；如果其他的游戏内容没有地方下锚，它们就会漂走。如有必要，重新评估你的创意，或着试试更加深入地挖掘你挑选出来的东西，从中找到那个可以使你的想法成为现实的 MOD。

如果你 *还是* 缺少核心 MOD，当然，这并不意味着一切都完蛋了；但是，我不会建议你继续往下做，除非你真的非常相信，你的想法是可以依靠你所掌握的能力和资源去实现的。

### 朴素裁剪法

把核心 MOD 定下来之后，就该看看哪些东西可以和它适配了。我这时候就会用鼠标中键点击收藏夹，一下打开几百个 Vivaldi 浏览器的标签页，让我的电脑内存体验一下心绞痛。*Vivaldi 真是一款好浏览器啊。*（译者注：作者原话如此）

我把这叫做“朴素裁剪法”，是因为我们会从这些 MOD 上寻找和我们想要做的整合包不相适配的特征，一旦找到就把这个 MOD 否决掉。如何决定这些特征是取决于你自己的整合包的，但是就我自己而言，我会检查下面这些东西：

- 数量多得过头的内容（*比如 10 种矿石就太多了*）
- MCreator 制作的 MOD（*这类 MOD 也不总是不好，但是 MCreator 生成的 MOD 有很高的性能开销*）
- 相互冲突的美术风格（*MOD 如果不大的话，也可以做个资源包来解决这个问题*）
- MOD 的最基本内容与整合包的核心 MOD 相冲突或者相重复（*比如你核心 MOD 里有 Biomes o’Plenty 超多生物群系，你就不会想再要一个添加树木的 MOD，毕竟 BOP 已经添加过了*）
- 不必要的内容（*“我们真的需要这个内容吗？”尝试训练自己在加 MOD 的时候能够自我控制，毕竟多不总是等于好*）

分享一个关于最后这一点的实操经验。评估一个 MOD 有没有必要加的时候，不要问自己“为什么不加”，而是问自己“为什么加”——这个 MOD 可以带来什么？这些东西足够重要吗？挑选一些这样那样的，个人偏爱的 MOD，当然是可以的，但要尽量减少那些“*只是因为它有...*”就被你添加到整合包中的 MOD。加太多的 MOD 不仅会冲淡你最初的创意，而且会拉低整合包的整体性能表现，还会在后续的维护当中给你带来来自更多方面的问题，甚至还会在你魔改和调整游戏平衡的环节，给你制造更多的工作量。

> 因为没办法用 *Abnormals Mods* 全家桶添加的那些木头类型去制作这些物品，*Crucial 2* 放弃了很多添加了新的木制物品的流行 MOD。

你知道我特别强调整合包的创作要确保内容的一致连贯性，所以那些会导致你的整合包内容出现不一致、不连贯的东西，就要比其他的 MOD 更加慎重地考虑保留与否。

完成上述的“裁剪”之后，我个人喜欢递归地浏览剩下的 MOD 列表，根据剩下的 MOD 的质量，重新调整我的标准，并再进行一些削减，直到我对列表中的每个 MOD 都感到满意。这个过程取决于你最开始希望的“裁剪”严格程度，因此你有可能不必再进行这一步。

### 第一版草稿

既然已经初步列出了 MOD 的清单，那现在就把它们全部倒入你的整合包，看看你要面对的游戏内容都有哪些。

到这一步，假如整合包可以启动，那么现在就应该开始统计一下这些 MOD 都有哪些 *问题* 了。这可以帮助你进行后续的删减和魔改。

下面这些是我喜欢去检查的项目：

- 名字相似或重复的物品（*认真地告诉我，一个整合包到底要有多少种“蓝色下界砖”？*）
- 被重复实现的游戏机制（*烧 RF 的熔炉有一个就够了*）
- 材质难看或者命名不规范的游戏内容（*命名的时候请注意大小写，朋友们*）
- 和你的想法相矛盾，甚至可能有害于你实现你的创意的游戏内容
- 你不喜欢的游戏内容

专家建议：这是你的整合包，只要是你不喜欢的东西，都可以去掉。你觉得这个游戏内容不够好，你就可以删了它。警察叔叔不会因为这个来抓你的。（译者注：作者原话如此）

一旦你列出了你能注意到的所有初步的问题，那么从中找出根本性的问题，并据此删减你的 MOD 内容。配方和进度很容易就可以删掉，物品可以从 JEI 中隐藏，而且大多数 MOD 都带有一些配置选项，允许你关闭每一个游戏内容或机制。

对于任何留下的根本性问题，如果你觉得它们值得想办法删掉，可以考虑联系有关的 MOD 开发者，并要求提供一些解决问题的方法。例如，如果一个 MOD 增加了一个你不喜欢的游戏机制，又不提供禁用它的配置选项，就要求作者提供一个。

> *Crucial 2* 加了 Storage Drawers 储物抽屉 MOD，但我把所有的自定义材质、名称和所有的升级都去掉了。因为这一大堆它添加的方块远比原版的方块复杂得多，而这是不符合整合包主题的。

这时候你可能需要暂停一下，检查一下你的创意在经历了如此的删减之后，是不是仍然能够实现。如果答案是否定的，那么你应当问问自己为什么，并试试与 MOD 的作者合作来解决这些问题。

把这些做完以后，你已经完成了建造你整合包大厦的第一步：打好地基。如果整合包是个披萨饼，那面团已经准备好了，现在该烤它了。

# 🔧 工具

了解你的工具，就是了解你的极限。如果你知道你能做到什么、不能做到什么，你就更容易找准问题。数据包和 CraftTweaker、KubeJS 这类的自定义脚本 MOD 赋予了整合包修改整个游戏的强大能力，那么聪明地使用这些能力，可以让你避免很多可能成为麻烦的设计上的障碍。

有很多 MOD 可以让你载入默认的数据包和资源包，例如 Open Loader 和 Paxi。我特别推荐你装一个，这样你可以改动的内容范围就会变得更宽。

我们来看看几个我用过的例子。

### 配方修改

这基本上是绝大多数整合包必做的事情了。显然，使用数据包或者自定义脚本 MOD，你可以增删改任何 MOD 添加的任何配方。而且，你还可以写一些自定义的钩子，来给那些没有直接支持配方修改的 MOD 自动生成 JSON 格式的配方。

> *Bliss* 包含有能让 Farmer’s Delight 农夫乐事 MOD 的砧板和 Corail Woodcutter 的锯木机支持自定义配方的自定义脚本。

### 隐藏物品

JEI 允许你让它向玩家隐藏一些物品。你可以通过快捷键开启这个功能。

> *Crucial 2* 和 *Bliss* 都大量运用这个功能，以确保你只能看到那些你可以获得的物品。

### 文档说明

Patchouli 和 JEITweaker 这类 MOD 可以让你为整合包编写游戏内的引导文字。“玩家不得不从可能已经年久失修的 Wiki 当中查找你整合包里的这个东西是怎么工作的”这类的事情，会让你的整合包质量大打折扣。所以，任何玩家需要的信息，都应该允许玩家非常容易地看到。

> *Crucial 2* 和 *Bliss* 都在玩家背包里放了 Patchouli 指南书，同时也都通过 JEITweaker 在 JEI 当中放入了几百条短小的说明文字。

### 搜索标签

JEI 的配置文件中可以设置一些搜索标签，便于玩家利用它们搜索物品。利用数据包，你可以给物品加标签，作为方便搜索的目录。

> *Crucial 2* 和 *Bliss* 都大量运用了这个机制。它们都提供了用于模糊搜索的标签，比如“building block”和“decorative block”，以及一些专门设计的搜索重定向，比如“weather sensor”会指向 Supplementaries MOD 的 [风向标](https://www.mcmod.cn/item/430708.html) 物品。（译者注：此处指向 MCMOD 百科的超链接为译者添加）

### 重命名或者重画材质

如果它们和整合包其他部分向冲突，或者单纯地只是不合适的话，资源包可以帮助你给物品和方块改名。

> *Bliss* 对 Corail Woodcutter MOD 做了大量的换皮工作，这样它和整合包的其余部分就更适应了。

### 战利品表

通过修改战利品表，数据包可以更改任何生物或方块的掉落物，以及游戏的其他机制。

> *Crucial 2* 和 *Bliss* 使用这个方法清空了 Waystones 传送石碑 MOD 的战利品表，因为在这两个整合包中，这个 MOD 添加的方块是不允许玩家获得的。此外，*Bliss* 修改了猪灵以物易物的战利品表，往里面加了一些新的物品。

### 删减物品信息提示（Tooltip）

CraftTweaker 允许你删除 Tooltip 的一部分行。这是一个非常细节的用法，但是你可以用它来移除 MOD 所加的那些与整合包中其他的 Tooltip 风格不一致的、不相干的 Tooltip。

> *Bliss* 使用这个方法删去了 Corail Woodcutter MOD 的方块包含的不必要的 Tooltip。

### 生物控制

InControl 允许你设置自定义的规则，来控制什么情况下生物可以/不能生成。根据你的整合包的不同情况，这个调整可能是没有意义的，也有可能是意义重大的。

> *Bliss* 使用这个方法限制蜘蛛只能在露天生成。

### 删减进度

利用数据包，你可以把任何一个进度替换成不会显示的版本。这样替换后的进度 *在技术上* 仍然存在，但完全不会再显示出来了。如果你删除了一个游戏内容，检查一下有没有和它相关的进度，你也许也会需要隐藏它们。

> *Crucial 2* 大量删减了 Alex’s Mobs Alex 的生物 MOD 的内容，所以也把相应的进度隐藏了。

### 自定义内容

使用 ContentTweaker 之类的 MOD 可以让你添加属于你的物品或方块。如果 MOD 的内容之间有一些简单的环节缺失，这通常是将这个缺失的环节补上的基本方法。

> *Crucial 2* 使用这个方法在可选的 Create 机械动力 MOD 兼容部分添加了“粗铜”材料物品。
> 

### Advanced Scripting

*KubeJS* and *CraftTweaker* both support advanced scripting, using an event system to change things that happen in the game based on custom code. This effectively has the same scope of possible changes as a server-side mod, but comes with the complexity of having to understand their coding languages and APIs, so it’s generally not used other than to bridge niche gaps that otherwise couldn’t be done with available tweak mods.

> Neither *Bliss* nor *Crucial 2* use this feature, but the original *Crucial* used [this script](https://github.com/Vazkii/Crucial/blob/master/scripts/ore_correction.zs) to replace every ore block drop with the raw item equivalent.
> 

### Worldgen Changes

As of recently, data packs are able to vastly modify the way the world generates. Entire mods such as *Terralith* are actually just complex data packs in disguise. You’re unlikely to be making a massive worldgen data pack for your modpack, but you can use them to make small tweaks to worldgen that otherwise wouldn’t be possible via simple config editing.

> *Crucial 2* uses a custom data pack to remove lakes from biomes, make mountains taller, and rivers deeper. *Bliss* uses a custom data pack to remove select structures from mods I don’t wish to have spawning, such as the shrines from *Paraglider*.
> 

### Block Swap

The *Block Swap* mod allows you to replace any block with another, in any situation. This is mainly very relevant for worldgen, but can be used to do other weird tricks, such as preventing specific blocks from existing in the world.

> *Crucial 2* uses this to swap the worldgenned Leaf Pile blocks from the *Mirabilis* mod with the respective Leaf Carpet blocks from *Quark*, in order to ensure a lack of content overlap.
> 

### Default Options

The *Default Options* mod lets you ship out a custom options config that players will start the game with. This can be used to set game settings to your preference and is essential to ensure players don’t start their game with a pile of mismatched keybinds.

> Both *Crucial 2* and *Bliss* use this to ship a clean keybind sheet as well as Auto Jump disabled. Additionally, *Bliss* ships with several accessibility options enabled.
> 

### And Much, Much More

This list is very much non-exhaustive, and shows only some of the tools I’ve used to ensure every pack feels like a proper, cohesive experience. There are a myriad of pack dev mods I haven’t even touched, many of which may be exactly what you need. 

This section serves mainly as a demonstration of the tools you have access to, and the ones I’ve used to good effect in the past. If you feel you need to make a change to the pack and don’t know of any mods that let you do it, ask around, maybe one already exists.

# 🏗️ Development

This is the fun part.

Now that we have our base and our tools ready, it’s time to put them to work. There are two types of tasks you’ll have to tackle in this stage: **Issue**, and **Vision**.

- **Issue** tasks are problems you find with the mods or how they play with each other
- **Vision** tasks are those that pertain to creating the experience you want to deliver

**Vision** tasks are, unfortunately, out of the scope of this document, as the way you chase your vision is entirely up to you. If you want to make an expert progression pack, be prepared to change a lot of recipes. If you want to make some adventure and combat focused romp, open up those worldgen data pack json files. Quest pack? Better start writing. That part is for you to determine.

Instead, I’ll focus on more generic advice for the tenets I follow when creating packs, as well as the **Issues** that can break those tenets and need to be resolved.

### Disabling features is good, actually

Let’s start with a kicker. For me, the way to think about this is that, in disabling a feature, you aren’t *removing* it, but rather opting *not to add it*.

Whenever someone asks me why a feature disabled, my answer is to explain my stance on adding features. If you think of disabling features as *removing them*, you’re making the assumption that the default state of a bit of content is *added to the game,* and this just isn’t true.

Every feature in every mod you haven’t added yet is ***not** added to the game,* and you choose to *add* it when you include the mod. I believe that disabling features is not turning them back to *not added*, but rather pick and choosing which features get *added* in the first place.

Just because a mod comes with a myriad of different features doesn’t mean all of them are appropriate for what you’re trying to make. More often than not, you just want a few. If you’ve played any of my packs, you know I cut liberally, because I’m selective about I want to add. I prefer to examine each feature with a positive-focused mindset (”*what does this bring to the table?*”), rather than a negative-focused one (”*is this bad enough to remove?*”).

This is the part where it’s important to know your audience, and be able to place yourself in their shoes. A lot of features might be ones you’re not particularly interested in yourself, but other players might love, but you can’t go too crazy with this thought, or you’ll end up massively diluting your pack.

It’s important to strike a balance between cutting features and letting features in. This is something you learn over time, and is definitely not a science.

> *Crucial 2* has 994 disabled items (non-vanilla items hidden from JEI).
> 

In the following few sections, I’ll explain multiple reasons you’d opt *not* to add a feature.

### Create a cohesive whole

While in a technical state, a pack is just a bunch of disconnected mods glued together by configs and scripts*,* I like to think of it as more than that. Put yourself in the position of someone shipping *an actual game*. 

When you play a commercial game, you notice inconsistencies in it. 

- Maybe this menu uses one texture while another uses a different one for no reason.
- Why is this item named “*Thing of Person*” and this one “*Person’s Thing*”?
- Why does this boss drop items you have to combine into big items to craft but this other one already drops the big items?
- Why is the first point in this list an affirmation and the others questions?

These are simple example questions that create blemishes in a game. When you’re taking in dozens or hundreds of mods made by dozens or hundreds of disconnected authors, the amount you are bound to find will be incredibly high.

By thinking of making a pack as if you were making a game, these blemishes become things you are more sensitive to, and likely to fix. This is important because every small inconsistency can act as a small road bump in a player’s overall experience.

> *“Oh right this item is from another mod, I can’t use it with this machine”*
- strawman I just made up but you’ve probably heard a lot
> 

> *“Why do these two Cherry Log blocks not stack… oh right”*
- average kitchen sink vanilla+ modpack player
> 

 Each blemish is a “*ugh, why didn’t they fix this*” thought in the player’s head. While each one is minor individually, they pile up, and over time can cause the player to enjoy your pack less and less.

By thinking of making a game, we think of reducing these road bumps and bits of inconsistency - we think of making the experience as smooth and logical for a player. This is important.

You can think of this as a high amount of nitpicking or unnecessary polish for minor effect, which you likely will if you are used to modpacks that don't do this. But let me tell you that these tiny changes are the key difference between a good pack and a great one.

Here are some inconsistencies I like to watch out for and patch up:

- Multiple items with the same or similar look, name, or functionality (*content overlap*)
    
    > In *Crucial 2*, both *Charm* and *Environmental* add a Kiln block. These fill a similar purpose, so one was disabled.
    > 
- Mod content resulting in missing expected combinations (*content gaps*)
    
    > e.g. A mod adds Willow Wood, and another adds Tables for each type of wood. Unless intentionally coded, you won’t be able to make a Willow Table.
    > 
- Specific features being far too complex in comparison to others in the pack
    
    > In *Crucial 2*, all the upgrades for *Storage Drawers* are disabled to bring the level of complexity of the feature down to the same as the other mods in the pack.
    > 
- Specific non-core sections of the game being weighed in content far too heavily versus others
    
    > I do not include *Pam’s Harvestcraft* in packs I make due to the sheer amount of content it adds, which would unbalance the game heavily towards farming.
    > 
- Visual inconsistencies in textures, naming schemes, tooltip styles, or type of functionality
    
    > *Crucial 2* retextures and renames many different items and blocks. For example, *Charm*’s “Bat in a Bucket” is renamed to “Bucket of Bat”, to be consistent with the naming scheme in vanilla.
    > 
    
    > In *Bliss*, the tooltips for *Corail Woodcutter* blocks are hidden, as equivalent blocks in the rest of the pack do not have any.
    > 
- Multiple different outcomes for the same recipe
    
    > Some modpacks like to use the *Polymorph* mod for this purpose. I just change the recipes to not overlap.
    > 

This list is also non-exhaustive but should help you give an idea of the main types of blemishes I look for and try to fix.

Please know that you will never be able to fix everything. Mods are often fickle, and as a third-party author, there is only so much you can do - still, you should try your best within your constraints, and avoid mods that create blemishes large enough that can take players out of the experience by themselves.

### Let the player discover

I’m not a fan of directly telling players what exists for them to use.

Ideally, you want to *lead* the player to the feature, while still making them believe they found the feature on their own. Telling people directly that they should make something takes away from the feeling of self-made creation that *Minecraft* relies on, and ends up in a more traditional style of linear game.

You can introduce players to features via hints in documentation, dotting the feature in the world, or strategically placing it in the middle of an important crafting chain, with some info on *JEI* of what the item does.

I like designing content discovery flows via a method I call *Backpropagation*, which is, in essence, having the player start with a goal or idea in mind, and from there going back to discover the steps they need to take to bring this idea to reality.

My personal favorite example of a game that implements *Backpropagation* is *RuneScape*, be it the modern version, or the oldschool one. Here’s an example of a player thinking “*I wish I could move around the world better”.* Click on the arrows on the left to backpropagate.

- “I wish I could move around the world better”
    - “Let’s look up what methods for transport exist”
        - “Fairy Rings can go to a lot of places, what do I need to clear to get those?”
            - “[Fairy Tale Part 1](https://oldschool.runescape.wiki/w/Fairytale_I_-_Growing_Pains)” Quest
                
                This quest has multiple requirements…
                
                - “Lost City” Quest
                    - Level 31 Crafting
                    - Level 36 Woodcutting
                - “Nature Spirit” Quest
                    - “The Restless Ghost” Quest
                    - “Priest in Peril” Quest

Once you’ve fully expanded the arrows, you can see we went from a vague “How do I get around” question to a list of actionable points we can work on to get to the end goal. We went from the end to the start, and without the game telling us where to start.

In fact, at this point we can backpropagate non-linearly. For example, let’s say you don’t want to level up your Crafting level - you can look for some quests that can give you crafting EXP.

- 30 Crafting
    
    By clicking on the Crafting skill on the wiki, we can see [quests that reward crafting EXP](https://oldschool.runescape.wiki/w/Crafting#Quests_rewarding_Crafting_experience).
    
    - “Tower of Life” Quest
        - Level 10 Construction
    - “The Golem” Quest
        - Level 25 Thieving
    - “Sheep Shearer” Quest
    - “Goblin Diplomacy” Quest
    - etc…

If you’ve expanded the “The Golem” Quest, you can see that you now need to level up Thieving. A player can then opt to level up Thieving via doing basic pickpocketing on NPCs or doing more quests, which would lead to another backpropagation.

The freedom this type of progression gives players is unparalleled - and as a consequence, allowing players to chart their own path and make their own goals leads to them feeling much more connected and satisfied while accomplishing them. It’s not what the game told you to do, it’s what *you* told yourself to do. That’s powerful, and in such an open game like *Minecraft* can be an essential tool to elevate an experience to new heights.

 If you’ve played either version of *RuneScape,* you know exactly what I mean.

The one major downside of backpropagation is that it requires a way for players to graph out the content available, as well as a way for the content to be visible from a *bird’s eye view*. Fortunately, every modded player already has a view of every item in the pack in *JEI -* so all that’s missing is for you, the pack maker, to organize the content in there in a digestible way that can be sorted and searched through by a player so they can build their own backpropagation.

> Both *Crucial 2* and *Bliss* utilize a combination of multiple systems to make this happen. Establishing potential goals is done through the *Gossip* system, and being able to search for blocks or items you may wish to get in *JEI.* Further backpropagation often comes from searching up specific keywords in *JEI,* like “bigger inventory”, which redirects to the Backpack from *Quark Oddities*.
> 

### Less is more

Looking back at the previous point, given a player will have full vision of everything they can do, it’s important to make it so everything is relevant. One very important term to keep in mind here is that of “[*analysis paralysis*](https://en.wikipedia.org/wiki/Analysis_paralysis)” - this is, essentially, the feeling that you can not make a proper choice due to being presented with far too many options.

Analysis Paralysis can often be thwarted by limiting the amount of options presented to the player at one time - but in a scenario where a player is eyeing through *JEI* to figure out what to do next, you don’t want to flood them with dozens, if not hundreds, of viable paths.

An area I usually try and cut down on is that of variant blocks. Many mods tend to add lots of variants for building blocks, be them texture variants, or shape variants. The more you add, the more complex each choice becomes. Picking a block palette goes from grabbing some colors that go together and finding blocks in those colors to creating complex textures, gradients, visual energy flows, etc. 

Depending on your style of pack, this may actually be what you want. I’m aware many packs exist with the focus of providing highly complex building options, and that’s great - but if that’s not your focus, try to avoid overloading the player.

Additionally, for building, the more options are present and the higher complexity is, the higher the skill ceiling becomes. When you increase the upper end of what a build can look like, other builds within the same context end up being compared to said high end, thus inadvertently also increasing the skill floor - the minimum required amount of building skill to create something that, in context, passes as “visually pleasing”.

Upping the amount of skill and effort required to make a good looking build within the context of your pack has the potential side effect of alienating many players on the lower end of those metrics. Consider that *Minecraft* is so incredibly popular in part because of its simplicity, and how approachable it is compared to more “flexible” options like CAD or 3D modelling.

> I don’t include popular massive building block mods such as *Chisel*, *Chipped*, **or *Chisels and Bits* in my packs due to the amount of mental overhead they introduce. *Chisels and Bits* in particular introduces such an overwhelming amount of options that it can leave non-users in the dust by comparison.
> 

### A bad apple can spoil the bunch

A chain is only as strong as its weakest link is. While not a direct translation to game design, you can think of it as the fact that one poor part in a game can bring down the whole thing.

How many games do you know that you recommend with a “yeah it’s really good, **but**…” - the weak chains, or bad parts of the game, are those “but”s. Ideally, you want to identify what the “but”s in your project are and either improve or cut them out.

This section is short, because all it intends to say is that it’s better to have less content than bad content. “Bad content” is subjective, and can often be content that’s just not up to par with other, higher quality, parts of the pack.

You can think of this as grading. If you’re an A+ student, getting a B+ is going to put your average grade down. B+ is still a good grade, but having gotten it lowers your average. In the same way, including poor quality features or mods lowers the average quality of your pack.

> I’ll refrain from naming any particular mods here as to not upset any of the authors, but in the design phase for *Crucial 2*, many entire mods were removed simply for not being up to par with the quality standards of the others.
> 

### Protect the player from themselves

Players are not stupid. When given multiple options to reach a goal, a player will, in the majority of situations, take that which is more efficient. This behavior is perfectly normal, and just simply human behavior - why would you purposely hamstring yourself when a more effective option is right there?

Your part as a designer comes in protecting the player from letting these urges ruin their fun.

> “*Make the fun part also the correct strategy to win*”
- Mark Rosewater, lead designer for *Magic, the Gathering,* at [GDC 2016](https://www.youtube.com/watch?v=QHHg99hwQGY)
> 

Here’s a very straightforward, abstract, example: Let’s say there’s an item in the game that can be acquired in two ways - a enjoyable way and a boring way. The enjoyable way creates 1000 per hour, and the boring way 2000. Any player wishing to create this item would naturally take the boring way, as without having tried out both ways prior, they do not know which one is enjoyable and which one is boring, as all they see is the efficiency.

In this situation, you’d either remove the boring way entirely, or make it so the fun way is more efficient.

Obviously, in a real life scenario, things aren’t as black and white, and this section requires a lot of nuance that I can’t fully fit here. It’s very important to watch how you and your playtesters interact with what you’ve created, and ensure they’re actually doing the fun stuff, and not getting themselves in uninteresting grinds you never intended to be ideal.

Also for the love of god please patch any dupes.

> In 2015, I heavily nerfed, and eventually removed, the passive generating flowers from *Botania* for this very reason.
You can read more about this decision from 7-years-ago me [here](https://www.notion.so/Sins-of-a-Solar-Empire-or-The-Passive-Generation-Conundrum-c5971117fd3648139a4a078541096fac). I do not fully agree with everything in this post to this day, but the historical context is definitely important.
> 

### Create avenues for fulfilment

Ultimately, as a designer, we want the player to *feel* something. I personally like to target the feeling of fulfilment upon finalizing an awesome build that’s present in vanilla *Minecraft -* that “I’ve done it!” moment when you look back at your creation and feel all the dopamine you’ve been building up while creating it release.

I have previously called this style of design “Player Focused Design”, which is the term I use to describe the mindset for features in *Quark Oddities.*

To do this, try to create challenges that players will face that require some sort of ingenuity or personal touch to solve. This often comes from messing with some sort of preconceived notion in the game, or by making the automatic method to generate some important resource be quirky and not immediately intuitive.

Combining with backpropagation and good a bird’s eye view of the game’s content, we can turn goals like “automate this resource” into a player having to identify what components they need, then looking for them individually, and going on further adventures or tangents to acquire them.

At the end of all that, given the player set themselves up for this goal and all it came with, and overcame the challenges (ideally, with a bit of nudging from documentation bits we laid down), they’ll feel incredibly fulfilled - and that completes *our* goal as well.

In essence, when creating, create something the player will create with.

> In *Crucial 2*, Iron Golems do not drop Iron Ingots, specifically to throw a wrench in the plans of making a standard Iron farm. Iron, and other ores, can still be farmed in the pack, using the Toretoise from *Quark*, but this method is much more complex, and requires using tools the pack provides.
> 

### Bringing it back

Having introduced my main pillars of design, it’s now time to get our hands dirty and make something with them.

At this point, I’ll have a preliminary mod list, a small list of immediate issues found in early testing, and ideas that I want to bring to life. Here’s the order in which I tend to tackle creating the pack:

- Establishing a first-pass list of content you wish to disable.
- Loading up every mod’s config and tweaking them initially as necessary - this often results in a decent amount of the immediate issues just going away as configs often allow you to remove features that are otherwise problematic.
- Hiding every item from *JEI* that was in the disabled items list, and then writing a simple *CraftTweaker* script that removes the recipes from all of them.
    
    > *Bliss* uses a python script to transpose the list of items hidden from *JEI* and generate the zs script to remove them.
    > 
- Creating recipe changes or removals to help bridge mods or fix issues.
    
    > In both *Crucial 2* and *Bliss*, Paintings and Scaffolding are made using Canvas from *Farmer’s Delight,* encouraging players to delve into that mod. Furthermore, Rope from *Farmer’s Delight* is an important resource in *Crucial 2*, and its recipe is changed to require Yak Hair from *Environmental*.
    > 
- Open ended development - at this point, the pack should be in a fundamentally *decent* state. Conflicts should be fixed, and a very basic flow to progress should be introduced. Now it’s time to start making more in-depth changes. This falls under the **Vision** part of development, and will ultimately depend on what your goal is.
    
    > In *Bliss*, a lot of this was configuring miscellaneous parts of game to adapt to the peaceful-like gameplay - such as writing custom *Apathy* mod rulesets, and changing loot tables.
    > 
- Writing documentation for the pack - this part includes writing straightforward guides in a *Patchouli* book, as well as smaller micro-documentation in *JEI,* and laying the foundations for backpropagation via tagging items correctly for search and setting up hints and goals for players to look for.
- Playtesting - at this point, the pack should be in a reasonably finished state, and it’s time to throw it at a small trusted crowd to break it and give you feedback on how it plays. The feedback you receive will lead you back to a previous step in this list. Repeat until you’re content with the results.

One thing to keep in mind during this process is that your mod list is *not* set in stone. In my development cycles, many mods end up added or cut during late stages of development, either because some specific feature was missing from the pack, or because after development, the mod now falls into pitfalls that go against the design principles.

Creating a pack is not a science, and you’ll find yourself going back and forth between the steps often, as you identify further issues and vision goals. Make sure to take note of everything that needs to be done, and do some basic playtesting yourself to make sure what you created is actually enjoyable.

> *Bliss* development used *GitHub* issues to note down bugs and missing pieces. I’ve also previously used *Trello* when collaborating with Dylan for the original *Crucial.*
> 

With the pack created, I whip up a fancy image to market it and post it on social media. Given I already have a large audience and am a house name, I don’t think it’s fit for me to give marketing advice, but at the very least post about it on the [/r/feedthebeast](https://www.reddit.com/r/feedthebeast/) subreddit with a catchy graphic so people know it exists.

> The promo graphic for *Bliss* was commissioned from Kach and made specifically to appeal to a more casual crowd.
> 

Set up a GitHub to take in bugs, maybe a Discord server to chat with the pack’s players, and throw it on CurseForge. Congratulations, your pack is now released.

# 🔄 Post-Release

Now that the pack is out for everyone to try, we need to talk about continuing it.

It’s obvious you should be updating your pack reasonably often to keep up with the mod updates inside, so I won’t go into basic maintenance. Instead, I’d like to focus on how to take feedback from your players, how to dissect gameplay, and how to approach content updates.

### Feedback is dangerous

Everyone has an opinion, but not all opinions are made equal. When listening to feedback from your players, there are two important steps in assessing it: **Filtering** and **Distilling**.

**Filtering** describes the process of figuring out which feedback is appropriate and which isn’t. Often filtering involves understanding who your target audience is, and what sort of feedback falls outside that of your target audience.

Understanding what feedback is appropriate is important. If you’re making a pack focused on a relaxed and sedentary gameplay experience, you may want to discard feedback from someone asking for more combat and adventure, for example.

The more people you want to appeal to, the less focused your experience will have to be. Sometimes it is worth taking off-target feedback to expand your audience, but more often than not, those players might be better served by a different pack.

> *Create* is very often suggested as an addition for both *Crucial 2* and *Bliss.* While *Crucial 2* would eventually receive optional integration via a Pull Request, I’ve stood firm in not adding it to the base packs, as it does not fit what the pack is trying to do.
> 

**Distilling** means understanding what a bit of feedback *truly* means - it’s delving into the root of an issue, rather than taking something a player says at face value.

Very often, a player might complain about something, attempt to identify the problem or a solution on their own, and then pitch you their conclusion. The problem here is that most players aren’t game designers, and their conclusion is very often wrong.

Here’s an example. In *Crucial 2*, many players had requested the *Simple Storage Network* mod - a mod I absolutely did not want to add to the pack due to the complexity difference. I was faced with the following problem:

- Is this feedback appropriate? If so, what’s the root cause of the issue?

Since the suggested mod is out of scope, it would be easy to dismiss the feedback as out of scope itself, which I did for a bit. On a further inspection, though, I distilled the problem down - people were asking for a storage solution because the pack has a storage problem. There were too many different items and not enough space to put them.

This seems pretty obvious in hindsight, but that wasn’t what I was being told. I was being told to “add this mod…”, and I had to extrapolate the “…to solve this problem” part. Knowing what the root issue behind the feedback was, I could now fix the complaints without doing directly what I was requested and didn’t want to do.

> In order to solve the storage problem in *Crucial 2*, I added the Crate to *Quark Oddities,* which was specifically designed to hold a high variety of items, but not a high quantity.
> 

Misunderstanding feedback can lead to your pack getting worse over time, or it losing its focus and charm. Players generally mean well when they take the time to come to you, but incorrectly reading their pleas can mean eroding the quality design you put time into.

Taking in feedback from players, much like most of the development process, is not a science. Over time you may learn how to filter better, and not over-filter, or to better distill meaning from more opaque feedback. Taking in feedback is a skill, and as such, one you build over time.

> In *Bliss*, I set up a long Google Docs form to take feedback during the beta stage, which asked many specific questions I wanted to know.
> 

### Gameplay is precious

If you have access to a let’s play, live stream, or live blog, **treasure it**.

Unfiltered gameplay without your intervention is the greatest source of feedback you can ask for. By watching a player experience your creation, you can see what they do, how they react to your changes, how they adapt and what their thoughts are. If possible, try not to intervene, as your average player won’t have your help, and you want to keep that source of raw feedback handy.

> For both *Crucial 2* and *Bliss,* I had my friends Wyld and Ellpeck stream the pack, while I lurked in chat to watch them play and their chat’s reactions. I also watched let’s plays. Both these sources proved invaluable in finding needed changes.
> 

### Content updates are scary

Read. Every. Changelog.

When mods add new content, it’s important to take it with the same scrutiny that you applied to adding a new mod.

Remember what I said before, that content starts as *not added*. For updates, you have to act as the gatekeeper for the new features.  Everything that applies when adding the mod applies here too.

It’s important to understand that once a feature is *added* to the modpack, you can no longer go back to *not added -* the best you can do is *removed -* and players **do not like** content they’re used to being removed.

> *Crucial 2* had inconsistent maintenance updates due to mods updating regularly with new content for 1.16. Every update required me to assess the new features.
> 

# 🎁 Wrap-Up

That’s all I got for you today. I hope this document helped you learn about the pack development process, or at least grab a few tips if you’re experienced already.

Big thank you to Rorax, amadornes, Kamefrede, and Kinomora for proofreading this and helping me fix my countless grammar mistakes, and thank you to everyone who enjoyed my packs and even gave me enough confidence in my design to put it into words.

If you make any packs informed by my musings here, please give me a poke on your social media of choice, I’d love to see it.

[Discuss this post on reddit](https://www.reddit.com/r/feedthebeast/comments/xfwblh/how_i_design_modpacks_vazkiis_blog/).

<3
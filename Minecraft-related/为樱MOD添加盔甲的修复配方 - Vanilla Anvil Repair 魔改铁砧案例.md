# 为樱MOD添加盔甲的修复配方 - Vanilla Anvil Repair 魔改铁砧案例
## 前言
[[1.12.2][Sakura——樱] 在新版本中还原日式文化](https://www.mcbbs.net/thread-895337-1-1.html)

随着樱 MOD 被越来越多的玩家熟知和喜爱，大家对于樱 MOD 的玩法也有了更深入的了解。

前不久我从一位群友那里得知，樱 MOD 的特色护甲：武士套装和士兵套装，

不能在铁砧上用樱色钻石 / 钢锭修复，只能做两个再用铁砧或工作台合在一起来修复，或者借助经验修补附魔。

了解到这个情况后，我进行了简单的孤狗搜索，

了解到有一款魔改模组 [Vanilla Anvil Repair](https://www.mcbbs.net/thread-1210670-1-1.html) 可以很简单地添加铁砧修复的配方，

正好可以解决这个问题。
## 问题解决步骤
1. 安装 CraftTweaker 和 Vanilla Anvil Repair 两个模组。
2. 启动游戏一次，再关闭游戏。<br>这一步是为了让 CraftTweaker 生成脚本文件夹 `.minecraft/script`，<br>让 Vanilla Anvil Repair 生成默认配置文件 `.minecraft\config\vanillaanvilrepair.cfg`。
3. 将 Vanilla Anvil Repair 配置文件 `.minecraft\config\vanillaanvilrepair.cfg` 中的<br>`B:repairsIncreaseCost=false` 改为 `B:repairsIncreaseCost=true`。
4. 将本帖子的附件放入 CraftTweaker 的脚本文件夹 `.minecraft/script`。
5. 重启游戏，完成。
## 使用效果
[![2bdJuq.png](https://z3.ax1x.com/2021/06/15/2bdJuq.png)](https://imgtu.com/i/2bdJuq)

[![2bd8vn.png](https://z3.ax1x.com/2021/06/15/2bd8vn.png)](https://imgtu.com/i/2bd8vn)

可以看到，武士套装和士兵套装都可以在铁砧上用樱钻或钢锭修复了。
## 脚本源码
```ZenScript
import crafttweaker.item.IIngredient;
import mods.vanillaanvilrepair.addRepairEntry;
val samuraiArmor as IIngredient[] = [
    <sakura:samurai_helmet>,
    <sakura:samurai_chest>,
    <sakura:samurai_pants>,
    <sakura:samurai_shoes>
];
val solderArmor as IIngredient[] = [
    <sakura:soldier_helmet>,
    <sakura:soldier_chest>,
    <sakura:soldier_pants>,
    <sakura:soldier_shoes>
];
for armor in samuraiArmor
{
    addRepairEntry(armor, <sakura:sakura_diamond>);
}
for armor in solderArmor
{
    addRepairEntry(armor, <ore:ingotSteel>);
}
```
## 结语
Vanilla Anvil Repair 是一个功能极其简单的魔改模组，用它魔改铁砧也只有唯一的一个函数可供使用。

我们可以借助 ZenScript 的数组按元素遍历语法，简单地将同种材料的盔甲编组，统一赋予修复配方。

事实上魔改并没有什么很高的门槛，只要你对你的 MC 游戏有功能需求或者想法，

只要简单地读一读文档，随手写一写，就可以满足你的不少需要。

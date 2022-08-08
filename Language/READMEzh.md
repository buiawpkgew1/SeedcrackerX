# SeedCrackerX [![Github All Releases](https://img.shields.io/github/downloads/19MisterX98/SeedCrackerX/total.svg)]

## 语言选择

[中文](./READMEzh.md) [Русский](./READMEru.md)

## 我活动于：

- [我的 Discord](https://discord.gg/JRmHzqQYfp)
- [油管（视频网站）](https://www.youtube.com/channel/UCby9ZxEjJCqmccQGF3GSYlA)

## 安装

下载并安装 [fabric模组加载器](https://fabricmc.net/use/)

下载SeedCrackerX最新的 [版本或预发布](https://github.com/19MisterX98/SeedCrackerX/releases)

将.jar文件放入您的模组目录中，或者是为了原版启动器的 %appdata%/.minecraft/mods/文件夹或者是您自己的 MultiMC 实例文件夹。

#### 可选

下载最新的 [版本的 MultiConnect 到 MC 版本上的服务器连接](https://github.com/Earthcomputer/multiconnect/releases)

## 数据库设置

由于这个模组已被许多人使用，我已决定创建一个谷歌的服务器种子。 如果您在配置界面启用数据库选项，模组将直接将10+个玩家服务器的破解种子发送到Google表中。

[工作表](https://docs.google.com/spreadsheets/d/1tuQiE-0leW88em9OHbZnH-RFNhVqgoHhIt9WQbeqqWw/edit?usp=sharing)

## 使用

### 1.17.X及以下

在世界各地运行，直到模组找到一个垃圾。 在模组找到一个后，破解过程自动开始。 如果它没有给你一个世界种子，你可能想要找到另一个地牢。

这个模组还支持裂种子：
- [结构和末尾柱子](https://youtu.be/aUuPSZVPH8E?t=462)
- [诡异菌](https://www.youtu.be/HKjwgofhKs4)

### 1.18.X 和未来潜在版本

邓珠破裂，真菌打碎已不再起作用。

通过"/seed gui"进入配置菜单，确保绿宝石、网关、生物群落， 沙漠水井和经燃的真菌被禁用，因为它们没有更新，可能会提供错误的数据。

为了打碎，你现在需要从上面列出的结构中找到5个结构：\
沙漠金字塔，丛林模板，女巫小屋，船难，Igloos，Pillager前哨。

任何组合都是有效的。 例如：3个沉船、1坐金字塔和1个金字塔。 您可以用"/seed data bits"跟踪您的进程(查看可提升结构的 bits 计数) 当它周围有一个轮廓时发现一个结构。 在你得到足够的数据后，破解过程会自动开始。 这个过程需要1-5分钟左右。 在这之后, 模组可能会要求你找到其他结构。 在同一类型的比特和结构较少的情况下更可能发生这种情况。 在减少你的结构种子后，这个模组会通过粪便位置或哈希的种子使你的世界种子变得更猛烈。

  ### 支持的结构
    - 海底神殿
    - 末地城
    - 埋藏的宝藏
    - 沙漠神殿
    - 丛林神庙
    - 沼泽小屋
    - 沉船
    - 冰屋
    - 掠夺者前哨站


  ### 支持的装饰
    - 地牢
    - 末地折跃门
    - 沙漠水井
    - 绿宝石矿石
    - 诡异真菌

## 指令

  ### GUI命令
  - `/seed gui`

  打开配置界面，如服务器mc版本、所有查找器、数据库和渲染模式。 其中大多数都有命令替代品，但不应再使用。


  ### 查找重新加载命令
  - `/seed finder reload`

  重置已加载的模板片段以找到以前找不到的结构。


  ### 数据命令
  - `/seed data clear`

  清除所有收集到的数据，而不需要重新日志。 这对多世界服务器有用。

  - `/seed data bits`

  显示已收集多少信息。 普通比特用于终端支柱+结构碎裂。 冷却开始于32位。 液化比特用于提升结构碎裂。 冷却开始于40位。

  - `/seed data restore`

  当您离开一个世界，模组将会在 .minecraft/config 目录文件中保存当前收集的结构信息。 在重新加入后，您可以使用此命令还原它。



  ### 调试 -> 命令
  - `/seed cracker debug`

  显示更多信息


  ### 数据库命令
  - `/seed database`

  打开由模组维护的 [谷歌板](https://docs.google.com/spreadsheets/d/1tuQiE-0leW88em9OHbZnH-RFNhVqgoHhIt9WQbeqqWw/edit?usp=sharing)

## 视频教程

Neil's:
- [1.15](https://youtu.be/1ChmLi9og8Q)
- [1.16](https://youtu.be/aUuPSZVPH8E)

Mine:
- [Dungeon 破解 & 终端柱裂。](https://youtu.be/8ytfZ2MXosY)
- [地狱碎裂。](https://youtu.be/HKjwgofhKs4)
- [结构崩溃了](https://www.youtu.be/UXVrBaOR8H0)


## 设置工作区

-克隆当前仓库

-运行 `gradlew genSource <idea|eclipse>`

## 构建模组

-更新 `build.gradle` 和 `fra.mod.json` 中的版本。

-运行 `gradlew build`。

## 其他模组的 API

- 在你的build.gradle 中包含种子打印机-api和jitpack。
  
      repositories {
          mavenCentral()
          maven { url "https://jitpack.io" }
      }
      
      dependencies {
          implementation (include('com.github.19MisterX98.SeedcrackerX:seedcrackerx-api:master-SNAPSHOT')) {transitive = false}
      }

- 添加实现api接口的类
  
      package misterx.myMod.seedManagemnet.SeedCrackerEP
      
      import kaptainwutax.seedcrackerX.api.SeedCrackerAPI;
      
      public class SeedCrackerEP implements SeedCrackerAPI {
          @Override
          public void pushWorldSeed(long seed) {
              //do something
              Foo.bar(seed)
          }
      }

- 告诉您的入口所在位置
  
      "entrypoints": {
        "main": [...],
        "client": [...],
        "server": [...],
        "seedcrackerx": [
          "misterx.myMod.seedManagemnet.SeedCrackerEP"
        ]
      },

## 贡献者

[KaptainWutax](https://github.com/KaptainWutax) - 作者

[neil](https://www.youtube.com/watch?v=aUuPSZVPH8E) - 视频教程

[Nekzuris](https://github.com/Nekzuris) - README

[19MisterX98](https://www.youtube.com/channel/UCby9ZxEjJCqmccQGF3GSYlA) - 这个派生的

[farkon00](https://github.com/farkon00) - 俄语版README

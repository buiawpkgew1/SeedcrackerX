# SeedCrackerX [![Github 所有版本](https://img.shields.io/github/downloads/19MisterX98/SeedCrackerX/total.svg)]

## Discord

PS:请以后更新翻译的同学参照en_us.json改的地方并在同样的位置添加，让后人修改时更方便。

## 安装

- [Discord](https://discord.gg/JRmHzqQYfp)
- [油管（视频网站）](https://www.youtube.com/channel/UCby9ZxEjJCqmccQGF3GSYlA)

## 使用方法

下载并安装 [fabric模组加载器](https://fabricmc.net/use/)

### 官方启动器/其他启动器

下载并安装[Fabric](https://fabricmc.net/use/).

#### 可选

### MultiMC

## 命令（已废弃，请使用GUI）.

由于这个模组已被许多人使用，我已决定创建一个谷歌的服务器种子。 如果您在配置界面启用数据库选项，模组将直接将10+个玩家服务器的破解种子发送到Google表中。

[工作表](https://docs.google.com/spreadsheets/d/1tuQiE-0leW88em9OHbZnH-RFNhVqgoHhIt9WQbeqqWw/edit?usp=sharing)

## 视频教程

### 1.17.X及以下

在这个世界上跑来跑去，直到Mod找到一个地牢。 当Mod找到一个地牢后，破解过程就会自动开始。 如果它没有获取世界种子，你可能需要找另一个地牢。

下载 Mod Menu 最新[发布版](https://www.curseforge.com/minecraft/mc-mods/modmenu/files)
- [结构和末尾柱子](https://youtu.be/aUuPSZVPH8E?t=462)
- [Warped Fungus(诡异菌)](https://www.youtu.be/HKjwgofhKs4)

### 1.18.X及未来版本

下载 Fabric API 最新[发布版](https://www.curseforge.com/minecraft/mc-mods/fabric-api/files)

把.jar文件放在你的mods目录下, 或者是%appdata%/.minecraft/mods/文件夹, 用于官方启动器, 或者是你自己的MultiMC实例文件夹.

#### 可选

任何组合都是有效的。 例如：3 艘沉船、1 座金字塔和 1 座冰屋。 您可以使用“/seed data bits”查看您的进程。 在你得到足够的数据后，破解过程会自动开始。 这个过程需要1-5分钟左右。 在这之后, 模组可能会要求你找到其他结构。 在同一类型的比特和结构较少的情况下更可能发生这种情况。 在减少你的结构种子后，这个模组会通过粪便位置或哈希的种子使你的世界种子变得更猛烈。

  ### 模组安装
    - Ocean Monument(海底神殿)
    - End City(末地城)
    - Buried Treasure(埋藏的宝藏)
    - Desert Pyramid(沙漠神殿)
    - Jungle Temple(丛林神庙)
    - Swamp Hut(沼泽小屋)
    - Shipwreck(沉船)
    - 冰屋
    - 掠夺者前哨站


  ### 支持的装饰
    - Dungeon(地牢)
    - End Gateway(地牢)
    - Desert Well(沙漠水井)
    - Emerald Ore(绿宝石矿石)
    - 诡异菌

## 设置工作区

  地牢破解，诡异菌破解不再起作用。
  - `/seed cracker <ON/OFF>`

  打开配置界面，如服务器mc版本、所有查找器、数据库和渲染模式。 其中大多数都有命令替代品，但不应再使用。


  ### `/seed finder reload`
  - `再次搜索加已加载的区域`

  重置已加载的模板片段以找到以前找不到的结构。


  ### ### 数据指令
  - `/seed data clear`

  清除所有收集到的数据，而不需要重新日志。 这对多世界服务器有用。

  - `/seed data bits`

  显示已收集多少信息。 普通比特用于终端支柱+结构碎裂。 冷却开始于32位。 液化比特用于提升结构碎裂。 戒严开始于40位。

  - `/seed data restore`

  当您离开一个世界，模组将会在 .minecraft/config 目录文件中保存当前收集的结构信息。 在重新加入后，您可以使用此命令还原它。



  ### 破解器指令
  - `/seed cracker debug`

  显示调试信息


  ### 数据库命令
  - `/seed database`

  打开由模组维护的 [谷歌板](https://docs.google.com/spreadsheets/d/1tuQiE-0leW88em9OHbZnH-RFNhVqgoHhIt9WQbeqqWw/edit?usp=sharing)

## 编译此Mod

通过“/seed gui”进入配置菜单并确保绿宝石矿石、末地折跃门、生物群系、沙漠水井和诡异菌被禁用，因为它们没有更新并且可能提供错误的数据。
- [1.15](https://youtu.be/1ChmLi9og8Q)
- [1.16](https://youtu.be/aUuPSZVPH8E)

为了破解你现在需要找到下列结构中至少 5 个：
- [Dungeon 崩溃 & 终端柱裂。](https://youtu.be/8ytfZ2MXosY)
- [地狱碎裂。](https://youtu.be/HKjwgofhKs4)
- [结构崩溃了](https://www.youtu.be/UXVrBaOR8H0)


## 贡献者

沙漠神殿、丛林神殿、女巫小屋、沉船、雪屋、掠夺者前哨站。

-运行 `gradlew genSources <idea|eclipse>`.

## 构建模组

-在 `build.gradle` 和 `fabric.mod.json` 里更新版本.

### 支持的结构

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
  
      下载 SeedCrackerX 最新<a href="https://github.com/19MisterX98/SeedCrackerX/releases">发布版</a>

- 告诉您的入口在哪里了 fram.mod.json
  
      "entrypoints": {
        "main": [...],
        "client": [...],
        "server": [...],
        "seedcrackerx": [
          "misterx.myMod.seedManagemnet.SeedCrackerEP"
        ]
      },

## 贡献者

这个mod的命令前缀是/seed.

### 渲染命令 -`/seed render outlines <ON/OFF/XRAY>`

[Nekzuris](https://github.com/Nekzuris) - README

### 搜索器命令 -`/seed finder type <FEATURE_TYPE> (ON/OFF)`

`/seed finder category (BIOMES/ORES/OTHERS/STRUCTURES) (ON/OFF)`

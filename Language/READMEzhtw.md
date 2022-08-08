# SeedCrackerX [![Github 所有版本](https://img.shields.io/github/downloads/19MisterX98/SeedCrackerX/total.svg)]

## Discord

PS:请以后更新翻译的同学参照en_us.json改的地方并在同样的位置添加，让后人修改时更方便。

## 安装

- [Discord](https://discord.gg/JRmHzqQYfp)
- [Youtube](https://www.youtube.com/channel/UCby9ZxEjJCqmccQGF3GSYlA)

## 使用方法

下载并安装 [fabric模组加载器](https://fabricmc.net/use/)

### 官方启动器/其他启动器

下载并安装[Fabric](https://fabricmc.net/use/).

#### 選項

### MultiMC

## Database

Since the mod is used by many people, I have decided to create a Google sheet for server seeds. If you enable the database option in the config gui the mod will send cracked seeds from 10+ player servers directly to the Google sheet.

[The Sheet](https://docs.google.com/spreadsheets/d/1tuQiE-0leW88em9OHbZnH-RFNhVqgoHhIt9WQbeqqWw/edit?usp=sharing)

## 视频教程

### 1.17.X及以下

在这个世界上跑来跑去，直到Mod找到一个地牢。 当Mod找到一个地牢后，破解过程就会自动开始。 如果它没有获取世界种子，你可能需要找另一个地牢。

下载 Mod Menu 最新[发布版](https://www.curseforge.com/minecraft/mc-mods/modmenu/files)
- [Structures and Endpillars](https://youtu.be/aUuPSZVPH8E?t=462)
- [Warped Fungus(诡异菌)](https://www.youtu.be/HKjwgofhKs4)

### 1.18.X及未来版本

下载 Fabric API 最新[发布版](https://www.curseforge.com/minecraft/mc-mods/fabric-api/files)

把.jar文件放在你的mods目录下, 或者是%appdata%/.minecraft/mods/文件夹, 用于官方启动器, 或者是你自己的MultiMC实例文件夹.

#### 可选

任何组合都是有效的。 例如：3 艘沉船、1 座金字塔和 1 座冰屋。 您可以使用“/seed data bits”查看您的进程。 在你得到足够的数据后，破解过程会自动开始。 This process takes around 1-5 mins. The mod may ask you to find additional structures after this. It's more likely to happen with fewer bits and structures of the same type. After reducing your structure seeds, the mod will brute force your world seed via dungeon positions or hashed seed.

  ### 模组安装
    - Ocean Monument(海底神殿)
    - End City(末地城)
    - Buried Treasure(埋藏的宝藏)
    - Desert Pyramid(沙漠神殿)
    - Jungle Temple(丛林神庙)
    - Swamp Hut(沼泽小屋)
    - Shipwreck(沉船)
    - Igloo
    - Pillager Outpost


  ### 支持的装饰
    - Dungeon(地牢)
    - End Gateway(地牢)
    - Desert Well(沙漠水井)
    - Emerald Ore(绿宝石矿石)
    - Warped Fungus

## 设置工作区

  地牢破解，诡异菌破解不再起作用。
  - `/seed cracker <ON/OFF>`

  Opens the config gui where you can modify settings like the server mc-version, all finders, database and rendermode. There are command alternatives for most of this, but they should'nt be used anymore.


  ### `/seed finder reload`
  - `再次搜索加已加载的区域`

  Rescans the loaded Chunks to find structures that weren't found before.


  ### ### 数据指令
  - `/seed data clear`

  Clears all the collected data without requiring a relog. This is useful for multi-world servers.

  - `/seed data bits`

  Display how many bits of information have been collected. Normal bits are used for end pillar + structure cracking. Cracking starts at 32 bits. Lifting bits are used for liftable structure cracking. Cracking starts at 40 bits.

  - `/seed data restore`

  When you leave a world, the mod will save currently collected structure information in a file of the .minecraft/config directory. After rejoining, you can restore it with this command.



  ### 破解器指令
  - `/seed cracker debug`

  显示调试信息


  ### Database Command
  - `/seed database`

  Opens a [google sheet](https://docs.google.com/spreadsheets/d/1tuQiE-0leW88em9OHbZnH-RFNhVqgoHhIt9WQbeqqWw/edit?usp=sharing) that is maintained by the mod

## 编译此Mod

通过“/seed gui”进入配置菜单并确保绿宝石矿石、末地折跃门、生物群系、沙漠水井和诡异菌被禁用，因为它们没有更新并且可能提供错误的数据。
- [1.15](https://youtu.be/1ChmLi9og8Q)
- [1.16](https://youtu.be/aUuPSZVPH8E)

为了破解你现在需要找到下列结构中至少 5 个：
- [Dungeon cracking & end pillar cracking](https://youtu.be/8ytfZ2MXosY)
- [Nether cracking](https://youtu.be/HKjwgofhKs4)
- [Structure cracking](https://www.youtu.be/UXVrBaOR8H0)


## 贡献者

沙漠神殿、丛林神殿、女巫小屋、沉船、雪屋、掠夺者前哨站。

-运行 `gradlew genSources <idea|eclipse>`.

## Building the Mod

-在 `build.gradle` 和 `fabric.mod.json` 里更新版本.

### 支持的结构

## API for other mods

- Include seedcracker-api and jitpack in your build.gradle
  
      repositories {
          mavenCentral()
          maven { url "https://jitpack.io" }
      }
      
      dependencies {
          implementation (include('com.github.19MisterX98.SeedcrackerX:seedcrackerx-api:master-SNAPSHOT')) {transitive = false}
      }

- Add a class that implements the api interface
  
      下载 SeedCrackerX 最新<a href="https://github.com/19MisterX98/SeedCrackerX/releases">发布版</a>

- Tell fabric.mod.json where your entrypoint is
  
      "entrypoints": {
        "main": [...],
        "client": [...],
        "server": [...],
        "seedcrackerx": [
          "misterx.myMod.seedManagemnet.SeedCrackerEP"
        ]
      },

## Contributors

这个mod的命令前缀是/seed.

### 渲染命令 -`/seed render outlines <ON/OFF/XRAY>`

[Nekzuris](https://github.com/Nekzuris) - README

### 搜索器命令 -`/seed finder type <FEATURE_TYPE> (ON/OFF)`

`/seed finder category (BIOMES/ORES/OTHERS/STRUCTURES) (ON/OFF)`

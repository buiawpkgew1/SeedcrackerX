# SeedCrackerX [![Github All Releases](https://img.shields.io/github/downloads/19MisterX98/SeedCrackerX/total.svg)]

## 語言選擇

[中文](./READMEzh.md) [Русский](./READMEru.md)

## I'm active on:

- [Discord](https://discord.gg/JRmHzqQYfp)
- [Youtube](https://www.youtube.com/channel/UCby9ZxEjJCqmccQGF3GSYlA)

## 安裝

Download and install the [fabric mod loader](https://fabricmc.net/use/)

Download the latest [release or pre-release](https://github.com/19MisterX98/SeedCrackerX/releases) of SeedCrackerX

put the .jar files in your mod directory, either %appdata%/.minecraft/mods/ folder for the vanilla launcher or your own MultiMC instance folder.

#### 選項

Download the latest [release](https://github.com/Earthcomputer/multiconnect/releases) of Multiconnect to connect to servers on lower MC versions

## Database

Since the mod is used by many people, I have decided to create a Google sheet for server seeds. Since the mod is used by many people, I have decided to create a Google sheet for server seeds. If you enable the database option in the config gui the mod will send cracked seeds from 10+ player servers directly to the Google sheet.

[The Sheet](https://docs.google.com/spreadsheets/d/1tuQiE-0leW88em9OHbZnH-RFNhVqgoHhIt9WQbeqqWw/edit?usp=sharing)

## Usage

### 1.17.X及以下

Run around in the world until the mod finds a dungeon. After the mod found one the cracking process starts automatically. If it doesn't give you a world seed, you may want to find another dungeon. After the mod found one the cracking process starts automatically. If it doesn't give you a world seed, you may want to find another dungeon.

This mod also supports cracking the seed via:
- [Structures and Endpillars](https://youtu.be/aUuPSZVPH8E?t=462)
- [warped fungus](https://www.youtu.be/HKjwgofhKs4)

### 1.18.X及未來版本

Dungeon cracking, fungus cracking don't work anymore.

Go to the config menu via "/seed gui" and make sure that Emeralds, Gateways, Biomes, Desert wells and Warped fungi are disabled since they aren't updated and can give wrong data.

For cracking, you now need to find 5 structures from the listed ones:\
Desert pyramids, Jungle temples, Witch huts, Shipwrecks, Igloos, Pillager Outposts

Any combination is valid. 例如：3個沉船、1坐金字塔和1個金字塔。 例如：3個沉船、1坐金字塔和1個金字塔。 You can track your process with "/seed data bits" (look at the bits count for liftable structures) A structure is found when there is an outline around it. After you get enough, the cracking process starts automatically. This process takes around 1-5 mins. The mod may ask you to find additional structures after this. It's more likely to happen with fewer bits and structures of the same type. You can track your process with "/seed data bits" (look at the bits count for liftable structures) A structure is found when there is an outline around it. After you get enough, the cracking process starts automatically. This process takes around 1-5 mins. The mod may ask you to find additional structures after this. It's more likely to happen with fewer bits and structures of the same type. After reducing your structure seeds, the mod will brute force your world seed via dungeon positions or hashed seed.

  ### Supported Structures
    - Ocean Monument
    - 末地之城
    - Buried Treasure
    - 沙漠神殿
    - 叢林神廟
    - 沼澤小屋
    - 沉船
    - 冰屋
    - 掠奪者前哨站


  ### 支持的裝飾
    - 地牢
    - 終界折躍門
    - 沙漠水井
    - 綠寶石礦
    - 诡异真菌

## 指令

  ### GUI Command
  - `/seed gui`

  Opens the config gui where you can modify settings like the server mc-version, all finders, database and rendermode. There are command alternatives for most of this, but they should'nt be used anymore. There are command alternatives for most of this, but they should'nt be used anymore.


  ### Finder Reload Command
  - `/seed finder reload`

  Rescans the loaded Chunks to find structures that weren't found before.


  ### 數據指令
  - `/seed data clear`

  Clears all the collected data without requiring a relog. This is useful for multi-world servers. This is useful for multi-world servers.

  - `/seed data bits`

  Display how many bits of information have been collected. Normal bits are used for end pillar + structure cracking. Cracking starts at 32 bits. Lifting bits are used for liftable structure cracking. Cracking starts at 40 bits.

  - `/seed data restore`

  When you leave a world, the mod will save currently collected structure information in a file of the .minecraft/config directory. After rejoining, you can restore it with this command. After rejoining, you can restore it with this command.



  ### 破解器指令
  - `/seed cracker debug`

  顯示調試信息


  ### Database Command
  - `/seed database`

  Opens a [google sheet](https://docs.google.com/spreadsheets/d/1tuQiE-0leW88em9OHbZnH-RFNhVqgoHhIt9WQbeqqWw/edit?usp=sharing) that is maintained by the mod

## 影片教學

Neil's:
- [1.15](https://youtu.be/1ChmLi9og8Q)
- [1.16](https://youtu.be/aUuPSZVPH8E)

为了破解你现在需要找到下列结构中至少 5 个：
- [Dungeon cracking & end pillar cracking](https://youtu.be/8ytfZ2MXosY)
- [Nether cracking](https://youtu.be/HKjwgofhKs4)
- [Structure cracking](https://www.youtu.be/UXVrBaOR8H0)


## Setting up the Workspace

沙漠神殿、丛林神殿、女巫小屋、沉船、雪屋、掠夺者前哨站。

-运行 `gradlew genSources <idea|eclipse>`.

## Building the Mod

-在 `build.gradle` 和 `fabric.mod.json` 里更新版本.

-Run `gradlew build`.

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
  
      package misterx.myMod.seedManagemnet.SeedCrackerEP
      
      import kaptainwutax.seedcrackerX.api.SeedCrackerAPI;
      
      public class SeedCrackerEP implements SeedCrackerAPI {
          @Override
          public void pushWorldSeed(long seed) {
              //do something
              Foo.bar(seed)
          }
      }

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

[KaptainWutax](https://github.com/KaptainWutax) - Author

[neil](https://www.youtube.com/watch?v=aUuPSZVPH8E) - Video Tutorial

[Nekzuris](https://github.com/Nekzuris) - README

[19MisterX98](https://www.youtube.com/channel/UCby9ZxEjJCqmccQGF3GSYlA) - Author of this fork

[farkon00](https://github.com/farkon00) - README in russian

# SeedCrackerX [![Github All Releases](https://img.shields.io/github/downloads/19MisterX98/SeedCrackerX/total.svg)]

## Моя активность:

Загрузите и установите [загрузчик fabric](https://fabricmc.net/use/)

## Установка

- [Дискорд](https://discord.gg/JRmHzqQYfp)
- [Ютуб](https://www.youtube.com/channel/UCby9ZxEjJCqmccQGF3GSYlA)

## База данных

Загрузите последний [релиз или пре-релиз](https://github.com/19MisterX98/SeedCrackerX/releases) SeedCrackerX

Поместите .jar файл в папку с модами, либо %appdata%/.minecraft/mods/ для ванильного лаунчера, либо папка модов вашей сборки в MultiMC.

Загрузите последний [релиз](https://github.com/Earthcomputer/multiconnect/releases) Multiconnect для подключения к серверам на более старых версиях MC

#### Опционально

Download the latest [release](https://github.com/Earthcomputer/multiconnect/releases) of Multiconnect to connect to servers on lower MC versions

## Использование

Поскольку мод используется многими людьми, я решил создать google таблицу для серверных сидов. Если вы включите опцию базы данных в конфигурации, мод отправит найденные сиды для серверов с 10+ игроками непосредственно в google таблицу.

[Таблица](https://docs.google.com/spreadsheets/d/1tuQiE-0leW88em9OHbZnH-RFNhVqgoHhIt9WQbeqqWw/edit?usp=sharing)

## Команды

### 1.17.X и ниже

Пробегитесь по миру, пока мод не найдёт сокровищницу (комнату со спаунером). После того как мод нашел одну из них, процесс поиска начнётся автоматически. Если это не дало вам сид мира, вы можете найти другую сокровищницу.

Поиск через сокровищницы и искажённые грибы больше не работает.
- [структуры и башни в крае](https://youtu.be/aUuPSZVPH8E?t=462)
- [искажённые грибы](https://www.youtu.be/HKjwgofhKs4)

### 1.18.X и потенциальные будущие версии

Зайдите в меню конфигурации через "/seed gui" и убедитесь, что Emeralds, Gateways, Biomes, Desert wells и Warped fungi отключены, поскольку они не обновляются и могут выдавать неправильные данные.

Теперь для нахождения сида нужно найти 5 структур из перечисленных:\
Пустынные храмы, храмы в джунглях, хижины ведьм, затонувшие корабли, иглу, аванпосты разбойников

For cracking, you now need to find 5 structures from the listed ones:\
Desert pyramids, Jungle temples, Witch huts, Shipwrecks, Igloos, Pillager Outposts

Допустима любая комбинация структур. Например: 3 затонувших корабля, 1 пустынный храм и 1 иглу. Вы можете отслеживать свой прогресс с помощью "/seed data bits". Структура считается обнаруженной, когда вокруг неё есть контур. После того как вы набрали достаточное количество бит, процесс поиска начинается автоматически. Это займёт 1-5 минут После этого мод может попросить вас найти дополнительные структуры. Это, скорее всего, произойдет с малым количеством битов и структур одного типа. После сокращения ваших структурных сидов мод начнёт перебирать сиды мира с помощью позиций сокровищниц или хэшированных сидов.

  ### Графический интерфейс
    - Подводная крепость
    - Город Края
    - Клад
    - Пустынный храм
    - Храм в джунглях
    - Хижина ведьмы
    - Затонувший корабль
    - Иглу
    - Аванпост разбойников


  ### Поддерживаемые Декораторы
    - Сокровищница
    - Врата Края
    - Колодец
    - Изумрудная руда
    - Искажённый гриб

## Туториалы на английском

  Neil:
  - `/seed gui`

  Открывает графический интерфейс, в котором вы можете изменить такие настройки, как MC версия сервера, средства поиска, база данных и режим отображения. Для большей части этого существуют альтернативные команды, но их более не следует использовать.


  ### Поисковик
  - `/seed finder reload`

  Повторно сканирует загруженные чанки, чтобы найти структуры, которые не были найдены ранее.


  ### Данные
  - `/seed data clear`

  Очищает все собранные данные, не требуя переподключения к серверу. Это полезно для серверов с несколькими мирами.

  - `/seed data bits`

  Показывает количество собранных бит информации. Normal bits are used for end pillar + structure cracking. Cracking starts at 32 bits. Lifting bits are used for liftable structure cracking. Cracking starts at 40 bits.

  - `/seed data restore`

  Когда вы покинете мир, мод сохранит собранную в данный момент информацию о структурах в директории .minecraft/config. После повторного подключения вы можете восстановить её с помощью этой команды.



  ### Дебаг
  - `/seed cracker debug`

  Показывает дополнительную информацию


  ### База данных
  - `/seed database`

  Открывает [google таблицу](https://docs.google.com/spreadsheets/d/1tuQiE-0leW88em9OHbZnH-RFNhVqgoHhIt9WQbeqqWw/edit?usp=sharing), которая поддерживается модом

## Настройка рабочего пространства

Мои:
- [1.15](https://youtu.be/1ChmLi9og8Q)
- [1.16](https://youtu.be/aUuPSZVPH8E)

[KaptainWutax](https://github.com/KaptainWutax) - Автор
- [Dungeon cracking & end pillar cracking](https://youtu.be/8ytfZ2MXosY)
- [Nether cracking](https://youtu.be/HKjwgofhKs4)
- [Structure cracking](https://www.youtu.be/UXVrBaOR8H0)


## Сборка мода

[neil](https://www.youtube.com/watch?v=aUuPSZVPH8E) - Видео туториалы

Выполните `gradlew build`.

## API для других модов

[19MisterX98](https://www.youtube.com/channel/UCby9ZxEjJCqmccQGF3GSYlA) - Автор форка

[~~farkon00~~](https://github.com/farkon00) - перевод README на русский

## Контрибуторы

- Клонируйте репозиторий.
  
      repositories {
          mavenCentral()
          maven { url "https://jitpack.io" }
      }
      
      dependencies {
          implementation (include('com.github.19MisterX98.SeedcrackerX:seedcrackerx-api:master-SNAPSHOT')) {transitive = false}
      }

- Выполните `gradlew genSources <idea|eclipse>`.
  
      package misterx.myMod.seedManagemnet.SeedCrackerEP
      
      import kaptainwutax.seedcrackerX.api.SeedCrackerAPI;
      
      public class SeedCrackerEP implements SeedCrackerAPI {
          @Override
          public void pushWorldSeed(long seed) {
              //do something
              Foo.bar(seed)
          }
      }

- Укажите в fabric.mod.json точку входа
  
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

# Counter-Strike Portable (Critical Strike) — Global Maps Archive

[English](#english) | [Русский](#русский)

---

## Русский

### О проекте
Данный репозиторий является открытым историческим архивом пользовательских и официальных карт для легендарного мобильного шутера **Counter-Strike Portable** (позже известного как *Critical Strike Portable* / *CS-Portable*), разрабатывавшегося командой Studio OnMars (Игорь Лёвочкин) в 2012–2015 гг.

После отключения официальных серверов автозагрузки (`://cs-portable.com`) сотни уникальных локаций, созданных сообществом, оказались утеряны. Цель этого проекта — собрать, структурировать и сохранить цифровое наследие игры в одном месте. Все файлы восстановлены из веб-архивов (Wayback Machine) и старых фанатских бэкапов.


### Структура архива / Repository Structure
Карты разделены по целевым платформам (в соответствии с архитектурой Unity AssetBundles):
* `/Android` — Карты для мобильной версии игры (`*.unity3dAndroid`).
* `/Windows` — Карты для ПК-версии (`*.unity3dStandaloneWindows`).
* `/iOS` — Карты для iPhone/iPad (`*.unity3dIphone`).
* `/WebPlayer` — Браузерные карты (`*.unity3d`).


### Инструкция по установке (Android)
1. Скачайте необходимый файл карты из папки `Android`.
2. Перенесите файл во внутреннюю память вашего устройства по пути установки игры (обычно в корневую папку во внутренней памяти или на SD-карте, в зависимости от версии игры — ищите папку `cs-portable` или `CriticalStrikePortable`).
3. Запустите игру, перейдите в одиночный режим или создание сервера и выберите карту из локального списка.

*Примечание: Совместимость карт зависит от версии игры. Из-за различий в версиях движка Unity некоторые старые карты могут некорректно работать на поздних версиях игры (v3.x).*

---

## English

### About The Project
This repository is an open historical archive of custom and official maps for the legendary mobile shooter **Counter-Strike Portable** (later known as *Critical Strike Portable* / *CS-Portable*), developed by Studio OnMars (Igor Leochkin) between 2012 and 2015.

Following the shutdown of the official map delivery servers (`://cs-portable.com`), hundreds of community-made maps were lost. The goal of this project is to collect, preserve, and catalog this digital heritage. All files contained herein have been recovered via the Wayback Machine and legacy community backups.

### Repository Structure
Maps are organized by platform architecture (Unity AssetBundles compatibility):
* `/Android` — Maps compiled for Android (`*.unity3dAndroid`).
* `/Windows` — Maps compiled for Windows Standalone (`*.unity3dStandaloneWindows`).
* `/iOS` — Maps compiled for iOS (`*.unity3dIphone`).
* `/WebPlayer` —Legacy Unity WebPlayer maps (`*.unity3d`).

### How to Install (Android)
1. Download the preferred map file from the `Android` directory.
2. Move the file to your device's internal storage inside the game directory (typically a folder named `cs-portable` or `CriticalStrikePortable` on your SD card/internal storage root).
3. Open the game, go to Singleplayer or Host Game, and select the loaded map.

*Note: Map compatibility strictly depends on the game version. Due to changes in Unity engine versions over the lifecycle of the game, some legacy maps might glitch or crash on later client versions (v3.x).*

---

## Contribution / Как помочь проекту
If you possess old `.unity3d` map files on your legacy devices or hard drives, please feel free to open a Pull Request or create an Issue to contribute to the archive.

Если у вас сохранились файлы карт на старых устройствах или дисках, вы можете отправить их через Pull Request или создать тему в разделе Issues.

# AnyDevStudio

Open source tools and example games for PS5 homebrew. The main project is AnyDevKit Studio, a desktop
app for making games from drag and drop scenes and jigsaw logic blocks, without living in a terminal.
The other repositories are games and demos made with it or with
[AnyDevKit](https://github.com/boykopovar/AnyDevKit), the SDK it is built on.

## Repositories

| Repository | What it is | Latest release | Platforms |
|---|---|---|---|
| [AnyDevKit Studio](https://github.com/AnyDevStudio/AnyDevKit-Studio) | Desktop studio for making PS5 homebrew games and apps with AnyDevKit. Qt 6 and C++20, MIT. | [v0.1.0-alpha.5](https://github.com/AnyDevStudio/AnyDevKit-Studio/releases/latest) | Runs on macOS (Apple Silicon), Windows x64 and Linux x86_64. Builds games for PS5, Windows and Linux. |
| [Greenhollow](https://github.com/AnyDevStudio/Greenhollow) | A small 2.5D RPG with ink-drawn art, made in Studio with no hand-written game code. GPL-2.0-only. | [v0.3.0](https://github.com/AnyDevStudio/Greenhollow/releases/latest) | PS5 homebrew, Windows x64, Linux x86_64, Mac with Apple silicon |
| [Pixel Fireworks](https://github.com/AnyDevStudio/PixelFireworks) | A silent pixel-art fireworks show written in C++ with AnyDevKit. GPL-2.0-only. | None yet, build from source | PS5 homebrew |
| [AnyDevKit (fork)](https://github.com/AnyDevStudio/AnyDevKit) | Our fork of boykopovar's SDK: the macOS arm64 build of `adk` that Studio installs on a Mac, and the branches of our pull requests upstream. | [0.1.7-mac1](https://github.com/AnyDevStudio/AnyDevKit/releases) | Runs on macOS (Apple Silicon) |

## AnyDevKit Studio

AnyDevKit is a command line SDK that compiles C++ and GLSL and packages the result for PS5. Studio puts
a visual workspace on top of it: place shapes, text, images, sprites and tilemaps on a stage, snap
together events and actions as logic blocks, and press one button to get a PS5 package. The same game
can also be built as a Windows `.zip` or a Linux `.tar.gz`.

![The Village scene of Greenhollow on the stage in Studio](https://raw.githubusercontent.com/AnyDevStudio/AnyDevKit-Studio/main/docs/screenshots/stage.png)

| | |
|---|---|
| ![The logic blocks of Greenhollow's Title scene, with the variables and sounds on the left](https://raw.githubusercontent.com/AnyDevStudio/AnyDevKit-Studio/main/docs/screenshots/blocks.png) | ![The Game page with Greenhollow's icon and background, and Windows chosen as the format](https://raw.githubusercontent.com/AnyDevStudio/AnyDevKit-Studio/main/docs/screenshots/game-page.png) |
| Rules snapped together from blocks | One button builds for PS5, Windows or Linux |

Studio is in alpha. The full flow has been tested on Apple Silicon macOS, and CI also builds Studio on
Windows and Linux. Windows and Linux builds of games build from a Mac but have not been run on Windows
or Linux by us. Nothing has been run on a real PS5 yet. The
[Studio README](https://github.com/AnyDevStudio/AnyDevKit-Studio#what-it-does) lists the state of each
feature.

## Greenhollow

A small RPG made entirely in Studio: one `scene.json` and one `logic.json`, about 12,800 blocks in all.
Make a Warrior, a Ranger or a Mage, help the people of the village and of Brookmere, and follow the
green dew into the woods and down into the cave. It has six places, five quests, a pet cat or dog, two
players on one screen, friends online each on their own console, and saving and loading.

| | |
|---|---|
| ![The village: two cottages, Mira's garden with three slimes, two players and the townsfolk](https://raw.githubusercontent.com/AnyDevStudio/Greenhollow/main/docs/screens/village.jpg) | ![Brookmere's market square with its fountain, shops and animal shelter](https://raw.githubusercontent.com/AnyDevStudio/Greenhollow/main/docs/screens/town.jpg) |
| The village, with Mira's garden and two players | Brookmere, the market town |
| ![The dark forest with wolves, boars, a blue slime and a cat following its owner](https://raw.githubusercontent.com/AnyDevStudio/Greenhollow/main/docs/screens/forest.jpg) | ![The cave of crystals, after the Stone Warden falls](https://raw.githubusercontent.com/AnyDevStudio/Greenhollow/main/docs/screens/cave.jpg) |
| Wolf packs and boars in the forest | The cave and its Stone Warden |

![The host in the village and a friend in the meadow, at the same moment](https://raw.githubusercontent.com/AnyDevStudio/Greenhollow/main/docs/screens/online-apart.jpg)

Online, each friend has a screen of their own: here the host is in the village while a friend walks the meadow.

These pictures are drawn by a script from the game's real state at those moments. They are not captures
from a GPU. The game has been played through by scripted bots against the real game runtime, alone, with
two players on one screen and online. It has run in a window on one Apple silicon Mac, where two copies
played together online. It has not been run on a real PS5, on Windows or on Linux. See
[Where it has run](https://github.com/AnyDevStudio/Greenhollow#where-it-has-run) for the details.

## Download

- [AnyDevKit Studio, latest release](https://github.com/AnyDevStudio/AnyDevKit-Studio/releases/latest):
  packages for macOS on Apple Silicon, Windows x64 and Linux x86_64. They are not signed, so your
  system will warn you the first time you open one.
- [Greenhollow, latest release](https://github.com/AnyDevStudio/Greenhollow/releases/latest): a PS5
  homebrew package (`.ffpfsc`), and builds for Windows x64, Linux x86_64 and Mac with Apple silicon.

## Get involved

Everything here is public. Fork it, try it, open an issue or send a pull request. Start with the
[contributing guide](https://github.com/AnyDevStudio/AnyDevKit-Studio/blob/main/CONTRIBUTING.md).

## Credits

This work exists because of [AnyDevKit](https://github.com/boykopovar/AnyDevKit), created by
[boykopovar](https://github.com/boykopovar). Every PS5 package Studio builds is compiled and packaged
by AnyDevKit, and the Windows and Linux builds of games run on the desktop libraries of
[AnyPS5](https://github.com/boykopovar/AnyPS5), also by boykopovar.

AnyDevStudio is an independent project, not an official boykopovar project, and not affiliated with or
endorsed by Sony Interactive Entertainment. PlayStation and PS5 are trademarks of their respective
owner. Packages made with AnyDevKit are homebrew and cannot be published on PlayStation Store.

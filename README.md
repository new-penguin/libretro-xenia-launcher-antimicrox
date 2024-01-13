# libretro-xenia-launcher

![Xenia-Emulator](https://github.com/new-penguin/libretro-xenia-launcher-antimicrox/assets/139792946/dc1f3dc7-ecce-41e1-97bc-9b7e3c97275e)


Based on [libretro-dolphin-launcher](https://github.com/RobLoach/libretro-dolphin-launcher) and [libretro-PCSX2-launcher](https://github.com/eduardomozart/libretro-pcsx2-launcher). 

Launch Microsoft Xbox 360 games through [Xenia](https://xenia.jp/), directly from [RetroArch](http://www.libretro.com/) with full controller support using [antimicrox](https://github.com/AntiMicroX/antimicrox/).


## Installation

Download the Linux core from releases and skip to step 2 or...

1. Compile the core
  ``` bash
  git clone https://github.com/new-penguin/libretro-xenia-launcher-antimicrox
  cd libretro-xenia-launcher-antimicrox
  make
  ```

2. Copy the core file to the RetroArch cores directory. For example, to copy to the default core directory
  ``` bash
  cp xenia_launcher_libretro.so /usr/lib/libretro/xenia_launcher_libretro.so
  cp xenia_launcher_libretro.info /usr/share/libretro/info/xenia_launcher_libretro.info
  ```

3. Make sure [Xenia](https://xenia.jp/) is installed either natively or have wine installed and the xenia directory copied to ./config/retroarch/system/xenia/xenia.exe as well as [antimicrox](https://github.com/AntiMicroX/antimicrox/). I recommend as of now that you use it via Wine because the native Linux version is very experimental and I've not had much luck with it.

## Usage

1. Scan your 360 games in RetroArch. I recommend manually scanning and importing because Retroarch doesn't have a 360 database to know what files are game executables.

2. Associate your games with the Microsoft 360 (Xenia Launcher) core

3. Configure antimicrox to use your distro's 'close window' binding to your controller button preference. Or you can use my pre-configured controller mappings [here](https://ufile.io/9t4vnq6m) for the 360 and Xbox One controllers. Place in your user ~/ directory. In the provided examples I've mapped LS click + RS click to exit Xenia. Also you should make sure Xenia is configured correctly to run a game first as there's a bit of initial setup involved.
  
3. And once done you should be able to launch and switch games directly from the RetroArch menu.

3. Alternatively, you can run games through the command line as this is the only way I've tested the launcher so far. Retroarch currently has an issue crashing when playlist entries have no file extensions.
  ``` bash
  retroarch -L xenia_launcher_libretro.so "game.xex"
  ```

## Contributors

- [Rob Loach](http://github.com/robloach)
- [Alcaro](https://github.com/Alcaro)
- [Eduardo Mozart de Oliveira](https://github.com/coldscientist)

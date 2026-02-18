# ![GameboyIcon](http://i.imgur.com/ROUq7NT.gif) Awesome Game Boy Development

#### [Join us on Discord](https://gbdev.io/chat.html) [![Discord Badge](https://img.shields.io/badge/dynamic/json.svg?label=chat\&colorB=green\&suffix=%20online\&query=presence_count\&uri=https://discordapp.com/api/guilds/303217943234215948/widget.json)](https://discord.gg/tKGMPNr)

A curated list of awesome Game Boy (Color) Development resources, tools, docs, related projects and open-source ROMs. Inspired by the [awesome](https://github.com/sindresorhus/awesome) ⭐ 438,155 | 🐛 70 | 📅 2026-01-28 list thing.

You can find a (way cooler) web version of this list [here](https://gbdev.github.io/resources).

## Contents

* [Introduction](#introduction)
  * [Disambiguation](#disambiguation)
* [Community](#community)
* [Documentation](#documentation)
  * [Misc](#misc)
  * [Opcodes](#opcodes)
  * [Game Boy Color](#game-boy-color)
  * [Hardware](#hardware)
  * [Peripherals](#peripherals)
  * [Cartridges](#cartridges)
* [Emulator Development](#emulator-development)
  * [Testing](#testing)
* [Software Development](#software-development)
  * [Assemblers](#assemblers)
  * [Compilers](#compilers)
    * [Experimental/Proof of Concepts](#experimentalproof-of-concepts)
  * [Emulators](#emulators)
  * [Tools](#tools)
    * [Engines](#engines)
    * [Development tools](#development-tools)
    * [Graphics utilities](#graphics-utilities)
    * [Hardware and ROM utilities](#hardware-and-rom-utilities)
    * [Music drivers and trackers](#music-drivers-and-trackers)
* [Programming](#programming)
  * [ASM](#asm)
    * [Sources](#sources)
    * [Timings](#timings)
    * [Boilerplates](#boilerplates)
    * [Syntax highlighting packages](#syntax-highlighting-packages)
  * [C](#c)
* [Homebrews](#homebrews)
  * [ASM](#asm-1)
  * [C](#c-1)
  * [GB Studio](#gb-studio)
  * [Demos](#demos)
* [Reverse Engineering](#reverse-engineering)
  * [Game Disassemblies](#game-disassemblies)
* [Game Boy Camera](#game-boy-camera)
  * [Retrieving Images](#retrieving-images)
  * [Changing the camera's behavior](#changing-the-cameras-behavior)
  * [Post-processing](#post-processing)
* [Related projects](#related-projects)
  * [Directories](#directories)
  * [Websites](#websites)
* [About](#about)
  * [Contribute](#contribute)
  * [License](#license)
  * [Acknowledgements](#acknowledgements)
  * [Sponsors](#sponsors)

## Introduction

* [The Game Boy, a hardware autopsy](https://www.youtube.com/playlist?list=PLu3xpmdUP-GRDp8tknpXC_Y4RUQtMMqEu)
* [The Ultimate Game Boy Talk](https://media.ccc.de/v/33c3-8029-the_ultimate_game_boy_talk)

> ### Disambiguation
>
> #### Game Boy Advance
>
> Game Boy Advance development is covered by another project, the [awesome-gbadev](https://github.com/gbdev/awesome-gbadev) ⭐ 1,281 | 🐛 4 | 📅 2026-01-30 list.
> GBA, however, *can run* GB/GBC games. It does so in a slightly different way compared to native hardware: this is covered in the Emulator Development section of this list.
>
> #### Game Boy Color and Super Game Boy
>
> This list is focused on the original *Game Boy* (GB or DMG, 1989), the *Game Boy Color* (GBC or CGB) and the *Super Game Boy* (SGB) are very similar systems, with a few important distinctions, such as:
>
> * Different hardware specifications;
> * Specific hardware and software features;
> * Specific registers;
> * Specific bugs, quirks and exploitable behaviours.
>
> If you aim to develop your software for SGB or GBC, or you want to know how it runs on the other systems, you may want to take advantage and adapt to these differences, check the [Game Boy Color](#game-boy-color) category and look for specific references to GBC/CGB and SGB.

## Community

* [Chat channels](https://gbdev.io/chat)
* [Forum](https://gbdev.gg8.se/forums/)

## Documentation

* [The Cycle-Accurate Game Boy Docs](https://github.com/AntonioND/giibiiadvance/blob/master/docs/TCAGBD.pdf) ⭐ 206 | 🐛 0 | 🌐 C | 📅 2026-01-25 - A precise documentation by AntonioND to make a cycle-accurate Game Boy emulator.
* [Game Boy Project Report](http://www.cs.columbia.edu/~sedwards/classes/2019/4840-spring/reports/GameBoy.pdf) - Report of an hardware [emulator](https://github.com/kitsuneh/SVGameBoy) ⭐ 8 | 🐛 0 | 🌐 SystemVerilog | 📅 2021-04-15 (on a Terasic DE1-SoC Board) developed as final project for the CSEE4840 Embedded Systems Design course at Columbia University.
* [**Pan Docs**](https://gbdev.github.io/pandocs/) - The single, most comprehensive technical reference to Game Boy available to the public. Corrected, updated and maintained by the community.
* [Complete Technical Reference](https://gekkio.fi/files/gb-docs/gbctr.pdf) - by Gekkio.
* [Game Boy Architecture: A Practical Analysis](https://www.copetti.org/writings/consoles/game-boy/) - by Rodrigo Copetti.

#### Opcodes

* [gb-opcodes](https://gbdev.github.io/gb-opcodes/optables/) - Opcodes table
* [RGBDS opcodes reference](https://rgbds.gbdev.io/docs/gbz80.7) - A reference of all instructions, including short descriptions, cycle and byte counts, and explanations of flag modifications.

### Game Boy Color

* [Bootstrap ROM](https://tcrf.net/Game_Boy_Color_Bootstrap_ROM)
* [Unused Palettes](https://tcrf.net/Notes:Game_Boy_Color_Bootstrap_ROM)
* [Colorization palettes in the BIOS](https://forums.nesdev.com/viewtopic.php?p=114388\&sid=c3d4ce08cfd9d9c834958d4f148750c3#p114388)
* [Boot ROM Disassembly](https://gist.github.com/drhelius/6063265)
* [GBC Hicolour notes](https://romhack.github.io/doc/gbcHiColour/) - A technical note regarding Hicolour mode trick for Game Boy Color and its realization in the GBC game “Crystalis”.

### Hardware

* [Related custom hardware](https://github.com/Gekkio/gb-hardware) ⭐ 361 | 🐛 1 | 🌐 Shell | 📅 2023-07-20 - by Gekkio.
* [ESP8266 GB Printer](https://github.com/applefreak/esp8266-gameboy-printer) ⭐ 49 | 🐛 0 | 🌐 C++ | 📅 2020-10-12 - A device that emulates the GB Printer and lets you retrieve images using WiFi.
* [dmg-schematics](https://github.com/msinger/dmg-schematics) ⭐ 34 | 🐛 2 | 🌐 KiCad Schematic | 📅 2026-02-17 - Schematics and annotated overlay for the DMG-CPU B chip, extracted from die photos, made with KiCad. Also contains Electric VLSI library with layouts for some of the cells and memories.
* [ESP8266 GB Dev Board](https://github.com/applefreak/esp8266-gameboy-dev-board) ⭐ 28 | 🐛 0 | 📅 2020-10-14 - Dev board for Game Boy accessories development, powered by ESP8266.
* [DMG Schematics](http://gbdev.gg8.se/wiki/articles/DMG_Schematics) - Hardware schematics.
* [The Game Boy Project](http://marc.rawer.de/Gameboy/Docs/GBProject.pdf) - Provides a study on the hardware and detailed constructional information for the implementation of three 8-bit bidirectional parallel ports.
* [fruttenboel](https://web.archive.org/web/20220628023315/https://verhoeven272.nl/fruttenboel/Gameboy/index.html) - Page with loads of information on the hardware, custom boards to interface with the console and other related projects.
* [Game Boy hardware database](https://gbhwdb.gekkio.fi/) - Data and photos of various types of Game Boy consoles.

### Peripherals

* [Edge of Emulation](https://shonumi.github.io/articles.html), a series of articles about emulating and investigating Game Boy accessories. Also available as [technical documents](https://github.com/shonumi/gbe-plus/tree/master/src/docs/technical) ⭐ 572 | 🐛 76 | 🌐 C++ | 📅 2026-01-08 in the GBE- emulator documentation.
  * [Mobile Adapter GB](https://shonumi.github.io/articles/art14.html) - Internet connectivity and DLC on the Game Boy Color.
  * [The Game Boy Printer](https://shonumi.github.io/articles/art2.html)
  * [Pocket Sonar](https://shonumi.github.io/articles/art13.html) - A blue cart with built-in sonar hardware.
  * [Zok Zok Heroes](https://shonumi.github.io/articles/art8.html)  - Zok Zok Heroes' Full Changer, a motion-activated accessory.
  * [Infrared Madness](https://shonumi.github.io/articles/art11.html) - Infrared communication on the Game Boy Color.
  * [Game Boy 4-Player Adapter](https://shonumi.github.io/articles/art9.html) - DMG-07.
  * [Barcode Boy](https://shonumi.github.io/articles/art7.html) - The first Game Boy card-scanner.
  * [Barcode Taisen Bardigun](https://shonumi.github.io/articles/art6.html) - A late 90s DMG-GBC barcode reader.
* [Arduino Game Boy Printer Emulator](https://github.com/mofosyne/arduino-gameboy-printer-emulator) ⭐ 353 | 🐛 3 | 🌐 C++ | 📅 2024-06-15 - Emulating a Game Boy Printer via the Game Boy Link cable with an Arduino.
* [Game Boy Camera RE](https://github.com/AntonioND/gbcam-rev-engineer) ⚠️ Archived - Documentation about GB Camera and tools used to reverse engineer it by using Arduino.
* [Dan Docs](https://shonumi.github.io/dandocs.html) - Obscure Game Boy hardware documentation.
* [DMG-07 Technical Documentation](https://raw.githubusercontent.com/shonumi/gbe-plus/master/src/docs/technical/DMG_07.txt)
* [Creating photo realistic images with neural networks and a Gameboy Camera](http://www.pinchofintelligence.com/photorealistic-neural-network-gameboy/)
* [The Game Boy Printer](https://shonumi.github.io/articles/art2.html) - An in-depth technical document about the printer hardware, the communication protocol and the usual routine that games used for implementing the print feature.
* [Ben Heck Reverse Engineers Game Boy Printer](https://www.youtube.com/watch?v=43FfJvd-YP4) (Errata: the used thermal paper is expired, 4 colors are actually printable).
* [Mobile Game Boy Adapter](https://bulbapedia.bulbagarden.net/wiki/Mobile_Game_Boy_Adapter)
* [GB KISS LINK MODEM](http://nectaris.tg-16.com/GB-KISS-LINK-FAQ-hudson-gameboy-nectaris.html)

### Cartridges

* [GB Flash Cartridges for Sale](https://bbbbbr.github.io/GameBoy-Flash-Carts/) - A List of available, ready-made Game Boy Flash Cartridges.
* [AntonioND's docs](https://github.com/AntonioND/giibiiadvance/tree/master/docs) ⭐ 206 | 🐛 0 | 🌐 C | 📅 2026-01-25 - Corrected schematics and infos on cartridge header data.
* [Gekkio's Game Boy cartridge types](http://gekkio.fi/blog/2015-02-14-mooneye-gb-gameboy-cartridge-types.html) - An overview on existing cartridge types.
* Gekkio's cartridge analysis:
  * [DMG-BEAN-02](http://gekkio.fi/blog/2015-05-18-mooneye-gb-cartridge-analysis-dmg-bean-02.html);
  * [MBC1](http://gekkio.fi/blog/2015-05-17-mooneye-gb-cartridge-analysis-fortress-of-fear.html);
  * [no MBC](http://gekkio.fi/blog/2015-02-28-mooneye-gb-cartridge-analysis-tetris.html).
* Pinout, registers descriptions and VHDL code of some cartridge types on Tauwasser's wiki:
  * [MBC1](https://wiki.tauwasser.eu/view/MBC1)
  * [MBC2](https://wiki.tauwasser.eu/view/MBC2)
  * [MMM01](https://wiki.tauwasser.eu/view/MMM01)
* [Game Boy Cartridges Schematics](http://www.devrs.com/gb/files/gb.html) - Schematics for MBC2 and MBC3 types.
* [Cartridges PCB photos](https://imgur.com/a/D5bpC)
* [MBC1+RAM+Battery cartridge Schematic](http://www.devrs.com/gb/files/mbc1.gif) - First schematics by Jeff Frohwein.
* [MBC1 and MBC2 cartridges circuits](http://fms.komkon.org/GameBoy/Tech/Carts.html) - and explanation on how these MBC bank switch and control RAM.
* [GB Rom List](origin/CartridgeList.csv) - Navigable table of every game released with details on their cartridges.
* [Game Boy cartridge PCB photos](http://gekkio.fi/blog/2016-03-19-game-boy-cartridge-pcb-photos.html)

#### Custom cartridges

* [Homebrew-Gameboy-Cartridge](https://github.com/dwaq/Homebrew-Gameboy-Cartridge) ⭐ 139 | 🐛 0 | 📅 2020-02-13 - Eagle library, schematic, and board files for a cartridge PCB using an Atmel AT49F040 as ROM.
* [Nekocart](https://github.com/zephray/NekoCart-GB) ⭐ 131 | 🐛 5 | 🌐 Assembly | 📅 2024-06-06 - Open-source flash cartridge using an Xilinx CPLD as MBC5 ([Post](https://hackaday.io/project/41160-nekocart-cpld-gameboy-cartridge)).
* [Homebrew Gameboy Color Cartridge](https://github.com/Xyl2k/Gameboy-Color-Cartridge) ⭐ 75 | 🐛 0 | 📅 2021-05-24 - Board layout for an EEPROM powered cartridge.
* [Gameboy-MBC5-MBC1-Hybrid](https://github.com/insidegadgets/Gameboy-MBC5-MBC1-Hybrid) ⭐ 54 | 🐛 1 | 🌐 C | 📅 2023-05-17 - CPLD implementation of a MBC5/MBC1 Hybrid cartridge.
* [Emulating a GameBoy Cartridge](https://dhole.github.io/post/gameboy_cartridge_emu_1/) - Emulating the functionality of a Game Boy cartridge with the development board STM32F4.
* [Wolf](http://www.happydaze.se/wolf/) - Game Boy cartridge with co-processor.
* [Reiner Ziegler's Game Boy page](http://reinerziegler.de.mirrors.gg8.se/) - Commercial and homemade programmable cartridges and programming systems. Tutorials, wiring and schematics provided.

#### Misc

* [Introduction to Game Boy Hacking](http://pepijndevos.nl/sha2017/workshop.pdf) - Workshop introducing basic assembly, debugging and reverse engineering.
* [GBSOUND.txt](https://github.com/bwhitman/pushpin/blob/master/src/gbsound.txt) ⭐ 54 | 🐛 1 | 🌐 C | 📅 2021-07-12 - A document detailing the Game Boy sound engine.
* [gbdev FAQs](http://www.devrs.com/gb/files/faqs.html) - Must read by Jeff Frohwein.
* [Game Boy Bootrom](http://www.neviksti.com/DMG/DMG_ROM.asm) - Commented dump of the DMG bootrom.
* [Differences between the Z80 and the gameboy's processor](http://www.z80.info/z80gboy.txt)
* [Gameboy 2BPP Graphics Format](http://www.huderlem.com/demos/gameboy2bpp.html) - Information on how the Game Boy interprets VRAM tile data to color pixels.

## Emulator Development

* [Emulation of Nintendo Game Boy](https://github.com/Baekalfen/PyBoy/blob/master/extras/PyBoy.pdf) ⭐ 5,077 | 🐛 33 | 🌐 Python | 📅 2026-01-31 - Overview of the Game Boy hardware with the perspective of building an emulator.
* [Game Boy Doctor](https://github.com/robert/gameboy-doctor) ⭐ 263 | 🐛 5 | 🌐 Python | 📅 2024-10-06 - A command line tool for comparing logs from your emulator to those from a known-correct one. Useful for line-by-line debugging of Blargg's test ROMs.
* [Reverse Engineering fine details of Game Boy hardware](https://www.youtube.com/watch?v=GBYwjch6oEE) - 43 minutes talk by Gekkio given at Disobey 2018 ([errata](https://gekkio.fi/blog/2018-02-05-errata-for-reverse-engineering-fine-details-of-game-boy-hardware.html)).
* [DMG-01](https://rylev.github.io/DMG-01/public/book/) - An educational Gameboy Emulator in Rust and a companion book explaining its development. \*[Oh Boy! Creating a Game Boy Emulator in Rust](https://media.ccc.de/v/rustfest-rome-3-gameboy-emulator)- is a talk given at Rust Fest 18 about this.
* [Building a Game Boy emulator in JavaScript](http://imrannazar.com/gameboy-Emulation-in-JavaScript) - Step by step tutorial.
* [Writing a Game Boy emulator, Cinoop](https://cturt.github.io/cinoop.html)
* [0dmg](https://jeremybanks.github.io/0dmg/2018/05/23/getting-started.html) - Learning Rust by building a partial Game Boy emulator.
* [RealBoy Emulator](https://realboyemulator.wordpress.com/posts/) - A series of posts about the design and implementation of the RealBoy Emulator.
* [Codeslinger](http://www.codeslinger.co.uk/pages/projects/gameboy.html) - Another series of posts documenting the building of an emulator.
* [Why did I spend 1.5 months creating a Gameboy emulator?](http://blog.rekawek.eu/2017/02/09/coffee-gb/) - Blog post.
* [binjgb rewind](https://binji.github.io/2017/12/31/binjgb-rewind.html) - Implementing a \*rewind- feature.
* [binjgb on the web](https://binji.github.io/2017/02/26/binjgb-on-the-web-part-1.html) - Porting of the binjgb emulator to Web Assembly. [(Part 2)](https://binji.github.io/2017/02/27/binjgb-on-the-web-part-2.html)
* [binjgb debugging hangs](https://binji.github.io/2017/05/03/debugging-hangs.html) - Investigations on emulations quirks.
* [Decoding Gameboy Z80 opcodes](https://gb-archive.github.io/salvage/decoding_gbz80_opcodes/Decoding%20Gamboy%20Z80%20Opcodes.html) - How to algorithmically decode Game Boy instructions (as opposed to writing one huge switch-case statement).
* [Porting a GO Game Boy emulator to WebAssembly](https://djhworld.github.io/post/2018/09/21/i-ported-my-gameboy-color-emulator-to-webassembly/)
* [About swotGB](https://mitxela.com/projects/swotgb/about) - Notes about the development of a Game Boy emulator in JavaScript.
* [List of open source emulators](origin/EMULATORS.md)

### Testing

* [144p Test Suite](https://github.com/pinobatch/240p-test-mini/tree/master/gameboy) ⭐ 280 | 🐛 7 | 🌐 Assembly | 📅 2025-09-02 - Port of Artemio Urbina's 240p Test Suite to the Game Boy.
* [dmg-acid2](https://github.com/mattcurrie/dmg-acid2) ⭐ 229 | 🐛 5 | 🌐 Assembly | 📅 2024-05-23 and [cgb-acid2](https://github.com/mattcurrie/cgb-acid2) ⭐ 83 | 🐛 0 | 🌐 Assembly | 📅 2021-02-26 - Basic PPU rendering tests.
* [Mealybug Tearoom Tests](https://github.com/mattcurrie/mealybug-tearoom-tests) ⭐ 65 | 🐛 0 | 🌐 Assembly | 📅 2020-12-19
* [SameSuite](https://github.com/LIJI32/SameSuite) ⭐ 43 | 🐛 2 | 🌐 Assembly | 📅 2025-10-11
* [MBC3 RTC test ROM](https://github.com/aaaaaa123456789/rtc3test) ⭐ 39 | 🐛 1 | 🌐 Assembly | 📅 2022-12-03
* [Blargg's test roms](http://gbdev.gg8.se/files/roms/blargg-gb-tests/)
* [Gekkio's test roms](https://gekkio.fi/files/mooneye-gb/latest/)
* [GB Accuracy Tests](http://tasvideos.org/EmulatorResources/GBAccuracyTests.html)

## Software Development

The [Choosing tools for Game Boy development](https://gbdev.io/guides/tools.html) essay provides an overview of the available development tools for Game Boy.

### Assemblers

* [RGBDS](https://github.com/gbdev/rgbds) ⭐ 1,564 | 🐛 60 | 🌐 C++ | 📅 2026-02-07 - Assembler and linker package. [Documentation](https://rgbds.gbdev.io).
* [wla-dx](https://github.com/vhelin/wla-dx) ⭐ 588 | 🐛 49 | 🌐 C | 📅 2026-02-18 - Yet Another GB-Z80/Z80/... Multi Platform Cross Assembler Package. [Documentation](http://www.villehelin.com/wla.txt).
* [ASMotor](https://github.com/csoren/asmotor) ⭐ 88 | 🐛 2 | 🌐 C | 📅 2026-01-21 - Assembler engine and development system targeting Game Boy, among other CPUs. Written by the original RGBDS author. [Documentation](https://github.com/asmotor/asmotor/tree/develop#further-reading) ⭐ 88 | 🐛 2 | 🌐 C | 📅 2026-01-21.

### Compilers

* [GBDK](https://github.com/gbdk-2020/gbdk-2020/) ⭐ 2,152 | 🐛 9 | 🌐 C | 📅 2026-02-13 - Maintained and modernized GBDK (Game Boy Development Kit) powered by an updated version of the SDCC toolchain. Provides a C compiler, assembler, linker and a set of libraries.
  * [API docs: Getting Started](https://gbdk-2020.github.io/gbdk-2020/docs/api/docs_getting_started.html)
  * [Examples](https://github.com/mrombout/gbdk_playground) ⭐ 202 | 🐛 1 | 🌐 C | 📅 2025-09-30
  * [Documentation, links and tools](https://gbdk-2020.github.io/gbdk-2020/docs/api/docs_links_and_tools.html)
* [Turbo Rascal Syntax Error](https://lemonspawn.com/turbo-rascal-syntax-error-expected-but-begin/) - Complete suite (IDE, compiler, programming language, resource editor) intended for developing games/demos for 8 / 16-bit line of computers, including the Game Boy and Game Boy Color.

#### Experimental/Proof of Concepts

* [Wiz](https://github.com/wiz-lang/wiz) ⭐ 427 | 🐛 75 | 🌐 C++ | 📅 2025-04-10 - A high-level assembly language for writing homebrew on retro console platforms (Game Boy, NES, Atari 2600, and more).
* [Rust-GB](https://github.com/zlfn/rust-gb) ⭐ 249 | 🐛 3 | 🌐 Rust | 📅 2025-08-06 - A compiler and library that enable the development of GB ROMs using Rust.
* [gbforth](https://github.com/ams-hackers/gbforth) ⭐ 146 | 🐛 75 | 🌐 Forth | 📅 2025-10-09 - A Forth-based Game Boy development kit.
* [gbasm](https://github.com/BonsaiDen/gbasm) ⭐ 132 | 🐛 1 | 🌐 JavaScript | 📅 2018-05-27 - A JavaScript based compiler for Game Boy z80 assembly code.
* [Assembler](https://github.com/ulrikdamm/Assembler) ⭐ 119 | 🐛 0 | 🌐 Swift | 📅 2021-10-21 - Assembler written in Swift.
* [llvm-gbz80](https://github.com/Bevinsky/llvm-gbz80) ⭐ 37 | 🐛 2 | 🌐 LLVM | 📅 2018-10-20 / [clang-gbz80](https://github.com/Bevinsky/clang-gbz80) ⭐ 24 | 🐛 0 | 🌐 C++ | 📅 2018-09-15 - Clang/LLVM port to the GBZ80 CPU (similar to the deprecated [euclio/llvm-gbz80](https://github.com/euclio/llvm-gbz80) ⚠️ Archived).
* [gbdk-go](https://github.com/pokemium/gbdk-go) ⚠️ Archived - A compiler translates Go programs to C code. The output C code is built into GB ROM by GBDK.
* [RGBDS-Live](https://gbdev.io/rgbds-live) - In-browser coding environment to try out RGBDS.
* [gbasm-rs](https://gitlab.com/BonsaiDen/gbasm-rs) - An opinionated Rust based compiler for Game Boy z80 assembly code.
* [tniASM](http://www.tni.nl/products/tniasm.html) - Macro Assembler.

### Emulators

* [mGBA](https://github.com/mgba-emu/mgba) ⭐ 6,795 | 🐛 811 | 🌐 C | 📅 2026-02-15 - Modern cross platform GBA emulator which also runs GB/GBC games.

* [SameBoy](https://github.com/LIJI32/SameBoy) ⭐ 2,012 | 🐛 152 | 🌐 C | 📅 2026-02-15 - Accurate emulator with a wide range of powerful debugging features.

* [MetroBoy](https://github.com/aappleby/MetroBoy) ⭐ 1,156 | 🐛 4 | 🌐 C++ | 📅 2025-02-23 - A playable, circuit-level simulation of an entire Game Boy.

* [Mooneye GB](https://github.com/Gekkio/mooneye-gb) ⭐ 958 | 🐛 44 | 🌐 Rust | 📅 2023-03-16 - Research project and emulator in Rust.

* [Binjgb](https://github.com/binji/binjgb) ⭐ 595 | 🐛 10 | 🌐 C | 📅 2026-01-05 - 5Kloc emulator that passes most of the tests. \*Rewind- feature. Runs in the browser using WebAssembly.

* [gbe-plus](https://github.com/shonumi/gbe-plus) ⭐ 572 | 🐛 76 | 🌐 C++ | 📅 2026-01-08 - A recently rewritten emulator that has a large effort in preserving the functions of obscure accessories (such as IR link, Mobile Network GB, Barcode Boy, GB Printer, local and online GB Serial Link Cable, ... )

* [Gambatte](https://github.com/gb-archive/gambatte) ⭐ 7 | 🐛 0 | 🌐 Assembly | 📅 2021-07-06 - Cross-platform and accurate emulator.

* [BGB](https://bgb.bircd.org/) - Powerful emulator and debugger. Provides an accurate hardware emulation.

* [Emulicious](https://emulicious.net/) - Provides accurate emulation and includes powerful tools such as a profiler and source-level debugging for ASM and C via a [VS Code debug adapter](https://marketplace.visualstudio.com/items?itemName=emulicious.emulicious-debugger).

[Complete list of open source emulators](origin/EMULATORS.md)

### Tools

#### Engines

* [ZGB](https://github.com/Zal0/ZGB) ⭐ 773 | 🐛 10 | 🌐 C++ | 📅 2024-08-01 - A little engine for creating games for the original Game Boy (expands gbdk, more info [here](http://zalods.blogspot.com/2017/01/zgb-little-engine-for-game-boy.html)).
* [Retr0 GB](https://bitbucket.org/HellSuffering/retr0-gb/) - An engine for creating games (expands GBDK).

#### Development tools

* [mgbdis](https://github.com/mattcurrie/mgbdis) ⭐ 299 | 🐛 11 | 🌐 Assembly | 📅 2025-12-17 - Game Boy ROM disassembler with RGBDS compatible output.
* [awake](https://github.com/devdri/awake) ⭐ 76 | 🐛 2 | 🌐 Python | 📅 2014-01-30 - Game Boy decompiler.
* [romusage](https://github.com/bbbbbr/romusage) ⭐ 55 | 🐛 2 | 🌐 JavaScript | 📅 2025-11-01 - Command line tool for estimating usage (free space) of Game Boy ROMs from a .map, .noi or ihx file. Works with GBDK-2020 and RGBDS.
* [evunit](https://github.com/eievui5/evunit) ⭐ 21 | 🐛 4 | 🌐 Rust | 📅 2025-02-28 - A unit testing program for assembly code.
* [evscript](https://github.com/eievui5/evscript) ⭐ 16 | 🐛 12 | 🌐 Rust | 📅 2024-03-11 - A scripting language for the Game Boy, useful for enemy AI, dialogue, animations, and coroutines.
* [gbdk-lib-extension](https://github.com/ProGM/gbdk-lib-extension) ⭐ 13 | 🐛 0 | 🌐 Java | 📅 2013-08-07 - A small set of sources and tools for the Game Boy Development Kit by Michael Hope.
* [Game Boy Text Tools](https://github.com/raphaklaus/gameboy-text-tools) ⭐ 11 | 🐛 1 | 🌐 JavaScript | 📅 2017-12-02 - Set of tools for text manipulation and translation of Game Boy ROMs written in Node.js.
* [opcode\_count](https://github.com/rondnelson99/opcode_count) ⭐ 2 | 🐛 0 | 🌐 Python | 📅 2023-06-01 - Generates statistics on which CPU instructions are run the most often using Python and Emulicious
* [GBExtended](https://www.tensi.eu/thomas/programming/utilities/gbx_library/gbx_library.html) - C library extending gbdk.
* [ROM Header Utility](http://catskull.net/GB-Logo-Generator/) - An online tool to inspect and modify a ROM's header data, including the logo.

#### Graphics utilities

* [Tilemap Studio](https://github.com/Rangi42/tilemap-studio) ⭐ 488 | 🐛 24 | 🌐 C++ | 📅 2025-09-12 - A tilemap editor for Game Boy, Color, Advance, and SNES projects. Written in C++ with FLTK.
* [Superfamiconv](https://github.com/Optiroc/SuperFamiconv) ⭐ 180 | 🐛 22 | 🌐 C++ | 📅 2025-02-19 - Flexible and composable tile graphics converter supporting Super Nintendo, Game Boy, Game Boy Color, Game Boy Advance, Mega Drive and PC Engine formats.
* [Game Boy Tile Data Generator](https://github.com/chrisantonellis/gbtdg) ⭐ 92 | 🐛 4 | 🌐 JavaScript | 📅 2023-12-31 - HTML5 / JS web application that will convert bitmap images to hexadecimal data appropriate for use in tile based graphical applications, specifically GB.
* [Tilemap GB](https://github.com/bbbbbr/gimp-tilemap-gb) ⭐ 66 | 🐛 1 | 🌐 C | 📅 2024-04-16 - GIMP image editor plug-in for importing & exporting GBMB and GBTD tilemaps and tilesets (as bitmap images or .GBM/.GBR files).
* [vtGBte](https://github.com/paul-arutyunov/vtGBte) ⭐ 36 | 🐛 4 | 🌐 C | 📅 2021-05-24 - A minimalistic ncurses tile editor.
* [bmp2cgb](https://github.com/gitendo/bmp2cgb) ⚠️ Archived - Graphics converter for Game Boy Color development providing real time palette adjustments.
* [Tilemap Helper](https://github.com/bbbbbr/gimp-tilemap-helper) ⭐ 28 | 🐛 1 | 🌐 C | 📅 2020-11-11 - GIMP image editor plug-in for optimizing tile maps and tile sets.
* [tpp1](https://github.com/TwitchPlaysPokemon/tpp1) ⭐ 24 | 🐛 2 | 🌐 Assembly | 📅 2022-10-02 - Definition and specification of a custom GB/GBC memory/hardware mapper, as a functional superset of MBC.
* [png2gb](https://github.com/LuckyLights/png2gb) ⭐ 21 | 🐛 0 | 🌐 C | 📅 2015-08-02 - CLI tool to convert image file to game boy .c array.
* [GBTiles](https://github.com/bashaus/gbtiles) ⭐ 16 | 🐛 0 | 🌐 Ruby | 📅 2016-04-27 - Converts .GBR files created with Harry Mulder's Tile Designer (GBTD) and .GBM files created with Harry Mulder's Map Builder (GBMB) to different formats for use with the Game Boy and GBDK.
* [libstdgb](https://github.com/delwink/libstdgb) ⭐ 12 | 🐛 0 | 🌐 Python | 📅 2021-08-08 - A C library of useful Game Boy operations (SDCC).
* [GB-convert](https://github.com/gb-archive/gb-convert) ⭐ 0 | 🐛 0 | 🌐 C | 📅 2018-05-21 - Game Boy tile conversion and map editor tool (converts to assembly).
* [Harry Mulder's GB Development](http://www.devrs.com/gb/hmgd/intro.html) - Some sources and home of Game Boy Tile Designer (GBTD) and Game Boy Map Builder (GBMB) tools.
* [brewtool](http://make.vg/brewtool/) - A collection of primitive editor/converter tools for making assets used with homebrew ROM development.

#### Hardware and ROM utilities

* [Game Boy LCD sniffing](https://github.com/svendahlstrand/game-boy-lcd-sniffing) ⭐ 180 | 🐛 0 | 🌐 C | 📅 2017-08-11 - Sniff your Game Boy's LCD using a logic analyzer.
* [gbcamextract](https://github.com/jkbenaim/gbcamextract) ⭐ 52 | 🐛 0 | 🌐 C | 📅 2022-05-08 - Extracts photos from Game Boy Camera saves.
* [cart-dumper](https://github.com/Palmr/cart-dumper) ⭐ 44 | 🐛 0 | 🌐 Assembly | 📅 2018-07-09 - Game Boy Cartridge Dumper ROM.
* [swapdump](https://github.com/sanqui/swapdump) ⭐ 3 | 🐛 0 | 🌐 Assembly | 📅 2016-07-23 - Diagnostic utility for Game Boy flashcarts.
* [Gameboy-LinkUp](https://github.com/JustinLloyd/Gameboy-LinkUp) ⚠️ Archived - Game Boy LinkUp serial cable networking project.

#### Music drivers and trackers

* [hUGETracker](https://github.com/SuperDisk/hUGETracker) ⭐ 336 | 🐛 57 | 🌐 Pascal | 📅 2025-09-07 - A music tracker based on OpenMPT, focused on ease of use, compact output, and embeddability in homebrew games.
* [GBT PLAYER](https://github.com/AntonioND/gbt-player) ⭐ 299 | 🐛 0 | 🌐 C | 📅 2026-01-25 - A music player library and converter kit.
* [mmlgb](https://github.com/SimonLarsen/mmlgb) ⭐ 43 | 🐛 6 | 🌐 C | 📅 2024-04-12 - A MML parser and GBDK sound driver for the Nintendo Game Boy.
* [CBT-FX](https://github.com/datguywitha3ds/CBT-FX) ⚠️ Archived - A GBDK-2020 sound effect driver compatible with FX-Hammer sound effects.
* [XPMCK](https://github.com/bazzinotti/XPMCK) ⭐ 27 | 🐛 23 | 🌐 Assembly | 📅 2016-04-15 - An MML based music compiler with support for Game Boy & Game Boy Color.
* [GBSoundSystem](https://github.com/gbdev/GBSoundSystem) ⭐ 18 | 🐛 0 | 🌐 Assembly | 📅 2023-05-09 - A modernized audio driver for GameBoy Tracker (aka the Paragon 5 music player).
* [DevSoundX](https://github.com/DevEd2/DevSoundX) ⚠️ Archived - Sound driver embeddable in homebrews which supports pulse width manipulation, arpeggios, and multiple waveforms.
* [Carillon Player](http://gbdev.gg8.se/files/musictools/Aleksi%20Eeben/Carillon%20Editor.zip) - Music Engine.

## Programming

Guides, tutorials and tools to develop software for Game Boy using the development toolchains described in the [Software Development](#software-development) chapter.

### ASM

* [Game Boy Assembly Programming for the Modern Game Developer](https://github.com/ahrnbom/gbapfomgd) ⭐ 167 | 🐛 0 | 🌐 TeX | 📅 2023-02-25 - An e-book about making Game Boy games in Assembly.
* [hardware.inc](https://github.com/tobiasvl/hardware.inc) ⭐ 150 | 🐛 8 | 🌐 Assembly | 📅 2026-01-01 - Standard include file containing Game Boy hardware definitions for use in RGBDS projects.
* [assemblydigest](https://github.com/assemblydigest/gameboy) ⭐ 78 | 🐛 3 | 🌐 Shell | 📅 2017-10-26 - Exploring Game Boy programming techniques:
  * [Making an Empty Game Boy ROM (in Wiz)](http://assemblydigest.tumblr.com/post/77203696711/tutorial-making-an-empty-game-boy-rom-in-wiz)
  * [Making Art for the Game Boy](http://assemblydigest.tumblr.com/post/77404621743/tutorial-making-art-for-the-game-boy)
* [DMGreport](https://github.com/lancekindle/DMGreport) ⭐ 62 | 🐛 1 | 🌐 Assembly | 📅 2024-09-01 - Game programming tutorials in assembly.
* **[gb asm tutorial](https://gbdev.io/gb-asm-tutorial)** - Step by step tutorial, building several ROMs to accompany its explanations.
* [Assembly tutorial by David Pello](https://gb-archive.github.io/salvage/tutorial_de_ensamblador/tutorial_de_ensamblador_la_decadence.html) - Good document to learn to produce working asm code for gb. Brief explanations of many important topics. Many examples with commented source code.
* [Beginner's Guide to Reverse Engineering GB](http://web.archive.org/web/20150511145100/http://www.bennvenn.com/Beginners_Guide_To_Reverse_Engineering.htm) - Some starting tips on disassembling and reverse engineering.
* [FlappyBoy: Making a simple Game Boy Game](http://voidptr.io/blog/2017/01/21/GameBoy.html)
* [Super Game Boy development](https://imanoleasgames.blogspot.no/2016/12/games-aside-1-super-game-boy.html) - Step by step tutorial to implement Super Game Boy features (frame and palettes).
* [GameBoy programming tutorial: Hello World!](https://peterwynroberts.wordpress.com/2014/05/11/gameboy-programming-tutorial-hello-world/) - Step by step tutorial.
* [OAM DMA tutorial](https://gbdev.gg8.se/wiki/articles/OAM_DMA_tutorial) - Example of how to use OAM DMA in assembly.

#### Sources

Fragments of code, effects, proof of concepts and generally non complete games.

* [EmmaEwert's experiments](https://github.com/EmmaEwert/gameboy) ⭐ 25 | 🐛 0 | 🌐 Makefile | 📅 2017-03-02 - A collection of prototype programs, mostly just toying around. Among others, a daylight effect, transparency and a weather effect.
* [DeadCScroll](https://github.com/gb-archive/DeadCScroll) ⭐ 25 | 🐛 0 | 📅 2021-04-17 - A detailed tutorial on how to make the screen wobble, among other "raster effects"
* [dev'rs ASM section](https://web.archive.org/web/20250329180046/http://www.devrs.com/gb/asmcode.php) - A lot of working demos and sources.

#### Timings

* [Nitty Gritty Gameboy Cycle Timing](http://blog.kevtris.org/blogfiles/Nitty%20Gritty%20Gameboy%20VRAM%20Timing.txt)
* [Mode3 Sprite Timing](https://old.reddit.com/r/EmuDev/comments/59pawp/gb_mode3_sprite_timing/)
* [GameBoy Color DMA-Transfers v0.0.1](http://gameboy.mongenel.com/dmg/gbc_dma_transfers.txt)
* [STAT interrupt timings](http://gameboy.mongenel.com/dmg/istat98.txt)
* [Video Timing](https://github.com/jdeblese/gbcpu/wiki/Video-Timing) ⭐ 9 | 🐛 1 | 🌐 VHDL | 📅 2013-04-25

#### Boilerplates and libraries

* [GingerBread](https://github.com/ahrnbom/gingerbread) ⭐ 138 | 🐛 1 | 🌐 Assembly | 📅 2021-01-19 - A software library for making your own Game Boy games. It is made to be used alongside the book [Game Boy Assembly Programming for the Modern Game Developer](https://github.com/ahrnbom/gbapfomgd) ⭐ 167 | 🐛 0 | 🌐 TeX | 📅 2023-02-25 which also doubles as documentation.
* [gb-boilerplate](https://github.com/ISSOtm/gb-boilerplate) ⚠️ Archived - A template for starting Game Boy projects, providing a Makefile for infrastructure.
* [gb-starter-kit](https://github.com/ISSOtm/gb-starter-kit) ⚠️ Archived - An expansion on the above, including base library code as well to get started faster.
* [gb-vwf](https://github.com/ISSOtm/gb-vwf) ⚠️ Archived - Library to print variable-width text, comes with a demo.
* [rgbds-template](https://github.com/nezticle/rgbds-template) ⭐ 43 | 🐛 0 | 🌐 Assembly | 📅 2015-01-31 - Basic hello-world example for Game Boy using RGBDS.
* [bootstrap.gb](https://github.com/yenatch/bootstrap.gb) ⭐ 32 | 🐛 4 | 🌐 Assembly | 📅 2024-05-31 - An example Game Boy project.
* [Gameboy Boilerplate](https://github.com/junebug12851/GameboyBoilerplateProj) ⭐ 31 | 🐛 0 | 🌐 Assembly | 📅 2020-07-15 - Boilerplate project to move quicker into the actual assembly code for your game.
* [gb-template](https://github.com/gb-archive/gb-template) ⭐ 4 | 🐛 0 | 🌐 Assembly | 📅 2018-05-21 - A template with basic functions such as joypad input, DMA transfers, and map/tile data loading.
* [Game Boy Assembly Language Primer](http://www.devrs.com/gb/files/galp.zip) - Simple template code with memory defines, copy routines and IBM font tilemap.

#### Syntax highlighting packages

* [rgbds-vscode](https://github.com/DonaldHays/rgbds-vscode) ⭐ 76 | 🐛 4 | 🌐 TypeScript | 📅 2025-11-06 - Visual Studio Code language extension for RGBDS GBZ80 Assembly.
* [Z80 Assembly support for Visual Studio Code](https://github.com/Imanolea/z80asm-vscode) ⭐ 36 | 🐛 0 | 📅 2025-08-16
* [Vim syntax file for RGBDS](https://github.com/Leandros/dotfiles/blob/master/.vim/syntax/rgbds.vim) ⭐ 11 | 🐛 3 | 🌐 Lua | 📅 2026-02-04 - Another Vim syntax highlighting file for RGBDS assembly.
* [gbz80-highlight](https://github.com/ISSOtm/gbz80-highlight) ⚠️ Archived - Notepad+- and gedit syntax highlighting files for RGBDS assembly.
* [rgbds-mode](https://github.com/japanoise/rgbds-mode) ⭐ 5 | 🐛 0 | 🌐 Emacs Lisp | 📅 2018-12-25 - Emacs major mode for RGBDS assembly.
* [Vim syntax file for the Game Boy assembler RGBASM](http://www.vim.org/scripts/script.php?script_id=819) - Vim syntax highlighting for RGBDS assembly.
* [sublime-rgbds](https://packagecontrol.io/packages/RGBDS) - A Sublime Text 3 package for RGBDS, including syntax highlighting and some completion snippets.

### C

* [Simplified GBDK examples](https://github.com/mrombout/gbdk_playground) ⭐ 202 | 🐛 1 | 🌐 C | 📅 2025-09-30
* [Grooves Game Boy Programming](https://github.com/gbdk-salvage/grooves-game-boy-programming) ⭐ 89 | 🐛 2 | 🌐 C | 📅 2023-03-30 - A complete set of lessons about implementing various game mechanics in a Game Boy game.
* [8-Bit Wonderland](https://github.com/gb-archive/salvage/blob/master/misc/8bit_wonderland.pdf) ⭐ 38 | 🐛 2 | 🌐 HTML | 📅 2025-04-22 - Well-written introductory document about how the Game Boy works and how to start developing working code for it.
* [How to Write a Simple Side Scrolling Game](http://pastebin.com/F3tHLj68) - Old (but still relevant) tutorial.
* [Just another simple tutorial](http://web.archive.org/web/20230327070526/http://pastebin.com/gzT47MPJ)
* [GBDK Tutorial](https://refreshgames.co.uk/2016/04/18/gameboy-tutorial-rom/) - Fairly minimal game demo for getting started with GBDK.
* [GBDK Sprite](http://gbdev.gg8.se/wiki/articles/GBDK_Sprite_Tutorial) - Presents a workflow for getting multiple sprites to display and animate.
* [GBDK Color](http://gbdev.gg8.se/wiki/articles/GBDK_Color_Tutorial) - Extends your knowledge of basic spriting on the Game Boy by adding colors to sprites, backgrounds and the window layer.
* [GBDK Joypad](http://gbdev.gg8.se/wiki/articles/GBDK_Joypad_Tutorial) - Details the use of the joypad with GBDK.
* [Game Boy home of Flavor](https://web.archive.org/web/20210427064949/www.personal.triticom.com/~erm/GameBoy/) - Some full games and sources.
* [GBDK Configuring and Programming Tutorial](https://videlais.com/2016/07/03/programming-game-boy-games-using-gbdk-part-1-configuring-programming-and-compiling/) - Configuring GBDK, Using Tiles, Colliding Sprites, GBTD, GBMB, Memory Management and ROM Banking.
* [GBDK Programming Video Tutorials](https://www.youtube.com/playlist?list=PLeEj4c2zF7PaFv5MPYhNAkBGrkx4iPGJo) - A series of video tutorials introducing beginners to programming with GBDK.
* [Larold's Retro Gameyard](https://laroldsretrogameyard.com/category/tutorials/gb/) - A collection of detailed GBDK-2020 based tutorials.

## Homebrews

Complete and open source games.

* [Homebrew Hub](https://hh.gbdev.io) - A community-led attempt to collect, archive and preserve every unlicensed and homebrew game released for Game Boy. Entries are playable online.

### ASM

* [µCity](https://github.com/AntonioND/ucity) ⭐ 467 | 🐛 0 | 🌐 Assembly | 📅 2026-01-25
* [Tuff](https://github.com/BonsaiDen/Tuff.gb) ⭐ 312 | 🐛 5 | 🌐 Assembly | 📅 2018-10-27
* [Pokered-gbc](https://github.com/dannye/pokered-gbc) ⭐ 171 | 🐛 2 | 🌐 Assembly | 📅 2026-01-25 - Pokémon Red remade with full GBC support.
* [GB303](https://github.com/furrtek/GB303) ⚠️ Archived - GB303 wavetable-based TB-303 style synthesizer for the Nintendo Game Boy.
* [2048-gb](https://github.com/Sanqui/2048-gb) ⭐ 115 | 🐛 2 | 🌐 Assembly | 📅 2015-02-11
* [Flappy-boy-asm](https://github.com/bitnenfer/flappy-boy-asm) ⭐ 94 | 🐛 2 | 🌐 Assembly | 📅 2020-08-25
* [Aevilia](https://github.com/ISSOtm/Aevilia-GB) ⚠️ Archived
* [Libbet and the Magic Floor](https://github.com/pinobatch/libbet) ⭐ 39 | 🐛 5 | 🌐 Python | 📅 2025-09-02
* [GBSlides](https://github.com/Kartones/gameboy) ⭐ 32 | 🐛 0 | 🌐 Assembly | 📅 2024-09-19 - A simple Game Boy Powerpoint-like slides viewer.
* [Geometrix](https://github.com/AntonioND/geometrix) ⚠️ Archived
* [Snake-gb](https://github.com/DonaldHays/snake-gb) ⭐ 20 | 🐛 0 | 🌐 Assembly | 📅 2023-04-03
* [waveform-gb](https://github.com/dannye/waveform-gb) ⭐ 20 | 🐛 0 | 🌐 Assembly | 📅 2021-02-11 - Program visualizing the wave form used by the wave channel. The wave form can be edited freely and playback of the wave is updated immediately.
* [Carazu](https://github.com/mholtkamp/carazu) ⭐ 18 | 🐛 1 | 🌐 Assembly | 📅 2019-09-11
* [Adjustris](https://github.com/tbsp/Adjustris) ⭐ 15 | 🐛 4 | 🌐 Assembly | 📅 2022-01-19
* [Lazerpong](https://github.com/huderlem/lazerpong) ⭐ 14 | 🐛 0 | 🌐 Assembly | 📅 2015-05-02
* [desgb](https://github.com/sanqui/desgb) ⭐ 14 | 🐛 0 | 🌐 Assembly | 📅 2018-03-29 - DES encryption.
* [minesweepGB](https://github.com/lancekindle/minesweepGB) ⭐ 13 | 🐛 0 | 🌐 Assembly | 📅 2017-12-14
* [ToyToy](https://github.com/tslanina/Retro-GameBoyColor-ToyToy) ⭐ 10 | 🐛 0 | 🌐 Assembly | 📅 2018-01-21
* [Sushi](https://github.com/JustSid/Sushi) ⭐ 5 | 🐛 0 | 🌐 Assembly | 📅 2017-01-22
* [kupman](https://github.com/dubvulture/gbdev) ⭐ 5 | 🐛 0 | 🌐 Assembly | 📅 2017-11-05 and some other projects.
* [superhappyfunbubbletime](https://github.com/l0k1/superhappyfunbubbletime) ⭐ 5 | 🐛 0 | 🌐 Assembly | 📅 2020-02-19
* [StefaN](https://github.com/tslanina/Retro-GameBoyColor-StefaN) ⭐ 4 | 🐛 0 | 🌐 Assembly | 📅 2017-04-19 - Fourway Breakout clone.
* [Galaxia](https://github.com/tslanina/Retro-GameBoyColor-Galaxia) ⭐ 4 | 🐛 0 | 🌐 Assembly | 📅 2018-02-13
* [PlantBoy](https://github.com/gb-archive/plantboy) ⭐ 1 | 🐛 0 | 🌐 Assembly | 📅 2018-05-21
* [exeman](https://github.com/gb-archive/exeman) ⭐ 0 | 🐛 0 | 🌐 Assembly | 📅 2018-05-21
* [Snake](https://bitbucket.org/Sanqui/snake/src/?at=master)
* [vectroid.gb](https://gitlab.com/BonsaiDen/vectroid.gb) - Developed with gbasm.
* [Death Planet](https://makrill.itch.io/death-planet)
* [Quartet](https://makrill.itch.io/quartet) - Puzzle game for the Game Boy (Color) and Super Game Boy.
* [Dangan](https://snorpung.itch.io/dangan-gb)

### C

* [Powa!](https://aiguanachein.itch.io/powa) - Side scrolling platformer for the Game Boy (Color)  ([ZGB engine](https://github.com/Zal0/ZGB/) ⭐ 773 | 🐛 10 | 🌐 C++ | 📅 2024-08-01).
* [Cavern](https://thegreatgallus.itch.io/cavern-mvm-9) - ([ZGB engine](https://github.com/Zal0/ZGB/) ⭐ 773 | 🐛 10 | 🌐 C++ | 📅 2024-08-01).
* [Mona and the Witch's Hat Deluxe](https://ctneptune.itch.io/mona-and-the-witchs-hat-dx) - ([ZGB engine](https://github.com/Zal0/ZGB/) ⭐ 773 | 🐛 10 | 🌐 C++ | 📅 2024-08-01).
* [Tobu Tobu Girl Deluxe](https://github.com/SimonLarsen/tobutobugirl-dx) ⭐ 86 | 🐛 1 | 🌐 C | 📅 2023-01-29 - An arcade platformer for the Game Boy (Color).
* [Dino's Offline Adventure](https://github.com/gingemonster/DinosOfflineAdventure) ⭐ 59 | 🐛 0 | 🌐 JavaScript | 📅 2020-06-14 - A clone of the Google Chrome offline game.
* [Evoland.gb](https://github.com/flozz/evoland.gb) ⭐ 43 | 🐛 0 | 🌐 C | 📅 2019-04-21 - A port of the first level of Evoland.
* [gb-mines](https://github.com/andreasjhkarlsson/gb-mines) ⭐ 36 | 🐛 2 | 🌐 C | 📅 2018-05-06
* [Petris](https://github.com/bbbbbr/Petris) ⭐ 34 | 🐛 0 | 🌐 C | 📅 2024-04-18 - A puzzle game of shapely pets for the Game Boy Color ([itch.io](https://bbbbbr.itch.io/petris)).
* [GBsnake](https://github.com/brovador/GBsnake) ⭐ 32 | 🐛 0 | 🌐 C++ | 📅 2017-04-23
* [Super Princess' 2092 Exodus](https://github.com/Zal0/gbjam2016) ⭐ 30 | 🐛 0 | 🌐 C | 📅 2022-11-02 - ([ZGB engine](https://github.com/Zal0/ZGB/) ⭐ 773 | 🐛 10 | 🌐 C++ | 📅 2024-08-01).
* [Doctor How](https://github.com/elfgames/doctorhow) ⭐ 28 | 🐛 0 | 🌐 Assembly | 📅 2016-04-10
* [Bubble Factory](https://github.com/DonaldHays/bubblefactory) ⭐ 27 | 🐛 3 | 🌐 C | 📅 2023-04-03 - \*Vanilla- SDCC (no gbdk).
* [dino-gb](https://github.com/rnegron/dino-gb) ⭐ 26 | 🐛 1 | 🌐 C | 📅 2024-08-10 - Another clone of the Chrome game.
* [Infinity](https://github.com/gb-archive/infinity-gbc) ⭐ 26 | 🐛 0 | 🌐 C | 📅 2021-04-14 - RPG developed by Affinix Software primarily between the years 1999 and 2001. The game never found a publisher and was eventually canceled. Got recently released with the full source, development tools and workflows.
* [FlappyBoy](https://github.com/bitnenfer/FlappyBoy) ⭐ 20 | 🐛 0 | 🌐 C | 📅 2015-03-26
* [flappybird-gameboy](https://github.com/pashutk/flappybird-gameboy) ⭐ 15 | 🐛 0 | 🌐 C | 📅 2017-05-18
* [GB raycaster, Vision-8](https://github.com/haroldo-ok/really-old-stuff/tree/master/gameboy) ⭐ 15 | 🐛 0 | 🌐 C | 📅 2017-11-02 - and some other projects.
* [Guns & Riders](https://github.com/kanfor/gunsridersgameboy) ⭐ 14 | 🐛 1 | 🌐 C | 📅 2016-05-16
* [Quadratino](https://github.com/avivace/quadratino) ⭐ 12 | 🐛 0 | 🌐 C | 📅 2019-07-09
* [Squishy the Turtle](https://github.com/cppchriscpp/SquishyTheTurtle) ⭐ 8 | 🐛 0 | 🌐 C | 📅 2024-01-26
* [PostBot](https://github.com/MasterIV/PostBot) ⭐ 7 | 🐛 0 | 🌐 C | 📅 2020-10-02
* [red hot princess carnage](https://github.com/Imanolea/bitbitjam3_red_hot_princess_carnage) ⭐ 6 | 🐛 0 | 🌐 C | 📅 2016-07-04
* [fbgb](https://github.com/gb-archive/fbgb) ⭐ 3 | 🐛 0 | 🌐 C | 📅 2018-01-09
* [GBC Atari Boxing](https://github.com/rubfi/gbc-atari-boxing) ⭐ 3 | 🐛 0 | 🌐 C | 📅 2017-10-11 - Atari 2600 Boxing clone for the Game Boy (Color).
* [Novascape](https://web.archive.org/web/20171002042716/http://ludumdare.com/compo/ludum-dare-34/?action=preview\&uid=6823)
* [oranges](http://www.atari2600land.com/gameboy/oranges.html)
* [loderunner](https://www.tensi.eu/thomas/programming/games/loderunner/loderunner.html)
* [Hives](https://refreshgames.co.uk/2017/04/24/ludum-dare-38-entry-hives/)
* [Burly Bear vs. The Mean Foxes](http://sebastianmihai.com/gameboy-burly-bear.html) ([GBC](http://sebastianmihai.com/gameboy-color-burly-bear.html) port)
* [Black Castle](https://gbdev.gg8.se/forums/viewtopic.php?id=743) - Side scrolling platformer for the Game Boy ([itch.io](https://user0x7f.itch.io/black-castle)).
* [Genesis](https://gbdev.gg8.se/forums/viewtopic.php?id=674) - Shmup for the Game Boy ([itch.io](https://user0x7f.itch.io/genesis)).
* [Indestructo Tank!](https://antonylavelle.itch.io/indestructotank-gb)
* [Super JetPak DX](https://asobitech.itch.io/super-jetpak-dx)
* [The Bouncing Ball](https://gamejolt.com/games/the-bouncing-ball-gb/86699)
* [DMG Deals Damage](https://drludos.itch.io/dmg-deals-damage)

### GB Studio

* [Soul Void](https://kadabura.itch.io/soul-void) - Interactive horror fiction.
* [Deadeus](https://izma.itch.io/deadeus)
* [SUPER IMPOSTOR BROS.](https://lumpytouch.itch.io/super-impostor-bros)

### Demos

* [GBVideoPlayer2](https://github.com/LIJI32/GBVideoPlayer2) ⭐ 125 | 🐛 7 | 🌐 C | 📅 2019-11-02 - The second iteration of the above demo, which increases the resolution, adds *stereo- PCM audio, and introduces video compression*.
* [GBVideoPlayer](https://github.com/LIJI32/GBVideoPlayer) ⭐ 100 | 🐛 4 | 🌐 Python | 📅 2018-02-26 - A technical demo demonstrating how the Game Boy LCD controller can be hacked to make a Game Boy Color play a full motion video in color, together with music.
* [CUTE DEMO](https://github.com/mills32/CUTE_DEMO) ⭐ 39 | 🐛 1 | 🌐 C | 📅 2020-06-17
* [matrix-rain-gb](https://github.com/wtjones/matrix-rain-gb) ⭐ 32 | 🐛 0 | 🌐 Assembly | 📅 2024-07-30 - A Matrix digital rain effect in assembler.
* [`10 PRINT` Game Boy](https://github.com/svendahlstrand/10-print-game-boy) ⭐ 30 | 🐛 0 | 🌐 Assembly | 📅 2018-07-30
* [Back to Color](https://github.com/AntonioND/back-to-color) ⚠️ Archived
* [Roboto Demo](https://github.com/naavis/roboto-demo) ⭐ 27 | 🐛 0 | 🌐 Assembly | 📅 2018-03-13
* [beach-gbc](https://github.com/vegard/beach-gbc) ⭐ 14 | 🐛 1 | 🌐 Python | 📅 2019-08-21

## Reverse Engineering

* [pokemontools](https://github.com/pret/pokemon-reverse-engineering-tools) ⚠️ Archived - a python module that provides various reverse engineering components for various Pokémon games.
* [Reverse Engineering the GameBoy Tetris](https://github.com/h3nnn4n/Reverse-Engineering-the-GameBoy-Tetris) ⭐ 27 | 🐛 0 | 🌐 Shell | 📅 2017-07-17
* [Reverse engineering Kirby's Dreamland 2](http://ecc-comp.blogspot.it/2016/03/reverse-engineering-kirbys-dreamland-2.html)
* [Reverse Engineering a Gameboy ROM with radare2](https://www.megabeets.net/reverse-engineering-a-gameboy-rom-with-radare2) - A walkthrough to reverse engineer a Game Boy ROM challenge using radare2.
* [Disassembling Link's Awakening](http://kemenaran.winosx.com/posts/category-disassembling-links-awakening/) - A series of blog posts about disassembling Link's Awakening DX.
* [DMA hijacking](https://gbdev.io/guides/dma_hijacking) - A simple technique that allows you to run custom code in most GB/SGB/CGB games, provided you have an ACE exploit.

### Game Disassemblies

* [Pokémon Red/Blue](https://github.com/pret/pokered) ⭐ 4,548 | 🐛 21 | 🌐 Assembly | 📅 2026-01-24
* [Pokémon Crystal](https://github.com/pret/pokecrystal) ⭐ 2,353 | 🐛 56 | 🌐 Assembly | 📅 2026-02-08
* [Link's Awakening DX](https://github.com/mojobojo/LADX-Disassembly) ⭐ 878 | 🐛 18 | 🌐 Assembly | 📅 2026-02-05
* [Pokémon Yellow](https://github.com/pret/pokeyellow) ⭐ 809 | 🐛 2 | 🌐 Assembly | 📅 2026-01-18
* [Pokémon Gold and Silver](https://github.com/pret/pokegold) ⭐ 644 | 🐛 6 | 🌐 Assembly | 📅 2026-02-08
* [pokegold-spaceworld](https://github.com/pret/pokegold-spaceworld) ⭐ 375 | 🐛 12 | 🌐 Assembly | 📅 2026-01-21 - Pokémon Gold and Silver 1997 Space World demo.
* [Pokémon TCG](https://github.com/pret/poketcg) ⭐ 304 | 🐛 4 | 🌐 Assembly | 📅 2026-02-15
* [Oracle of Ages](https://github.com/drenn1/ages-disasm) ⭐ 187 | 🐛 4 | 🌐 Assembly | 📅 2025-12-23
* [Pokémon Pinball](https://github.com/pret/pokepinball) ⭐ 185 | 🐛 3 | 🌐 Assembly | 📅 2025-11-14
* [Tetris](https://github.com/vinheim3/tetris-gb-disasm) ⭐ 29 | 🐛 1 | 🌐 Assembly | 📅 2023-01-19 - Complete Tetris disassembly.
* [Harvest Moon 3](https://github.com/sanqui/hm3) ⭐ 19 | 🐛 6 | 🌐 Assembly | 📅 2023-05-01
* [FX Hammer](https://github.com/DevEd2/FXHammer-Disasm) ⭐ 9 | 🐛 0 | 🌐 Assembly | 📅 2022-03-09
* [The Jungle Book](https://github.com/not-chciken/jungle-book-gb-disassembly) ⭐ 4 | 🐛 0 | 🌐 Assembly | 📅 2026-01-10
* [Final Fantasy Adventure](https://daid.github.io/FFA-Disassembly/)

## Game Boy Camera

### Retrieving images

Game Boy Printer emulation (e.g. to retrieve images from the camera):

* [Arduino Gameboy Printer Emulator](https://github.com/mofosyne/arduino-gameboy-printer-emulator) ⭐ 353 | 🐛 3 | 🌐 C++ | 📅 2024-06-15 - Emulate a gameboy printer via the gameboy link cable.
* [WiFi GBP Emulator](https://github.com/HerrZatacke/wifi-gbp-emulator) ⭐ 75 | 🐛 6 | 🌐 C++ | 📅 2025-05-31 - A GameBoy printer emulator which provides the received data over a WiFi connection.
* [ESP8266 Game Boy Printer](https://github.com/applefreak/esp8266-gameboy-printer) ⭐ 49 | 🐛 0 | 🌐 C++ | 📅 2020-10-12 -  A device that emulates the Gameboy Printer and lets you retrieve images using WiFi powered by an ESP8266.
* [Game Boy WiFi Printer - D1 Mini Shield](https://github.com/cristofercruz/gbp-esp-shield-pcb) ⭐ 24 | 🐛 0 | 📅 2021-08-31 - Game Boy Printer interface shield for D1 mini/mini Pro ESP8266 boards.
* [Game Boy Printer Sniffer](https://github.com/mofosyne/GameboyPrinterSniffer) ⭐ 9 | 🐛 0 | 🌐 C++ | 📅 2022-06-21 - Sniff packet communications between a Game Boy and the Printer.

### Changing the camera's behavior

Methods to improve and/or manipulate the camera's quality and behavior:

* [Game Boy Camera Canon EF Lens Mount](http://ekeler.com/game-boy-camera-canon-ef-mount)
* [Game Boy Camera to Canon Lens mount](https://www.thingiverse.com/thing:4337362) - based on the above.
* [game-boy-camera-frame-replacer](https://github.com/cristofercruz/game-boy-camera-frame-replacer) ⭐ 41 | 🐛 0 | 🌐 Python | 📅 2024-04-28 - Manipulate the ROM of a camera to include custom frames

### Post processing

* [Game Boy Printer Paper Simulation](https://github.com/mofosyne/GameboyPrinterPaperSimulation) ⭐ 83 | 🐛 0 | 🌐 C++ | 📅 2025-09-30 - Generate as-if-printed images of digital printed images.
* [Game Boy Printer Web](https://github.com/HerrZatacke/gb-printer-web) ⭐ 68 | 🐛 0 | 🌐 TypeScript | 📅 2026-02-15 - Gallery app for to the Game Boy camera: import pictures from exports or cartridge dumps and choose color palettes.

## Related projects

* [VerilogBoy](https://github.com/zephray/VerilogBoy/) ⭐ 514 | 🐛 5 | 🌐 Verilog | 📅 2022-12-10 - Game Boy compatible console Verilog RTL implementation.
* [ArduinoBoy](https://github.com/trash80/Arduinoboy) ⭐ 358 | 🐛 7 | 🌐 Max | 📅 2020-11-16 - Serial communication (MIDI) from an Arduino to the Game Boy for music applications such as LittleSoundDJ, Nanoloop, and mGB.
* [mGB](https://github.com/trash80/mGB) ⭐ 259 | 🐛 14 | 🌐 Assembly | 📅 2024-07-16 - A Game Boy cartridge program that enables the Game Boy to act as a full MIDI supported sound module.
* [lsdpatch](https://github.com/jkotlinski/lsdpatch) ⭐ 201 | 🐛 19 | 🌐 Java | 📅 2025-10-19 - Tool for modifying samples, fonts and palettes on LSDj ROM images.
* [gb-save-states](https://github.com/mattcurrie/gb-save-states) ⭐ 177 | 🐛 28 | 🌐 Assembly | 📅 2025-02-18 - Patches to add save state support to Game Boy games when playing on the original hardware.
* [ArduinoGameBoy](https://github.com/drhelius/arduinogameboy) ⭐ 163 | 🐛 1 | 🌐 C++ | 📅 2023-12-13 - Arduino based Game Boy cartridge reader and writer.
* [liblsdj](https://github.com/stijnfrishert/liblsdj) ⭐ 104 | 🐛 14 | 🌐 C | 📅 2024-05-02 - Utility library for interacting with the LSDj save format (.sav), song files (.lsdsng) and more.
* [Game Boy Link Cable Breakout Board](https://github.com/Palmr/gb-link-cable) ⭐ 104 | 🐛 0 | 📅 2022-08-18
* [GBxCart-RW](https://github.com/insidegadgets/GBxCart-RW) ⭐ 103 | 🐛 4 | 🌐 C | 📅 2022-12-29 - A device for reading game ROMs, save games and restoring saves for GB, GBC and GBA carts from your PC via USB.
* [fpgaboy](https://github.com/trun/fpgaboy) ⭐ 99 | 🐛 3 | 🌐 Verilog | 📅 2016-09-10 - Implementation Nintendo's Game Boy console on an FPGA.
* [GBCamcorder](https://github.com/furrtek/GBCamcorder) ⭐ 95 | 🐛 3 | 🌐 C | 📅 2021-12-20 - Lo-Fi portable video recorder using a GameBoy Camera cartridge.
* [GBCartRead](https://github.com/insidegadgets/GBCartRead) ⭐ 68 | 🐛 2 | 🌐 Eagle | 📅 2016-07-21 - Read ROM, Read RAM or Write RAM from/to a GameBoy Cartridge.
* [Piglet](https://github.com/danShumway/Piglet) ⭐ 44 | 🐛 3 | 🌐 Lua | 📅 2014-12-08 - A LUA-driven AI that plays classic Game Boy color games using experimentation. In active development.
* [Ostrich](https://github.com/PumpMagic/ostrich) ⭐ 43 | 🐛 0 | 🌐 Swift | 📅 2017-06-09 - A Game Boy Sound System player written in Swift.
* [GBVisualizer](https://github.com/LIJI32/GBVisualizer) ⭐ 28 | 🐛 0 | 🌐 Assembly | 📅 2017-04-14 - Demonstrating the use of two undocumented Game Boy Color registers, nicknamed PCM12 (FF76) and PCM34 (FF77), which can be used to read the current PCM amplitude of the 4 APU channels.
* [gbos](https://github.com/ekimekim/gbos) ⭐ 28 | 🐛 0 | 🌐 Assembly | 📅 2019-09-25 - A basic operating system for the Game Boy.
* [GBCartFlasher firmware](https://github.com/Tauwasser/GBCartFlasher) ⭐ 24 | 🐛 1 | 🌐 C | 📅 2019-06-01
* [papiGB](https://github.com/diegovalverde/papiGB) ⭐ 16 | 🐛 5 | 🌐 Verilog | 📅 2017-07-19 - Game Boy Classic fully functional FPGA implementation from scratch.
* [gameboy-brainfuck](https://github.com/bitnenfer/gameboy-brainfuck) ⭐ 16 | 🐛 0 | 🌐 Pascal | 📅 2017-01-27 - Brainf\*ck interpreter.
* [gbcpu](https://github.com/jdeblese/gbcpu) ⭐ 9 | 🐛 1 | 🌐 VHDL | 📅 2013-04-25 - A CPU and peripherals implementing the Game Boy instruction set and functionality.
* [Game Boy video effects](https://github.com/ChaosCabbage/crazy-gameboy-video-experiments) ⭐ 5 | 🐛 1 | 🌐 Assembly | 📅 2018-03-13 - Some little experiments using the STAT interrupt to do funny video manipulations.
* [gbfk](https://github.com/elseyf/gbfk) ⭐ 2 | 🐛 0 | 🌐 Assembly | 📅 2018-07-11 - Brainf\*ck interpreter, with input.
* [sm83-render](https://github.com/msinger/sm83-render) ⭐ 1 | 🐛 0 | 📅 2025-11-16 - A 3D model of the Game Boy CPU layout in Blender.
* [GB Studio](https://www.gbstudio.dev/) - Drag and drop game creator with simple, no knowledge required, visual scripting.
  * [Resources to get started](https://gbstudiocentral.com/resources/)
  * [Dedicated Discord](https://discord.gg/knRryZWGcm)
  * [Lets Build a Platformer Game!](https://gumpyfunction.itch.io/lets-build-a-platformer) - A course designed to teach anyone how to create a platformer game using GB Studio 4+.
* [Digitized Speech in Game Boy Games](https://youtube.com/watch?v=1lzHfLYzyRM)
* [Sniffing Game Boy serial traffic with an STM32F4](https://dhole.github.io/post/gameboy_serial_1/)
* [Virtual Game Boy Printer with an STM32F4](https://dhole.github.io/post/gameboy_serial_2/)
* [Printing on the Game Boy Printer using an STM32F4](https://dhole.github.io/post/gameboy_serial_3/)
* [Programming Game Boy Chinese cartridges with an STM32F4](https://dhole.github.io/post/gameboy_cartridge_rw_1/)
* [Pokemon Pocket Computer:](https://tilde.town/~minerobber/techwriteups/pokemonpc.html) - What is it and how to use it to make cheat codes.
* [Booting the Game Boy with a custom logo](https://dhole.github.io/post/gameboy_custom_logo/) - Bypassing the Nintendo logo check.
* Making a Game Boy game in 2017: A "Sheep It Up!" Post-Mortem ([part 1](https://www.gamasutra.com/blogs/DoctorLudos/20171207/311143/), [part 2](https://www.gamasutra.com/blogs/DoctorLudos/20180213/314554/))
* [Nintendo's fake logos](http://fuji.drillspirits.net/?post=87) - Every cartridge has to show the authentic logo to be considered valid and be run, but obviously some companies managed to exploit the check system.
* [Work Master OS](https://translate.google.com/translate?hl=\&sl=ru\&tl=en\&u=https%3A%2F%2Fweb.archive.org%2Fweb%2F20081226145726%2Fhttp%3A%2F%2Fworkmaster.ru%2Findex.php%3Fp%3D8\&sandbox=1) - Russian multi tasking operating system.
* [Dumping the Super Game Boy Boot ROM](http://www.its.caltech.edu/~costis/sgb_hack/)
* [visual-sm83](https://iceboy.a-singer.de/visual6502/expert-sm83.html) - A visual transistor level simulation of the Game Boy CPU core in JavaScript, running in a browser.

### Directories

* [Archive of related files](http://gbdev.gg8.se/files/)
* [The Game Boy Archive](https://github.com/gb-archive) - A library of Game Boy related software, hardware and literature. Aimed to mirror and preserve old and fragmented contributions from the last three decades.
* [The Game Boy Archive - Salvage](https://github.com/gb-archive/salvage) ⭐ 38 | 🐛 2 | 🌐 HTML | 📅 2025-04-22 - Historical archive of software, old articles, FAQs and various documents.

### Websites

* [devrs.com/gb](http://devrs.com/gb) - Old home of the scene: examples, sources, complete documentation, guides, tutorials and various tools.
* [pdroms.de](http://pdroms.de/news/gameboy/) - Game Boy releases.
* [Handheld Underground](http://hhug.me) - Unlicensed games, blog posts about Game Boy, home of the hhugboy emulator.

## About

### Contribute

Take a look at [Contribution Guidelines](origin/CONTRIBUTING.md).

### License

Licensed under **GPLv3**.
See [LICENSE](origin/LICENSE) for more information.

### Acknowledgements

Thanks to [every](https://github.com/avivace/awesome-gbdev/graphs/contributors) ⭐ 4,376 | 🐛 21 | 📅 2026-01-13 contributor of this project, Jeff Frohwein, Pascal Felber, KOOPa, Pan of Anthrox, GABY, Marat Fayzullin, Paul Robson, BOWSER, neviksti, Martin "nocash" Korth, Nitro2k01, Duo, Chris Antonellis, Michael Hope, Beware, Jonathan “Lord Nightmare” Gevaryahu, Carsten Sorense, Sindre Aamås, Otaku No Zoku, GeeBee.

### Sponsors

Special thanks to our friends at [DigitalOcean](https://www.digitalocean.com/) and [Incube8 Games](https://incube8games.com/), sponsoring the open source activites of our Game Boy Development community.

# PokéBot Gen 3
[![Wiki](wiki/images/badge_wiki.svg)](wiki/Readme.md) [![Python 3.12](wiki/images/badge_python.svg)](https://www.python.org/downloads/release/python-3132/) 

**PokéBot Gen3** is a shiny hunting bot, written in Python that runs `libmgba` + mGBA Python bindings under the hood. Pokémon Ruby, Sapphire, Emerald, FireRed and LeafGreen are supported. 

# ❓ Getting Started

- ❓ [Getting Started](wiki/pages/Getting%20Started.md)
- 🎮 [Emulator Input Mapping](wiki/pages/Configuration%20-%20Key%20Mappings.md)

# ✨ Preamble

The intent of this bot is not to _cheat_ for shinies or complete the game as fast as possible, but instead to transform generation 3 Pokémon games into somewhat of an idle game, stacking up millions of encounters searching for that one encounter, or completing an absurd challenge.

The bot is frame perfect and can _technically_ cheat by reading data from any point in memory and manipulating RNG. By default, it will attempt to perform actions as if a human were playing to make gameplay as representative as possible, some examples:
- Starter Pokémon are generated just _1 frame_ after confirming the starter selection, the bot will wait until the battle begins, and the starter Pokémon sprite is visible before soft resetting
- It's possible to peek inside un-hatched eggs to view stats and shininess as soon as they're received from the daycare, the bot will wait until the eggs are fully hatched before checking and logging
- Feebas tile locations _could_ be instantly located by reading memory, instead, the bot will attempt to locate the tiles by searching each tile individually

# 😎 Showcase

|              Main interface              |              Load save state              |              Debug mode              |
|:----------------------------------------:|:-----------------------------------------:|:------------------------------------:|
| ![image](wiki/images/main_interface.png) | ![image](wiki/images/load_save_state.png) | ![image](wiki/images/debug_mode.png) |

| Shiny encounter GIFs            | 
|---------------------------------|
| ![image](wiki/images/shiny.gif) |


| HTTP API                           |
|------------------------------------|
| ![image](wiki/images/http_api.png) |

# ❤ Attributions

Core functionality:

- [mGBA](https://github.com/mgba-emu/mgba)
- [libmgba-py](https://github.com/hanzi/libmgba-py/)

Decompiled symbol tables and other various data from the following projects:

- [Pokémon Emerald decompilation](https://github.com/pret/pokeemerald) ([symbols](https://github.com/pret/pokeemerald/tree/symbols))
- [Pokémon Ruby and Sapphire decompilation](https://github.com/pret/pokeruby) ([symbols](https://github.com/pret/pokeruby/tree/symbols))
- [Pokémon FireRed and LeafGreen decompilation](https://github.com/pret/pokefirered) ([symbols](https://github.com/pret/pokefirered/tree/symbols))


---
description: Baimless LUA-scripts API documentation
---

# Overview

## 📚 Information

Backend LUA engine: [**LuaJIT**](https://github.com/LuaJIT/LuaJIT) **v2.1.0**

Supported LuaJIT [extensions](https://luajit.org/extensions.html):

* [bit](https://bitop.luajit.org/api.html) - bit operations
* [ffi](https://luajit.org/ext_ffi_api.html) - calling external C functions and using C data structures
* [jit](https://luajit.org/ext_jit.html) - just-in-time lua compiler behavior control
* [coroutine](https://www.lua.org/manual/5.1/manual.html#5.2) - collaborative multithreading
* [modules](https://www.lua.org/manual/5.1/manual.html#5.3) - loading and building modules for LUA
* [string](https://www.lua.org/manual/5.1/manual.html#5.4) - strings manipulation
* [table](https://www.lua.org/manual/5.1/manual.html#5.5) - tables manipulation
* [math](https://www.lua.org/manual/5.1/manual.html#5.6) - built-in mathematic functions
* [io](https://www.lua.org/manual/5.1/manual.html#5.7) - input/output file manipulations
* [os](https://www.lua.org/manual/5.1/manual.html#5.8) - operating system facilities
* [utf8](https://github.com/rollraw/baimless-lua-api/blob/master) - support of UTF-8 encoded characters

## 🗺️ Navigation

#### 💡 Core

Description: tables of main i/o cheat parts

* [Client](https://github.com/rollraw/baimless-lua-api/blob/master/doc/core/client.md)
* [Config](https://github.com/rollraw/baimless-lua-api/blob/master/doc/core/config.md)
* [Menu](https://github.com/rollraw/baimless-lua-api/blob/master/doc/core/menu.md)
* [Draw](https://github.com/rollraw/baimless-lua-api/blob/master/doc/core/draw.md)
* [HTTP](https://github.com/rollraw/baimless-lua-api/blob/master/doc/core/http.md)

#### 📢 Interfaces

Description: tables of source-SDK abstract classes to work with game

* [IClientState](https://github.com/rollraw/baimless-lua-api/blob/master/doc/interfaces/iclientstate.md)
* [IConVar](https://github.com/rollraw/baimless-lua-api/blob/master/doc/interfaces/iconvar.md)
* [IEngine](https://github.com/rollraw/baimless-lua-api/blob/master/doc/interfaces/iengine.md)
* [IEntityList](https://github.com/rollraw/baimless-lua-api/blob/master/doc/interfaces/ientitylist.md)
* [IGlobals](https://github.com/rollraw/baimless-lua-api/blob/master/doc/interfaces/iglobals.md)

#### 📦 Data Types

Description: classes to work with game or cheat functions/variables

* [Color](https://github.com/rollraw/baimless-lua-api/blob/master/doc/datatypes/color.md)
* [Vector2D](https://github.com/rollraw/baimless-lua-api/blob/master/doc/datatypes/vector2d.md)
* [Vector](https://github.com/rollraw/baimless-lua-api/blob/master/doc/datatypes/vector.md)
* [QAngle](https://github.com/rollraw/baimless-lua-api/blob/master/doc/datatypes/qangle.md)

#### 🔗 Classes

Description: classes to get/set values from/to the game

* [IGameEvent](https://github.com/rollraw/baimless-lua-api/blob/master/doc/classes/igameevent.md)
* [INetChannelInfo](https://github.com/rollraw/baimless-lua-api/blob/master/doc/classes/inetchannelinfo.md)
* [IClientEntity](https://github.com/rollraw/baimless-lua-api/blob/master/doc/classes/icliententity.md)
* [CBaseEntity](https://github.com/rollraw/baimless-lua-api/blob/master/doc/classes/cbaseentity.md)
* [CBaseCombatWeapon](https://github.com/rollraw/baimless-lua-api/blob/master/doc/classes/cbasecombatweapon.md)
* [CUserCmd](https://github.com/rollraw/baimless-lua-api/blob/master/doc/classes/cusercmd.md)
* [CConVar](https://github.com/rollraw/baimless-lua-api/blob/master/doc/classes/cconvar.md)
* [PlayerInfo\_t](https://github.com/rollraw/baimless-lua-api/blob/master/doc/classes/playerinfo_t.md)

## 🧬 Remarks

1. Default LUA library function `print()` is overloaded to cheat logging system
2. Added `math.hypotf` function overload to standart math LUA library
3. Added `math.roundf` function overload to standart math LUA library
4. Added `math.lerp` function overload to standart math LUA library

## ⭐ Contribute

_Found a mistake in documentation? Looking for a better explanation or API enhancement?_

Feel free to open [issue](https://github.com/rollraw/baimless-api-book/issues) or [pull request](https://github.com/rollraw/baimless-api-book/pulls)


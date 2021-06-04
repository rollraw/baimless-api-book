# readme

## :books: Information

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
* [utf8](undefined.md) - support of UTF-8 encoded characters

## :world\_map: Navigation

:bulb: Core  
 &gt; Description: tables of main i/o cheat parts - \[Client\]\(doc/core/client.md\) - \[Config\]\(doc/core/config.md\) - \[Menu\]\(doc/core/menu.md\) - \[Draw\]\(doc/core/draw.md\) - \[HTTP\]\(doc/core/http.md\)

:loudspeaker: Interfaces  
 &gt; Description: tables of source-SDK abstract classes to work with game - \[IClientState\]\(doc/interfaces/iclientstate.md\) - \[IConVar\]\(doc/interfaces/iconvar.md\) - \[IEngine\]\(doc/interfaces/iengine.md\) - \[IEntityList\]\(doc/interfaces/ientitylist.md\) - \[IGlobals\]\(doc/interfaces/iglobals.md\)

:package: Data Types  
 &gt; Description: classes to work with game or cheat functions/variables - \[Color\]\(doc/datatypes/color.md\) - \[Vector2D\]\(doc/datatypes/vector2d.md\) - \[Vector\]\(doc/datatypes/vector.md\) - \[QAngle\]\(doc/datatypes/qangle.md\)

:link: Classes  
 &gt; Description: classes to get/set values from/to the game - \[IGameEvent\]\(doc/classes/igameevent.md\) - \[INetChannelInfo\]\(doc/classes/inetchannelinfo.md\) - \[IClientEntity\]\(doc/classes/icliententity.md\) - \[CBaseEntity\]\(doc/classes/cbaseentity.md\) - \[CBaseCombatWeapon\]\(doc/classes/cbasecombatweapon.md\) - \[CUserCmd\]\(doc/classes/cusercmd.md\) - \[CConVar\]\(doc/classes/cconvar.md\) - \[PlayerInfo\_t\]\(doc/classes/playerinfo\_t.md\)

## :dna: Remarks

1. Default LUA library function `print()` is overloaded to cheat logging system
2. Added `math.hypotf` function overload to standart math LUA library
3. Added `math.roundf` function overload to standart math LUA library
4. Added `math.lerp` function overload to standart math LUA library

## :star: Contribute

_Found a mistake in documentation? Looking for a better explanation or API enhancement?_

Feel free to open [issue](https://github.com/rollraw/baimless-lua-api/issues) or [pull request](https://github.com/rollraw/baimless-lua-api/pulls)


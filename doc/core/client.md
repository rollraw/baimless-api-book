---
description: General cheat-related functions
---

# client

🚧 _API of this file is not finished yet and could be changed in any time_

## Functions

### RegisterCallback

List:

| Name | Arguments | Description |
| :--- | :--- | :--- |
| Paint | - | primitives drawing |
| FrameStageNotify | nStage | called on every frame stage |
| CreateMoveIn | [CUserCmd](../classes/cusercmd.md), bSendPacket | createmove inside engine prediction |
| CreateMovePre | [CUserCmd](../classes/cusercmd.md), bSendPacket | createmove before engine prediction |
| CreateMovePost | [CUserCmd](../classes/cusercmd.md), bSendPacket | createmove post engine prediction |
| Destroy | - | called on current script unload |

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szCallbackName | string | name of callback where function will be called |
| pFunction | function | function to be called within callback |

Code:

```lua
local flRainbow = 0.001
Client.RegisterCallback("Paint", function()
    if (flRainbow >= 1.0) then
        flRainbow = 0.0 -- clamp
    else
        flRainbow = flRainbow + 0.001
    end

    local colRainbow = Color.FromHSB(flRainbow, 1.0, 1.0, 1.0)
    Draw.AddCircle(Vector2D.new(150.0, 150.0), 50.0, colRainbow, 12, bit.bor(ECircleRenderFlags.DRAW_CIRCLE_FILLED, ECircleRenderFlags.DRAW_CIRCLE_OUTLINE))
end)
```

### RegisterEventCallback

List: [CS:GO Game Events](https://wiki.alliedmods.net/Counter-Strike:_Global_Offensive_Events)

Arguments: [IGameEvent\*](../classes/igameevent.md)

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szEventName | string | name of event where on trigger function will be called |
| pFunction | function | function to be called on event trigger |

Code:

```lua
Client.RegisterEventCallback("player_death", function(pEvent)
    local localPlayer = IEngine.GetLocalPlayer()
    local nAttackerID = IEngine.GetPlayerForUserId(pEvent.GetInt("attacker"))
    local nDeadID = IEngine.GetPlayerForUserId(pEvent.GetInt("userid"))
    
    if nAttackerID == nDeadID or nAttackerID ~= localPlayer then
        return
        end
    
    IEngine.ExecuteClientCmd('say trashtalk on kill')
end)
```

### LoadScript

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szScriptName | string | name of script to load |

Code:

```lua
Client.LoadScript("qo0.lua")
```

### UnloadScript

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szScriptName | string | name of script to unload |

Code:

```lua
Client.UnloadScript("qo0.lua")
```

### FindPattern

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szModule | string | name of module to search signature in |
| szSignature | string | IDA style signature to search |

Returns:

| Type | Description |
| :--- | :--- |
| unsigned int | address of given pattern |

Code:

```lua
local ffi = require("ffi")
local oSetClanTag = ffi.cast('int(__fastcall*)(const char*, const char*)', Client.FindPattern('engine.dll', '53 56 57 8B DA 8B F9 FF 15'))

Client.RegisterCallback("CreateMovePre", function(pCmd)
    oSetClanTag('baimless', 'baimless')
end)
```

### CaptureInterface

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szModule | string | name of module where interface defined |
| szInterface | string | name of interface to capture |

Returns:

| Type | Description |
| :--- | :--- |
| void\* | pointer of captured interface |

Code:

```lua
local ffi = require("ffi")
ffi.cdef[[
struct IGameConsole
{
	virtual			~IGameConsole() { }
	virtual void	Activate() = 0; // activates the console, makes it visible and brings it to the foreground
	virtual void	Initialize() = 0;
	virtual void	Hide() = 0; // hides the console
	virtual void	Clear() = 0; // clears the console
	virtual bool	IsConsoleVisible() = 0; // return true if the console has focus
	virtual void	SetParent(int iParent) = 0;
};
]]

local IGameConsole = ffi.cast('IGameConsole*', Client.CaptureInterface('client.dll', 'GameConsole'))
IGameConsole.Clear()
```

### GetCheatUserName

Returns:

| Type | Description |
| :--- | :--- |
| string | cheat username |

Code:

```lua
local szUserName = Client.GetCheatUserName()
print(szUserName)
```


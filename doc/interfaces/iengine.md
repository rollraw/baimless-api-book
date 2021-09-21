# iengine

## Functions

### GetScreenSize

Returns:

| Type | Description |
| :--- | :--- |
| [Vector2D](../datatypes/vector2d.md) | width and height of game screen |

Code:

```lua
local vecScreenSize = IEngine.GetScreenSize()
```

### GetPlayerInfo

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| nEntityIndex | int | index of entity to get player info for |

Returns:

| Type | Description |
| :--- | :--- |
| [PlayerInfo\_t](../classes/playerinfo_t.md) | entity player info of given index |

Code:

```lua
local playerInfo = IEngine.GetPlayerInfo(pLocal:GetIndex())
```

### GetPlayerForUserID

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| nUserID | int | user index to get player index for |

Returns:

| Type | Description |
| :--- | :--- |
| int | player index of given user index |

Code:

```lua
local nPlayerID = IEngine.GetPlayerForUserID(1)
```

### GetLocalPlayer

Returns:

| Type | Description |
| :--- | :--- |
| int | entity index of local player |

Code:

```lua
local nLocalPlayerIndex = IEngine.GetLocalPlayer()
```

### GetViewAngles

Return value:

| Type | Description |
| :--- | :--- |
| [QAngle](../datatypes/qangle.md) | local player view angles |

Code:

```lua
local angViewPoint = IEngine.GetViewAngles()
```

### SetViewAngles

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| angViewPoint | [QAngle](../datatypes/qangle.md) | view angles to set for local player |

Code:

```lua
IEngine.SetViewAngles(QAngle.new(-90.0, 180.0, 0.0))
```

### GetMaxClients

Returns:

| Type | Description |
| :--- | :--- |
| int | max client count for server |

Code:

```lua
local nMaxClients = IEngine.GetMaxClients()
```

### IsInGame

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if we're in-game |

Code:

```lua
local bIsInGame = IEngine.IsInGame()
```

### IsConnected

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if we're connected \(connection message was shown\) |

Code:

```lua
local bIsConnected = IEngine.IsConnected()
```

### GetLevelName

Returns:

| Type | Description |
| :--- | :--- |
| string | current map full name |

Code:

```lua
local szLevelName = IEngine.GetLevelName()
```

### GetLevelNameShort

Returns:

| Type | Description |
| :--- | :--- |
| string | current map short name |

Code:

```lua
local szShortLevelName = IEngine.GetLevelNameShort()
```

### GetMapGroupName

Returns:

| Type | Description |
| :--- | :--- |
| string | current map group name |

Code:

```lua
local szMapGroupName = IEngine.GetMapGroupName()
```

### GetNetChannelInfo

Returns:

| Type | Description |
| :--- | :--- |
| [INetChannelInfo\*](../classes/inetchannelinfo.md) | pointer of net channel info |

Code:

```lua
local pNetChannelInfo = IEngine.GetNetChannelInfo()
```

### IsPlayingDemo

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if demo is being played back |

Code:

```lua
local bIsPlayingDemo = IEngine.IsPlayingDemo()
```

### IsRecordingDemo

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if demo is being recorded |

Code:

```lua
local bIsRecordingDemo = IEngine.IsRecordingDemo()
```

### IsPaused

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if game is paused |

Code:

```lua
local bIsPaused = IEngine.IsPaused()
```

### IsHLTV

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if currently used HLTV \(kill replay etc\) |

Code:

```lua
local bIsHLTV = IEngine.IsHLTV()
```

### ExecuteClientCmd

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szCmdString | string | command to execute \(without flag checks\) |

Code:

```lua
IEngine.ExecuteClientCmd("say console log")
```

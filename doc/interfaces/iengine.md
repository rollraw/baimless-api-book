# iengine

## Functions

### GetScreenSize

Returns:

| Type | Description |
| :--- | :--- |
| Vector2D | width and height of game screen |

Code:

```text
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
| PlayerInfo\_t | entity player info of given index |

Code:

```text
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

```text
local nPlayerID = IEngine.GetPlayerForUserID(1)
```

### GetLocalPlayer

Returns:

| Type | Description |
| :--- | :--- |
| int | entity index of local player |

Code:

```text
local nLocalPlayerIndex = IEngine.GetLocalPlayer()
```

### GetViewAngles

Return value:

| Type | Description |
| :--- | :--- |
| QAngle | local player view angles |

Code:

```text
local angViewPoint = IEngine.GetViewAngles()
```

### SetViewAngles

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| angViewPoint | QAngle | view angles to set for local player |

Code:

```text
IEngine.SetViewAngles(QAngle.new(-90.0, 180.0, 0.0))
```

### GetMaxClients

Returns:

| Type | Description |
| :--- | :--- |
| int | max client count for server |

Code:

```text
local nMaxClients = IEngine.GetMaxClients()
```

### IsInGame

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if we're in-game |

Code:

```text
local bIsInGame = IEngine.IsInGame()
```

### IsConnected

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if we're connected \(connection message was shown\) |

Code:

```text
local bIsConnected = IEngine.IsConnected()
```

### GetLevelName

Returns:

| Type | Description |
| :--- | :--- |
| string | current map full name |

Code:

```text
local szLevelName = IEngine.GetLevelName()
```

### GetLevelNameShort

Returns:

| Type | Description |
| :--- | :--- |
| string | current map short name |

Code:

```text
local szShortLevelName = IEngine.GetLevelNameShort()
```

### GetMapGroupName

Returns:

| Type | Description |
| :--- | :--- |
| string | current map group name |

Code:

```text
local szMapGroupName = IEngine.GetMapGroupName()
```

### GetNetChannelInfo

Returns:

| Type | Description |
| :--- | :--- |
| [INetChannelInfo\*](https://github.com/rollraw/baimless-lua-api/blob/master/doc/classes/inetchannelinfo.md) | pointer of net channel info |

Code:

```text
local pNetChannelInfo = IEngine.GetNetChannelInfo()
```

### IsPlayingDemo

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if demo is being played back |

Code:

```text
local bIsPlayingDemo = IEngine.IsPlayingDemo()
```

### IsRecordingDemo

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if demo is being recorded |

Code:

```text
local bIsRecordingDemo = IEngine.IsRecordingDemo()
```

### IsPaused

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if game is paused |

Code:

```text
local bIsPaused = IEngine.IsPaused()
```

### IsHLTV

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if currently used HLTV \(kill replay etc\) |

Code:

```text
local bIsHLTV = IEngine.IsHLTV()
```

### ExecuteClientCmd

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szCmdString | string | command to execute \(within flag checks\) |

Code:

```text
IEngine.ExecuteClientCmd("say console log")
```

### ClientCmdUnrestricted

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szCmdString | string | command to execute \(without flag checks\) |

Code:

```text
IEngine.ExecuteClientCmd("sv_cheats 1")
```


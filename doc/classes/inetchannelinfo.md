# inetchannelinfo

## Functions

### GetName

Returns:

| Type | Description |
| :--- | :--- |
| string | current channel name |

Code:

```lua
local pNetChannelInfo = IEngine.GetNetChannelInfo()
local szChannelName = pNetChannelInfo:GetName()
print(szChannelName)
```

### GetAddress

Returns:

| Type | Description |
| :--- | :--- |
| string | current channel IP address |

Code:

```lua
local pNetChannelInfo = IEngine.GetNetChannelInfo()
local szServerIP = pNetChannelInfo:GetAddress()
print(szServerIP)
```

### IsLoopback

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if channel is loopback |

Code:

```lua
local pNetChannelInfo = IEngine.GetNetChannelInfo()
local bIsLoopback = pNetChannelInfo:IsLoopback()
```

### IsPlayback

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if demo playback |

Code:

```lua
local pNetChannelInfo = IEngine.GetNetChannelInfo()
local bIsPlayback = pNetChannelInfo:IsPlayback()
```

### GetLatency

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| iFlow | int | flow type |

Returns:

| Type | Description |
| :--- | :--- |
| float | current latency \(RTT\) |

Code:

```lua
local pNetChannelInfo = IEngine.GetNetChannelInfo()
local flPing = pNetChannelInfo:GetLatency(0)
print(tostring(flPing))
```

### GetAvgLatency

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| iFlow | int | flow type |

Returns:

| Type | Description |
| :--- | :--- |
| float | average packet latency in seconds |

Code:

```lua
local pNetChannelInfo = IEngine.GetNetChannelInfo()
local flAvgPing = pNetChannelInfo:GetAvgLatency(0)
print(tostring(flAvgPing))
```

### GetAvgLoss

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| iFlow | int | flow type |

Returns:

| Type | Description |
| :--- | :--- |
| float | average packet loss \[0..1\] |

Code:

```lua
local pNetChannelInfo = IEngine.GetNetChannelInfo()
local flAvgLoss = pNetChannelInfo:GetAvgLoss(0)
print(tostring(flAvgLoss))
```

### GetAvgChoke

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| iFlow | int | flow type |

Returns:

| Type | Description |
| :--- | :--- |
| float | average packet choke \[0..1\] |

Code:

```lua
local pNetChannelInfo = IEngine.GetNetChannelInfo()
local flAvgChoke = pNetChannelInfo:GetAvgChoke(0)
print(tostring(flAvgChoke))
```

### GetAvgData

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| iFlow | int | flow type |

Returns:

| Type | Description |
| :--- | :--- |
| float | data flow in bytes/sec |

Code:

```lua
local pNetChannelInfo = IEngine.GetNetChannelInfo()
local flAvgData = pNetChannelInfo:GetAvgData(0)
print(tostring(flAvgData))
```

### GetAvgPackets

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| iFlow | int | flow type |

Returns:

| Type | Description |
| :--- | :--- |
| float | average packets/sec |

Code:

```lua
local pNetChannelInfo = IEngine.GetNetChannelInfo()
local flAvgPackets = pNetChannelInfo:GetAvgPackets(0)
print(tostring(flAvgPackets))
```


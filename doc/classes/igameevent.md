# igameevent

## Functions

### GetName

Returns:

| Type | Description |
| :--- | :--- |
| string | current event name |

Code:

```lua
local szName = pEvent:GetName()
print(szName)
```

### GetBool

Returns:

| Type | Description |
| :--- | :--- |
| bool | returns bool value |

Code:

```lua
local bValue = pEvent:GetBool()
```

### GetInt

Returns:

| Type | Description |
| :--- | :--- |
| int | returns int value |

Code:

```lua
local iValue = pEvent:GetInt()
```

### GetUint64

Returns:

| Type | Description |
| :--- | :--- |
| uint64 | returns uint64 value |

Code:

```lua
local ullValue = pEvent:GetUint64()
```

### GetFloat

Returns:

| Type | Description |
| :--- | :--- |
| float | returns float value |

Code:

```lua
local flValue = pEvent:GetFloat()
```

### GetString

Returns:

| Type | Description |
| :--- | :--- |
| string | returns string value |

Code:

```lua
local szValue = pEvent:GetString()
```

### SetBool

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| bValue | bool | value to set |

Code:

```lua
pEvent:SetBool(true)
```

### SetInt

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| iValue | int | value to set |

```lua
pEvent:SetInt(1)
```

Code:

### SetUint64

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| ullValue | uint64 | value to set |

Code:

```lua
pEvent:SetUint64(1)
```

### SetFloat

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| flValue | float | value to set |

Code:

```lua
pEvent:SetFloat(1.0)
```

### SetString

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szValue | string | value to set |

Code:

```lua
pEvent:SetString("1")
```


# cconvar

## Functions

### GetName

Returns:

| Type | Description |
| :--- | :--- |
| string | convar name |

Code:

```lua
local sv_cheats = IConVar.FindVar("sv_cheats")
local szName = sv_cheats:GetName()
print(szName)
```

### GetFloat

Returns:

| Type | Description |
| :--- | :--- |
| float | convar value |

Code:

```lua
local flValue = pSomeCVar:GetFloat()
```

### GetInt

Returns:

| Type | Description |
| :--- | :--- |
| int | convar value |

Code:

```lua
local iValue = pSomeCVar:GetInt()
```

### GetBool

Returns:

| Type | Description |
| :--- | :--- |
| bool | convar value |

Code:

```lua
local bValue = pSomeCVar:GetBool()
```

### GetString

Returns:

| Type | Description |
| :--- | :--- |
| string | convar value |

Code:

```lua
local szValue = pSomeCVar:GetString()
```

### SetFloat

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| flValue | float | value to set |

Code:

```lua
pSomeCVar:SetFloat(1.0)
```

### SetInt

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| iValue | int | value to set |

Code:

```lua
pSomeCVar:SetInt(1)
```

### SetBool

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| bValue | bool | value to set |

Code:

```lua
pSomeCVar:SetBool(true)
```

### SetString

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szValue | string | value to set |

Code:

```lua
pSomeCVar:SetString("1")
```

### SetColor

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| colValue | [Color](../datatypes/color.md) | value to set |

Code:

```lua
pSomeCVar:SetColor(Color.new(255, 255, 255))
```

### ChangeCallback

Code:

```lua
local cl_fullupdate = IConVar.FindVar("cl_fullupdate")

-- invoke to call change callback, executes a ConCommand or convar callback
-- in this case will cause to force full update
cl_fullupdate:ChangeCallback()
```


# cconvar

## Functions

### GetName

Returns:

| Type | Description |
| :--- | :--- |
| string | convar name |

Code:

```text
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

```text
local flValue = pSomeCVar:GetFloat()
```

### GetInt

Returns:

| Type | Description |
| :--- | :--- |
| int | convar value |

Code:

```text
local iValue = pSomeCVar:GetInt()
```

### GetBool

Returns:

| Type | Description |
| :--- | :--- |
| bool | convar value |

Code:

```text
local bValue = pSomeCVar:GetBool()
```

### GetString

Returns:

| Type | Description |
| :--- | :--- |
| string | convar value |

Code:

```text
local szValue = pSomeCVar:GetString()
```

### SetFloat

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| flValue | float | value to set |

Code:

### SetInt

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| iValue | int | value to set |

Code:

### SetBool

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| bValue | bool | value to set |

Code:

### SetString

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szValue | string | value to set |

Code:

### SetColor

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| colValue | Color | value to set |

Code:

```text
pSomeCVar:SetColor(Color.new(255, 255, 255))
```

### ChangeCallback

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| colValue | Color | value to set |

Code:

```text
local cl_fullupdate = IConVar.FindVar("cl_fullupdate")

-- invoke to call change callback, executes a ConCommand or convar callback
-- in this case will cause to force full update
cl_fullupdate:ChangeCallback()
```


# iconvar

## Functions

### FindVar

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szVariableName | string | console variable name |

Returns:

| Type | Description |
| :--- | :--- |
| [CConVar\*](../classes/cconvar.md) | console variable pointer |

Code:

```lua
local sv_cheats = IConVar.FindVar("sv_cheats")
```

### ConsolePrintf

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szFormat | string | text to output into game console |

Code:

```lua
IConVar.ConsolePrintf("text to print")
```

### ConsoleColorPrintf

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| colText | color | color of output text |
| szFormat | string | text to output into game console |

Code:

```lua
IConVar.ConsoleColorPrintf(Color.new(0, 255, 255), "text to print")
```


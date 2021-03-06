---
description: >-
  Functions to add widgets into special group for scripts, and modulating
  variables (not a built-in cheat configuration variables! see config table for
  more info) of them
---

# menu

🚧 _API of this file is not finished yet and could be changed in any time_

## Enumerations

### EKeyBindMode

Description: keybind variables switch mode

| Indentifiers |
| :--- |
| KEYBIND\_HOLD |
| KEYBIND\_TOGGLE |

## Functions

### IsOpened

Returns:

| Type | Description |
| :--- | :--- |
| bool | true when cheat menu opened |

Code:

```lua
local bIsMenuOpened = Menu.IsOpened()
```

### Button

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szName | string | widget name |
| pCallback | function | callback on button click |
| _szTooltip_ | string | tooltip when user hovers widget |

Code:

```lua
Menu.Button("Test button", function()
    print("clicked!")
end, "Optional tooltip")
```

### Checkbox

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szName | string | widget name |
| _bDefault_ | bool | default widget variable value |
| _szTooltip_ | string | tooltip when user hovers widget |

Code:

```lua
Menu.Checkbox("Test checkbox", true, "Optional tooltip")
```

### Toggle

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szName | string | widget name |
| _bDefault_ | bool | default widget variable value |
| _szTooltip_ | string | tooltip when user hovers widget |

Code:

```lua
Menu.Toggle("Test toggle", true, "Optional tooltip")
```

### HotKey

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szName | string | widget name |
| _iDefualtKey_ | int | default hotkey widget key |
| _iDefaultMode_ | int | default hotkey widget key mode |
| _szTooltip_ | string | tooltip when user hovers widget |

Code:

```lua
Menu.HotKey("Test hotkey", 0, EKeyBindMode.KEYBIND_TOGGLE, "Optional tooltip")
```

### Combo

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szName | string | widget name |
| vecLabels | table | combo widget entries labels |
| _nDefault_ | int | default combo widget selected label index |
| _szTooltip_ | string | tooltip when user hovers widget |

Code:

```lua
Menu.Combo("Test combo", { "First", "Second", "Third" }, 1, "Optional tooltip")
```

### MultiCombo

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szName | string | widget name |
| vecLabels | table | multicombo widget entries labels |
| _nDefault_ | bitflag | default multicombo widget selected labels flags |
| _szTooltip_ | string | tooltip when user hovers widget |

Code:

```lua
local bit = require("bit")
Menu.MultiCombo("Test combo", { "First", "Second", "Third" }, bit.bor(bit.lshift(1, 0), bit.lshift(2, 0)), "Optional tooltip")
```

### SliderInt

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szName | string | widget name |
| iMinimal | int | sliderint widget minimal allowed variable value |
| iMaximal | int | sliderint widget maximal allowed variable value |
| _iDefault_ | int | default sliderint widget variable value |
| _szTooltip_ | string | tooltip when user hovers widget |

Code:

```lua
Menu.SliderInt("Test slider int", -5, 10, 2)
```

### SliderFloat

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szName | string | widget name |
| flMinimal | float | sliderfloat widget minimal allowed variable value |
| flMaximal | float | sliderfloat widget maximal allowed variable value |
| _flDefault_ | float | default sliderfloat widget variable value |
| _szTooltip_ | string | tooltip when user hovers widget |

Code:

```lua
Menu.SliderFloat("Test slider float", 0.0, 100.0, 25.5)
```

### ColorPicker

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szName | string | widget name |
| _colDefault_ | [Color](../datatypes/color.md) | default color picker widget variable value |
| _szTooltip_ | string | tooltip when user hovers widget |

Code:

```lua
Menu.ColorPicker("Test color picker", Color.new())
```

### Get

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szWidgetName | string | widget name to get value from |
| _szScriptName_ | string | script name where located widget |

Returns:

| Type | Description |
| :--- | :--- |
| any | automatic value, for a checkbox/toggle, returns boolean. for a sliderint/combo/multicombo, returns an integer. for a sliderfloat, returns a float. for a hotkey, returns true if the hotkey is active. for a color picker, returns [Color](../datatypes/color.md) |

Code:

```lua
Menu.ColorPicker("Test color picker", Color.new(150, 200, 50))
local colValue = Menu.Get("Test color picker", "qo0.lua")
```

### Set

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szWidgetName | string | widget name to set value to |
| value | any | automatic value, for a checkbox/toggle - bool. for a sliderint/combo/multicombo - integer. for a sliderfloat - float. for a hotkey - bool. for a color picker -[ Color](../datatypes/color.md) |
| _szScriptName_ | string | script name where located widget |

Code:

```lua
Menu.SliderFloat("Test Slider", 0.0, 100.0, 50.0)
Menu.Set("Test Slider", 1.5)
```

### DeleteWidget

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szWidgetName | string | widget name to delete from menu |

Code:

```lua
Menu.Checkbox("I'll be removed soon")
Menu.Button("Click to remove", function()
    Menu.DeleteWidget("I'll be removed soon")
end)
```


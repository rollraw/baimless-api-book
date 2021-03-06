---
description: IClientEntity is base class
---

# cbasecombatweapon

## Functions

### IsReloading

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if weapon in reload |

Code:

```lua
local bIsReloading = pWeapon:IsReloading()
```

### IsWeapon

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if entity is weapon |

Code:

```lua
local bIsWeapon = pWeapon:IsWeapon()
```

### GetItemDefinitionIndex

Returns:

| Type | Description |
| :--- | :--- |
| short | item definition index |

Code:

```lua
local nDefinitionIndex = pWeapon:GetItemDefinitionIndex()
```

### GetSpread

Returns:

| Type | Description |
| :--- | :--- |
| float | spread factor |

Code:

```lua
local flSpread = pWeapon:GetSpread()
```

### GetInaccuracy

Returns:

| Type | Description |
| :--- | :--- |
| float | innacuracy factor |

Code:

```lua
local flInaccuracy = pWeapon:GetInaccuracy()
```

### GetMaxTickbaseShift

Returns:

| Type | Description |
| :--- | :--- |
| int | maximal number of ticks can be shifted |

Code:

```lua
local nMaxShift = pWeapon:GetMaxTickbaseShift()
```


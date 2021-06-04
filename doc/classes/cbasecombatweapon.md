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

```text
local bIsReloading = pWeapon:IsReloading()
```

### IsWeapon

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if entity is weapon |

Code:

```text
local bIsWeapon = pWeapon:IsWeapon()
```

### GetItemDefinitionIndex

Returns:

| Type | Description |
| :--- | :--- |
| short | item definition index |

Code:

```text
local nDefinitionIndex = pWeapon:GetItemDefinitionIndex()
```

### GetSpread

Returns:

| Type | Description |
| :--- | :--- |
| float | spread factor |

Code:

```text
local flSpread = pWeapon:GetSpread()
```

### GetInaccuracy

Returns:

| Type | Description |
| :--- | :--- |
| float | innacuracy factor |

Code:

```text
local flInaccuracy = pWeapon:GetInaccuracy()
```

### GetMaxTickbaseShift

Returns:

| Type | Description |
| :--- | :--- |
| int | maximal number of ticks can be shifted |

Code:

```text
local nMaxShift = pWeapon:GetMaxTickbaseShift()
```


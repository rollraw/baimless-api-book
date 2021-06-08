---
description: >-
  Base class of all entities, inherited into CBaseEntity, CBaseCombatWeapon
  classes
---

# icliententity

🚧 _API of this file is not finished yet and could be changed in any time_

## Functions

### GetRefEHandle

Returns:

| Type | Description |
| :--- | :--- |
| CBaseHandle | reference of current entity handle |

Code:

```lua
local hHandle = pEntity:GetRefEHandle()
```

### GetRenderOrigin

Returns:

| Type | Description |
| :--- | :--- |
| [Vector](../datatypes/vector.md) | render origin |

Code:

```lua
local vecRenderOrigin = pEntity:GetRenderOrigin()
```

### GetRenderAngles

Returns:

| Type | Description |
| :--- | :--- |
| [QAngle](../datatypes/qangle.md) | render view point |

Code:

```lua
local angRenderViewPoint = pEntity:GetRenderAngles()
```

### IsDormant

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if entity have dormancy |

Code:

```lua
local bIsDormant = pEntity:IsDormant()
```

### GetIndex

Returns:

| Type | Description |
| :--- | :--- |
| int | entity index |

Code:

```lua
local nIndex = pEntity:GetIndex()
```

### GetAbsOrigin

Returns:

| Type | Description |
| :--- | :--- |
| [Vector](../datatypes/vector.md) | absolute origin |

Code:

```lua
local vecAbsOrigin = pEntity:GetAbsOrigin()
```

### GetAbsAngles

Returns:

| Type | Description |
| :--- | :--- |
| [QAngle](../datatypes/qangle.md) | absolute view point |

Code:

```lua
local angAbsViewPoint = pEntity:GetAbsAngles()
```

### SetAbsOrigin

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecAbsOrigin | [Vector](../datatypes/vector.md) | absolute origin to set |

Code:

```lua
pEntity:SetAbsOrigin(Vector.new(0.0, 0.0, 0.0))
```

### SetAbsAngles

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| angAbsViewPoint | [QAngle](../datatypes/qangle.md) | absolute angles to set |

Code:

```lua
pEntity:SetAbsAngles(QAngle.new(0.0, 0.0, 0.0))
```

### SetModelIndex

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| nModelIndex | int | override model index to set |

Code:

### GetPropertyBool, GetPropertyInt, GetPropertyFloat, GetPropertyVector, GetPropertyVector2D, GetPropertyQAngle, GetPropertyHandle

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szNetwordVariable | string | class and network variable name to get |

Returns:

| Type | Description |
| :--- | :--- |
| bool, int, float, [Vector](../datatypes/vector.md), [QAngle](../datatypes/qangle.md), CBaseHandle | value of given network variable in networked data table \(class\), type depends by function |

Code:

```lua
local bSpotted = pEntity:GetPropertyBool("CBaseEntity->m_bSpotted")
local iArmor = pLocal:GetPropertyInt("CCSPlayer->m_ArmorValue")
local flAnimationTime = pLocal:GetPropertyFloat("CBaseEntity->m_flAnimTime")
local angRotation = pEntity:GetPropertyQAngle("CBaseEntity->m_angRotation")
local vecMins = pEntity:GetPropertyVector("CBaseEntity->m_vecMins")
local hOwner = pEntity:GetPropertyHandle("CBaseEntity->m_hOwnerEntity")
```

### SetPropertyBool, SetPropertyInt, SetPropertyFloat, SetPropertyVector, SetPropertyVector2D, SetPropertyQAngle, SetPropertyHandle

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szNetwordVariable | string | class and network variable name to set |
| value | bool, int, float, [Vector](../datatypes/vector.md), [QAngle](../datatypes/qangle.md), CBaseHandle | value to set for given network variable in networked data table \(class\), type depends by function |

Code:

```lua
pEntity:SetPropertyBool("CBaseEntity->m_bSpotted", true)
pLocal:GetPropertyInt("CCSPlayer->m_ArmorValue", 100)
pLocal:GetPropertyFloat("CBaseEntity->m_flAnimTime", 0.0)
pEntity:GetPropertyQAngle("CBaseEntity->m_angRotation", QAngle.new())
pEntity:GetPropertyVector("CBaseEntity->m_vecMins", Vector.new())
pEntity:GetPropertyHandle("CBaseEntity->m_hOwnerEntity", 0)
```


---
description: >-
  Base class of all entities, inherited into CBaseEntity, CBaseCombatWeapon
  classes
---

# icliententity

> Description: base class of all entities, inherited into [CBaseEntity](cbaseentity.md), [CBaseCombatWeapon](cbasecombatweapon.md) classes

🚧 _API of this file is not finished yet and could be changed in any time_

:construction: _API of this file is not finished yet and could be changed in any time_

## Functions

## Functions

### GetRefEHandle

Returns:

| Type | Description |
| :--- | :--- |
| CBaseHandle | reference of current entity handle |

Code:

```text
local hHandle = pEntity:GetRefEHandle()
```

### GetRenderOrigin

Returns:

| Type | Description |
| :--- | :--- |
| Vector | render origin |

Code:

```text
local vecRenderOrigin = pEntity:GetRenderOrigin()
```

### GetRenderAngles

Returns:

| Type | Description |
| :--- | :--- |
| QAngle | render view point |

Code:

```text
local angRenderViewPoint = pEntity:GetRenderAngles()
```

### IsDormant

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if entity have dormancy |

Code:

```text
local bIsDormant = pEntity:IsDormant()
```

### GetIndex

Returns:

| Type | Description |
| :--- | :--- |
| int | entity index |

Code:

```text
local nIndex = pEntity:GetIndex()
```

### GetAbsOrigin

Returns:

| Type | Description |
| :--- | :--- |
| Vector | absolute origin |

Code:

```text
local vecAbsOrigin = pEntity:GetAbsOrigin()
```

### GetAbsAngles

Returns:

| Type | Description |
| :--- | :--- |
| QAngle | absolute view point |

Code:

```text
local angAbsViewPoint = pEntity:GetAbsAngles()
```

### SetAbsOrigin

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecAbsOrigin | Vector | absolute origin to set |

Code:

```text
pEntity:SetAbsOrigin(Vector.new(0.0, 0.0, 0.0))
```

### SetAbsAngles

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| angAbsViewPoint | QAngle | absolute angles to set |

Code:

```text
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
| bool, int, float, [Vector](https://github.com/rollraw/baimless-lua-api/blob/master/doc/datatypes/vector.md), [QAngle](https://github.com/rollraw/baimless-lua-api/blob/master/doc/datatypes/qangle.md), CBaseHandle | value of given network variable in networked data table \(class\), type depends on function |

Code:

```text
local bSpotted = pEntity:GetPropertyBool("CBaseEntity->m_bSpotted")
local iArmor = pLocal:GetPropertyInt("CCSPlayer->m_ArmorValue")
local flAnimationTime = pLocal:GetPropertyFloat("CBaseEntity->m_flAnimTime")
local angRotation = pEntity:GetPropertyVector("CBaseEntity->m_angRotation")
local vecMins = pEntity:GetPropertyVector("CBaseEntity->m_vecMins")
local hOwner = pEntity:GetPropertyHandle("CBaseEntity->m_hOwnerEntity")
```

### SetPropertyBool, SetPropertyInt, SetPropertyFloat, SetPropertyVector, SetPropertyVector2D, SetPropertyQAngle, SetPropertyHandle

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| szNetwordVariable | string | class and network variable name to set |
| value | bool, int, float, [Vector](https://github.com/rollraw/baimless-lua-api/blob/master/doc/datatypes/vector.md), [QAngle](https://github.com/rollraw/baimless-lua-api/blob/master/doc/datatypes/qangle.md), CBaseHandle | value to set for given network variable in networked data table \(class\), type depends on function |

Code:

```text
pEntity:SetPropertyBool("CBaseEntity->m_bSpotted", true)
pLocal:GetPropertyInt("CCSPlayer->m_ArmorValue", 100)
pLocal:GetPropertyFloat("CBaseEntity->m_flAnimTime", 0.0)
pEntity:GetPropertyVector("CBaseEntity->m_angRotation", QAngle.new())
pEntity:GetPropertyVector("CBaseEntity->m_vecMins", Vector.new())
pEntity:GetPropertyHandle("CBaseEntity->m_hOwnerEntity", 0)
```


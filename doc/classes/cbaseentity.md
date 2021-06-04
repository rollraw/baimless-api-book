---
description: IClientEntity is base class
---

# cbaseentity

## Enumerations

### EMoveType

| Indentificators |
| :--- |
| MOVETYPE\_NONE |
| MOVETYPE\_ISOMETRIC |
| MOVETYPE\_WALK |
| MOVETYPE\_STEP |
| MOVETYPE\_FLY |
| MOVETYPE\_FLYGRAVITY |
| MOVETYPE\_VPHYSICS |
| MOVETYPE\_PUSH |
| MOVETYPE\_NOCLIP |
| MOVETYPE\_LADDER |
| MOVETYPE\_OBSERVER |

## Functions

### GetLocalPlayer

ℹ **Note:** `GetLocalPlayer()` is static class member function constructing color, it doesn't requires to call `.new()`

Returns:

| Type | Description |
| :--- | :--- |
| CBaseEntity | local player entity |

Code:

```lua
local pLocal = CBaseEntity.GetLocalPlayer()
```

### GetWeapon

Returns:

| Type | Description |
| :--- | :--- |
| [CBaseCombatWeapon](cbasecombatweapon.md) | active weapon entity |

Code:

```lua
local pWeapon = pLocal:GetWeapon()
```

### GetSequenceActivity

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| iSequence | int | index of sequence to get activity of |

Returns:

| Type | Description |
| :--- | :--- |
| int | sequence activity |

Code:

```lua
local iActivity = pLocal:GetSequenceActivity()
```

### IsAlive

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if entity's lifestate equals alive |

Code:

```lua
local bIsAlive = pLocal:IsAlive()
```

### IsPlayer

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if entity is player |

Code:

```lua
local bIsPlayer = pLocal:IsPlayer()
```

### IsEnemy

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| pEntity | CBaseEntity | entity to check for enmity with current entity |

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if given entity is enemy for current entity |

Code:

```lua
local bIsEnemy = pLocal:IsEnemy(pEntity)
```

### IsVisible

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| pEntity | CBaseEntity | entity to check for visibility with current entity |
| vecEnd | [Vector](../datatypes/vector.md) | end position of visibility check |
| bSmokeCheck | bool | additional check is line goes through smoke |

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if given entity is visible for current entity |

Code:

```lua
local bIsVisible = pLocal:IsVisible(pEntity, pEntity:BonePosition(8), true)
```

### GetSimulationTime

Returns:

| Type | Description |
| :--- | :--- |
| float | time when entity was in simulation |

Code:

```lua
local flSimulationTime = pLocal:GetSimulationTime()
```

### GetOldSimulationTime

Returns:

| Type | Description |
| :--- | :--- |
| float | previous time when entity was in simulation |

Code:

```lua
local flOldSimulationTime = pLocal:GetOldSimulationTime()
```

### GetSpawnTime

Returns:

| Type | Description |
| :--- | :--- |
| float | time point when player was spawned |

Code:

```lua
local flSpawnTime = pLocal:GetSpawnTime()
```

### GetMoveType

Returns:

| Type | Description |
| :--- | :--- |
| [int](cbaseentity.md#emovetype) | current type of entity movement |

Code:

```lua
local nMoveType = pLocal:GetMoveType()
```

### GetEyePosition

Returns:

| Type | Description |
| :--- | :--- |
| [Vector](../datatypes/vector.md) | eye position origin in world space |

Code:

```lua
local vecEyePosition = pLocal:GetEyePosition()
```

### GetBonePosition

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| iBone | int | index of bone you want get position of |

Returns:

| Type | Description |
| :--- | :--- |
| [Vector](../datatypes/vector.md) | bone origin in world space |

Code:

```lua
local vecHeadOrigin = pLocal:GetBonePosition(8)
```

### GetHitGroupPosition

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| iHitGroup | int | index of hitgroup you want get position of |

Returns:

| Type | Description |
| :--- | :--- |
| [Vector](../datatypes/vector.md) | hitgroup origin in world space |

Code:

```lua
local vecHeadOrigin = pLocal:GetHitGroupPosition(1)
```


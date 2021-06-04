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

Returns:

| Type | Description |
| :--- | :--- |
| CBaseEntity | local player entity |

Code:

```text
local pLocal = CBaseEntity.GetLocalPlayer()
```

### GetWeapon

Returns:

| Type | Description |
| :--- | :--- |
| CBaseCombatWeapon | active weapon entity |

Code:

```text
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

```text
local iActivity = pLocal:GetSequenceActivity()
```

### IsAlive

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if entity's lifestate equals alive |

Code:

```text
local bIsAlive = pLocal:IsAlive()
```

### IsPlayer

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if entity is player |

Code:

```text
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

```text
local bIsEnemy = pLocal:IsEnemy(pEntity)
```

### IsVisible

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| pEntity | CBaseEntity | entity to check for visibility with current entity |
| vecEnd | Vector | end position of visibility check |
| bSmokeCheck | bool | additional check is line goes through smoke |

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if given entity is visible for current entity |

Code:

```text
local bIsVisible = pLocal:IsVisible(pEntity, pEntity:BonePosition(8), true)
```

### GetSimulationTime

Returns:

| Type | Description |
| :--- | :--- |
| float | time when entity was in simulation |

Code:

```text
local flSimulationTime = pLocal:GetSimulationTime()
```

### GetOldSimulationTime

Returns:

| Type | Description |
| :--- | :--- |
| float | previous time when entity was in simulation |

Code:

```text
local flOldSimulationTime = pLocal:GetOldSimulationTime()
```

### GetSpawnTime

Returns:

| Type | Description |
| :--- | :--- |
| float | time point when player was spawned |

Code:

```text
local flSpawnTime = pLocal:GetSpawnTime()
```

### GetMoveType

Returns:

| Type | Description |
| :--- | :--- |
| [int]() | current type of entity movement |

Code:

```text
local nMoveType = pLocal:GetMoveType()
```

### GetEyePosition

Returns:

| Type | Description |
| :--- | :--- |
| Vector | eye position origin in world space |

Code:

```text
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
| Vector | bone origin in world space |

Code:

```text
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
| Vector | hitgroup origin in world space |

Code:

```text
local vecHeadOrigin = pLocal:GetHitGroupPosition(1)
```


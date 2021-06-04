# ientitylist

## Functions

### GetClientEntity

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| nIndex | int | index of entity to get |

Returns:

| Type | Description |
| :--- | :--- |
| IClientEntity\* | entity pointer of given index |

Code:

```text
local pLocal = IEntityList.GetClientEntity(IEngine.GetLocalPlayer())
```

### GetClientEntityFromHandle

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| hHandle | CBaseHandle | handle of entity to get |

Returns:

| Type | Description |
| :--- | :--- |
| IClientEntity\* | entity pointer of given handle |

Code:

```text
local pLocalWeapon = IEntityList.GetClientEntity(pLocal.GetWeaponHandle())
```

### GetHighestEntityIndex

Returns:

| Type | Description |
| :--- | :--- |
| int | highest entity index |

Code:

```text
local nHighestEntityIndex = IEntityList.GetHighestEntityIndex()
```


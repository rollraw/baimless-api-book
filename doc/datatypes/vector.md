# vector

## Variables

| Name | Type |
| :--- | :--- |
| x | float |
| y | float |
| z | float |

## Functions

### IsZero

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if all vector axes equals zero |

Code:

```lua
local vecZero = Vector.new(0.0, 0.0, 0.0)
local bIsZero = vecZero.IsZero()
```

### IsValid

Returns:

| Type | Description |
| :--- | :--- |
| bool | true if all vector axes is finite |

Code:

```lua
local vecValid = Vector.new(1.0, 1.0, 1.0)
local bIsValid = vecValid.IsValid()
```

### Length

Returns:

| Type | Description |
| :--- | :--- |
| float | length of current vector |

Code:

```lua
local vecTest = Vector.new(100.0, 100.0, 100.0)
local flLength = vecTest.Length()
```

### LengthSqr

Returns:

| Type | Description |
| :--- | :--- |
| float | squared length of current vector |

Code:

```lua
local vecTest = Vector.new(100.0, 100.0, 100.0)
local flSquaredLength = vecTest.LengthSqr()
```

### Length2D

Returns:

| Type | Description |
| :--- | :--- |
| float | length of current vector, only `x` and `y` axes |

Code:

```lua
local vecTest = Vector.new(100.0, 100.0, 100.0)
local flLength2D = vecTest.Length2D()
```

### Length2DSqr

Returns:

| Type | Description |
| :--- | :--- |
| float | squared length of current vector, only `x` and `y` axes |

Code:

```lua
local vecTest = Vector.new(100.0, 100.0, 100.0)
local flSquaredLength2D = vecTest.Length2DSqr()
```

### DistTo

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecEnd | Vector | end point to calculate distance from current vector |

Returns:

| Type | Description |
| :--- | :--- |
| float | distance between current and given vector |

Code:

```lua
local vecStart = Vector.new(100.0, 100.0, 100.0)
local vecEnd = Vector.new(200.0, 200.0, 200.0)
local flDist = vecStart.DistTo(vecEnd)
```

### DistToSqr

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecEnd | Vector | end point to calculate distance from current vector |

Returns:

| Type | Description |
| :--- | :--- |
| float | squared distance between current and given vector |

Code:

```lua
local vecStart = Vector.new(100.0, 100.0, 100.0)
local vecEnd = Vector.new(200.0, 200.0, 200.0)
local flDistSqr = vecStart.DistToSqr(vecEnd)
```

### DotProduct

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecDot | Vector | point to calculate dot of current vector with |

Returns:

| Type | Description |
| :--- | :--- |
| Vector | dot product of current and given vectors |

Code:

```lua
local vecToDot = Vector.new(100.0, 100.0, 100.0)
local vecDot = Vector.new(200.0, 200.0, 200.0)
local vecDotProduct = vecToDot.CrossProduct(vecDot)
```

### CrossProduct

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecCross | Vector | point to calculate cross of current vector with |

Returns:

| Type | Description |
| :--- | :--- |
| Vector | cross product of current and given vectors |

Code:

```lua
local vecToCross = Vector.new(100.0, 100.0, 100.0)
local vecCross = Vector.new(200.0, 200.0, 200.0)
local vecCrossProduct = vecToCross.CrossProduct(vecCross)
```

### Normalized

Returns:

| Type | Description |
| :--- | :--- |
| Vector | normalized to legit values vector |

Code:

```lua
local vecTest = Vector.new(0.025, 0.025, 0.025)

-- create a copy of vecTest, then NormalizeInPlace it and assign normalized vector to copied vector
local vecNormalized = vecTest.Normalized() 
```

### NormalizeInPlace

Returns:

| Type | Description |
| :--- | :--- |
| float | lenght of vector |

Code:

```lua
local vecTest = Vector.new(0.025, 0.025, 0.025)
local flLenght = vecTest.NormalizeInPlace()
```


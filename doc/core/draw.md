---
description: Functions for drawing primitives. Usually won't work outside the `Paint` event
---

# draw

## Enumerations

### ECornerRenderFlags

Description: rounding corners render flags for all function with `roundingCorners` argument, requires `flRounding` greater than 0.0

⚠️ **Warning:** `ALL` cannot be used with other flags

| Indentifiers |
| :--- |
| NONE |
| TOP\_LEFT |
| TOP\_RIGHT |
| BOTTOM\_LEFT |
| BOTTOM\_RIGHT |
| ALL |

### ERectRenderFlags

Description: render flags for [AddRect\(\)](draw.md#addrect)

| Indentifiers |
| :--- |
| DRAW\_RECT\_NONE |
| DRAW\_RECT\_OUTLINE |
| DRAW\_RECT\_BORDER |
| DRAW\_RECT\_FILLED |

### EBox3DRenderFlags

Description: render flags for [AddBox3D\(\)](draw.md#addbox-3-d)

| Indentifiers |
| :--- |
| DRAW\_BOX3D\_NONE |
| DRAW\_BOX3D\_OUTLINE |
| DRAW\_BOX3D\_FILLED |

### ECircleRenderFlags

Description: render flags for [AddCircle\(\)](draw.md#addcircle)

| Indentifiers |
| :--- |
| DRAW\_CIRCLE\_NONE |
| DRAW\_CIRCLE\_OUTLINE |
| DRAW\_CIRCLE\_FILLED |

### ECircle3DRenderFlags

Description: render flags for [AddCircle3D\(\)](draw.md#addcircle-3-d)

| Indentifiers |
| :--- |
| DRAW\_CIRCLE3D\_NONE |
| DRAW\_CIRCLE3D\_OUTLINE |
| DRAW\_CIRCLE3D\_FILLED |
| DRAW\_CIRCLE3D\_DOTTED |

### ETriangleRenderFlags

Description: render flags for [AddTriangle\(\)](draw.md#addtriangle)

| Indentifiers |
| :--- |
| DRAW\_TRIANGLE\_NONE |
| DRAW\_TRIANGLE\_OUTLINE |
| DRAW\_TRIANGLE\_FILLED |

### EQuadRenderFlags

Description: render flags for [AddQuad\(\)](draw.md#addquad)

| Indentifiers |
| :--- |
| DRAW\_QUAD\_NONE |
| DRAW\_QUAD\_OUTLINE |
| DRAW\_QUAD\_FILLED |

### EPolygonRenderFlags

Description: render flags for [AddPolygon\(\)](draw.md#addpolygon)

| Indentifiers |
| :--- |
| DRAW\_POLYGON\_NONE |
| DRAW\_POLYGON\_OUTLINE |
| DRAW\_POLYGON\_FILLED |

### ETextRenderFlags

Description: render flags for [AddText\(\)](draw.md#addtext)

⚠️ **Warning:** `DRAW_TEXT_DROPSHADOW` and `DRAW_TEXT_OUTLINE` flags cannot be used together

| Indentifiers |
| :--- |
| DRAW\_TEXT\_NONE |
| DRAW\_TEXT\_DROPSHADOW |
| DRAW\_TEXT\_OUTLINE |

### ERasterizerFlags

Description: rasterizer flags for [AddFont\(\)](draw.md#addfont)

| Indentifiers |
| :--- |
| NO\_HINTING |
| NO\_AUTOHINT |
| FORCE\_AUTOHINT |
| LIGHT\_HINTING |
| MONO\_HINTING |
| BOLD |
| OBLIQUE |
| MONOCHROME |

## Functions

### WorldToScreen

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecWorldOrigin | [Vector](../datatypes/vector.md) | position in world space |

Returns:

| Type | Description |
| :--- | :--- |
| [Vector2D](../datatypes/vector2d.md) | position of given world space in screen space |

Code:

```lua
local vecLocalOrigin = pLocal.GetOrigin()
local vecScreen = Draw.WorldToScreen(vecLocalOrigin)
```

### AddLine

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecStart | [Vector2D](../datatypes/vector2d.md) | start position of line |
| vecEnd | [Vector2D](../datatypes/vector2d.md) | end position of line |
| colLine | [Color](../datatypes/color.md) | color of line |
| _flThickness_ | float | thickness of line |

Code:

```lua
Draw.AddLine(Vector2D.new(100.0, 100.0), Vector2D.new(200.0, 100.0), Color.new(), 2.0)
```

### AddRect

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecMin | [Vector2D](../datatypes/vector2d.md) | minimal position of rect |
| vecMax | [Vector2D](../datatypes/vector2d.md) | maximal position of rect |
| colRect | [Color](../datatypes/color.md) | color of rect |
| \_\_[_uFlags_](draw.md#erectrenderflags)\_\_ | [bitflag](https://en.wiktionary.org/wiki/bitflag) | render flags |
| _colOutline_ | [Color](../datatypes/color.md) | color of outline |
| _flRounding_ | float | corners rounding value |
| \_\_[_roundingCorners_](draw.md#ecornerrenderflags)\_\_ | [bitflag](https://en.wiktionary.org/wiki/bitflag) | rounding corners render flags |
| _flThickness_ | float | thickness of non-filled rect / outline of filled rect |

Code:

```lua
local bit = require("bit")
Draw.AddRect(Vector2D.new(100.0, 100.0), Vector2D.new(200.0, 200.0), Color.new(), bit.bor(ERectRenderFlags.DRAW_RECT_OUTLINE, ERectRenderFlags.DRAW_RECT_BORDER), Color.new(100, 0, 0, 255), 15.0)
```

### AddRectMultiColor

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecMin | [Vector2D](../datatypes/vector2d.md) | minimal position of rect |
| vecMax | [Vector2D](../datatypes/vector2d.md) | maximal position of rect |
| colUpperLeft | [Color](../datatypes/color.md) | color of upper-left corner of rect |
| colUpperRight | [Color](../datatypes/color.md) | color of upper-right corner of rect |
| colBottomRight | [Color](../datatypes/color.md) | color of bottom-right corner of rect |
| colBottomLeft | [Color](../datatypes/color.md) | color of bottom-left corner of rect |

Code:

```lua
Draw.AddRectMultiColor(Vector2D.new(100.0, 100.0), Vector2D.new(200.0, 200.0), Color.new(0, 150, 200), Color.new(100, 150, 0), Color.new(0, 200, 0), Color.new(180, 0, 0))
```

### AddBox3D

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecCenter | [Vector](../datatypes/vector.md) | center position of 3D box in world space |
| vecAbsMin | [Vector](../datatypes/vector.md) | absolute minimal 3D box expansion |
| vecAbsMax | [Vector](../datatypes/vector.md) | absolute maximal 3D box expansion |
| angOrientation | [QAngle](../datatypes/qangle.md) | angle of 3D box rotation |
| colBox | [Color](../datatypes/color.md) | color of 3D box |
| \_\_[_uFlags_](draw.md#ebox-3-drenderflags)\_\_ | [bitflag](https://en.wiktionary.org/wiki/bitflag) | render flags |
| _colOutline_ | [Color](../datatypes/color.md) | color of outline |
| _flThickness_ | float | thickness of non-filled 3D box / outline of filled 3D box |

Code:

```lua
Draw.AddBox(Vector.new(150.0, 150.0, 150.0), Vector.new(-2.0, -2.0, -2.0), Vector.new(2.0, 2.0, 2.0), QAngle.new(), Color.new(), EBox3DRenderFlags.DRAW_BOX3D_FILLED)
```

### AddCircle

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecCenter | [Vector2D](../datatypes/vector2d.md) | center position of circle |
| flRadius | float | radius of circle |
| colCircle | [Color](../datatypes/color.md) | color of circle |
| nSegments | int | segments count for circle |
| \_\_[_uFlags_](draw.md#ecirclerenderflags)\_\_ | [bitflag](https://en.wiktionary.org/wiki/bitflag) | render flags |
| _colOutline_ | [Color](../datatypes/color.md) | color of outline |
| _flThickness_ | float | thickness of non-filled circle / outline of filled circle |

Code:

```lua
local bit = require("bit")
Draw.AddCircle(Vector2D.new(150.0, 150.0), 50.0, Color.new(), 12, bit.bor(ECircleRenderFlags.DRAW_CIRCLE_FILLED, ECircleRenderFlags.DRAW_CIRCLE_OUTLINE))
```

### AddCircle3D

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecCenter | [Vector](../datatypes/vector.md) | center position of 3D circle in world space |
| flRadius | float | radius of 3D circle |
| colCircle | [Color](../datatypes/color.md) | color of 3D circle |
| nSegments | int | segments count for 3D circle |
| \_\_[_uFlags_](draw.md#ecircle-3-drenderflags)\_\_ | [bitflag](https://en.wiktionary.org/wiki/bitflag) | render flags |
| _colOutline_ | [Color](../datatypes/color.md) | color of outline |
| _flThickness_ | float | thickness of non-filled 3D circle / outline of filled 3D circle |

Code:

```lua
Draw.AddCircle3D(pLocal.GetOrigin(), 50.0, Color.new(), 36, ECircle3DRenderFlags.DRAW_CIRCLE3D_DOTTED)
```

### AddTriangle

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecFirst | [Vector2D](../datatypes/vector2d.md) | first position of triangle |
| vecSecond | [Vector2D](../datatypes/vector2d.md) | second position of triangle |
| vecThird | [Vector2D](../datatypes/vector2d.md) | third position of triangle |
| colTriangle | [Color](../datatypes/color.md) | color of triangle |
| \_\_[_uFlags_](draw.md#etrianglerenderflags)\_\_ | [bitflag](https://en.wiktionary.org/wiki/bitflag) | render flags |
| _colOutline_ | [Color](../datatypes/color.md) | color of outline |
| _flThickness_ | float | thickness of non-filled triangle / outline of filled triangle |

Code:

```lua
Draw.AddTriangle(Vector2D.new(150.0, 100.0), Vector2D.new(100.0, 200.0), Vector2D.new(200.0, 200.0), Color.new())
```

### AddQuad

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecFirst | [Vector2D](../datatypes/vector2d.md) | first position of quad |
| vecSecond | [Vector2D](../datatypes/vector2d.md) | second position of quad |
| vecThird | [Vector2D](../datatypes/vector2d.md) | third position of quad |
| vecFourth | [Vector2D](../datatypes/vector2d.md) | fourth position of quad |
| colQuad | [Color](../datatypes/color.md) | color of quad |
| \_\_[_uFlags_](draw.md#equadrenderflags)\_\_ | [bitflag](https://en.wiktionary.org/wiki/bitflag) | render flags |
| _colOutline_ | [Color](../datatypes/color.md) | color of outline |
| _flThickness_ | float | thickness of non-filled quad / outline of filled quad |

Code:

```lua
Draw.AddTriangle(Vector2D.new(150.0, 100.0), Vector2D.new(100.0, 200.0), Vector2D.new(200.0, 200.0), Color.new(), EQuadRenderFlags.DRAW_QUAD_OUTLINE)
```

### AddArc

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecCenter | [Vector2D](../datatypes/vector2d.md) | center position of arc |
| flRadius | float | radius of arc |
| vecAngleRange | [Vector2D](../datatypes/vector2d.md) | minimal and maximal angles of arc |
| colArc | [Color](../datatypes/color.md) | color of arc |
| flThickness | float | thickness of arc |

Code:

```lua
Draw.AddArc(Vector2D.new(150.0, 150.0), 50.0, Vector2D.new(-45.0, 45.0), Color.new(), 2.0)
```

### AddPolygon

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecPoints | table | polygon positions |
| colPolygon | [Color](../datatypes/color.md) | color of polygon |
| \_\_[_uFlags_](draw.md#epolygonrenderflags)\_\_ | [bitflag](https://en.wiktionary.org/wiki/bitflag) | render flags |
| _colOutline_ | [Color](../datatypes/color.md) | color of outline |
| _bClosed_ | bool | if true after last point will be automatically added first point |
| _flThickness_ | float | thickness of non-filled polygon / outline of filled polygon |

Code:

```lua
Draw.AddPolygon({ Vector2D.new(150.0, 100.0), Vector2D.new(140.0, 120.0), Vector2D.new(110.0, 140.0), Vector2D.new(140.0, 160.0), Vector2D.new(150.0, 180.0) }, Color.new(), EPolygonRenderFlags.DRAW_POLYGON_OUTLINE)
```

### AddFont

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecPoints | string | path to font file \(.ttf / .otf\) |
| flFontSize | float | size of font in pixels |
| \_\_[_uFlags_](draw.md#erasterizerflags)\_\_ | [bitflag](https://en.wiktionary.org/wiki/bitflag) | rasterizer flags |

Returns:

| Type | Description |
| :--- | :--- |
| uint32 | hash of added font |

Code:

```lua
local uSeguiUI = Draw.AddFont("C:\\Windows\\Fonts\\seguiui.ttf", 20.0, ERasterizerFlags.BOLD)
```

### RemoveFont

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| uFontHash | uint32 | hash of font that will be removed |

Code:

```lua
Client.RegisterCallback("Destroy", function()
Draw.RemoveFont(uSeguiUI)
end)
```

### GetTextSize

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| uFontHash | uint32 | hash of font for will be calculated size |
| flFontSize | float | size of font in pixels |
| szText | string | text for will be calculated size |

Returns:

| Type | Description |
| :--- | :--- |
| [Vector2D](../datatypes/vector2d.md) | size for given font with given text |

Code:

```lua
local vecTextSize = Draw.GetTextSize(uSeguiUI, 20.0, "Test")
```

### AddText

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| uFontHash | uint32 | hash of font text will be rendered with |
| flFontSize | float | size of font in pixels |
| vecPosition | [Vector2D](../datatypes/vector2d.md) | left-top corner position of text |
| szText | string | text to render by given font hash |
| colText | [Color](../datatypes/color.md) | color of text |
| \_\_[_uFlags_](draw.md#etextrenderflags)\_\_ | [bitflag](https://en.wiktionary.org/wiki/bitflag) | render flags |
| _colOutline_ | [Color](../datatypes/color.md) | color of outline |
| _flThickness_ | float | thickness of outlined text |

Code:

```lua
Draw.AddText(uSeguiUI, 20.0, Vector2D.new(150.0, 150.0) - vecTextSize * 0.5, Color.new(), "Test", ETextRenderFlags.DRAW_TEXT_OUTLINE)
```


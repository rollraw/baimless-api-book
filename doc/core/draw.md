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

Description: render flags for `AddRect()`

| Indentifiers |
| :--- |
| DRAW\_RECT\_NONE |
| DRAW\_RECT\_OUTLINE |
| DRAW\_RECT\_BORDER |
| DRAW\_RECT\_FILLED |

### ECircleRenderFlags

Description: render flags for `AddCircle()`

| Indentifiers |
| :--- |
| DRAW\_CIRCLE\_NONE |
| DRAW\_CIRCLE\_OUTLINE |
| DRAW\_CIRCLE\_FILLED |

### ECircle3DRenderFlags

Description: render flags for `AddCircle3D()`

| Indentifiers |
| :--- |
| DRAW\_CIRCLE3D\_NONE |
| DRAW\_CIRCLE3D\_OUTLINE |
| DRAW\_CIRCLE3D\_FILLED |
| DRAW\_CIRCLE3D\_DOTTED |

### ETriangleRenderFlags

Description: render flags for `AddTriangle()`

| Indentifiers |
| :--- |
| DRAW\_TRIANGLE\_NONE |
| DRAW\_TRIANGLE\_OUTLINE |
| DRAW\_TRIANGLE\_FILLED |

### EQuadRenderFlags

Description: render flags for `AddQuad()`

| Indentifiers |
| :--- |
| DRAW\_QUAD\_NONE |
| DRAW\_QUAD\_OUTLINE |
| DRAW\_QUAD\_FILLED |

### EPolygonRenderFlags

Description: render flags for `AddPolygon()`

| Indentifiers |
| :--- |
| DRAW\_POLYGON\_NONE |
| DRAW\_POLYGON\_OUTLINE |
| DRAW\_POLYGON\_FILLED |

### ETextRenderFlags

Description: render flags for `AddText()`

⚠️ **Warning:** `DRAW_TEXT_DROPSHADOW` and `DRAW_TEXT_OUTLINE` flags cannot be used together

| Indentifiers |
| :--- |
| DRAW\_TEXT\_NONE |
| DRAW\_TEXT\_DROPSHADOW |
| DRAW\_TEXT\_OUTLINE |

### ERasterizerFlags

Description: rasterizer flags for `AddFont()`

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
| vecWorldOrigin | Vector | position in world space |

Returns:

| Type | Description |
| :--- | :--- |
| Vector2D | position of given world space in screen space |

Code:

```text
local vecLocalOrigin = pLocal.GetOrigin()
local vecScreen = Draw.WorldToScreen(vecLocalOrigin)
```

### AddLine

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecStart | Vector2D | start position of line |
| vecEnd | Vector2D | end position of line |
| colLine | Color | color of line |
| _flThickness_ | float | thickness of line |

Code:

```text
Draw.AddLine(Vector2D.new(100.0, 100.0), Vector2D.new(200.0, 100.0), Color.new(), 2.0)
```

### AddRect

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecMin | Vector2D | minimal position of rect |
| vecMax | Vector2D | maximal position of rect |
| colRect | Color | color of rect |
| [_uFlags_]() | [bitflag](https://en.wiktionary.org/wiki/bitflag) | render flags |
| [_colOutline_]() | Color | color of outline |
| [_flRounding_]() | float | corners rounding value |
| [_roundingCorners_]() | [bitflag](https://en.wiktionary.org/wiki/bitflag) | rounding corners render flags |
| [_flThickness_]() | float | thickness of non-filled rect / outline of filled rect |

Code:

```text
local bit = require("bit")
Draw.AddRect(Vector2D.new(100.0, 100.0), Vector2D.new(200.0, 200.0), Color.new(), bit.bor(ERectRenderFlags.DRAW_RECT_OUTLINE, ERectRenderFlags.DRAW_RECT_BORDER), Color.new(100, 0, 0, 255), 15.0)
```

### AddRectMultiColor

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecMin | Vector2D | minimal position of rect |
| vecMax | Vector2D | maximal position of rect |
| colUpperLeft | Color | color of upper-left corner of rect |
| colUpperRight | Color | color of upper-right corner of rect |
| colBottomRight | Color | color of bottom-right corner of rect |
| colBottomLeft | Color | color of bottom-left corner of rect |

Code:

```text
Draw.AddRectMultiColor(Vector2D.new(100.0, 100.0), Vector2D.new(200.0, 200.0), Color.new(0, 150, 200), Color.new(100, 150, 0), Color.new(0, 200, 0), Color.new(180, 0, 0))
```

### AddCircle

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecCenter | Vector2D | center position of circle |
| flRadius | float | radius of circle |
| colCircle | Color | color of circle |
| nSegments | int | segments count for circle |
| [_uFlags_]() | [bitflag](https://en.wiktionary.org/wiki/bitflag) | render flags |
| [_colOutline_]() | Color | color of outline |
| [_flThickness_]() | float | thickness of non-filled circle / outline of filled circle |

Code:

```text
local bit = require("bit")
Draw.AddCircle(Vector2D.new(150.0, 150.0), 50.0, Color.new(), 12, bit.bor(ECircleRenderFlags.DRAW_CIRCLE_FILLED, ECircleRenderFlags.DRAW_CIRCLE_OUTLINE))
```

### AddCircle3D

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecCenter | Vector | center position of 3D circle in world space |
| flRadius | float | radius of 3D circle |
| colCircle | Color | color of 3D circle |
| nSegments | int | segments count for 3D circle |
| [_uFlags_]() | [bitflag](https://en.wiktionary.org/wiki/bitflag) | render flags |
| [_colOutline_]() | Color | color of outline |
| [_flThickness_]() | float | thickness of non-filled 3D circle / outline of filled 3D circle |

Code:

```text
Draw.AddCircle3D(pLocal.GetOrigin(), 50.0, Color.new(), 36, ECircle3DRenderFlags.DRAW_CIRCLE3D_DOTTED)
```

### AddTriangle

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecFirst | Vector2D | first position of triangle |
| vecSecond | Vector2D | second position of triangle |
| vecThird | Vector2D | third position of triangle |
| colTriangle | Color | color of triangle |
| [_uFlags_]() | [bitflag](https://en.wiktionary.org/wiki/bitflag) | render flags |
| [_colOutline_]() | Color | color of outline |
| [_flThickness_]() | float | thickness of non-filled triangle / outline of filled triangle |

Code:

```text
Draw.AddTriangle(Vector2D.new(150.0, 100.0), Vector2D.new(100.0, 200.0), Vector2D.new(200.0, 200.0), Color.new())
```

### AddQuad

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecFirst | Vector2D | first position of quad |
| vecSecond | Vector2D | second position of quad |
| vecThird | Vector2D | third position of quad |
| vecFourth | Vector2D | fourth position of quad |
| colQuad | Color | color of quad |
| [_uFlags_]() | [bitflag](https://en.wiktionary.org/wiki/bitflag) | render flags |
| [_colOutline_]() | Color | color of outline |
| [_flThickness_]() | float | thickness of non-filled quad / outline of filled quad |

Code:

```text
Draw.AddTriangle(Vector2D.new(150.0, 100.0), Vector2D.new(100.0, 200.0), Vector2D.new(200.0, 200.0), Color.new(), EQuadRenderFlags.DRAW_QUAD_OUTLINE)
```

### AddArc

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecCenter | Vector2D | center position of arc |
| flRadius | float | radius of arc |
| vecAngleRange | Vector2D | minimal and maximal angles of arc |
| colArc | Color | color of arc |
| flThickness | float | thickness of arc |

Code:

```text
Draw.AddArc(Vector2D.new(150.0, 150.0), 50.0, Vector2D.new(-45.0, 45.0), Color.new(), 2.0)
```

### AddPolygon

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecPoints | [table]() | polygon positions |
| colPolygon | Color | color of polygon |
| [_uFlags_]() | [bitflag](https://en.wiktionary.org/wiki/bitflag) | render flags |
| [_colOutline_]() | Color | color of outline |
| [_bClosed_]() | bool | if true after last point will be automatically added first point |
| [_flThickness_]() | float | thickness of non-filled polygon / outline of filled polygon |

Code:

```text
Draw.AddPolygon({ Vector2D.new(150.0, 100.0), Vector2D.new(140.0, 120.0), Vector2D.new(110.0, 140.0), Vector2D.new(140.0, 160.0), Vector2D.new(150.0, 180.0) }, Color.new(), EPolygonRenderFlags.DRAW_POLYGON_OUTLINE)
```

### AddFont

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| vecPoints | string | path to font file \(.ttf / .otf\) |
| flFontSize | float | size of font in pixels |
| [_uFlags_]() | [bitflag]() | rasterizer flags |

Returns:

| Type | Description |
| :--- | :--- |
| unsigned int | hash of added font |

Code:

```text
local uSeguiUI = Draw.AddFont("C:\\Windows\\Fonts\\seguiui.ttf", 20.0, ERasterizerFlags.BOLD)
```

### RemoveFont

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| uFontHash | unsigned int | hash of font that will be removed |

Code:

```text
Client.RegisterCallback("Destroy", function()
Draw.RemoveFont(uSeguiUI)
end)
```

### GetTextSize

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| uFontHash | unsigned int | hash of font for will be calculated size |
| flFontSize | float | size of font in pixels |
| szText | string | text for will be calculated size |

Returns:

| Type | Description |
| :--- | :--- |
| Vector2D | size for given font with given text |

Code:

```text
local vecTextSize = Draw.GetTextSize(uSeguiUI, 20.0, "Test")
```

### AddText

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| uFontHash | unsigned int | hash of font text will be rendered with |
| flFontSize | float | size of font in pixels |
| vecPosition | Vector2D | left-top corner position of text |
| szText | string | text to render by given font hash |
| colText | Color | color of text |
| [_uFlags_]() | [bitflag](https://en.wiktionary.org/wiki/bitflag) | render flags |
| [_colOutline_]() | Color | color of outline |
| [_flThickness_]() | float | thickness of outlined text |

Code:

```text
Draw.AddText(uSeguiUI, 20.0, Vector2D.new(150.0, 150.0) - vecTextSize * 0.5, Color.new(), "Test", ETextRenderFlags.DRAW_TEXT_OUTLINE)
```


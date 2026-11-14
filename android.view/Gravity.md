# Gravity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Gravity

Kotlin| [Java](Gravity.md) 
| --- | --- |

```
open class Gravity
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.Gravity](Gravity.md) |

Standard constants and tools for placing an object within a potentially larger container.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_CLIP](Gravity.md) Raw bit controlling whether the right/bottom edge is clipped to its container, based on the gravity direction being applied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_PULL_AFTER](Gravity.md) Raw bit controlling how the right/bottom edge is placed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_PULL_BEFORE](Gravity.md) Raw bit controlling how the left/top edge is placed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_SPECIFIED](Gravity.md) Raw bit indicating the gravity for an axis has been specified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_X_SHIFT](Gravity.md) Bits defining the horizontal axis. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AXIS_Y_SHIFT](Gravity.md) Bits defining the vertical axis. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BOTTOM](Gravity.md) Push object to the bottom of its container, not changing its size. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENTER](Gravity.md) Place the object in the center of its container in both the vertical and horizontal axis, not changing its size. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENTER_HORIZONTAL](Gravity.md) Place object in the horizontal center of its container, not changing its size. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENTER_VERTICAL](Gravity.md) Place object in the vertical center of its container, not changing its size. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLIP_HORIZONTAL](Gravity.md) Flag to clip the edges of the object to its container along the horizontal axis. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLIP_VERTICAL](Gravity.md) Flag to clip the edges of the object to its container along the vertical axis. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISPLAY_CLIP_HORIZONTAL](Gravity.md) Special constant to enable clipping to an overall display along the horizontal dimension. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISPLAY_CLIP_VERTICAL](Gravity.md) Special constant to enable clipping to an overall display along the vertical dimension. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [END](Gravity.md) Push object to x-axis position at the end of its container, not changing its size. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FILL](Gravity.md) Grow the horizontal and vertical size of the object if needed so it completely fills its container. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FILL_HORIZONTAL](Gravity.md) Grow the horizontal size of the object if needed so it completely fills its container. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FILL_VERTICAL](Gravity.md) Grow the vertical size of the object if needed so it completely fills its container. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HORIZONTAL_GRAVITY_MASK](Gravity.md) Binary mask to get the absolute horizontal gravity of a gravity. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LEFT](Gravity.md) Push object to the left of its container, not changing its size. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_GRAVITY](Gravity.md) Constant indicating that no gravity has been set \* |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIVE_HORIZONTAL_GRAVITY_MASK](Gravity.md) Binary mask for the horizontal gravity and script specific direction bit. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RELATIVE_LAYOUT_DIRECTION](Gravity.md) Raw bit controlling whether the layout direction is relative or not (START/END instead of absolute LEFT/RIGHT). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RIGHT](Gravity.md) Push object to the right of its container, not changing its size. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [START](Gravity.md) Push object to x-axis position at the start of its container, not changing its size. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOP](Gravity.md) Push object to the top of its container, not changing its size. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VERTICAL_GRAVITY_MASK](Gravity.md) Binary mask to get the vertical gravity of a gravity. |
| --- | --- |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------|---|
| [Gravity](Gravity.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [apply](Gravity.md))`(`gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `w:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `h:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `container:` ` [Rect](../android.graphics/Rect.md)!`, `outRect:` ` [Rect](../android.graphics/Rect.md)!`)` Apply a gravity constant to an object. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [apply](Gravity.md))`(`gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `w:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `h:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `container:` ` [Rect](../android.graphics/Rect.md)`, `outRect:` ` [Rect](../android.graphics/Rect.md)`, `layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Apply a gravity constant to an object and take care if layout direction is RTL or not. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [apply](Gravity.md))`(`gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `w:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `h:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `container:` ` [Rect](../android.graphics/Rect.md)`, `xAdj:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `yAdj:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `outRect:` ` [Rect](../android.graphics/Rect.md)`)` Apply a gravity constant to an object. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [apply](Gravity.md))`(`gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `w:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `h:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `container:` ` [Rect](../android.graphics/Rect.md)`, `xAdj:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `yAdj:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `outRect:` ` [Rect](../android.graphics/Rect.md)`, `layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Apply a gravity constant to an object. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyDisplay](Gravity.md))`(`gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `display:` ` [Rect](../android.graphics/Rect.md)`, `inoutObj:` ` [Rect](../android.graphics/Rect.md)`)` Apply additional gravity behavior based on the overall "display" that an object exists in. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyDisplay](Gravity.md))`(`gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `display:` ` [Rect](../android.graphics/Rect.md)`, `inoutObj:` ` [Rect](../android.graphics/Rect.md)`, `layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Apply additional gravity behavior based on the overall "display" that an object exists in. |
| --- | --- |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAbsoluteGravity](Gravity.md))`(`gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `layoutDirection:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Convert script specific gravity to absolute horizontal value. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHorizontal](Gravity.md))`(`gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicate whether the supplied gravity has an horizontal pull. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVertical](Gravity.md))`(`gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicate whether the supplied gravity has a vertical pull. |
| --- | --- |

## Constants

### AXIS_CLIP

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_CLIP: Int
```

Raw bit controlling whether the right/bottom edge is clipped to its container, based on the gravity direction being applied. 

 Value: 8

### AXIS_PULL_AFTER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_PULL_AFTER: Int
```

Raw bit controlling how the right/bottom edge is placed. 

 Value: 4

### AXIS_PULL_BEFORE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_PULL_BEFORE: Int
```

Raw bit controlling how the left/top edge is placed. 

 Value: 2

### AXIS_SPECIFIED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_SPECIFIED: Int
```

Raw bit indicating the gravity for an axis has been specified. 

 Value: 1

### AXIS_X_SHIFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_X_SHIFT: Int
```

Bits defining the horizontal axis. 

 Value: 0

### AXIS_Y_SHIFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AXIS_Y_SHIFT: Int
```

Bits defining the vertical axis. 

 Value: 4

### BOTTOM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BOTTOM: Int
```

Push object to the bottom of its container, not changing its size. 

 Value: 80

### CENTER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENTER: Int
```

Place the object in the center of its container in both the vertical and horizontal axis, not changing its size. 

 Value: 17

### CENTER_HORIZONTAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENTER_HORIZONTAL: Int
```

Place object in the horizontal center of its container, not changing its size. 

 Value: 1

### CENTER_VERTICAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENTER_VERTICAL: Int
```

Place object in the vertical center of its container, not changing its size. 

 Value: 16

### CLIP_HORIZONTAL

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CLIP_HORIZONTAL: Int
```

Flag to clip the edges of the object to its container along the horizontal axis. 

 Value: 8

### CLIP_VERTICAL

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CLIP_VERTICAL: Int
```

Flag to clip the edges of the object to its container along the vertical axis. 

 Value: 128

### DISPLAY_CLIP_HORIZONTAL

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISPLAY_CLIP_HORIZONTAL: Int
```

Special constant to enable clipping to an overall display along the horizontal dimension. This is not applied by default by [apply(int,int,int,android.graphics.Rect,int,int,android.graphics.Rect)](Gravity.md)); you must do so yourself by calling #applyDisplay. 

 Value: 16777216

### DISPLAY_CLIP_VERTICAL

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISPLAY_CLIP_VERTICAL: Int
```

Special constant to enable clipping to an overall display along the vertical dimension. This is not applied by default by [apply(int,int,int,android.graphics.Rect,int,int,android.graphics.Rect)](Gravity.md)); you must do so yourself by calling #applyDisplay. 

 Value: 268435456

### END

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val END: Int
```

Push object to x-axis position at the end of its container, not changing its size. 

 Value: 8388613

### FILL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FILL: Int
```

Grow the horizontal and vertical size of the object if needed so it completely fills its container. 

 Value: 119

### FILL_HORIZONTAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FILL_HORIZONTAL: Int
```

Grow the horizontal size of the object if needed so it completely fills its container. 

 Value: 7

### FILL_VERTICAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FILL_VERTICAL: Int
```

Grow the vertical size of the object if needed so it completely fills its container. 

 Value: 112

### HORIZONTAL_GRAVITY_MASK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HORIZONTAL_GRAVITY_MASK: Int
```

Binary mask to get the absolute horizontal gravity of a gravity. 

 Value: 7

### LEFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LEFT: Int
```

Push object to the left of its container, not changing its size. 

 Value: 3

### NO_GRAVITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_GRAVITY: Int
```

Constant indicating that no gravity has been set \* 

 Value: 0

### RELATIVE_HORIZONTAL_GRAVITY_MASK

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RELATIVE_HORIZONTAL_GRAVITY_MASK: Int
```

Binary mask for the horizontal gravity and script specific direction bit. 

 Value: 8388615

### RELATIVE_LAYOUT_DIRECTION

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RELATIVE_LAYOUT_DIRECTION: Int
```

Raw bit controlling whether the layout direction is relative or not (START/END instead of absolute LEFT/RIGHT). 

 Value: 8388608

### RIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RIGHT: Int
```

Push object to the right of its container, not changing its size. 

 Value: 5

### START

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val START: Int
```

Push object to x-axis position at the start of its container, not changing its size. 

 Value: 8388611

### TOP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TOP: Int
```

Push object to the top of its container, not changing its size. 

 Value: 48

### VERTICAL_GRAVITY_MASK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VERTICAL_GRAVITY_MASK: Int
```

Binary mask to get the vertical gravity of a gravity. 

 Value: 112

## Public constructors

### Gravity

```
Gravity()
```

## Public methods

### apply

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun apply(
    gravity: Int, 
    w: Int, 
    h: Int, 
    container: Rect!, 
    outRect: Rect!
): Unit
```

Apply a gravity constant to an object. This supposes that the layout direction is LTR.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired placement of the object, as defined by the constants in this class. |
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The horizontal size of the object. |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The vertical size of the object. |
| --- | --- |
| `container` | [Rect](../android.graphics/Rect.md)!:The frame of the containing space, in which the object will be placed. Should be large enough to contain the width and height of the object. |
| `outRect` | [Rect](../android.graphics/Rect.md)!:Receives the computed frame of the object in its container. |

### apply

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun apply(
    gravity: Int, 
    w: Int, 
    h: Int, 
    container: Rect, 
    outRect: Rect, 
    layoutDirection: Int
): Unit
```

Apply a gravity constant to an object and take care if layout direction is RTL or not.

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired placement of the object, as defined by the constants in this class. |
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The horizontal size of the object. |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The vertical size of the object. |
| --- | --- |
| `container` | [Rect](../android.graphics/Rect.md):The frame of the containing space, in which the object will be placed. Should be large enough to contain the width and height of the object. This value cannot be`null`. |
| `outRect` | [Rect](../android.graphics/Rect.md):Receives the computed frame of the object in its container. This value cannot be`null`. |
| `layoutDirection` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The layout direction. |
| --- | --- |

**See Also**

- [android.view.View#LAYOUT_DIRECTION_LTR](View.md)
- [android.view.View#LAYOUT_DIRECTION_RTL](View.md) 

### apply

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun apply(
    gravity: Int, 
    w: Int, 
    h: Int, 
    container: Rect, 
    xAdj: Int, 
    yAdj: Int, 
    outRect: Rect
): Unit
```

Apply a gravity constant to an object.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired placement of the object, as defined by the constants in this class. |
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The horizontal size of the object. |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The vertical size of the object. |
| --- | --- |
| `container` | [Rect](../android.graphics/Rect.md):The frame of the containing space, in which the object will be placed. Should be large enough to contain the width and height of the object. This value cannot be`null`. |
| `xAdj` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset to apply to the X axis. If gravity is LEFT this pushes it to the right; if gravity is RIGHT it pushes it to the left; if gravity is CENTER_HORIZONTAL it pushes it to the right or left; otherwise it is ignored. |
| `yAdj` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset to apply to the Y axis. If gravity is TOP this pushes it down; if gravity is BOTTOM it pushes it up; if gravity is CENTER_VERTICAL it pushes it down or up; otherwise it is ignored. |
| --- | --- |
| `outRect` | [Rect](../android.graphics/Rect.md):Receives the computed frame of the object in its container. This value cannot be`null`. |

### apply

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun apply(
    gravity: Int, 
    w: Int, 
    h: Int, 
    container: Rect, 
    xAdj: Int, 
    yAdj: Int, 
    outRect: Rect, 
    layoutDirection: Int
): Unit
```

Apply a gravity constant to an object.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired placement of the object, as defined by the constants in this class. |
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The horizontal size of the object. |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The vertical size of the object. |
| --- | --- |
| `container` | [Rect](../android.graphics/Rect.md):The frame of the containing space, in which the object will be placed. Should be large enough to contain the width and height of the object. This value cannot be`null`. |
| `xAdj` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset to apply to the X axis. If gravity is LEFT this pushes it to the right; if gravity is RIGHT it pushes it to the left; if gravity is CENTER_HORIZONTAL it pushes it to the right or left; otherwise it is ignored. |
| `yAdj` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset to apply to the Y axis. If gravity is TOP this pushes it down; if gravity is BOTTOM it pushes it up; if gravity is CENTER_VERTICAL it pushes it down or up; otherwise it is ignored. |
| --- | --- |
| `outRect` | [Rect](../android.graphics/Rect.md):Receives the computed frame of the object in its container. This value cannot be`null`. |
| `layoutDirection` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The layout direction. |

**See Also**

- [android.view.View#LAYOUT_DIRECTION_LTR](View.md)
- [android.view.View#LAYOUT_DIRECTION_RTL](View.md) 

### applyDisplay

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun applyDisplay(
    gravity: Int, 
    display: Rect, 
    inoutObj: Rect
): Unit
```

Apply additional gravity behavior based on the overall "display" that an object exists in. This can be used after [apply(int,int,int,android.graphics.Rect,int,int,android.graphics.Rect)](Gravity.md))to place the object within a visible display. By default this moves or clips the object to be visible in the display; the gravity flags [DISPLAY_CLIP_HORIZONTAL](Gravity.md) and [DISPLAY_CLIP_VERTICAL](Gravity.md) can be used to change this behavior.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Gravity constants to modify the placement within the display. |
| `display` | [Rect](../android.graphics/Rect.md):The rectangle of the display in which the object is being placed. This value cannot be`null`. |
| `inoutObj` | [Rect](../android.graphics/Rect.md):Supplies the current object position; returns with it modified if needed to fit in the display. This value cannot be`null`. |
| --- | --- |

### applyDisplay

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun applyDisplay(
    gravity: Int, 
    display: Rect, 
    inoutObj: Rect, 
    layoutDirection: Int
): Unit
```

Apply additional gravity behavior based on the overall "display" that an object exists in. This can be used after [apply(int,int,int,android.graphics.Rect,int,int,android.graphics.Rect)](Gravity.md))to place the object within a visible display. By default this moves or clips the object to be visible in the display; the gravity flags [DISPLAY_CLIP_HORIZONTAL](Gravity.md) and [DISPLAY_CLIP_VERTICAL](Gravity.md) can be used to change this behavior.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Gravity constants to modify the placement within the display. |
| `display` | [Rect](../android.graphics/Rect.md):The rectangle of the display in which the object is being placed. This value cannot be`null`. |
| `inoutObj` | [Rect](../android.graphics/Rect.md):Supplies the current object position; returns with it modified if needed to fit in the display. This value cannot be`null`. |
| --- | --- |
| `layoutDirection` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The layout direction. |

**See Also**

- [android.view.View#LAYOUT_DIRECTION_LTR](View.md)
- [android.view.View#LAYOUT_DIRECTION_RTL](View.md) 

### getAbsoluteGravity

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAbsoluteGravity(
    gravity: Int, 
    layoutDirection: Int
): Int
```

Convert script specific gravity to absolute horizontal value.
if horizontal direction is LTR, then START will set LEFT and END will set RIGHT. if horizontal direction is RTL, then START will set RIGHT and END will set LEFT.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The gravity to convert to absolute (horizontal) values. |
| `layoutDirection` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The layout direction. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | gravity converted to absolute (horizontal) values. |

### isHorizontal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isHorizontal(gravity: Int): Boolean
```

Indicate whether the supplied gravity has an horizontal pull.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------|
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the gravity to check for horizontal pull |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the supplied gravity has an horizontal pull |

### isVertical

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isVertical(gravity: Int): Boolean
```

Indicate whether the supplied gravity has a vertical pull.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------|
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the gravity to check for vertical pull |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the supplied gravity has a vertical pull |

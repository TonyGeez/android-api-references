# RectShape

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RectShape

Kotlin| [Java](RectShape.md) 
| --- | --- |

```
open class RectShape : Shape
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.drawable.shapes.Shape](Shape.md) ||
| | ↳ | [android.graphics.drawable.shapes.RectShape](RectShape.md) |

| Known Direct Subclasses [ArcShape](ArcShape.md), [OvalShape](OvalShape.md), [RoundRectShape](RoundRectShape.md) |------------------------------------------------------------------------------------------------------------------|-------------------------------------| | [ArcShape](ArcShape.md) | Creates an arc shape. | | [OvalShape](OvalShape.md) | Defines an oval shape. | | [RoundRectShape](RoundRectShape.md) | Creates a rounded-corner rectangle. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Defines a rectangle shape.

The rectangle can be drawn to a Canvas with its own draw() method, but more graphical control is available if you instead pass the RectShape to a [android.graphics.drawable.ShapeDrawable](../android.graphics.drawable/ShapeDrawable.md).

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------|---|
| [RectShape](RectShape.md))`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [RectShape](RectShape.md) | [clone](RectShape.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](RectShape.md))`(`canvas:` ` [Canvas](../android.graphics/Canvas.md)!`, `paint:` ` [Paint](../android.graphics/Paint.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](RectShape.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](RectShape.md))`(`outline:` ` [Outline](../android.graphics/Outline.md)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](RectShape.md))`()` <br /> |

| Protected methods ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResize](RectShape.md))`(`width:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `height:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |
| [RectF](../android.graphics/RectF.md)! | [rect](RectShape.md))`()` Returns the RectF that defines this rectangle's bounds. |

| Inherited functions ||
|---|---|
| From class [Shape](Shape.md) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHeight](Shape.md))`()` <br /> Returns the height of the Shape. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getWidth](Shape.md))`()` <br /> Returns the width of the Shape. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAlpha](Shape.md))`()` <br /> Checks whether the Shape is opaque. Default impl returns`true`. Override if your subclass can be opaque. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resize](Shape.md))`(`width:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `height:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Resizes the dimensions of this shape. Must be called before [draw(android.graphics.Canvas,android.graphics.Paint)](Shape.md)). <br /> | ||

## Public constructors

### RectShape

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RectShape()
```

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): RectShape
```

| Return ||
|---------------------------------------------------------------------------------------------------------|---------------------------|
| [RectShape](RectShape.md) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### draw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun draw(
    canvas: Canvas!, 
    paint: Paint!
): Unit
```

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](../android.graphics/Canvas.md)!:the Canvas within which this shape should be drawn |
| `paint` | [Paint](../android.graphics/Paint.md)!:the Paint object that defines this shape's characteristics |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getOutline

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOutline(outline: Outline): Unit
```

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `outline` | [Outline](../android.graphics/Outline.md):the Outline to be populated with the result. Must be non-`null`. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

## Protected methods

### onResize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onResize(
    width: Float, 
    height: Float
): Unit
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `width` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the new width of the Shape |
| `height` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the new height of the Shape |

### rect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun rect(): RectF!
```

Returns the RectF that defines this rectangle's bounds.

# OvalShape

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OvalShape

Kotlin| [Java](../android/graphics/drawable/shapes/OvalShape.md) 
| --- | --- |

```
open class OvalShape : RectShape
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.graphics.drawable.shapes.Shape](../android/graphics/drawable/shapes/Shape.md) |||
| | ↳ | [android.graphics.drawable.shapes.RectShape](../android/graphics/drawable/shapes/RectShape.md) ||
| | | ↳ | [android.graphics.drawable.shapes.OvalShape](../android/graphics/drawable/shapes/OvalShape.md) |
| --- | --- | --- | --- |

Defines an oval shape.

The oval can be drawn to a Canvas with its own draw() method, but more graphical control is available if you instead pass the OvalShape to a [android.graphics.drawable.ShapeDrawable](../android/graphics/drawable/ShapeDrawable.md).

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------|---|
| [OvalShape](../android/graphics/drawable/shapes/OvalShape.md))`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [OvalShape](../android/graphics/drawable/shapes/OvalShape.md) | [clone](../android/graphics/drawable/shapes/OvalShape.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](../android/graphics/drawable/shapes/OvalShape.md))`(`canvas:` ` [Canvas](../android/graphics/Canvas.md)!`, `paint:` ` [Paint](../android/graphics/Paint.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](../android/graphics/drawable/shapes/OvalShape.md))`(`outline:` ` [Outline](../android/graphics/Outline.md)`)` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [RectShape](../android/graphics/drawable/shapes/RectShape.md) |---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/graphics/drawable/shapes/RectShape.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/graphics/drawable/shapes/RectShape.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResize](../android/graphics/drawable/shapes/RectShape.md))`(`width:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `height:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> | | [RectF](../android/graphics/RectF.md)! | [rect](../android/graphics/drawable/shapes/RectShape.md))`()` <br /> Returns the RectF that defines this rectangle's bounds. <br /> | ||
| From class [Shape](../android/graphics/drawable/shapes/Shape.md) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHeight](../android/graphics/drawable/shapes/Shape.md))`()` <br /> Returns the height of the Shape. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getWidth](../android/graphics/drawable/shapes/Shape.md))`()` <br /> Returns the width of the Shape. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAlpha](../android/graphics/drawable/shapes/Shape.md))`()` <br /> Checks whether the Shape is opaque. Default impl returns`true`. Override if your subclass can be opaque. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resize](../android/graphics/drawable/shapes/Shape.md))`(`width:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `height:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Resizes the dimensions of this shape. Must be called before [draw(android.graphics.Canvas,android.graphics.Paint)](../android/graphics/drawable/shapes/Shape.md)). <br /> | ||

## Public constructors

### OvalShape

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OvalShape()
```

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): OvalShape
```

| Return ||
|---------------------------------------------------------------------------------------------------------|---------------------------|
| [OvalShape](../android/graphics/drawable/shapes/OvalShape.md) | a clone of this instance. |

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
| `canvas` | [Canvas](../android/graphics/Canvas.md)!:the Canvas within which this shape should be drawn |
| `paint` | [Paint](../android/graphics/Paint.md)!:the Paint object that defines this shape's characteristics |

### getOutline

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOutline(outline: Outline): Unit
```

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `outline` | [Outline](../android/graphics/Outline.md):the Outline to be populated with the result. Must be non-`null`. |

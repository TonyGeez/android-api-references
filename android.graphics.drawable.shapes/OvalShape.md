# OvalShape

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OvalShape

Kotlin| [Java](https://developer.android.com/reference/android/graphics/drawable/shapes/OvalShape "View this page in Java") 
| --- | --- |

```
open class OvalShape : RectShape
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.graphics.drawable.shapes.Shape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape) |||
| | ↳ | [android.graphics.drawable.shapes.RectShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape) ||
| | | ↳ | [android.graphics.drawable.shapes.OvalShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/OvalShape#) |
| --- | --- | --- | --- |

Defines an oval shape.

The oval can be drawn to a Canvas with its own draw() method, but more graphical control is available if you instead pass the OvalShape to a [android.graphics.drawable.ShapeDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ShapeDrawable.html#).

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------|---|
| [OvalShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/OvalShape#OvalShape())`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [OvalShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/OvalShape#) | [clone](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/OvalShape#clone())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/OvalShape#draw(android.graphics.Canvas,%20android.graphics.Paint))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)!`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/OvalShape#getOutline(android.graphics.Outline))`(`outline:` ` [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline.html#)`)` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [RectShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape) |---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape#hashCode())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResize](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape#onResize(kotlin.Float,%20kotlin.Float))`(`width:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `height:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> | | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)! | [rect](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape#rect())`()` <br /> Returns the RectF that defines this rectangle's bounds. <br /> | ||
| From class [Shape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHeight](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#getHeight())`()` <br /> Returns the height of the Shape. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getWidth](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#getWidth())`()` <br /> Returns the width of the Shape. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAlpha](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#hasAlpha())`()` <br /> Checks whether the Shape is opaque. Default impl returns`true`. Override if your subclass can be opaque. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resize](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#resize(kotlin.Float,%20kotlin.Float))`(`width:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `height:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Resizes the dimensions of this shape. Must be called before [draw(android.graphics.Canvas,android.graphics.Paint)](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#draw(android.graphics.Canvas,%20android.graphics.Paint)). <br /> | ||

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
| [OvalShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/OvalShape#) | a clone of this instance. |

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
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)!:the Canvas within which this shape should be drawn |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)!:the Paint object that defines this shape's characteristics |

### getOutline

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOutline(outline: Outline): Unit
```

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `outline` | [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline.html#):the Outline to be populated with the result. Must be non-`null`. |

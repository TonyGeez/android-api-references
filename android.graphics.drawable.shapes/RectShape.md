# RectShape

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RectShape

Kotlin| [Java](https://developer.android.com/reference/android/graphics/drawable/shapes/RectShape "View this page in Java") 
| --- | --- |

```
open class RectShape : Shape
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.drawable.shapes.Shape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape) ||
| | ↳ | [android.graphics.drawable.shapes.RectShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape#) |

| Known Direct Subclasses [ArcShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/ArcShape), [OvalShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/OvalShape), [RoundRectShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RoundRectShape) |------------------------------------------------------------------------------------------------------------------|-------------------------------------| | [ArcShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/ArcShape) | Creates an arc shape. | | [OvalShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/OvalShape) | Defines an oval shape. | | [RoundRectShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RoundRectShape) | Creates a rounded-corner rectangle. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Defines a rectangle shape.

The rectangle can be drawn to a Canvas with its own draw() method, but more graphical control is available if you instead pass the RectShape to a [android.graphics.drawable.ShapeDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ShapeDrawable.html#).

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------|---|
| [RectShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape#RectShape())`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [RectShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape#) | [clone](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape#clone())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape#draw(android.graphics.Canvas,%20android.graphics.Paint))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)!`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape#getOutline(android.graphics.Outline))`(`outline:` ` [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline.html#)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape#hashCode())`()` <br /> |

| Protected methods ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResize](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape#onResize(kotlin.Float,%20kotlin.Float))`(`width:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `height:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |
| [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)! | [rect](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape#rect())`()` Returns the RectF that defines this rectangle's bounds. |

| Inherited functions ||
|---|---|
| From class [Shape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHeight](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#getHeight())`()` <br /> Returns the height of the Shape. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getWidth](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#getWidth())`()` <br /> Returns the width of the Shape. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAlpha](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#hasAlpha())`()` <br /> Checks whether the Shape is opaque. Default impl returns`true`. Override if your subclass can be opaque. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resize](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#resize(kotlin.Float,%20kotlin.Float))`(`width:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `height:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Resizes the dimensions of this shape. Must be called before [draw(android.graphics.Canvas,android.graphics.Paint)](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#draw(android.graphics.Canvas,%20android.graphics.Paint)). <br /> | ||

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
| [RectShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape#) | a clone of this instance. |

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
| `outline` | [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline.html#):the Outline to be populated with the result. Must be non-`null`. |

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

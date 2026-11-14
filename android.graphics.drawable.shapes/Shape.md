# Shape

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Shape

Kotlin | [Java](https://developer.android.com/reference/android/graphics/drawable/shapes/Shape "View this page in Java") 
| --- | --- |

```
abstract class Shape : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.drawable.shapes.Shape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#) |

| Known Direct Subclasses [PathShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/PathShape), [RectShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape) |--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------| | [PathShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/PathShape) | Creates geometric paths, utilizing the [android.graphics.Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#) class. | | [RectShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RectShape) | Defines a rectangle shape. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ArcShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/ArcShape), [OvalShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/OvalShape), [RoundRectShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RoundRectShape) |------------------------------------------------------------------------------------------------------------------|-------------------------------------| | [ArcShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/ArcShape) | Creates an arc shape. | | [OvalShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/OvalShape) | Defines an oval shape. | | [RoundRectShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/RoundRectShape) | Creates a rounded-corner rectangle. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Defines a generic graphical "shape."

Any Shape can be drawn to a Canvas with its own draw() method, but more graphical control is available if you instead pass it to a [android.graphics.drawable.ShapeDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ShapeDrawable.html#).

Custom Shape classes must implement [clone()](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#clone()) and return an instance of the custom Shape class.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------|---|
| [Shape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#Shape())`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Shape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#) | [clone](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#clone())`()` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#draw(android.graphics.Canvas,%20android.graphics.Paint))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)!`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)!`)` Draws this shape into the provided Canvas, with the provided Paint. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHeight](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#getHeight())`()` Returns the height of the Shape. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#getOutline(android.graphics.Outline))`(`outline:` ` [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline.html#)`)` Computes the Outline of the shape and return it in the supplied Outline parameter. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getWidth](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#getWidth())`()` Returns the width of the Shape. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAlpha](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#hasAlpha())`()` Checks whether the Shape is opaque. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#hashCode())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resize](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#resize(kotlin.Float,%20kotlin.Float))`(`width:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `height:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Resizes the dimensions of this shape. |
| --- | --- |

| Protected methods ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResize](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#onResize(kotlin.Float,%20kotlin.Float))`(`width:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `height:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Callback method called when [resize(float,float)](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#resize(kotlin.Float,%20kotlin.Float)) is executed. |

## Public constructors

### Shape

```
Shape()
```

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Shape
```

| Return ||
|-------------------------------------------------------------------------------------------------|---------------------------|
| [Shape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### draw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun draw(
    canvas: Canvas!, 
    paint: Paint!
): Unit
```

Draws this shape into the provided Canvas, with the provided Paint.

Before calling this, you must call [resize(float,float)](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#resize(kotlin.Float,%20kotlin.Float)).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)!: the Canvas within which this shape should be drawn |
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)!: the Paint object that defines this shape's characteristics |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if this object is the same as the obj argument; `false` otherwise. |

### getHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHeight(): Float
```

Returns the height of the Shape. 

### getOutline

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOutline(outline: Outline): Unit
```

Computes the Outline of the shape and return it in the supplied Outline parameter. The default implementation does nothing and `outline` is not changed.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `outline` | [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline.html#): the Outline to be populated with the result. Must be non-`null`. |

### getWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWidth(): Float
```

Returns the width of the Shape. 

### hasAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasAlpha(): Boolean
```

Checks whether the Shape is opaque.

Default impl returns `true`. Override if your subclass can be opaque.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if any part of the drawable is *not* opaque. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### resize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun resize(
    width: Float, 
    height: Float
): Unit
```

Resizes the dimensions of this shape.

Must be called before [draw(android.graphics.Canvas,android.graphics.Paint)](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#draw(android.graphics.Canvas,%20android.graphics.Paint)).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------|
| `width` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the width of the shape (in pixels) |
| `height` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the height of the shape (in pixels) |

## Protected methods

### onResize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onResize(
    width: Float, 
    height: Float
): Unit
```

Callback method called when [resize(float,float)](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#resize(kotlin.Float,%20kotlin.Float)) is executed.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------|
| `width` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the new width of the Shape |
| `height` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the new height of the Shape |

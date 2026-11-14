# Shape

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Shape

Kotlin | [Java](../android/graphics/drawable/shapes/Shape.md) 
| --- | --- |

```
abstract class Shape : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.drawable.shapes.Shape](../android/graphics/drawable/shapes/Shape.md) |

| Known Direct Subclasses [PathShape](../android/graphics/drawable/shapes/PathShape.md), [RectShape](../android/graphics/drawable/shapes/RectShape.md) |--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------| | [PathShape](../android/graphics/drawable/shapes/PathShape.md) | Creates geometric paths, utilizing the [android.graphics.Path](../android/graphics/Path.md) class. | | [RectShape](../android/graphics/drawable/shapes/RectShape.md) | Defines a rectangle shape. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ArcShape](../android/graphics/drawable/shapes/ArcShape.md), [OvalShape](../android/graphics/drawable/shapes/OvalShape.md), [RoundRectShape](../android/graphics/drawable/shapes/RoundRectShape.md) |------------------------------------------------------------------------------------------------------------------|-------------------------------------| | [ArcShape](../android/graphics/drawable/shapes/ArcShape.md) | Creates an arc shape. | | [OvalShape](../android/graphics/drawable/shapes/OvalShape.md) | Defines an oval shape. | | [RoundRectShape](../android/graphics/drawable/shapes/RoundRectShape.md) | Creates a rounded-corner rectangle. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Defines a generic graphical "shape."

Any Shape can be drawn to a Canvas with its own draw() method, but more graphical control is available if you instead pass it to a [android.graphics.drawable.ShapeDrawable](../android/graphics/drawable/ShapeDrawable.md).

Custom Shape classes must implement [clone()](../android/graphics/drawable/shapes/Shape.md)) and return an instance of the custom Shape class.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------|---|
| [Shape](../android/graphics/drawable/shapes/Shape.md))`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Shape](../android/graphics/drawable/shapes/Shape.md) | [clone](../android/graphics/drawable/shapes/Shape.md))`()` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](../android/graphics/drawable/shapes/Shape.md))`(`canvas:` ` [Canvas](../android/graphics/Canvas.md)!`, `paint:` ` [Paint](../android/graphics/Paint.md)!`)` Draws this shape into the provided Canvas, with the provided Paint. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/graphics/drawable/shapes/Shape.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHeight](../android/graphics/drawable/shapes/Shape.md))`()` Returns the height of the Shape. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](../android/graphics/drawable/shapes/Shape.md))`(`outline:` ` [Outline](../android/graphics/Outline.md)`)` Computes the Outline of the shape and return it in the supplied Outline parameter. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getWidth](../android/graphics/drawable/shapes/Shape.md))`()` Returns the width of the Shape. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAlpha](../android/graphics/drawable/shapes/Shape.md))`()` Checks whether the Shape is opaque. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/graphics/drawable/shapes/Shape.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resize](../android/graphics/drawable/shapes/Shape.md))`(`width:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `height:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Resizes the dimensions of this shape. |
| --- | --- |

| Protected methods ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResize](../android/graphics/drawable/shapes/Shape.md))`(`width:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `height:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Callback method called when [resize(float,float)](../android/graphics/drawable/shapes/Shape.md)) is executed. |

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
| [Shape](../android/graphics/drawable/shapes/Shape.md) | a clone of this instance. |

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

Before calling this, you must call [resize(float,float)](../android/graphics/drawable/shapes/Shape.md)).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](../android/graphics/Canvas.md)!: the Canvas within which this shape should be drawn |
| `paint` | [Paint](../android/graphics/Paint.md)!: the Paint object that defines this shape's characteristics |

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
| `outline` | [Outline](../android/graphics/Outline.md): the Outline to be populated with the result. Must be non-`null`. |

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

Must be called before [draw(android.graphics.Canvas,android.graphics.Paint)](../android/graphics/drawable/shapes/Shape.md)).

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

Callback method called when [resize(float,float)](../android/graphics/drawable/shapes/Shape.md)) is executed.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------|
| `width` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the new width of the Shape |
| `height` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the new height of the Shape |

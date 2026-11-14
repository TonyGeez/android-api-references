# PathShape

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PathShape

Kotlin| [Java](https://developer.android.com/reference/android/graphics/drawable/shapes/PathShape "View this page in Java") 

```
open class PathShape : Shape
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.graphics.drawable.shapes.Shape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape) ||
| | ↳ | [android.graphics.drawable.shapes.PathShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/PathShape#) |

Creates geometric paths, utilizing the [android.graphics.Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#) class.

The path can be drawn to a Canvas with its own draw() method, but more graphical control is available if you instead pass the PathShape to a [android.graphics.drawable.ShapeDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ShapeDrawable.html#).

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PathShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/PathShape#PathShape(android.graphics.Path,%20kotlin.Float,%20kotlin.Float))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)`, `stdWidth:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `stdHeight:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` PathShape constructor. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [PathShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/PathShape#) | [clone](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/PathShape#clone())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/PathShape#draw(android.graphics.Canvas,%20android.graphics.Paint))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)!`, `paint:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/PathShape#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/PathShape#hashCode())`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResize](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/PathShape#onResize(kotlin.Float,%20kotlin.Float))`(`width:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `height:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Shape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHeight](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#getHeight())`()` <br /> Returns the height of the Shape. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#getOutline(android.graphics.Outline))`(`outline:` ` [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline.html#)`)` <br /> Computes the Outline of the shape and return it in the supplied Outline parameter. The default implementation does nothing and`outline`is not changed. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getWidth](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#getWidth())`()` <br /> Returns the width of the Shape. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAlpha](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#hasAlpha())`()` <br /> Checks whether the Shape is opaque. Default impl returns`true`. Override if your subclass can be opaque. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resize](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#resize(kotlin.Float,%20kotlin.Float))`(`width:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `height:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Resizes the dimensions of this shape. Must be called before [draw(android.graphics.Canvas,android.graphics.Paint)](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/Shape#draw(android.graphics.Canvas,%20android.graphics.Paint)). <br /> | ||

## Public constructors

### PathShape

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PathShape(
    path: Path, 
    stdWidth: Float, 
    stdHeight: Float)
```

PathShape constructor.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#):a Path that defines the geometric paths for this shape This value cannot be`null`. |
| `stdWidth` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the standard width for the shape. Any changes to the width with resize() will result in a width scaled based on the new width divided by this width. |
| `stdHeight` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the standard height for the shape. Any changes to the height with resize() will result in a height scaled based on the new height divided by this height. |

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): PathShape
```

| Return ||
|---------------------------------------------------------------------------------------------------------|---------------------------|
| [PathShape](https://developer.android.com/reference/kotlin/android/graphics/drawable/shapes/PathShape#) | a clone of this instance. |

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

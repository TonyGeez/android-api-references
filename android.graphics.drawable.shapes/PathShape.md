# PathShape

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PathShape

Kotlin| [Java](PathShape.md) 
| --- | --- |

```
open class PathShape : Shape
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.drawable.shapes.Shape](Shape.md) ||
| | ↳ | [android.graphics.drawable.shapes.PathShape](PathShape.md) |

Creates geometric paths, utilizing the [android.graphics.Path](../android.graphics/Path.md) class.

The path can be drawn to a Canvas with its own draw() method, but more graphical control is available if you instead pass the PathShape to a [android.graphics.drawable.ShapeDrawable](../android.graphics.drawable/ShapeDrawable.md).

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PathShape](PathShape.md))`(`path:` ` [Path](../android.graphics/Path.md)`, `stdWidth:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `stdHeight:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` PathShape constructor. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [PathShape](PathShape.md) | [clone](PathShape.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [draw](PathShape.md))`(`canvas:` ` [Canvas](../android.graphics/Canvas.md)!`, `paint:` ` [Paint](../android.graphics/Paint.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](PathShape.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](PathShape.md))`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResize](PathShape.md))`(`width:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `height:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Shape](Shape.md) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHeight](Shape.md))`()` <br /> Returns the height of the Shape. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](Shape.md))`(`outline:` ` [Outline](../android.graphics/Outline.md)`)` <br /> Computes the Outline of the shape and return it in the supplied Outline parameter. The default implementation does nothing and`outline`is not changed. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getWidth](Shape.md))`()` <br /> Returns the width of the Shape. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAlpha](Shape.md))`()` <br /> Checks whether the Shape is opaque. Default impl returns`true`. Override if your subclass can be opaque. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resize](Shape.md))`(`width:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `height:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Resizes the dimensions of this shape. Must be called before [draw(android.graphics.Canvas,android.graphics.Paint)](Shape.md)). <br /> | ||

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
| `path` | [Path](../android.graphics/Path.md):a Path that defines the geometric paths for this shape This value cannot be`null`. |
| `stdWidth` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the standard width for the shape. Any changes to the width with resize() will result in a width scaled based on the new width divided by this width. |
| `stdHeight` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the standard height for the shape. Any changes to the height with resize() will result in a height scaled based on the new height divided by this height. |
| --- | --- |

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): PathShape
```

| Return ||
|---------------------------------------------------------------------------------------------------------|---------------------------|
| [PathShape](PathShape.md) | a clone of this instance. |

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

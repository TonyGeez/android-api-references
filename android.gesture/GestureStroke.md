# GestureStroke

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GestureStroke

Kotlin| [Java](../android/gesture/GestureStroke.md) 
| --- | --- |

```
open class GestureStroke
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.gesture.GestureStroke](../android/gesture/GestureStroke.md) |

A gesture stroke started on a touch down and ended on a touch up. A stroke consists of a sequence of timed points. One or multiple strokes form a gesture.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GestureStroke](../android/gesture/GestureStroke.md))`(`points:` ` [ArrayList](../java/util/ArrayList.md)< [GesturePoint](../android/gesture/GesturePoint.md)!>!`)` A constructor that constructs a gesture stroke from a list of gesture points. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearPath](../android/gesture/GestureStroke.md))`()` Invalidates the cached path that is used to render the stroke. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [clone](../android/gesture/GestureStroke.md))`()` <br /> |
| open [OrientedBoundingBox](../android/gesture/OrientedBoundingBox.md)! | [computeOrientedBoundingBox](../android/gesture/GestureStroke.md))`()` Computes an oriented bounding box of the stroke. |
| --- | --- |
| open [Path](../android/graphics/Path.md)! | [getPath](../android/gesture/GestureStroke.md))`()` <br /> |
| open [Path](../android/graphics/Path.md)! | [toPath](../android/gesture/GestureStroke.md))`(`width:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `height:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `numSample:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Converts the stroke to a Path of a given number of points. |

| Properties ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [RectF](../android/graphics/RectF.md)! | [boundingBox](../android/gesture/GestureStroke.md) <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [length](../android/gesture/GestureStroke.md) <br /> |
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | [points](../android/gesture/GestureStroke.md) <br /> |
| --- | --- |

## Public constructors

### GestureStroke

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GestureStroke(points: ArrayList<GesturePoint!>!)
```

A constructor that constructs a gesture stroke from a list of gesture points.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `points` | [ArrayList](../java/util/ArrayList.md)\< [GesturePoint](../android/gesture/GesturePoint.md)!\>!: |

## Public methods

### clearPath

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearPath(): Unit
```

Invalidates the cached path that is used to render the stroke. 

### clone

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any!
```

| Return ||
|-----------------------------------------------------------------------------|---------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### computeOrientedBoundingBox

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun computeOrientedBoundingBox(): OrientedBoundingBox!
```

Computes an oriented bounding box of the stroke.

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------|
| [OrientedBoundingBox](../android/gesture/OrientedBoundingBox.md)! | OrientedBoundingBox |

### getPath

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPath(): Path!
```  

### toPath

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toPath(
    width: Float, 
    height: Float, 
    numSample: Int
): Path!
```

Converts the stroke to a Path of a given number of points.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------|
| `width` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the width of the bounding box of the target path |
| `height` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the height of the bounding box of the target path |
| `numSample` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of points needed |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------|----------|
| [Path](../android/graphics/Path.md)! | the path |

## Properties

### boundingBox

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val boundingBox: RectF!
```  

### length

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val length: Float
```  

### points

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val points: FloatArray!
```

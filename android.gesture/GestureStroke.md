# GestureStroke

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GestureStroke

Kotlin| [Java](https://developer.android.com/reference/android/gesture/GestureStroke "View this page in Java") 

```
open class GestureStroke
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.gesture.GestureStroke](https://developer.android.com/reference/kotlin/android/gesture/GestureStroke#) |

A gesture stroke started on a touch down and ended on a touch up. A stroke consists of a sequence of timed points. One or multiple strokes form a gesture.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GestureStroke](https://developer.android.com/reference/kotlin/android/gesture/GestureStroke#GestureStroke(java.util.ArrayList))`(`points:` ` [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)< [GesturePoint](https://developer.android.com/reference/kotlin/android/gesture/GesturePoint)!>!`)` A constructor that constructs a gesture stroke from a list of gesture points. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearPath](https://developer.android.com/reference/kotlin/android/gesture/GestureStroke#clearPath())`()` Invalidates the cached path that is used to render the stroke. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [clone](https://developer.android.com/reference/kotlin/android/gesture/GestureStroke#clone())`()` <br /> |
| open [OrientedBoundingBox](https://developer.android.com/reference/kotlin/android/gesture/OrientedBoundingBox)! | [computeOrientedBoundingBox](https://developer.android.com/reference/kotlin/android/gesture/GestureStroke#computeOrientedBoundingBox())`()` Computes an oriented bounding box of the stroke. |
| open [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)! | [getPath](https://developer.android.com/reference/kotlin/android/gesture/GestureStroke#getPath())`()` <br /> |
| open [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)! | [toPath](https://developer.android.com/reference/kotlin/android/gesture/GestureStroke#toPath(kotlin.Float,%20kotlin.Float,%20kotlin.Int))`(`width:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `height:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `numSample:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Converts the stroke to a Path of a given number of points. |

| Properties ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)! | [boundingBox](https://developer.android.com/reference/kotlin/android/gesture/GestureStroke#boundingBox:android.graphics.RectF) <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [length](https://developer.android.com/reference/kotlin/android/gesture/GestureStroke#length:kotlin.Float) <br /> |
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | [points](https://developer.android.com/reference/kotlin/android/gesture/GestureStroke#points:kotlin.FloatArray) <br /> |

## Public constructors

### GestureStroke

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GestureStroke(points: ArrayList<GesturePoint!>!)
```

A constructor that constructs a gesture stroke from a list of gesture points.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `points` | [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [GesturePoint](https://developer.android.com/reference/kotlin/android/gesture/GesturePoint)!\>!: |

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
| [OrientedBoundingBox](https://developer.android.com/reference/kotlin/android/gesture/OrientedBoundingBox)! | OrientedBoundingBox |

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

| Return ||
|-------------------------------------------------------------------------------------|----------|
| [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)! | the path |

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

# MeteringRectangle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MeteringRectangle

Kotlin | [Java](https://developer.android.com/reference/android/hardware/camera2/params/MeteringRectangle "View this page in Java") 

```
class MeteringRectangle
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.camera2.params.MeteringRectangle](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle#) |

An immutable class to represent a rectangle `(x, y, width, height)` with an additional weight component.

The rectangle is defined to be inclusive of the specified coordinates.

When used with a [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#), the coordinate system is based on the active pixel array, with `(0,0)` being the top-left pixel in the [active pixel array](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key), and `(android.sensor.info.activeArraySize.width - 1, android.sensor.info.activeArraySize.height - 1)` being the bottom-right pixel in the active pixel array.

The weight must range from {@value #METERING_WEIGHT_MIN} to {@value #METERING_WEIGHT_MAX} inclusively, and represents a weight for every pixel in the area. This means that a large metering area with the same weight as a smaller area will have more effect in the metering result. Metering areas can partially overlap and the camera device will add the weights in the overlap rectangle.

If all rectangles have 0 weight, then no specific metering area needs to be used by the camera device. If the metering rectangle is outside the used android.scaler.cropRegion returned in capture result metadata, the camera device will ignore the sections outside the rectangle and output the used sections in the result metadata.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METERING_WEIGHT_DONT_CARE](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle#METERING_WEIGHT_DONT_CARE:kotlin.Int) Weights set to this value will cause the camera device to ignore this rectangle. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METERING_WEIGHT_MAX](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle#METERING_WEIGHT_MAX:kotlin.Int) The maximum value of valid metering weight. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METERING_WEIGHT_MIN](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle#METERING_WEIGHT_MIN:kotlin.Int) The minimum value of valid metering weight. |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MeteringRectangle](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle#MeteringRectangle(android.graphics.Point,%20android.util.Size,%20kotlin.Int))`(`xy:` ` [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#)!`, `dimensions:` ` [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!`, `meteringWeight:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new metering rectangle. |
| [MeteringRectangle](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle#MeteringRectangle(android.graphics.Rect,%20kotlin.Int))`(`rect:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!`, `meteringWeight:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new metering rectangle. |
| [MeteringRectangle](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle#MeteringRectangle(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `meteringWeight:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new metering rectangle. |

| Public methods ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle#equals(android.hardware.camera2.params.MeteringRectangle))`(`other:` ` [MeteringRectangle](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle#)!`)` Compare two metering rectangles to see if they are equal. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle#getHeight())`()` Return the height of the rectangle. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMeteringWeight](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle#getMeteringWeight())`()` Return the metering weight of the rectangle. |
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)! | [getRect](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle#getRect())`()` Convenience method to create a [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) from this metering rectangle. |
| [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)! | [getSize](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle#getSize())`()` Convenience method to create the size from this metering rectangle. |
| [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#)! | [getUpperLeftPoint](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle#getUpperLeftPoint())`()` Convenience method to create the upper-left (X,Y) coordinate as a [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle#getWidth())`()` Return the width of the rectangle. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getX](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle#getX())`()` Return the X coordinate of the left side of the rectangle. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getY](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle#getY())`()` Return the Y coordinate of the upper side of the rectangle. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle#hashCode())`()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle#toString())`()` Return the metering rectangle as a string representation `"(x:%d, y:%d, w:%d, h:%d, wt:%d)"` where each `%d` respectively represents the x, y, width, height, and weight points. |

## Constants

### METERING_WEIGHT_DONT_CARE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METERING_WEIGHT_DONT_CARE: Int
```

Weights set to this value will cause the camera device to ignore this rectangle. If all metering rectangles are weighed with 0, the camera device will choose its own metering rectangles. 

 Value: 0

### METERING_WEIGHT_MAX

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METERING_WEIGHT_MAX: Int
```

The maximum value of valid metering weight. 

 Value: 1000

### METERING_WEIGHT_MIN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METERING_WEIGHT_MIN: Int
```

The minimum value of valid metering weight. 

 Value: 0

## Public constructors

### MeteringRectangle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MeteringRectangle(
    xy: Point!, 
    dimensions: Size!, 
    meteringWeight: Int)
```

Create a new metering rectangle.

The point `xy`'s data is copied; the reference is not retained.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `xy` | [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#)!: a non-`null` [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#) with both x,y \>= 0 |
| `dimensions` | [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!: a non-`null` [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#) with width, height \>= 0 |
| `meteringWeight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): weight \>= 0 |

| Exceptions ||
|--------------------------------------|----------------------------------------|
| `java.lang.IllegalArgumentException` | if any of the parameters were negative |
| `java.lang.NullPointerException` | if any of the arguments were null |

### MeteringRectangle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MeteringRectangle(
    rect: Rect!, 
    meteringWeight: Int)
```

Create a new metering rectangle.

The rectangle data is copied; the reference is not retained.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `rect` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!: a non-`null` rectangle with all x,y,w,h dimensions \>= 0 |
| `meteringWeight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): weight \>= 0 |

| Exceptions ||
|--------------------------------------|----------------------------------------|
| `java.lang.IllegalArgumentException` | if any of the parameters were negative |
| `java.lang.NullPointerException` | if any of the arguments were null |

### MeteringRectangle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MeteringRectangle(
    x: Int, 
    y: Int, 
    width: Int, 
    height: Int, 
    meteringWeight: Int)
```

Create a new metering rectangle.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): coordinate \>= 0 |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): coordinate \>= 0 |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): width \>= 0 |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): height \>= 0 |
| `meteringWeight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): weight between {@value #METERING_WEIGHT_MIN} and {@value #METERING_WEIGHT_MAX} inclusively |

| Exceptions ||
|--------------------------------------|----------------------------------------|
| `java.lang.IllegalArgumentException` | if any of the parameters were negative |

## Public methods

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: MeteringRectangle!): Boolean
```

Compare two metering rectangles to see if they are equal. Two weighted rectangles are only considered equal if each of their components (x, y, width, height, weight) is respectively equal.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [MeteringRectangle](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle#)!: Another MeteringRectangle |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if the metering rectangles are equal, `false` otherwise |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if this object is the same as the obj argument; `false` otherwise. |

### getHeight

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHeight(): Int
```

Return the height of the rectangle.

| Return ||
|----------------------------------------------------------------------------|--------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | height \>= 0 |

### getMeteringWeight

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMeteringWeight(): Int
```

Return the metering weight of the rectangle.

| Return ||
|----------------------------------------------------------------------------|--------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | weight \>= 0 |

### getRect

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRect(): Rect!
```

Convenience method to create a [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) from this metering rectangle.

This strips away the weight from the rectangle.

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)! | a new [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) with non-negative x1, y1, x2, y2 |

### getSize

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSize(): Size!
```

Convenience method to create the size from this metering rectangle.

This strips away the X,Y,weight from the rectangle.

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)! | a new [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#) with non-negative width and height |

### getUpperLeftPoint

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUpperLeftPoint(): Point!
```

Convenience method to create the upper-left (X,Y) coordinate as a [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#).

| Return ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#)! | a new `(x,y)` [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#) with both x,y \>= 0 |

### getWidth

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWidth(): Int
```

Return the width of the rectangle.

| Return ||
|----------------------------------------------------------------------------|-------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | width \>= 0 |

### getX

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getX(): Int
```

Return the X coordinate of the left side of the rectangle.

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | x coordinate \>= 0 |

### getY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getY(): Int
```

Return the Y coordinate of the upper side of the rectangle.

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | y coordinate \>= 0 |

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#).

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)) method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)) method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Return the metering rectangle as a string representation `"(x:%d, y:%d, w:%d, h:%d, wt:%d)"` where each `%d` respectively represents the x, y, width, height, and weight points.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | string representation of the metering rectangle |

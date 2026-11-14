# TonemapCurve

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TonemapCurve

Kotlin| [Java](TonemapCurve.md) 
| --- | --- |

```
class TonemapCurve
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.params.TonemapCurve](TonemapCurve.md) |

Immutable class for describing a`2 x M x 3`tonemap curve of floats.

This defines red, green, and blue curves that the [CameraDevice](../android.hardware.camera2/CameraDevice.md) will use as the tonemapping/contrast/gamma curve when [CaptureRequest.TONEMAP_MODE](../android.hardware.camera2/CaptureRequest.md) is set to [CameraMetadata.TONEMAP_MODE_CONTRAST_CURVE](../android.hardware.camera2/CameraMetadata.md).

For a camera device with [MONOCHROME](../android.hardware.camera2/CameraMetadata.md) capability, all 3 channels will contain the same set of control points.

The total number of points`(Pin, Pout)`for each color channel can be no more than [CameraCharacteristics.TONEMAP_MAX_CURVE_POINTS](../android.hardware.camera2/CameraCharacteristics.md).

The coordinate system for each point is within the inclusive range \[{@value #LEVEL_BLACK}, {@value #LEVEL_WHITE}\].

## Summary

| Constants ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_BLUE](TonemapCurve.md) Index of the blue color channel curve. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_GREEN](TonemapCurve.md) Index of the green color channel curve. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_RED](TonemapCurve.md) Index of the red color channel curve. |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [LEVEL_BLACK](TonemapCurve.md) Lower bound tonemap value corresponding to pure black for a single color channel. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [LEVEL_WHITE](TonemapCurve.md) Upper bound tonemap value corresponding to a pure white for a single color channel. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POINT_SIZE](TonemapCurve.md) Number of elements in a`(Pin, Pout)`point; |
| --- | --- |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TonemapCurve](TonemapCurve.md))`(`red:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `green:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `blue:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Create a new immutable TonemapCurve instance. |

| Public methods ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyColorCurve](TonemapCurve.md))`(`colorChannel:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `destination:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Copy the color curve for a single color channel from this tonemap curve into the destination. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](TonemapCurve.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Check if this TonemapCurve is equal to another TonemapCurve. |
| [PointF](../android.graphics/PointF.md)! | [getPoint](TonemapCurve.md))`(`colorChannel:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the point for a color channel at a specified index. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPointCount](TonemapCurve.md))`(`colorChannel:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the number of points stored in this tonemap curve for the specified color channel. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](TonemapCurve.md))`()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](TonemapCurve.md))`()` Return the TonemapCurve as a string representation. |
| --- | --- |

## Constants

### CHANNEL_BLUE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANNEL_BLUE: Int
```

Index of the blue color channel curve. 

 Value: 2

### CHANNEL_GREEN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANNEL_GREEN: Int
```

Index of the green color channel curve. 

 Value: 1

### CHANNEL_RED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANNEL_RED: Int
```

Index of the red color channel curve. 

 Value: 0

### LEVEL_BLACK

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LEVEL_BLACK: Float
```

Lower bound tonemap value corresponding to pure black for a single color channel. 

 Value: 0.0f

### LEVEL_WHITE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LEVEL_WHITE: Float
```

Upper bound tonemap value corresponding to a pure white for a single color channel. 

 Value: 1.0f

### POINT_SIZE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POINT_SIZE: Int
```

Number of elements in a`(Pin, Pout)`point; 

 Value: 2

## Public constructors

### TonemapCurve

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TonemapCurve(
    red: FloatArray!, 
    green: FloatArray!, 
    blue: FloatArray!)
```

Create a new immutable TonemapCurve instance.

Values are stored as a contiguous array of`(Pin, Pout)`points.

All parameters may have independent length but should have at most [CameraCharacteristics.TONEMAP_MAX_CURVE_POINTS](../android.hardware.camera2/CameraCharacteristics.md)\* {@value #POINT_SIZE} elements and at least 2 \* {@value #POINT_SIZE} elements.

All sub-elements must be in the inclusive range of \[{@value #LEVEL_BLACK}, {@value #LEVEL_WHITE}\].

This constructor copies the array contents and does not retain ownership of the array.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `red` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:An array of elements whose length is divisible by {@value #POINT_SIZE} |
| `green` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:An array of elements whose length is divisible by {@value #POINT_SIZE} |
| `blue` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:An array of elements whose length is divisible by {@value #POINT_SIZE} |
| --- | --- |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if any of input array length is invalid, or if any of the elements in the array are not in the range of \[{@value #LEVEL_BLACK}, {@value #LEVEL_WHITE}\] |
| `java.lang.NullPointerException` | if any of the parameters are`null` |

## Public methods

### copyColorCurve

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun copyColorCurve(
    colorChannel: Int, 
    destination: FloatArray!, 
    offset: Int
): Unit
```

Copy the color curve for a single color channel from this tonemap curve into the destination.

Values are stored as packed`(Pin, Pout`) points, and there are a total of [getPointCount](TonemapCurve.md))points for that respective channel.

All returned coordinates are between the range of \[{@value #LEVEL_BLACK}, {@value #LEVEL_WHITE}\].

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `destination` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:an array big enough to hold at least [getPointCount](TonemapCurve.md))`*` [POINT_SIZE](TonemapCurve.md) elements after the`offset` |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a non-negative offset into the array |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If`destination`was`null` |
| `java.lang.IllegalArgumentException` | If offset was negative |
| `java.lang.ArrayIndexOutOfBoundsException` | If there's not enough room to write the elements at the specified destination and offset. |
| --- | --- |

**See Also**

- [#LEVEL_BLACK](TonemapCurve.md)
- [#LEVEL_WHITE](TonemapCurve.md) 

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Check if this TonemapCurve is equal to another TonemapCurve.

Two matrices are equal if and only if all of their elements are [equal](../java.lang/Object.md)).

| Parameters ||
|-------|--------------------------|
| `obj` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the objects were equal,`false`otherwise |

### getPoint

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPoint(
    colorChannel: Int, 
    index: Int
): PointF!
```

Get the point for a color channel at a specified index.

The index must be at least 0 but no greater than [getPointCount(int)](TonemapCurve.md))for that`colorChannel`.

All returned coordinates in the point are between the range of \[{@value #LEVEL_BLACK}, {@value #LEVEL_WHITE}\].

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `colorChannel` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): [CHANNEL_RED](TonemapCurve.md), [CHANNEL_GREEN](TonemapCurve.md), or [CHANNEL_BLUE](TonemapCurve.md) |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):at least 0 but no greater than`getPointCount(colorChannel)` |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------|
| [PointF](../android.graphics/PointF.md)! | the`(Pin, Pout)`pair mapping the tone for that index |

| Exceptions ||
|--------------------------------------|-------------------------------------------|
| `java.lang.IllegalArgumentException` | if`colorChannel`or`index`was out of range |

**See Also**

- [#LEVEL_BLACK](TonemapCurve.md)
- [#LEVEL_WHITE](TonemapCurve.md) 

### getPointCount

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPointCount(colorChannel: Int): Int
```

Get the number of points stored in this tonemap curve for the specified color channel.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `colorChannel` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of [CHANNEL_RED](TonemapCurve.md), [CHANNEL_GREEN](TonemapCurve.md), [CHANNEL_BLUE](TonemapCurve.md) |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | number of points stored in this tonemap for that color's curve (\>= 0) |

| Exceptions ||
|--------------------------------------|----------------------------------|
| `java.lang.IllegalArgumentException` | if`colorChannel`was out of range |

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](../java.util/HashMap.md).

The general contract of`hashCode`is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the`hashCode`method must consistently return the same integer, provided no information used in`equals`comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the [equals](../java.lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce the same integer result.
- It is*not* required that if two objects are unequal according to the [equals](../java.lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Return the TonemapCurve as a string representation.

`"TonemapCurve{R:[(%f, %f), (%f, %f) ... (%f, %f)], G:[(%f, %f), (%f, %f) ... (%f, %f)], B:[(%f, %f), (%f, %f) ... (%f, %f)]}"`, where each`(%f, %f)`respectively represents one point of the corresponding tonemap curve.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | string representation of [TonemapCurve](TonemapCurve.md) |

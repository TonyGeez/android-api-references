# RggbChannelVector

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RggbChannelVector

Kotlin| [Java](https://developer.android.com/reference/android/hardware/camera2/params/RggbChannelVector "View this page in Java") 

```
class RggbChannelVector
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.camera2.params.RggbChannelVector](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#) |

Immutable class to store a 4-element vector of floats indexable by a bayer RAW 2x2 pixel block.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BLUE](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#BLUE:kotlin.Int) Blue color channel in a bayer Raw pattern. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COUNT](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#COUNT:kotlin.Int) The number of color channels in this vector. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GREEN_EVEN](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#GREEN_EVEN:kotlin.Int) Green color channel in a bayer Raw pattern used by the even rows. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GREEN_ODD](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#GREEN_ODD:kotlin.Int) Green color channel in a bayer Raw pattern used by the odd rows. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RED](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#RED:kotlin.Int) Red color channel in a bayer Raw pattern. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RggbChannelVector](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#RggbChannelVector(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`red:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `greenEven:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `greenOdd:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `blue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Create a new [RggbChannelVector](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#) from an RGGB 2x2 pixel. |

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyTo](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#copyTo(kotlin.FloatArray,%20kotlin.Int))`(`destination:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Copy the vector into the destination in the order`[R, Geven, Godd, B]`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Check if this [RggbChannelVector](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#) is equal to another [RggbChannelVector](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getBlue](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#getBlue())`()` Get the blue component. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getComponent](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#getComponent(kotlin.Int))`(`colorChannel:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the component by the color channel index. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getGreenEven](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#getGreenEven())`()` Get the green (even rows) component. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getGreenOdd](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#getGreenOdd())`()` Get the green (odd rows) component. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getRed](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#getRed())`()` Get the red component. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#hashCode())`()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#toString())`()` Return the RggbChannelVector as a string representation. |

## Constants

### BLUE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BLUE: Int
```

Blue color channel in a bayer Raw pattern. 

 Value: 3

### COUNT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COUNT: Int
```

The number of color channels in this vector. 

 Value: 4

### GREEN_EVEN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GREEN_EVEN: Int
```

Green color channel in a bayer Raw pattern used by the even rows. 

 Value: 1

### GREEN_ODD

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GREEN_ODD: Int
```

Green color channel in a bayer Raw pattern used by the odd rows. 

 Value: 2

### RED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RED: Int
```

Red color channel in a bayer Raw pattern. 

 Value: 0

## Public constructors

### RggbChannelVector

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RggbChannelVector(
    red: Float, 
    greenEven: Float, 
    greenOdd: Float, 
    blue: Float)
```

Create a new [RggbChannelVector](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#) from an RGGB 2x2 pixel.

All pixel values are considered normalized within`[0.0f, 1.0f]`(i.e.`1.0f`could be linearized to`255`if converting to a non-floating point pixel representation).

All arguments must be finite; NaN and infinity is not allowed.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------|
| `red` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):red pixel |
| `greenEven` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):green pixel (even row) |
| `greenOdd` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):green pixel (odd row) |
| `blue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):blue pixel |

| Exceptions ||
|--------------------------------------|-----------------------------------------|
| `java.lang.IllegalArgumentException` | if any of the arguments were not finite |

## Public methods

### copyTo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun copyTo(
    destination: FloatArray!, 
    offset: Int
): Unit
```

Copy the vector into the destination in the order`[R, Geven, Godd, B]`.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `destination` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:an array big enough to hold at least {@value #COUNT} elements after the`offset` |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a non-negative offset into the array |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If`destination`was`null` |
| `java.lang.ArrayIndexOutOfBoundsException` | If there's not enough room to write the elements at the specified destination and offset. |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Check if this [RggbChannelVector](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#) is equal to another [RggbChannelVector](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#).

Two vectors are only equal if and only if each of the respective elements is equal.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the objects were equal,`false`otherwise |

### getBlue

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBlue(): Float
```

Get the blue component.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | a floating point value (guaranteed to be finite) |

### getComponent

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getComponent(colorChannel: Int): Float
```

Get the component by the color channel index.

`colorChannel`must be one of [RED](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#RED:kotlin.Int), [GREEN_EVEN](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#GREEN_EVEN:kotlin.Int), [GREEN_ODD](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#GREEN_ODD:kotlin.Int), [BLUE](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#BLUE:kotlin.Int).

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `colorChannel` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):greater or equal to`0`and less than [COUNT](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#COUNT:kotlin.Int) |

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | a floating point value (guaranteed to be finite) |

| Exceptions ||
|--------------------------------------|----------------------------------|
| `java.lang.IllegalArgumentException` | if`colorChannel`was out of range |

### getGreenEven

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGreenEven(): Float
```

Get the green (even rows) component.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | a floating point value (guaranteed to be finite) |

### getGreenOdd

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGreenOdd(): Float
```

Get the green (odd rows) component.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | a floating point value (guaranteed to be finite) |

### getRed

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRed(): Float
```

Get the red component.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | a floating point value (guaranteed to be finite) |

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#).

The general contract of`hashCode`is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the`hashCode`method must consistently return the same integer, provided no information used in`equals`comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))method, then calling the`hashCode`method on each of the two objects must produce the same integer result.
- It is*not* required that if two objects are unequal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))method, then calling the`hashCode`method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Return the RggbChannelVector as a string representation.

`"RggbChannelVector{R:%f, G_even:%f, G_odd:%f, B:%f}"`, where each`%f`respectively represents one of the the four color channels.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | string representation of [RggbChannelVector](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector#) |

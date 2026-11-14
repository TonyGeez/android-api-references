# LensShadingMap

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LensShadingMap

Kotlin| [Java](LensShadingMap.md) 
| --- | --- |

```
class LensShadingMap
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.params.LensShadingMap](LensShadingMap.md) |

Immutable class for describing a`4 x N x M`lens shading map of floats.

## Summary

| Constants ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [MINIMUM_GAIN_FACTOR](LensShadingMap.md) The smallest gain factor in this map. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyGainFactors](LensShadingMap.md))`(`destination:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Copy all gain factors in row-major order from this lens shading map into the destination. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](LensShadingMap.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Check if this LensShadingMap is equal to another LensShadingMap. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnCount](LensShadingMap.md))`()` Get the number of columns in this map. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getGainFactor](LensShadingMap.md))`(`colorChannel:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get a single color channel gain factor from this lens shading map by its row and column. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGainFactorCount](LensShadingMap.md))`()` Get the total number of gain factors in this map. |
| [RggbChannelVector](RggbChannelVector.md)! | [getGainFactorVector](LensShadingMap.md))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get a gain factor vector from this lens shading map by its row and column. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRowCount](LensShadingMap.md))`()` Get the number of rows in this map. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](LensShadingMap.md))`()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](LensShadingMap.md))`()` Return the LensShadingMap as a string representation. |
| --- | --- |

## Constants

### MINIMUM_GAIN_FACTOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MINIMUM_GAIN_FACTOR: Float
```

The smallest gain factor in this map.

All values in this map will be at least this large. 

 Value: 1.0f

## Public methods

### copyGainFactors

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun copyGainFactors(
    destination: FloatArray!, 
    offset: Int
): Unit
```

Copy all gain factors in row-major order from this lens shading map into the destination.

Each gain factor will be \>= [MINIMUM_GAIN_FACTOR](LensShadingMap.md).

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `destination` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:an array big enough to hold at least [RggbChannelVector.COUNT](RggbChannelVector.md) elements after the`offset` |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a non-negative offset into the array |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If`destination`was`null` |
| `java.lang.IllegalArgumentException` | If offset was negative |
| `java.lang.ArrayIndexOutOfBoundsException` | If there's not enough room to write the elements at the specified destination and offset. |
| --- | --- |

**See Also**

- [android.hardware.camera2.CaptureResult#STATISTICS_LENS_SHADING_CORRECTION_MAP](../android.hardware.camera2/CaptureResult.md) 

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Check if this LensShadingMap is equal to another LensShadingMap.

Two lens shading maps are equal if and only if they have the same rows/columns, and all of their elements are [equal](../java.lang/Object.md)).

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the objects were equal,`false`otherwise |

### getColumnCount

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getColumnCount(): Int
```

Get the number of columns in this map. 

### getGainFactor

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGainFactor(
    colorChannel: Int, 
    column: Int, 
    row: Int
): Float
```

Get a single color channel gain factor from this lens shading map by its row and column.

The rows must be within the range \ [0,[getRowCount](LensShadingMap.md))), the column must be within the range \ [0,[getColumnCount](LensShadingMap.md))), and the color channel must be within the range \[0, {@value android.hardware.camera2.params.RggbChannelVector#COUNT RggbChannelVector.COUNT}).

The channel order is`[R, Geven, Godd, B]`, where`Geven`is the green channel for the even rows of a Bayer pattern, and`Godd`is the odd rows.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `colorChannel` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):color channel from`[R, Geven, Godd, B]` |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):within the range \ [0,[getColumnCount](LensShadingMap.md))) |
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):within the range \ [0,[getRowCount](LensShadingMap.md))) |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | a gain factor \>= {@value #MINIMUM_GAIN_FACTOR} |

| Exceptions ||
|--------------------------------------|-------------------------------------------|
| `java.lang.IllegalArgumentException` | if any of the parameters was out of range |

**See Also**

- [android.hardware.camera2.params.RggbChannelVector#RED](RggbChannelVector.md)
- [android.hardware.camera2.params.RggbChannelVector#GREEN_EVEN](RggbChannelVector.md)
- [android.hardware.camera2.params.RggbChannelVector#GREEN_ODD](RggbChannelVector.md)
- [android.hardware.camera2.params.RggbChannelVector#BLUE](RggbChannelVector.md)
- [#getRowCount](LensShadingMap.md))
- [#getColumnCount](LensShadingMap.md)) 

### getGainFactorCount

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGainFactorCount(): Int
```

Get the total number of gain factors in this map.

A single gain factor contains exactly one color channel. Use with [copyGainFactors](LensShadingMap.md))to allocate a large-enough array. 

### getGainFactorVector

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGainFactorVector(
    column: Int, 
    row: Int
): RggbChannelVector!
```

Get a gain factor vector from this lens shading map by its row and column.

The rows must be within the range \ [0,[getRowCount](LensShadingMap.md))), the column must be within the range \ [0,[getColumnCount](LensShadingMap.md))).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):within the range \ [0,[getColumnCount](LensShadingMap.md))) |
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):within the range \ [0,[getRowCount](LensShadingMap.md))) |

| Return ||
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RggbChannelVector](RggbChannelVector.md)! | an [RggbChannelVector](RggbChannelVector.md) where each gain factor \>= {@value #MINIMUM_GAIN_FACTOR} |

| Exceptions ||
|--------------------------------------|-------------------------------------------|
| `java.lang.IllegalArgumentException` | if any of the parameters was out of range |

**See Also**

- [#getRowCount](LensShadingMap.md))
- [#getColumnCount](LensShadingMap.md)) 

### getRowCount

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRowCount(): Int
```

Get the number of rows in this map. 

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

Return the LensShadingMap as a string representation.

`"LensShadingMap{R:([%f, %f, ... %f], ... [%f, %f, ... %f]), G_even:([%f, %f, ... %f], ... [%f, %f, ... %f]), G_odd:([%f, %f, ... %f], ... [%f, %f, ... %f]), B:([%f, %f, ... %f], ... [%f, %f, ... %f])}"`, where each`%f`represents one gain factor and each`[%f, %f, ... %f]`represents a row of the lens shading map

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | string representation of [LensShadingMap](LensShadingMap.md) |

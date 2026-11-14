# Interpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Interpolator

Kotlin| [Java](../android/graphics/Interpolator.md) 
| --- | --- |

```
open class Interpolator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.Interpolator](../android/graphics/Interpolator.md) |

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------|
| | [Result](../android/graphics/Interpolator.Result.md) <br /> |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Interpolator](../android/graphics/Interpolator.md))`(`valueCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [Interpolator](../android/graphics/Interpolator.md))`(`valueCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `frameCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getKeyFrameCount](../android/graphics/Interpolator.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getValueCount](../android/graphics/Interpolator.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](../android/graphics/Interpolator.md))`(`valueCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reset the Interpolator to have the specified number of values and an implicit keyFrame count of 2 (just a start and end). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](../android/graphics/Interpolator.md))`(`valueCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `frameCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reset the Interpolator to have the specified number of values and keyFrames. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setKeyFrame](../android/graphics/Interpolator.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `msec:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `values:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Assign the keyFrame (specified by index) a time value and an array of key values (with an implicitly blend array of \[0, 0, 1, 1\] giving linear transition to the next set of key values). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setKeyFrame](../android/graphics/Interpolator.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `msec:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `values:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `blend:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Assign the keyFrame (specified by index) a time value and an array of key values and blend array. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRepeatMirror](../android/graphics/Interpolator.md))`(`repeatCount:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `mirror:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set a repeat count (which may be fractional) for the interpolator, and whether the interpolator should mirror its repeats. |
| open [Interpolator.Result](../android/graphics/Interpolator.Result.md)! | [timeToValues](../android/graphics/Interpolator.md))`(`values:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Calls timeToValues(msec, values) with the msec set to now (by calling (int)SystemClock. |
| open [Interpolator.Result](../android/graphics/Interpolator.Result.md)! | [timeToValues](../android/graphics/Interpolator.md))`(`msec:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `values:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Given a millisecond time value (msec), return the interpolated values and return whether the specified time was within the range of key times (NORMAL), was before the first key time (FREEZE_START) or after the last key time (FREEZE_END). |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/graphics/Interpolator.md))`()` <br /> |

## Public constructors

### Interpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Interpolator(valueCount: Int)
```  

### Interpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Interpolator(
    valueCount: Int, 
    frameCount: Int)
```

## Public methods

### getKeyFrameCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getKeyFrameCount(): Int
```  

### getValueCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getValueCount(): Int
```  

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(valueCount: Int): Unit
```

Reset the Interpolator to have the specified number of values and an implicit keyFrame count of 2 (just a start and end). After this call the values for each keyFrame must be assigned using setKeyFrame(). 

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(
    valueCount: Int, 
    frameCount: Int
): Unit
```

Reset the Interpolator to have the specified number of values and keyFrames. After this call the values for each keyFrame must be assigned using setKeyFrame(). 

### setKeyFrame

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setKeyFrame(
    index: Int, 
    msec: Int, 
    values: FloatArray!
): Unit
```

Assign the keyFrame (specified by index) a time value and an array of key values (with an implicitly blend array of \[0, 0, 1, 1\] giving linear transition to the next set of key values).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the key frame to assign |
| `msec` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The time (in mililiseconds) for this key frame. Based on the SystemClock.uptimeMillis() clock |
| `values` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:Array of values associated with theis key frame |
| --- | --- |

### setKeyFrame

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setKeyFrame(
    index: Int, 
    msec: Int, 
    values: FloatArray!, 
    blend: FloatArray!
): Unit
```

Assign the keyFrame (specified by index) a time value and an array of key values and blend array.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the key frame to assign |
| `msec` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The time (in mililiseconds) for this key frame. Based on the SystemClock.uptimeMillis() clock |
| `values` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:Array of values associated with theis key frame |
| --- | --- |
| `blend` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:(may be null) Optional array of 4 blend values |

### setRepeatMirror

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRepeatMirror(
    repeatCount: Float, 
    mirror: Boolean
): Unit
```

Set a repeat count (which may be fractional) for the interpolator, and whether the interpolator should mirror its repeats. The default settings are repeatCount = 1, and mirror = false. 

### timeToValues

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun timeToValues(values: FloatArray!): Interpolator.Result!
```

Calls timeToValues(msec, values) with the msec set to now (by calling (int)SystemClock.uptimeMillis().) 

### timeToValues

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun timeToValues(
    msec: Int, 
    values: FloatArray!
): Interpolator.Result!
```

Given a millisecond time value (msec), return the interpolated values and return whether the specified time was within the range of key times (NORMAL), was before the first key time (FREEZE_START) or after the last key time (FREEZE_END). In any event, computed values are always returned.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `msec` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The time (in milliseconds) used to sample into the Interpolator. Based on the SystemClock.uptimeMillis() clock |
| `values` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:Where to write the computed values (may be NULL). |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Interpolator.Result](../android/graphics/Interpolator.Result.md)! | how the values were computed (even if values == null) |

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |

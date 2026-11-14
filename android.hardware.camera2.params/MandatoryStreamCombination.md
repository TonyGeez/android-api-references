# MandatoryStreamCombination

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MandatoryStreamCombination

Kotlin| [Java](https://developer.android.com/reference/android/hardware/camera2/params/MandatoryStreamCombination "View this page in Java") 
| --- | --- |

```
class MandatoryStreamCombination
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.params.MandatoryStreamCombination](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination#) |

Immutable class to store the available mandatory stream combination.

A mandatory stream combination refers to a specific entry in the documented sets of required stream android.hardware.camera2.CameraDevice#createCaptureSession. These combinations of streams are required to be supported by the camera device.

The list of stream combinations is available by invoking [CameraCharacteristics.get](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#get(android.hardware.camera2.CameraCharacteristics.Key))and passing key [android.hardware.camera2.CameraCharacteristics#SCALER_MANDATORY_STREAM_COMBINATIONS](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SCALER_MANDATORY_STREAM_COMBINATIONS:android.hardware.camera2.CameraCharacteristics.Key).

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [MandatoryStreamInformation](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination.MandatoryStreamInformation) Immutable class to store available mandatory stream information. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Check if this [MandatoryStreamCombination](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination#) is equal to another [MandatoryStreamCombination](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination#). |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getDescription](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination#getDescription())`()` Get the mandatory stream combination description. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MandatoryStreamCombination.MandatoryStreamInformation](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination.MandatoryStreamInformation)!\> | [getStreamsInformation](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination#getStreamsInformation())`()` Get information about each stream in the mandatory combination. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination#hashCode())`()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReprocessable](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination#isReprocessable())`()` Indicates whether the mandatory stream combination is reprocessable. |

## Public methods

### equals

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Check if this [MandatoryStreamCombination](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination#) is equal to another [MandatoryStreamCombination](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination#).

Two vectors are only equal if and only if each of the respective elements is equal.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the objects were equal,`false`otherwise |

### getDescription

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDescription(): CharSequence
```

Get the mandatory stream combination description.

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | CharSequence with the mandatory combination description. This value cannot be`null`. |

### getStreamsInformation

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStreamsInformation(): MutableList<MandatoryStreamCombination.MandatoryStreamInformation!>
```

Get information about each stream in the mandatory combination.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MandatoryStreamCombination.MandatoryStreamInformation](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination.MandatoryStreamInformation)!> | Non-modifiable list of stream information. This value cannot be`null`. |

### hashCode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### isReprocessable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isReprocessable(): Boolean
```

Indicates whether the mandatory stream combination is reprocessable. Reprocessable is defined as a stream combination that contains one input stream ([MandatoryStreamInformation.isInput](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination.MandatoryStreamInformation#isInput())return true).

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`in case the mandatory stream combination contains an input,`false`otherwise. |

# MandatoryStreamCombination

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MandatoryStreamCombination

Kotlin| [Java](MandatoryStreamCombination.md) 
| --- | --- |

```
class MandatoryStreamCombination
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.params.MandatoryStreamCombination](MandatoryStreamCombination.md) |

Immutable class to store the available mandatory stream combination.

A mandatory stream combination refers to a specific entry in the documented sets of required stream android.hardware.camera2.CameraDevice#createCaptureSession. These combinations of streams are required to be supported by the camera device.

The list of stream combinations is available by invoking [CameraCharacteristics.get](../android.hardware.camera2/CameraCharacteristics.md))and passing key [android.hardware.camera2.CameraCharacteristics#SCALER_MANDATORY_STREAM_COMBINATIONS](../android.hardware.camera2/CameraCharacteristics.md).

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [MandatoryStreamInformation](../android/hardware/camera2/params/MandatoryStreamCombination.MandatoryStreamInformation.md) Immutable class to store available mandatory stream information. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](MandatoryStreamCombination.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Check if this [MandatoryStreamCombination](MandatoryStreamCombination.md) is equal to another [MandatoryStreamCombination](MandatoryStreamCombination.md). |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getDescription](MandatoryStreamCombination.md))`()` Get the mandatory stream combination description. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MandatoryStreamCombination.MandatoryStreamInformation](../android/hardware/camera2/params/MandatoryStreamCombination.MandatoryStreamInformation.md)!\> | [getStreamsInformation](MandatoryStreamCombination.md))`()` Get information about each stream in the mandatory combination. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](MandatoryStreamCombination.md))`()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReprocessable](MandatoryStreamCombination.md))`()` Indicates whether the mandatory stream combination is reprocessable. |

## Public methods

### equals

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Check if this [MandatoryStreamCombination](MandatoryStreamCombination.md) is equal to another [MandatoryStreamCombination](MandatoryStreamCombination.md).

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
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MandatoryStreamCombination.MandatoryStreamInformation](../android/hardware/camera2/params/MandatoryStreamCombination.MandatoryStreamInformation.md)!> | Non-modifiable list of stream information. This value cannot be`null`. |

### hashCode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### isReprocessable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isReprocessable(): Boolean
```

Indicates whether the mandatory stream combination is reprocessable. Reprocessable is defined as a stream combination that contains one input stream ([MandatoryStreamInformation.isInput](../android/hardware/camera2/params/MandatoryStreamCombination.MandatoryStreamInformation.md))return true).

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`in case the mandatory stream combination contains an input,`false`otherwise. |

# ConsumerIrManager

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConsumerIrManager

Kotlin| [Java](ConsumerIrManager.md) 
| --- | --- |

```
class ConsumerIrManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.ConsumerIrManager](ConsumerIrManager.md) |

Class that operates consumer infrared on the device. 
Requires the [PackageManager#FEATURE_CONSUMER_IR](../android.content.pm/PackageManager.md) feature which can be detected using [PackageManager.hasSystemFeature(String)](../android.content.pm/PackageManager.md)).

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [CarrierFrequencyRange](../android/hardware/ConsumerIrManager.CarrierFrequencyRange.md) Represents a range of carrier frequencies (inclusive) on which the infrared transmitter can transmit |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ConsumerIrManager.CarrierFrequencyRange](../android/hardware/ConsumerIrManager.CarrierFrequencyRange.md)!\>! | [getCarrierFrequencies](ConsumerIrManager.md))`()` Query the infrared transmitter's supported carrier frequencies |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasIrEmitter](ConsumerIrManager.md))`()` Check whether the device has an infrared emitter. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [transmit](ConsumerIrManager.md))`(`carrierFrequency:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pattern:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Transmit an infrared pattern |
| --- | --- |

## Public methods

### getCarrierFrequencies

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCarrierFrequencies(): Array<ConsumerIrManager.CarrierFrequencyRange!>!
```

Query the infrared transmitter's supported carrier frequencies

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ConsumerIrManager.CarrierFrequencyRange](../android/hardware/ConsumerIrManager.CarrierFrequencyRange.md)!>! | an array of [android.hardware.ConsumerIrManager.CarrierFrequencyRange](../android/hardware/ConsumerIrManager.CarrierFrequencyRange.md) objects representing the ranges that the transmitter can support, or null if there was an error communicating with the Consumer IR Service. |

### hasIrEmitter

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasIrEmitter(): Boolean
```

Check whether the device has an infrared emitter.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the device has an infrared emitter, else false. |

### transmit

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun transmit(
    carrierFrequency: Int, 
    pattern: IntArray!
): Unit
```

Transmit an infrared pattern

This method is synchronous; when it returns the pattern has been transmitted. Only patterns shorter than 2 seconds will be transmitted.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `carrierFrequency` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The IR carrier frequency in Hertz. |
| `pattern` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The alternating on/off pattern in microseconds to transmit. |

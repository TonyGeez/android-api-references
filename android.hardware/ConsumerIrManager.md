# ConsumerIrManager

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConsumerIrManager

Kotlin| [Java](https://developer.android.com/reference/android/hardware/ConsumerIrManager "View this page in Java") 

```
class ConsumerIrManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.ConsumerIrManager](https://developer.android.com/reference/kotlin/android/hardware/ConsumerIrManager#) |

Class that operates consumer infrared on the device. 
Requires the [PackageManager#FEATURE_CONSUMER_IR](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_CONSUMER_IR:kotlin.String) feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [CarrierFrequencyRange](https://developer.android.com/reference/kotlin/android/hardware/ConsumerIrManager.CarrierFrequencyRange) Represents a range of carrier frequencies (inclusive) on which the infrared transmitter can transmit |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ConsumerIrManager.CarrierFrequencyRange](https://developer.android.com/reference/kotlin/android/hardware/ConsumerIrManager.CarrierFrequencyRange)!\>! | [getCarrierFrequencies](https://developer.android.com/reference/kotlin/android/hardware/ConsumerIrManager#getCarrierFrequencies())`()` Query the infrared transmitter's supported carrier frequencies |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasIrEmitter](https://developer.android.com/reference/kotlin/android/hardware/ConsumerIrManager#hasIrEmitter())`()` Check whether the device has an infrared emitter. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [transmit](https://developer.android.com/reference/kotlin/android/hardware/ConsumerIrManager#transmit(kotlin.Int,%20kotlin.IntArray))`(`carrierFrequency:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pattern:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Transmit an infrared pattern |

## Public methods

### getCarrierFrequencies

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCarrierFrequencies(): Array<ConsumerIrManager.CarrierFrequencyRange!>!
```

Query the infrared transmitter's supported carrier frequencies

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ConsumerIrManager.CarrierFrequencyRange](https://developer.android.com/reference/kotlin/android/hardware/ConsumerIrManager.CarrierFrequencyRange)!>! | an array of [android.hardware.ConsumerIrManager.CarrierFrequencyRange](https://developer.android.com/reference/kotlin/android/hardware/ConsumerIrManager.CarrierFrequencyRange) objects representing the ranges that the transmitter can support, or null if there was an error communicating with the Consumer IR Service. |

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

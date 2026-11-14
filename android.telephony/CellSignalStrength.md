# CellSignalStrength

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CellSignalStrength

Kotlin| [Java](../android/telephony/CellSignalStrength.md) 
| --- | --- |

```
abstract class CellSignalStrength
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.CellSignalStrength](../android/telephony/CellSignalStrength.md) |

| Known Direct Subclasses [CellSignalStrengthCdma](../android/telephony/CellSignalStrengthCdma.md), [CellSignalStrengthGsm](../android/telephony/CellSignalStrengthGsm.md), [CellSignalStrengthLte](../android/telephony/CellSignalStrengthLte.md), [CellSignalStrengthNr](../android/telephony/CellSignalStrengthNr.md), [CellSignalStrengthTdscdma](../android/telephony/CellSignalStrengthTdscdma.md), [CellSignalStrengthWcdma](../android/telephony/CellSignalStrengthWcdma.md) |-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------| | [CellSignalStrengthCdma](../android/telephony/CellSignalStrengthCdma.md) | Signal strength related information. | | [CellSignalStrengthGsm](../android/telephony/CellSignalStrengthGsm.md) | GSM signal strength related information. | | [CellSignalStrengthLte](../android/telephony/CellSignalStrengthLte.md) | LTE signal strength related information. | | [CellSignalStrengthNr](../android/telephony/CellSignalStrengthNr.md) | 5G NR signal strength related information. | | [CellSignalStrengthTdscdma](../android/telephony/CellSignalStrengthTdscdma.md) | Tdscdma signal strength related information. | | [CellSignalStrengthWcdma](../android/telephony/CellSignalStrengthWcdma.md) | Wcdma signal strength related information. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Abstract base class for cell phone signal strength related information.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_GOOD](../android/telephony/CellSignalStrength.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_GREAT](../android/telephony/CellSignalStrength.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_MODERATE](../android/telephony/CellSignalStrength.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_NONE_OR_UNKNOWN](../android/telephony/CellSignalStrength.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_POOR](../android/telephony/CellSignalStrength.md) <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/telephony/CellSignalStrength.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAsuLevel](../android/telephony/CellSignalStrength.md))`()` Get the technology-specific signal strength in Arbitrary Strength Units, calculated from the strength of the pilot signal or equivalent. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDbm](../android/telephony/CellSignalStrength.md))`()` Get the technology-specific signal strength in dBm, which is the signal strength of the pilot signal or equivalent. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLevel](../android/telephony/CellSignalStrength.md))`()` Retrieve an abstract level value for the overall signal quality. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/telephony/CellSignalStrength.md))`()` <br /> |

## Constants

### SIGNAL_STRENGTH_GOOD

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_STRENGTH_GOOD: Int
```  

 Value: 3

### SIGNAL_STRENGTH_GREAT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_STRENGTH_GREAT: Int
```  

 Value: 4

### SIGNAL_STRENGTH_MODERATE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_STRENGTH_MODERATE: Int
```  

 Value: 2

### SIGNAL_STRENGTH_NONE_OR_UNKNOWN

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_STRENGTH_NONE_OR_UNKNOWN: Int
```  

 Value: 0

### SIGNAL_STRENGTH_POOR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_STRENGTH_POOR: Int
```  

 Value: 1

## Public methods

### equals

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAsuLevel

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAsuLevel(): Int
```

Get the technology-specific signal strength in Arbitrary Strength Units, calculated from the strength of the pilot signal or equivalent. 

### getDbm

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDbm(): Int
```

Get the technology-specific signal strength in dBm, which is the signal strength of the pilot signal or equivalent. 

### getLevel

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLevel(): Int
```

Retrieve an abstract level value for the overall signal quality.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a single integer from 0 to 4 representing the general signal quality. 0 represents very poor or unknown signal quality while 4 represents excellent signal quality. Value is between [android.telephony.CellSignalStrength#SIGNAL_STRENGTH_NONE_OR_UNKNOWN](../android/telephony/CellSignalStrength.md) and [android.telephony.CellSignalStrength#SIGNAL_STRENGTH_GREAT](../android/telephony/CellSignalStrength.md) inclusive |

### hashCode

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

# CellSignalStrength

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CellSignalStrength

Kotlin| [Java](https://developer.android.com/reference/android/telephony/CellSignalStrength "View this page in Java") 

```
abstract class CellSignalStrength
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.CellSignalStrength](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#) |

| Known Direct Subclasses [CellSignalStrengthCdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthCdma), [CellSignalStrengthGsm](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm), [CellSignalStrengthLte](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthLte), [CellSignalStrengthNr](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr), [CellSignalStrengthTdscdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthTdscdma), [CellSignalStrengthWcdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthWcdma) |-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------| | [CellSignalStrengthCdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthCdma) | Signal strength related information. | | [CellSignalStrengthGsm](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm) | GSM signal strength related information. | | [CellSignalStrengthLte](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthLte) | LTE signal strength related information. | | [CellSignalStrengthNr](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr) | 5G NR signal strength related information. | | [CellSignalStrengthTdscdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthTdscdma) | Tdscdma signal strength related information. | | [CellSignalStrengthWcdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthWcdma) | Wcdma signal strength related information. | |

Abstract base class for cell phone signal strength related information.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_GOOD](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#SIGNAL_STRENGTH_GOOD:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_GREAT](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#SIGNAL_STRENGTH_GREAT:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_MODERATE](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#SIGNAL_STRENGTH_MODERATE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_NONE_OR_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#SIGNAL_STRENGTH_NONE_OR_UNKNOWN:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_POOR](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#SIGNAL_STRENGTH_POOR:kotlin.Int) <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAsuLevel](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#getAsuLevel())`()` Get the technology-specific signal strength in Arbitrary Strength Units, calculated from the strength of the pilot signal or equivalent. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDbm](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#getDbm())`()` Get the technology-specific signal strength in dBm, which is the signal strength of the pilot signal or equivalent. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLevel](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#getLevel())`()` Retrieve an abstract level value for the overall signal quality. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#hashCode())`()` <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a single integer from 0 to 4 representing the general signal quality. 0 represents very poor or unknown signal quality while 4 represents excellent signal quality. Value is between [android.telephony.CellSignalStrength#SIGNAL_STRENGTH_NONE_OR_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#SIGNAL_STRENGTH_NONE_OR_UNKNOWN:kotlin.Int) and [android.telephony.CellSignalStrength#SIGNAL_STRENGTH_GREAT](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#SIGNAL_STRENGTH_GREAT:kotlin.Int) inclusive |

### hashCode

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

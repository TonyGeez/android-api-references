Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# CervicalMucusRecord

```
class CervicalMucusRecord : InstantRecord
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [android.health.connect.datatypes.Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record) |||
| | ↳ | [android.health.connect.datatypes.InstantRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord) ||
| | | ↳ | [android.health.connect.datatypes.CervicalMucusRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord#) |

Captures the description of cervical mucus. Each record represents a self-assessed description of cervical mucus for a user. All fields are optional and can be used to describe the look and feel of cervical mucus.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord.Builder` Builder class for `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord#` |
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord.CervicalMucusAppearance` Identifier for Cervical Mucus Appearance |
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord.CervicalMucusSensation` Identifier for Cervical Mucus Sensation |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord#getAppearance()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord#getSensation()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord#hashCode()()` Returns a hash code value for the object. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Metadata` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#getMetadata()()` <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord` |---|---| | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord#getTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord#getZoneOffset()()` <br /> | ||

## Public methods

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `object` | the reference object with which to compare. This value may be `null`. |
| `o` | the reference object with which to compare. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj |

### getAppearance

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getAppearance(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | appearance. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord.CervicalMucusAppearance#APPEARANCE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord.CervicalMucusAppearance#APPEARANCE_DRY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord.CervicalMucusAppearance#APPEARANCE_STICKY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord.CervicalMucusAppearance#APPEARANCE_CREAMY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord.CervicalMucusAppearance#APPEARANCE_WATERY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord.CervicalMucusAppearance#APPEARANCE_EGG_WHITE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord.CervicalMucusAppearance#APPEARANCE_UNUSUAL:kotlin.Int` |

### getSensation

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getSensation(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | sensation. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord.CervicalMucusSensation#SENSATION_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord.CervicalMucusSensation#SENSATION_LIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord.CervicalMucusSensation#SENSATION_MEDIUM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord.CervicalMucusSensation#SENSATION_HEAVY:kotlin.Int` |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

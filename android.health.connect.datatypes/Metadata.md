# Metadata

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Metadata

Kotlin| [Java](../android/health/connect/datatypes/Metadata.md) 
| --- | --- |

```
class Metadata
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.datatypes.Metadata](../android/health/connect/datatypes/Metadata.md) |

Set of shared metadata fields for [Record](../android/health/connect/datatypes/Record.md)

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/health/connect/datatypes/Metadata.Builder.md) <br /> |

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RECORDING_METHOD_ACTIVELY_RECORDED](../android/health/connect/datatypes/Metadata.md) For actively recorded data by the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RECORDING_METHOD_AUTOMATICALLY_RECORDED](../android/health/connect/datatypes/Metadata.md) For passively recorded data by the app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RECORDING_METHOD_MANUAL_ENTRY](../android/health/connect/datatypes/Metadata.md) For manually entered data by the user. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RECORDING_METHOD_UNKNOWN](../android/health/connect/datatypes/Metadata.md) Unknown recording method. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/health/connect/datatypes/Metadata.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getClientRecordId](../android/health/connect/datatypes/Metadata.md))`()` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getClientRecordVersion](../android/health/connect/datatypes/Metadata.md))`()` <br /> |
| --- | --- |
| [DataOrigin](../android/health/connect/datatypes/DataOrigin.md) | [getDataOrigin](../android/health/connect/datatypes/Metadata.md))`()` <br /> |
| [Device](../android/health/connect/datatypes/Device.md) | [getDevice](../android/health/connect/datatypes/Metadata.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getId](../android/health/connect/datatypes/Metadata.md))`()` <br /> |
| --- | --- |
| [Instant](../java/time/Instant.md) | [getLastModifiedTime](../android/health/connect/datatypes/Metadata.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRecordingMethod](../android/health/connect/datatypes/Metadata.md))`()` Returns recording method which indicates how data was recorded for the [Record](../android/health/connect/datatypes/Record.md) |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/health/connect/datatypes/Metadata.md))`()` Returns a hash code value for the object. |
| --- | --- |

## Constants

### RECORDING_METHOD_ACTIVELY_RECORDED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RECORDING_METHOD_ACTIVELY_RECORDED: Int
```

For actively recorded data by the user.

For e.g. An exercise session actively recorded by the user using a phone or a watch device. 

 Value: 1

### RECORDING_METHOD_AUTOMATICALLY_RECORDED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RECORDING_METHOD_AUTOMATICALLY_RECORDED: Int
```

For passively recorded data by the app.

For e.g. Steps data recorded by a watch or phone without the user starting a session. 

 Value: 2

### RECORDING_METHOD_MANUAL_ENTRY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RECORDING_METHOD_MANUAL_ENTRY: Int
```

For manually entered data by the user.

For e.g. Nutrition or weight data entered by the user. 

 Value: 3

### RECORDING_METHOD_UNKNOWN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RECORDING_METHOD_UNKNOWN: Int
```

Unknown recording method. 

 Value: 0

## Public methods

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

| Parameters ||
|----------|----------------------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `object` | the reference object with which to compare. This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj |

### getClientRecordId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientRecordId(): String?
```

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | Client record ID if set, null otherwise |

### getClientRecordVersion

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientRecordVersion(): Long
```

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Client record version if set, 0 otherwise |

### getDataOrigin

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDataOrigin(): DataOrigin
```

| Return ||
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [DataOrigin](../android/health/connect/datatypes/DataOrigin.md) | Corresponds to package name if set. If no data origin is set`getDataOrigin().getPackageName()`will return null |

### getDevice

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDevice(): Device
```

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Device](../android/health/connect/datatypes/Device.md) | The device details that contributed to this record This value cannot be`null`. |

### getId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): String
```

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | Record identifier if set, empty string otherwise This value cannot be`null`. |

### getLastModifiedTime

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLastModifiedTime(): Instant
```

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Instant](../java/time/Instant.md) | Record's last modified time if set, Instant.EPOCH otherwise This value cannot be`null`. |

### getRecordingMethod

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRecordingMethod(): Int
```

Returns recording method which indicates how data was recorded for the [Record](../android/health/connect/datatypes/Record.md)

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.health.connect.datatypes.Metadata#RECORDING_METHOD_UNKNOWN](../android/health/connect/datatypes/Metadata.md), [android.health.connect.datatypes.Metadata#RECORDING_METHOD_ACTIVELY_RECORDED](../android/health/connect/datatypes/Metadata.md), [android.health.connect.datatypes.Metadata#RECORDING_METHOD_AUTOMATICALLY_RECORDED](../android/health/connect/datatypes/Metadata.md), or [android.health.connect.datatypes.Metadata#RECORDING_METHOD_MANUAL_ENTRY](../android/health/connect/datatypes/Metadata.md) |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code value for the object.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

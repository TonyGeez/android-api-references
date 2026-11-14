# ProviderProperties

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProviderProperties

Kotlin| [Java](https://developer.android.com/reference/android/location/provider/ProviderProperties "View this page in Java") 
| --- | --- |

```
class ProviderProperties : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.location.provider.ProviderProperties](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#) |

Location provider properties.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties.Builder) Builder for ProviderProperties. |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCURACY_COARSE](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#ACCURACY_COARSE:kotlin.Int) A constant indicating a coarser location accuracy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCURACY_FINE](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#ACCURACY_FINE:kotlin.Int) A constant indicating a finer location accuracy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POWER_USAGE_HIGH](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#POWER_USAGE_HIGH:kotlin.Int) A constant indicating high power usage. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POWER_USAGE_LOW](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#POWER_USAGE_LOW:kotlin.Int) A constant indicating low power usage. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POWER_USAGE_MEDIUM](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#POWER_USAGE_MEDIUM:kotlin.Int) A constant indicating a medium power usage. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAccuracy](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#getAccuracy())`()` Rough location accuracy for this provider, primarily with respect to horizontal location accuracy. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPowerUsage](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#getPowerUsage())`()` Power usage for this provider. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAltitudeSupport](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#hasAltitudeSupport())`()` True if the provider is able to provide altitude under at least some conditions. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasBearingSupport](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#hasBearingSupport())`()` True if the provider is able to provide bearing under at least some conditions. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasCellRequirement](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#hasCellRequirement())`()` True if the provider requires access to a cellular network (e.g., for cell tower IDs). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMonetaryCost](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#hasMonetaryCost())`()` True if this provider may result in a monetary charge to the user. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasNetworkRequirement](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#hasNetworkRequirement())`()` True if provider requires access to a data network (e.g., the Internet). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasSatelliteRequirement](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#hasSatelliteRequirement())`()` True if the provider requires access to a satellite-based positioning system (e.g., GPS). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasSpeedSupport](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#hasSpeedSupport())`()` True if the provider is able to provide speed under at least some conditions. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#hashCode())`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ProviderProperties](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### ACCURACY_COARSE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCURACY_COARSE: Int
```

A constant indicating a coarser location accuracy. 

 Value: 2

### ACCURACY_FINE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCURACY_FINE: Int
```

A constant indicating a finer location accuracy. 

 Value: 1

### POWER_USAGE_HIGH

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POWER_USAGE_HIGH: Int
```

A constant indicating high power usage. 

 Value: 3

### POWER_USAGE_LOW

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POWER_USAGE_LOW: Int
```

A constant indicating low power usage. 

 Value: 1

### POWER_USAGE_MEDIUM

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POWER_USAGE_MEDIUM: Int
```

A constant indicating a medium power usage. 

 Value: 2

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAccuracy

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAccuracy(): Int
```

Rough location accuracy for this provider, primarily with respect to horizontal location accuracy.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.location.provider.ProviderProperties#ACCURACY_FINE](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#ACCURACY_FINE:kotlin.Int), or [android.location.provider.ProviderProperties#ACCURACY_COARSE](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#ACCURACY_COARSE:kotlin.Int) |

### getPowerUsage

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPowerUsage(): Int
```

Power usage for this provider.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.location.provider.ProviderProperties#POWER_USAGE_LOW](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#POWER_USAGE_LOW:kotlin.Int), [android.location.provider.ProviderProperties#POWER_USAGE_MEDIUM](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#POWER_USAGE_MEDIUM:kotlin.Int), or [android.location.provider.ProviderProperties#POWER_USAGE_HIGH](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#POWER_USAGE_HIGH:kotlin.Int) |

### hasAltitudeSupport

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasAltitudeSupport(): Boolean
```

True if the provider is able to provide altitude under at least some conditions. 

### hasBearingSupport

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasBearingSupport(): Boolean
```

True if the provider is able to provide bearing under at least some conditions. 

### hasCellRequirement

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasCellRequirement(): Boolean
```

True if the provider requires access to a cellular network (e.g., for cell tower IDs). 

### hasMonetaryCost

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasMonetaryCost(): Boolean
```

True if this provider may result in a monetary charge to the user. Network usage is not considered a monetary cost. 

### hasNetworkRequirement

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasNetworkRequirement(): Boolean
```

True if provider requires access to a data network (e.g., the Internet). 

### hasSatelliteRequirement

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasSatelliteRequirement(): Boolean
```

True if the provider requires access to a satellite-based positioning system (e.g., GPS). 

### hasSpeedSupport

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasSpeedSupport(): Boolean
```

True if the provider is able to provide speed under at least some conditions. 

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
| `parcel` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ProviderProperties!>
```

# ConfigurationStats

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConfigurationStats

Kotlin| [Java](https://developer.android.com/reference/android/app/usage/ConfigurationStats "View this page in Java") 
| --- | --- |

```
class ConfigurationStats : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.usage.ConfigurationStats](https://developer.android.com/reference/kotlin/android/app/usage/ConfigurationStats#) |

Represents the usage statistics of a device [android.content.res.Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#) for a specific time range.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ConfigurationStats](https://developer.android.com/reference/kotlin/android/app/usage/ConfigurationStats#ConfigurationStats(android.app.usage.ConfigurationStats))`(`stats:` ` [ConfigurationStats](https://developer.android.com/reference/kotlin/android/app/usage/ConfigurationStats#)!`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/usage/ConfigurationStats#describeContents())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getActivationCount](https://developer.android.com/reference/kotlin/android/app/usage/ConfigurationStats#getActivationCount())`()` Get the number of times this configuration was active. |
| [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)! | [getConfiguration](https://developer.android.com/reference/kotlin/android/app/usage/ConfigurationStats#getConfiguration())`()` <br /> |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFirstTimeStamp](https://developer.android.com/reference/kotlin/android/app/usage/ConfigurationStats#getFirstTimeStamp())`()` Get the beginning of the time range this [ConfigurationStats](https://developer.android.com/reference/kotlin/android/app/usage/ConfigurationStats#) represents, measured in milliseconds since the epoch. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLastTimeActive](https://developer.android.com/reference/kotlin/android/app/usage/ConfigurationStats#getLastTimeActive())`()` Get the last time this configuration was active, measured in milliseconds since the epoch. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLastTimeStamp](https://developer.android.com/reference/kotlin/android/app/usage/ConfigurationStats#getLastTimeStamp())`()` Get the end of the time range this [ConfigurationStats](https://developer.android.com/reference/kotlin/android/app/usage/ConfigurationStats#) represents, measured in milliseconds since the epoch. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTotalTimeActive](https://developer.android.com/reference/kotlin/android/app/usage/ConfigurationStats#getTotalTimeActive())`()` Get the total time this configuration was active, measured in milliseconds. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/usage/ConfigurationStats#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ConfigurationStats](https://developer.android.com/reference/kotlin/android/app/usage/ConfigurationStats#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/usage/ConfigurationStats#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### ConfigurationStats

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConfigurationStats(stats: ConfigurationStats!)
```

## Public methods

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getActivationCount

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActivationCount(): Int
```

Get the number of times this configuration was active. 

### getConfiguration

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConfiguration(): Configuration!
```  

### getFirstTimeStamp

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFirstTimeStamp(): Long
```

Get the beginning of the time range this [ConfigurationStats](https://developer.android.com/reference/kotlin/android/app/usage/ConfigurationStats#) represents, measured in milliseconds since the epoch.

<br />

See [System.currentTimeMillis()](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()). 

### getLastTimeActive

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLastTimeActive(): Long
```

Get the last time this configuration was active, measured in milliseconds since the epoch.

<br />

See [System.currentTimeMillis()](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()). 

### getLastTimeStamp

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLastTimeStamp(): Long
```

Get the end of the time range this [ConfigurationStats](https://developer.android.com/reference/kotlin/android/app/usage/ConfigurationStats#) represents, measured in milliseconds since the epoch.

<br />

See [System.currentTimeMillis()](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()). 

### getTotalTimeActive

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTotalTimeActive(): Long
```

Get the total time this configuration was active, measured in milliseconds. 

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ConfigurationStats!>
```

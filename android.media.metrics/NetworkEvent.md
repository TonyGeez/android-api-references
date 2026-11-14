# NetworkEvent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NetworkEvent

Kotlin| [Java](https://developer.android.com/reference/android/media/metrics/NetworkEvent "View this page in Java") 

```
class NetworkEvent : Event, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.media.metrics.Event](https://developer.android.com/reference/kotlin/android/media/metrics/Event) ||
| | ↳ | [android.media.metrics.NetworkEvent](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#) |

Media network event.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent.Builder) A builder for [NetworkEvent](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#) |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NETWORK_TYPE_2G](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#NETWORK_TYPE_2G:kotlin.Int) 2G network |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NETWORK_TYPE_3G](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#NETWORK_TYPE_3G:kotlin.Int) 3G network |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NETWORK_TYPE_4G](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#NETWORK_TYPE_4G:kotlin.Int) 4G network |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NETWORK_TYPE_5G_NSA](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#NETWORK_TYPE_5G_NSA:kotlin.Int) 5G NSA network |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NETWORK_TYPE_5G_SA](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#NETWORK_TYPE_5G_SA:kotlin.Int) 5G SA network |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NETWORK_TYPE_ETHERNET](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#NETWORK_TYPE_ETHERNET:kotlin.Int) Ethernet network |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NETWORK_TYPE_OFFLINE](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#NETWORK_TYPE_OFFLINE:kotlin.Int) Not network connected |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NETWORK_TYPE_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#NETWORK_TYPE_OTHER:kotlin.Int) Other network type |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NETWORK_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#NETWORK_TYPE_UNKNOWN:kotlin.Int) Network type is not known. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NETWORK_TYPE_WIFI](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#NETWORK_TYPE_WIFI:kotlin.Int) Wi-Fi network |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getMetricsBundle](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#getMetricsBundle())`()` Gets metrics-related information that is not supported by dedicated methods. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNetworkType](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#getNetworkType())`()` Gets network type. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimeSinceCreatedMillis](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#getTimeSinceCreatedMillis())`()` Gets timestamp since the creation of the log session in milliseconds. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [NetworkEvent](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#CREATOR:android.os.Parcelable.Creator) Used to read a NetworkEvent from a Parcel. |

## Constants

### NETWORK_TYPE_2G

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NETWORK_TYPE_2G: Int
```

2G network 

 Value: 4

### NETWORK_TYPE_3G

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NETWORK_TYPE_3G: Int
```

3G network 

 Value: 5

### NETWORK_TYPE_4G

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NETWORK_TYPE_4G: Int
```

4G network 

 Value: 6

### NETWORK_TYPE_5G_NSA

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NETWORK_TYPE_5G_NSA: Int
```

5G NSA network 

 Value: 7

### NETWORK_TYPE_5G_SA

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NETWORK_TYPE_5G_SA: Int
```

5G SA network 

 Value: 8

### NETWORK_TYPE_ETHERNET

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NETWORK_TYPE_ETHERNET: Int
```

Ethernet network 

 Value: 3

### NETWORK_TYPE_OFFLINE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NETWORK_TYPE_OFFLINE: Int
```

Not network connected 

 Value: 9

### NETWORK_TYPE_OTHER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NETWORK_TYPE_OTHER: Int
```

Other network type 

 Value: 1

### NETWORK_TYPE_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NETWORK_TYPE_UNKNOWN: Int
```

Network type is not known. Default type. 

 Value: 0

### NETWORK_TYPE_WIFI

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NETWORK_TYPE_WIFI: Int
```

Wi-Fi network 

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

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getMetricsBundle

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMetricsBundle(): Bundle
```

Gets metrics-related information that is not supported by dedicated methods.

It is intended to be used for backwards compatibility by the metrics infrastructure.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | This value cannot be`null`. |

### getNetworkType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNetworkType(): Int
```

Gets network type.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.metrics.NetworkEvent#NETWORK_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#NETWORK_TYPE_UNKNOWN:kotlin.Int), [android.media.metrics.NetworkEvent#NETWORK_TYPE_OTHER](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#NETWORK_TYPE_OTHER:kotlin.Int), [android.media.metrics.NetworkEvent#NETWORK_TYPE_WIFI](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#NETWORK_TYPE_WIFI:kotlin.Int), [android.media.metrics.NetworkEvent#NETWORK_TYPE_ETHERNET](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#NETWORK_TYPE_ETHERNET:kotlin.Int), [android.media.metrics.NetworkEvent#NETWORK_TYPE_2G](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#NETWORK_TYPE_2G:kotlin.Int), [android.media.metrics.NetworkEvent#NETWORK_TYPE_3G](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#NETWORK_TYPE_3G:kotlin.Int), [android.media.metrics.NetworkEvent#NETWORK_TYPE_4G](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#NETWORK_TYPE_4G:kotlin.Int), [android.media.metrics.NetworkEvent#NETWORK_TYPE_5G_NSA](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#NETWORK_TYPE_5G_NSA:kotlin.Int), [android.media.metrics.NetworkEvent#NETWORK_TYPE_5G_SA](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#NETWORK_TYPE_5G_SA:kotlin.Int), or [android.media.metrics.NetworkEvent#NETWORK_TYPE_OFFLINE](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent#NETWORK_TYPE_OFFLINE:kotlin.Int) |

### getTimeSinceCreatedMillis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimeSinceCreatedMillis(): Long
```

Gets timestamp since the creation of the log session in milliseconds.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the timestamp since the creation in milliseconds, or -1 if unknown. Value is -1 or greater |

**See Also**

- [android.media.metrics.LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId)
- [android.media.metrics.PlaybackSession](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackSession)
- [android.media.metrics.RecordingSession](https://developer.android.com/reference/kotlin/android/media/metrics/RecordingSession) 

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
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<NetworkEvent!>
```

Used to read a NetworkEvent from a Parcel.

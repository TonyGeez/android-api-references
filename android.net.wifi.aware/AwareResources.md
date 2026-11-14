# AwareResources

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AwareResources

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/aware/AwareResources "View this page in Java") 

```
class AwareResources : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.wifi.aware.AwareResources](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwareResources#) |

The resources of the Aware service.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AwareResources](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwareResources#AwareResources(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`availableDataPathsCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `availablePublishSessionsCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `availableSubscribeSessionsCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Construct a [AwareResources](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwareResources#) object, which represents the currently available Aware resources. |

| Public methods ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwareResources#describeContents())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAvailableDataPathsCount](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwareResources#getAvailableDataPathsCount())`()` Return the number of Aware data-paths (also known as NDPs - NAN Data Paths) which an app could create. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAvailablePublishSessionsCount](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwareResources#getAvailablePublishSessionsCount())`()` Return the number of Aware publish sessions which an app could create. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAvailableSubscribeSessionsCount](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwareResources#getAvailableSubscribeSessionsCount())`()` Return the number of Aware subscribe sessions which an app could create. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwareResources#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AwareResources](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwareResources#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwareResources#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### AwareResources

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AwareResources(
    availableDataPathsCount: Int, 
    availablePublishSessionsCount: Int, 
    availableSubscribeSessionsCount: Int)
```

Construct a [AwareResources](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwareResources#) object, which represents the currently available Aware resources.

| Parameters ||
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `availableDataPathsCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of available Aware data-path. Value is 0 or greater |
| `availablePublishSessionsCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of available Aware publish sessions. Value is 0 or greater |
| `availableSubscribeSessionsCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of available Aware subscribe sessions. Value is 0 or greater |

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getAvailableDataPathsCount

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAvailableDataPathsCount(): Int
```

Return the number of Aware data-paths (also known as NDPs - NAN Data Paths) which an app could create. Please refer to the [WifiAwareNetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkSpecifier) to create a Network Specifier and request a data-path.

Note that these resources aren't reserved - other apps could use them by the time you attempt to create a data-path.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A Non-negative integer, number of data-paths that could be created. Value is 0 or greater |

### getAvailablePublishSessionsCount

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAvailablePublishSessionsCount(): Int
```

Return the number of Aware publish sessions which an app could create. Please refer to the [WifiAwareSession.publish(PublishConfig, DiscoverySessionCallback, Handler)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#publish(android.net.wifi.aware.PublishConfig,%20android.net.wifi.aware.DiscoverySessionCallback,%20android.os.Handler))to create a publish session.

Note that these resources aren't reserved - other apps could use them by the time you attempt to create a publish session.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A Non-negative integer, number of publish sessions that could be created. Value is 0 or greater |

### getAvailableSubscribeSessionsCount

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAvailableSubscribeSessionsCount(): Int
```

Return the number of Aware subscribe sessions which an app could create. Please refer to the [WifiAwareSession.subscribe(SubscribeConfig, DiscoverySessionCallback, Handler)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareSession#subscribe(android.net.wifi.aware.SubscribeConfig,%20android.net.wifi.aware.DiscoverySessionCallback,%20android.os.Handler))to create a subscribe session.

Note that these resources aren't reserved - other apps could use them by the time you attempt to create a subscribe session.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A Non-negative integer, number of subscribe sessions that could be created. Value is 0 or greater |

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
static val CREATOR: Parcelable.Creator<AwareResources!>
```

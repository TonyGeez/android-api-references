# AwareResources

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AwareResources

Kotlin| [Java](../android/net/wifi/aware/AwareResources.md) 
| --- | --- |

```
class AwareResources : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.aware.AwareResources](../android/net/wifi/aware/AwareResources.md) |

The resources of the Aware service.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AwareResources](../android/net/wifi/aware/AwareResources.md))`(`availableDataPathsCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `availablePublishSessionsCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `availableSubscribeSessionsCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Construct a [AwareResources](../android/net/wifi/aware/AwareResources.md) object, which represents the currently available Aware resources. |

| Public methods ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/net/wifi/aware/AwareResources.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAvailableDataPathsCount](../android/net/wifi/aware/AwareResources.md))`()` Return the number of Aware data-paths (also known as NDPs - NAN Data Paths) which an app could create. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAvailablePublishSessionsCount](../android/net/wifi/aware/AwareResources.md))`()` Return the number of Aware publish sessions which an app could create. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAvailableSubscribeSessionsCount](../android/net/wifi/aware/AwareResources.md))`()` Return the number of Aware subscribe sessions which an app could create. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/net/wifi/aware/AwareResources.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AwareResources](../android/net/wifi/aware/AwareResources.md)!\> | [CREATOR](../android/net/wifi/aware/AwareResources.md) <br /> |

## Public constructors

### AwareResources

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AwareResources(
    availableDataPathsCount: Int, 
    availablePublishSessionsCount: Int, 
    availableSubscribeSessionsCount: Int)
```

Construct a [AwareResources](../android/net/wifi/aware/AwareResources.md) object, which represents the currently available Aware resources.

| Parameters ||
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `availableDataPathsCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of available Aware data-path. Value is 0 or greater |
| `availablePublishSessionsCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of available Aware publish sessions. Value is 0 or greater |
| `availableSubscribeSessionsCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of available Aware subscribe sessions. Value is 0 or greater |
| --- | --- |

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getAvailableDataPathsCount

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAvailableDataPathsCount(): Int
```

Return the number of Aware data-paths (also known as NDPs - NAN Data Paths) which an app could create. Please refer to the [WifiAwareNetworkSpecifier](../android/net/wifi/aware/WifiAwareNetworkSpecifier.md) to create a Network Specifier and request a data-path.

Note that these resources aren't reserved - other apps could use them by the time you attempt to create a data-path.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A Non-negative integer, number of data-paths that could be created. Value is 0 or greater |

### getAvailablePublishSessionsCount

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAvailablePublishSessionsCount(): Int
```

Return the number of Aware publish sessions which an app could create. Please refer to the [WifiAwareSession.publish(PublishConfig, DiscoverySessionCallback, Handler)](../android/net/wifi/aware/WifiAwareSession.md))to create a publish session.

Note that these resources aren't reserved - other apps could use them by the time you attempt to create a publish session.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A Non-negative integer, number of publish sessions that could be created. Value is 0 or greater |

### getAvailableSubscribeSessionsCount

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAvailableSubscribeSessionsCount(): Int
```

Return the number of Aware subscribe sessions which an app could create. Please refer to the [WifiAwareSession.subscribe(SubscribeConfig, DiscoverySessionCallback, Handler)](../android/net/wifi/aware/WifiAwareSession.md))to create a subscribe session.

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
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AwareResources!>
```

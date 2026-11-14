# TvInteractiveAppServiceInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TvInteractiveAppServiceInfo

Kotlin| [Java](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md) 
| --- | --- |

```
class TvInteractiveAppServiceInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.tv.interactive.TvInteractiveAppServiceInfo](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md) |

This class is used to specify meta information of a TV interactive app.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERACTIVE_APP_TYPE_ATSC](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md) ATSC interactive app type |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERACTIVE_APP_TYPE_GINGA](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md) Ginga interactive app type |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERACTIVE_APP_TYPE_HBBTV](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md) HbbTV interactive app type |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERACTIVE_APP_TYPE_OTHER](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md) Other interactive app type |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERACTIVE_APP_TYPE_TARGETED_AD](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md) Targeted Advertisement interactive app type |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TvInteractiveAppServiceInfo](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md))`(`context:` ` [Context](../android/content/Context.md)`, `component:` ` [ComponentName](../android/content/ComponentName.md)`)` Constructs a TvInteractiveAppServiceInfo object. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md))`()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getCustomSupportedTypes](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md))`()` Gets custom supported interactive app types which are not listed. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getId](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md))`()` Returns a unique ID for this TV interactive app service. |
| --- | --- |
| [ServiceInfo](../android/content/pm/ServiceInfo.md)? | [getServiceInfo](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md))`()` Returns the information of the service that implements this TV Interactive App service. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSupportedTypes](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md))`()` Gets supported interactive app types. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [TvInteractiveAppServiceInfo](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md)!\> | [CREATOR](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md) <br /> |

## Constants

### INTERACTIVE_APP_TYPE_ATSC

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTERACTIVE_APP_TYPE_ATSC: Int
```

ATSC interactive app type 

 Value: 2

### INTERACTIVE_APP_TYPE_GINGA

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTERACTIVE_APP_TYPE_GINGA: Int
```

Ginga interactive app type 

 Value: 4

### INTERACTIVE_APP_TYPE_HBBTV

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTERACTIVE_APP_TYPE_HBBTV: Int
```

HbbTV interactive app type 

 Value: 1

### INTERACTIVE_APP_TYPE_OTHER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTERACTIVE_APP_TYPE_OTHER: Int
```

Other interactive app type 

 Value: -2147483648

### INTERACTIVE_APP_TYPE_TARGETED_AD

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTERACTIVE_APP_TYPE_TARGETED_AD: Int
```

Targeted Advertisement interactive app type 

 Value: 8

## Public constructors

### TvInteractiveAppServiceInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TvInteractiveAppServiceInfo(
    context: Context, 
    component: ComponentName)
```

Constructs a TvInteractiveAppServiceInfo object.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):the application context This value cannot be`null`. |
| `component` | [ComponentName](../android/content/ComponentName.md):the component name of the TvInteractiveAppService This value cannot be`null`. |

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getCustomSupportedTypes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCustomSupportedTypes(): MutableList<String!>
```

Gets custom supported interactive app types which are not listed.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#getSupportedTypes()> 

### getId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): String
```

Returns a unique ID for this TV interactive app service. The ID is generated from the package and class name implementing the TV interactive app service.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getServiceInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceInfo(): ServiceInfo?
```

Returns the information of the service that implements this TV Interactive App service.

| Return ||
|-----------------------------------------------------------------------------------------------------|--------------------------|
| [ServiceInfo](../android/content/pm/ServiceInfo.md)? | This value may be`null`. |

### getSupportedTypes

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSupportedTypes(): Int
```

Gets supported interactive app types.

The supported interactive app types is in a bit map format. For example: 

```kotlin
<code>
    int types = tvInteractiveAppInfo.getSupportedTypes();
    if (types &amp; TvInteractiveAppInfo.INTERACTIVE_APP_TYPE_HBBTV != 0) {
      // HbbTV type is supported. Do something...
    }
    if (types &amp; TvInteractiveAppInfo.INTERACTIVE_APP_TYPE_ATSC == 0) {
      // ATSC type is not supported. Do something...
    }
  </code>
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An int bit map representing supported types. Value is [android.media.tv.interactive.TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_HBBTV](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md), [android.media.tv.interactive.TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_ATSC](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md), [android.media.tv.interactive.TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_GINGA](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md), [android.media.tv.interactive.TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_TARGETED_AD](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md), or [android.media.tv.interactive.TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_OTHER](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md) This value cannot be`null`. |

### writeToParcel

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TvInteractiveAppServiceInfo!>
```

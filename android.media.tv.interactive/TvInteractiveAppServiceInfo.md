# TvInteractiveAppServiceInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TvInteractiveAppServiceInfo

Kotlin| [Java](https://developer.android.com/reference/android/media/tv/interactive/TvInteractiveAppServiceInfo "View this page in Java") 
| --- | --- |

```
class TvInteractiveAppServiceInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.tv.interactive.TvInteractiveAppServiceInfo](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#) |

This class is used to specify meta information of a TV interactive app.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERACTIVE_APP_TYPE_ATSC](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_ATSC:kotlin.Int) ATSC interactive app type |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERACTIVE_APP_TYPE_GINGA](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_GINGA:kotlin.Int) Ginga interactive app type |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERACTIVE_APP_TYPE_HBBTV](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_HBBTV:kotlin.Int) HbbTV interactive app type |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERACTIVE_APP_TYPE_OTHER](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_OTHER:kotlin.Int) Other interactive app type |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERACTIVE_APP_TYPE_TARGETED_AD](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_TARGETED_AD:kotlin.Int) Targeted Advertisement interactive app type |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TvInteractiveAppServiceInfo](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#TvInteractiveAppServiceInfo(android.content.Context,%20android.content.ComponentName))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `component:` ` [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)`)` Constructs a TvInteractiveAppServiceInfo object. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#describeContents())`()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getCustomSupportedTypes](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#getCustomSupportedTypes())`()` Gets custom supported interactive app types which are not listed. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getId](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#getId())`()` Returns a unique ID for this TV interactive app service. |
| --- | --- |
| [ServiceInfo](https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#)? | [getServiceInfo](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#getServiceInfo())`()` Returns the information of the service that implements this TV Interactive App service. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSupportedTypes](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#getSupportedTypes())`()` Gets supported interactive app types. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [TvInteractiveAppServiceInfo](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):the application context This value cannot be`null`. |
| `component` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#):the component name of the TvInteractiveAppService This value cannot be`null`. |

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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
| [ServiceInfo](https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#)? | This value may be`null`. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An int bit map representing supported types. Value is [android.media.tv.interactive.TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_HBBTV](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_HBBTV:kotlin.Int), [android.media.tv.interactive.TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_ATSC](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_ATSC:kotlin.Int), [android.media.tv.interactive.TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_GINGA](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_GINGA:kotlin.Int), [android.media.tv.interactive.TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_TARGETED_AD](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_TARGETED_AD:kotlin.Int), or [android.media.tv.interactive.TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_OTHER](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#INTERACTIVE_APP_TYPE_OTHER:kotlin.Int) This value cannot be`null`. |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TvInteractiveAppServiceInfo!>
```

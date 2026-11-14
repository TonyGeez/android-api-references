# FileServiceInfo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileServiceInfo

Kotlin| [Java](https://developer.android.com/reference/android/telephony/mbms/FileServiceInfo "View this page in Java") 
| --- | --- |

```
class FileServiceInfo : ServiceInfo, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.telephony.mbms.ServiceInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo) ||
| | ↳ | [android.telephony.mbms.FileServiceInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/FileServiceInfo#) |

Describes a file service available from the carrier from which files can be downloaded via cell-broadcast.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telephony/mbms/FileServiceInfo#describeContents())`()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [FileInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/FileInfo)!\>! | [getFiles](https://developer.android.com/reference/kotlin/android/telephony/mbms/FileServiceInfo#getFiles())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telephony/mbms/FileServiceInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [ServiceInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!>! | [getLocales](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#getLocales())`()` <br /> The languages available for this service content <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getNameForLocale](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#getNameForLocale(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)`)` <br /> Get the user-displayable name for this cell-broadcast service corresponding to the provided [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#). <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!> | [getNamedContentLocales](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#getNamedContentLocales())`()` <br /> Return an unmodifiable set of the current [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) s that have a user-displayable name associated with them. The user-displayable name associated with any [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) in this set can be retrieved with [getNameForLocale(java.util.Locale)](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#getNameForLocale(java.util.Locale)). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getServiceClassName](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#getServiceClassName())`()` <br /> The class name for this service - used to categorize and filter <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getServiceId](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#getServiceId())`()` <br /> The carrier's identifier for the service. <br /> | | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | [getSessionEndTime](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#getSessionEndTime())`()` <br /> The end time indicating when this session stops being available. <br /> | | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | [getSessionStartTime](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#getSessionStartTime())`()` <br /> The start time indicating when this service will be available. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#hashCode())`()` <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [FileServiceInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/FileServiceInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telephony/mbms/FileServiceInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getFiles

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFiles(): MutableList<FileInfo!>!
```

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [FileInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/FileInfo)!>! | A list of files available from this service. Note that this list may not be exhaustive -- the middleware may not have information on all files that are available. Consult the carrier for an authoritative and exhaustive list. |

### writeToParcel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<FileServiceInfo!>
```

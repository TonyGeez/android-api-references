# DataRemovalRequest

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataRemovalRequest

Kotlin| [Java](https://developer.android.com/reference/android/view/contentcapture/DataRemovalRequest "View this page in Java") 
| --- | --- |

```
class DataRemovalRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.contentcapture.DataRemovalRequest](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataRemovalRequest#) |

Class used by apps to request the content capture service to remove data associated with [LocusIds](https://developer.android.com/reference/kotlin/android/content/LocusId.html#).

An app which has tagged data with a LocusId can therefore delete them later. This is intended to let apps propagate deletions of user data into the operating system.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataRemovalRequest.Builder) Builder for [DataRemovalRequest](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataRemovalRequest#) objects. |
| | [LocusIdRequest](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataRemovalRequest.LocusIdRequest) Representation of a request to remove data associated with a [LocusId](https://developer.android.com/reference/kotlin/android/content/LocusId.html#). |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_IS_PREFIX](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataRemovalRequest#FLAG_IS_PREFIX:kotlin.Int) When set, service should use the [LocusId.getId()](https://developer.android.com/reference/kotlin/android/content/LocusId.html#getId())as prefix for the data to be removed. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataRemovalRequest#describeContents())`()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [DataRemovalRequest.LocusIdRequest](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataRemovalRequest.LocusIdRequest)!\> | [getLocusIdRequests](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataRemovalRequest#getLocusIdRequests())`()` Gets the list of`LousId`s the apps is requesting to remove. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getPackageName](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataRemovalRequest#getPackageName())`()` Gets the name of the app that's making the request. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isForEverything](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataRemovalRequest#isForEverything())`()` Checks if app is requesting to remove content capture data associated with its package. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataRemovalRequest#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [DataRemovalRequest](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataRemovalRequest#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataRemovalRequest#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### FLAG_IS_PREFIX

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_IS_PREFIX: Int
```

When set, service should use the [LocusId.getId()](https://developer.android.com/reference/kotlin/android/content/LocusId.html#getId())as prefix for the data to be removed. 

 Value: 1

## Public methods

### describeContents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getLocusIdRequests

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocusIdRequests(): MutableList<DataRemovalRequest.LocusIdRequest!>
```

Gets the list of`LousId`s the apps is requesting to remove.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [DataRemovalRequest.LocusIdRequest](https://developer.android.com/reference/kotlin/android/view/contentcapture/DataRemovalRequest.LocusIdRequest)!> | This value cannot be`null`. |

### getPackageName

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPackageName(): String
```

Gets the name of the app that's making the request.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### isForEverything

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isForEverything(): Boolean
```

Checks if app is requesting to remove content capture data associated with its package. 

### writeToParcel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<DataRemovalRequest!>
```

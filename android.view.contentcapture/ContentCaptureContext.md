# ContentCaptureContext

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentCaptureContext

Kotlin| [Java](https://developer.android.com/reference/android/view/contentcapture/ContentCaptureContext "View this page in Java") 
| --- | --- |

```
class ContentCaptureContext : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.contentcapture.ContentCaptureContext](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext#) |

Context associated with a [ContentCaptureSession](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession)- see [ContentCaptureManager](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureManager) for more info.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext.Builder) Builder for [ContentCaptureContext](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext#) objects. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext#describeContents())`()` <br /> |
| static [ContentCaptureContext](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext#) | [forLocusId](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext#forLocusId(kotlin.String))`(`id:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Helper that creates a [ContentCaptureContext](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext#) associated with the given`id`. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | [getExtras](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext#getExtras())`()` Gets the (optional) extras set by the app (through [Builder.setExtras(Bundle)](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext.Builder#setExtras(android.os.Bundle))). |
| --- | --- |
| [LocusId](https://developer.android.com/reference/kotlin/android/content/LocusId.html#)? | [getLocusId](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext#getLocusId())`()` Gets the context id. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ContentCaptureContext](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### forLocusId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun forLocusId(id: String): ContentCaptureContext
```

Helper that creates a [ContentCaptureContext](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext#) associated with the given`id`.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ContentCaptureContext](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext#) | This value cannot be`null`. |

### getExtras

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtras(): Bundle?
```

Gets the (optional) extras set by the app (through [Builder.setExtras(Bundle)](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext.Builder#setExtras(android.os.Bundle))).

It can be used to provide vendor-specific data that can be modified and examined.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | This value may be`null`. |

### getLocusId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocusId(): LocusId?
```

Gets the context id.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------|
| [LocusId](https://developer.android.com/reference/kotlin/android/content/LocusId.html#)? | This value may be`null`. |

### toString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

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
static val CREATOR: Parcelable.Creator<ContentCaptureContext!>
```

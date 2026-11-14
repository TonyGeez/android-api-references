# ContentCaptureContext

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentCaptureContext

Kotlin| [Java](ContentCaptureContext.md) 
| --- | --- |

```
class ContentCaptureContext : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.contentcapture.ContentCaptureContext](ContentCaptureContext.md) |

Context associated with a [ContentCaptureSession](ContentCaptureSession.md)- see [ContentCaptureManager](ContentCaptureManager.md) for more info.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/view/contentcapture/ContentCaptureContext.Builder.md) Builder for [ContentCaptureContext](ContentCaptureContext.md) objects. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](ContentCaptureContext.md))`()` <br /> |
| static [ContentCaptureContext](ContentCaptureContext.md) | [forLocusId](ContentCaptureContext.md))`(`id:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Helper that creates a [ContentCaptureContext](ContentCaptureContext.md) associated with the given`id`. |
| [Bundle](../android.os/Bundle.md)? | [getExtras](ContentCaptureContext.md))`()` Gets the (optional) extras set by the app (through [Builder.setExtras(Bundle)](../android/view/contentcapture/ContentCaptureContext.Builder.md))). |
| --- | --- |
| [LocusId](../android.content/LocusId.md)? | [getLocusId](ContentCaptureContext.md))`()` Gets the context id. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](ContentCaptureContext.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](ContentCaptureContext.md))`(`parcel:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ContentCaptureContext](ContentCaptureContext.md)!\> | [CREATOR](ContentCaptureContext.md) <br /> |

## Public methods

### describeContents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### forLocusId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun forLocusId(id: String): ContentCaptureContext
```

Helper that creates a [ContentCaptureContext](ContentCaptureContext.md) associated with the given`id`.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ContentCaptureContext](ContentCaptureContext.md) | This value cannot be`null`. |

### getExtras

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtras(): Bundle?
```

Gets the (optional) extras set by the app (through [Builder.setExtras(Bundle)](../android/view/contentcapture/ContentCaptureContext.Builder.md))).

It can be used to provide vendor-specific data that can be modified and examined.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [Bundle](../android.os/Bundle.md)? | This value may be`null`. |

### getLocusId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocusId(): LocusId?
```

Gets the context id.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------|
| [LocusId](../android.content/LocusId.md)? | This value may be`null`. |

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ContentCaptureContext!>
```

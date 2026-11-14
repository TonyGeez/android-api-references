Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClassifiableContent

```
class ClassifiableContent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.contentsafety.ClassifiableContent](ClassifiableContent.md) |

A class representing content to be classified.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/contentsafety/ClassifiableContent.Builder` Builder for `https://developer.android.com/reference/kotlin/android/app/contentsafety/ClassifiableContent#`. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/contentsafety/ClassifiableContent#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)? | `https://developer.android.com/reference/kotlin/android/app/contentsafety/ClassifiableContent#getData()()` Returns a `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` containing the raw data of this content. |
| [LocusId](../android.content/LocusId.md) | `https://developer.android.com/reference/kotlin/android/app/contentsafety/ClassifiableContent#getId()()` Returns the `https://developer.android.com/reference/kotlin/android/content/LocusId.html#` associated with this content. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/contentsafety/ClassifiableContent#getMimeType()()` Returns the MIME type of the content. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/app/contentsafety/ClassifiableContent#getOriginatingPackageName()()` Returns the package name of the app that requested the classification. |
| [Uri](../android.net/Uri.md)? | `https://developer.android.com/reference/kotlin/android/app/contentsafety/ClassifiableContent#getUri()()` Returns the `https://developer.android.com/reference/kotlin/android/net/Uri.html#` associated with this content. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/contentsafety/ClassifiableContent#writeToParcel(android.os.Parcel,%20kotlin.Int)(parcel: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ClassifiableContent](ClassifiableContent.md)!\> | `https://developer.android.com/reference/kotlin/android/app/contentsafety/ClassifiableContent#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### describeContents

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getData

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getData(): ParcelFileDescriptor?
```

Returns a `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` containing the raw data of this content.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#?` | the `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` containing the content data, or `null` if the raw content isn't provided |

### getId

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getId(): LocusId
```

Returns the `https://developer.android.com/reference/kotlin/android/content/LocusId.html#` associated with this content.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/LocusId.html#` | the `https://developer.android.com/reference/kotlin/android/content/LocusId.html#` of the content. This value cannot be `null`. |

### getMimeType

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMimeType(): String
```

Returns the MIME type of the content.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the MIME type. This value cannot be `null`. |

### getOriginatingPackageName

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOriginatingPackageName(): String?
```

Returns the package name of the app that requested the classification.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the originating package name, or `null` if the originating package is unknown or not provided |

### getUri

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUri(): Uri?
```

Returns the `https://developer.android.com/reference/kotlin/android/net/Uri.html#` associated with this content.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | the content `https://developer.android.com/reference/kotlin/android/net/Uri.html#`, or `null` if this content is not associated with a Uri |

### writeToParcel

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
| `parcel` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<ClassifiableContent!>
```

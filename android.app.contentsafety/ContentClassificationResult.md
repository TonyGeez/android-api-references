Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentClassificationResult

```
class ContentClassificationResult : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.contentsafety.ContentClassificationResult](ContentClassificationResult.md) |

A result reported by a Content Safety app in response to a content classification request.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentClassificationResult#TYPE_ALLOWED:kotlin.Int` Indicates that the content is allowed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentClassificationResult#TYPE_BLOCKED:kotlin.Int` Indicates that the content should be blocked. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentClassificationResult#TYPE_UNCLASSIFIED:kotlin.Int` Indicates that the content could not be classified. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentClassificationResult#TYPE_WARNING:kotlin.Int` Indicates that a warning should be issued for the content. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| ContentClassificationResult Creates a new content classification result. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [LocusId](../android.content/LocusId.md) | getLocusId Returns the `https://developer.android.com/reference/kotlin/android/content/LocusId.html#` of the content that was classified. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getType Returns the classification type of the content. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ContentClassificationResult](ContentClassificationResult.md)!\> | `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentClassificationResult#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### TYPE_ALLOWED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_ALLOWED: Int
```

Indicates that the content is allowed.

 Value: 1

### TYPE_BLOCKED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_BLOCKED: Int
```

Indicates that the content should be blocked.

 Value: 3

### TYPE_UNCLASSIFIED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_UNCLASSIFIED: Int
```

Indicates that the content could not be classified.

 Value: 0

### TYPE_WARNING

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_WARNING: Int
```

Indicates that a warning should be issued for the content.

 Value: 2

## Public constructors

### ContentClassificationResult

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ContentClassificationResult(
    locusId: LocusId, 
    type: Int)
```

Creates a new content classification result.

| Parameters ||
|---|---|
| `locusId` | [LocusId](../android.content/LocusId.md): the `https://developer.android.com/reference/kotlin/android/content/LocusId.html#` of the content that was classified. This value cannot be `null`. |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the classification type of the content. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentClassificationResult#TYPE_UNCLASSIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentClassificationResult#TYPE_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentClassificationResult#TYPE_WARNING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentClassificationResult#TYPE_BLOCKED:kotlin.Int` |

## Public methods

### describeContents

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getLocusId

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLocusId(): LocusId
```

Returns the `https://developer.android.com/reference/kotlin/android/content/LocusId.html#` of the content that was classified.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/LocusId.html#` | the `https://developer.android.com/reference/kotlin/android/content/LocusId.html#` This value cannot be `null`. |

### getType

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getType(): Int
```

Returns the classification type of the content.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the classification type. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentClassificationResult#TYPE_UNCLASSIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentClassificationResult#TYPE_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentClassificationResult#TYPE_WARNING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentClassificationResult#TYPE_BLOCKED:kotlin.Int` |

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
| `parcel` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<ContentClassificationResult!>
```

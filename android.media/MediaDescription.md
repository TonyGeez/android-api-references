Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaDescription

Kotlin | [Java](https://developer.android.com/reference/android/media/MediaDescription "View this page in Java")

```
open class MediaDescription : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.MediaDescription](https://developer.android.com/reference/kotlin/android/media/MediaDescription#) |

A simple set of metadata for a media item suitable for display. This can be created using the Builder or retrieved from existing metadata using `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#getDescription()`.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/media/MediaDescription.Builder` Builder for `https://developer.android.com/reference/kotlin/android/media/MediaDescription#` objects. |

| Constants ||
|---|---|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescription#BT_FOLDER_TYPE_ALBUMS:kotlin.Long` The type of folder that contains folders categorized by album as specified in the section 6. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescription#BT_FOLDER_TYPE_ARTISTS:kotlin.Long` The type of folder that contains folders categorized by artist as specified in the section 6. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescription#BT_FOLDER_TYPE_GENRES:kotlin.Long` The type of folder that contains folders categorized by genre as specified in the section 6. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescription#BT_FOLDER_TYPE_MIXED:kotlin.Long` The type of folder that is unknown or contains media elements of mixed types as specified in the section 6. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescription#BT_FOLDER_TYPE_PLAYLISTS:kotlin.Long` The type of folder that contains folders categorized by playlist as specified in the section 6. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescription#BT_FOLDER_TYPE_TITLES:kotlin.Long` The type of folder that contains media elements only as specified in the section 6. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescription#BT_FOLDER_TYPE_YEARS:kotlin.Long` The type of folder that contains folders categorized by year as specified in the section 6. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescription#EXTRA_BT_FOLDER_TYPE:kotlin.String` Used as a long extra field to indicate the bluetooth folder type of the media item as specified in the section 6. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescription#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescription#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/media/MediaDescription#getDescription()()` Returns a description suitable for display or null. |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | `https://developer.android.com/reference/kotlin/android/media/MediaDescription#getExtras()()` Returns any extras that were added to the description. |
| open [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | `https://developer.android.com/reference/kotlin/android/media/MediaDescription#getIconBitmap()()` Returns a bitmap icon suitable for display or null. |
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | `https://developer.android.com/reference/kotlin/android/media/MediaDescription#getIconUri()()` Returns a Uri for an icon suitable for display or null. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/media/MediaDescription#getMediaId()()` Returns the media id or null. |
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | `https://developer.android.com/reference/kotlin/android/media/MediaDescription#getMediaUri()()` Returns a Uri representing this content or null. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/media/MediaDescription#getSubtitle()()` Returns a subtitle suitable for display or null. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/media/MediaDescription#getTitle()()` Returns a title suitable for display or null. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescription#toString()()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescription#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [MediaDescription](https://developer.android.com/reference/kotlin/android/media/MediaDescription#)!\> | `https://developer.android.com/reference/kotlin/android/media/MediaDescription#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### BT_FOLDER_TYPE_ALBUMS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BT_FOLDER_TYPE_ALBUMS: Long
```

The type of folder that contains folders categorized by album as specified in the section 6.10.2.2 of the Bluetooth AVRCP 1.5.

 Value: 2L

### BT_FOLDER_TYPE_ARTISTS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BT_FOLDER_TYPE_ARTISTS: Long
```

The type of folder that contains folders categorized by artist as specified in the section 6.10.2.2 of the Bluetooth AVRCP 1.5.

 Value: 3L

### BT_FOLDER_TYPE_GENRES

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BT_FOLDER_TYPE_GENRES: Long
```

The type of folder that contains folders categorized by genre as specified in the section 6.10.2.2 of the Bluetooth AVRCP 1.5.

 Value: 4L

### BT_FOLDER_TYPE_MIXED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BT_FOLDER_TYPE_MIXED: Long
```

The type of folder that is unknown or contains media elements of mixed types as specified in the section 6.10.2.2 of the Bluetooth AVRCP 1.5.

 Value: 0L

### BT_FOLDER_TYPE_PLAYLISTS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BT_FOLDER_TYPE_PLAYLISTS: Long
```

The type of folder that contains folders categorized by playlist as specified in the section 6.10.2.2 of the Bluetooth AVRCP 1.5.

 Value: 5L

### BT_FOLDER_TYPE_TITLES

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BT_FOLDER_TYPE_TITLES: Long
```

The type of folder that contains media elements only as specified in the section 6.10.2.2 of the Bluetooth AVRCP 1.5.

 Value: 1L

### BT_FOLDER_TYPE_YEARS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BT_FOLDER_TYPE_YEARS: Long
```

The type of folder that contains folders categorized by year as specified in the section 6.10.2.2 of the Bluetooth AVRCP 1.5.

 Value: 6L

### EXTRA_BT_FOLDER_TYPE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_BT_FOLDER_TYPE: String
```

Used as a long extra field to indicate the bluetooth folder type of the media item as specified in the section 6.10.2.2 of the Bluetooth AVRCP 1.5. This is valid only for `https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser.MediaItem` with `https://developer.android.com/reference/kotlin/android/media/browse/MediaBrowser.MediaItem#FLAG_BROWSABLE:kotlin.Int`. The value should be one of the following:

- `https://developer.android.com/reference/kotlin/android/media/MediaDescription#BT_FOLDER_TYPE_MIXED:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/media/MediaDescription#BT_FOLDER_TYPE_TITLES:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/media/MediaDescription#BT_FOLDER_TYPE_ALBUMS:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/media/MediaDescription#BT_FOLDER_TYPE_ARTISTS:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/media/MediaDescription#BT_FOLDER_TYPE_GENRES:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/media/MediaDescription#BT_FOLDER_TYPE_PLAYLISTS:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/media/MediaDescription#BT_FOLDER_TYPE_YEARS:kotlin.Long`

<br />

 Value: "android.media.extra.BT_FOLDER_TYPE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaDescription#getExtras()`

## Public methods

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getDescription

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDescription(): CharSequence?
```

Returns a description suitable for display or null.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | A description or null. |

### getExtras

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getExtras(): Bundle?
```

Returns any extras that were added to the description.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#?` | A bundle of extras or null. |

### getIconBitmap

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIconBitmap(): Bitmap?
```

Returns a bitmap icon suitable for display or null.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#?` | An icon or null. |

### getIconUri

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIconUri(): Uri?
```

Returns a Uri for an icon suitable for display or null.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | An icon uri or null. |

### getMediaId

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMediaId(): String?
```

Returns the media id or null. See `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_MEDIA_ID:kotlin.String`.

### getMediaUri

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMediaUri(): Uri?
```

Returns a Uri representing this content or null.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | A media Uri or null. |

### getSubtitle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSubtitle(): CharSequence?
```

Returns a subtitle suitable for display or null.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | A subtitle or null. |

### getTitle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTitle(): CharSequence?
```

Returns a title suitable for display or null.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | A title or null. |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<MediaDescription!>
```

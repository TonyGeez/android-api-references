Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaMetadata

Kotlin | [Java](MediaMetadata.md)
| --- | --- |

```
class MediaMetadata : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaMetadata](MediaMetadata.md) |

Contains metadata about an item, such as the title, artist, etc.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata.Builder` Use to build MediaMetadata objects. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_ALBUM:kotlin.String` The album title for the media. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_ALBUM_ART:kotlin.String` The artwork for the album of the media's original source as a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_ALBUM_ARTIST:kotlin.String` The artist for the album of the media's original source. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_ALBUM_ART_URI:kotlin.String` The artwork for the album of the media's original source as a Uri formatted String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_ART:kotlin.String` The artwork for the media as a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_ARTIST:kotlin.String` The artist of the media. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_ART_URI:kotlin.String` The artwork for the media as a Uri formatted String. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_AUTHOR:kotlin.String` The author of the media. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_BT_FOLDER_TYPE:kotlin.String` The bluetooth folder type of the media specified in the section 6. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_COMPILATION:kotlin.String` The compilation status of the media. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_COMPOSER:kotlin.String` The composer of the media. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DATE:kotlin.String` The date the media was created or published. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DISC_NUMBER:kotlin.String` The disc number for the media's original source. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DISPLAY_DESCRIPTION:kotlin.String` A description that is suitable for display to the user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DISPLAY_ICON:kotlin.String` An icon or thumbnail that is suitable for display to the user. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DISPLAY_ICON_URI:kotlin.String` A Uri formatted String for an icon or thumbnail that is suitable for display to the user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DISPLAY_SUBTITLE:kotlin.String` A subtitle that is suitable for display to the user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DISPLAY_TITLE:kotlin.String` A title that is suitable for display to the user. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DURATION:kotlin.String` The duration of the media in ms. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_GENRE:kotlin.String` The genre of the media. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_MEDIA_ID:kotlin.String` A String key for identifying the content. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_MEDIA_URI:kotlin.String` A Uri formatted String representing the content. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_NUM_TRACKS:kotlin.String` The number of tracks in the media's original source. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_RATING:kotlin.String` The overall rating for the media. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_TITLE:kotlin.String` The title of the media. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_TRACK_NUMBER:kotlin.String` The track number for the media. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_USER_RATING:kotlin.String` The user's rating for the media. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_WRITER:kotlin.String` The writer of the media. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_YEAR:kotlin.String` The year the media was created or published as a long. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | containsKey Returns true if the given key is contained in the metadata |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Compares the contents of this object to another MediaMetadata object. |
| --- | --- |
| [Bitmap](../android.graphics/Bitmap.md)? | getBitmap Returns a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` for the given key or null if no bitmap exists for the given key. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getBitmapDimensionLimit Gets the width/height limit (in pixels) for the bitmaps when this metadata was created. |
| [MediaDescription](MediaDescription.md) | getDescription Returns a simple description of this metadata for display purposes. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getLong Returns the value associated with the given key, or 0L if no long exists for the given key. |
| [Rating](Rating.md)? | getRating Returns a Rating for the given key or null if no rating exists for the given key. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getString Returns the text value associated with the given key as a String, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | getText Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | keySet Returns a Set containing the Strings used as keys in this metadata. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | size Returns the number of fields in this metadata. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [MediaMetadata](MediaMetadata.md)!\> | `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### METADATA_KEY_ALBUM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_ALBUM: String
```

The album title for the media.

 Value: "android.media.metadata.ALBUM"

### METADATA_KEY_ALBUM_ART

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_ALBUM_ART: String
```

The artwork for the album of the media's original source as a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#`.

The artwork should be relatively small and may be scaled down by the system if it is too large. For higher resolution artwork `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_ALBUM_ART_URI:kotlin.String` should be used instead.

 Value: "android.media.metadata.ALBUM_ART"

### METADATA_KEY_ALBUM_ARTIST

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_ALBUM_ARTIST: String
```

The artist for the album of the media's original source.

 Value: "android.media.metadata.ALBUM_ARTIST"

### METADATA_KEY_ALBUM_ART_URI

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_ALBUM_ART_URI: String
```

The artwork for the album of the media's original source as a Uri formatted String. The artwork can be loaded using a combination of openInputStream and android.graphics.BitmapFactory#decodeStream.

For the best results, Uris should use the content:// style and support `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_SIZE:kotlin.String` for retrieving scaled artwork through openTypedAssetFileDescriptor.

 Value: "android.media.metadata.ALBUM_ART_URI"

### METADATA_KEY_ART

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_ART: String
```

The artwork for the media as a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#`.

The artwork should be relatively small and may be scaled down by the system if it is too large. For higher resolution artwork `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_ART_URI:kotlin.String` should be used instead.

 Value: "android.media.metadata.ART"

### METADATA_KEY_ARTIST

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_ARTIST: String
```

The artist of the media.

 Value: "android.media.metadata.ARTIST"

### METADATA_KEY_ART_URI

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_ART_URI: String
```

The artwork for the media as a Uri formatted String. The artwork can be loaded using a combination of openInputStream and android.graphics.BitmapFactory#decodeStream.

For the best results, Uris should use the content:// style and support `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_SIZE:kotlin.String` for retrieving scaled artwork through openTypedAssetFileDescriptor.

 Value: "android.media.metadata.ART_URI"

### METADATA_KEY_AUTHOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_AUTHOR: String
```

The author of the media.

 Value: "android.media.metadata.AUTHOR"

### METADATA_KEY_BT_FOLDER_TYPE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_BT_FOLDER_TYPE: String
```

The bluetooth folder type of the media specified in the section 6.10.2.2 of the Bluetooth AVRCP 1.5. It should be one of the following:

- `https://developer.android.com/reference/kotlin/android/media/MediaDescription#BT_FOLDER_TYPE_MIXED:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/media/MediaDescription#BT_FOLDER_TYPE_TITLES:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/media/MediaDescription#BT_FOLDER_TYPE_ALBUMS:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/media/MediaDescription#BT_FOLDER_TYPE_ARTISTS:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/media/MediaDescription#BT_FOLDER_TYPE_GENRES:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/media/MediaDescription#BT_FOLDER_TYPE_PLAYLISTS:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/media/MediaDescription#BT_FOLDER_TYPE_YEARS:kotlin.Long`

<br />

 Value: "android.media.metadata.BT_FOLDER_TYPE"

### METADATA_KEY_COMPILATION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_COMPILATION: String
```

The compilation status of the media.

 Value: "android.media.metadata.COMPILATION"

### METADATA_KEY_COMPOSER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_COMPOSER: String
```

The composer of the media.

 Value: "android.media.metadata.COMPOSER"

### METADATA_KEY_DATE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_DATE: String
```

The date the media was created or published. The format is unspecified but RFC 3339 is recommended.

 Value: "android.media.metadata.DATE"

### METADATA_KEY_DISC_NUMBER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_DISC_NUMBER: String
```

The disc number for the media's original source.

 Value: "android.media.metadata.DISC_NUMBER"

### METADATA_KEY_DISPLAY_DESCRIPTION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_DISPLAY_DESCRIPTION: String
```

A description that is suitable for display to the user. When displaying more information for media described by this metadata this should be preferred to other fields if present.

 Value: "android.media.metadata.DISPLAY_DESCRIPTION"

### METADATA_KEY_DISPLAY_ICON

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_DISPLAY_ICON: String
```

An icon or thumbnail that is suitable for display to the user. When displaying an icon for media described by this metadata this should be preferred to other fields if present. This must be a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#`.

The icon should be relatively small and may be scaled down by the system if it is too large. For higher resolution artwork `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DISPLAY_ICON_URI:kotlin.String` should be used instead.

 Value: "android.media.metadata.DISPLAY_ICON"

### METADATA_KEY_DISPLAY_ICON_URI

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_DISPLAY_ICON_URI: String
```

A Uri formatted String for an icon or thumbnail that is suitable for display to the user. When displaying more information for media described by this metadata the display description should be preferred to other fields when present. The icon can be loaded using a combination of openInputStream and android.graphics.BitmapFactory#decodeStream.

For the best results, Uris should use the content:// style and support `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_SIZE:kotlin.String` for retrieving scaled artwork through openTypedAssetFileDescriptor.

 Value: "android.media.metadata.DISPLAY_ICON_URI"

### METADATA_KEY_DISPLAY_SUBTITLE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_DISPLAY_SUBTITLE: String
```

A subtitle that is suitable for display to the user. When displaying a second line for media described by this metadata this should be preferred to other fields if present.

 Value: "android.media.metadata.DISPLAY_SUBTITLE"

### METADATA_KEY_DISPLAY_TITLE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_DISPLAY_TITLE: String
```

A title that is suitable for display to the user. This will generally be the same as `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_TITLE:kotlin.String` but may differ for some formats. When displaying media described by this metadata this should be preferred if present.

 Value: "android.media.metadata.DISPLAY_TITLE"

### METADATA_KEY_DURATION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_DURATION: String
```

The duration of the media in ms. A negative duration indicates that the duration is unknown (or infinite).

 Value: "android.media.metadata.DURATION"

### METADATA_KEY_GENRE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_GENRE: String
```

The genre of the media.

 Value: "android.media.metadata.GENRE"

### METADATA_KEY_MEDIA_ID

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_MEDIA_ID: String
```

A String key for identifying the content. This value is specific to the service providing the content. If used, this should be a persistent unique key for the underlying content. It may be used with playFromMediaId to initiate playback when provided by a MediaBrowser connected to the same app.

 Value: "android.media.metadata.MEDIA_ID"

### METADATA_KEY_MEDIA_URI

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_MEDIA_URI: String
```

A Uri formatted String representing the content. This value is specific to the service providing the content. It may be used with playFromUri to initiate playback when provided by a MediaBrowser connected to the same app.

 Value: "android.media.metadata.MEDIA_URI"

### METADATA_KEY_NUM_TRACKS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_NUM_TRACKS: String
```

The number of tracks in the media's original source.

 Value: "android.media.metadata.NUM_TRACKS"

### METADATA_KEY_RATING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_RATING: String
```

The overall rating for the media.

 Value: "android.media.metadata.RATING"

**See Also**

- Rating

### METADATA_KEY_TITLE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_TITLE: String
```

The title of the media.

 Value: "android.media.metadata.TITLE"

### METADATA_KEY_TRACK_NUMBER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_TRACK_NUMBER: String
```

The track number for the media.

 Value: "android.media.metadata.TRACK_NUMBER"

### METADATA_KEY_USER_RATING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_USER_RATING: String
```

The user's rating for the media.

 Value: "android.media.metadata.USER_RATING"

**See Also**

- Rating

### METADATA_KEY_WRITER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_WRITER: String
```

The writer of the media.

 Value: "android.media.metadata.WRITER"

### METADATA_KEY_YEAR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val METADATA_KEY_YEAR: String
```

The year the media was created or published as a long.

 Value: "android.media.metadata.YEAR"

## Public methods

### containsKey

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun containsKey(key: String!): Boolean
```

Returns true if the given key is contained in the metadata

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a String key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the key exists in this metadata, false otherwise |

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Compares the contents of this object to another MediaMetadata object. It does not compare Bitmaps and Ratings as the media player can choose to forgo these fields depending on how you retrieve the MediaMetadata.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `o` | The Metadata object to compare this object against |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether or not the two objects have matching fields (excluding Bitmaps and Ratings) |

### getBitmap

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBitmap(key: String!): Bitmap?
```

Returns a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` for the given key or null if no bitmap exists for the given key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The key the value is stored under. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_ART:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_ALBUM_ART:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DISPLAY_ICON:kotlin.String` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#?` | A `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` or null |

### getBitmapDimensionLimit

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBitmapDimensionLimit(): Int
```

Gets the width/height limit (in pixels) for the bitmaps when this metadata was created. This method always returns a positive value.

If it returns `https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int`, then no scaling down was applied to the bitmaps when this metadata was created.

If it returns another positive value, then all the bitmaps in this metadata has width/height not greater than this limit. Bitmaps may have been scaled down according to the limit.

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is 1 or greater |

**See Also**

- setBitmapDimensionLimit

### getDescription

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDescription(): MediaDescription
```

Returns a simple description of this metadata for display purposes.

| Return ||
|---|---|
| MediaDescription | A simple description of this metadata. This value cannot be `null`. |

### getLong

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLong(key: String!): Long
```

Returns the value associated with the given key, or 0L if no long exists for the given key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The key the value is stored under. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DURATION:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_YEAR:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_TRACK_NUMBER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_NUM_TRACKS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DISC_NUMBER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_BT_FOLDER_TYPE:kotlin.String` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | a long value |

### getRating

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRating(key: String!): Rating?
```

Returns a Rating for the given key or null if no rating exists for the given key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The key the value is stored under. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_USER_RATING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_RATING:kotlin.String` |

| Return ||
|---|---|
| Rating | A Rating or null |

### getString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getString(key: String!): String?
```

Returns the text value associated with the given key as a String, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. This is equivalent to calling getText if the value is not null.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The key the value is stored under. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_TITLE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_ARTIST:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_ALBUM:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_AUTHOR:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_WRITER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_COMPOSER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_COMPILATION:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DATE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_GENRE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_ALBUM_ARTIST:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_ART_URI:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_ALBUM_ART_URI:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DISPLAY_TITLE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DISPLAY_SUBTITLE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DISPLAY_DESCRIPTION:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DISPLAY_ICON_URI:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_MEDIA_ID:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_MEDIA_URI:kotlin.String` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | a String value, or null |

### getText

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getText(key: String!): CharSequence?
```

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The key the value is stored under. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_TITLE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_ARTIST:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_ALBUM:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_AUTHOR:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_WRITER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_COMPOSER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_COMPILATION:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DATE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_GENRE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_ALBUM_ARTIST:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_ART_URI:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_ALBUM_ART_URI:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DISPLAY_TITLE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DISPLAY_SUBTITLE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DISPLAY_DESCRIPTION:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_DISPLAY_ICON_URI:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_MEDIA_ID:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaMetadata#METADATA_KEY_MEDIA_URI:kotlin.String` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | a CharSequence value, or null |

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the equals method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the equals method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### keySet

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun keySet(): MutableSet<String!>!
```

Returns a Set containing the Strings used as keys in this metadata.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | a Set of String keys |

### size

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun size(): Int
```

Returns the number of fields in this metadata.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of fields in the metadata. |

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<MediaMetadata!>
```

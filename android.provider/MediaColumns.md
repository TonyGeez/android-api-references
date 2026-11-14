Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaColumns

```
interface MediaColumns : BaseColumns
```

| [android.provider.MediaStore.MediaColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#) |

| Known Direct Subclasses [MediaStore.Audio.AudioColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Audio.AudioColumns), [MediaStore.Audio.PlaylistsColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Audio.PlaylistsColumns), [MediaStore.DownloadColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.DownloadColumns), [MediaStore.Files.FileColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Files.FileColumns), [MediaStore.Images.ImageColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Images.ImageColumns), [MediaStore.Video.VideoColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Video.VideoColumns) |---|---| | [MediaStore.Audio.AudioColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Audio.AudioColumns) | Audio metadata columns. | | [MediaStore.Audio.PlaylistsColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Audio.PlaylistsColumns) | Audio playlist metadata columns. | | [MediaStore.DownloadColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.DownloadColumns) | Download metadata columns. | | [MediaStore.Files.FileColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Files.FileColumns) | File metadata columns. | | [MediaStore.Images.ImageColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Images.ImageColumns) | Image metadata columns. | | [MediaStore.Video.VideoColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Video.VideoColumns) | Video metadata columns. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [MediaStore.Audio.Genres.Members](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Audio.Genres.Members), [MediaStore.Audio.Media](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Audio.Media), [MediaStore.Audio.Playlists](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Audio.Playlists), [MediaStore.Audio.Playlists.Members](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Audio.Playlists.Members), [MediaStore.Downloads](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Downloads), [MediaStore.Images.Media](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Images.Media), [MediaStore.Video.Media](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Video.Media) |---|---| | [MediaStore.Audio.Genres.Members](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Audio.Genres.Members) | Sub-directory of each genre containing all members. | | [MediaStore.Audio.Media](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Audio.Media) | <br /> | | [MediaStore.Audio.Playlists](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Audio.Playlists) | Contains playlists for audio files | | [MediaStore.Audio.Playlists.Members](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Audio.Playlists.Members) | Sub-directory of each playlist containing all members. | | [MediaStore.Downloads](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Downloads) | Collection of downloaded items. | | [MediaStore.Images.Media](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Images.Media) | <br /> | | [MediaStore.Video.Media](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Video.Media) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Common media metadata columns.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#ALBUM:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_ALBUM:kotlin.Int` extracted from this media item. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#ALBUM_ARTIST:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_ALBUMARTIST:kotlin.Int` extracted from this media item. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#ARTIST:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_ARTIST:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/ExifInterface.html#TAG_ARTIST:kotlin.String` extracted from this media item. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#AUTHOR:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_AUTHOR:kotlin.Int` extracted from this media item. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#BITRATE:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_BITRATE:kotlin.Int` extracted from this media item. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#BUCKET_DISPLAY_NAME:kotlin.String` The primary bucket display name of this media item. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#BUCKET_ID:kotlin.String` The primary bucket ID of this media item. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#CAPTURE_FRAMERATE:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_CAPTURE_FRAMERATE:kotlin.Int` extracted from this media item. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#CD_TRACK_NUMBER:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_CD_TRACK_NUMBER:kotlin.Int` extracted from this media item. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#COMPILATION:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_COMPILATION:kotlin.Int` extracted from this media item. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#COMPOSER:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_COMPOSER:kotlin.Int` extracted from this media item. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#DATA:kotlin.String` Absolute filesystem path to the media item on disk. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#DATE_ADDED:kotlin.String` The time the media item was first added. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#DATE_EXPIRES:kotlin.String` The time the media item should be considered expired. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#DATE_MODIFIED:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/java/io/File.html#lastModified()` extracted from this media item. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#DATE_TAKEN:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_DATE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/ExifInterface.html#TAG_DATETIME_ORIGINAL:kotlin.String` extracted from this media item. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#DISC_NUMBER:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_DISC_NUMBER:kotlin.Int` extracted from this media item. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#DISPLAY_NAME:kotlin.String` The display name of the media item. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#DOCUMENT_ID:kotlin.String` The "document ID" GUID as defined by the *XMP Media Management* standard, extracted from any XMP metadata contained within this media item. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#DURATION:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_DURATION:kotlin.Int` extracted from this media item. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#GENERATION_ADDED:kotlin.String` Generation number at which metadata for this media item was first inserted. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#GENERATION_MODIFIED:kotlin.String` Generation number at which metadata for this media item was last changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#GENRE:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_GENRE:kotlin.Int` extracted from this media item. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#HEIGHT:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_VIDEO_HEIGHT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_IMAGE_HEIGHT:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/ExifInterface.html#TAG_IMAGE_LENGTH:kotlin.String` extracted from this media item. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#INFERRED_DATE:kotlin.String` File's approximate creation date. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#INSTANCE_ID:kotlin.String` The "instance ID" GUID as defined by the *XMP Media Management* standard, extracted from any XMP metadata contained within this media item. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_DOWNLOAD:kotlin.String` Flag indicating if the media item has been marked as being part of the `https://developer.android.com/reference/kotlin/android/provider/MediaStore.Downloads` collection. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_DRM:kotlin.String` Flag indicating if a media item is DRM protected. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_FAVORITE:kotlin.String` Flag indicating if the media item has been marked as being a "favorite" by the user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_PENDING:kotlin.String` Flag indicating if a media item is pending, and still being inserted by its owner. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_TRASHED:kotlin.String` Flag indicating if a media item is trashed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#MIME_TYPE:kotlin.String` The MIME type of the media item. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#NUM_TRACKS:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_NUM_TRACKS:kotlin.Int` extracted from this media item. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#OEM_METADATA:kotlin.String` Column which allows OEMs to store custom metadata for a media file. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#ORIENTATION:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_VIDEO_ROTATION:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_IMAGE_ROTATION:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/media/ExifInterface.html#TAG_ORIENTATION:kotlin.String` extracted from this media item. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#ORIGINAL_DOCUMENT_ID:kotlin.String` The "original document ID" GUID as defined by the *XMP Media Management* standard, extracted from any XMP metadata contained within this media item. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#OWNER_PACKAGE_NAME:kotlin.String` Package name that contributed this media. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#RELATIVE_PATH:kotlin.String` Relative path of this media item within the storage device where it is persisted. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#RESOLUTION:kotlin.String` Calculated value that combines `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#WIDTH:kotlin.String` and `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#HEIGHT:kotlin.String` into a user-presentable string. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#SIZE:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/java/io/File.html#length()` extracted from this media item. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#TITLE:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_TITLE:kotlin.Int` extracted from this media item. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#VOLUME_NAME:kotlin.String` Volume name of the specific storage device where this media item is persisted. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#WIDTH:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_VIDEO_WIDTH:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_IMAGE_WIDTH:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/ExifInterface.html#TAG_IMAGE_WIDTH:kotlin.String` extracted from this media item. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#WRITER:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_WRITER:kotlin.Int` extracted from this media item. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#XMP:kotlin.String` Indexed XMP metadata extracted from this media item. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#YEAR:kotlin.String` Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_YEAR:kotlin.Int` extracted from this media item. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/provider/BaseColumns` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_COUNT:kotlin.String` The count of rows in a directory. Type: INTEGER <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String` The unique ID for a row. Type: INTEGER (long) <br /> | ||

## Constants

### ALBUM

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALBUM: String
```

Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_ALBUM:kotlin.Int` extracted from this media item. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "album"

### ALBUM_ARTIST

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALBUM_ARTIST: String
```

Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_ALBUMARTIST:kotlin.Int` extracted from this media item. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "album_artist"

### ARTIST

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARTIST: String
```

Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_ARTIST:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/ExifInterface.html#TAG_ARTIST:kotlin.String` extracted from this media item. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "artist"

### AUTHOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTHOR: String
```

Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_AUTHOR:kotlin.Int` extracted from this media item. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "author"

### BITRATE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BITRATE: String
```

Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_BITRATE:kotlin.Int` extracted from this media item. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_INTEGER:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "bitrate"

### BUCKET_DISPLAY_NAME

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BUCKET_DISPLAY_NAME: String
```

The primary bucket display name of this media item. This can be useful to present the user a first-level clustering of related media items. This is a read-only column that is automatically computed. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "bucket_display_name"

### BUCKET_ID

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BUCKET_ID: String
```

The primary bucket ID of this media item. This can be useful to present the user a first-level clustering of related media items. This is a read-only column that is automatically computed. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_INTEGER:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "bucket_id"

### CAPTURE_FRAMERATE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPTURE_FRAMERATE: String
```

Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_CAPTURE_FRAMERATE:kotlin.Int` extracted from this media item. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_FLOAT:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "capture_framerate"

### CD_TRACK_NUMBER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CD_TRACK_NUMBER: String
```

Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_CD_TRACK_NUMBER:kotlin.Int` extracted from this media item. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "cd_track_number"

### COMPILATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COMPILATION: String
```

Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_COMPILATION:kotlin.Int` extracted from this media item. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "compilation"

### COMPOSER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COMPOSER: String
```

Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_COMPOSER:kotlin.Int` extracted from this media item. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "composer"

### DATA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA: String
```

Absolute filesystem path to the media item on disk.

Apps may use this path to do file operations. However, they should not assume that the file is always available. Apps must be prepared to handle any file-based I/O errors that could occur.

From Android 11 onwards, this column is read-only for apps that target `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` and higher. On those devices, when creating or updating a uri, this column's value is not accepted. Instead, to update the filesystem location of a file, use the values of the `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#DISPLAY_NAME:kotlin.String` and `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#RELATIVE_PATH:kotlin.String` columns.

Though direct file operations are supported, `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openFileDescriptor(android.net.Uri,%20kotlin.String)` API is recommended for better performance. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` .

 Value: "_data"

### DATE_ADDED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATE_ADDED: String
```

The time the media item was first added. 
Value is a non-negative timestamp measured as the number of seconds since 1970-01-01T00:00:00Z. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_INTEGER:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "date_added"

### DATE_EXPIRES

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATE_EXPIRES: String
```

The time the media item should be considered expired. Typically only meaningful in the context of `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_PENDING:kotlin.String` or `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_TRASHED:kotlin.String`.

The value stored in this column is automatically calculated when `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_PENDING:kotlin.String` or `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_TRASHED:kotlin.String` is changed. The default pending expiration is typically 7 days, and the default trashed expiration is typically 30 days.

Expired media items are automatically deleted once their expiration time has passed, typically during the next device idle period. 
Value is a non-negative timestamp measured as the number of seconds since 1970-01-01T00:00:00Z. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_INTEGER:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "date_expires"

### DATE_MODIFIED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATE_MODIFIED: String
```

Indexed value of `https://developer.android.com/reference/kotlin/java/io/File.html#lastModified()` extracted from this media item. 
Value is a non-negative timestamp measured as the number of seconds since 1970-01-01T00:00:00Z. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_INTEGER:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "date_modified"

### DATE_TAKEN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATE_TAKEN: String
```

Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_DATE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/ExifInterface.html#TAG_DATETIME_ORIGINAL:kotlin.String` extracted from this media item.

Note that images must define both `https://developer.android.com/reference/kotlin/android/media/ExifInterface.html#TAG_DATETIME_ORIGINAL:kotlin.String` and `ExifInterface#TAG_OFFSET_TIME_ORIGINAL` to reliably determine this value in relation to the epoch. 
Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_INTEGER:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "datetaken"

### DISC_NUMBER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISC_NUMBER: String
```

Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_DISC_NUMBER:kotlin.Int` extracted from this media item. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "disc_number"

### DISPLAY_NAME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISPLAY_NAME: String
```

The display name of the media item.

For example, an item stored at `/storage/0000-0000/DCIM/Vacation/IMG1024.JPG` would have a display name of `IMG1024.JPG`. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` .

 Value: "_display_name"

### DOCUMENT_ID

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DOCUMENT_ID: String
```

The "document ID" GUID as defined by the *XMP Media Management* standard, extracted from any XMP metadata contained within this media item. The value is `null` when no metadata was found.

Each "document ID" is created once for each new resource. Different renditions of that resource are expected to have different IDs. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "document_id"

### DURATION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DURATION: String
```

Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_DURATION:kotlin.Int` extracted from this media item. 
Value is a non-negative duration in milliseconds. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_INTEGER:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "duration"

### GENERATION_ADDED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GENERATION_ADDED: String
```

Generation number at which metadata for this media item was first inserted. This is useful for apps that are attempting to quickly identify exactly which media items have been added since a previous point in time. Generation numbers are monotonically increasing over time, and can be safely arithmetically compared.

Detecting media additions using generation numbers is more robust than using `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#DATE_ADDED:kotlin.String`, since those values may change in unexpected ways when apps use `https://developer.android.com/reference/kotlin/java/io/File.html#setLastModified(kotlin.Long)` or when the system clock is set incorrectly.

Note that before comparing these detailed generation values, you should first confirm that the overall version hasn't changed by checking `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getVersion(android.content.Context,%20kotlin.String)`, since that indicates when a more radical change has occurred. If the overall version changes, you should assume that generation numbers have been reset and perform a full synchronization pass. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_INTEGER:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "generation_added"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getGeneration(android.content.Context,%20kotlin.String)`

### GENERATION_MODIFIED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GENERATION_MODIFIED: String
```

Generation number at which metadata for this media item was last changed. This is useful for apps that are attempting to quickly identify exactly which media items have changed since a previous point in time. Generation numbers are monotonically increasing over time, and can be safely arithmetically compared.

Detecting media changes using generation numbers is more robust than using `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#DATE_MODIFIED:kotlin.String`, since those values may change in unexpected ways when apps use `https://developer.android.com/reference/kotlin/java/io/File.html#setLastModified(kotlin.Long)` or when the system clock is set incorrectly.

Note that before comparing these detailed generation values, you should first confirm that the overall version hasn't changed by checking `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getVersion(android.content.Context,%20kotlin.String)`, since that indicates when a more radical change has occurred. If the overall version changes, you should assume that generation numbers have been reset and perform a full synchronization pass. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_INTEGER:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "generation_modified"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getGeneration(android.content.Context,%20kotlin.String)`

### GENRE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GENRE: String
```

Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_GENRE:kotlin.Int` extracted from this media item. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "genre"

### HEIGHT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HEIGHT: String
```

Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_VIDEO_HEIGHT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_IMAGE_HEIGHT:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/ExifInterface.html#TAG_IMAGE_LENGTH:kotlin.String` extracted from this media item.

Type: INTEGER. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_INTEGER:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "height"

### INFERRED_DATE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 15](https://developer.android.com/sdkExtensions)

```
static val INFERRED_DATE: String
```

File's approximate creation date.

Following is the derivation logic: 1. If `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#DATE_TAKEN:kotlin.String` is present, use it. 2. If `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#DATE_TAKEN:kotlin.String` is absent, use `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#DATE_MODIFIED:kotlin.String`. Note: When `https://developer.android.com/reference/kotlin/android/provider/MediaStore#QUERY_ARG_MEDIA_STANDARD_SORT_ORDER:kotlin.String` query argument is used, the sorting is based on this column in descending order. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_INTEGER:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "inferred_date"

### INSTANCE_ID

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INSTANCE_ID: String
```

The "instance ID" GUID as defined by the *XMP Media Management* standard, extracted from any XMP metadata contained within this media item. The value is `null` when no metadata was found.

This "instance ID" changes with each save operation of a specific "document ID". 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "instance_id"

### IS_DOWNLOAD

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IS_DOWNLOAD: String
```

Flag indicating if the media item has been marked as being part of the `https://developer.android.com/reference/kotlin/android/provider/MediaStore.Downloads` collection. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_INTEGER:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "is_download"

### IS_DRM

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IS_DRM: String
```

Flag indicating if a media item is DRM protected. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_INTEGER:kotlin.Int` .

 Value: "is_drm"

### IS_FAVORITE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IS_FAVORITE: String
```

Flag indicating if the media item has been marked as being a "favorite" by the user. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_INTEGER:kotlin.Int` .

 Value: "is_favorite"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_FAVORITE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#QUERY_ARG_MATCH_FAVORITE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#createFavoriteRequest(android.content.ContentResolver,%20kotlin.collections.MutableCollection,%20kotlin.Boolean)`

### IS_PENDING

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IS_PENDING: String
```

Flag indicating if a media item is pending, and still being inserted by its owner. While this flag is set, only the owner of the item can open the underlying file; requests from other apps will be rejected.

Pending items are retained either until they are published by setting the field to `0`, or until they expire as defined by `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#DATE_EXPIRES:kotlin.String`. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_INTEGER:kotlin.Int` .

 Value: "is_pending"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#QUERY_ARG_MATCH_PENDING:kotlin.String`

### IS_TRASHED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IS_TRASHED: String
```

Flag indicating if a media item is trashed.

Trashed items are retained until they expire as defined by `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#DATE_EXPIRES:kotlin.String`. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_INTEGER:kotlin.Int` .

 Value: "is_trashed"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_TRASHED:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#QUERY_ARG_MATCH_TRASHED:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#createTrashRequest(android.content.ContentResolver,%20kotlin.collections.MutableCollection,%20kotlin.Boolean)`

### MIME_TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIME_TYPE: String
```

The MIME type of the media item.

This is typically defined based on the file extension of the media item. However, it may be the value of the `format` attribute defined by the *Dublin Core Media Initiative* standard, extracted from any XMP metadata contained within this media item.

Note: the `format` attribute may be ignored if the top-level MIME type disagrees with the file extension. For example, it's reasonable for an `image/jpeg` file to declare a `format` of `image/vnd.google.panorama360+jpg`, but declaring a `format` of `audio/ogg` would be ignored.

This is a read-only column that is automatically computed. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` .

 Value: "mime_type"

### NUM_TRACKS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NUM_TRACKS: String
```

Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_NUM_TRACKS:kotlin.Int` extracted from this media item. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_INTEGER:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "num_tracks"

### OEM_METADATA

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 15](https://developer.android.com/sdkExtensions)

```
static val OEM_METADATA: String
```

Column which allows OEMs to store custom metadata for a media file. It is expected to contain a JSON string. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_BLOB:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "oem_metadata"

### ORIENTATION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ORIENTATION: String
```

Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_VIDEO_ROTATION:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_IMAGE_ROTATION:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/media/ExifInterface.html#TAG_ORIENTATION:kotlin.String` extracted from this media item.

For consistency the indexed value is expressed in degrees, such as 0, 90, 180, or 270.

Type: INTEGER. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_INTEGER:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "orientation"

### ORIGINAL_DOCUMENT_ID

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ORIGINAL_DOCUMENT_ID: String
```

The "original document ID" GUID as defined by the *XMP Media Management* standard, extracted from any XMP metadata contained within this media item.

This "original document ID" links a resource to its original source. For example, when you save a PSD document as a JPEG, then convert the JPEG to GIF format, the "original document ID" of both the JPEG and GIF files is the "document ID" of the original PSD file. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "original_document_id"

### OWNER_PACKAGE_NAME

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OWNER_PACKAGE_NAME: String
```

Package name that contributed this media. The value may be `NULL` if ownership cannot be reliably determined.

From Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` onwards, visibility and query of this field will depend on [package visibility](https://developer.android.com/reference/kotlin/training/basics/intents/package-visibility). For android.content.ContentResolver#query operation, result set will be restricted to visible packages only. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "owner_package_name"

### RELATIVE_PATH

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RELATIVE_PATH: String
```

Relative path of this media item within the storage device where it is persisted. For example, an item stored at `/storage/0000-0000/DCIM/Vacation/IMG1024.JPG` would have a path of `DCIM/Vacation/`.

This value should only be used for organizational purposes, and you should not attempt to construct or access a raw filesystem path using this value. If you need to open a media item, use an API like `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openFileDescriptor(android.net.Uri,%20kotlin.String)`.

When this value is set to `NULL` during an android.content.ContentResolver#insert operation, the newly created item will be placed in a relevant default location based on the type of media being inserted. For example, a `image/jpeg` item will be placed under `https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_PICTURES:kotlin.String`.

You can modify this column during an android.content.ContentResolver#update call, which will move the underlying file on disk.

In both cases above, content must be placed under a top-level directory that is relevant to the media type. For example, attempting to place a `audio/mpeg` file under `https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_PICTURES:kotlin.String` will be rejected. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` .

 Value: "relative_path"

### RESOLUTION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESOLUTION: String
```

Calculated value that combines `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#WIDTH:kotlin.String` and `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#HEIGHT:kotlin.String` into a user-presentable string. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "resolution"

### SIZE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIZE: String
```

Indexed value of `https://developer.android.com/reference/kotlin/java/io/File.html#length()` extracted from this media item. 
Value is a non-negative number of bytes. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_INTEGER:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "_size"

### TITLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TITLE: String
```

Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_TITLE:kotlin.Int` extracted from this media item. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "title"

### VOLUME_NAME

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VOLUME_NAME: String
```

Volume name of the specific storage device where this media item is persisted. The value is typically one of the volume names returned from `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getExternalVolumeNames(android.content.Context)`.

This is a read-only column that is automatically computed. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "volume_name"

### WIDTH

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIDTH: String
```

Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_VIDEO_WIDTH:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_IMAGE_WIDTH:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/ExifInterface.html#TAG_IMAGE_WIDTH:kotlin.String` extracted from this media item.

Type: INTEGER. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_INTEGER:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "width"

### WRITER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WRITER: String
```

Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_WRITER:kotlin.Int` extracted from this media item. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_STRING:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "writer"

### XMP

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val XMP: String
```

Indexed XMP metadata extracted from this media item.

The structure of this metadata is defined by the [*XMP Media Management* standard](https://en.wikipedia.org/wiki/Extensible_Metadata_Platform), published as ISO 16684-1:2012.

This metadata is typically extracted from a `https://developer.android.com/reference/kotlin/android/media/ExifInterface.html#TAG_XMP:kotlin.String` contained inside an image file or from a `XMP_` box contained inside an ISO/IEC base media file format (MPEG-4 Part 12).

Note that any location details are redacted from this metadata for privacy reasons. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_BLOB:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "xmp"

### YEAR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR: String
```

Indexed value of `https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.html#METADATA_KEY_YEAR:kotlin.Int` extracted from this media item. 
This constant represents a column name that can be used with a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` through a `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` or `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` object. The values stored in this column are `https://developer.android.com/reference/kotlin/android/database/Cursor.html#FIELD_TYPE_INTEGER:kotlin.Int` , and are read-only and cannot be mutated.

 Value: "year"

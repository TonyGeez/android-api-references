# MediaMetadataEditor

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaMetadataEditor

Kotlin | [Java](https://developer.android.com/reference/android/media/MediaMetadataEditor "View this page in Java") 

```
abstract class MediaMetadataEditor
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.MediaMetadataEditor](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#) |

| Known Direct Subclasses [RemoteControlClient.MetadataEditor](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.MetadataEditor), [RemoteController.MetadataEditor](https://developer.android.com/reference/kotlin/android/media/RemoteController.MetadataEditor) |---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RemoteControlClient.MetadataEditor](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.MetadataEditor) | Class used to modify metadata in a [RemoteControlClient](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient) object. | | [RemoteController.MetadataEditor](https://developer.android.com/reference/kotlin/android/media/RemoteController.MetadataEditor) | A class to read the metadata published by a [RemoteControlClient](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient), or send a [RemoteControlClient](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient) new values for keys that can be edited. | |

| **This class was deprecated in API level 21.**
|
| Use [MediaMetadata](https://developer.android.com/reference/kotlin/android/media/MediaMetadata) instead together with [MediaSession](https://developer.android.com/reference/kotlin/android/media/session/MediaSession).

An abstract class for editing and storing metadata that can be published by [RemoteControlClient](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient). See the [RemoteControlClient.editMetadata(boolean)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#editMetadata(kotlin.Boolean)) method to instantiate a [RemoteControlClient.MetadataEditor](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.MetadataEditor) object.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BITMAP_KEY_ARTWORK](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#BITMAP_KEY_ARTWORK:kotlin.Int) The metadata key for the content artwork / album art. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATING_KEY_BY_OTHERS](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#RATING_KEY_BY_OTHERS:kotlin.Int) The metadata key for the content's average rating, not the user's rating. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATING_KEY_BY_USER](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#RATING_KEY_BY_USER:kotlin.Int) The metadata key for the content's user rating. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addEditableKey](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#addEditableKey(kotlin.Int))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flags the given key as being editable. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [apply](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#apply())`()` Applies all of the metadata changes that have been set since the MediaMetadataEditor instance was created or since [clear()](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#clear()) was called. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#clear())`()` Clears all the pending metadata changes set since the MediaMetadataEditor instance was created or since this method was last called. |
| open [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)! | [getBitmap](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#getBitmap(kotlin.Int,%20android.graphics.Bitmap))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defaultValue:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!`)` Returns the [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) value for the key. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [getEditableKeys](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#getEditableKeys())`()` Retrieves the keys flagged as editable. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#getLong(kotlin.Int,%20kotlin.Long))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defaultValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the long value for the key. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getObject](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#getObject(kotlin.Int,%20kotlin.Any))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defaultValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Returns an object representation of the value for the key |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#getString(kotlin.Int,%20kotlin.String))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defaultValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) value for the key. |
| open [MediaMetadataEditor](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#)! | [putBitmap](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#putBitmap(kotlin.Int,%20android.graphics.Bitmap))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bitmap:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!`)` Adds image. |
| open [MediaMetadataEditor](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#)! | [putLong](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#putLong(kotlin.Int,%20kotlin.Long))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Adds numerical information. |
| open [MediaMetadataEditor](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#)! | [putObject](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#putObject(kotlin.Int,%20kotlin.Any))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Adds information stored as an instance. |
| open [MediaMetadataEditor](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#)! | [putString](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#putString(kotlin.Int,%20kotlin.String))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adds textual information. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeEditableKeys](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#removeEditableKeys())`()` Causes all metadata fields to be read-only. |

## Constants

### BITMAP_KEY_ARTWORK

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BITMAP_KEY_ARTWORK: Int
```

**Deprecated:** *Deprecated in Java.*

The metadata key for the content artwork / album art. 

 Value: 100

### RATING_KEY_BY_OTHERS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RATING_KEY_BY_OTHERS: Int
```

**Deprecated:** *Deprecated in Java.*

The metadata key for the content's average rating, not the user's rating. The value associated with this key is a [Rating](https://developer.android.com/reference/kotlin/android/media/Rating) instance. 

 Value: 101

**See Also**

- [#RATING_KEY_BY_USER](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#RATING_KEY_BY_USER:kotlin.Int) 

### RATING_KEY_BY_USER

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RATING_KEY_BY_USER: Int
```

**Deprecated:** *Deprecated in Java.*

The metadata key for the content's user rating. The value associated with this key is a [Rating](https://developer.android.com/reference/kotlin/android/media/Rating) instance. This key can be flagged as "editable" (with [addEditableKey(int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#addEditableKey(kotlin.Int))) to enable receiving user rating values through the [android.media.RemoteControlClient.OnMetadataUpdateListener](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.OnMetadataUpdateListener) interface. 

 Value: 268435457

## Public methods

### addEditableKey

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addEditableKey(key: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Flags the given key as being editable. This should only be used by metadata publishers, such as [RemoteControlClient](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient), which will declare the metadata field as eligible to be updated, with new values received through the [RemoteControlClient.OnMetadataUpdateListener](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.OnMetadataUpdateListener) interface.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the type of metadata that can be edited. The supported key is [RATING_KEY_BY_USER](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#RATING_KEY_BY_USER:kotlin.Int). |

### apply

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun apply(): Unit
```

**Deprecated:** *Deprecated in Java.*

Applies all of the metadata changes that have been set since the MediaMetadataEditor instance was created or since [clear()](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#clear()) was called. Subclasses should synchronize on `this` for thread safety. 

### clear

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

**Deprecated:** *Deprecated in Java.*

Clears all the pending metadata changes set since the MediaMetadataEditor instance was created or since this method was last called. Note that clearing the metadata doesn't reset the editable keys (use [removeEditableKeys()](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#removeEditableKeys()) instead). 

### getBitmap

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBitmap(
    key: Int, 
    defaultValue: Bitmap!
): Bitmap!
```

**Deprecated:** *Deprecated in Java.*

Returns the [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) value for the key.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the [BITMAP_KEY_ARTWORK](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#BITMAP_KEY_ARTWORK:kotlin.Int) key |
| `defaultValue` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!: the value returned if the key is not present |

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)! | the [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) value for the key, or the supplied default value if the key is not present |

| Exceptions ||
|--------------------------------------|---|
| `java.lang.IllegalArgumentException` | |

### getEditableKeys

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEditableKeys(): IntArray!
```

**Deprecated:** *Deprecated in Java.*

Retrieves the keys flagged as editable.

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | null if there are no editable keys, or an array containing the keys. |

### getLong

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLong(
    key: Int, 
    defaultValue: Long
): Long
```

**Deprecated:** *Deprecated in Java.*

Returns the long value for the key.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of the keys supported in [putLong(int,long)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#putLong(kotlin.Int,%20kotlin.Long)) |
| `defaultValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the value returned if the key is not present |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the long value for the key, or the supplied default value if the key is not present |

| Exceptions ||
|--------------------------------------|---|
| `java.lang.IllegalArgumentException` | |

### getObject

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getObject(
    key: Int, 
    defaultValue: Any!
): Any!
```

**Deprecated:** *Deprecated in Java.*

Returns an object representation of the value for the key

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of the keys supported in [putObject(int,java.lang.Object)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#putObject(kotlin.Int,%20kotlin.Any)) |
| `defaultValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the value returned if the key is not present |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the object for the key, as a [Long](https://developer.android.com/reference/kotlin/java/lang/Long.html#), [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#), [String](https://developer.android.com/reference/kotlin/java/lang/String.html#), or [Rating](https://developer.android.com/reference/kotlin/android/media/Rating) depending on the key value, or the supplied default value if the key is not present |

| Exceptions ||
|--------------------------------------|---|
| `java.lang.IllegalArgumentException` | |

### getString

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getString(
    key: Int, 
    defaultValue: String!
): String!
```

**Deprecated:** *Deprecated in Java.*

Returns the [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) value for the key.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of the keys supported in [putString(int,java.lang.String)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#putString(kotlin.Int,%20kotlin.String)) |
| `defaultValue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the value returned if the key is not present |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) value for the key, or the supplied default value if the key is not present |

| Exceptions ||
|--------------------------------------|---|
| `java.lang.IllegalArgumentException` | |

### putBitmap

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putBitmap(
    key: Int, 
    bitmap: Bitmap!
): MediaMetadataEditor!
```

**Deprecated:** *Deprecated in Java.*

Adds image.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the identifier of the bitmap to set. The only valid value is [BITMAP_KEY_ARTWORK](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#BITMAP_KEY_ARTWORK:kotlin.Int) |
| `bitmap` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!: The bitmap for the artwork, or null if there isn't any. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [MediaMetadataEditor](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#)! | Returns a reference to the same MediaMetadataEditor object, so you can chain put calls together. |

| Exceptions ||
|--------------------------------------|---|
| `java.lang.IllegalArgumentException` | |

**See Also**

- [android.graphics.Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) 

### putLong

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putLong(
    key: Int, 
    value: Long
): MediaMetadataEditor!
```

**Deprecated:** *Deprecated in Java.*

Adds numerical information. Note that none of the information added after [apply()](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#apply()) has been called will be available to consumers of metadata stored by the MediaMetadataEditor.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the identifier of a the metadata field to set. Valid values are [android.media.MediaMetadataRetriever#METADATA_KEY_CD_TRACK_NUMBER](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_CD_TRACK_NUMBER:kotlin.Int), [android.media.MediaMetadataRetriever#METADATA_KEY_DISC_NUMBER](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_DISC_NUMBER:kotlin.Int), [android.media.MediaMetadataRetriever#METADATA_KEY_DURATION](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_DURATION:kotlin.Int) (with a value expressed in milliseconds), [android.media.MediaMetadataRetriever#METADATA_KEY_YEAR](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_YEAR:kotlin.Int). |
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The long value for the given key |

| Return ||
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [MediaMetadataEditor](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#)! | Returns a reference to the same MediaMetadataEditor object, so you can chain put calls together. |

| Exceptions ||
|--------------------------------------|---|
| `java.lang.IllegalArgumentException` | |

### putObject

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putObject(
    key: Int, 
    value: Any!
): MediaMetadataEditor!
```

**Deprecated:** *Deprecated in Java.*

Adds information stored as an instance. Note that none of the information added after [apply()](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#apply()) has been called will be available to consumers of metadata stored by the MediaMetadataEditor.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the identifier of a the metadata field to set. Valid keys for a: - [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) object are [BITMAP_KEY_ARTWORK](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#BITMAP_KEY_ARTWORK:kotlin.Int), - [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) object are the same as for [putString(int,java.lang.String)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#putString(kotlin.Int,%20kotlin.String)) - [Long](https://developer.android.com/reference/kotlin/java/lang/Long.html#) object are the same as for [putLong(int,long)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#putLong(kotlin.Int,%20kotlin.Long)) - [Rating](https://developer.android.com/reference/kotlin/android/media/Rating) object are [RATING_KEY_BY_OTHERS](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#RATING_KEY_BY_OTHERS:kotlin.Int) and [RATING_KEY_BY_USER](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#RATING_KEY_BY_USER:kotlin.Int). |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the metadata to add. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [MediaMetadataEditor](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#)! | Returns a reference to the same MediaMetadataEditor object, so you can chain put calls together. |

| Exceptions ||
|--------------------------------------|---|
| `java.lang.IllegalArgumentException` | |

### putString

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putString(
    key: Int, 
    value: String!
): MediaMetadataEditor!
```

**Deprecated:** *Deprecated in Java.*

Adds textual information. Note that none of the information added after [apply()](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#apply()) has been called, will be available to consumers of metadata stored by the MediaMetadataEditor.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The identifier of a the metadata field to set. Valid values are [android.media.MediaMetadataRetriever#METADATA_KEY_ALBUM](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_ALBUM:kotlin.Int), [android.media.MediaMetadataRetriever#METADATA_KEY_ALBUMARTIST](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_ALBUMARTIST:kotlin.Int), [android.media.MediaMetadataRetriever#METADATA_KEY_TITLE](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_TITLE:kotlin.Int), [android.media.MediaMetadataRetriever#METADATA_KEY_ARTIST](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_ARTIST:kotlin.Int), [android.media.MediaMetadataRetriever#METADATA_KEY_AUTHOR](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_AUTHOR:kotlin.Int), [android.media.MediaMetadataRetriever#METADATA_KEY_COMPILATION](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_COMPILATION:kotlin.Int), [android.media.MediaMetadataRetriever#METADATA_KEY_COMPOSER](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_COMPOSER:kotlin.Int), [android.media.MediaMetadataRetriever#METADATA_KEY_DATE](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_DATE:kotlin.Int), [android.media.MediaMetadataRetriever#METADATA_KEY_GENRE](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_GENRE:kotlin.Int), [android.media.MediaMetadataRetriever#METADATA_KEY_WRITER](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_WRITER:kotlin.Int). |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The text for the given key, or `null` to signify there is no valid information for the field. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [MediaMetadataEditor](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#)! | Returns a reference to the same MediaMetadataEditor object, so you can chain put calls together. |

### removeEditableKeys

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeEditableKeys(): Unit
```

**Deprecated:** *Deprecated in Java.*

Causes all metadata fields to be read-only.

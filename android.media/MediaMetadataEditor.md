# MediaMetadataEditor

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaMetadataEditor

Kotlin | [Java](../android/media/MediaMetadataEditor.md) 
| --- | --- |

```
abstract class MediaMetadataEditor
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaMetadataEditor](../android/media/MediaMetadataEditor.md) |

| Known Direct Subclasses [RemoteControlClient.MetadataEditor](../android/media/RemoteControlClient.MetadataEditor.md), [RemoteController.MetadataEditor](../android/media/RemoteController.MetadataEditor.md) |---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RemoteControlClient.MetadataEditor](../android/media/RemoteControlClient.MetadataEditor.md) | Class used to modify metadata in a [RemoteControlClient](../android/media/RemoteControlClient.md) object. | | [RemoteController.MetadataEditor](../android/media/RemoteController.MetadataEditor.md) | A class to read the metadata published by a [RemoteControlClient](../android/media/RemoteControlClient.md), or send a [RemoteControlClient](../android/media/RemoteControlClient.md) new values for keys that can be edited. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 21.**
|
| Use [MediaMetadata](../android/media/MediaMetadata.md) instead together with [MediaSession](../android/media/session/MediaSession.md).

An abstract class for editing and storing metadata that can be published by [RemoteControlClient](../android/media/RemoteControlClient.md). See the [RemoteControlClient.editMetadata(boolean)](../android/media/RemoteControlClient.md)) method to instantiate a [RemoteControlClient.MetadataEditor](../android/media/RemoteControlClient.MetadataEditor.md) object.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BITMAP_KEY_ARTWORK](../android/media/MediaMetadataEditor.md) The metadata key for the content artwork / album art. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATING_KEY_BY_OTHERS](../android/media/MediaMetadataEditor.md) The metadata key for the content's average rating, not the user's rating. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATING_KEY_BY_USER](../android/media/MediaMetadataEditor.md) The metadata key for the content's user rating. |
| --- | --- |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addEditableKey](../android/media/MediaMetadataEditor.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flags the given key as being editable. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [apply](../android/media/MediaMetadataEditor.md))`()` Applies all of the metadata changes that have been set since the MediaMetadataEditor instance was created or since [clear()](../android/media/MediaMetadataEditor.md)) was called. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](../android/media/MediaMetadataEditor.md))`()` Clears all the pending metadata changes set since the MediaMetadataEditor instance was created or since this method was last called. |
| --- | --- |
| open [Bitmap](../android/graphics/Bitmap.md)! | [getBitmap](../android/media/MediaMetadataEditor.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defaultValue:` ` [Bitmap](../android/graphics/Bitmap.md)!`)` Returns the [Bitmap](../android/graphics/Bitmap.md) value for the key. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [getEditableKeys](../android/media/MediaMetadataEditor.md))`()` Retrieves the keys flagged as editable. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](../android/media/MediaMetadataEditor.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defaultValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the long value for the key. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getObject](../android/media/MediaMetadataEditor.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defaultValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Returns an object representation of the value for the key |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](../android/media/MediaMetadataEditor.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defaultValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the [String](../java/lang/String.md) value for the key. |
| open [MediaMetadataEditor](../android/media/MediaMetadataEditor.md)! | [putBitmap](../android/media/MediaMetadataEditor.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bitmap:` ` [Bitmap](../android/graphics/Bitmap.md)!`)` Adds image. |
| --- | --- |
| open [MediaMetadataEditor](../android/media/MediaMetadataEditor.md)! | [putLong](../android/media/MediaMetadataEditor.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Adds numerical information. |
| open [MediaMetadataEditor](../android/media/MediaMetadataEditor.md)! | [putObject](../android/media/MediaMetadataEditor.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Adds information stored as an instance. |
| open [MediaMetadataEditor](../android/media/MediaMetadataEditor.md)! | [putString](../android/media/MediaMetadataEditor.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adds textual information. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeEditableKeys](../android/media/MediaMetadataEditor.md))`()` Causes all metadata fields to be read-only. |

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

The metadata key for the content's average rating, not the user's rating. The value associated with this key is a [Rating](../android/media/Rating.md) instance. 

 Value: 101

**See Also**

- [#RATING_KEY_BY_USER](../android/media/MediaMetadataEditor.md) 

### RATING_KEY_BY_USER

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RATING_KEY_BY_USER: Int
```

**Deprecated:** *Deprecated in Java.*

The metadata key for the content's user rating. The value associated with this key is a [Rating](../android/media/Rating.md) instance. This key can be flagged as "editable" (with [addEditableKey(int)](../android/media/MediaMetadataEditor.md))) to enable receiving user rating values through the [android.media.RemoteControlClient.OnMetadataUpdateListener](../android/media/RemoteControlClient.OnMetadataUpdateListener.md) interface. 

 Value: 268435457

## Public methods

### addEditableKey

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addEditableKey(key: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Flags the given key as being editable. This should only be used by metadata publishers, such as [RemoteControlClient](../android/media/RemoteControlClient.md), which will declare the metadata field as eligible to be updated, with new values received through the [RemoteControlClient.OnMetadataUpdateListener](../android/media/RemoteControlClient.OnMetadataUpdateListener.md) interface.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the type of metadata that can be edited. The supported key is [RATING_KEY_BY_USER](../android/media/MediaMetadataEditor.md). |

### apply

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun apply(): Unit
```

**Deprecated:** *Deprecated in Java.*

Applies all of the metadata changes that have been set since the MediaMetadataEditor instance was created or since [clear()](../android/media/MediaMetadataEditor.md)) was called. Subclasses should synchronize on `this` for thread safety. 

### clear

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

**Deprecated:** *Deprecated in Java.*

Clears all the pending metadata changes set since the MediaMetadataEditor instance was created or since this method was last called. Note that clearing the metadata doesn't reset the editable keys (use [removeEditableKeys()](../android/media/MediaMetadataEditor.md)) instead). 

### getBitmap

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBitmap(
    key: Int, 
    defaultValue: Bitmap!
): Bitmap!
```

**Deprecated:** *Deprecated in Java.*

Returns the [Bitmap](../android/graphics/Bitmap.md) value for the key.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the [BITMAP_KEY_ARTWORK](../android/media/MediaMetadataEditor.md) key |
| `defaultValue` | [Bitmap](../android/graphics/Bitmap.md)!: the value returned if the key is not present |

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmap](../android/graphics/Bitmap.md)! | the [Bitmap](../android/graphics/Bitmap.md) value for the key, or the supplied default value if the key is not present |

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
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of the keys supported in [putLong(int,long)](../android/media/MediaMetadataEditor.md)) |
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
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of the keys supported in [putObject(int,java.lang.Object)](../android/media/MediaMetadataEditor.md)) |
| `defaultValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the value returned if the key is not present |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the object for the key, as a [Long](../java/lang/Long.md), [Bitmap](../android/graphics/Bitmap.md), [String](../java/lang/String.md), or [Rating](../android/media/Rating.md) depending on the key value, or the supplied default value if the key is not present |

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

Returns the [String](../java/lang/String.md) value for the key.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of the keys supported in [putString(int,java.lang.String)](../android/media/MediaMetadataEditor.md)) |
| `defaultValue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the value returned if the key is not present |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the [String](../java/lang/String.md) value for the key, or the supplied default value if the key is not present |

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
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the identifier of the bitmap to set. The only valid value is [BITMAP_KEY_ARTWORK](../android/media/MediaMetadataEditor.md) |
| `bitmap` | [Bitmap](../android/graphics/Bitmap.md)!: The bitmap for the artwork, or null if there isn't any. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [MediaMetadataEditor](../android/media/MediaMetadataEditor.md)! | Returns a reference to the same MediaMetadataEditor object, so you can chain put calls together. |

| Exceptions ||
|--------------------------------------|---|
| `java.lang.IllegalArgumentException` | |

**See Also**

- [android.graphics.Bitmap](../android/graphics/Bitmap.md) 

### putLong

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putLong(
    key: Int, 
    value: Long
): MediaMetadataEditor!
```

**Deprecated:** *Deprecated in Java.*

Adds numerical information. Note that none of the information added after [apply()](../android/media/MediaMetadataEditor.md)) has been called will be available to consumers of metadata stored by the MediaMetadataEditor.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the identifier of a the metadata field to set. Valid values are [android.media.MediaMetadataRetriever#METADATA_KEY_CD_TRACK_NUMBER](../android/media/MediaMetadataRetriever.md), [android.media.MediaMetadataRetriever#METADATA_KEY_DISC_NUMBER](../android/media/MediaMetadataRetriever.md), [android.media.MediaMetadataRetriever#METADATA_KEY_DURATION](../android/media/MediaMetadataRetriever.md) (with a value expressed in milliseconds), [android.media.MediaMetadataRetriever#METADATA_KEY_YEAR](../android/media/MediaMetadataRetriever.md). |
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The long value for the given key |

| Return ||
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [MediaMetadataEditor](../android/media/MediaMetadataEditor.md)! | Returns a reference to the same MediaMetadataEditor object, so you can chain put calls together. |

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

Adds information stored as an instance. Note that none of the information added after [apply()](../android/media/MediaMetadataEditor.md)) has been called will be available to consumers of metadata stored by the MediaMetadataEditor.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the identifier of a the metadata field to set. Valid keys for a: - [Bitmap](../android/graphics/Bitmap.md) object are [BITMAP_KEY_ARTWORK](../android/media/MediaMetadataEditor.md), - [String](../java/lang/String.md) object are the same as for [putString(int,java.lang.String)](../android/media/MediaMetadataEditor.md)) - [Long](../java/lang/Long.md) object are the same as for [putLong(int,long)](../android/media/MediaMetadataEditor.md)) - [Rating](../android/media/Rating.md) object are [RATING_KEY_BY_OTHERS](../android/media/MediaMetadataEditor.md) and [RATING_KEY_BY_USER](../android/media/MediaMetadataEditor.md). |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the metadata to add. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [MediaMetadataEditor](../android/media/MediaMetadataEditor.md)! | Returns a reference to the same MediaMetadataEditor object, so you can chain put calls together. |

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

Adds textual information. Note that none of the information added after [apply()](../android/media/MediaMetadataEditor.md)) has been called, will be available to consumers of metadata stored by the MediaMetadataEditor.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The identifier of a the metadata field to set. Valid values are [android.media.MediaMetadataRetriever#METADATA_KEY_ALBUM](../android/media/MediaMetadataRetriever.md), [android.media.MediaMetadataRetriever#METADATA_KEY_ALBUMARTIST](../android/media/MediaMetadataRetriever.md), [android.media.MediaMetadataRetriever#METADATA_KEY_TITLE](../android/media/MediaMetadataRetriever.md), [android.media.MediaMetadataRetriever#METADATA_KEY_ARTIST](../android/media/MediaMetadataRetriever.md), [android.media.MediaMetadataRetriever#METADATA_KEY_AUTHOR](../android/media/MediaMetadataRetriever.md), [android.media.MediaMetadataRetriever#METADATA_KEY_COMPILATION](../android/media/MediaMetadataRetriever.md), [android.media.MediaMetadataRetriever#METADATA_KEY_COMPOSER](../android/media/MediaMetadataRetriever.md), [android.media.MediaMetadataRetriever#METADATA_KEY_DATE](../android/media/MediaMetadataRetriever.md), [android.media.MediaMetadataRetriever#METADATA_KEY_GENRE](../android/media/MediaMetadataRetriever.md), [android.media.MediaMetadataRetriever#METADATA_KEY_WRITER](../android/media/MediaMetadataRetriever.md). |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The text for the given key, or `null` to signify there is no valid information for the field. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [MediaMetadataEditor](../android/media/MediaMetadataEditor.md)! | Returns a reference to the same MediaMetadataEditor object, so you can chain put calls together. |

### removeEditableKeys

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeEditableKeys(): Unit
```

**Deprecated:** *Deprecated in Java.*

Causes all metadata fields to be read-only.

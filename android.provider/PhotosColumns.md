# Contacts.PhotosColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PhotosColumns

Kotlin| [Java](../android/provider/Contacts.PhotosColumns.md) 
| --- | --- |

```
interface PhotosColumns
```

| [android.provider.Contacts.PhotosColumns](../android/provider/Contacts.PhotosColumns.md) |

| Known Direct Subclasses [Contacts.Photos](../android/provider/Contacts.Photos.md) |----------------------------------------------------------------------------------------------------|-----------------------------------| | [Contacts.Photos](../android/provider/Contacts.Photos.md) | The photos over all of the people | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 5.**
|
| see [android.provider.ContactsContract](../android/provider/ContactsContract.md)

Columns from the Photos table that other columns join into themselves.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA](../android/provider/Contacts.PhotosColumns.md) The image data, or null if there is no image. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DOWNLOAD_REQUIRED](../android/provider/Contacts.PhotosColumns.md) non-zero if a download is required and the photo isn't marked as a bad resource. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXISTS_ON_SERVER](../android/provider/Contacts.PhotosColumns.md) non-zero if this photo is known to exist on the server |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LOCAL_VERSION](../android/provider/Contacts.PhotosColumns.md) The _SYNC_VERSION of the photo that was last downloaded |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PERSON_ID](../android/provider/Contacts.PhotosColumns.md) The person this photo is associated with. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_ERROR](../android/provider/Contacts.PhotosColumns.md) Contains the description of the upload or download error from the previous attempt. |
| --- | --- |

## Constants

### DATA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA: String
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

The image data, or null if there is no image.

Type: BLOB 

 Value: "data"

### DOWNLOAD_REQUIRED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOWNLOAD_REQUIRED: String
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

non-zero if a download is required and the photo isn't marked as a bad resource. You must specify this in the columns in order to use it in the where clause.

Type: INTEGER(boolean) 

 Value: "download_required"

### EXISTS_ON_SERVER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXISTS_ON_SERVER: String
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

non-zero if this photo is known to exist on the server

Type: INTEGER(boolean) 

 Value: "exists_on_server"

### LOCAL_VERSION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCAL_VERSION: String
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

The _SYNC_VERSION of the photo that was last downloaded

Type: TEXT 

 Value: "local_version"

### PERSON_ID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERSON_ID: String
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

The person this photo is associated with.

Type: TEXT 

 Value: "person"

### SYNC_ERROR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_ERROR: String
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

Contains the description of the upload or download error from the previous attempt. If null then the previous attempt succeeded.

Type: TEXT 

 Value: "sync_error"

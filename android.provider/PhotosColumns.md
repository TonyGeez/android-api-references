# Contacts.PhotosColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PhotosColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/Contacts.PhotosColumns "View this page in Java") 
| --- | --- |

```
interface PhotosColumns
```

| [android.provider.Contacts.PhotosColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhotosColumns#) |

| Known Direct Subclasses [Contacts.Photos](https://developer.android.com/reference/kotlin/android/provider/Contacts.Photos) |----------------------------------------------------------------------------------------------------|-----------------------------------| | [Contacts.Photos](https://developer.android.com/reference/kotlin/android/provider/Contacts.Photos) | The photos over all of the people | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 5.**
|
| see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)

Columns from the Photos table that other columns join into themselves.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhotosColumns#DATA:kotlin.String) The image data, or null if there is no image. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DOWNLOAD_REQUIRED](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhotosColumns#DOWNLOAD_REQUIRED:kotlin.String) non-zero if a download is required and the photo isn't marked as a bad resource. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXISTS_ON_SERVER](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhotosColumns#EXISTS_ON_SERVER:kotlin.String) non-zero if this photo is known to exist on the server |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LOCAL_VERSION](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhotosColumns#LOCAL_VERSION:kotlin.String) The _SYNC_VERSION of the photo that was last downloaded |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PERSON_ID](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhotosColumns#PERSON_ID:kotlin.String) The person this photo is associated with. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_ERROR](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhotosColumns#SYNC_ERROR:kotlin.String) Contains the description of the upload or download error from the previous attempt. |
| --- | --- |

## Constants

### DATA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The image data, or null if there is no image.

Type: BLOB 

 Value: "data"

### DOWNLOAD_REQUIRED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOWNLOAD_REQUIRED: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

non-zero if a download is required and the photo isn't marked as a bad resource. You must specify this in the columns in order to use it in the where clause.

Type: INTEGER(boolean) 

 Value: "download_required"

### EXISTS_ON_SERVER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXISTS_ON_SERVER: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

non-zero if this photo is known to exist on the server

Type: INTEGER(boolean) 

 Value: "exists_on_server"

### LOCAL_VERSION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCAL_VERSION: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The _SYNC_VERSION of the photo that was last downloaded

Type: TEXT 

 Value: "local_version"

### PERSON_ID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERSON_ID: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The person this photo is associated with.

Type: TEXT 

 Value: "person"

### SYNC_ERROR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_ERROR: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

Contains the description of the upload or download error from the previous attempt. If null then the previous attempt succeeded.

Type: TEXT 

 Value: "sync_error"

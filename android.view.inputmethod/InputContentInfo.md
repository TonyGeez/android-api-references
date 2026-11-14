# InputContentInfo

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputContentInfo

Kotlin| [Java](https://developer.android.com/reference/android/view/inputmethod/InputContentInfo "View this page in Java") 
| --- | --- |

```
class InputContentInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inputmethod.InputContentInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo#) |

A container object with which input methods can send content files to the target application.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InputContentInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo#InputContentInfo(android.net.Uri,%20android.content.ClipDescription))`(`contentUri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `description:` ` [ClipDescription](https://developer.android.com/reference/kotlin/android/content/ClipDescription.html#)`)` Constructs [InputContentInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo#) object only with mandatory data. |
| [InputContentInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo#InputContentInfo(android.net.Uri,%20android.content.ClipDescription,%20android.net.Uri))`(`contentUri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `description:` ` [ClipDescription](https://developer.android.com/reference/kotlin/android/content/ClipDescription.html#)`, `linkUri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?`)` Constructs [InputContentInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo#) object with additional link URI. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo#describeContents())`()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | [getContentUri](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo#getContentUri())`()` <br /> |
| [ClipDescription](https://developer.android.com/reference/kotlin/android/content/ClipDescription.html#) | [getDescription](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo#getDescription())`()` <br /> |
| --- | --- |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [getLinkUri](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo#getLinkUri())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releasePermission](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo#releasePermission())`()` Releases a temporary read-only access permission for content URI associated with this object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestPermission](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo#requestPermission())`()` Requests a temporary [read-only](https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int) access permission for the content URI associated with this object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used to package this object into a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#). |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [InputContentInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo#CREATOR:android.os.Parcelable.Creator) Used to make this class parcelable. |

## Public constructors

### InputContentInfo

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InputContentInfo(
    contentUri: Uri, 
    description: ClipDescription)
```

Constructs [InputContentInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo#) object only with mandatory data.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `contentUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):Content URI to be exported from the input method. This cannot be`null`. |
| `description` | [ClipDescription](https://developer.android.com/reference/kotlin/android/content/ClipDescription.html#):A [ClipDescription](https://developer.android.com/reference/kotlin/android/content/ClipDescription.html#) object that contains the metadata of`contentUri`such as MIME type(s). This object cannot be`null`. Also [ClipDescription.getLabel()](https://developer.android.com/reference/kotlin/android/content/ClipDescription.html#getLabel())should be describing the content specified by`contentUri`for accessibility reasons. |

### InputContentInfo

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InputContentInfo(
    contentUri: Uri, 
    description: ClipDescription, 
    linkUri: Uri?)
```

Constructs [InputContentInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo#) object with additional link URI.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `contentUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):Content URI to be exported from the input method. This cannot be`null`. |
| `description` | [ClipDescription](https://developer.android.com/reference/kotlin/android/content/ClipDescription.html#):A [ClipDescription](https://developer.android.com/reference/kotlin/android/content/ClipDescription.html#) object that contains the metadata of`contentUri`such as MIME type(s). This object cannot be`null`. Also [ClipDescription.getLabel()](https://developer.android.com/reference/kotlin/android/content/ClipDescription.html#getLabel())should be describing the content specified by`contentUri`for accessibility reasons. |
| `linkUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?:An optional`http`or`https`URI. The editor author may provide a way to navigate the user to the specified web page if this is not`null`. |
| --- | --- |

| Exceptions ||
|-------------------------------------------|----------------------------------------|
| `java.security.InvalidParameterException` | if any invalid parameter is specified. |

## Public methods

### describeContents

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of [writeToParcel(android.os.Parcel,int)](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)), the return value of this method must include the [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) bit.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getContentUri

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContentUri(): Uri
```

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | Content URI with which the content can be obtained. This value cannot be`null`. |

### getDescription

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDescription(): ClipDescription
```

| Return ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ClipDescription](https://developer.android.com/reference/kotlin/android/content/ClipDescription.html#) | [ClipDescription](https://developer.android.com/reference/kotlin/android/content/ClipDescription.html#) object that contains the metadata of`getContentUri()`such as MIME type(s). [ClipDescription.getLabel()](https://developer.android.com/reference/kotlin/android/content/ClipDescription.html#getLabel())can be used for accessibility purpose. This value cannot be`null`. |

### getLinkUri

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLinkUri(): Uri?
```

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | An optional`http`or`https`URI that is related to this content. This value may be`null`. |

### releasePermission

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun releasePermission(): Unit
```

Releases a temporary read-only access permission for content URI associated with this object.

Does nothing if the temporary permission is not granted. 

### requestPermission

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun requestPermission(): Unit
```

Requests a temporary [read-only](https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int) access permission for the content URI associated with this object.

The lifecycle of the permission granted here is tied to this object instance. If the permission is not released explicitly via [releasePermission()](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo#releasePermission()), it will be released automatically when there are no more references to this object.

Does nothing if the temporary permission is already granted. 

### writeToParcel

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Used to package this object into a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#) to be written. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<InputContentInfo!>
```

Used to make this class parcelable.

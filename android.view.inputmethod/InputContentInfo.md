# InputContentInfo

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputContentInfo

Kotlin| [Java](../android/view/inputmethod/InputContentInfo.md) 
| --- | --- |

```
class InputContentInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inputmethod.InputContentInfo](../android/view/inputmethod/InputContentInfo.md) |

A container object with which input methods can send content files to the target application.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InputContentInfo](../android/view/inputmethod/InputContentInfo.md))`(`contentUri:` ` [Uri](../android/net/Uri.md)`, `description:` ` [ClipDescription](../android/content/ClipDescription.md)`)` Constructs [InputContentInfo](../android/view/inputmethod/InputContentInfo.md) object only with mandatory data. |
| [InputContentInfo](../android/view/inputmethod/InputContentInfo.md))`(`contentUri:` ` [Uri](../android/net/Uri.md)`, `description:` ` [ClipDescription](../android/content/ClipDescription.md)`, `linkUri:` ` [Uri](../android/net/Uri.md)?`)` Constructs [InputContentInfo](../android/view/inputmethod/InputContentInfo.md) object with additional link URI. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/view/inputmethod/InputContentInfo.md))`()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Uri](../android/net/Uri.md) | [getContentUri](../android/view/inputmethod/InputContentInfo.md))`()` <br /> |
| [ClipDescription](../android/content/ClipDescription.md) | [getDescription](../android/view/inputmethod/InputContentInfo.md))`()` <br /> |
| --- | --- |
| [Uri](../android/net/Uri.md)? | [getLinkUri](../android/view/inputmethod/InputContentInfo.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releasePermission](../android/view/inputmethod/InputContentInfo.md))`()` Releases a temporary read-only access permission for content URI associated with this object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestPermission](../android/view/inputmethod/InputContentInfo.md))`()` Requests a temporary [read-only](../android/content/Intent.md) access permission for the content URI associated with this object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/view/inputmethod/InputContentInfo.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used to package this object into a [Parcel](../android/os/Parcel.md). |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [InputContentInfo](../android/view/inputmethod/InputContentInfo.md)!\> | [CREATOR](../android/view/inputmethod/InputContentInfo.md) Used to make this class parcelable. |

## Public constructors

### InputContentInfo

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InputContentInfo(
    contentUri: Uri, 
    description: ClipDescription)
```

Constructs [InputContentInfo](../android/view/inputmethod/InputContentInfo.md) object only with mandatory data.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `contentUri` | [Uri](../android/net/Uri.md):Content URI to be exported from the input method. This cannot be`null`. |
| `description` | [ClipDescription](../android/content/ClipDescription.md):A [ClipDescription](../android/content/ClipDescription.md) object that contains the metadata of`contentUri`such as MIME type(s). This object cannot be`null`. Also [ClipDescription.getLabel()](../android/content/ClipDescription.md))should be describing the content specified by`contentUri`for accessibility reasons. |

### InputContentInfo

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InputContentInfo(
    contentUri: Uri, 
    description: ClipDescription, 
    linkUri: Uri?)
```

Constructs [InputContentInfo](../android/view/inputmethod/InputContentInfo.md) object with additional link URI.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `contentUri` | [Uri](../android/net/Uri.md):Content URI to be exported from the input method. This cannot be`null`. |
| `description` | [ClipDescription](../android/content/ClipDescription.md):A [ClipDescription](../android/content/ClipDescription.md) object that contains the metadata of`contentUri`such as MIME type(s). This object cannot be`null`. Also [ClipDescription.getLabel()](../android/content/ClipDescription.md))should be describing the content specified by`contentUri`for accessibility reasons. |
| `linkUri` | [Uri](../android/net/Uri.md)?:An optional`http`or`https`URI. The editor author may provide a way to navigate the user to the specified web page if this is not`null`. |
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

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of [writeToParcel(android.os.Parcel,int)](../android/os/Parcelable.md)), the return value of this method must include the [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) bit.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getContentUri

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContentUri(): Uri
```

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Uri](../android/net/Uri.md) | Content URI with which the content can be obtained. This value cannot be`null`. |

### getDescription

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDescription(): ClipDescription
```

| Return ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ClipDescription](../android/content/ClipDescription.md) | [ClipDescription](../android/content/ClipDescription.md) object that contains the metadata of`getContentUri()`such as MIME type(s). [ClipDescription.getLabel()](../android/content/ClipDescription.md))can be used for accessibility purpose. This value cannot be`null`. |

### getLinkUri

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLinkUri(): Uri?
```

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Uri](../android/net/Uri.md)? | An optional`http`or`https`URI that is related to this content. This value may be`null`. |

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

Requests a temporary [read-only](../android/content/Intent.md) access permission for the content URI associated with this object.

The lifecycle of the permission granted here is tied to this object instance. If the permission is not released explicitly via [releasePermission()](../android/view/inputmethod/InputContentInfo.md)), it will be released automatically when there are no more references to this object.

Does nothing if the temporary permission is already granted. 

### writeToParcel

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Used to package this object into a [Parcel](../android/os/Parcel.md).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The [Parcel](../android/os/Parcel.md) to be written. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<InputContentInfo!>
```

Used to make this class parcelable.

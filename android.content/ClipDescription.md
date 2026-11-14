Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClipDescription

```
open class ClipDescription : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.ClipDescription](ClipDescription.md) |

Meta-data describing the contents of a `https://developer.android.com/reference/kotlin/android/content/ClipData`. Provides enough information to know if you can handle the ClipData, but not the data itself.

> [!NOTE]
>
> ### Developer Guides
>
> For more information about using the clipboard framework, read the [Copy and Paste](https://developer.android.com/guide/topics/clipboard/copy-paste.html) developer guide.

<br />

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#CLASSIFICATION_COMPLETE:kotlin.Int` Value returned by `https://developer.android.com/reference/kotlin/android/content/ClipDescription#getConfidenceScore(kotlin.String)` if text classification has been completed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#CLASSIFICATION_NOT_COMPLETE:kotlin.Int` Value returned by `https://developer.android.com/reference/kotlin/android/content/ClipDescription#getConfidenceScore(kotlin.String)` if text classification has not been completed on the associated clip. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#CLASSIFICATION_NOT_PERFORMED:kotlin.Int` Value returned by `https://developer.android.com/reference/kotlin/android/content/ClipDescription#getConfidenceScore(kotlin.String)` if text classification was not and will not be performed on the associated clip. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#EXTRA_IS_REMOTE_DEVICE:kotlin.String` Indicates that a ClipData's source is a remote device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#EXTRA_IS_SENSITIVE:kotlin.String` Indicates that a ClipData contains potentially sensitive information, such as a password or credit card number. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#MIMETYPE_TEXT_HTML:kotlin.String` The MIME type for a clip holding HTML text. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#MIMETYPE_TEXT_INTENT:kotlin.String` The MIME type for a clip holding an Intent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#MIMETYPE_TEXT_PLAIN:kotlin.String` The MIME type for a clip holding plain text. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#MIMETYPE_TEXT_URILIST:kotlin.String` The MIME type for a clip holding one or more URIs. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#MIMETYPE_UNKNOWN:kotlin.String` The MIME type for data whose type is otherwise unknown. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/ClipDescription#ClipDescription(android.content.ClipDescription)(o: https://developer.android.com/reference/kotlin/android/content/ClipDescription#!)` Create a copy of a ClipDescription. |
| `https://developer.android.com/reference/kotlin/android/content/ClipDescription#ClipDescription(kotlin.CharSequence,%20kotlin.Array)(label: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, mimeTypes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Create a new clip. |

| Public methods ||
|---|---|
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#compareMimeTypes(kotlin.String,%20kotlin.String)(concreteType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, desiredType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Helper to compare two MIME types, where one may be a pattern. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#filterMimeTypes(kotlin.String)(mimeType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Filter the clip description MIME types by the given MIME type. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#getClassificationStatus()()` Returns `https://developer.android.com/reference/kotlin/android/content/ClipDescription#CLASSIFICATION_COMPLETE:kotlin.Int` if text classification has been performed on the associated `https://developer.android.com/reference/kotlin/android/content/ClipData`. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#getConfidenceScore(kotlin.String)(entity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns a score indicating confidence that an instance of the given entity is present in the first item of the clip data, if that item is plain text and text classification has been performed. |
| open [PersistableBundle](../android.os/PersistableBundle.md)! | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#getExtras()()` Retrieve extended data from the clip description. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#getLabel()()` Return the label for this clip. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#getMimeType(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return one of the possible clip MIME types. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#getMimeTypeCount()()` Return the number of MIME types the clip is available in. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#getSourceDeviceName()()` Returns the name of the source device where the clip originated from. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#getTimestamp()()` Return the timestamp at which the associated `https://developer.android.com/reference/kotlin/android/content/ClipData` is copied to global clipboard in the `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()` time base. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#hasMimeType(kotlin.String)(mimeType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Check whether the clip description contains the given MIME type. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#isExcludedFromRemoteClipboard()()` Returns true if this ClipData should be excluded from remote clipboard syncing. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#isRemoteClipboard()()` Returns true if this ClipData was set by a remote clipboard. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#isStyledText()()` Returns true if the first item of the associated `https://developer.android.com/reference/kotlin/android/content/ClipData` contains styled text, i. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#setExcludedFromRemoteClipboard(kotlin.Boolean)(excludeFromRemoteClipboard: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this ClipData should be excluded from remote clipboard syncing. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#setExtras(android.os.PersistableBundle)(extras: https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#!)` Add extended data to the clip description. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#toString()()` Returns a string representation of the object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ClipDescription](ClipDescription.md)!\> | `https://developer.android.com/reference/kotlin/android/content/ClipDescription#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### CLASSIFICATION_COMPLETE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CLASSIFICATION_COMPLETE: Int
```

Value returned by `https://developer.android.com/reference/kotlin/android/content/ClipDescription#getConfidenceScore(kotlin.String)` if text classification has been completed.

 Value: 3

### CLASSIFICATION_NOT_COMPLETE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CLASSIFICATION_NOT_COMPLETE: Int
```

Value returned by `https://developer.android.com/reference/kotlin/android/content/ClipDescription#getConfidenceScore(kotlin.String)` if text classification has not been completed on the associated clip. This will be always be the case if the clip has not been copied to clipboard, or if there is no associated clip.

 Value: 1

### CLASSIFICATION_NOT_PERFORMED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CLASSIFICATION_NOT_PERFORMED: Int
```

Value returned by `https://developer.android.com/reference/kotlin/android/content/ClipDescription#getConfidenceScore(kotlin.String)` if text classification was not and will not be performed on the associated clip. This may be the case if the clip does not contain text in its first item, or if the text is too long.

 Value: 2

### EXTRA_IS_REMOTE_DEVICE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_IS_REMOTE_DEVICE: String
```

Indicates that a ClipData's source is a remote device.

Type: boolean

This extra can be used to indicate that a ClipData comes from a separate device rather than being local. It is a rendering hint that can be used to take different behavior based on the source device of copied data.

 Value: "android.content.extra.IS_REMOTE_DEVICE"

### EXTRA_IS_SENSITIVE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_IS_SENSITIVE: String
```

Indicates that a ClipData contains potentially sensitive information, such as a password or credit card number.

Type: boolean

This extra can be used to indicate that a ClipData contains sensitive information that should be redacted or hidden from view until a user takes explicit action to reveal it (e.g., by pasting).

Adding this extra does not change clipboard behavior or add additional security to the ClipData. Its purpose is essentially a rendering hint from the source application, asking that the data within be obfuscated or redacted, unless the user has taken action to make it visible.

 Value: "android.content.extra.IS_SENSITIVE"

### MIMETYPE_TEXT_HTML

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_TEXT_HTML: String
```

The MIME type for a clip holding HTML text.

 Value: "text/html"

### MIMETYPE_TEXT_INTENT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_TEXT_INTENT: String
```

The MIME type for a clip holding an Intent.

 Value: "text/vnd.android.intent"

### MIMETYPE_TEXT_PLAIN

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_TEXT_PLAIN: String
```

The MIME type for a clip holding plain text.

 Value: "text/plain"

### MIMETYPE_TEXT_URILIST

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_TEXT_URILIST: String
```

The MIME type for a clip holding one or more URIs. This should be used for URIs that are meaningful to a user (such as an http: URI). It should *not* be used for a content: URI that references some other piece of data; in that case the MIME type should be the type of the referenced data.

 Value: "text/uri-list"

### MIMETYPE_UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_UNKNOWN: String
```

The MIME type for data whose type is otherwise unknown.

Per RFC 2046, the "application" media type is to be used for discrete data which do not fit in any of the other categories, and the "octet-stream" subtype is used to indicate that a body contains arbitrary binary data.

 Value: "application/octet-stream"

## Public constructors

### ClipDescription

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ClipDescription(o: ClipDescription!)
```

Create a copy of a ClipDescription.

### ClipDescription

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ClipDescription(
    label: CharSequence!, 
    mimeTypes: Array<String!>!)
```

Create a new clip.

| Parameters ||
|---|---|
| `label` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: Label to show to the user describing this clip. |
| `mimeTypes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: An array of MIME types this data is available as. |

## Public methods

### compareMimeTypes

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun compareMimeTypes(
    concreteType: String!, 
    desiredType: String!
): Boolean
```

Helper to compare two MIME types, where one may be a pattern.

| Parameters ||
|---|---|
| `concreteType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A fully-specified MIME type. |
| `desiredType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A desired MIME type that may be a pattern such as \*/\*. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the two MIME types match. |

### describeContents

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### filterMimeTypes

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun filterMimeTypes(mimeType: String!): Array<String!>!
```

Filter the clip description MIME types by the given MIME type. Returns all MIME types in the clip that match the given MIME type.

| Parameters ||
|---|---|
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The desired MIME type. May be a pattern. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | Returns an array of all matching MIME types. If there are no matching MIME types, null is returned. |

### getClassificationStatus

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getClassificationStatus(): Int
```

Returns `https://developer.android.com/reference/kotlin/android/content/ClipDescription#CLASSIFICATION_COMPLETE:kotlin.Int` if text classification has been performed on the associated `https://developer.android.com/reference/kotlin/android/content/ClipData`. If this is the case then `https://developer.android.com/reference/kotlin/android/content/ClipDescription#getConfidenceScore(kotlin.String)` may be used to retrieve information about entities within the text. Otherwise, returns `https://developer.android.com/reference/kotlin/android/content/ClipDescription#CLASSIFICATION_NOT_COMPLETE:kotlin.Int` if classification has not yet returned results, or `https://developer.android.com/reference/kotlin/android/content/ClipDescription#CLASSIFICATION_NOT_PERFORMED:kotlin.Int` if classification was not attempted (e.g. because the text was too long).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/ClipDescription#CLASSIFICATION_NOT_COMPLETE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ClipDescription#CLASSIFICATION_NOT_PERFORMED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ClipDescription#CLASSIFICATION_COMPLETE:kotlin.Int` |

### getConfidenceScore

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getConfidenceScore(entity: String): Float
```

Returns a score indicating confidence that an instance of the given entity is present in the first item of the clip data, if that item is plain text and text classification has been performed. The value ranges from 0 (low confidence) to 1 (high confidence). 0 indicates that the entity was not found in the classified text.

Entities should be as defined in the `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier.html#` class, such as `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier.html#TYPE_ADDRESS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier.html#TYPE_URL:kotlin.String`, or `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier.html#TYPE_EMAIL:kotlin.String`.

If the result is positive for any entity, the full classification result as a `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks.html#` object may be obtained using the `https://developer.android.com/reference/kotlin/android/content/ClipData.Item#getTextLinks()` method.

| Parameters ||
|---|---|
| `entity` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier.html#TYPE_UNKNOWN:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier.html#TYPE_OTHER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier.html#TYPE_EMAIL:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier.html#TYPE_PHONE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier.html#TYPE_ADDRESS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier.html#TYPE_URL:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier.html#TYPE_DATE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier.html#TYPE_DATE_TIME:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier.html#TYPE_FLIGHT_NUMBER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier.html#TYPE_OTP:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier.html#TYPE_SMS_RETRIEVER_OTP:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier.html#TYPE_SMS_WEB_OTP:kotlin.String` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Value is between 0.0f and 1.0f inclusive |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if `https://developer.android.com/reference/kotlin/android/content/ClipDescription#getClassificationStatus()` is not `https://developer.android.com/reference/kotlin/android/content/ClipDescription#CLASSIFICATION_COMPLETE:kotlin.Int` |

### getExtras

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getExtras(): PersistableBundle!
```

Retrieve extended data from the clip description.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#!` | the bundle containing extended data previously set with `https://developer.android.com/reference/kotlin/android/content/ClipDescription#setExtras(android.os.PersistableBundle)`, or null if no extras have been set. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/ClipDescription#setExtras(android.os.PersistableBundle)`

### getLabel

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLabel(): CharSequence!
```

Return the label for this clip.

### getMimeType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMimeType(index: Int): String!
```

Return one of the possible clip MIME types.

### getMimeTypeCount

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMimeTypeCount(): Int
```

Return the number of MIME types the clip is available in.

### getSourceDeviceName

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSourceDeviceName(): String?
```

Returns the name of the source device where the clip originated from.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

### getTimestamp

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTimestamp(): Long
```

Return the timestamp at which the associated `https://developer.android.com/reference/kotlin/android/content/ClipData` is copied to global clipboard in the `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()` time base.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | timestamp at which the associated `https://developer.android.com/reference/kotlin/android/content/ClipData` is copied to global clipboard or `0` if it is not copied to clipboard. |

### hasMimeType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasMimeType(mimeType: String!): Boolean
```

Check whether the clip description contains the given MIME type.

| Parameters ||
|---|---|
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The desired MIME type. May be a pattern. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if one of the MIME types in the clip description matches the desired MIME type, else false. |

### isExcludedFromRemoteClipboard

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isExcludedFromRemoteClipboard(): Boolean
```

Returns true if this ClipData should be excluded from remote clipboard syncing.

### isRemoteClipboard

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isRemoteClipboard(): Boolean
```

Returns true if this ClipData was set by a remote clipboard.

### isStyledText

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isStyledText(): Boolean
```

Returns true if the first item of the associated `https://developer.android.com/reference/kotlin/android/content/ClipData` contains styled text, i.e. if it contains spans such as `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle.html#`, `https://developer.android.com/reference/kotlin/android/text/style/ParagraphStyle.html#`, or `https://developer.android.com/reference/kotlin/android/text/style/UpdateAppearance.html#`. Returns false if it does not, or if there is no associated clip data.

### setExcludedFromRemoteClipboard

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setExcludedFromRemoteClipboard(excludeFromRemoteClipboard: Boolean): Unit
```

Sets whether this ClipData should be excluded from remote clipboard syncing.

### setExtras

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setExtras(extras: PersistableBundle!): Unit
```

Add extended data to the clip description.
**See Also**

- `https://developer.android.com/reference/kotlin/android/content/ClipDescription#getExtras()`

### toString

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
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

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<ClipDescription!>
```

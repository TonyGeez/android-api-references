Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentInfo

Kotlin | [Java](https://developer.android.com/reference/android/view/ContentInfo "View this page in Java")
| --- | --- |

```
class ContentInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.ContentInfo](https://developer.android.com/reference/kotlin/android/view/ContentInfo#) |

Holds all the relevant data for a request to `https://developer.android.com/reference/kotlin/android/view/View#performReceiveContent(android.view.ContentInfo)`.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/view/ContentInfo.Builder` Builder for `https://developer.android.com/reference/kotlin/android/view/ContentInfo#`. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ContentInfo#FLAG_CONVERT_TO_PLAIN_TEXT:kotlin.Int` Flag requesting that the content should be converted to plain text prior to inserting. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ContentInfo#SOURCE_APP:kotlin.Int` Specifies that the operation was triggered by the app that contains the target view. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ContentInfo#SOURCE_AUTOFILL:kotlin.Int` Specifies that the operation was triggered by the autofill framework. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ContentInfo#SOURCE_CLIPBOARD:kotlin.Int` Specifies that the operation was triggered by a paste from the clipboard (e.g. "Paste" or "Paste as plain text" action in the insertion/selection menu). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ContentInfo#SOURCE_DRAG_AND_DROP:kotlin.Int` Specifies that the operation was triggered by the drag/drop framework. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ContentInfo#SOURCE_INPUT_METHOD:kotlin.Int` Specifies that the operation was triggered from the soft keyboard (also known as input method editor or IME). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ContentInfo#SOURCE_PROCESS_TEXT:kotlin.Int` Specifies that the operation was triggered by a result from a `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PROCESS_TEXT:kotlin.String` action in the selection menu. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ContentInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [ClipData](https://developer.android.com/reference/kotlin/android/content/ClipData.html#) | `https://developer.android.com/reference/kotlin/android/view/ContentInfo#getClip()()` The data to be inserted. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | `https://developer.android.com/reference/kotlin/android/view/ContentInfo#getExtras()()` Optional additional metadata. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ContentInfo#getFlags()()` Optional flags that control the insertion behavior. |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | `https://developer.android.com/reference/kotlin/android/view/ContentInfo#getLinkUri()()` Optional http/https URI for the content that may be provided by the IME. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/ContentInfo#getSource()()` The source of the operation. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/ContentInfo#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ContentInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Writes this object into the given parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ContentInfo](https://developer.android.com/reference/kotlin/android/view/ContentInfo#)!\> | `https://developer.android.com/reference/kotlin/android/view/ContentInfo#CREATOR:android.os.Parcelable.Creator` Creates `https://developer.android.com/reference/kotlin/android/view/ContentInfo#` instances from parcels. |

## Constants

### FLAG_CONVERT_TO_PLAIN_TEXT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_CONVERT_TO_PLAIN_TEXT: Int
```

Flag requesting that the content should be converted to plain text prior to inserting.

 Value: 1

### SOURCE_APP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SOURCE_APP: Int
```

Specifies that the operation was triggered by the app that contains the target view.

 Value: 0

### SOURCE_AUTOFILL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SOURCE_AUTOFILL: Int
```

Specifies that the operation was triggered by the autofill framework. See https://developer.android.com/guide/topics/text/autofill for more info.

 Value: 4

### SOURCE_CLIPBOARD

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SOURCE_CLIPBOARD: Int
```

Specifies that the operation was triggered by a paste from the clipboard (e.g. "Paste" or "Paste as plain text" action in the insertion/selection menu).

 Value: 1

### SOURCE_DRAG_AND_DROP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SOURCE_DRAG_AND_DROP: Int
```

Specifies that the operation was triggered by the drag/drop framework. See https://developer.android.com/guide/topics/ui/drag-drop for more info.

 Value: 3

### SOURCE_INPUT_METHOD

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SOURCE_INPUT_METHOD: Int
```

Specifies that the operation was triggered from the soft keyboard (also known as input method editor or IME). See https://developer.android.com/guide/topics/text/image-keyboard for more info.

 Value: 2

### SOURCE_PROCESS_TEXT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SOURCE_PROCESS_TEXT: Int
```

Specifies that the operation was triggered by a result from a `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PROCESS_TEXT:kotlin.String` action in the selection menu.

 Value: 5

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getClip

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getClip(): ClipData
```

The data to be inserted.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` | This value cannot be `null`. |

### getExtras

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExtras(): Bundle?
```

Optional additional metadata. If the source is `https://developer.android.com/reference/kotlin/android/view/ContentInfo#SOURCE_INPUT_METHOD:kotlin.Int`, this will include the `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#commitContent(android.view.inputmethod.InputContentInfo,%20kotlin.Int,%20android.os.Bundle)` passed by the IME.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#?` | This value may be `null`. |

### getFlags

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFlags(): Int
```

Optional flags that control the insertion behavior. See `FLAG_` constants.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or - `https://developer.android.com/reference/kotlin/android/view/ContentInfo#FLAG_CONVERT_TO_PLAIN_TEXT:kotlin.Int` |

### getLinkUri

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLinkUri(): Uri?
```

Optional http/https URI for the content that may be provided by the IME. This is only populated if the source is `https://developer.android.com/reference/kotlin/android/view/ContentInfo#SOURCE_INPUT_METHOD:kotlin.Int` and if a non-empty `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputContentInfo#getLinkUri()` was passed by the IME.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | This value may be `null`. |

### getSource

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSource(): Int
```

The source of the operation. See `SOURCE_` constants. Future versions of Android may pass additional values.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/ContentInfo#SOURCE_APP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/ContentInfo#SOURCE_CLIPBOARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/ContentInfo#SOURCE_INPUT_METHOD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/ContentInfo#SOURCE_DRAG_AND_DROP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/ContentInfo#SOURCE_AUTOFILL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/ContentInfo#SOURCE_PROCESS_TEXT:kotlin.Int` |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Writes this object into the given parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The parcel to write into. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The flags to use for parceling. |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<ContentInfo!>
```

Creates `https://developer.android.com/reference/kotlin/android/view/ContentInfo#` instances from parcels.

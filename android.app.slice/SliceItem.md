# SliceItem

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SliceItem

Kotlin| [Java](https://developer.android.com/reference/android/app/slice/SliceItem "View this page in Java") 
| --- | --- |

```
class SliceItem : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.slice.SliceItem](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#) |

| **This class was deprecated in API level 35.**
|
| Slice framework has been deprecated, it will not receive any updates from android.os.Build.VANILLA_ICE_CREAM and forward. If you are looking for a framework that sends displayable data from one app to another, consider using [android.app.appsearch.AppSearchManager](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchManager.html#).

A SliceItem is a single unit in the tree structure of a [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice). A SliceItem a piece of content and some hints about what that content means or how it should be displayed. The types of content can be:
- [FORMAT_SLICE](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_SLICE:kotlin.String)
- [FORMAT_TEXT](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_TEXT:kotlin.String)
- [FORMAT_IMAGE](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_IMAGE:kotlin.String)
- [FORMAT_ACTION](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_ACTION:kotlin.String)
- [FORMAT_INT](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_INT:kotlin.String)
- [FORMAT_LONG](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_LONG:kotlin.String)
- [FORMAT_REMOTE_INPUT](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_REMOTE_INPUT:kotlin.String)
- [FORMAT_BUNDLE](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_BUNDLE:kotlin.String)
The hints that a [SliceItem](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#) are a set of strings which annotate the content. The hints that are guaranteed to be understood by the system are defined on [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FORMAT_ACTION](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_ACTION:kotlin.String) A [SliceItem](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#) that contains a [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) Note: Actions contain 2 pieces of data, In addition to the pending intent, the item contains a [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice) that the action applies to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FORMAT_BUNDLE](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_BUNDLE:kotlin.String) A [SliceItem](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#) that contains a [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FORMAT_IMAGE](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_IMAGE:kotlin.String) A [SliceItem](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#) that contains an [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#) |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FORMAT_INT](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_INT:kotlin.String) A [SliceItem](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#) that contains an int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FORMAT_LONG](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_LONG:kotlin.String) A [SliceItem](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#) that contains a long. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FORMAT_REMOTE_INPUT](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_REMOTE_INPUT:kotlin.String) A [SliceItem](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#) that contains a [RemoteInput](https://developer.android.com/reference/kotlin/android/app/RemoteInput.html#). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FORMAT_SLICE](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_SLICE:kotlin.String) A [SliceItem](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#) that contains a [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FORMAT_TEXT](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_TEXT:kotlin.String) A [SliceItem](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#) that contains a [CharSequence](https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#) |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#describeContents())`()` <br /> |
| [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)! | [getAction](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#getAction())`()` <br /> |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [getBundle](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#getBundle())`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFormat](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#getFormat())`()` Get the format of this SliceItem. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getHints](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#getHints())`()` Gets all hints associated with this SliceItem. |
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)! | [getIcon](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#getIcon())`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#getInt())`()` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#getLong())`()` <br /> |
| [RemoteInput](https://developer.android.com/reference/kotlin/android/app/RemoteInput.html#)! | [getRemoteInput](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#getRemoteInput())`()` <br /> |
| --- | --- |
| [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice)! | [getSlice](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#getSlice())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSubType](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#getSubType())`()` Get the sub-type of this SliceItem. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getText](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#getText())`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasHint](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#hasHint(kotlin.String))`(`hint:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [SliceItem](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### FORMAT_ACTION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_ACTION: String
```

**Deprecated:** *Deprecated in Java.*

A [SliceItem](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#) that contains a [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) Note: Actions contain 2 pieces of data, In addition to the pending intent, the item contains a [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice) that the action applies to. 

 Value: "action"

### FORMAT_BUNDLE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_BUNDLE: String
```

**Deprecated:** *Deprecated in Java.*

A [SliceItem](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#) that contains a [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#). 

 Value: "bundle"

### FORMAT_IMAGE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_IMAGE: String
```

**Deprecated:** *Deprecated in Java.*

A [SliceItem](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#) that contains an [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#) 

 Value: "image"

### FORMAT_INT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_INT: String
```

**Deprecated:** *Deprecated in Java.*

A [SliceItem](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#) that contains an int. 

 Value: "int"

### FORMAT_LONG

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_LONG: String
```

**Deprecated:** *Deprecated in Java.*

A [SliceItem](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#) that contains a long. 

 Value: "long"

### FORMAT_REMOTE_INPUT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_REMOTE_INPUT: String
```

**Deprecated:** *Deprecated in Java.*

A [SliceItem](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#) that contains a [RemoteInput](https://developer.android.com/reference/kotlin/android/app/RemoteInput.html#). 

 Value: "input"

### FORMAT_SLICE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_SLICE: String
```

**Deprecated:** *Deprecated in Java.*

A [SliceItem](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#) that contains a [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice) 

 Value: "slice"

### FORMAT_TEXT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_TEXT: String
```

**Deprecated:** *Deprecated in Java.*

A [SliceItem](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#) that contains a [CharSequence](https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#) 

 Value: "text"

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getAction

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAction(): PendingIntent!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)! | The pending intent held by this [FORMAT_ACTION](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_ACTION:kotlin.String) SliceItem |

### getBundle

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBundle(): Bundle!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | The parcelable held by this [FORMAT_BUNDLE](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_BUNDLE:kotlin.String) SliceItem |

### getFormat

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFormat(): String!
```

**Deprecated:** *Deprecated in Java.*

Get the format of this SliceItem.

The format will be one of the following types supported by the platform:
- [FORMAT_SLICE](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_SLICE:kotlin.String)
- [FORMAT_TEXT](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_TEXT:kotlin.String)
- [FORMAT_IMAGE](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_IMAGE:kotlin.String)
- [FORMAT_ACTION](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_ACTION:kotlin.String)
- [FORMAT_INT](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_INT:kotlin.String)
- [FORMAT_LONG](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_LONG:kotlin.String)
- [FORMAT_REMOTE_INPUT](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_REMOTE_INPUT:kotlin.String)
- [FORMAT_BUNDLE](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_BUNDLE:kotlin.String) 
**See Also**

- <https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#getSubType()>

### getHints

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHints(): MutableList<String!>
```

**Deprecated:** *Deprecated in Java.*

Gets all hints associated with this SliceItem.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | Array of hints. This value cannot be`null`. Value is [android.app.slice.Slice#HINT_TITLE](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_TITLE:kotlin.String), [android.app.slice.Slice#HINT_LIST](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_LIST:kotlin.String), [android.app.slice.Slice#HINT_LIST_ITEM](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_LIST_ITEM:kotlin.String), [android.app.slice.Slice#HINT_LARGE](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_LARGE:kotlin.String), [android.app.slice.Slice#HINT_ACTIONS](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_ACTIONS:kotlin.String), [android.app.slice.Slice#HINT_SELECTED](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_SELECTED:kotlin.String), [android.app.slice.Slice#HINT_NO_TINT](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_NO_TINT:kotlin.String), [android.app.slice.Slice#HINT_SHORTCUT](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_SHORTCUT:kotlin.String), android.app.slice.Slice.HINT_TOGGLE, [android.app.slice.Slice#HINT_HORIZONTAL](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_HORIZONTAL:kotlin.String), [android.app.slice.Slice#HINT_PARTIAL](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_PARTIAL:kotlin.String), [android.app.slice.Slice#HINT_SEE_MORE](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_SEE_MORE:kotlin.String), [android.app.slice.Slice#HINT_KEYWORDS](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_KEYWORDS:kotlin.String), [android.app.slice.Slice#HINT_ERROR](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_ERROR:kotlin.String), [android.app.slice.Slice#HINT_TTL](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_TTL:kotlin.String), [android.app.slice.Slice#HINT_LAST_UPDATED](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_LAST_UPDATED:kotlin.String), or [android.app.slice.Slice#HINT_PERMISSION_REQUEST](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_PERMISSION_REQUEST:kotlin.String) |

### getIcon

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIcon(): Icon!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)! | The icon held by this [FORMAT_IMAGE](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_IMAGE:kotlin.String) SliceItem |

### getInt

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInt(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The color held by this [FORMAT_INT](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_INT:kotlin.String) SliceItem |

### getLong

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLong(): Long
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The long held by this [FORMAT_LONG](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_LONG:kotlin.String) SliceItem |

### getRemoteInput

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRemoteInput(): RemoteInput!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RemoteInput](https://developer.android.com/reference/kotlin/android/app/RemoteInput.html#)! | The remote input held by this [FORMAT_REMOTE_INPUT](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_REMOTE_INPUT:kotlin.String) SliceItem |

### getSlice

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSlice(): Slice!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice)! | The slice held by this [FORMAT_ACTION](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_ACTION:kotlin.String) or [FORMAT_SLICE](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_SLICE:kotlin.String) SliceItem |

### getSubType

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSubType(): String!
```

**Deprecated:** *Deprecated in Java.*

Get the sub-type of this SliceItem.

Subtypes provide additional information about the type of this information beyond basic interpretations inferred by [getFormat()](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#getFormat()). For example a slice may contain many [FORMAT_TEXT](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_TEXT:kotlin.String) items, but only some of them may be [Slice.SUBTYPE_MESSAGE](https://developer.android.com/reference/kotlin/android/app/slice/Slice#SUBTYPE_MESSAGE:kotlin.String). 
**See Also**

- <https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#getFormat()> 

### getText

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getText(): CharSequence!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | The text held by this [FORMAT_TEXT](https://developer.android.com/reference/kotlin/android/app/slice/SliceItem#FORMAT_TEXT:kotlin.String) SliceItem |

### hasHint

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasHint(hint: String!): Boolean
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `hint` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The hint to check for Value is [android.app.slice.Slice#HINT_TITLE](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_TITLE:kotlin.String), [android.app.slice.Slice#HINT_LIST](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_LIST:kotlin.String), [android.app.slice.Slice#HINT_LIST_ITEM](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_LIST_ITEM:kotlin.String), [android.app.slice.Slice#HINT_LARGE](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_LARGE:kotlin.String), [android.app.slice.Slice#HINT_ACTIONS](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_ACTIONS:kotlin.String), [android.app.slice.Slice#HINT_SELECTED](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_SELECTED:kotlin.String), [android.app.slice.Slice#HINT_NO_TINT](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_NO_TINT:kotlin.String), [android.app.slice.Slice#HINT_SHORTCUT](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_SHORTCUT:kotlin.String), android.app.slice.Slice.HINT_TOGGLE, [android.app.slice.Slice#HINT_HORIZONTAL](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_HORIZONTAL:kotlin.String), [android.app.slice.Slice#HINT_PARTIAL](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_PARTIAL:kotlin.String), [android.app.slice.Slice#HINT_SEE_MORE](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_SEE_MORE:kotlin.String), [android.app.slice.Slice#HINT_KEYWORDS](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_KEYWORDS:kotlin.String), [android.app.slice.Slice#HINT_ERROR](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_ERROR:kotlin.String), [android.app.slice.Slice#HINT_TTL](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_TTL:kotlin.String), [android.app.slice.Slice#HINT_LAST_UPDATED](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_LAST_UPDATED:kotlin.String), or [android.app.slice.Slice#HINT_PERMISSION_REQUEST](https://developer.android.com/reference/kotlin/android/app/slice/Slice#HINT_PERMISSION_REQUEST:kotlin.String) |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this item contains the given hint |

### writeToParcel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SliceItem!>
```

**Deprecated:** *Deprecated in Java.*

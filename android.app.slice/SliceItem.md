# SliceItem

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SliceItem

Kotlin| [Java](SliceItem.md) 
| --- | --- |

```
class SliceItem : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.slice.SliceItem](SliceItem.md) |

| **This class was deprecated in API level 35.**
|
| Slice framework has been deprecated, it will not receive any updates from android.os.Build.VANILLA_ICE_CREAM and forward. If you are looking for a framework that sends displayable data from one app to another, consider using [android.app.appsearch.AppSearchManager](../android.app.appsearch/AppSearchManager.md).

A SliceItem is a single unit in the tree structure of a [Slice](Slice.md). A SliceItem a piece of content and some hints about what that content means or how it should be displayed. The types of content can be:
- [FORMAT_SLICE](SliceItem.md)
- [FORMAT_TEXT](SliceItem.md)
- [FORMAT_IMAGE](SliceItem.md)
- [FORMAT_ACTION](SliceItem.md)
- [FORMAT_INT](SliceItem.md)
- [FORMAT_LONG](SliceItem.md)
- [FORMAT_REMOTE_INPUT](SliceItem.md)
- [FORMAT_BUNDLE](SliceItem.md)
The hints that a [SliceItem](SliceItem.md) are a set of strings which annotate the content. The hints that are guaranteed to be understood by the system are defined on [Slice](Slice.md).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FORMAT_ACTION](SliceItem.md) A [SliceItem](SliceItem.md) that contains a [PendingIntent](../android.app/PendingIntent.md) Note: Actions contain 2 pieces of data, In addition to the pending intent, the item contains a [Slice](Slice.md) that the action applies to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FORMAT_BUNDLE](SliceItem.md) A [SliceItem](SliceItem.md) that contains a [Bundle](../android.os/Bundle.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FORMAT_IMAGE](SliceItem.md) A [SliceItem](SliceItem.md) that contains an [Icon](../android.graphics.drawable/Icon.md) |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FORMAT_INT](SliceItem.md) A [SliceItem](SliceItem.md) that contains an int. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FORMAT_LONG](SliceItem.md) A [SliceItem](SliceItem.md) that contains a long. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FORMAT_REMOTE_INPUT](SliceItem.md) A [SliceItem](SliceItem.md) that contains a [RemoteInput](../android.app/RemoteInput.md). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FORMAT_SLICE](SliceItem.md) A [SliceItem](SliceItem.md) that contains a [Slice](Slice.md) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FORMAT_TEXT](SliceItem.md) A [SliceItem](SliceItem.md) that contains a [CharSequence](../java.lang/CharSequence.md) |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](SliceItem.md))`()` <br /> |
| [PendingIntent](../android.app/PendingIntent.md)! | [getAction](SliceItem.md))`()` <br /> |
| [Bundle](../android.os/Bundle.md)! | [getBundle](SliceItem.md))`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFormat](SliceItem.md))`()` Get the format of this SliceItem. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getHints](SliceItem.md))`()` Gets all hints associated with this SliceItem. |
| [Icon](../android.graphics.drawable/Icon.md)! | [getIcon](SliceItem.md))`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](SliceItem.md))`()` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](SliceItem.md))`()` <br /> |
| [RemoteInput](../android.app/RemoteInput.md)! | [getRemoteInput](SliceItem.md))`()` <br /> |
| --- | --- |
| [Slice](Slice.md)! | [getSlice](SliceItem.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSubType](SliceItem.md))`()` Get the sub-type of this SliceItem. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getText](SliceItem.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasHint](SliceItem.md))`(`hint:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](SliceItem.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SliceItem](SliceItem.md)!\> | [CREATOR](SliceItem.md) <br /> |

## Constants

### FORMAT_ACTION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_ACTION: String
```

**Deprecated:** *Deprecated in Java.*

A [SliceItem](SliceItem.md) that contains a [PendingIntent](../android.app/PendingIntent.md) Note: Actions contain 2 pieces of data, In addition to the pending intent, the item contains a [Slice](Slice.md) that the action applies to. 

 Value: "action"

### FORMAT_BUNDLE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_BUNDLE: String
```

**Deprecated:** *Deprecated in Java.*

A [SliceItem](SliceItem.md) that contains a [Bundle](../android.os/Bundle.md). 

 Value: "bundle"

### FORMAT_IMAGE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_IMAGE: String
```

**Deprecated:** *Deprecated in Java.*

A [SliceItem](SliceItem.md) that contains an [Icon](../android.graphics.drawable/Icon.md) 

 Value: "image"

### FORMAT_INT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_INT: String
```

**Deprecated:** *Deprecated in Java.*

A [SliceItem](SliceItem.md) that contains an int. 

 Value: "int"

### FORMAT_LONG

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_LONG: String
```

**Deprecated:** *Deprecated in Java.*

A [SliceItem](SliceItem.md) that contains a long. 

 Value: "long"

### FORMAT_REMOTE_INPUT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_REMOTE_INPUT: String
```

**Deprecated:** *Deprecated in Java.*

A [SliceItem](SliceItem.md) that contains a [RemoteInput](../android.app/RemoteInput.md). 

 Value: "input"

### FORMAT_SLICE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_SLICE: String
```

**Deprecated:** *Deprecated in Java.*

A [SliceItem](SliceItem.md) that contains a [Slice](Slice.md) 

 Value: "slice"

### FORMAT_TEXT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_TEXT: String
```

**Deprecated:** *Deprecated in Java.*

A [SliceItem](SliceItem.md) that contains a [CharSequence](../java.lang/CharSequence.md) 

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getAction

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAction(): PendingIntent!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PendingIntent](../android.app/PendingIntent.md)! | The pending intent held by this [FORMAT_ACTION](SliceItem.md) SliceItem |

### getBundle

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBundle(): Bundle!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](../android.os/Bundle.md)! | The parcelable held by this [FORMAT_BUNDLE](SliceItem.md) SliceItem |

### getFormat

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFormat(): String!
```

**Deprecated:** *Deprecated in Java.*

Get the format of this SliceItem.

The format will be one of the following types supported by the platform:
- [FORMAT_SLICE](SliceItem.md)
- [FORMAT_TEXT](SliceItem.md)
- [FORMAT_IMAGE](SliceItem.md)
- [FORMAT_ACTION](SliceItem.md)
- [FORMAT_INT](SliceItem.md)
- [FORMAT_LONG](SliceItem.md)
- [FORMAT_REMOTE_INPUT](SliceItem.md)
- [FORMAT_BUNDLE](SliceItem.md) 
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
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | Array of hints. This value cannot be`null`. Value is [android.app.slice.Slice#HINT_TITLE](Slice.md), [android.app.slice.Slice#HINT_LIST](Slice.md), [android.app.slice.Slice#HINT_LIST_ITEM](Slice.md), [android.app.slice.Slice#HINT_LARGE](Slice.md), [android.app.slice.Slice#HINT_ACTIONS](Slice.md), [android.app.slice.Slice#HINT_SELECTED](Slice.md), [android.app.slice.Slice#HINT_NO_TINT](Slice.md), [android.app.slice.Slice#HINT_SHORTCUT](Slice.md), android.app.slice.Slice.HINT_TOGGLE, [android.app.slice.Slice#HINT_HORIZONTAL](Slice.md), [android.app.slice.Slice#HINT_PARTIAL](Slice.md), [android.app.slice.Slice#HINT_SEE_MORE](Slice.md), [android.app.slice.Slice#HINT_KEYWORDS](Slice.md), [android.app.slice.Slice#HINT_ERROR](Slice.md), [android.app.slice.Slice#HINT_TTL](Slice.md), [android.app.slice.Slice#HINT_LAST_UPDATED](Slice.md), or [android.app.slice.Slice#HINT_PERMISSION_REQUEST](Slice.md) |

### getIcon

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIcon(): Icon!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Icon](../android.graphics.drawable/Icon.md)! | The icon held by this [FORMAT_IMAGE](SliceItem.md) SliceItem |

### getInt

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInt(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The color held by this [FORMAT_INT](SliceItem.md) SliceItem |

### getLong

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLong(): Long
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The long held by this [FORMAT_LONG](SliceItem.md) SliceItem |

### getRemoteInput

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRemoteInput(): RemoteInput!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RemoteInput](../android.app/RemoteInput.md)! | The remote input held by this [FORMAT_REMOTE_INPUT](SliceItem.md) SliceItem |

### getSlice

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSlice(): Slice!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Slice](Slice.md)! | The slice held by this [FORMAT_ACTION](SliceItem.md) or [FORMAT_SLICE](SliceItem.md) SliceItem |

### getSubType

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSubType(): String!
```

**Deprecated:** *Deprecated in Java.*

Get the sub-type of this SliceItem.

Subtypes provide additional information about the type of this information beyond basic interpretations inferred by [getFormat()](SliceItem.md)). For example a slice may contain many [FORMAT_TEXT](SliceItem.md) items, but only some of them may be [Slice.SUBTYPE_MESSAGE](Slice.md). 
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
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | The text held by this [FORMAT_TEXT](SliceItem.md) SliceItem |

### hasHint

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasHint(hint: String!): Boolean
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `hint` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The hint to check for Value is [android.app.slice.Slice#HINT_TITLE](Slice.md), [android.app.slice.Slice#HINT_LIST](Slice.md), [android.app.slice.Slice#HINT_LIST_ITEM](Slice.md), [android.app.slice.Slice#HINT_LARGE](Slice.md), [android.app.slice.Slice#HINT_ACTIONS](Slice.md), [android.app.slice.Slice#HINT_SELECTED](Slice.md), [android.app.slice.Slice#HINT_NO_TINT](Slice.md), [android.app.slice.Slice#HINT_SHORTCUT](Slice.md), android.app.slice.Slice.HINT_TOGGLE, [android.app.slice.Slice#HINT_HORIZONTAL](Slice.md), [android.app.slice.Slice#HINT_PARTIAL](Slice.md), [android.app.slice.Slice#HINT_SEE_MORE](Slice.md), [android.app.slice.Slice#HINT_KEYWORDS](Slice.md), [android.app.slice.Slice#HINT_ERROR](Slice.md), [android.app.slice.Slice#HINT_TTL](Slice.md), [android.app.slice.Slice#HINT_LAST_UPDATED](Slice.md), or [android.app.slice.Slice#HINT_PERMISSION_REQUEST](Slice.md) |

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
| `dest` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SliceItem!>
```

**Deprecated:** *Deprecated in Java.*

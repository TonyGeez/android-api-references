Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CompletionInfo

```
class CompletionInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inputmethod.CompletionInfo](CompletionInfo.md) |

Information about a single text completion that an editor has reported to an input method.

This class encapsulates a completion offered by an application that wants it to be presented to the user by the IME. Usually, apps present their completions directly in a scrolling list for example (UI developers will usually use or extend `https://developer.android.com/reference/kotlin/android/widget/AutoCompleteTextView.html#` to implement this). However, in some cases, the editor may not be visible, as in the case in extract mode where the IME has taken over the full screen. In this case, the editor can choose to send their completions to the IME for display.

Most applications who want to send completions to an IME should use `https://developer.android.com/reference/kotlin/android/widget/AutoCompleteTextView.html#` as this class makes this process easy. In this case, the application would not have to deal directly with this class.

An application who implements its own editor and wants direct control over this would create an array of CompletionInfo objects, and send it to the IME using displayCompletions. The IME would present the completions however they see fit, and call back to the editor through commitCompletion. The application can then pick up the commit event by overriding onCommitCompletion.

## Summary

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| CompletionInfo Create a simple completion with just text, no label. |
| CompletionInfo Create a full completion with both text and label. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getId Return the abstract identifier for this completion, typically corresponding to the id associated with it in the original adapter. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | getLabel Return the user-visible label for the completion, or null if the plain text should be shown. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPosition Return the original position of this completion, typically corresponding to its position in the original adapter. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | getText Return the actual text associated with this completion. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Used to package this object into a `https://developer.android.com/reference/kotlin/android/os/Parcel.html#`. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [CompletionInfo](CompletionInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CompletionInfo#CREATOR:android.os.Parcelable.Creator` Used to make this class parcelable. |

## Public constructors

### CompletionInfo

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CompletionInfo(
    id: Long, 
    index: Int, 
    text: CharSequence!)
```

Create a simple completion with just text, no label.

| Parameters ||
|---|---|
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): An id that get passed as is (to the editor's discretion) |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An index that get passed as is. Typically this is the index in the list of completions inside the editor. |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The text that should be inserted into the editor when this completion is chosen. |
| --- | --- |

### CompletionInfo

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CompletionInfo(
    id: Long, 
    index: Int, 
    text: CharSequence!, 
    label: CharSequence!)
```

Create a full completion with both text and label. The text is what will get inserted into the editor, while the label is what the IME should display. If they are the same, use the version of the constructor without a \`label' argument.

| Parameters ||
|---|---|
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): An id that get passed as is (to the editor's discretion) |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An index that get passed as is. Typically this is the index in the list of completions inside the editor. |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The text that should be inserted into the editor when this completion is chosen. |
| --- | --- |
| `label` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The text that the IME should be showing among the completions list. |

## Public methods

### describeContents

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getId

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getId(): Long
```

Return the abstract identifier for this completion, typically corresponding to the id associated with it in the original adapter.

### getLabel

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLabel(): CharSequence!
```

Return the user-visible label for the completion, or null if the plain text should be shown. If non-null, this will be what the user sees as the completion option instead of the actual text.

### getPosition

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPosition(): Int
```

Return the original position of this completion, typically corresponding to its position in the original adapter.

### getText

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getText(): CharSequence!
```

Return the actual text associated with this completion. This is the real text that will be inserted into the editor if the user selects it.

### toString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Used to package this object into a `https://developer.android.com/reference/kotlin/android/os/Parcel.html#`.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The `https://developer.android.com/reference/kotlin/android/os/Parcel.html#` to be written. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<CompletionInfo!>
```

Used to make this class parcelable.

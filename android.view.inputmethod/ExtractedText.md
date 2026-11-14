# ExtractedText

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExtractedText

Kotlin| [Java](../android/view/inputmethod/ExtractedText.md) 
| --- | --- |

```
open class ExtractedText : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inputmethod.ExtractedText](../android/view/inputmethod/ExtractedText.md) |

Information about text that has been extracted for use by an input method. This contains information about a portion of the currently edited text, that the IME should display into its own interface while in extracted mode.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_SELECTING](../android/view/inputmethod/ExtractedText.md) Bit for [flags](../android/view/inputmethod/ExtractedText.md): set if the editor is currently in selection mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_SINGLE_LINE](../android/view/inputmethod/ExtractedText.md) Bit for [flags](../android/view/inputmethod/ExtractedText.md): set if the text being edited can only be on a single line. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------|---|
| [ExtractedText](../android/view/inputmethod/ExtractedText.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/view/inputmethod/ExtractedText.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/view/inputmethod/ExtractedText.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used to package this object into a [Parcel](../android/os/Parcel.md). |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ExtractedText](../android/view/inputmethod/ExtractedText.md)!\> | [CREATOR](../android/view/inputmethod/ExtractedText.md) Used to make this class parcelable. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [flags](../android/view/inputmethod/ExtractedText.md) Additional bit flags of information about the edited text. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [hint](../android/view/inputmethod/ExtractedText.md) The hint that has been extracted. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [partialEndOffset](../android/view/inputmethod/ExtractedText.md) If the content is a report of a partial text change, this is the offset where the change ends. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [partialStartOffset](../android/view/inputmethod/ExtractedText.md) If the content is a report of a partial text change, this is the offset where the change starts and it runs until [partialEndOffset](../android/view/inputmethod/ExtractedText.md). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [selectionEnd](../android/view/inputmethod/ExtractedText.md) The offset where the selection currently ends within the extracted text. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [selectionStart](../android/view/inputmethod/ExtractedText.md) The offset where the selection currently starts within the extracted text. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [startOffset](../android/view/inputmethod/ExtractedText.md) The offset in the overall text at which the extracted text starts. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [text](../android/view/inputmethod/ExtractedText.md) The text that has been extracted. |
| --- | --- |

## Constants

### FLAG_SELECTING

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_SELECTING: Int
```

Bit for [flags](../android/view/inputmethod/ExtractedText.md): set if the editor is currently in selection mode. This happens when a hardware keyboard with latched keys is attached and the shift key is currently latched. 

 Value: 2

### FLAG_SINGLE_LINE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_SINGLE_LINE: Int
```

Bit for [flags](../android/view/inputmethod/ExtractedText.md): set if the text being edited can only be on a single line. 

 Value: 1

## Public constructors

### ExtractedText

```
ExtractedText()
```

## Public methods

### describeContents

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### writeToParcel

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
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

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ExtractedText!>
```

Used to make this class parcelable. 

### flags

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var flags: Int
```

Additional bit flags of information about the edited text. 

### hint

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var hint: CharSequence!
```

The hint that has been extracted. 
**See Also**

- [android.widget.TextView#getHint()](../android/widget/TextView.md)) 

### partialEndOffset

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var partialEndOffset: Int
```

If the content is a report of a partial text change, this is the offset where the change ends. Note that the actual text may be larger or smaller than the difference between this and [partialStartOffset](../android/view/inputmethod/ExtractedText.md), meaning a reduction or increase, respectively, in the total text. 

### partialStartOffset

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var partialStartOffset: Int
```

If the content is a report of a partial text change, this is the offset where the change starts and it runs until [partialEndOffset](../android/view/inputmethod/ExtractedText.md). If the content is the full text, this field is -1. 

### selectionEnd

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var selectionEnd: Int
```

The offset where the selection currently ends within the extracted text. The real selection end position is at startOffset+selectionEnd. 

### selectionStart

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var selectionStart: Int
```

The offset where the selection currently starts within the extracted text. The real selection start position is at startOffset+selectionStart. 

### startOffset

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var startOffset: Int
```

The offset in the overall text at which the extracted text starts. 

### text

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var text: CharSequence!
```

The text that has been extracted. 
**See Also**

- [android.widget.TextView#getText()](../android/widget/TextView.md))

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextLinks

Kotlin | [Java](TextLinks.md)
| --- | --- |

```
class TextLinks : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.textclassifier.TextLinks](TextLinks.md) |

A collection of links, representing subsequences of text and the entity types (phone number, address, url, etc) they may be.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks.Builder` A builder to construct a TextLinks instance. |
| | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks.Request` A request object for generating TextLinks. |
| | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks.TextLink` A link, identifying a substring of text and possible entity types for it. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks.TextLinkSpan` A ClickableSpan for a TextLink. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks#APPLY_STRATEGY_IGNORE:kotlin.Int` Do not replace `https://developer.android.com/reference/kotlin/android/text/style/ClickableSpan.html#`s that exist where the `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks.TextLinkSpan` needs to be applied to. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks#APPLY_STRATEGY_REPLACE:kotlin.Int` Replace any `https://developer.android.com/reference/kotlin/android/text/style/ClickableSpan.html#`s that exist where the `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks.TextLinkSpan` needs to be applied to. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks#STATUS_DIFFERENT_TEXT:kotlin.Int` The specified text does not match the text used to generate the links. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks#STATUS_LINKS_APPLIED:kotlin.Int` Links were successfully applied to the text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks#STATUS_NO_LINKS_APPLIED:kotlin.Int` No links applied to text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks#STATUS_NO_LINKS_FOUND:kotlin.Int` No links exist to apply to text. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks#STATUS_UNSUPPORTED_CHARACTER:kotlin.Int` The specified text contains unsupported characters. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | apply Annotates the given text with the generated links. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Bundle](../android.os/Bundle.md) | getExtras Returns the extended data. |
| --- | --- |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [TextLinks.TextLink](../android/view/textclassifier/TextLinks.TextLink.md)!\> | getLinks Returns an unmodifiable Collection of the links. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | getText Returns the text that was used to generate these links. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [TextLinks](TextLinks.md)!\> | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### APPLY_STRATEGY_IGNORE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APPLY_STRATEGY_IGNORE: Int
```

Do not replace `https://developer.android.com/reference/kotlin/android/text/style/ClickableSpan.html#`s that exist where the `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks.TextLinkSpan` needs to be applied to. Do not apply the TextLinkSpan.

 Value: 0

### APPLY_STRATEGY_REPLACE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APPLY_STRATEGY_REPLACE: Int
```

Replace any `https://developer.android.com/reference/kotlin/android/text/style/ClickableSpan.html#`s that exist where the `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks.TextLinkSpan` needs to be applied to.

 Value: 1

### STATUS_DIFFERENT_TEXT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_DIFFERENT_TEXT: Int
```

The specified text does not match the text used to generate the links.

 Value: 3

### STATUS_LINKS_APPLIED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_LINKS_APPLIED: Int
```

Links were successfully applied to the text.

 Value: 0

### STATUS_NO_LINKS_APPLIED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_NO_LINKS_APPLIED: Int
```

No links applied to text. The links were filtered out.

 Value: 2

### STATUS_NO_LINKS_FOUND

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_NO_LINKS_FOUND: Int
```

No links exist to apply to text. Links count is zero.

 Value: 1

### STATUS_UNSUPPORTED_CHARACTER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_UNSUPPORTED_CHARACTER: Int
```

The specified text contains unsupported characters.

 Value: 4

## Public methods

### apply

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun apply(
    text: Spannable, 
    applyStrategy: Int, 
    spanFactory: Function<TextLinks.TextLink!, TextLinks.TextLinkSpan!>?
): Int
```

Annotates the given text with the generated links. It will fail if the provided text doesn't match the original text used to create the TextLinks.

**NOTE:** It may be necessary to set a LinkMovementMethod on the TextView widget to properly handle links. See setMovementMethod

| Parameters ||
|---|---|
| `text` | [Spannable](../android.text/Spannable.md): the text to apply the links to. Must match the original text. This value cannot be `null`. |
| `applyStrategy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the apply strategy used to determine how to apply links to text. e.g `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks#APPLY_STRATEGY_IGNORE:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks#APPLY_STRATEGY_IGNORE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks#APPLY_STRATEGY_REPLACE:kotlin.Int` |
| `spanFactory` | [Function](../java.util.function/Function.md)\< [TextLinks.TextLink](../android/view/textclassifier/TextLinks.TextLink.md)!, [TextLinks.TextLinkSpan](../android/view/textclassifier/TextLinks.TextLinkSpan.md)!\>?: a custom span factory for converting TextLinks to TextLinkSpans. Set to `null` to use the default span factory. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a status code indicating whether or not the links were successfully applied e.g. `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks#STATUS_LINKS_APPLIED:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks#STATUS_LINKS_APPLIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks#STATUS_NO_LINKS_FOUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks#STATUS_NO_LINKS_APPLIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks#STATUS_DIFFERENT_TEXT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks#STATUS_UNSUPPORTED_CHARACTER:kotlin.Int` |

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getExtras

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExtras(): Bundle
```

Returns the extended data.

**NOTE:**Do not modify this bundle.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` | This value cannot be `null`. |

### getLinks

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLinks(): MutableCollection<TextLinks.TextLink!>
```

Returns an unmodifiable Collection of the links.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks.TextLink!>` | This value cannot be `null`. |

### getText

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getText(): CharSequence
```

Returns the text that was used to generate these links.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` | This value cannot be `null`. |

### toString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
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

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<TextLinks!>
```

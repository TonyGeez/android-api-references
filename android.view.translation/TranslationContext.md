Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TranslationContext

Kotlin | [Java](TranslationContext.md)
| --- | --- |

```
class TranslationContext : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.translation.TranslationContext](TranslationContext.md) |

Info class holding information for Translators and used by createOnDeviceTranslator.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext.Builder` A builder for TranslationContext |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext#FLAG_DEFINITIONS:kotlin.Int` This context will enable the Translator to return dictionary definitions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext#FLAG_LOW_LATENCY:kotlin.Int` This context will perform translations in low latency mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext#FLAG_TRANSLITERATION:kotlin.Int` This context will enable the Translator to return transliteration results. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [TranslationSpec](TranslationSpec.md) | getSourceSpec TranslationSpec describing the source data to be translated. |
| [TranslationSpec](TranslationSpec.md) | getTargetSpec TranslationSpec describing the target translated data. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getTranslationFlags Translation flags to be used by the Translator |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [TranslationContext](TranslationContext.md)!\> | `https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### FLAG_DEFINITIONS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_DEFINITIONS: Int
```

This context will enable the Translator to return dictionary definitions. 
Value is either `0` or a combination of the following:

- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext#FLAG_LOW_LATENCY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext#FLAG_TRANSLITERATION:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext#FLAG_DEFINITIONS:kotlin.Int`

<br />

 Value: 4

### FLAG_LOW_LATENCY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_LOW_LATENCY: Int
```

This context will perform translations in low latency mode. 
Value is either `0` or a combination of the following:

- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext#FLAG_LOW_LATENCY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext#FLAG_TRANSLITERATION:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext#FLAG_DEFINITIONS:kotlin.Int`

<br />

 Value: 1

### FLAG_TRANSLITERATION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_TRANSLITERATION: Int
```

This context will enable the Translator to return transliteration results. 
Value is either `0` or a combination of the following:

- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext#FLAG_LOW_LATENCY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext#FLAG_TRANSLITERATION:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext#FLAG_DEFINITIONS:kotlin.Int`

<br />

 Value: 2

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getSourceSpec

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSourceSpec(): TranslationSpec
```

TranslationSpec describing the source data to be translated.

| Return ||
|---|---|
| TranslationSpec | This value cannot be `null`. |

### getTargetSpec

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTargetSpec(): TranslationSpec
```

TranslationSpec describing the target translated data.

| Return ||
|---|---|
| TranslationSpec | This value cannot be `null`. |

### getTranslationFlags

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTranslationFlags(): Int
```

Translation flags to be used by the Translator

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext#FLAG_LOW_LATENCY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext#FLAG_TRANSLITERATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext#FLAG_DEFINITIONS:kotlin.Int` |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<TranslationContext!>
```

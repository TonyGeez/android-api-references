# LineBreakConfig

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LineBreakConfig

Kotlin | [Java](../android/graphics/text/LineBreakConfig.md) 
| --- | --- |

```
class LineBreakConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.text.LineBreakConfig](../android/graphics/text/LineBreakConfig.md) |

Specifies the line-break strategies for text wrapping.

See the [line-break property](https://www.w3.org/TR/css-text-3/#line-break-property) for more information.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/graphics/text/LineBreakConfig.Builder.md) A builder for creating a `LineBreakConfig` instance. |

| Constants ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HYPHENATION_DISABLED](../android/graphics/text/LineBreakConfig.md) The hyphenation is disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HYPHENATION_ENABLED](../android/graphics/text/LineBreakConfig.md) The hyphenation is enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HYPHENATION_UNSPECIFIED](../android/graphics/text/LineBreakConfig.md) No hyphenation preference is specified. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LINE_BREAK_STYLE_AUTO](../android/graphics/text/LineBreakConfig.md) A special value for the line breaking style option. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LINE_BREAK_STYLE_LOOSE](../android/graphics/text/LineBreakConfig.md) The least restrictive line-break rules are used for line breaking. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LINE_BREAK_STYLE_NONE](../android/graphics/text/LineBreakConfig.md) No line-break rules are used for line breaking. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LINE_BREAK_STYLE_NORMAL](../android/graphics/text/LineBreakConfig.md) The most common line-break rules are used for line breaking. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LINE_BREAK_STYLE_NO_BREAK](../android/graphics/text/LineBreakConfig.md) The line break style that used for preventing automatic line breaking. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LINE_BREAK_STYLE_STRICT](../android/graphics/text/LineBreakConfig.md) The most strict line-break rules are used for line breaking. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LINE_BREAK_STYLE_UNSPECIFIED](../android/graphics/text/LineBreakConfig.md) No line break style is specified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LINE_BREAK_WORD_STYLE_AUTO](../android/graphics/text/LineBreakConfig.md) A special value for the line breaking word style option. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LINE_BREAK_WORD_STYLE_NONE](../android/graphics/text/LineBreakConfig.md) No line-break word style is used for line breaking. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LINE_BREAK_WORD_STYLE_PHRASE](../android/graphics/text/LineBreakConfig.md) Line breaking is based on phrases, which results in text wrapping only on meaningful words. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LINE_BREAK_WORD_STYLE_UNSPECIFIED](../android/graphics/text/LineBreakConfig.md) No line break word style is specified. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/graphics/text/LineBreakConfig.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/graphics/text/LineBreakConfig.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHyphenation](../android/graphics/text/LineBreakConfig.md))`()` Returns a hyphenation preference. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineBreakStyle](../android/graphics/text/LineBreakConfig.md))`()` Gets the current line-break style. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineBreakWordStyle](../android/graphics/text/LineBreakConfig.md))`()` Gets the current line-break word style. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/graphics/text/LineBreakConfig.md))`()` <br /> |
| --- | --- |
| [LineBreakConfig](../android/graphics/text/LineBreakConfig.md) | [merge](../android/graphics/text/LineBreakConfig.md))`(`config:` ` [LineBreakConfig](../android/graphics/text/LineBreakConfig.md)`)` Generates a new [LineBreakConfig](../android/graphics/text/LineBreakConfig.md) instance merged with given `config`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/graphics/text/LineBreakConfig.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/graphics/text/LineBreakConfig.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [LineBreakConfig](../android/graphics/text/LineBreakConfig.md)!\> | [CREATOR](../android/graphics/text/LineBreakConfig.md) <br /> |

## Constants

### HYPHENATION_DISABLED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HYPHENATION_DISABLED: Int
```

The hyphenation is disabled. 

 Value: 0

### HYPHENATION_ENABLED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HYPHENATION_ENABLED: Int
```

The hyphenation is enabled. Note: Even if the hyphenation is enabled with a line break strategy [LineBreaker.BREAK_STRATEGY_SIMPLE](../android/graphics/text/LineBreaker.md), the hyphenation will not be performed unless a single word cannot meet width constraints. 

 Value: 1

### HYPHENATION_UNSPECIFIED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HYPHENATION_UNSPECIFIED: Int
```

No hyphenation preference is specified.

This is a special value of hyphenation preference indicating no hyphenation preference is specified. When overriding a [LineBreakConfig](../android/graphics/text/LineBreakConfig.md) with another [LineBreakConfig](../android/graphics/text/LineBreakConfig.md) with [Builder.merge(LineBreakConfig)](../android/graphics/text/LineBreakConfig.Builder.md)) function, the hyphenation preference of overridden config will be kept if the hyphenation preference of overriding config is [HYPHENATION_UNSPECIFIED](../android/graphics/text/LineBreakConfig.md).

```kotlin
val override = LineBreakConfig.Builder()
           .setLineBreakWordStyle(LineBreakConfig.LINE_BREAK_WORD_STYLE_PHRASE)
           .build();  // UNSPECIFIED if no setHyphenation is called.
      val config = LineBreakConfig.Builder()
           .setHyphenation(LineBreakConfig.HYPHENATION_DISABLED)
           .merge(override)
           .build()
      // Here, config has HYPHENATION_DISABLED for line break config and
      // LINE_BREAK_WORD_STYLE_PHRASE for line break word style.
  
```

This value is resolved to [HYPHENATION_ENABLED](../android/graphics/text/LineBreakConfig.md) if this value is used for text layout/rendering. 

 Value: -1

### LINE_BREAK_STYLE_AUTO

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LINE_BREAK_STYLE_AUTO: Int
```

A special value for the line breaking style option.

The auto option for the line break style set the line break style based on the locale of the text rendering context. You can specify the context locale by [android.widget.TextView#setTextLocales(LocaleList)](../android/widget/TextView.md)) or [android.graphics.Paint#setTextLocales(LocaleList)](../android/graphics/Paint.md)).

In the API [Build.VERSION_CODES.VANILLA_ICE_CREAM](../android/os/Build.VERSION_CODES.md), auto option does followings: - If at least one locale in the locale list contains Japanese script, this option is equivalent to [LINE_BREAK_STYLE_STRICT](../android/graphics/text/LineBreakConfig.md). - Otherwise, this option is equivalent to [LINE_BREAK_STYLE_NONE](../android/graphics/text/LineBreakConfig.md).

Note: future versions may have special line breaking style rules for other locales. 

 Value: 5

### LINE_BREAK_STYLE_LOOSE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LINE_BREAK_STYLE_LOOSE: Int
```

The least restrictive line-break rules are used for line breaking. This setting is typically used for short lines. 

 Value: 1

### LINE_BREAK_STYLE_NONE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LINE_BREAK_STYLE_NONE: Int
```

No line-break rules are used for line breaking. 

 Value: 0

### LINE_BREAK_STYLE_NORMAL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LINE_BREAK_STYLE_NORMAL: Int
```

The most common line-break rules are used for line breaking. 

 Value: 2

### LINE_BREAK_STYLE_NO_BREAK

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LINE_BREAK_STYLE_NO_BREAK: Int
```

The line break style that used for preventing automatic line breaking. This is useful when you want to preserve some words in the same line by using [android.text.style.LineBreakConfigSpan](../android/text/style/LineBreakConfigSpan.md) or [android.text.style.LineBreakConfigSpan#createNoBreakSpan()](../android/text/style/LineBreakConfigSpan.md)) as a shorthand. Note that even if this style is specified, the grapheme based line break is still performed for preventing clipping text. 

 Value: 4

**See Also**

- [android.text.style.LineBreakConfigSpan](../android/text/style/LineBreakConfigSpan.md)
- [android.text.style.LineBreakConfigSpan#createNoBreakSpan()](../android/text/style/LineBreakConfigSpan.md)) 

### LINE_BREAK_STYLE_STRICT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LINE_BREAK_STYLE_STRICT: Int
```

The most strict line-break rules are used for line breaking. 

 Value: 3

### LINE_BREAK_STYLE_UNSPECIFIED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LINE_BREAK_STYLE_UNSPECIFIED: Int
```

No line break style is specified.

This is a special value of line break style indicating no style value is specified. When overriding a [LineBreakConfig](../android/graphics/text/LineBreakConfig.md) with another [LineBreakConfig](../android/graphics/text/LineBreakConfig.md) with [Builder.merge(LineBreakConfig)](../android/graphics/text/LineBreakConfig.Builder.md)) function, the line break style of overridden config will be kept if the line break style of overriding config is [LINE_BREAK_STYLE_UNSPECIFIED](../android/graphics/text/LineBreakConfig.md). 

```kotlin
val override = LineBreakConfig.Builder()
           .setLineBreakWordStyle(LineBreakConfig.LINE_BREAK_WORD_STYLE_PHRASE)
           .build();  // UNSPECIFIED if no setLineBreakStyle is called.
      val config = LineBreakConfig.Builder()
           .setLineBreakStyle(LineBreakConfig.LINE_BREAK_STYLE_STRICT)
           .merge(override)
           .build()
      // Here, config has LINE_BREAK_STYLE_STRICT for line break config and
      // LINE_BREAK_WORD_STYLE_PHRASE for line break word style.
  
```

This value is resolved to [LINE_BREAK_STYLE_NONE](../android/graphics/text/LineBreakConfig.md) if the target SDK version is API [Build.VERSION_CODES.UPSIDE_DOWN_CAKE](../android/os/Build.VERSION_CODES.md) or before and this value is used for text layout/rendering. This value is resolved to [LINE_BREAK_STYLE_AUTO](../android/graphics/text/LineBreakConfig.md) if the target SDK version is API [Build.VERSION_CODES.VANILLA_ICE_CREAM](../android/os/Build.VERSION_CODES.md) or after and this value is used for text layout/rendering. 

 Value: -1

### LINE_BREAK_WORD_STYLE_AUTO

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LINE_BREAK_WORD_STYLE_AUTO: Int
```

A special value for the line breaking word style option.

The auto option for the line break word style does some heuristics based on locales and line count.

In the API [Build.VERSION_CODES.VANILLA_ICE_CREAM](../android/os/Build.VERSION_CODES.md), auto option does followings: - If at least one locale in the locale list contains Korean script, this option is equivalent to [LINE_BREAK_WORD_STYLE_PHRASE](../android/graphics/text/LineBreakConfig.md). - If not, then if at least one locale in the locale list contains Japanese script, this option is equivalent to [LINE_BREAK_WORD_STYLE_PHRASE](../android/graphics/text/LineBreakConfig.md) if the result of its line count is less than 5 lines. - Otherwise, this option is equivalent to [LINE_BREAK_WORD_STYLE_NONE](../android/graphics/text/LineBreakConfig.md).

Note: future versions may have special line breaking word style rules for other locales. 

 Value: 2

### LINE_BREAK_WORD_STYLE_NONE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LINE_BREAK_WORD_STYLE_NONE: Int
```

No line-break word style is used for line breaking. 

 Value: 0

### LINE_BREAK_WORD_STYLE_PHRASE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LINE_BREAK_WORD_STYLE_PHRASE: Int
```

Line breaking is based on phrases, which results in text wrapping only on meaningful words.

Support for this line-break word style depends on locale. If the current locale does not support phrase-based text wrapping, this setting has no effect. 

 Value: 1

### LINE_BREAK_WORD_STYLE_UNSPECIFIED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LINE_BREAK_WORD_STYLE_UNSPECIFIED: Int
```

No line break word style is specified. This is a special value of line break word style indicating no style value is specified. When overriding a [LineBreakConfig](../android/graphics/text/LineBreakConfig.md) with another [LineBreakConfig](../android/graphics/text/LineBreakConfig.md) with [Builder.merge(LineBreakConfig)](../android/graphics/text/LineBreakConfig.Builder.md)) function, the line break word style of overridden config will be kept if the line break word style of overriding config is [LINE_BREAK_WORD_STYLE_UNSPECIFIED](../android/graphics/text/LineBreakConfig.md). 

```kotlin
val override = LineBreakConfig.Builder()
           .setLineBreakStyle(LineBreakConfig.LINE_BREAK_STYLE_STRICT)
           .build();  // UNSPECIFIED if no setLineBreakWordStyle is called.
      val config = LineBreakConfig.Builder()
           .setLineBreakWordStyle(LineBreakConfig.LINE_BREAK_WORD_STYLE_PHRASE)
           .merge(override)
           .build()
      // Here, config has LINE_BREAK_STYLE_STRICT for line break config and
      // LINE_BREAK_WORD_STYLE_PHRASE for line break word style.
  
```
This value is resolved to [LINE_BREAK_WORD_STYLE_NONE](../android/graphics/text/LineBreakConfig.md) if the target SDK version is API [Build.VERSION_CODES.UPSIDE_DOWN_CAKE](../android/os/Build.VERSION_CODES.md) or before and this value is used for text layout/rendering. This value is resolved to [LINE_BREAK_WORD_STYLE_AUTO](../android/graphics/text/LineBreakConfig.md) if the target SDK version is API [Build.VERSION_CODES.VANILLA_ICE_CREAM](../android/os/Build.VERSION_CODES.md) or after and this value is used for text layout/rendering.

<br />

 Value: -1

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if this object is the same as the obj argument; `false` otherwise. |

### getHyphenation

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHyphenation(): Int
```

Returns a hyphenation preference.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A hyphenation preference. Value is [android.graphics.text.LineBreakConfig#HYPHENATION_UNSPECIFIED](../android/graphics/text/LineBreakConfig.md), [android.graphics.text.LineBreakConfig#HYPHENATION_ENABLED](../android/graphics/text/LineBreakConfig.md), or [android.graphics.text.LineBreakConfig#HYPHENATION_DISABLED](../android/graphics/text/LineBreakConfig.md) |

### getLineBreakStyle

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLineBreakStyle(): Int
```

Gets the current line-break style.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The line-break style to be used for text wrapping. Value is [android.graphics.text.LineBreakConfig#LINE_BREAK_STYLE_NONE](../android/graphics/text/LineBreakConfig.md), [android.graphics.text.LineBreakConfig#LINE_BREAK_STYLE_LOOSE](../android/graphics/text/LineBreakConfig.md), [android.graphics.text.LineBreakConfig#LINE_BREAK_STYLE_NORMAL](../android/graphics/text/LineBreakConfig.md), [android.graphics.text.LineBreakConfig#LINE_BREAK_STYLE_STRICT](../android/graphics/text/LineBreakConfig.md), [android.graphics.text.LineBreakConfig#LINE_BREAK_STYLE_UNSPECIFIED](../android/graphics/text/LineBreakConfig.md), [android.graphics.text.LineBreakConfig#LINE_BREAK_STYLE_NO_BREAK](../android/graphics/text/LineBreakConfig.md), or [android.graphics.text.LineBreakConfig#LINE_BREAK_STYLE_AUTO](../android/graphics/text/LineBreakConfig.md) |

### getLineBreakWordStyle

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLineBreakWordStyle(): Int
```

Gets the current line-break word style.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The line-break word style to be used for text wrapping. Value is [android.graphics.text.LineBreakConfig#LINE_BREAK_WORD_STYLE_NONE](../android/graphics/text/LineBreakConfig.md), [android.graphics.text.LineBreakConfig#LINE_BREAK_WORD_STYLE_PHRASE](../android/graphics/text/LineBreakConfig.md), [android.graphics.text.LineBreakConfig#LINE_BREAK_WORD_STYLE_UNSPECIFIED](../android/graphics/text/LineBreakConfig.md), or [android.graphics.text.LineBreakConfig#LINE_BREAK_WORD_STYLE_AUTO](../android/graphics/text/LineBreakConfig.md) |

### hashCode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### merge

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun merge(config: LineBreakConfig): LineBreakConfig
```

Generates a new [LineBreakConfig](../android/graphics/text/LineBreakConfig.md) instance merged with given `config`. If values of passing `config` are unspecified, the original values are kept. For example, the following code shows how line break config is merged. 

```kotlin
val override = LineBreakConfig.Builder()
           .setLineBreakWordStyle(LineBreakConfig.LINE_BREAK_WORD_STYLE_PHRASE)
           .build();  // UNSPECIFIED if no setLineBreakStyle is called.
      val config = LineBreakConfig.Builder()
           .setLineBreakStyle(LineBreakConfig.LINE_BREAK_STYLE_STRICT)
           .build();
 
      val newConfig = config.merge(override)
      // newConfig has LINE_BREAK_STYLE_STRICT of line break style and
      LINE_BREAK_WORD_STYLE_PHRASE of line break word style.
  
```

<br />

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `config` | [LineBreakConfig](../android/graphics/text/LineBreakConfig.md): an overriding config. This value cannot be `null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [LineBreakConfig](../android/graphics/text/LineBreakConfig.md) | newly created instance that is current style merged with passed config. This value cannot be `null`. |

### toString

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either `0` or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<LineBreakConfig!>
```

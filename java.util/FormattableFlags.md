# FormattableFlags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FormattableFlags

```
open class FormattableFlags
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.FormattableFlags](FormattableFlags.md) |

FormattableFlags are passed to the [Formattable.formatTo()](Formattable.md))method and modify the output format for [Formattables](Formattable.md). Implementations of [Formattable](Formattable.md) are responsible for interpreting and validating any flags.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALTERNATE](FormattableFlags.md) Requires the output to use an alternate form. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LEFT_JUSTIFY](FormattableFlags.md) Left-justifies the output. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UPPERCASE](FormattableFlags.md) Converts the output to upper case according to the rules of the [locale](Locale.md) given during creation of the`formatter`argument of the [formatTo()](Formattable.md))method. |
| --- | --- |

## Constants

### ALTERNATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALTERNATE: Int
```

Requires the output to use an alternate form. The definition of the form is specified by the`Formattable`.

This flag corresponds to`'#'`(`'\u0023'`) in the format specifier. 

 Value: 4

### LEFT_JUSTIFY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LEFT_JUSTIFY: Int
```

Left-justifies the output. Spaces (`'\u0020'`) will be added at the end of the converted value as required to fill the minimum width of the field. If this flag is not set then the output will be right-justified.

This flag corresponds to`'-'`(`'\u002d'`) in the format specifier. 

 Value: 1

### UPPERCASE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UPPERCASE: Int
```

Converts the output to upper case according to the rules of the [locale](Locale.md) given during creation of the`formatter`argument of the [formatTo()](Formattable.md))method. The output should be equivalent the following invocation of [String.toUpperCase(java.util.Locale)](../java.lang/String.md)) 

```kotlin
out.toUpperCase() 
```

<br />

This flag corresponds to`'S'`(`'\u0053'`) in the format specifier. 

 Value: 2

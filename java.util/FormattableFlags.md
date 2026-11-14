# FormattableFlags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FormattableFlags

```
open class FormattableFlags
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.util.FormattableFlags](https://developer.android.com/reference/kotlin/java/util/FormattableFlags#) |

FormattableFlags are passed to the [Formattable.formatTo()](https://developer.android.com/reference/kotlin/java/util/Formattable#formatTo(java.util.Formatter,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))method and modify the output format for [Formattables](https://developer.android.com/reference/kotlin/java/util/Formattable). Implementations of [Formattable](https://developer.android.com/reference/kotlin/java/util/Formattable) are responsible for interpreting and validating any flags.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALTERNATE](https://developer.android.com/reference/kotlin/java/util/FormattableFlags#ALTERNATE:kotlin.Int) Requires the output to use an alternate form. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LEFT_JUSTIFY](https://developer.android.com/reference/kotlin/java/util/FormattableFlags#LEFT_JUSTIFY:kotlin.Int) Left-justifies the output. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UPPERCASE](https://developer.android.com/reference/kotlin/java/util/FormattableFlags#UPPERCASE:kotlin.Int) Converts the output to upper case according to the rules of the [locale](https://developer.android.com/reference/kotlin/java/util/Locale) given during creation of the`formatter`argument of the [formatTo()](https://developer.android.com/reference/kotlin/java/util/Formattable#formatTo(java.util.Formatter,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))method. |

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

Converts the output to upper case according to the rules of the [locale](https://developer.android.com/reference/kotlin/java/util/Locale) given during creation of the`formatter`argument of the [formatTo()](https://developer.android.com/reference/kotlin/java/util/Formattable#formatTo(java.util.Formatter,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))method. The output should be equivalent the following invocation of [String.toUpperCase(java.util.Locale)](https://developer.android.com/reference/kotlin/java/lang/String.html#toUpperCase(java.util.Locale)) 

```kotlin
out.toUpperCase() 
```

<br />

This flag corresponds to`'S'`(`'\u0053'`) in the format specifier. 

 Value: 2

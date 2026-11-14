# ScientificNumberFormatter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScientificNumberFormatter

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/ScientificNumberFormatter "View this page in Java") 
| --- | --- |

```
class ScientificNumberFormatter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.ScientificNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/text/ScientificNumberFormatter#) |

A formatter that formats numbers in user-friendly scientific notation. ScientificNumberFormatter instances are immutable and thread-safe. Sample code: 

```kotlin
ULocale en = new ULocale("en");
  ScientificNumberFormatter fmt = ScientificNumberFormatter.getMarkupInstance(
          en, "<sup>", "</sup>");
  
```  

```kotlin
// Output: "1.23456×10<sup>-78</sup>"
  System.out.println(fmt.format(1.23456e-78));
  
```

<br />

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/ScientificNumberFormatter#format(kotlin.Any))`(`number:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Formats a number |
| static [ScientificNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/text/ScientificNumberFormatter#)! | [getMarkupInstance](https://developer.android.com/reference/kotlin/android/icu/text/ScientificNumberFormatter#getMarkupInstance(android.icu.text.DecimalFormat,%20kotlin.String,%20kotlin.String))`(`df:` ` [DecimalFormat](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat)!`, `beginMarkup:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `endMarkup:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets a ScientificNumberFormatter instance that uses markup for exponents. |
| static [ScientificNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/text/ScientificNumberFormatter#)! | [getMarkupInstance](https://developer.android.com/reference/kotlin/android/icu/text/ScientificNumberFormatter#getMarkupInstance(android.icu.util.ULocale,%20kotlin.String,%20kotlin.String))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`, `beginMarkup:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `endMarkup:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets a ScientificNumberFormatter instance that uses markup for exponents for this locale. |
| --- | --- |
| static [ScientificNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/text/ScientificNumberFormatter#)! | [getSuperscriptInstance](https://developer.android.com/reference/kotlin/android/icu/text/ScientificNumberFormatter#getSuperscriptInstance(android.icu.text.DecimalFormat))`(`df:` ` [DecimalFormat](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat)!`)` Gets a ScientificNumberFormatter instance that uses superscript characters for exponents. |
| static [ScientificNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/text/ScientificNumberFormatter#)! | [getSuperscriptInstance](https://developer.android.com/reference/kotlin/android/icu/text/ScientificNumberFormatter#getSuperscriptInstance(android.icu.util.ULocale))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` Gets a ScientificNumberFormatter instance that uses superscript characters for exponents for this locale. |

## Public methods

### format

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(number: Any!): String!
```

Formats a number

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `number` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:Can be a double, int, Number or anything that DecimalFormat#format(Object) accepts. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the formatted string. |

### getMarkupInstance

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getMarkupInstance(
    df: DecimalFormat!, 
    beginMarkup: String!, 
    endMarkup: String!
): ScientificNumberFormatter!
```

Gets a ScientificNumberFormatter instance that uses markup for exponents.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `df` | [DecimalFormat](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat)!:The DecimalFormat must be configured for scientific notation. Caller may safely change df after this call as this method clones it when creating the ScientificNumberFormatter. |
| `beginMarkup` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the markup to start superscript e.g`<sup>` |
| `endMarkup` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the markup to end superscript e.g`</sup>` |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [ScientificNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/text/ScientificNumberFormatter#)! | The ScientificNumberFormatter instance. |

### getMarkupInstance

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getMarkupInstance(
    locale: ULocale!, 
    beginMarkup: String!, 
    endMarkup: String!
): ScientificNumberFormatter!
```

Gets a ScientificNumberFormatter instance that uses markup for exponents for this locale.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!:The locale |
| `beginMarkup` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the markup to start superscript e.g`<sup>` |
| `endMarkup` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the markup to end superscript e.g`</sup>` |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [ScientificNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/text/ScientificNumberFormatter#)! | The ScientificNumberFormatter instance. |

### getSuperscriptInstance

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getSuperscriptInstance(df: DecimalFormat!): ScientificNumberFormatter!
```

Gets a ScientificNumberFormatter instance that uses superscript characters for exponents.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `df` | [DecimalFormat](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat)!:The DecimalFormat must be configured for scientific notation. Caller may safely change df after this call as this method clones it when creating the ScientificNumberFormatter. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [ScientificNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/text/ScientificNumberFormatter#)! | the ScientificNumberFormatter instance. |

### getSuperscriptInstance

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getSuperscriptInstance(locale: ULocale!): ScientificNumberFormatter!
```

Gets a ScientificNumberFormatter instance that uses superscript characters for exponents for this locale.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!:The locale |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [ScientificNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/text/ScientificNumberFormatter#)! | The ScientificNumberFormatter instance. |

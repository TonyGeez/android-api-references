# ScientificNumberFormatter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScientificNumberFormatter

Kotlin| [Java](ScientificNumberFormatter.md) 
| --- | --- |

```
class ScientificNumberFormatter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.ScientificNumberFormatter](ScientificNumberFormatter.md) |

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
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](ScientificNumberFormatter.md))`(`number:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Formats a number |
| static [ScientificNumberFormatter](ScientificNumberFormatter.md)! | [getMarkupInstance](ScientificNumberFormatter.md))`(`df:` ` [DecimalFormat](DecimalFormat.md)!`, `beginMarkup:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `endMarkup:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets a ScientificNumberFormatter instance that uses markup for exponents. |
| static [ScientificNumberFormatter](ScientificNumberFormatter.md)! | [getMarkupInstance](ScientificNumberFormatter.md))`(`locale:` ` [ULocale](../android.icu.util/ULocale.md)!`, `beginMarkup:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `endMarkup:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets a ScientificNumberFormatter instance that uses markup for exponents for this locale. |
| --- | --- |
| static [ScientificNumberFormatter](ScientificNumberFormatter.md)! | [getSuperscriptInstance](ScientificNumberFormatter.md))`(`df:` ` [DecimalFormat](DecimalFormat.md)!`)` Gets a ScientificNumberFormatter instance that uses superscript characters for exponents. |
| static [ScientificNumberFormatter](ScientificNumberFormatter.md)! | [getSuperscriptInstance](ScientificNumberFormatter.md))`(`locale:` ` [ULocale](../android.icu.util/ULocale.md)!`)` Gets a ScientificNumberFormatter instance that uses superscript characters for exponents for this locale. |

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
| `df` | [DecimalFormat](DecimalFormat.md)!:The DecimalFormat must be configured for scientific notation. Caller may safely change df after this call as this method clones it when creating the ScientificNumberFormatter. |
| `beginMarkup` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the markup to start superscript e.g`<sup>` |
| `endMarkup` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the markup to end superscript e.g`</sup>` |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [ScientificNumberFormatter](ScientificNumberFormatter.md)! | The ScientificNumberFormatter instance. |

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
| `locale` | [ULocale](../android.icu.util/ULocale.md)!:The locale |
| `beginMarkup` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the markup to start superscript e.g`<sup>` |
| `endMarkup` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the markup to end superscript e.g`</sup>` |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [ScientificNumberFormatter](ScientificNumberFormatter.md)! | The ScientificNumberFormatter instance. |

### getSuperscriptInstance

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getSuperscriptInstance(df: DecimalFormat!): ScientificNumberFormatter!
```

Gets a ScientificNumberFormatter instance that uses superscript characters for exponents.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `df` | [DecimalFormat](DecimalFormat.md)!:The DecimalFormat must be configured for scientific notation. Caller may safely change df after this call as this method clones it when creating the ScientificNumberFormatter. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [ScientificNumberFormatter](ScientificNumberFormatter.md)! | the ScientificNumberFormatter instance. |

### getSuperscriptInstance

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getSuperscriptInstance(locale: ULocale!): ScientificNumberFormatter!
```

Gets a ScientificNumberFormatter instance that uses superscript characters for exponents for this locale.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android.icu.util/ULocale.md)!:The locale |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [ScientificNumberFormatter](ScientificNumberFormatter.md)! | The ScientificNumberFormatter instance. |

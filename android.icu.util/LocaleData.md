# LocaleData

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocaleData

Kotlin | [Java](https://developer.android.com/reference/android/icu/util/LocaleData "View this page in Java") 

```
class LocaleData
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.icu.util.LocaleData](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#) |

A class for accessing miscellaneous data in the locale bundles

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [MeasurementSystem](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData.MeasurementSystem) Enumeration for representing the measurement systems. |
| | [PaperSize](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData.PaperSize) A class that represents the size of letter head used in the country |

| Constants ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALT_QUOTATION_END](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#ALT_QUOTATION_END:kotlin.Int) Delimiter type for [getDelimiter(int)](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#getDelimiter(kotlin.Int)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALT_QUOTATION_START](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#ALT_QUOTATION_START:kotlin.Int) Delimiter type for [getDelimiter(int)](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#getDelimiter(kotlin.Int)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUOTATION_END](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#QUOTATION_END:kotlin.Int) Delimiter type for [getDelimiter(int)](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#getDelimiter(kotlin.Int)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUOTATION_START](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#QUOTATION_START:kotlin.Int) Delimiter type for [getDelimiter(int)](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#getDelimiter(kotlin.Int)). |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [VersionInfo](https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo)! | [getCLDRVersion](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#getCLDRVersion())`()` Returns the current CLDR version |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDelimiter](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#getDelimiter(kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves a delimiter string from the locale data. |
| static [LocaleData](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#getInstance())`()` Gets the LocaleData object associated with the default `FORMAT` locale |
| static [LocaleData](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#getInstance(android.icu.util.ULocale))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!`)` Gets the LocaleData object associated with the ULocale specified in locale |
| static [LocaleData.MeasurementSystem](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData.MeasurementSystem)! | [getMeasurementSystem](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#getMeasurementSystem(android.icu.util.ULocale))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!`)` Returns the measurement system used in the locale specified by the locale. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getNoSubstitute](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#getNoSubstitute())`()` Gets the "no substitute" behavior of this locale data object. |
| static [LocaleData.PaperSize](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData.PaperSize)! | [getPaperSize](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#getPaperSize(android.icu.util.ULocale))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!`)` Returns the size of paper used in the locale. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNoSubstitute](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#setNoSubstitute(kotlin.Boolean))`(`setting:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the "no substitute" behavior of this locale data object. |

## Constants

### ALT_QUOTATION_END

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALT_QUOTATION_END: Int
```

Delimiter type for [getDelimiter(int)](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#getDelimiter(kotlin.Int)). 

 Value: 3

### ALT_QUOTATION_START

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALT_QUOTATION_START: Int
```

Delimiter type for [getDelimiter(int)](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#getDelimiter(kotlin.Int)). 

 Value: 2

### QUOTATION_END

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUOTATION_END: Int
```

Delimiter type for [getDelimiter(int)](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#getDelimiter(kotlin.Int)). 

 Value: 1

### QUOTATION_START

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUOTATION_START: Int
```

Delimiter type for [getDelimiter(int)](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#getDelimiter(kotlin.Int)). 

 Value: 0

## Public methods

### getCLDRVersion

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getCLDRVersion(): VersionInfo!
```

Returns the current CLDR version 

### getDelimiter

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDelimiter(type: Int): String!
```

Retrieves a delimiter string from the locale data.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of delimiter string desired. Currently, the valid choices are QUOTATION_START, QUOTATION_END, ALT_QUOTATION_START, or ALT_QUOTATION_END. |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The desired delimiter string. |

### getInstance

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(): LocaleData!
```

Gets the LocaleData object associated with the default `FORMAT` locale

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------|
| [LocaleData](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#)! | A locale data object. |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category) 

### getInstance

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(locale: ULocale!): LocaleData!
```

Gets the LocaleData object associated with the ULocale specified in locale

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!: Locale with thich the locale data object is associated. |

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------|
| [LocaleData](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData#)! | A locale data object. |

### getMeasurementSystem

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getMeasurementSystem(locale: ULocale!): LocaleData.MeasurementSystem!
```

Returns the measurement system used in the locale specified by the locale.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!: The locale for which the measurement system to be retrieved. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [LocaleData.MeasurementSystem](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData.MeasurementSystem)! | MeasurementSystem the measurement system used in the locale. |

### getNoSubstitute

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNoSubstitute(): Boolean
```

Gets the "no substitute" behavior of this locale data object.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Value for the no substitute behavior. If true, methods of this locale data object will return an error when no data is available for that method, given the locale ID supplied to the constructor. |

### getPaperSize

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getPaperSize(locale: ULocale!): LocaleData.PaperSize!
```

Returns the size of paper used in the locale. The paper sizes returned are always in *milli-meters*.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!: The locale for which the measurement system to be retrieved. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [LocaleData.PaperSize](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData.PaperSize)! | The paper size used in the locale |

### setNoSubstitute

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setNoSubstitute(setting: Boolean): Unit
```

Sets the "no substitute" behavior of this locale data object.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `setting` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Value for the no substitute behavior. If true, methods of this locale data object will return an error when no data is available for that method, given the locale ID supplied to the constructor. |

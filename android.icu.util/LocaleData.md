# LocaleData

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocaleData

Kotlin | [Java](../android/icu/util/LocaleData.md) 
| --- | --- |

```
class LocaleData
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.util.LocaleData](../android/icu/util/LocaleData.md) |

A class for accessing miscellaneous data in the locale bundles

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [MeasurementSystem](../android/icu/util/LocaleData.MeasurementSystem.md) Enumeration for representing the measurement systems. |
| | [PaperSize](../android/icu/util/LocaleData.PaperSize.md) A class that represents the size of letter head used in the country |

| Constants ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALT_QUOTATION_END](../android/icu/util/LocaleData.md) Delimiter type for [getDelimiter(int)](../android/icu/util/LocaleData.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALT_QUOTATION_START](../android/icu/util/LocaleData.md) Delimiter type for [getDelimiter(int)](../android/icu/util/LocaleData.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUOTATION_END](../android/icu/util/LocaleData.md) Delimiter type for [getDelimiter(int)](../android/icu/util/LocaleData.md)). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUOTATION_START](../android/icu/util/LocaleData.md) Delimiter type for [getDelimiter(int)](../android/icu/util/LocaleData.md)). |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [VersionInfo](../android/icu/util/VersionInfo.md)! | [getCLDRVersion](../android/icu/util/LocaleData.md))`()` Returns the current CLDR version |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDelimiter](../android/icu/util/LocaleData.md))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves a delimiter string from the locale data. |
| static [LocaleData](../android/icu/util/LocaleData.md)! | [getInstance](../android/icu/util/LocaleData.md))`()` Gets the LocaleData object associated with the default `FORMAT` locale |
| --- | --- |
| static [LocaleData](../android/icu/util/LocaleData.md)! | [getInstance](../android/icu/util/LocaleData.md))`(`locale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` Gets the LocaleData object associated with the ULocale specified in locale |
| static [LocaleData.MeasurementSystem](../android/icu/util/LocaleData.MeasurementSystem.md)! | [getMeasurementSystem](../android/icu/util/LocaleData.md))`(`locale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` Returns the measurement system used in the locale specified by the locale. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getNoSubstitute](../android/icu/util/LocaleData.md))`()` Gets the "no substitute" behavior of this locale data object. |
| --- | --- |
| static [LocaleData.PaperSize](../android/icu/util/LocaleData.PaperSize.md)! | [getPaperSize](../android/icu/util/LocaleData.md))`(`locale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` Returns the size of paper used in the locale. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNoSubstitute](../android/icu/util/LocaleData.md))`(`setting:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the "no substitute" behavior of this locale data object. |

## Constants

### ALT_QUOTATION_END

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALT_QUOTATION_END: Int
```

Delimiter type for [getDelimiter(int)](../android/icu/util/LocaleData.md)). 

 Value: 3

### ALT_QUOTATION_START

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALT_QUOTATION_START: Int
```

Delimiter type for [getDelimiter(int)](../android/icu/util/LocaleData.md)). 

 Value: 2

### QUOTATION_END

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUOTATION_END: Int
```

Delimiter type for [getDelimiter(int)](../android/icu/util/LocaleData.md)). 

 Value: 1

### QUOTATION_START

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUOTATION_START: Int
```

Delimiter type for [getDelimiter(int)](../android/icu/util/LocaleData.md)). 

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
| [LocaleData](../android/icu/util/LocaleData.md)! | A locale data object. |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](../android/icu/util/ULocale.Category.md) 

### getInstance

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(locale: ULocale!): LocaleData!
```

Gets the LocaleData object associated with the ULocale specified in locale

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android/icu/util/ULocale.md)!: Locale with thich the locale data object is associated. |

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------|
| [LocaleData](../android/icu/util/LocaleData.md)! | A locale data object. |

### getMeasurementSystem

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getMeasurementSystem(locale: ULocale!): LocaleData.MeasurementSystem!
```

Returns the measurement system used in the locale specified by the locale.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android/icu/util/ULocale.md)!: The locale for which the measurement system to be retrieved. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [LocaleData.MeasurementSystem](../android/icu/util/LocaleData.MeasurementSystem.md)! | MeasurementSystem the measurement system used in the locale. |

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
| `locale` | [ULocale](../android/icu/util/ULocale.md)!: The locale for which the measurement system to be retrieved. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [LocaleData.PaperSize](../android/icu/util/LocaleData.PaperSize.md)! | The paper size used in the locale |

### setNoSubstitute

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setNoSubstitute(setting: Boolean): Unit
```

Sets the "no substitute" behavior of this locale data object.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `setting` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Value for the no substitute behavior. If true, methods of this locale data object will return an error when no data is available for that method, given the locale ID supplied to the constructor. |

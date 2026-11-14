# MeasureFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MeasureFormat

Kotlin| [Java](MeasureFormat.md) 
| --- | --- |

```
open class MeasureFormat : UFormat
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.text.Format](../java.text/Format.md) |||
| | ↳ | [android.icu.text.UFormat](UFormat.md) ||
| | | ↳ | [android.icu.text.MeasureFormat](MeasureFormat.md) |
| --- | --- | --- | --- |

A formatter for Measure objects.

**IMPORTANT:** New users are strongly encouraged to see if [NumberFormatter](../android.icu.number/NumberFormatter.md) fits their use case. Although not deprecated, this class, MeasureFormat, is provided for backwards compatibility only, and has much more limited capabilities.

To format a Measure object, first create a formatter object using a MeasureFormat factory method. Then use that object's format or formatMeasures methods. Here is sample code: 

```kotlin
MeasureFormat fmtFr = MeasureFormat.getInstance(ULocale.FRENCH, FormatWidth.SHORT);
  Measure measure = new Measure(23, MeasureUnit.CELSIUS);
 
  // Output: 23 °C
  System.out.println(fmtFr.format(measure));
 
  Measure measureF = new Measure(70, MeasureUnit.FAHRENHEIT);
 
  // Output: 70 °F
  System.out.println(fmtFr.format(measureF));
 
  MeasureFormat fmtFrFull = MeasureFormat.getInstance(ULocale.FRENCH, FormatWidth.WIDE);
  // Output: 70 pieds et 5,3 pouces
  System.out.println(fmtFrFull.formatMeasures(new Measure(70, MeasureUnit.FOOT),
          new Measure(5.3, MeasureUnit.INCH)));
 
  // Output: 1 pied et 1 pouce
  System.out.println(
          fmtFrFull.formatMeasures(new Measure(1, MeasureUnit.FOOT), new Measure(1, MeasureUnit.INCH)));
 
  MeasureFormat fmtFrNarrow = MeasureFormat.getInstance(ULocale.FRENCH, FormatWidth.NARROW);
  // Output: 1′ 1″
  System.out.println(fmtFrNarrow.formatMeasures(new Measure(1, MeasureUnit.FOOT),
          new Measure(1, MeasureUnit.INCH)));
 
  MeasureFormat fmtEn = MeasureFormat.getInstance(ULocale.ENGLISH, FormatWidth.WIDE);
 
  // Output: 1 inch, 2 feet
  fmtEn.formatMeasures(new Measure(1, MeasureUnit.INCH), new Measure(2, MeasureUnit.FOOT));
  
```

This class does not do conversions from one unit to another. It simply formats whatever units it is given

This class is immutable and thread-safe so long as its deprecated subclass, TimeUnitFormat, is never used. TimeUnitFormat is not thread-safe, and is mutable. Although this class has existing subclasses, this class does not support new sub-classes.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------|
| | [FormatWidth](../android/icu/text/MeasureFormat.FormatWidth.md) Formatting width enum. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](MeasureFormat.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Two MeasureFormats, a and b, are equal if and only if they have the same formatWidth, locale, and equal number formats. |
| open [StringBuffer](../java.lang/StringBuffer.md)! | [format](MeasureFormat.md))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `toAppendTo:` ` [StringBuffer](../java.lang/StringBuffer.md)!`, `fpos:` ` [FieldPosition](../java.text/FieldPosition.md)!`)` Able to format Collection\<? extends Measure\>, Measure\[\], and Measure by delegating to formatMeasures. |
| open [StringBuilder](../java.lang/StringBuilder.md)! | [formatMeasurePerUnit](MeasureFormat.md))`(`measure:` ` [Measure](../android.icu.util/Measure.md)!`, `perUnit:` ` [MeasureUnit](../android.icu.util/MeasureUnit.md)!`, `appendTo:` ` [StringBuilder](../java.lang/StringBuilder.md)!`, `pos:` ` [FieldPosition](../java.text/FieldPosition.md)!`)` Formats a single measure per unit. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [formatMeasures](MeasureFormat.md))`(`vararg` `measures:` ` [Measure](../android.icu.util/Measure.md)!`)` Format a sequence of measures. |
| open [StringBuilder](../java.lang/StringBuilder.md)! | [formatMeasures](MeasureFormat.md))`(`appendTo:` ` [StringBuilder](../java.lang/StringBuilder.md)!`, `fpos:` ` [FieldPosition](../java.text/FieldPosition.md)!`, `vararg` `measures:` ` [Measure](../android.icu.util/Measure.md)!`)` Formats a sequence of measures. |
| openstatic [MeasureFormat](MeasureFormat.md)! | [getCurrencyFormat](MeasureFormat.md))`()` Return a formatter for CurrencyAmount objects in the default`FORMAT`locale. |
| --- | --- |
| openstatic [MeasureFormat](MeasureFormat.md)! | [getCurrencyFormat](MeasureFormat.md))`(`locale:` ` [ULocale](../android.icu.util/ULocale.md)!`)` Return a formatter for CurrencyAmount objects in the given locale. |
| openstatic [MeasureFormat](MeasureFormat.md)! | [getCurrencyFormat](MeasureFormat.md))`(`locale:` ` [Locale](../java.util/Locale.md)!`)` Return a formatter for CurrencyAmount objects in the given [java.util.Locale](../java.util/Locale.md). |
| openstatic [MeasureFormat](MeasureFormat.md)! | [getInstance](MeasureFormat.md))`(`locale:` ` [ULocale](../android.icu.util/ULocale.md)!`, `formatWidth:` ` [MeasureFormat.FormatWidth](../android/icu/text/MeasureFormat.FormatWidth.md)!`)` Create a format from the locale, formatWidth, and format. |
| --- | --- |
| openstatic [MeasureFormat](MeasureFormat.md)! | [getInstance](MeasureFormat.md))`(`locale:` ` [ULocale](../android.icu.util/ULocale.md)!`, `formatWidth:` ` [MeasureFormat.FormatWidth](../android/icu/text/MeasureFormat.FormatWidth.md)!`, `format:` ` [NumberFormat](NumberFormat.md)!`)` Create a format from the locale, formatWidth, and format. |
| openstatic [MeasureFormat](MeasureFormat.md)! | [getInstance](MeasureFormat.md))`(`locale:` ` [Locale](../java.util/Locale.md)!`, `formatWidth:` ` [MeasureFormat.FormatWidth](../android/icu/text/MeasureFormat.FormatWidth.md)!`)` Create a format from the [java.util.Locale](../java.util/Locale.md) and formatWidth. |
| openstatic [MeasureFormat](MeasureFormat.md)! | [getInstance](MeasureFormat.md))`(`locale:` ` [Locale](../java.util/Locale.md)!`, `formatWidth:` ` [MeasureFormat.FormatWidth](../android/icu/text/MeasureFormat.FormatWidth.md)!`, `format:` ` [NumberFormat](NumberFormat.md)!`)` Create a format from the [java.util.Locale](../java.util/Locale.md), formatWidth, and format. |
| --- | --- |
| [ULocale](../android.icu.util/ULocale.md)! | [getLocale](MeasureFormat.md))`()` Get the locale of this instance. |
| open [NumberFormat](NumberFormat.md)! | [getNumberFormat](MeasureFormat.md))`()` Get a copy of the number format. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getUnitDisplayName](MeasureFormat.md))`(`unit:` ` [MeasureUnit](../android.icu.util/MeasureUnit.md)!`)` Gets the display name of the specified [MeasureUnit](../android.icu.util/MeasureUnit.md) corresponding to the current locale and format width. |
| --- | --- |
| open [MeasureFormat.FormatWidth](../android/icu/text/MeasureFormat.FormatWidth.md)! | [getWidth](MeasureFormat.md))`()` Get the format width this instance is using. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](MeasureFormat.md))`()` Returns a hash code value for the object. |

## Public methods

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Two MeasureFormats, a and b, are equal if and only if they have the same formatWidth, locale, and equal number formats.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun format(
    obj: Any!, 
    toAppendTo: StringBuffer!, 
    fpos: FieldPosition!
): StringBuffer!
```

Able to format Collection\<? extends Measure\>, Measure\[\], and Measure by delegating to formatMeasures. If the pos argument identifies a NumberFormat field, then its indices are set to the beginning and end of the first such field encountered. MeasureFormat itself does not supply any fields. Calling a`formatMeasures`method is preferred over calling this method as they give better performance.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:must be a Collection\<? extends Measure\>, Measure\[\], or Measure object. |
| `toAppendTo` | [StringBuffer](../java.lang/StringBuffer.md)!:Formatted string appended here. |
| `pos` | A`FieldPosition`identifying a field in the formatted text |
| --- | --- |
| `fpos` | [FieldPosition](../java.text/FieldPosition.md)!:Identifies a field in the formatted text. |

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [StringBuffer](../java.lang/StringBuffer.md)! | the string buffer passed in as`toAppendTo`, with formatted text appended |

| Exceptions ||
|--------------------------------------|----------------------------------------------|
| `java.lang.NullPointerException` | if`toAppendTo`or`pos`is null |
| `java.lang.IllegalArgumentException` | if the Format cannot format the given object |

**See Also**

- [java.text.Format#format(java.lang.Object, java.lang.StringBuffer, java.text.FieldPosition)](../java.text/Format.md)) 

### formatMeasurePerUnit

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun formatMeasurePerUnit(
    measure: Measure!, 
    perUnit: MeasureUnit!, 
    appendTo: StringBuilder!, 
    pos: FieldPosition!
): StringBuilder!
```

Formats a single measure per unit. An example of such a formatted string is "3.5 meters per second."

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `measure` | [Measure](../android.icu.util/Measure.md)!:the measure object. In above example, 3.5 meters. |
| `perUnit` | [MeasureUnit](../android.icu.util/MeasureUnit.md)!:the per unit. In above example, it is MeasureUnit.SECOND |
| `appendTo` | [StringBuilder](../java.lang/StringBuilder.md)!:formatted string appended here. |
| --- | --- |
| `pos` | [FieldPosition](../java.text/FieldPosition.md)!:The field position. |

| Return ||
|------------------------------------------------------------------------------------------------|-----------|
| [StringBuilder](../java.lang/StringBuilder.md)! | appendTo. |

### formatMeasures

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun formatMeasures(vararg measures: Measure!): String!
```

Format a sequence of measures. Uses the ListFormatter unit lists. So, for example, one could format "3 feet, 2 inches". Zero values are formatted (eg, "3 feet, 0 inches"). It is the caller's responsibility to have the appropriate values in appropriate order, and using the appropriate Number values. Typically the units should be in descending order, with all but the last Measure having integer values (eg, not "3.2 feet, 2 inches").

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------|
| `measures` | [Measure](../android.icu.util/Measure.md)!:a sequence of one or more measures. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the formatted string. |

### formatMeasures

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun formatMeasures(
    appendTo: StringBuilder!, 
    fpos: FieldPosition!, 
    vararg measures: Measure!
): StringBuilder!
```

Formats a sequence of measures. If the fieldPosition argument identifies a NumberFormat field, then its indices are set to the beginning and end of the first such field encountered. MeasureFormat itself does not supply any fields.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `appendTo` | [StringBuilder](../java.lang/StringBuilder.md)!:the formatted string appended here. |
| `fpos` | [FieldPosition](../java.text/FieldPosition.md)!:Identifies a field in the formatted text. |
| `measures` | [Measure](../android.icu.util/Measure.md)!:the measures to format. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------------|-----------|
| [StringBuilder](../java.lang/StringBuilder.md)! | appendTo. |

**See Also**

- [android.icu.text.MeasureFormat#formatMeasures(Measure...)](MeasureFormat.md)) 

### getCurrencyFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCurrencyFormat(): MeasureFormat!
```

Return a formatter for CurrencyAmount objects in the default`FORMAT`locale.

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------|
| [MeasureFormat](MeasureFormat.md)! | a formatter object |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](../android/icu/util/ULocale.Category.md) 

### getCurrencyFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCurrencyFormat(locale: ULocale!): MeasureFormat!
```

Return a formatter for CurrencyAmount objects in the given locale.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android.icu.util/ULocale.md)!:desired locale |

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------|
| [MeasureFormat](MeasureFormat.md)! | a formatter object |

### getCurrencyFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCurrencyFormat(locale: Locale!): MeasureFormat!
```

Return a formatter for CurrencyAmount objects in the given [java.util.Locale](../java.util/Locale.md).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java.util/Locale.md)!:desired [java.util.Locale](../java.util/Locale.md) |

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------|
| [MeasureFormat](MeasureFormat.md)! | a formatter object |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    locale: ULocale!, 
    formatWidth: MeasureFormat.FormatWidth!
): MeasureFormat!
```

Create a format from the locale, formatWidth, and format.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android.icu.util/ULocale.md)!:the locale. |
| `formatWidth` | [MeasureFormat.FormatWidth](../android/icu/text/MeasureFormat.FormatWidth.md)!:hints how long formatted strings should be. |

| Return ||
|--------------------------------------------------------------------------------------------------|-------------------------------|
| [MeasureFormat](MeasureFormat.md)! | The new MeasureFormat object. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    locale: ULocale!, 
    formatWidth: MeasureFormat.FormatWidth!, 
    format: NumberFormat!
): MeasureFormat!
```

Create a format from the locale, formatWidth, and format.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android.icu.util/ULocale.md)!:the locale. |
| `formatWidth` | [MeasureFormat.FormatWidth](../android/icu/text/MeasureFormat.FormatWidth.md)!:hints how long formatted strings should be. |
| `format` | [NumberFormat](NumberFormat.md)!:This is defensively copied. |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------------|-------------------------------|
| [MeasureFormat](MeasureFormat.md)! | The new MeasureFormat object. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    locale: Locale!, 
    formatWidth: MeasureFormat.FormatWidth!
): MeasureFormat!
```

Create a format from the [java.util.Locale](../java.util/Locale.md) and formatWidth.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java.util/Locale.md)!:the [java.util.Locale](../java.util/Locale.md). |
| `formatWidth` | [MeasureFormat.FormatWidth](../android/icu/text/MeasureFormat.FormatWidth.md)!:hints how long formatted strings should be. |

| Return ||
|--------------------------------------------------------------------------------------------------|-------------------------------|
| [MeasureFormat](MeasureFormat.md)! | The new MeasureFormat object. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    locale: Locale!, 
    formatWidth: MeasureFormat.FormatWidth!, 
    format: NumberFormat!
): MeasureFormat!
```

Create a format from the [java.util.Locale](../java.util/Locale.md), formatWidth, and format.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java.util/Locale.md)!:the [java.util.Locale](../java.util/Locale.md). |
| `formatWidth` | [MeasureFormat.FormatWidth](../android/icu/text/MeasureFormat.FormatWidth.md)!:hints how long formatted strings should be. |
| `format` | [NumberFormat](NumberFormat.md)!:This is defensively copied. |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------------|-------------------------------|
| [MeasureFormat](MeasureFormat.md)! | The new MeasureFormat object. |

### getLocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocale(): ULocale!
```

Get the locale of this instance. 

### getNumberFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNumberFormat(): NumberFormat!
```

Get a copy of the number format. 

### getUnitDisplayName

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUnitDisplayName(unit: MeasureUnit!): String!
```

Gets the display name of the specified [MeasureUnit](../android.icu.util/MeasureUnit.md) corresponding to the current locale and format width.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `unit` | [MeasureUnit](../android.icu.util/MeasureUnit.md)!:The unit for which to get a display name. |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The display name in the locale and width specified in android.icu.text.MeasureFormat#getInstance, or null if there is no display name available for the specified unit. |

### getWidth

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWidth(): MeasureFormat.FormatWidth!
```

Get the format width this instance is using. 

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](../java.util/HashMap.md).

The general contract of`hashCode`is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the`hashCode`method must consistently return the same integer, provided no information used in`equals`comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the [equals](../java.lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce the same integer result.
- It is*not* required that if two objects are unequal according to the [equals](../java.lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

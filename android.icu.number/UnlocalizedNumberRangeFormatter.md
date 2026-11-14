# UnlocalizedNumberRangeFormatter

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnlocalizedNumberRangeFormatter

Kotlin| [Java](../android/icu/number/UnlocalizedNumberRangeFormatter.md) 
| --- | --- |

```
open class UnlocalizedNumberRangeFormatter : NumberRangeFormatterSettings<UnlocalizedNumberRangeFormatter!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.icu.number.NumberRangeFormatterSettings](../android/icu/number/NumberRangeFormatterSettings.md)\< [android.icu.number.UnlocalizedNumberRangeFormatter](../android/icu/number/UnlocalizedNumberRangeFormatter.md)\> ||
| | ↳ | [android.icu.number.UnlocalizedNumberRangeFormatter](../android/icu/number/UnlocalizedNumberRangeFormatter.md) |

A NumberRangeFormatter that does not yet have a locale. In order to format, a locale must be specified. Instances of this class are immutable and thread-safe.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [LocalizedNumberRangeFormatter](../android/icu/number/LocalizedNumberRangeFormatter.md)! | [locale](../android/icu/number/UnlocalizedNumberRangeFormatter.md))`(`locale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` ULocale version of the [locale(java.util.Locale)](../android/icu/number/UnlocalizedNumberRangeFormatter.md))setter above. |
| open [LocalizedNumberRangeFormatter](../android/icu/number/LocalizedNumberRangeFormatter.md)! | [locale](../android/icu/number/UnlocalizedNumberRangeFormatter.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`)` Associate the given locale with the number range formatter. |

| Inherited functions ||
|---|---|
| From class [NumberRangeFormatterSettings](../android/icu/number/NumberRangeFormatterSettings.md) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | T | [collapse](../android/icu/number/NumberRangeFormatterSettings.md))`(`collapse:` ` [NumberRangeFormatter.RangeCollapse](../android/icu/number/NumberRangeFormatter.RangeCollapse.md)!`)` <br /> Sets the aggressiveness of "collapsing" fields across the range separator. Possible values: - ALL: "3-5K miles" - UNIT: "3K - 5K miles" - NONE: "3K miles - 5K miles" - AUTO: usually UNIT or NONE, depending on the locale and formatter settings <br /> The default value is AUTO. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/icu/number/NumberRangeFormatterSettings.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Indicates whether some other object is "equal to" this one. The`equals`method implements an equivalence relation on non-null object references: - It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`. - It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`. - It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`. - It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified. - For any non-null reference value`x`,`x.equals(null)`should return`false`. An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/icu/number/NumberRangeFormatterSettings.md))`()` <br /> Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](../java/util/HashMap.md). The general contract of`hashCode`is: - Whenever it is invoked on the same object more than once during an execution of a Java application, the`hashCode`method must consistently return the same integer, provided no information used in`equals`comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application. - If two objects are equal according to the [equals](../java/lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce the same integer result. - It is*not* required that if two objects are unequal according to the [equals](../java/lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables. <br /> | | T | [identityFallback](../android/icu/number/NumberRangeFormatterSettings.md))`(`identityFallback:` ` [NumberRangeFormatter.RangeIdentityFallback](../android/icu/number/NumberRangeFormatter.RangeIdentityFallback.md)!`)` <br /> Sets the behavior when the two sides of the range are the same. This could happen if the same two numbers are passed to the formatRange function, or if different numbers are passed to the function but they become the same after rounding rules are applied. Possible values: - SINGLE_VALUE: "5 miles" - APPROXIMATELY_OR_SINGLE_VALUE: "\~5 miles" or "5 miles", depending on whether the number was the same before rounding was applied - APPROXIMATELY: "\~5 miles" - RANGE: "5-5 miles" (with collapse=UNIT) <br /> The default value is APPROXIMATELY. <br /> | | T | [numberFormatterBoth](../android/icu/number/NumberRangeFormatterSettings.md))`(`formatter:` ` [UnlocalizedNumberFormatter](../android/icu/number/UnlocalizedNumberFormatter.md)!`)` <br /> Sets the NumberFormatter instance to use for the numbers in the range. The same formatter is applied to both sides of the range. The NumberFormatter instances must not have a locale applied yet; the locale specified on the NumberRangeFormatter will be used. <br /> | | T | [numberFormatterFirst](../android/icu/number/NumberRangeFormatterSettings.md))`(`formatterFirst:` ` [UnlocalizedNumberFormatter](../android/icu/number/UnlocalizedNumberFormatter.md)!`)` <br /> Sets the NumberFormatter instance to use for the first number in the range. The NumberFormatter instance must not have a locale applied yet; the locale specified on the NumberRangeFormatter will be used. <br /> | | T | [numberFormatterSecond](../android/icu/number/NumberRangeFormatterSettings.md))`(`formatterSecond:` ` [UnlocalizedNumberFormatter](../android/icu/number/UnlocalizedNumberFormatter.md)!`)` <br /> Sets the NumberFormatter instances to use for the second number in the range. The NumberFormatter instance must not have a locale applied yet; the locale specified on the NumberRangeFormatter will be used. <br /> | ||

## Public methods

### locale

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun locale(locale: ULocale!): LocalizedNumberRangeFormatter!
```

ULocale version of the [locale(java.util.Locale)](../android/icu/number/UnlocalizedNumberRangeFormatter.md))setter above.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android/icu/util/ULocale.md)!:The locale to use when loading data for number range formatting. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------|------------------|
| [LocalizedNumberRangeFormatter](../android/icu/number/LocalizedNumberRangeFormatter.md)! | The fluent chain |

**See Also**

- [#locale(Locale)](../android/icu/number/UnlocalizedNumberRangeFormatter.md)) 

### locale

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun locale(locale: Locale!): LocalizedNumberRangeFormatter!
```

Associate the given locale with the number range formatter. The locale is used for picking the appropriate symbols, formats, and other data for number display.

To use the Java default locale, call Locale.getDefault(): 

```kotlin
NumberFormatter.with(). ... .locale(Locale.getDefault())
  
```

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:The locale to use when loading data for number range formatting. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------|------------------|
| [LocalizedNumberRangeFormatter](../android/icu/number/LocalizedNumberRangeFormatter.md)! | The fluent chain |

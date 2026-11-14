Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DateIntervalInfo

Kotlin | [Java](DateIntervalInfo.md)
| --- | --- |

```
open class DateIntervalInfo : Cloneable, Freezable<DateIntervalInfo!>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.DateIntervalInfo](DateIntervalInfo.md) |

DateIntervalInfo is a public class for encapsulating localizable date time interval patterns. It is used by DateIntervalFormat.

For most users, ordinary use of DateIntervalFormat does not need to create DateIntervalInfo object directly. DateIntervalFormat will take care of it when creating a date interval formatter when user pass in skeleton and locale.

For power users, who want to create their own date interval patterns, or want to re-set date interval patterns, they could do so by directly creating DateIntervalInfo and manipulating it.

Logically, the interval patterns are mappings from (skeleton, the_largest_different_calendar_field) to (date_interval_pattern).

A skeleton

1. only keeps the field pattern letter and ignores all other parts in a pattern, such as space, punctuations, and string literals.
2. hides the order of fields.
3. might hide a field's pattern letter length. For those non-digit calendar fields, the pattern letter length is important, such as MMM, MMMM, and MMMMM; EEE and EEEE, and the field's pattern letter length is honored. For the digit calendar fields, such as M or MM, d or dd, yy or yyyy, the field pattern length is ignored and the best match, which is defined in date time patterns, will be returned without honor the field pattern letter length in skeleton.

The calendar fields we support for interval formatting are: year, month, date, day-of-week, am-pm, hour, hour-of-day, minute, and second (though we do not currently have specific intervalFormat data for skeletons with seconds). Those calendar fields can be defined in the following order: year \> month \> date \> am-pm \> hour \> minute \> second The largest different calendar fields between 2 calendars is the first different calendar field in above order. For example: the largest different calendar fields between "Jan 10, 2007" and "Feb 20, 2008" is year.

There is a set of pre-defined static skeleton strings. There are pre-defined interval patterns for those pre-defined skeletons in locales' resource files. For example, for a skeleton YEAR_ABBR_MONTH_DAY, which is "yMMMd", in en_US, if the largest different calendar field between date1 and date2 is "year", the date interval pattern is "MMM d, yyyy - MMM d, yyyy", such as "Jan 10, 2007 - Jan 10, 2008". If the largest different calendar field between date1 and date2 is "month", the date interval pattern is "MMM d - MMM d, yyyy", such as "Jan 10 - Feb 10, 2007". If the largest different calendar field between date1 and date2 is "day", the date interval pattern is ""MMM d-d, yyyy", such as "Jan 10-20, 2007". For date skeleton, the interval patterns when year, or month, or date is different are defined in resource files. For time skeleton, the interval patterns when am/pm, or hour, or minute is different are defined in resource files.

There are 2 dates in interval pattern. For most locales, the first date in an interval pattern is the earlier date. There might be a locale in which the first date in an interval pattern is the later date. We use fallback format for the default order for the locale. For example, if the fallback format is "{0} - {1}", it means the first date in the interval pattern for this locale is earlier date. If the fallback format is "{1} - {0}", it means the first date is the later date. For a particular interval pattern, the default order can be overridden by prefixing "latestFirst:" or "earliestFirst:" to the interval pattern. For example, if the fallback format is "{0}-{1}", but for skeleton "yMMMd", the interval pattern when day is different is "latestFirst:d-d MMM yy", it means by default, the first date in interval pattern is the earlier date. But for skeleton "yMMMd", when day is different, the first date in "d-d MMM yy" is the later date.

The recommended way to create a DateIntervalFormat object is to pass in the locale. By using a Locale parameter, the DateIntervalFormat object is initialized with the pre-defined interval patterns for a given or default locale.

Users can also create DateIntervalFormat object by supplying their own interval patterns. It provides flexibility for power usage.

After a DateIntervalInfo object is created, clients may modify the interval patterns using setIntervalPattern function as so desired. Currently, users can only set interval patterns when the following calendar fields are different: ERA, YEAR, MONTH, DATE, DAY_OF_MONTH, DAY_OF_WEEK, AM_PM, HOUR, HOUR_OF_DAY, MINUTE, SECOND, and MILLISECOND. Interval patterns when other calendar fields are different is not supported.

DateIntervalInfo objects are cloneable. When clients obtain a DateIntervalInfo object, they can feel free to modify it as necessary.

DateIntervalInfo are not expected to be subclassed. Data for a calendar is loaded out of resource bundles. Through ICU 4.4, date interval patterns are only supported in the Gregorian calendar; non-Gregorian calendars are supported from ICU 4.4.1.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo.PatternInfo` PatternInfo class saves the first and second part of interval pattern, and whether the interval pattern is earlier date first. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo#DateIntervalInfo(android.icu.util.ULocale)(locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` Construct DateIntervalInfo for the given locale, |
| `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo#DateIntervalInfo(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Construct DateIntervalInfo for the given `https://developer.android.com/reference/kotlin/java/util/Locale.html#`. |

| Public methods ||
|---|---|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo#clone()()` Clone this object. |
| open [DateIntervalInfo](DateIntervalInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo#cloneAsThawed()()` Provides for the clone operation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Override equals |
| --- | --- |
| open [DateIntervalInfo](DateIntervalInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo#freeze()()` Freezes the object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo#getDefaultOrder()()` Get default order -- whether the first date in pattern is later date or not. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo#getFallbackIntervalPattern()()` Get the fallback interval pattern. |
| --- | --- |
| open [DateIntervalInfo.PatternInfo](../android/icu/text/DateIntervalInfo.PatternInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo#getIntervalPattern(kotlin.String,%20kotlin.Int)(skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the interval pattern given the largest different calendar field. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo#hashCode()()` Override hashcode |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo#isFrozen()()` Determines whether the object has been frozen or not. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo#setFallbackIntervalPattern(kotlin.String)(fallbackPattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Re-set the fallback interval pattern. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo#setIntervalPattern(kotlin.String,%20kotlin.Int,%20kotlin.String)(skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, lrgDiffCalUnit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, intervalPattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Provides a way for client to build interval patterns. |

## Public constructors

### DateIntervalInfo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DateIntervalInfo(locale: ULocale!)
```

Construct DateIntervalInfo for the given locale,

| Parameters ||
|---|---|
| `locale` | [ULocale](../android.icu.util/ULocale.md)!: the interval patterns are loaded from the appropriate calendar data (specified calendar or default calendar) in this locale. |

### DateIntervalInfo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DateIntervalInfo(locale: Locale!)
```

Construct DateIntervalInfo for the given `https://developer.android.com/reference/kotlin/java/util/Locale.html#`.

| Parameters ||
|---|---|
| `locale` | [Locale](../java.util/Locale.md)!: the interval patterns are loaded from the appropriate calendar data (specified calendar or default calendar) in this locale. |

## Public methods

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): Any
```

Clone this object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a copy of the object |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### cloneAsThawed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cloneAsThawed(): DateIntervalInfo!
```

Provides for the clone operation. Any clone is initially unfrozen.

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Override equals

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### freeze

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun freeze(): DateIntervalInfo!
```

Freezes the object.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo#!` | the object itself. |

### getDefaultOrder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDefaultOrder(): Boolean
```

Get default order -- whether the first date in pattern is later date or not. return default date ordering in interval pattern. true if the first date in pattern is later date, false otherwise.

### getFallbackIntervalPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFallbackIntervalPattern(): String!
```

Get the fallback interval pattern.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | fallback interval pattern |

### getIntervalPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIntervalPattern(
    skeleton: String!, 
    field: Int
): DateIntervalInfo.PatternInfo!
```

Get the interval pattern given the largest different calendar field.

| Parameters ||
|---|---|
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the skeleton |
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the largest different calendar field |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo.PatternInfo!` | interval pattern return null if interval pattern is not found. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if getting interval pattern on a calendar field that is smaller than the MINIMUM_SUPPORTED_CALENDAR_FIELD |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Override hashcode

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isFrozen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isFrozen(): Boolean
```

Determines whether the object has been frozen or not.

### setFallbackIntervalPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFallbackIntervalPattern(fallbackPattern: String!): Unit
```

Re-set the fallback interval pattern. In construction, default fallback pattern is set as "{0} - {1}". And constructor taking locale as parameter will set the fallback pattern as what defined in the locale resource file. This method provides a way for user to replace the fallback pattern.

| Parameters ||
|---|---|
| `fallbackPattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: fall-back interval pattern. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if there is no pattern {0} or pattern {1} in fallbakckPattern |
| `java.lang.UnsupportedOperationException` | if the object is frozen |

### setIntervalPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIntervalPattern(
    skeleton: String!, 
    lrgDiffCalUnit: Int, 
    intervalPattern: String!
): Unit
```

Provides a way for client to build interval patterns. User could construct DateIntervalInfo by providing a list of skeletons and their patterns.

For example:

```kotlin
DateIntervalInfo dIntervalInfo = new DateIntervalInfo();
  dIntervalInfo.setIntervalPattern("yMd", Calendar.YEAR, "'from' yyyy-M-d 'to' yyyy-M-d");
  dIntervalInfo.setIntervalPattern("yMMMd", Calendar.MONTH, "'from' yyyy MMM d 'to' MMM d");
  dIntervalInfo.setIntervalPattern("yMMMd", Calendar.DAY, "yyyy MMM d-d");
  dIntervalInfo.setFallbackIntervalPattern("{0} ~ {1}");
  
```
Restriction: Currently, users can only set interval patterns when the following calendar fields are different: ERA, YEAR, MONTH, DATE, DAY_OF_MONTH, DAY_OF_WEEK, AM_PM, HOUR, HOUR_OF_DAY, MINUTE, SECOND, and MILLISECOND. Interval patterns when other calendar fields are different are not supported.

| Parameters ||
|---|---|
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the skeleton on which interval pattern based |
| `lrgDiffCalUnit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the largest different calendar unit. |
| `intervalPattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the interval pattern on the largest different calendar unit. For example, if lrgDiffCalUnit is "year", the interval pattern for en_US when year is different could be "'from' yyyy 'to' yyyy". |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if setting interval pattern on a calendar field that is smaller than the MINIMUM_SUPPORTED_CALENDAR_FIELD |
| `java.lang.UnsupportedOperationException` | if the object is frozen |

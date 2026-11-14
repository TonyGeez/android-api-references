Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DateTimePatternGenerator

```
open class DateTimePatternGenerator : Cloneable, Freezable<DateTimePatternGenerator!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.DateTimePatternGenerator](../android/icu/text/DateTimePatternGenerator.md) |

This class provides flexible generation of date format patterns, like "yy-MM-dd". The user can build up the generator by adding successive patterns. Once that is done, a query can be made using a "skeleton", which is a pattern which just includes the desired fields and lengths. The generator will return the "best fit" pattern corresponding to that skeleton.

The main method people will use is getBestPattern(String skeleton), since normally this class is pre-built with data from a particular locale. However, generators can be built directly from other data as well.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator.DisplayWidth` Field display name width constants for getFieldDisplayName |
| | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator.PatternInfo` PatternInfo supplies output parameters for addPattern(...). |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#DAY:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#DAYPERIOD:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#DAY_OF_WEEK_IN_MONTH:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#DAY_OF_YEAR:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#ERA:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#FRACTIONAL_SECOND:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#HOUR:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#MATCH_ALL_FIELDS_LENGTH:kotlin.Int` Option mask for forcing the width of all date and time fields. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#MATCH_HOUR_FIELD_LENGTH:kotlin.Int` Option mask for forcing the width of hour field. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#MATCH_NO_OPTIONS:kotlin.Int` Default option mask used for `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getBestPattern(kotlin.String,%20kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#replaceFieldTypes(kotlin.String,%20kotlin.String,%20kotlin.Int)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#MINUTE:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#MONTH:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#QUARTER:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#SECOND:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#WEEKDAY:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#WEEK_OF_MONTH:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#WEEK_OF_YEAR:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#YEAR:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#ZONE:kotlin.Int` <br /> |

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#DateTimePatternGenerator()()` Only for use by subclasses |

| Public methods ||
|---|---|
| open [DateTimePatternGenerator](../android/icu/text/DateTimePatternGenerator.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#addPattern(kotlin.String,%20kotlin.Boolean,%20android.icu.text.DateTimePatternGenerator.PatternInfo)(pattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, override: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, returnInfo: https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator.PatternInfo!)` Adds a pattern to the generator. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#clone()()` Returns a copy of this `DateTimePatternGenerator` object. |
| open [DateTimePatternGenerator](../android/icu/text/DateTimePatternGenerator.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#cloneAsThawed()()` Provides for the clone operation. |
| --- | --- |
| open [DateTimePatternGenerator](../android/icu/text/DateTimePatternGenerator.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#freeze()()` Freezes the object. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getAppendItemFormat(kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Getter corresponding to setAppendItemFormats. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getAppendItemName(kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Getter corresponding to setAppendItemName. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getBaseSkeleton(kotlin.String)(pattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Utility to return a unique base skeleton from a given pattern. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getBaseSkeletons(kotlin.collections.MutableSet)(result: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Return a list of all the base skeletons (in canonical form) from this class |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getBestPattern(kotlin.String)(skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Return the best pattern matching the input skeleton. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getBestPattern(kotlin.String,%20kotlin.Int)(skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, options: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the best pattern matching the input skeleton. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getDateTimeFormat()()` Getter corresponding to setDateTimeFormat. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getDateTimeFormat(kotlin.Int)(style: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Getter corresponding to setDateTimeFormat. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getDecimal()()` Getter corresponding to setDecimal. |
| open [DateFormat.HourCycle](../android/icu/text/DateFormat.HourCycle.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getDefaultHourCycle()()` Return the default hour cycle. |
| open static [DateTimePatternGenerator](../android/icu/text/DateTimePatternGenerator.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getEmptyInstance()()` Create empty generator, to be constructed with addPattern(...) etc. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getFieldDisplayName(kotlin.Int,%20android.icu.text.DateTimePatternGenerator.DisplayWidth)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, width: https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator.DisplayWidth!)` The general interface to get a display name for a particular date/time field, in one of several possible display widths. |
| open static [DateTimePatternGenerator](../android/icu/text/DateTimePatternGenerator.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getInstance()()` Construct a flexible generator according to data for the default `FORMAT` locale. |
| open static [DateTimePatternGenerator](../android/icu/text/DateTimePatternGenerator.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getInstance(android.icu.util.ULocale)(uLocale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` Construct a flexible generator according to data for a given locale. |
| --- | --- |
| open static [DateTimePatternGenerator](../android/icu/text/DateTimePatternGenerator.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getInstance(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Construct a flexible generator according to data for a given locale. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getSkeleton(kotlin.String)(pattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Utility to return a unique skeleton from a given pattern. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getSkeletons(kotlin.collections.MutableMap)(result: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Return a list of all the skeletons (in canonical form) from this class, and the patterns that they map to. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#isFrozen()()` Determines whether the object has been frozen or not. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#replaceFieldTypes(kotlin.String,%20kotlin.String)(pattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Adjusts the field types (width and subtype) of a pattern to match what is in a skeleton. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#replaceFieldTypes(kotlin.String,%20kotlin.String,%20kotlin.Int)(pattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, skeleton: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, options: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Adjusts the field types (width and subtype) of a pattern to match what is in a skeleton. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#setAppendItemFormat(kotlin.Int,%20kotlin.String)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` An AppendItem format is a pattern used to append a field if there is no good match. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#setAppendItemName(kotlin.Int,%20kotlin.String)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets the names of fields, eg "era" in English for ERA. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#setDateTimeFormat(kotlin.Int,%20kotlin.String)(style: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dateTimeFormat: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` dateTimeFormats are message patterns used to compose combinations of date and time patterns. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#setDateTimeFormat(kotlin.String)(dateTimeFormat: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` The date time format is a message format pattern used to compose date and time patterns. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#setDecimal(kotlin.String)(decimal: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` The decimal value is used in formatting fractions of seconds. |

## Constants

### DAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DAY: Int
```

 Value: 7

### DAYPERIOD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DAYPERIOD: Int
```

 Value: 10

### DAY_OF_WEEK_IN_MONTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DAY_OF_WEEK_IN_MONTH: Int
```

 Value: 9

### DAY_OF_YEAR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DAY_OF_YEAR: Int
```

 Value: 8

### ERA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERA: Int
```

 Value: 0

### FRACTIONAL_SECOND

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FRACTIONAL_SECOND: Int
```

 Value: 14

### HOUR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOUR: Int
```

 Value: 11

### MATCH_ALL_FIELDS_LENGTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_ALL_FIELDS_LENGTH: Int
```

Option mask for forcing the width of all date and time fields.

 Value: 65535

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getBestPattern(kotlin.String,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#replaceFieldTypes(kotlin.String,%20kotlin.String,%20kotlin.Int)`

### MATCH_HOUR_FIELD_LENGTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_HOUR_FIELD_LENGTH: Int
```

Option mask for forcing the width of hour field.

 Value: 2048

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getBestPattern(kotlin.String,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#replaceFieldTypes(kotlin.String,%20kotlin.String,%20kotlin.Int)`

### MATCH_NO_OPTIONS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_NO_OPTIONS: Int
```

Default option mask used for `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getBestPattern(kotlin.String,%20kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#replaceFieldTypes(kotlin.String,%20kotlin.String,%20kotlin.Int)`.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getBestPattern(kotlin.String,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#replaceFieldTypes(kotlin.String,%20kotlin.String,%20kotlin.Int)`

### MINUTE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MINUTE: Int
```

 Value: 12

### MONTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONTH: Int
```

 Value: 3

### QUARTER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUARTER: Int
```

 Value: 2

### SECOND

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SECOND: Int
```

 Value: 13

### WEEKDAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEEKDAY: Int
```

 Value: 6

### WEEK_OF_MONTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEEK_OF_MONTH: Int
```

 Value: 5

### WEEK_OF_YEAR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEEK_OF_YEAR: Int
```

 Value: 4

### YEAR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR: Int
```

 Value: 1

### ZONE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ZONE: Int
```

 Value: 15

## Protected constructors

### DateTimePatternGenerator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected DateTimePatternGenerator()
```

Only for use by subclasses

## Public methods

### addPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addPattern(
    pattern: String!, 
    override: Boolean, 
    returnInfo: DateTimePatternGenerator.PatternInfo!
): DateTimePatternGenerator!
```

Adds a pattern to the generator. If the pattern has the same skeleton as an existing pattern, and the override parameter is set, then the previous value is overridden. Otherwise, the previous value is retained. In either case, the conflicting information is returned in PatternInfo.

Note that single-field patterns (like "MMM") are automatically added, and don't need to be added explicitly!

Example code:

```kotlin
Date date= new GregorianCalendar(1999,9,13,23,58,59).getTime();
  ULocale locale = ULocale.FRANCE;
  // Create an DateTimePatternGenerator instance for the given locale
  DateTimePatternGenerator gen = DateTimePatternGenerator.getInstance(locale);
  SimpleDateFormat format = new SimpleDateFormat(gen.getBestPattern("MMMMddHmm"), locale);
  DateTimePatternGenerator.PatternInfo returnInfo = new DateTimePatternGenerator.PatternInfo();
  // Add '. von' to the existing pattern
  gen.addPattern("dd'. von' MMMM", true, returnInfo);
  // Apply the new pattern
  format.applyPattern(gen.getBestPattern("MMMMddHmm"));
  System.out.println("New Pattern for FRENCH: "+format.toPattern());
  System.out.println("Date Time in new Pattern: "+format.format(date));
 
  /** output of the sample code:
   **************************************************************************************************
   New Pattern for FRENCH: dd. 'von' MMMM HH:mm
   Date Time in new Pattern: 13. von octobre 23:58
   *************************************************************************************************<code>/</code>
```

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Pattern to add. |
| `override` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): When existing values are to be overridden use true, otherwise use false. |
| `returnInfo` | [DateTimePatternGenerator.PatternInfo](../android/icu/text/DateTimePatternGenerator.PatternInfo.md)!: Returned information. |
| --- | --- |

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): Any
```

Returns a copy of this `DateTimePatternGenerator` object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | A copy of this `DateTimePatternGenerator` object. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### cloneAsThawed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cloneAsThawed(): DateTimePatternGenerator!
```

Provides for the clone operation. Any clone is initially unfrozen.

### freeze

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun freeze(): DateTimePatternGenerator!
```

Freezes the object.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#!` | the object itself. |

### getAppendItemFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAppendItemFormat(field: Int): String!
```

Getter corresponding to setAppendItemFormats. Values below 0 or at or above TYPE_LIMIT are illegal arguments.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index to retrieve the append item formats. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | append pattern for field |

### getAppendItemName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAppendItemName(field: Int): String!
```

Getter corresponding to setAppendItemName. Values below 0 or at or above TYPE_LIMIT are illegal arguments. Note: The more general method for getting date/time field display names is getFieldDisplayName.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index to get the append item name. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | name for field |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator#getFieldDisplayName(kotlin.Int,%20android.icu.text.DateTimePatternGenerator.DisplayWidth)`

### getBaseSkeleton

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBaseSkeleton(pattern: String!): String!
```

Utility to return a unique base skeleton from a given pattern. This is the same as the skeleton, except that differences in length are minimized so as to only preserve the difference between string and numeric form. So for example, both "MMM-dd" and "d/MMM" produce the skeleton "MMMd" (notice the single d).

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Input pattern, such as "dd/MMM" |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | skeleton, such as "MMMdd" |

### getBaseSkeletons

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBaseSkeletons(result: MutableSet<String!>!): MutableSet<String!>!
```

Return a list of all the base skeletons (in canonical form) from this class

### getBestPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBestPattern(skeleton: String!): String!
```

Return the best pattern matching the input skeleton. It is guaranteed to have all of the fields in the skeleton.

Example code:

```kotlin
import java.util.Date;
 
  import android.icu.text.DateFormat;
  import android.icu.text.DateTimePatternGenerator;
  import android.icu.text.SimpleDateFormat;
  import android.icu.util.GregorianCalendar;
  import android.icu.util.TimeZone;
  import android.icu.util.ULocale;
  ...
  final String[] skeletons = {
          "yQQQQ", // year + full name of quarter, i.e., 4th quarter 1999
          "yMMMM", // year + full name of month, i.e., October 1999
          "MMMMd", // full name of month + day of the month, i.e., October 25
          "hhmm",  // 12-hour-cycle format, i.e., 1:32 PM
          "jjmm"   // preferred hour format for the given locale, i.e., 24-hour-cycle format for fr_FR
  };
  final ULocale[] locales = {
          new ULocale ("en_US"),
          new ULocale ("fr_FR"),
          new ULocale ("zh_CN"),
  };
  DateTimePatternGenerator dtfg = null;
  Date date= new GregorianCalendar(1999,9,13,23,58,59).getTime();
  System.out.printf("%-20s%-35s%-35s%-35s\n\n", "Skeleton", "en_US", "fr_FR","zh_CN");
  for (String skeleton:skeletons) {
      System.out.printf("%-20s", skeleton);
      for (ULocale locale:locales) {
          // create a DateTimePatternGenerator instance for given locale
          dtfg = DateTimePatternGenerator.getInstance(locale);
          // use getBestPattern method to get the best pattern for the given skeleton
          String pattern = dtfg.getBestPattern(skeleton);
          // Constructs a SimpleDateFormat with the best pattern generated above and the given locale
          SimpleDateFormat sdf = new SimpleDateFormat(pattern, locale);
          // Get the format of the given date
          System.out.printf("%-35s",sdf.format(date));
      }
      System.out.println("\n");
  }
  /** output of the sample code:
   *************************************************************************************************************
     Skeleton            en_US                              fr_FR                              zh_CN
     yQQQQ               4th quarter 1999                   4e trimestre 1999                  1999年第四季度
     yMMMM               October 1999                       octobre 1999                       1999年10月
     MMMMd               October 13                         13 octobre                         10月13日
     hhmm                11:58 PM                           11:58 PM                           下午11:58
     jjmm                11:58 PM                           23:58                              下午11:58
   **************************************************************************************************************<code>/</code>// Use DateTime.getPatternInstance to produce the same Date/Time format with predefined constant field value
  final String[] dtfskeleton = {
          DateFormat.YEAR_QUARTER, // year + full name of quarter, i.e., 4th quarter 1999
          DateFormat.YEAR_MONTH,   // year + full name of month, i.e., October 1999
          DateFormat.MONTH_DAY     // full name of month + day of the month, i.e., October 25
  };
  System.out.printf("%-20s%-35s%-35s%-35s\n\n", "Skeleton", "en_US", "fr_FR","zh_CN");
  for (String skeleton:dtfskeleton) {
      System.out.printf("%-20s", skeleton);
      for (ULocale locale:locales) {
          // Use DateFormat.getPatternInstance to get the date/time format for the locale,
          // and apply the format to the given date
          String df=DateFormat.getPatternInstance(skeleton,locale).format(date);
          System.out.printf("%-35s",df);
      }
      System.out.println("\n");
  }
 
  /** output of the sample code:
   ************************************************************************************************************
   Skeleton            en_US                              fr_FR                              zh_CN
   yQQQQ               4th quarter 1999                   4e trimestre 1999                  1999年第四季度
   yMMMM               October 1999                       octobre 1999                       1999年10月
   MMMMd               October 13                         13 octobre                         10月13日
   ************************************************************************************************************<code>/</code>
```

| Parameters ||
|---|---|
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The skeleton is a pattern containing only the variable fields. For example, "MMMdd" and "mmhh" are skeletons. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | Best pattern matching the input skeleton. |

### getBestPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBestPattern(
    skeleton: String!, 
    options: Int
): String!
```

Return the best pattern matching the input skeleton. It is guaranteed to have all of the fields in the skeleton.

| Parameters ||
|---|---|
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The skeleton is a pattern containing only the variable fields. For example, "MMMdd" and "mmhh" are skeletons. |
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): MATCH_xxx options for forcing the length of specified fields in the returned pattern to match those in the skeleton (when this would not happen otherwise). For default behavior, use MATCH_NO_OPTIONS. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | Best pattern matching the input skeleton (and options). |

### getDateTimeFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDateTimeFormat(): String!
```

Getter corresponding to setDateTimeFormat. There are four DateTimeFormats in a DateTimePatternGenerator object, corresponding to date styles DateFormat.FULL..DateFormat.SHORT. This method gets the style for DateFormat.MEDIUM (the default). To get them individually, see getDateTimeFormat(int style).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | pattern |

### getDateTimeFormat

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDateTimeFormat(style: Int): String!
```

Getter corresponding to setDateTimeFormat.

| Parameters ||
|---|---|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of DateFormat.FULL..DateFormat.SHORT. An exception will be thrown if out of range. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the current dateTimeFormat for the specified style. |

### getDecimal

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDecimal(): String!
```

Getter corresponding to setDecimal.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | string corresponding to the decimal point |

### getDefaultHourCycle

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDefaultHourCycle(): DateFormat.HourCycle!
```

Return the default hour cycle.

### getEmptyInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getEmptyInstance(): DateTimePatternGenerator!
```

Create empty generator, to be constructed with addPattern(...) etc.

### getFieldDisplayName

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFieldDisplayName(
    field: Int, 
    width: DateTimePatternGenerator.DisplayWidth!
): String!
```

The general interface to get a display name for a particular date/time field, in one of several possible display widths.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The field type, such as ERA. |
| `width` | [DateTimePatternGenerator.DisplayWidth](../android/icu/text/DateTimePatternGenerator.DisplayWidth.md)!: The desired DisplayWidth, such as DisplayWidth.ABBREVIATED. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The display name for the field |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(): DateTimePatternGenerator!
```

Construct a flexible generator according to data for the default `FORMAT` locale.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#`

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(uLocale: ULocale!): DateTimePatternGenerator!
```

Construct a flexible generator according to data for a given locale.

| Parameters ||
|---|---|
| `uLocale` | [ULocale](../android/icu/util/ULocale.md)!: The locale to pass. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(locale: Locale!): DateTimePatternGenerator!
```

Construct a flexible generator according to data for a given locale.

| Parameters ||
|---|---|
| `locale` | [Locale](../java/util/Locale.md)!: The `https://developer.android.com/reference/kotlin/java/util/Locale.html#` to pass. |

### getSkeleton

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSkeleton(pattern: String!): String!
```

Utility to return a unique skeleton from a given pattern. For example, both "MMM-dd" and "dd/MMM" produce the skeleton "MMMdd".

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Input pattern, such as "dd/MMM" |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | skeleton, such as "MMMdd" |

### getSkeletons

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSkeletons(result: MutableMap<String!, String!>!): MutableMap<String!, String!>!
```

Return a list of all the skeletons (in canonical form) from this class, and the patterns that they map to.

| Parameters ||
|---|---|
| `result` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: an output Map in which to place the mapping from skeleton to pattern. If you want to see the internal order being used, supply a LinkedHashMap. If the input value is null, then a LinkedHashMap is allocated. *Issue: an alternate API would be to just return a list of the skeletons, and then have a separate routine to get from skeleton to pattern.* |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | the input Map containing the values. |

### isFrozen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isFrozen(): Boolean
```

Determines whether the object has been frozen or not.

### replaceFieldTypes

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun replaceFieldTypes(
    pattern: String!, 
    skeleton: String!
): String!
```

Adjusts the field types (width and subtype) of a pattern to match what is in a skeleton. That is, if you supply a pattern like "d-M H:m", and a skeleton of "MMMMddhhmm", then the input pattern is adjusted to be "dd-MMMM hh:mm". This is used internally to get the best match for the input skeleton, but can also be used externally.

Example code:

```kotlin
Date date= new GregorianCalendar(1999,9,13,23,58,59).getTime();
  TimeZone zone = TimeZone.getTimeZone("Europe/Paris");
  ULocale locale = ULocale.FRANCE;
  DateTimePatternGenerator gen = DateTimePatternGenerator.getInstance(locale);
  SimpleDateFormat format = new SimpleDateFormat("EEEE d MMMM y HH:mm:ss zzzz",locale);
  format.setTimeZone(zone);
  String pattern = format.toPattern();
  System.out.println("Pattern before replacement:");
  System.out.println(pattern);
  System.out.println("Date/Time format in fr_FR:");
  System.out.println(format.format(date));
  // Replace zone "zzzz" in the pattern with "vvvv"
  String newPattern = gen.replaceFieldTypes(pattern, "vvvv");
  // Apply the new pattern
  format.applyPattern(newPattern);
  System.out.println("Pattern after replacement:");
  System.out.println(newPattern);
  System.out.println("Date/Time format in fr_FR:");
  System.out.println(format.format(date));
 
  /** output of the sample code:
  ***************************************************************************************************
   Pattern before replacement:
   EEEE d MMMM y HH:mm:ss zzzz
   Date/Time format in fr_FR:
   jeudi 14 octobre 1999 05:58:59 heure avancée d'Europe centrale
   Pattern after replacement:
   EEEE d MMMM y HH:mm:ss vvvv
   Date/Time format in fr_FR:
   jeudi 14 octobre 1999 05:58:59 heure de l'Europe centrale
 
  **************************************************************************************************<code>/</code>
```

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: input pattern |
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: For the pattern to match to. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | pattern adjusted to match the skeleton fields widths and subtypes. |

### replaceFieldTypes

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun replaceFieldTypes(
    pattern: String!, 
    skeleton: String!, 
    options: Int
): String!
```

Adjusts the field types (width and subtype) of a pattern to match what is in a skeleton. That is, if you supply a pattern like "d-M H:m", and a skeleton of "MMMMddhhmm", then the input pattern is adjusted to be "dd-MMMM hh:mm". This is used internally to get the best match for the input skeleton, but can also be used externally.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: input pattern |
| `skeleton` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: For the pattern to match to. |
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): MATCH_xxx options for forcing the length of specified fields in the returned pattern to match those in the skeleton (when this would not happen otherwise). For default behavior, use MATCH_NO_OPTIONS. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | pattern adjusted to match the skeleton fields widths and subtypes. |

### setAppendItemFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAppendItemFormat(
    field: Int, 
    value: String!
): Unit
```

An AppendItem format is a pattern used to append a field if there is no good match. For example, suppose that the input skeleton is "GyyyyMMMd", and there is no matching pattern internally, but there is a pattern matching "yyyyMMMd", say "d-MM-yyyy". Then that pattern is used, plus the G. The way these two are conjoined is by using the AppendItemFormat for G (era). So if that value is, say "{0}, {1}" then the final resulting pattern is "d-MM-yyyy, G".

There are actually three available variables: {0} is the pattern so far, {1} is the element we are adding, and {2} is the name of the element.

This reflects the way that the CLDR data is organized.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): such as ERA |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: pattern, such as "{0}, {1}" |

### setAppendItemName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAppendItemName(
    field: Int, 
    value: String!
): Unit
```

Sets the names of fields, eg "era" in English for ERA. These are only used if the corresponding AppendItemFormat is used, and if it contains a {2} variable.

This reflects the way that the CLDR data is organized.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Index of the append item names. |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The value to set the item to. |

### setDateTimeFormat

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDateTimeFormat(
    style: Int, 
    dateTimeFormat: String!
): Unit
```

dateTimeFormats are message patterns used to compose combinations of date and time patterns. There are four length styles, corresponding to the inferred style of the date pattern: - DateFormat.FULL (for date pattern with weekday and long month), else - DateFormat.LONG (for a date pattern with long month), else - DateFormat.MEDIUM (for a date pattern with abbreviated month), else - DateFormat.SHORT (for any other date pattern). For details on dateTimeFormats, see https://www.unicode.org/reports/tr35/tr35-dates.html#dateTimeFormats. The default pattern in the root locale for all styles is "{1} {0}".

| Parameters ||
|---|---|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of DateFormat.FULL..DateFormat.SHORT. An exception will be thrown if out of range. |
| `dateTimeFormat` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the new dateTimeFormat to set for the specified style |

### setDateTimeFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDateTimeFormat(dateTimeFormat: String!): Unit
```

The date time format is a message format pattern used to compose date and time patterns. The default value is "{1} {0}", where {1} will be replaced by the date pattern and {0} will be replaced by the time pattern.

This is used when the input skeleton contains both date and time fields, but there is not a close match among the added patterns. For example, suppose that this object was created by adding "dd-MMM" and "hh:mm", and its datetimeFormat is the default "{1} {0}". Then if the input skeleton is "MMMdhmm", there is not an exact match, so the input skeleton is broken up into two components "MMMd" and "hmm". There are close matches for those two skeletons, so the result is put together with this pattern, resulting in "d-MMM h:mm". There are four DateTimeFormats in a DateTimePatternGenerator object, corresponding to date styles DateFormat.FULL..DateFormat.SHORT. This method sets all of them to the specified pattern. To set them individually, see setDateTimeFormat(int style, ...).

| Parameters ||
|---|---|
| `dateTimeFormat` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: message format pattern, where {1} will be replaced by the date pattern and {0} will be replaced by the time pattern. |

### setDecimal

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDecimal(decimal: String!): Unit
```

The decimal value is used in formatting fractions of seconds. If the skeleton contains fractional seconds, then this is used with the fractional seconds. For example, suppose that the input pattern is "hhmmssSSSS", and the best matching pattern internally is "H:mm:ss", and the decimal string is ",". Then the resulting pattern is modified to be "H:mm:ss,SSSS"

| Parameters ||
|---|---|
| `decimal` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The decimal to set to. |

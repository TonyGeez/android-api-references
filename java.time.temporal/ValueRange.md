# ValueRange

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ValueRange

```
class ValueRange : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.time.temporal.ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#) |

The range of valid values for a date-time field.

All [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField) instances have a valid range of values. For example, the ISO day-of-month runs from 1 to somewhere between 28 and 31. This class captures that valid range.

It is important to be aware of the limitations of this class. Only the minimum and maximum values are provided. It is possible for there to be invalid values within the outer range. For example, a weird field may have valid values of 1, 2, 4, 6, 7, thus have a range of '1 - 7', despite that fact that values 3 and 5 are invalid.

Instances of this class are not tied to a specific field.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [checkValidIntValue](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#checkValidIntValue(kotlin.Long,%20java.time.temporal.TemporalField))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!`)` Checks that the specified value is valid and fits in an`int`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [checkValidValue](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#checkValidValue(kotlin.Long,%20java.time.temporal.TemporalField))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `field:` ` [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!`)` Checks that the specified value is valid. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Checks if this range is equal to another range. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLargestMinimum](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#getLargestMinimum())`()` Gets the largest possible minimum value that the field can take. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMaximum](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#getMaximum())`()` Gets the maximum value that the field can take. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMinimum](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#getMinimum())`()` Gets the minimum value that the field can take. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getSmallestMaximum](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#getSmallestMaximum())`()` Gets the smallest possible maximum value that the field can take. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#hashCode())`()` A hash code for this range. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFixed](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#isFixed())`()` Is the value range fixed and fully known. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isIntValue](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#isIntValue())`()` Checks if all values in the range fit in an`int`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValidIntValue](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#isValidIntValue(kotlin.Long))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Checks if the value is within the valid range and that all values in the range fit in an`int`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValidValue](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#isValidValue(kotlin.Long))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Checks if the value is within the valid range. |
| static [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#)! | [of](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#of(kotlin.Long,%20kotlin.Long))`(`min:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `max:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Obtains a fixed value range. |
| static [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#)! | [of](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#of(kotlin.Long,%20kotlin.Long,%20kotlin.Long))`(`min:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `maxSmallest:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `maxLargest:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Obtains a variable value range. |
| static [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#)! | [of](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#of(kotlin.Long,%20kotlin.Long,%20kotlin.Long,%20kotlin.Long))`(`minSmallest:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `minLargest:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `maxSmallest:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `maxLargest:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Obtains a fully variable value range. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#toString())`()` Outputs this range as a`String`. |

## Public methods

### checkValidIntValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun checkValidIntValue(
    value: Long, 
    field: TemporalField!
): Int
```

Checks that the specified value is valid and fits in an`int`.

This validates that the value is within the valid range of values and that all valid values are within the bounds of an`int`. The field is only used to improve the error message.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value to check |
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!:the field being checked, may be null |

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value that was passed in |

**See Also**

- [#isValidIntValue(long)](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#isValidIntValue(kotlin.Long)) 

### checkValidValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun checkValidValue(
    value: Long, 
    field: TemporalField!
): Long
```

Checks that the specified value is valid.

This validates that the value is within the valid range of values. The field is only used to improve the error message.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value to check |
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!:the field being checked, may be null |

| Return ||
|------------------------------------------------------------------------------|------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value that was passed in |

**See Also**

- [#isValidValue(long)](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#isValidValue(kotlin.Long)) 

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Checks if this range is equal to another range.

The comparison is based on the four values, minimum, largest minimum, smallest maximum and maximum. Only objects of type`ValueRange`are compared, other types return false.

| Parameters ||
|-------|-----------------------------------------|
| `obj` | the object to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this is equal to the other range |

### getLargestMinimum

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLargestMinimum(): Long
```

Gets the largest possible minimum value that the field can take.

For example, the ISO day-of-month always starts at 1. The largest minimum is therefore 1.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the largest possible minimum value for this field |

### getMaximum

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaximum(): Long
```

Gets the maximum value that the field can take.

For example, the ISO day-of-month runs to between 28 and 31 days. The maximum is therefore 31.

| Return ||
|------------------------------------------------------------------------------|----------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the maximum value for this field |

### getMinimum

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMinimum(): Long
```

Gets the minimum value that the field can take.

For example, the ISO day-of-month always starts at 1. The minimum is therefore 1.

| Return ||
|------------------------------------------------------------------------------|----------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the minimum value for this field |

### getSmallestMaximum

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSmallestMaximum(): Long
```

Gets the smallest possible maximum value that the field can take.

For example, the ISO day-of-month runs to between 28 and 31 days. The smallest maximum is therefore 28.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the smallest possible maximum value for this field |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

A hash code for this range.

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a suitable hash code |

### isFixed

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isFixed(): Boolean
```

Is the value range fixed and fully known.

For example, the ISO day-of-month runs from 1 to between 28 and 31. Since there is uncertainty about the maximum value, the range is not fixed. However, for the month of January, the range is always 1 to 31, thus it is fixed.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the set of values is fixed |

### isIntValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isIntValue(): Boolean
```

Checks if all values in the range fit in an`int`.

This checks that all valid values are within the bounds of an`int`.

For example, the ISO month-of-year has values from 1 to 12, which fits in an`int`. By comparison, ISO nano-of-day runs from 1 to 86,400,000,000,000 which does not fit in an`int`.

This implementation uses [getMinimum()](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#getMinimum())and [getMaximum()](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#getMaximum()).

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if a valid value always fits in an`int` |

### isValidIntValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isValidIntValue(value: Long): Boolean
```

Checks if the value is within the valid range and that all values in the range fit in an`int`.

This method combines [isIntValue()](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#isIntValue())and [isValidValue(long)](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#isValidValue(kotlin.Long)).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value to check |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the value is valid and fits in an`int` |

### isValidValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isValidValue(value: Long): Boolean
```

Checks if the value is within the valid range.

This checks that the value is within the stored range of values.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value to check |

| Return ||
|------------------------------------------------------------------------------------|----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the value is valid |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(
    min: Long, 
    max: Long
): ValueRange!
```

Obtains a fixed value range.

This factory obtains a range where the minimum and maximum values are fixed. For example, the ISO month-of-year always runs from 1 to 12.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------|
| `min` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the minimum value |
| `max` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum value |

| Return ||
|----------------------------------------------------------------------------------------------|---------------------------------------|
| [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#)! | the ValueRange for min, max, not null |

| Exceptions ||
|--------------------------------------|--------------------------------------------|
| `java.lang.IllegalArgumentException` | if the minimum is greater than the maximum |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(
    min: Long, 
    maxSmallest: Long, 
    maxLargest: Long
): ValueRange!
```

Obtains a variable value range.

This factory obtains a range where the minimum value is fixed and the maximum value may vary. For example, the ISO day-of-month always starts at 1, but ends between 28 and 31.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------|
| `min` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the minimum value |
| `maxSmallest` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the smallest maximum value |
| `maxLargest` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the largest maximum value |

| Return ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#)! | the ValueRange for min, smallest max, largest max, not null |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the minimum is greater than the smallest maximum, or the smallest maximum is greater than the largest maximum |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(
    minSmallest: Long, 
    minLargest: Long, 
    maxSmallest: Long, 
    maxLargest: Long
): ValueRange!
```

Obtains a fully variable value range.

This factory obtains a range where both the minimum and maximum value may vary.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------|
| `minSmallest` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the smallest minimum value |
| `minLargest` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the largest minimum value |
| `maxSmallest` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the smallest maximum value |
| `maxLargest` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the largest maximum value |

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange#)! | the ValueRange for smallest min, largest min, smallest max, largest max, not null |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the smallest minimum is greater than the smallest maximum, or the smallest maximum is greater than the largest maximum, or the largest minimum is greater than the largest maximum, or the smallest minimum is greater than the largest minimum |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Outputs this range as a`String`.

The format will be '{min}/{largestMin} - {smallestMax}/{max}', where the largestMin or smallestMax sections may be omitted, together with associated slash, if they are the same as the min or max.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this range, not null |

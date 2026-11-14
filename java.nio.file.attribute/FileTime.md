Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileTime

```
class FileTime : Comparable<FileTime!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.file.attribute.FileTime](FileTime.md) |

Represents the value of a file's time stamp attribute. For example, it may represent the time that the file was last `https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#lastModifiedTime()`, `https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#lastAccessTime()`, or `https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#creationTime()`.

Instances of this class are immutable.

## Summary

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime#compareTo(java.nio.file.attribute.FileTime)(other: https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime#!)` Compares the value of two `FileTime` objects for order. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Tests this `FileTime` for equality with the given object. |
| static [FileTime](FileTime.md)! | `https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime#from(java.time.Instant)(instant: https://developer.android.com/reference/kotlin/java/time/Instant.html#!)` Returns a `FileTime` representing the same point of time value on the time-line as the provided `Instant` object. |
| --- | --- |
| static [FileTime](FileTime.md)! | `https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime#from(kotlin.Long,%20java.util.concurrent.TimeUnit)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html#!)` Returns a `FileTime` representing a value at the given unit of granularity. |
| static [FileTime](FileTime.md)! | `https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime#fromMillis(kotlin.Long)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a `FileTime` representing the given value in milliseconds. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime#hashCode()()` Computes a hash code for this file time. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime#to(java.util.concurrent.TimeUnit)(unit: https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html#!)` Returns the value at the given unit of granularity. |
| [Instant](../java.time/Instant.md)! | `https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime#toInstant()()` Converts this `FileTime` object to an `Instant`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime#toMillis()()` Returns the value in milliseconds. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime#toString()()` Returns the string representation of this `FileTime`. |

## Public methods

### compareTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareTo(other: FileTime!): Int
```

Compares the value of two `FileTime` objects for order.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `other` | [FileTime](FileTime.md)!: the other `FileTime` to be compared |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `0` if this `FileTime` is equal to `other`, a value less than 0 if this `FileTime` represents a time that is before `other`, and a value greater than 0 if this `FileTime` represents a time that is after `other` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Tests this `FileTime` for equality with the given object.

The result is `true` if and only if the argument is not `null` and is a `FileTime` that represents the same time. This method satisfies the general contract of the `Object.equals` method.

| Parameters ||
|---|---|
| `obj` | the object to compare with |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if, and only if, the given object is a `FileTime` that represents the same time |

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun from(instant: Instant!): FileTime!
```

Returns a `FileTime` representing the same point of time value on the time-line as the provided `Instant` object.

| Parameters ||
|---|---|
| `instant` | [Instant](../java.time/Instant.md)!: the instant to convert |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime#!` | a `FileTime` representing the same point on the time-line as the provided instant |

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun from(
    value: Long, 
    unit: TimeUnit!
): FileTime!
```

Returns a `FileTime` representing a value at the given unit of granularity.

| Parameters ||
|---|---|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the value since the epoch (1970-01-01T00:00:00Z); can be negative |
| `unit` | [TimeUnit](../java.util.concurrent/TimeUnit.md)!: the unit of granularity to interpret the value |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime#!` | a `FileTime` representing the given value |

### fromMillis

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fromMillis(value: Long): FileTime!
```

Returns a `FileTime` representing the given value in milliseconds.

| Parameters ||
|---|---|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the value, in milliseconds, since the epoch (1970-01-01T00:00:00Z); can be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime#!` | a `FileTime` representing the given value |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Computes a hash code for this file time.

The hash code is based upon the value represented, and satisfies the general contract of the `https://developer.android.com/reference/kotlin/java/lang/Object.html#hashCode()` method.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the hash-code value |

### to

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun to(unit: TimeUnit!): Long
```

Returns the value at the given unit of granularity.

Conversion from a coarser granularity that would numerically overflow saturate to `Long.MIN_VALUE` if negative or `Long.MAX_VALUE` if positive.

| Parameters ||
|---|---|
| `unit` | [TimeUnit](../java.util.concurrent/TimeUnit.md)!: the unit of granularity for the return value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | value in the given unit of granularity, since the epoch since the epoch (1970-01-01T00:00:00Z); can be negative |

### toInstant

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toInstant(): Instant!
```

Converts this `FileTime` object to an `Instant`.

The conversion creates an `Instant` that represents the same point on the time-line as this `FileTime`.

`FileTime` can store points on the time-line further in the future and further in the past than `Instant`. Conversion from such further time points saturates to `https://developer.android.com/reference/kotlin/java/time/Instant.html#MIN:java.time.Instant` if earlier than `Instant.MIN` or `https://developer.android.com/reference/kotlin/java/time/Instant.html#MAX:java.time.Instant` if later than `Instant.MAX`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#!` | an instant representing the same point on the time-line as this `FileTime` object |

### toMillis

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toMillis(): Long
```

Returns the value in milliseconds.

Conversion from a coarser granularity that would numerically overflow saturate to `Long.MIN_VALUE` if negative or `Long.MAX_VALUE` if positive.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the value in milliseconds, since the epoch (1970-01-01T00:00:00Z) |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns the string representation of this `FileTime`. The string is returned in the [ISO 8601](http://www.w3.org/TR/NOTE-datetime) format:

```kotlin
YYYY-MM-DDThh:mm:ss[.s+]Z
  
```
where "`[.s+]`" represents a dot followed by one of more digits for the decimal fraction of a second. It is only present when the decimal fraction of a second is not zero. For example, `FileTime.fromMillis(1234567890000L).toString()` yields `"2009-02-13T23:31:30Z"`, and `FileTime.fromMillis(1234567890123L).toString()` yields `"2009-02-13T23:31:30.123Z"`.

<br />

A `FileTime` is primarily intended to represent the value of a file's time stamp. Where used to represent *extreme values* , where the year is less than "`0001`" or greater than "`9999`" then this method deviates from ISO 8601 in the same manner as the [XML Schema language](http://www.w3.org/TR/xmlschema-2/#deviantformats). That is, the year may be expanded to more than four digits and may be negative-signed. If more than four digits then leading zeros are not present. The year before "`0001`" is "`-0001`".

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the string representation of this file time |

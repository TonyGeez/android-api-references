# TimeInstantRangeFilter

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TimeInstantRangeFilter

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/TimeInstantRangeFilter "View this page in Java") 
| --- | --- |

```
class TimeInstantRangeFilter : TimeRangeFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.TimeInstantRangeFilter](https://developer.android.com/reference/kotlin/android/health/connect/TimeInstantRangeFilter#) |

Specification of time range for read and delete requests. Internally represents a SQLLite argument that specifies start and end time to put in as SQLLite parameters. The filter must be bound at least at one of the ends, i.e., either the start or end time must be set, or else an IllegalArgumentException is thrown.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/health/connect/TimeInstantRangeFilter.Builder) Builder class for [TimeInstantRangeFilter](https://developer.android.com/reference/kotlin/android/health/connect/TimeInstantRangeFilter#) |

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/health/connect/TimeInstantRangeFilter#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | [getEndTime](https://developer.android.com/reference/kotlin/android/health/connect/TimeInstantRangeFilter#getEndTime())`()` <br /> |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | [getStartTime](https://developer.android.com/reference/kotlin/android/health/connect/TimeInstantRangeFilter#getStartTime())`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/health/connect/TimeInstantRangeFilter#hashCode())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBounded](https://developer.android.com/reference/kotlin/android/health/connect/TimeInstantRangeFilter#isBounded())`()` <br /> |

## Public methods

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getEndTime

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEndTime(): Instant?
```

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | end time instant of this filter This value may be`null`. |

### getStartTime

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStartTime(): Instant?
```

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | start time instant of this filter This value may be`null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isBounded

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isBounded(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a boolean value indicating if the filter is bound or not. This value cannot be`null`. |

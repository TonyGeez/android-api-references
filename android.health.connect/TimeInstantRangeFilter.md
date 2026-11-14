# TimeInstantRangeFilter

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TimeInstantRangeFilter

Kotlin| [Java](../android/health/connect/TimeInstantRangeFilter.md) 
| --- | --- |

```
class TimeInstantRangeFilter : TimeRangeFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.TimeInstantRangeFilter](../android/health/connect/TimeInstantRangeFilter.md) |

Specification of time range for read and delete requests. Internally represents a SQLLite argument that specifies start and end time to put in as SQLLite parameters. The filter must be bound at least at one of the ends, i.e., either the start or end time must be set, or else an IllegalArgumentException is thrown.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/health/connect/TimeInstantRangeFilter.Builder.md) Builder class for [TimeInstantRangeFilter](../android/health/connect/TimeInstantRangeFilter.md) |

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/health/connect/TimeInstantRangeFilter.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Instant](../java/time/Instant.md)? | [getEndTime](../android/health/connect/TimeInstantRangeFilter.md))`()` <br /> |
| [Instant](../java/time/Instant.md)? | [getStartTime](../android/health/connect/TimeInstantRangeFilter.md))`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/health/connect/TimeInstantRangeFilter.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBounded](../android/health/connect/TimeInstantRangeFilter.md))`()` <br /> |

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
| [Instant](../java/time/Instant.md)? | end time instant of this filter This value may be`null`. |

### getStartTime

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStartTime(): Instant?
```

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Instant](../java/time/Instant.md)? | start time instant of this filter This value may be`null`. |

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

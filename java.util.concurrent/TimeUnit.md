# TimeUnit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TimeUnit

```
class TimeUnit
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.util.concurrent.TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#)\> ||
| | ↳ | [java.util.concurrent.TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#) |

| Known Direct Subclasses [TimeUnit.DAYS](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#ENUM_VALUE:DAYS), [TimeUnit.HOURS](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#ENUM_VALUE:HOURS), [TimeUnit.MICROSECONDS](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#ENUM_VALUE:MICROSECONDS), [TimeUnit.MILLISECONDS](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#ENUM_VALUE:MILLISECONDS), [TimeUnit.MINUTES](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#ENUM_VALUE:MINUTES), [TimeUnit.NANOSECONDS](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#ENUM_VALUE:NANOSECONDS), [TimeUnit.SECONDS](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#ENUM_VALUE:SECONDS) |-------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------| | [TimeUnit.DAYS](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#ENUM_VALUE:DAYS) | Time unit representing twenty four hours. | | [TimeUnit.HOURS](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#ENUM_VALUE:HOURS) | Time unit representing sixty minutes. | | [TimeUnit.MICROSECONDS](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#ENUM_VALUE:MICROSECONDS) | Time unit representing one thousandth of a millisecond. | | [TimeUnit.MILLISECONDS](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#ENUM_VALUE:MILLISECONDS) | Time unit representing one thousandth of a second. | | [TimeUnit.MINUTES](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#ENUM_VALUE:MINUTES) | Time unit representing sixty seconds. | | [TimeUnit.NANOSECONDS](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#ENUM_VALUE:NANOSECONDS) | Time unit representing one thousandth of a microsecond. | | [TimeUnit.SECONDS](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#ENUM_VALUE:SECONDS) | Time unit representing one second. | |

A represents time durations at a given unit of granularity and provides utility methods to convert across units, and to perform timing and delay operations in these units. A does not maintain time information, but only helps organize and use time representations that may be maintained separately across various contexts. A nanosecond is defined as one thousandth of a microsecond, a microsecond as one thousandth of a millisecond, a millisecond as one thousandth of a second, a minute as sixty seconds, an hour as sixty minutes, and a day as twenty four hours.

A`TimeUnit`is mainly used to inform time-based methods how a given timing parameter should be interpreted. For example, the following code will timeout in 50 milliseconds if the is not available: 

```kotlin
<code>Lock lock = ...;
  if (lock.tryLock(50L, TimeUnit.MILLISECONDS)) ...</code>
```
while this code will timeout in 50 seconds: 

```kotlin
<code>Lock lock = ...;
  if (lock.tryLock(50L, TimeUnit.SECONDS)) ...</code>
```
Note however, that there is no guarantee that a particular timeout implementation will be able to notice the passage of time at the same granularity as the given`TimeUnit`.

## Summary

| Enum values ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DAYS](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#ENUM_VALUE:DAYS) Time unit representing twenty four hours. |
| [HOURS](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#ENUM_VALUE:HOURS) Time unit representing sixty minutes. |
| [MICROSECONDS](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#ENUM_VALUE:MICROSECONDS) Time unit representing one thousandth of a millisecond. |
| [MILLISECONDS](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#ENUM_VALUE:MILLISECONDS) Time unit representing one thousandth of a second. |
| [MINUTES](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#ENUM_VALUE:MINUTES) Time unit representing sixty seconds. |
| [NANOSECONDS](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#ENUM_VALUE:NANOSECONDS) Time unit representing one thousandth of a microsecond. |
| [SECONDS](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#ENUM_VALUE:SECONDS) Time unit representing one second. |

| Public methods ||
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [convert](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#convert(java.time.Duration))`(`duration:` ` [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#)!`)` Converts the given time duration to this unit. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [convert](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#convert(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`sourceDuration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `sourceUnit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#)!`)` Converts the given time duration in the given unit to this unit. |
| static [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#)! | [of](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#of(java.time.temporal.ChronoUnit))`(`chronoUnit:` ` [ChronoUnit](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit.html#)!`)` Converts a`ChronoUnit`to the equivalent`TimeUnit`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sleep](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#sleep(kotlin.Long))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Performs a [Thread.sleep](https://developer.android.com/reference/kotlin/java/lang/Thread.html#sleep(kotlin.Long,%20kotlin.Int))using this time unit. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [timedJoin](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#timedJoin(java.lang.Thread,%20kotlin.Long))`(`thread:` ` [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Performs a timed [Thread.join](https://developer.android.com/reference/kotlin/java/lang/Thread.html#join(kotlin.Long,%20kotlin.Int))using this time unit. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [timedWait](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#timedWait(kotlin.Any,%20kotlin.Long))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Performs a timed [Object.wait](https://developer.android.com/reference/kotlin/java/lang/Object.html#wait(kotlin.Long,%20kotlin.Int))using this time unit. |
| [ChronoUnit](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit.html#)! | [toChronoUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#toChronoUnit())`()` Converts this`TimeUnit`to the equivalent`ChronoUnit`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toDays](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#toDays(kotlin.Long))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Equivalent to [DAYS.convert(duration, this)](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#convert(kotlin.Long,%20java.util.concurrent.TimeUnit)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toHours](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#toHours(kotlin.Long))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Equivalent to [HOURS.convert(duration, this)](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#convert(kotlin.Long,%20java.util.concurrent.TimeUnit)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toMicros](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#toMicros(kotlin.Long))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Equivalent to [MICROSECONDS.convert(duration, this)](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#convert(kotlin.Long,%20java.util.concurrent.TimeUnit)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toMillis](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#toMillis(kotlin.Long))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Equivalent to [MILLISECONDS.convert(duration, this)](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#convert(kotlin.Long,%20java.util.concurrent.TimeUnit)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toMinutes](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#toMinutes(kotlin.Long))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Equivalent to [MINUTES.convert(duration, this)](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#convert(kotlin.Long,%20java.util.concurrent.TimeUnit)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toNanos](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#toNanos(kotlin.Long))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Equivalent to [NANOSECONDS.convert(duration, this)](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#convert(kotlin.Long,%20java.util.concurrent.TimeUnit)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toSeconds](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#toSeconds(kotlin.Long))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Equivalent to [SECONDS.convert(duration, this)](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#convert(kotlin.Long,%20java.util.concurrent.TimeUnit)). |

## Enum values

### DAYS

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val DAYS : TimeUnit
```

Time unit representing twenty four hours. 

### HOURS

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val HOURS : TimeUnit
```

Time unit representing sixty minutes. 

### MICROSECONDS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val MICROSECONDS : TimeUnit
```

Time unit representing one thousandth of a millisecond. 

### MILLISECONDS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val MILLISECONDS : TimeUnit
```

Time unit representing one thousandth of a second. 

### MINUTES

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val MINUTES : TimeUnit
```

Time unit representing sixty seconds. 

### NANOSECONDS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val NANOSECONDS : TimeUnit
```

Time unit representing one thousandth of a microsecond. 

### SECONDS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SECONDS : TimeUnit
```

Time unit representing one second.

## Public methods

### convert

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun convert(duration: Duration!): Long
```

Converts the given time duration to this unit.

For any TimeUnit`unit`,`unit.convert(Duration.ofNanos(n))`is equivalent to`unit.convert(n, NANOSECONDS)`, and`unit.convert(Duration.of(n, unit.toChronoUnit()))`is equivalent to`n`(in the absence of overflow).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------|
| `duration` | [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#)!:the time duration |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the converted duration in this unit, or`Long.MIN_VALUE`if conversion would negatively overflow, or`Long.MAX_VALUE`if it would positively overflow. |

| Exceptions ||
|----------------------------------|---------------------|
| `java.lang.NullPointerException` | if`duration`is null |

**See Also**

### convert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun convert(
    sourceDuration: Long, 
    sourceUnit: TimeUnit!
): Long
```

Converts the given time duration in the given unit to this unit. Conversions from finer to coarser granularities truncate, so lose precision. For example, converting`999`milliseconds to seconds results in`0`. Conversions from coarser to finer granularities with arguments that would numerically overflow saturate to`Long.MIN_VALUE`if negative or`Long.MAX_VALUE`if positive.

For example, to convert 10 minutes to milliseconds, use:`TimeUnit.MILLISECONDS.convert(10L, TimeUnit.MINUTES)`

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `sourceDuration` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time duration in the given`sourceUnit` |
| `sourceUnit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#)!:the unit of the`sourceDuration`argument |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the converted duration in this unit, or`Long.MIN_VALUE`if conversion would negatively overflow, or`Long.MAX_VALUE`if it would positively overflow. |

### of

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(chronoUnit: ChronoUnit!): TimeUnit!
```

Converts a`ChronoUnit`to the equivalent`TimeUnit`.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------|
| `chronoUnit` | [ChronoUnit](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit.html#)!:the ChronoUnit to convert |

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------|
| [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#)! | the converted equivalent TimeUnit |

| Exceptions ||
|--------------------------------------|------------------------------------------|
| `java.lang.IllegalArgumentException` | if`chronoUnit`has no equivalent TimeUnit |
| `java.lang.NullPointerException` | if`chronoUnit`is null |

### sleep

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sleep(timeout: Long): Unit
```

Performs a [Thread.sleep](https://developer.android.com/reference/kotlin/java/lang/Thread.html#sleep(kotlin.Long,%20kotlin.Int))using this time unit. This is a convenience method that converts time arguments into the form required by the`Thread.sleep`method.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the minimum time to sleep. If less than or equal to zero, do not sleep at all. |

| Exceptions ||
|----------------------------------|-------------------------------|
| `java.lang.InterruptedException` | if interrupted while sleeping |

### timedJoin

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun timedJoin(
    thread: Thread!, 
    timeout: Long
): Unit
```

Performs a timed [Thread.join](https://developer.android.com/reference/kotlin/java/lang/Thread.html#join(kotlin.Long,%20kotlin.Int))using this time unit. This is a convenience method that converts time arguments into the form required by the`Thread.join`method.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `thread` | [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!:the thread to wait for |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait. If less than or equal to zero, do not wait at all. |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### timedWait

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun timedWait(
    obj: Any!, 
    timeout: Long
): Unit
```

Performs a timed [Object.wait](https://developer.android.com/reference/kotlin/java/lang/Object.html#wait(kotlin.Long,%20kotlin.Int))using this time unit. This is a convenience method that converts timeout arguments into the form required by the`Object.wait`method.

For example, you could implement a blocking`poll`method (see [BlockingQueue.poll](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#poll(kotlin.Long,%20java.util.concurrent.TimeUnit))) using: 

```kotlin
<code>public E poll(long timeout, TimeUnit unit)
      throws InterruptedException {
    synchronized (lock) {
      while (isEmpty()) {
        unit.timedWait(lock, timeout);
        ...
      }
    }
  }</code>
```

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the object to wait on |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait. If less than or equal to zero, do not wait at all. |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### toChronoUnit

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toChronoUnit(): ChronoUnit!
```

Converts this`TimeUnit`to the equivalent`ChronoUnit`.

| Return ||
|---------------------------------------------------------------------------------------------------|-------------------------------------|
| [ChronoUnit](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit.html#)! | the converted equivalent ChronoUnit |

### toDays

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toDays(duration: Long): Long
```

Equivalent to [DAYS.convert(duration, this)](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#convert(kotlin.Long,%20java.util.concurrent.TimeUnit)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------|
| `duration` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the duration |

| Return ||
|------------------------------------------------------------------------------|------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the converted duration |

### toHours

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toHours(duration: Long): Long
```

Equivalent to [HOURS.convert(duration, this)](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#convert(kotlin.Long,%20java.util.concurrent.TimeUnit)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------|
| `duration` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the duration |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the converted duration, or`Long.MIN_VALUE`if conversion would negatively overflow, or`Long.MAX_VALUE`if it would positively overflow. |

### toMicros

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toMicros(duration: Long): Long
```

Equivalent to [MICROSECONDS.convert(duration, this)](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#convert(kotlin.Long,%20java.util.concurrent.TimeUnit)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------|
| `duration` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the duration |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the converted duration, or`Long.MIN_VALUE`if conversion would negatively overflow, or`Long.MAX_VALUE`if it would positively overflow. |

### toMillis

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toMillis(duration: Long): Long
```

Equivalent to [MILLISECONDS.convert(duration, this)](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#convert(kotlin.Long,%20java.util.concurrent.TimeUnit)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------|
| `duration` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the duration |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the converted duration, or`Long.MIN_VALUE`if conversion would negatively overflow, or`Long.MAX_VALUE`if it would positively overflow. |

### toMinutes

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toMinutes(duration: Long): Long
```

Equivalent to [MINUTES.convert(duration, this)](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#convert(kotlin.Long,%20java.util.concurrent.TimeUnit)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------|
| `duration` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the duration |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the converted duration, or`Long.MIN_VALUE`if conversion would negatively overflow, or`Long.MAX_VALUE`if it would positively overflow. |

### toNanos

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toNanos(duration: Long): Long
```

Equivalent to [NANOSECONDS.convert(duration, this)](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#convert(kotlin.Long,%20java.util.concurrent.TimeUnit)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------|
| `duration` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the duration |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the converted duration, or`Long.MIN_VALUE`if conversion would negatively overflow, or`Long.MAX_VALUE`if it would positively overflow. |

### toSeconds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toSeconds(duration: Long): Long
```

Equivalent to [SECONDS.convert(duration, this)](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit#convert(kotlin.Long,%20java.util.concurrent.TimeUnit)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------|
| `duration` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the duration |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the converted duration, or`Long.MIN_VALUE`if conversion would negatively overflow, or`Long.MAX_VALUE`if it would positively overflow. |

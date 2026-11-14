# TimeUnit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TimeUnit

```
class TimeUnit
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.util.concurrent.TimeUnit](../java/util/concurrent/TimeUnit.md)\> ||
| | ↳ | [java.util.concurrent.TimeUnit](../java/util/concurrent/TimeUnit.md) |

| Known Direct Subclasses [TimeUnit.DAYS](../java/util/concurrent/TimeUnit.md), [TimeUnit.HOURS](../java/util/concurrent/TimeUnit.md), [TimeUnit.MICROSECONDS](../java/util/concurrent/TimeUnit.md), [TimeUnit.MILLISECONDS](../java/util/concurrent/TimeUnit.md), [TimeUnit.MINUTES](../java/util/concurrent/TimeUnit.md), [TimeUnit.NANOSECONDS](../java/util/concurrent/TimeUnit.md), [TimeUnit.SECONDS](../java/util/concurrent/TimeUnit.md) |-------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------| | [TimeUnit.DAYS](../java/util/concurrent/TimeUnit.md) | Time unit representing twenty four hours. | | [TimeUnit.HOURS](../java/util/concurrent/TimeUnit.md) | Time unit representing sixty minutes. | | [TimeUnit.MICROSECONDS](../java/util/concurrent/TimeUnit.md) | Time unit representing one thousandth of a millisecond. | | [TimeUnit.MILLISECONDS](../java/util/concurrent/TimeUnit.md) | Time unit representing one thousandth of a second. | | [TimeUnit.MINUTES](../java/util/concurrent/TimeUnit.md) | Time unit representing sixty seconds. | | [TimeUnit.NANOSECONDS](../java/util/concurrent/TimeUnit.md) | Time unit representing one thousandth of a microsecond. | | [TimeUnit.SECONDS](../java/util/concurrent/TimeUnit.md) | Time unit representing one second. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

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
| [DAYS](../java/util/concurrent/TimeUnit.md) Time unit representing twenty four hours. |
| [HOURS](../java/util/concurrent/TimeUnit.md) Time unit representing sixty minutes. |
| [MICROSECONDS](../java/util/concurrent/TimeUnit.md) Time unit representing one thousandth of a millisecond. |
| [MILLISECONDS](../java/util/concurrent/TimeUnit.md) Time unit representing one thousandth of a second. |
| [MINUTES](../java/util/concurrent/TimeUnit.md) Time unit representing sixty seconds. |
| [NANOSECONDS](../java/util/concurrent/TimeUnit.md) Time unit representing one thousandth of a microsecond. |
| [SECONDS](../java/util/concurrent/TimeUnit.md) Time unit representing one second. |

| Public methods ||
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [convert](../java/util/concurrent/TimeUnit.md))`(`duration:` ` [Duration](../java/time/Duration.md)!`)` Converts the given time duration to this unit. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [convert](../java/util/concurrent/TimeUnit.md))`(`sourceDuration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `sourceUnit:` ` [TimeUnit](../java/util/concurrent/TimeUnit.md)!`)` Converts the given time duration in the given unit to this unit. |
| static [TimeUnit](../java/util/concurrent/TimeUnit.md)! | [of](../java/util/concurrent/TimeUnit.md))`(`chronoUnit:` ` [ChronoUnit](../java/time/temporal/ChronoUnit.md)!`)` Converts a`ChronoUnit`to the equivalent`TimeUnit`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sleep](../java/util/concurrent/TimeUnit.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Performs a [Thread.sleep](../java/lang/Thread.md))using this time unit. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [timedJoin](../java/util/concurrent/TimeUnit.md))`(`thread:` ` [Thread](../java/lang/Thread.md)!`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Performs a timed [Thread.join](../java/lang/Thread.md))using this time unit. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [timedWait](../java/util/concurrent/TimeUnit.md))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Performs a timed [Object.wait](../java/lang/Object.md))using this time unit. |
| --- | --- |
| [ChronoUnit](../java/time/temporal/ChronoUnit.md)! | [toChronoUnit](../java/util/concurrent/TimeUnit.md))`()` Converts this`TimeUnit`to the equivalent`ChronoUnit`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toDays](../java/util/concurrent/TimeUnit.md))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Equivalent to [DAYS.convert(duration, this)](../java/util/concurrent/TimeUnit.md)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toHours](../java/util/concurrent/TimeUnit.md))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Equivalent to [HOURS.convert(duration, this)](../java/util/concurrent/TimeUnit.md)). |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toMicros](../java/util/concurrent/TimeUnit.md))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Equivalent to [MICROSECONDS.convert(duration, this)](../java/util/concurrent/TimeUnit.md)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toMillis](../java/util/concurrent/TimeUnit.md))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Equivalent to [MILLISECONDS.convert(duration, this)](../java/util/concurrent/TimeUnit.md)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toMinutes](../java/util/concurrent/TimeUnit.md))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Equivalent to [MINUTES.convert(duration, this)](../java/util/concurrent/TimeUnit.md)). |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toNanos](../java/util/concurrent/TimeUnit.md))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Equivalent to [NANOSECONDS.convert(duration, this)](../java/util/concurrent/TimeUnit.md)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toSeconds](../java/util/concurrent/TimeUnit.md))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Equivalent to [SECONDS.convert(duration, this)](../java/util/concurrent/TimeUnit.md)). |

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
| `duration` | [Duration](../java/time/Duration.md)!:the time duration |

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
| `sourceUnit` | [TimeUnit](../java/util/concurrent/TimeUnit.md)!:the unit of the`sourceDuration`argument |

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
| `chronoUnit` | [ChronoUnit](../java/time/temporal/ChronoUnit.md)!:the ChronoUnit to convert |

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------|
| [TimeUnit](../java/util/concurrent/TimeUnit.md)! | the converted equivalent TimeUnit |

| Exceptions ||
|--------------------------------------|------------------------------------------|
| `java.lang.IllegalArgumentException` | if`chronoUnit`has no equivalent TimeUnit |
| `java.lang.NullPointerException` | if`chronoUnit`is null |

### sleep

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sleep(timeout: Long): Unit
```

Performs a [Thread.sleep](../java/lang/Thread.md))using this time unit. This is a convenience method that converts time arguments into the form required by the`Thread.sleep`method.

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

Performs a timed [Thread.join](../java/lang/Thread.md))using this time unit. This is a convenience method that converts time arguments into the form required by the`Thread.join`method.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `thread` | [Thread](../java/lang/Thread.md)!:the thread to wait for |
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

Performs a timed [Object.wait](../java/lang/Object.md))using this time unit. This is a convenience method that converts timeout arguments into the form required by the`Object.wait`method.

For example, you could implement a blocking`poll`method (see [BlockingQueue.poll](../java/util/concurrent/BlockingQueue.md))) using: 

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
| [ChronoUnit](../java/time/temporal/ChronoUnit.md)! | the converted equivalent ChronoUnit |

### toDays

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toDays(duration: Long): Long
```

Equivalent to [DAYS.convert(duration, this)](../java/util/concurrent/TimeUnit.md)).

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

Equivalent to [HOURS.convert(duration, this)](../java/util/concurrent/TimeUnit.md)).

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

Equivalent to [MICROSECONDS.convert(duration, this)](../java/util/concurrent/TimeUnit.md)).

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

Equivalent to [MILLISECONDS.convert(duration, this)](../java/util/concurrent/TimeUnit.md)).

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

Equivalent to [MINUTES.convert(duration, this)](../java/util/concurrent/TimeUnit.md)).

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

Equivalent to [NANOSECONDS.convert(duration, this)](../java/util/concurrent/TimeUnit.md)).

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

Equivalent to [SECONDS.convert(duration, this)](../java/util/concurrent/TimeUnit.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------|
| `duration` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the duration |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the converted duration, or`Long.MIN_VALUE`if conversion would negatively overflow, or`Long.MAX_VALUE`if it would positively overflow. |

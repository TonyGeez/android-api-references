# InstantSource

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InstantSource

```
interface InstantSource
```

| [java.time.InstantSource](https://developer.android.com/reference/kotlin/java/time/InstantSource#) |

| Known Direct Subclasses [Clock](https://developer.android.com/reference/kotlin/java/time/Clock) |-------------------------------------------------------------------------|-----------------------------------------------------------------------------------| | [Clock](https://developer.android.com/reference/kotlin/java/time/Clock) | A clock providing access to the current instant, date and time using a time-zone. | |
| --- | --- | --- | --- | --- | --- | --- |

Provides access to the current instant.

Instances of this interface are used to access a pluggable representation of the current instant. For example,`InstantSource`can be used instead of [System.currentTimeMillis()](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()).

The primary purpose of this abstraction is to allow alternate instant sources to be plugged in as and when required. Applications use an object to obtain the current time rather than a static method. This can simplify testing.

As such, this interface does not guarantee the result actually represents the current instant on the time-line. Instead, it allows the application to provide a controlled view as to what the current instant is.

Best practice for applications is to pass an`InstantSource`into any method that requires the current instant. A dependency injection framework is one way to achieve this: 

```kotlin
public class MyBean {
     private InstantSource source;  // dependency inject
     ...
     public void process(Instant endInstant) {
       if (source.instant().isAfter(endInstant) {
         ...
       }
     }
   }
  
```
This approach allows an alternative source, such as [fixed](https://developer.android.com/reference/kotlin/java/time/InstantSource#fixed(java.time.Instant))or [offset](https://developer.android.com/reference/kotlin/java/time/InstantSource#offset(java.time.InstantSource,%20java.time.Duration))to be used during testing.

The`system`factory method provides a source based on the best available system clock. This may use [System.currentTimeMillis()](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()), or a higher resolution clock if one is available.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [InstantSource](https://developer.android.com/reference/kotlin/java/time/InstantSource#)! | [fixed](https://developer.android.com/reference/kotlin/java/time/InstantSource#fixed(java.time.Instant))`(`fixedInstant:` ` [Instant](https://developer.android.com/reference/kotlin/java/time/Instant)!`)` Obtains a source that always returns the same instant. |
| abstract [Instant](https://developer.android.com/reference/kotlin/java/time/Instant)! | [instant](https://developer.android.com/reference/kotlin/java/time/InstantSource#instant())`()` Gets the current instant of the source. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [millis](https://developer.android.com/reference/kotlin/java/time/InstantSource#millis())`()` Gets the current millisecond instant of the source. |
| --- | --- |
| openstatic [InstantSource](https://developer.android.com/reference/kotlin/java/time/InstantSource#)! | [offset](https://developer.android.com/reference/kotlin/java/time/InstantSource#offset(java.time.InstantSource,%20java.time.Duration))`(`baseSource:` ` [InstantSource](https://developer.android.com/reference/kotlin/java/time/InstantSource#)!`, `offsetDuration:` ` [Duration](https://developer.android.com/reference/kotlin/java/time/Duration)!`)` Obtains a source that returns instants from the specified source with the specified duration added. |
| openstatic [InstantSource](https://developer.android.com/reference/kotlin/java/time/InstantSource#)! | [system](https://developer.android.com/reference/kotlin/java/time/InstantSource#system())`()` Obtains a source that returns the current instant using the best available system clock. |
| openstatic [InstantSource](https://developer.android.com/reference/kotlin/java/time/InstantSource#)! | [tick](https://developer.android.com/reference/kotlin/java/time/InstantSource#tick(java.time.InstantSource,%20java.time.Duration))`(`baseSource:` ` [InstantSource](https://developer.android.com/reference/kotlin/java/time/InstantSource#)!`, `tickDuration:` ` [Duration](https://developer.android.com/reference/kotlin/java/time/Duration)!`)` Obtains a source that returns instants from the specified source truncated to the nearest occurrence of the specified duration. |
| --- | --- |
| open [Clock](https://developer.android.com/reference/kotlin/java/time/Clock)! | [withZone](https://developer.android.com/reference/kotlin/java/time/InstantSource#withZone(java.time.ZoneId))`(`zone:` ` [ZoneId](https://developer.android.com/reference/kotlin/java/time/ZoneId)!`)` Returns a clock with the specified time-zone. |

## Public methods

### fixed

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fixed(fixedInstant: Instant!): InstantSource!
```

Obtains a source that always returns the same instant.

This source simply returns the specified instant. As such, it is not a source that represents the current instant. The main use case for this is in testing, where the fixed source ensures tests are not dependent on the current source.

The returned implementation is immutable, thread-safe and`Serializable`.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------|
| `fixedInstant` | [Instant](https://developer.android.com/reference/kotlin/java/time/Instant)!:the instant to use, not null |

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [InstantSource](https://developer.android.com/reference/kotlin/java/time/InstantSource#)! | a source that always returns the same instant, not null |

### instant

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun instant(): Instant!
```

Gets the current instant of the source.

This returns an instant representing the current instant as defined by the source.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------|
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant)! | the current instant from this source, not null |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------|
| `java.time.DateTimeException` | if the instant cannot be obtained, not thrown by most implementations |

### millis

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun millis(): Long
```

Gets the current millisecond instant of the source.

This returns the millisecond-based instant, measured from 1970-01-01T00:00Z (UTC). This is equivalent to the definition of [System.currentTimeMillis()](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()).

Most applications should avoid this method and use [Instant](https://developer.android.com/reference/kotlin/java/time/Instant) to represent an instant on the time-line rather than a raw millisecond value. This method is provided to allow the use of the source in high performance use cases where the creation of an object would be unacceptable.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the current millisecond instant from this source, measured from the Java epoch of 1970-01-01T00:00Z (UTC), not null |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------|
| `java.time.DateTimeException` | if the instant cannot be obtained, not thrown by most implementations |

### offset

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun offset(
    baseSource: InstantSource!, 
    offsetDuration: Duration!
): InstantSource!
```

Obtains a source that returns instants from the specified source with the specified duration added.

This source wraps another source, returning instants that are later by the specified duration. If the duration is negative, the instants will be earlier than the current date and time. The main use case for this is to simulate running in the future or in the past.

A duration of zero would have no offsetting effect. Passing zero will return the underlying source.

The returned implementation is immutable, thread-safe and`Serializable`providing that the base source is.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `baseSource` | [InstantSource](https://developer.android.com/reference/kotlin/java/time/InstantSource#)!:the base source to add the duration to, not null |
| `offsetDuration` | [Duration](https://developer.android.com/reference/kotlin/java/time/Duration)!:the duration to add, not null |

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [InstantSource](https://developer.android.com/reference/kotlin/java/time/InstantSource#)! | a source based on the base source with the duration added, not null |

### system

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun system(): InstantSource!
```

Obtains a source that returns the current instant using the best available system clock.

This source is based on the best available system clock. This may use [System.currentTimeMillis()](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()), or a higher resolution system clock if one is available.

The returned implementation is immutable, thread-safe and`Serializable`.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [InstantSource](https://developer.android.com/reference/kotlin/java/time/InstantSource#)! | a source that uses the best available system clock, not null |

### tick

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun tick(
    baseSource: InstantSource!, 
    tickDuration: Duration!
): InstantSource!
```

Obtains a source that returns instants from the specified source truncated to the nearest occurrence of the specified duration.

This source will only tick as per the specified duration. Thus, if the duration is half a second, the source will return instants truncated to the half second.

The tick duration must be positive. If it has a part smaller than a whole millisecond, then the whole duration must divide into one second without leaving a remainder. All normal tick durations will match these criteria, including any multiple of hours, minutes, seconds and milliseconds, and sensible nanosecond durations, such as 20ns, 250,000ns and 500,000ns.

A duration of zero or one nanosecond would have no truncation effect. Passing one of these will return the underlying source.

Implementations may use a caching strategy for performance reasons. As such, it is possible that the start of the requested duration observed via this source will be later than that observed directly via the underlying source.

The returned implementation is immutable, thread-safe and`Serializable`providing that the base source is.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `baseSource` | [InstantSource](https://developer.android.com/reference/kotlin/java/time/InstantSource#)!:the base source to base the ticking source on, not null |
| `tickDuration` | [Duration](https://developer.android.com/reference/kotlin/java/time/Duration)!:the duration of each visible tick, not negative, not null |

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [InstantSource](https://developer.android.com/reference/kotlin/java/time/InstantSource#)! | a source that ticks in whole units of the duration, not null |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the duration is negative, or has a part smaller than a whole millisecond such that the whole duration is not divisible into one second |
| `java.lang.ArithmeticException` | if the duration is too large to be represented as nanos |

### withZone

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun withZone(zone: ZoneId!): Clock!
```

Returns a clock with the specified time-zone.

This returns a [Clock](https://developer.android.com/reference/kotlin/java/time/Clock), which is an extension of this interface that combines this source and the specified time-zone.

The returned implementation is immutable, thread-safe and`Serializable`providing that this source is.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------|
| `zone` | [ZoneId](https://developer.android.com/reference/kotlin/java/time/ZoneId)!:the time-zone to use, not null |

| Return ||
|--------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Clock](https://developer.android.com/reference/kotlin/java/time/Clock)! | a clock based on this source with the specified time-zone, not null |

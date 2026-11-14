# InstantSource

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InstantSource

```
interface InstantSource
```

| [java.time.InstantSource](../java/time/InstantSource.md) |

| Known Direct Subclasses [Clock](../java/time/Clock.md) |-------------------------------------------------------------------------|-----------------------------------------------------------------------------------| | [Clock](../java/time/Clock.md) | A clock providing access to the current instant, date and time using a time-zone. | |
| --- | --- | --- | --- | --- | --- | --- |

Provides access to the current instant.

Instances of this interface are used to access a pluggable representation of the current instant. For example,`InstantSource`can be used instead of [System.currentTimeMillis()](../java/lang/System.md)).

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
This approach allows an alternative source, such as [fixed](../java/time/InstantSource.md))or [offset](../java/time/InstantSource.md))to be used during testing.

The`system`factory method provides a source based on the best available system clock. This may use [System.currentTimeMillis()](../java/lang/System.md)), or a higher resolution clock if one is available.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [InstantSource](../java/time/InstantSource.md)! | [fixed](../java/time/InstantSource.md))`(`fixedInstant:` ` [Instant](../java/time/Instant.md)!`)` Obtains a source that always returns the same instant. |
| abstract [Instant](../java/time/Instant.md)! | [instant](../java/time/InstantSource.md))`()` Gets the current instant of the source. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [millis](../java/time/InstantSource.md))`()` Gets the current millisecond instant of the source. |
| --- | --- |
| openstatic [InstantSource](../java/time/InstantSource.md)! | [offset](../java/time/InstantSource.md))`(`baseSource:` ` [InstantSource](../java/time/InstantSource.md)!`, `offsetDuration:` ` [Duration](../java/time/Duration.md)!`)` Obtains a source that returns instants from the specified source with the specified duration added. |
| openstatic [InstantSource](../java/time/InstantSource.md)! | [system](../java/time/InstantSource.md))`()` Obtains a source that returns the current instant using the best available system clock. |
| openstatic [InstantSource](../java/time/InstantSource.md)! | [tick](../java/time/InstantSource.md))`(`baseSource:` ` [InstantSource](../java/time/InstantSource.md)!`, `tickDuration:` ` [Duration](../java/time/Duration.md)!`)` Obtains a source that returns instants from the specified source truncated to the nearest occurrence of the specified duration. |
| --- | --- |
| open [Clock](../java/time/Clock.md)! | [withZone](../java/time/InstantSource.md))`(`zone:` ` [ZoneId](../java/time/ZoneId.md)!`)` Returns a clock with the specified time-zone. |

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
| `fixedInstant` | [Instant](../java/time/Instant.md)!:the instant to use, not null |

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [InstantSource](../java/time/InstantSource.md)! | a source that always returns the same instant, not null |

### instant

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun instant(): Instant!
```

Gets the current instant of the source.

This returns an instant representing the current instant as defined by the source.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------|
| [Instant](../java/time/Instant.md)! | the current instant from this source, not null |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------|
| `java.time.DateTimeException` | if the instant cannot be obtained, not thrown by most implementations |

### millis

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun millis(): Long
```

Gets the current millisecond instant of the source.

This returns the millisecond-based instant, measured from 1970-01-01T00:00Z (UTC). This is equivalent to the definition of [System.currentTimeMillis()](../java/lang/System.md)).

Most applications should avoid this method and use [Instant](../java/time/Instant.md) to represent an instant on the time-line rather than a raw millisecond value. This method is provided to allow the use of the source in high performance use cases where the creation of an object would be unacceptable.

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
| `baseSource` | [InstantSource](../java/time/InstantSource.md)!:the base source to add the duration to, not null |
| `offsetDuration` | [Duration](../java/time/Duration.md)!:the duration to add, not null |

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [InstantSource](../java/time/InstantSource.md)! | a source based on the base source with the duration added, not null |

### system

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun system(): InstantSource!
```

Obtains a source that returns the current instant using the best available system clock.

This source is based on the best available system clock. This may use [System.currentTimeMillis()](../java/lang/System.md)), or a higher resolution system clock if one is available.

The returned implementation is immutable, thread-safe and`Serializable`.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [InstantSource](../java/time/InstantSource.md)! | a source that uses the best available system clock, not null |

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
| `baseSource` | [InstantSource](../java/time/InstantSource.md)!:the base source to base the ticking source on, not null |
| `tickDuration` | [Duration](../java/time/Duration.md)!:the duration of each visible tick, not negative, not null |

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [InstantSource](../java/time/InstantSource.md)! | a source that ticks in whole units of the duration, not null |

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

This returns a [Clock](../java/time/Clock.md), which is an extension of this interface that combines this source and the specified time-zone.

The returned implementation is immutable, thread-safe and`Serializable`providing that this source is.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------|
| `zone` | [ZoneId](../java/time/ZoneId.md)!:the time-zone to use, not null |

| Return ||
|--------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Clock](../java/time/Clock.md)! | a clock based on this source with the specified time-zone, not null |

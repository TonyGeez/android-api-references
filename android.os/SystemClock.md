# SystemClock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SystemClock

Kotlin| [Java](../android/os/SystemClock.md) 
| --- | --- |

```
class SystemClock
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.SystemClock](../android/os/SystemClock.md) |

Core timekeeping facilities.

Three different clocks are available, and they should not be confused:

- [System.currentTimeMillis()](../java/lang/System.md))is the standard "wall" clock (time and date) expressing milliseconds since the epoch. The wall clock can be set by the user or the phone network (see [setCurrentTimeMillis](../android/os/SystemClock.md))), so the time may jump backwards or forwards unpredictably. This clock should only be used when correspondence with real-world dates and times is important, such as in a calendar or alarm clock application. Interval or elapsed time measurements should use a different clock. If you are using System.currentTimeMillis(), consider listening to the [ACTION_TIME_TICK](../android/content/Intent.md), [ACTION_TIME_CHANGED](../android/content/Intent.md) and [ACTION_TIMEZONE_CHANGED](../android/content/Intent.md) [Intent](../android/content/Intent.md) broadcasts to find out when the time changes.

- [uptimeMillis](../android/os/SystemClock.md))is counted in milliseconds since the system was booted. This clock stops when the system enters deep sleep (CPU off, display dark, device waiting for external input), but is not affected by clock scaling, idle, or other power saving mechanisms. This is the basis for most interval timing such as [Thread.sleep(millis)](../java/lang/Thread.md)), [Object.wait(millis)](../java/lang/Object.md)), and [System.nanoTime()](../java/lang/System.md)). This clock is guaranteed to be monotonic, and is suitable for interval timing when the interval does not span device sleep. Most methods that accept a timestamp value currently expect the [uptimeMillis](../android/os/SystemClock.md))clock.

- [elapsedRealtime](../android/os/SystemClock.md))and [elapsedRealtimeNanos](../android/os/SystemClock.md))return the time since the system was booted, and include deep sleep. This clock is guaranteed to be monotonic, and continues to tick even when the CPU is in power saving modes, so is the recommend basis for general purpose interval timing.

There are several mechanisms for controlling the timing of events:

<!-- -->

- Standard functions like [Thread.sleep(millis)](../java/lang/Thread.md))and [Object.wait(millis)](../java/lang/Object.md))are always available. These functions use the [uptimeMillis](../android/os/SystemClock.md))clock; if the device enters sleep, the remainder of the time will be postponed until the device wakes up. These synchronous functions may be interrupted with [Thread.interrupt()](../java/lang/Thread.md)), and you must handle [InterruptedException](../java/lang/InterruptedException.md).

- [SystemClock.sleep(millis)](../android/os/SystemClock.md))is a utility function very similar to [Thread.sleep(millis)](../java/lang/Thread.md)), but it ignores [InterruptedException](../java/lang/InterruptedException.md). Use this function for delays if you do not use [Thread.interrupt()](../java/lang/Thread.md)), as it will preserve the interrupted state of the thread.

- The [android.os.Handler](../android/os/Handler.md) class can schedule asynchronous callbacks at an absolute or relative time. Handler objects also use the [uptimeMillis](../android/os/SystemClock.md))clock, and require an [event loop](../android/os/Looper.md)(normally present in any GUI application).

- The [android.app.AlarmManager](../android/app/AlarmManager.md) can trigger one-time or recurring events which occur even when the device is in deep sleep or your application is not running. Events may be scheduled with your choice of [java.lang.System#currentTimeMillis](../java/lang/System.md))(RTC) or [elapsedRealtime](../android/os/SystemClock.md))(ELAPSED_REALTIME), and cause an [android.content.Intent](../android/content/Intent.md) broadcast when they occur.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Clock](../java/time/Clock.md) | [currentGnssTimeClock](../android/os/SystemClock.md))`()` Returns a [Clock](../java/time/Clock.md) that starts at January 1, 1970 00:00:00. |
| static [Clock](../java/time/Clock.md) | [currentNetworkTimeClock](../android/os/SystemClock.md))`()` Returns a [Clock](../java/time/Clock.md) that starts at January 1, 1970 00:00:00. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [currentThreadTimeMillis](../android/os/SystemClock.md))`()` Returns milliseconds running in the current thread. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [elapsedRealtime](../android/os/SystemClock.md))`()` Returns milliseconds since boot, including time spent in sleep. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [elapsedRealtimeNanos](../android/os/SystemClock.md))`()` Returns nanoseconds since boot, including time spent in sleep. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setCurrentTimeMillis](../android/os/SystemClock.md))`(`millis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the current wall time, in milliseconds. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sleep](../android/os/SystemClock.md))`(`ms:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Waits a given number of milliseconds (of uptimeMillis) before returning. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [uptimeMillis](../android/os/SystemClock.md))`()` Returns milliseconds since boot, not counting time spent in deep sleep. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [uptimeNanos](../android/os/SystemClock.md))`()` Returns nanoseconds since boot, not counting time spent in deep sleep. |
| --- | --- |

## Public methods

### currentGnssTimeClock

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun currentGnssTimeClock(): Clock
```

Returns a [Clock](../java/time/Clock.md) that starts at January 1, 1970 00:00:00.0 UTC, synchronized using the device's location provider.

| Return ||
|-------------------------------------------------------------------------------|-----------------------------|
| [Clock](../java/time/Clock.md) | This value cannot be`null`. |

| Exceptions ||
|-------------------------------|-------------------------------------------------------------------|
| `java.time.DateTimeException` | when the location provider has not had a location fix since boot. |

### currentNetworkTimeClock

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun currentNetworkTimeClock(): Clock
```

Returns a [Clock](../java/time/Clock.md) that starts at January 1, 1970 00:00:00.0 UTC, synchronized using a remote network source outside the device.

While the time returned by [System.currentTimeMillis()](../java/lang/System.md))can be adjusted by the user, the time returned by this method cannot be adjusted by the user.

This performs no blocking network operations and returns values based on a recent successful synchronization event; it will either return a valid time or throw.

Note that synchronization may occur using an insecure network protocol, so the returned time should not be used for security purposes. The device may resynchronize with the same or different network source at any time. Due to network delays, variations between servers, or local (client side) clock drift, the accuracy of the returned times cannot be guaranteed. In extreme cases, consecutive calls to [Clock.millis()](../java/time/Clock.md))on the returned [Clock](../java/time/Clock.md) could return times that are out of order.

| Return ||
|-------------------------------------------------------------------------------|-----------------------------|
| [Clock](../java/time/Clock.md) | This value cannot be`null`. |

| Exceptions ||
|-------------------------------|---------------------------------------|
| `java.time.DateTimeException` | when no network time can be provided. |

### currentThreadTimeMillis

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun currentThreadTimeMillis(): Long
```

Returns milliseconds running in the current thread.

| Return ||
|------------------------------------------------------------------------------|------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | elapsed milliseconds in the thread |

### elapsedRealtime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun elapsedRealtime(): Long
```

Returns milliseconds since boot, including time spent in sleep.

| Return ||
|------------------------------------------------------------------------------|----------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | elapsed milliseconds since boot. |

### elapsedRealtimeNanos

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun elapsedRealtimeNanos(): Long
```

Returns nanoseconds since boot, including time spent in sleep.

| Return ||
|------------------------------------------------------------------------------|---------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | elapsed nanoseconds since boot. |

### setCurrentTimeMillis

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setCurrentTimeMillis(millis: Long): Boolean
```

Sets the current wall time, in milliseconds. Requires the calling process to have appropriate permissions.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | if the clock was successfully set to the specified time. |

### sleep

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun sleep(ms: Long): Unit
```

Waits a given number of milliseconds (of uptimeMillis) before returning. Similar to [java.lang.Thread#sleep(long)](../java/lang/Thread.md)), but does not throw [InterruptedException](../java/lang/InterruptedException.md); [Thread.interrupt()](../java/lang/Thread.md))events are deferred until the next interruptible operation. Does not return until at least the specified number of milliseconds has elapsed.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------|
| `ms` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):to sleep before returning, in milliseconds of uptime. |

### uptimeMillis

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun uptimeMillis(): Long
```

Returns milliseconds since boot, not counting time spent in deep sleep.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | milliseconds of non-sleep uptime since boot. |

### uptimeNanos

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun uptimeNanos(): Long
```

Returns nanoseconds since boot, not counting time spent in deep sleep.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | nanoseconds of non-sleep uptime since boot. |

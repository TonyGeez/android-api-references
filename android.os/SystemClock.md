# SystemClock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SystemClock

Kotlin| [Java](https://developer.android.com/reference/android/os/SystemClock "View this page in Java") 
| --- | --- |

```
class SystemClock
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.SystemClock](https://developer.android.com/reference/kotlin/android/os/SystemClock#) |

Core timekeeping facilities.

Three different clocks are available, and they should not be confused:

- [System.currentTimeMillis()](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis())is the standard "wall" clock (time and date) expressing milliseconds since the epoch. The wall clock can be set by the user or the phone network (see [setCurrentTimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock#setCurrentTimeMillis(kotlin.Long))), so the time may jump backwards or forwards unpredictably. This clock should only be used when correspondence with real-world dates and times is important, such as in a calendar or alarm clock application. Interval or elapsed time measurements should use a different clock. If you are using System.currentTimeMillis(), consider listening to the [ACTION_TIME_TICK](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_TIME_TICK:kotlin.String), [ACTION_TIME_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_TIME_CHANGED:kotlin.String) and [ACTION_TIMEZONE_CHANGED](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_TIMEZONE_CHANGED:kotlin.String) [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) broadcasts to find out when the time changes.

- [uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis())is counted in milliseconds since the system was booted. This clock stops when the system enters deep sleep (CPU off, display dark, device waiting for external input), but is not affected by clock scaling, idle, or other power saving mechanisms. This is the basis for most interval timing such as [Thread.sleep(millis)](https://developer.android.com/reference/kotlin/java/lang/Thread.html#sleep(kotlin.Long)), [Object.wait(millis)](https://developer.android.com/reference/kotlin/java/lang/Object.html#wait(kotlin.Long)), and [System.nanoTime()](https://developer.android.com/reference/kotlin/java/lang/System.html#nanoTime()). This clock is guaranteed to be monotonic, and is suitable for interval timing when the interval does not span device sleep. Most methods that accept a timestamp value currently expect the [uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis())clock.

- [elapsedRealtime](https://developer.android.com/reference/kotlin/android/os/SystemClock#elapsedRealtime())and [elapsedRealtimeNanos](https://developer.android.com/reference/kotlin/android/os/SystemClock#elapsedRealtimeNanos())return the time since the system was booted, and include deep sleep. This clock is guaranteed to be monotonic, and continues to tick even when the CPU is in power saving modes, so is the recommend basis for general purpose interval timing.

There are several mechanisms for controlling the timing of events:

<!-- -->

- Standard functions like [Thread.sleep(millis)](https://developer.android.com/reference/kotlin/java/lang/Thread.html#sleep(kotlin.Long))and [Object.wait(millis)](https://developer.android.com/reference/kotlin/java/lang/Object.html#wait(kotlin.Long))are always available. These functions use the [uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis())clock; if the device enters sleep, the remainder of the time will be postponed until the device wakes up. These synchronous functions may be interrupted with [Thread.interrupt()](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt()), and you must handle [InterruptedException](https://developer.android.com/reference/kotlin/java/lang/InterruptedException.html#).

- [SystemClock.sleep(millis)](https://developer.android.com/reference/kotlin/android/os/SystemClock#sleep(kotlin.Long))is a utility function very similar to [Thread.sleep(millis)](https://developer.android.com/reference/kotlin/java/lang/Thread.html#sleep(kotlin.Long)), but it ignores [InterruptedException](https://developer.android.com/reference/kotlin/java/lang/InterruptedException.html#). Use this function for delays if you do not use [Thread.interrupt()](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt()), as it will preserve the interrupted state of the thread.

- The [android.os.Handler](https://developer.android.com/reference/kotlin/android/os/Handler) class can schedule asynchronous callbacks at an absolute or relative time. Handler objects also use the [uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis())clock, and require an [event loop](https://developer.android.com/reference/kotlin/android/os/Looper)(normally present in any GUI application).

- The [android.app.AlarmManager](https://developer.android.com/reference/kotlin/android/app/AlarmManager.html#) can trigger one-time or recurring events which occur even when the device is in deep sleep or your application is not running. Events may be scheduled with your choice of [java.lang.System#currentTimeMillis](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis())(RTC) or [elapsedRealtime](https://developer.android.com/reference/kotlin/android/os/SystemClock#elapsedRealtime())(ELAPSED_REALTIME), and cause an [android.content.Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) broadcast when they occur.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Clock](https://developer.android.com/reference/kotlin/java/time/Clock.html#) | [currentGnssTimeClock](https://developer.android.com/reference/kotlin/android/os/SystemClock#currentGnssTimeClock())`()` Returns a [Clock](https://developer.android.com/reference/kotlin/java/time/Clock.html#) that starts at January 1, 1970 00:00:00. |
| static [Clock](https://developer.android.com/reference/kotlin/java/time/Clock.html#) | [currentNetworkTimeClock](https://developer.android.com/reference/kotlin/android/os/SystemClock#currentNetworkTimeClock())`()` Returns a [Clock](https://developer.android.com/reference/kotlin/java/time/Clock.html#) that starts at January 1, 1970 00:00:00. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [currentThreadTimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock#currentThreadTimeMillis())`()` Returns milliseconds running in the current thread. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [elapsedRealtime](https://developer.android.com/reference/kotlin/android/os/SystemClock#elapsedRealtime())`()` Returns milliseconds since boot, including time spent in sleep. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [elapsedRealtimeNanos](https://developer.android.com/reference/kotlin/android/os/SystemClock#elapsedRealtimeNanos())`()` Returns nanoseconds since boot, including time spent in sleep. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setCurrentTimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock#setCurrentTimeMillis(kotlin.Long))`(`millis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the current wall time, in milliseconds. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sleep](https://developer.android.com/reference/kotlin/android/os/SystemClock#sleep(kotlin.Long))`(`ms:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Waits a given number of milliseconds (of uptimeMillis) before returning. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis())`()` Returns milliseconds since boot, not counting time spent in deep sleep. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [uptimeNanos](https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeNanos())`()` Returns nanoseconds since boot, not counting time spent in deep sleep. |
| --- | --- |

## Public methods

### currentGnssTimeClock

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun currentGnssTimeClock(): Clock
```

Returns a [Clock](https://developer.android.com/reference/kotlin/java/time/Clock.html#) that starts at January 1, 1970 00:00:00.0 UTC, synchronized using the device's location provider.

| Return ||
|-------------------------------------------------------------------------------|-----------------------------|
| [Clock](https://developer.android.com/reference/kotlin/java/time/Clock.html#) | This value cannot be`null`. |

| Exceptions ||
|-------------------------------|-------------------------------------------------------------------|
| `java.time.DateTimeException` | when the location provider has not had a location fix since boot. |

### currentNetworkTimeClock

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun currentNetworkTimeClock(): Clock
```

Returns a [Clock](https://developer.android.com/reference/kotlin/java/time/Clock.html#) that starts at January 1, 1970 00:00:00.0 UTC, synchronized using a remote network source outside the device.

While the time returned by [System.currentTimeMillis()](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis())can be adjusted by the user, the time returned by this method cannot be adjusted by the user.

This performs no blocking network operations and returns values based on a recent successful synchronization event; it will either return a valid time or throw.

Note that synchronization may occur using an insecure network protocol, so the returned time should not be used for security purposes. The device may resynchronize with the same or different network source at any time. Due to network delays, variations between servers, or local (client side) clock drift, the accuracy of the returned times cannot be guaranteed. In extreme cases, consecutive calls to [Clock.millis()](https://developer.android.com/reference/kotlin/java/time/Clock.html#millis())on the returned [Clock](https://developer.android.com/reference/kotlin/java/time/Clock.html#) could return times that are out of order.

| Return ||
|-------------------------------------------------------------------------------|-----------------------------|
| [Clock](https://developer.android.com/reference/kotlin/java/time/Clock.html#) | This value cannot be`null`. |

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

Waits a given number of milliseconds (of uptimeMillis) before returning. Similar to [java.lang.Thread#sleep(long)](https://developer.android.com/reference/kotlin/java/lang/Thread.html#sleep(kotlin.Long)), but does not throw [InterruptedException](https://developer.android.com/reference/kotlin/java/lang/InterruptedException.html#); [Thread.interrupt()](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())events are deferred until the next interruptible operation. Does not return until at least the specified number of milliseconds has elapsed.

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

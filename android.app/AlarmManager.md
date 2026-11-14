Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AlarmManager

```
open class AlarmManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.AlarmManager](AlarmManager.md) |

This class provides access to the system alarm services. These allow you to schedule your application to be run at some point in the future. When an alarm goes off, the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` that had been registered for it is broadcast by the system, automatically starting the target application if it is not already running. Registered alarms are retained while the device is asleep (and can optionally wake the device up if they go off during that time), but will be cleared if it is turned off and rebooted.

The Alarm Manager holds a CPU wake lock as long as the alarm receiver's onReceive() method is executing. This guarantees that the phone will not sleep until you have finished handling the broadcast. Once onReceive() returns, the Alarm Manager releases this wake lock. This means that the phone will in some cases sleep as soon as your onReceive() method completes. If your alarm receiver called startService, it is possible that the phone will sleep before the requested service is launched. To prevent this, your BroadcastReceiver and Service will need to implement a separate wake lock policy to ensure that the phone continues running until the service becomes available.

**Note: The Alarm Manager is intended for cases where you want to have your application code run at a specific time, even if your application is not currently running. For normal timing operations (ticks, timeouts, etc) it is easier and much more efficient to use `https://developer.android.com/reference/kotlin/android/os/Handler.html#`.**

**Note:** Beginning with API 19 (`https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`) alarm delivery is inexact: the OS will shift alarms in order to minimize wakeups and battery use. There are new APIs to support applications which need strict delivery guarantees; see setWindow and setExact. Applications whose `targetSdkVersion` is earlier than API 19 will continue to see the previous behavior in which all alarms are delivered exactly when requested.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/AlarmManager.AlarmClockInfo` An immutable description of a scheduled "alarm clock" event. |
| abstract | `https://developer.android.com/reference/kotlin/android/app/AlarmManager.OnAlarmListener` Direct-notification alarms: the requester must be running continuously from the time the alarm is set to the time it is delivered, or delivery will fail. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ACTION_NEXT_ALARM_CLOCK_CHANGED:kotlin.String` Broadcast Action: Sent after the value returned by getNextAlarmClock has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ACTION_SCHEDULE_EXACT_ALARM_PERMISSION_STATE_CHANGED:kotlin.String` Broadcast Action: An app is granted the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SCHEDULE_EXACT_ALARM:kotlin.String` permission. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME:kotlin.Int` Alarm time in elapsedRealtime (time since boot, including sleep). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME_WAKEUP:kotlin.Int` Alarm time in elapsedRealtime (time since boot, including sleep), which will wake up the device when it goes off. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlarmManager#INTERVAL_DAY:kotlin.Long` Available inexact recurrence interval recognized by setInexactRepeating when running on Android prior to API 19. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlarmManager#INTERVAL_FIFTEEN_MINUTES:kotlin.Long` Available inexact recurrence interval recognized by setInexactRepeating when running on Android prior to API 19. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlarmManager#INTERVAL_HALF_DAY:kotlin.Long` Available inexact recurrence interval recognized by setInexactRepeating when running on Android prior to API 19. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlarmManager#INTERVAL_HALF_HOUR:kotlin.Long` Available inexact recurrence interval recognized by setInexactRepeating when running on Android prior to API 19. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlarmManager#INTERVAL_HOUR:kotlin.Long` Available inexact recurrence interval recognized by setInexactRepeating when running on Android prior to API 19. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC:kotlin.Int` Alarm time in currentTimeMillis (wall clock time in UTC). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC_WAKEUP:kotlin.Int` Alarm time in currentTimeMillis (wall clock time in UTC), which will wake up the device when it goes off. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canScheduleExactAlarms Called to check if the caller can schedule exact alarms. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | cancel Remove any alarm scheduled to be delivered to the given `https://developer.android.com/reference/kotlin/android/app/AlarmManager.OnAlarmListener`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | cancel Remove any alarms with a matching `https://developer.android.com/reference/kotlin/android/content/Intent.html#`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | cancelAll Remove all alarms previously set by the caller, if any. |
| open [AlarmManager.AlarmClockInfo](../android/app/AlarmManager.AlarmClockInfo.md)! | getNextAlarmClock Gets information about the next alarm clock currently scheduled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | set Schedule an alarm. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | set Direct callback version of set. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAlarmClock Schedule an alarm that represents an alarm clock, which will be used to notify the user when it goes off. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAndAllowWhileIdle Like set, but this alarm will be allowed to execute even when the system is in low-power idle (a.k.a. doze) modes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setExact Schedule an alarm to be delivered precisely at the stated time. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setExact Direct callback version of setExact. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setExactAndAllowWhileIdle Like setExact, but this alarm will be allowed to execute even when the system is in low-power idle modes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setExactAndAllowWhileIdle Like setExact, but this alarm will be allowed to execute even when the system is in low-power idle modes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setInexactRepeating Schedule a repeating alarm that has inexact trigger time requirements; for example, an alarm that repeats every hour, but not necessarily at the top of every hour. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRepeating Schedule a repeating alarm. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTime Set the system wall clock time. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTimeZone Sets the system's persistent default time zone. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setWindow Schedule an alarm to be delivered within a given window of time. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setWindow Direct callback version of setWindow. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setWindow Direct callback version of setWindow. |

## Constants

### ACTION_NEXT_ALARM_CLOCK_CHANGED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NEXT_ALARM_CLOCK_CHANGED: String
```

Broadcast Action: Sent after the value returned by getNextAlarmClock has changed.

This is a protected intent that can only be sent by the system. It is only sent to registered receivers.

 Value: "android.app.action.NEXT_ALARM_CLOCK_CHANGED"

### ACTION_SCHEDULE_EXACT_ALARM_PERMISSION_STATE_CHANGED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SCHEDULE_EXACT_ALARM_PERMISSION_STATE_CHANGED: String
```

Broadcast Action: An app is granted the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SCHEDULE_EXACT_ALARM:kotlin.String` permission.

When the user revokes the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SCHEDULE_EXACT_ALARM:kotlin.String` permission, all alarms scheduled with #setExact, #setExactAndAllowWhileIdle and setAlarmClock will be deleted.

When the user grants the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SCHEDULE_EXACT_ALARM:kotlin.String`, this broadcast will be sent. Applications can reschedule all the necessary alarms when receiving it.

This broadcast will *not* be sent when the user revokes the permission.

*Note:* Applications are still required to check canScheduleExactAlarms before using the above APIs after receiving this broadcast, because it's possible that the permission is already revoked again by the time applications receive this broadcast.

This broadcast will be sent to both runtime receivers and manifest receivers.

This broadcast is sent as a foreground broadcast. See `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_RECEIVER_FOREGROUND:kotlin.Int`.

When an application receives this broadcast, it's allowed to start a foreground service.

 Value: "android.app.action.SCHEDULE_EXACT_ALARM_PERMISSION_STATE_CHANGED"

### ELAPSED_REALTIME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ELAPSED_REALTIME: Int
```

Alarm time in elapsedRealtime (time since boot, including sleep). This alarm does not wake the device up; if it goes off while the device is asleep, it will not be delivered until the next time the device wakes up.

 Value: 3

### ELAPSED_REALTIME_WAKEUP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ELAPSED_REALTIME_WAKEUP: Int
```

Alarm time in elapsedRealtime (time since boot, including sleep), which will wake up the device when it goes off.

 Value: 2

### INTERVAL_DAY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTERVAL_DAY: Long
```

Available inexact recurrence interval recognized by setInexactRepeating when running on Android prior to API 19.

 Value: 86400000L

### INTERVAL_FIFTEEN_MINUTES

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTERVAL_FIFTEEN_MINUTES: Long
```

Available inexact recurrence interval recognized by setInexactRepeating when running on Android prior to API 19.

 Value: 900000L

### INTERVAL_HALF_DAY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTERVAL_HALF_DAY: Long
```

Available inexact recurrence interval recognized by setInexactRepeating when running on Android prior to API 19.

 Value: 43200000L

### INTERVAL_HALF_HOUR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTERVAL_HALF_HOUR: Long
```

Available inexact recurrence interval recognized by setInexactRepeating when running on Android prior to API 19.

 Value: 1800000L

### INTERVAL_HOUR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTERVAL_HOUR: Long
```

Available inexact recurrence interval recognized by setInexactRepeating when running on Android prior to API 19.

 Value: 3600000L

### RTC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RTC: Int
```

Alarm time in currentTimeMillis (wall clock time in UTC). This alarm does not wake the device up; if it goes off while the device is asleep, it will not be delivered until the next time the device wakes up.

 Value: 1

### RTC_WAKEUP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RTC_WAKEUP: Int
```

Alarm time in currentTimeMillis (wall clock time in UTC), which will wake up the device when it goes off.

 Value: 0

## Public methods

### canScheduleExactAlarms

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canScheduleExactAlarms(): Boolean
```

Called to check if the caller can schedule exact alarms. Your app schedules exact alarms when it calls any of the `setExact...` or setAlarmClock API methods.

Apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or higher can schedule exact alarms only if they have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SCHEDULE_EXACT_ALARM:kotlin.String` permission or they are on the device's power-save exemption list. These apps can also start `https://developer.android.com/reference/kotlin/android/provider/Settings.html#ACTION_REQUEST_SCHEDULE_EXACT_ALARM:kotlin.String` to request this permission from the user.

Apps targeting lower sdk versions, can always schedule exact alarms.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the caller can schedule exact alarms, `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/Settings.html#ACTION_REQUEST_SCHEDULE_EXACT_ALARM:kotlin.String`
- setExact
- setExactAndAllowWhileIdle
- setAlarmClock
- isIgnoringBatteryOptimizations

### cancel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cancel(listener: AlarmManager.OnAlarmListener): Unit
```

Remove any alarm scheduled to be delivered to the given `https://developer.android.com/reference/kotlin/android/app/AlarmManager.OnAlarmListener`.

| Parameters ||
|---|---|
| `listener` | [AlarmManager.OnAlarmListener](../android/app/AlarmManager.OnAlarmListener.md): OnAlarmListener instance that is the target of a currently-set alarm. This value cannot be `null`. |

### cancel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cancel(operation: PendingIntent): Unit
```

Remove any alarms with a matching `https://developer.android.com/reference/kotlin/android/content/Intent.html#`. Any alarm, of any type, whose Intent matches this one (as defined by filterEquals), will be canceled.

| Parameters ||
|---|---|
| `operation` | [PendingIntent](PendingIntent.md): IntentSender which matches a previously added IntentSender. This parameter must not be `null`. |

**See Also**

### cancelAll

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cancelAll(): Unit
```

Remove all alarms previously set by the caller, if any.

### getNextAlarmClock

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNextAlarmClock(): AlarmManager.AlarmClockInfo!
```

Gets information about the next alarm clock currently scheduled. The alarm clocks considered are those scheduled by any application using the setAlarmClock method.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/AlarmManager.AlarmClockInfo!` | An `https://developer.android.com/reference/kotlin/android/app/AlarmManager.AlarmClockInfo` object describing the next upcoming alarm clock event that will occur. If there are no alarm clock events currently scheduled, this method will return `null`. |

**See Also**

- setAlarmClock
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager.AlarmClockInfo`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ACTION_NEXT_ALARM_CLOCK_CHANGED:kotlin.String`

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun set(
    type: Int, 
    triggerAtMillis: Long, 
    operation: PendingIntent
): Unit
```

Schedule an alarm. **Note: for timing operations (ticks, timeouts, etc) it is easier and much more efficient to use `https://developer.android.com/reference/kotlin/android/os/Handler.html#`.** If there is already an alarm scheduled for the same IntentSender, that previous alarm will first be canceled.

If the stated trigger time is in the past, the alarm will be triggered immediately. If there is already an alarm for this Intent scheduled (with the equality of two intents being defined by filterEquals), then it will be removed and replaced by this one.

The alarm is an Intent broadcast that goes to a broadcast receiver that you registered with android.content.Context#registerReceiver or through the \<receiver\> tag in an AndroidManifest.xml file.

Alarm intents are delivered with a data extra of type int called `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ALARM_COUNT:kotlin.String` that indicates how many past alarm events have been accumulated into this intent broadcast. Recurring alarms that have gone undelivered because the phone was asleep may have a count greater than one when delivered.

> [!NOTE]
> **Note:** Beginning in API 19, the trigger time passed to this method is treated as inexact: the alarm will not be delivered before this time, but may be deferred and delivered some time later. The OS will use this policy in order to "batch" alarms together across the entire system, minimizing the number of times the device needs to "wake up" and minimizing battery use. In general, alarms scheduled in the near future will not be deferred as long as alarms scheduled far in the future.
>
> With the new batching policy, delivery ordering guarantees are not as strong as they were previously. If the application sets multiple alarms, it is possible that these alarms' *actual* delivery ordering may not match the order of their *requested* delivery times. If your application has strong ordering requirements there are other APIs that you can use to get the necessary behavior; see setWindow and setExact.
>
> Applications whose `targetSdkVersion` is before API 19 will continue to get the previous alarm behavior: all of their scheduled alarms will be treated as exact.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): type of alarm. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME:kotlin.Int` |
| `triggerAtMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): time in milliseconds that the alarm should go off, using the appropriate clock (depending on the alarm type). |
| `operation` | [PendingIntent](PendingIntent.md): Action to perform when the alarm goes off; typically comes from getBroadcast. This value cannot be `null`. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/Handler.html#`
- setRepeating
- filterEquals
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME_WAKEUP:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC_WAKEUP:kotlin.Int`

### set

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun set(
    type: Int, 
    triggerAtMillis: Long, 
    tag: String?, 
    listener: AlarmManager.OnAlarmListener, 
    targetHandler: Handler?
): Unit
```

Direct callback version of set. Rather than supplying a PendingIntent to be sent when the alarm time is reached, this variant supplies an `https://developer.android.com/reference/kotlin/android/app/AlarmManager.OnAlarmListener` instance that will be invoked at that time.

Listener based alarms may be canceled by the Android system whenever the calling process no longer has any components running, such as Activity, Service, or `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#`, so only use these APIs when you do not need to receive alarms after the current component finishes, and also make sure to [cancel(OnAlarmListener)](AlarmManager.md)) them when it does. For example, if you use these APIs from an Activity, make sure to cancel the respective alarms when the activity finishes. If you need to receive the alarm even after that, use the PendingIntent based APIs.

The OnAlarmListener's onAlarm method will be invoked via the specified target Handler, or on the application's main looper if `null` is passed as the `targetHandler` parameter.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): type of alarm. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME:kotlin.Int` |
| `triggerAtMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): time in milliseconds that the alarm should go off, using the appropriate clock (depending on the alarm type). |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: string describing the alarm, used for logging and battery-use attribution. This value may be `null`. |
| --- | --- |
| `listener` | [AlarmManager.OnAlarmListener](../android/app/AlarmManager.OnAlarmListener.md): `https://developer.android.com/reference/kotlin/android/app/AlarmManager.OnAlarmListener` instance whose onAlarm method will be called when the alarm time is reached. A given OnAlarmListener instance can only be the target of a single pending alarm, just as a given PendingIntent can only be used with one alarm at a time. This value cannot be `null`. |
| `targetHandler` | [Handler](../android.os/Handler.md)?: `https://developer.android.com/reference/kotlin/android/os/Handler.html#` on which to execute the listener's onAlarm() callback, or `null` to run that callback on the main looper. |

### setAlarmClock

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAlarmClock(
    info: AlarmManager.AlarmClockInfo, 
    operation: PendingIntent
): Unit
```

Schedule an alarm that represents an alarm clock, which will be used to notify the user when it goes off. The expectation is that when this alarm triggers, the application will further wake up the device to tell the user about the alarm -- turning on the screen, playing a sound, vibrating, etc. As such, the system will typically also use the information supplied here to tell the user about this upcoming alarm if appropriate.

Due to the nature of this kind of alarm, similar to #setExactAndAllowWhileIdle, these alarms will be allowed to trigger even if the system is in a low-power idle (a.k.a. doze) mode. The system may also do some prep-work when it sees that such an alarm coming up, to reduce the amount of background work that could happen if this causes the device to fully wake up -- this is to avoid situations such as a large number of devices having an alarm set at the same time in the morning, all waking up at that time and suddenly swamping the network with pending background work. As such, these types of alarms can be extremely expensive on battery use and should only be used for their intended purpose.

This method is like setExact, but implies `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC_WAKEUP:kotlin.Int`.

**Note:** Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps targeting SDK level 31 or higher need to request the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SCHEDULE_EXACT_ALARM:kotlin.String` permission to use this API. The user and the system can revoke this permission via the special app access screen in Settings.

**Note:** Exact alarms should only be used for user-facing features. For more details, see [Exact alarm permission](https://developer.android.com/about/versions/12/behavior-changes-12#exact-alarm-permission).

Alarms scheduled via this API will be allowed to start a foreground service even if the app is in the background. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SCHEDULE_EXACT_ALARM:kotlin.String`

| Parameters ||
|---|---|
| `info` | [AlarmManager.AlarmClockInfo](../android/app/AlarmManager.AlarmClockInfo.md): This value cannot be `null`. |
| `operation` | [PendingIntent](PendingIntent.md): Action to perform when the alarm goes off; typically comes from getBroadcast. This value cannot be `null`. |

**See Also**

- setRepeating
- getNextAlarmClock
- filterEquals
- `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SCHEDULE_EXACT_ALARM:kotlin.String`

### setAndAllowWhileIdle

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAndAllowWhileIdle(
    type: Int, 
    triggerAtMillis: Long, 
    operation: PendingIntent
): Unit
```

Like set, but this alarm will be allowed to execute even when the system is in low-power idle (a.k.a. doze) modes. This type of alarm must **only** be used for situations where it is actually required that the alarm go off while in idle -- a reasonable example would be for a calendar notification that should make a sound so the user is aware of it. When the alarm is dispatched, the app will also be added to the system's temporary power exemption list for approximately 10 seconds to allow that application to acquire further wake locks in which to complete its work.

<br />

These alarms can significantly impact the power use of the device when idle (and thus cause significant battery blame to the app scheduling them), so they should be used with care. To reduce abuse, there are restrictions on how frequently these alarms will go off for a particular application. Under normal system operation, it will not dispatch these alarms more than about every minute (at which point every such pending alarm is dispatched); when in low-power idle modes this duration may be significantly longer, such as 15 minutes.

Unlike other alarms, the system is free to reschedule this type of alarm to happen out of order with any other alarms, even those from the same app. This will clearly happen when the device is idle (since this alarm can go off while idle, when any other alarms from the app will be held until later), but may also happen even when not idle.

Regardless of the app's target SDK version, this call always allows batching of the alarm.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): type of alarm. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME:kotlin.Int` |
| `triggerAtMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): time in milliseconds that the alarm should go off, using the appropriate clock (depending on the alarm type). |
| `operation` | [PendingIntent](PendingIntent.md): Action to perform when the alarm goes off; typically comes from getBroadcast. This value cannot be `null`. |
| --- | --- |

**See Also**

- set
- filterEquals
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME_WAKEUP:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC_WAKEUP:kotlin.Int`

### setExact

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setExact(
    type: Int, 
    triggerAtMillis: Long, 
    operation: PendingIntent
): Unit
```

Schedule an alarm to be delivered precisely at the stated time.

This method is like set, but does not permit the OS to adjust the delivery time. The alarm will be delivered as nearly as possible to the requested trigger time.

**Note:** only alarms for which there is a strong demand for exact-time delivery (such as an alarm clock ringing at the requested time) should be scheduled as exact. Applications are strongly discouraged from using exact alarms unnecessarily as they reduce the OS's ability to minimize battery use.

**Note:** Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps targeting SDK level 31 or higher need to request the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SCHEDULE_EXACT_ALARM:kotlin.String` permission to use this API, unless the app is exempt from battery restrictions. The user and the system can revoke this permission via the special app access screen in Settings.

**Note:** Exact alarms should only be used for user-facing features. For more details, see [Exact alarm permission](https://developer.android.com/about/versions/12/behavior-changes-12#exact-alarm-permission).

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): type of alarm. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME:kotlin.Int` |
| `triggerAtMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): time in milliseconds that the alarm should go off, using the appropriate clock (depending on the alarm type). |
| `operation` | [PendingIntent](PendingIntent.md): Action to perform when the alarm goes off; typically comes from getBroadcast. This value cannot be `null`. |
| --- | --- |

**See Also**

- setRepeating
- filterEquals
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME_WAKEUP:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC_WAKEUP:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SCHEDULE_EXACT_ALARM:kotlin.String`

### setExact

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setExact(
    type: Int, 
    triggerAtMillis: Long, 
    tag: String?, 
    listener: AlarmManager.OnAlarmListener, 
    targetHandler: Handler?
): Unit
```

Direct callback version of setExact. Rather than supplying a PendingIntent to be sent when the alarm time is reached, this variant supplies an `https://developer.android.com/reference/kotlin/android/app/AlarmManager.OnAlarmListener` instance that will be invoked at that time.

Listener based alarms may be canceled by the Android system whenever the calling process no longer has any components running, such as Activity, Service, or `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#`, so only use these APIs when you do not need to receive alarms after the current component finishes, and also make sure to [cancel(OnAlarmListener)](AlarmManager.md)) them when it does. For example, if you use these APIs from an Activity, make sure to cancel the respective alarms when the activity finishes. If you need to receive the alarm even after that, use the PendingIntent based APIs.

The OnAlarmListener's onAlarm method will be invoked via the specified target Handler, or on the application's main looper if `null` is passed as the `targetHandler` parameter.

On previous android versions `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, apps targeting SDK level 31 or higher needed to hold the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SCHEDULE_EXACT_ALARM:kotlin.String` permission to use this API, unless the app was exempt from battery restrictions.

**Note:** Starting with android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the system will explicitly drop any alarms set via this API when the calling app goes out of lifecycle.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME:kotlin.Int` |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `listener` | [AlarmManager.OnAlarmListener](../android/app/AlarmManager.OnAlarmListener.md): This value cannot be `null`. |
| --- | --- |
| `targetHandler` | [Handler](../android.os/Handler.md)?: This value may be `null`. |

### setExactAndAllowWhileIdle

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setExactAndAllowWhileIdle(
    type: Int, 
    triggerAtMillis: Long, 
    operation: PendingIntent
): Unit
```

Like setExact, but this alarm will be allowed to execute even when the system is in low-power idle modes. If you don't need exact scheduling of the alarm but still need to execute while idle, consider using setAndAllowWhileIdle. This type of alarm must **only** be used for situations where it is actually required that the alarm go off while in idle -- a reasonable example would be for a calendar notification that should make a sound so the user is aware of it. When the alarm is dispatched, the app will also be added to the system's temporary power exemption list for approximately 10 seconds to allow that application to acquire further wake locks in which to complete its work.

<br />

These alarms can significantly impact the power use of the device when idle (and thus cause significant battery blame to the app scheduling them), so they should be used with care. To reduce abuse, there are restrictions on how frequently these alarms will go off for a particular application. Under normal system operation, it will not dispatch these alarms more than about every minute (at which point every such pending alarm is dispatched); when in low-power idle modes this duration may be significantly longer, such as 15 minutes.

Unlike other alarms, the system is free to reschedule this type of alarm to happen out of order with any other alarms, even those from the same app. This will clearly happen when the device is idle (since this alarm can go off while idle, when any other alarms from the app will be held until later), but may also happen even when not idle. Note that the OS will allow itself more flexibility for scheduling these alarms than regular exact alarms, since the application has opted into this behavior. When the device is idle it may take even more liberties with scheduling in order to optimize for battery life.

**Note:** Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps targeting SDK level 31 or higher need to request the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SCHEDULE_EXACT_ALARM:kotlin.String` permission to use this API, unless the app is exempt from battery restrictions. The user and the system can revoke this permission via the special app access screen in Settings.

**Note:** Exact alarms should only be used for user-facing features. For more details, see [Exact alarm permission](https://developer.android.com/about/versions/12/behavior-changes-12#exact-alarm-permission).

Alarms scheduled via this API will be allowed to start a foreground service even if the app is in the background.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): type of alarm. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME:kotlin.Int` |
| `triggerAtMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): time in milliseconds that the alarm should go off, using the appropriate clock (depending on the alarm type). |
| `operation` | [PendingIntent](PendingIntent.md): Action to perform when the alarm goes off; typically comes from getBroadcast. This value cannot be `null`. |
| --- | --- |

**See Also**

- setRepeating
- filterEquals
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME_WAKEUP:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC_WAKEUP:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SCHEDULE_EXACT_ALARM:kotlin.String`

### setExactAndAllowWhileIdle

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setExactAndAllowWhileIdle(
    type: Int, 
    triggerAtMillis: Long, 
    tag: String, 
    executor: Executor, 
    listener: AlarmManager.OnAlarmListener
): Unit
```

Like setExact, but this alarm will be allowed to execute even when the system is in low-power idle modes.

Listener based alarms may be canceled by the Android system whenever the calling process no longer has any components running, such as Activity, Service, or `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#`, so only use these APIs when you do not need to receive alarms after the current component finishes, and also make sure to [cancel(OnAlarmListener)](AlarmManager.md)) them when it does. For example, if you use these APIs from an Activity, make sure to cancel the respective alarms when the activity finishes. If you need to receive the alarm even after that, use the PendingIntent based APIs.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): type of alarm. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME:kotlin.Int` |
| `triggerAtMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The exact time in milliseconds, that the alarm should be delivered, expressed in the appropriate clock's units (depending on the alarm type). |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A string tag used to identify this alarm in logs and battery-attribution. This value cannot be `null`. |
| --- | --- |
| `executor` | [Executor](../java.util.concurrent/Executor.md): The `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` on which to execute the listener's onAlarm() callback. This value cannot be `null`. |
| `listener` | [AlarmManager.OnAlarmListener](../android/app/AlarmManager.OnAlarmListener.md): `https://developer.android.com/reference/kotlin/android/app/AlarmManager.OnAlarmListener` instance whose onAlarm method will be called when the alarm time is reached. This value cannot be `null`. |

### setInexactRepeating

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInexactRepeating(
    type: Int, 
    triggerAtMillis: Long, 
    intervalMillis: Long, 
    operation: PendingIntent
): Unit
```

Schedule a repeating alarm that has inexact trigger time requirements; for example, an alarm that repeats every hour, but not necessarily at the top of every hour. These alarms are more power-efficient than the strict recurrences traditionally supplied by setRepeating, since the system can adjust alarms' delivery times to cause them to fire simultaneously, avoiding waking the device from sleep more than necessary.

Your alarm's first trigger will not be before the requested time, but it might not occur for almost a full interval after that time. In addition, while the overall period of the repeating alarm will be as requested, the time between any two successive firings of the alarm may vary. If your application demands very low jitter, use one-shot alarms with an appropriate window instead; see setWindow and setExact.

As of API 19, all repeating alarms are inexact. Because this method has been available since API 3, your application can safely call it and be assured that it will get similar behavior on both current and older versions of Android.

Apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` will need to set the flag `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_MUTABLE:kotlin.Int` on the PendingIntent being used to set this alarm, if they want the alarm count to be supplied with the key `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ALARM_COUNT:kotlin.String`.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): type of alarm. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME:kotlin.Int` |
| `triggerAtMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): time in milliseconds that the alarm should first go off, using the appropriate clock (depending on the alarm type). This is inexact: the alarm will not fire before this time, but there may be a delay of almost an entire alarm interval before the first invocation of the alarm. |
| `intervalMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): interval in milliseconds between subsequent repeats of the alarm. Prior to API 19, if this is one of INTERVAL_FIFTEEN_MINUTES, INTERVAL_HALF_HOUR, INTERVAL_HOUR, INTERVAL_HALF_DAY, or INTERVAL_DAY then the alarm will be phase-aligned with other alarms to reduce the number of wakeups. Otherwise, the alarm will be set as though the application had called setRepeating. As of API 19, all repeating alarms will be inexact and subject to batching with other alarms regardless of their stated repeat interval. |
| --- | --- |
| `operation` | [PendingIntent](PendingIntent.md): Action to perform when the alarm goes off; typically comes from getBroadcast. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/Handler.html#`
- filterEquals
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME_WAKEUP:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC_WAKEUP:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#INTERVAL_FIFTEEN_MINUTES:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#INTERVAL_HALF_HOUR:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#INTERVAL_HOUR:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#INTERVAL_HALF_DAY:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#INTERVAL_DAY:kotlin.Long`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ALARM_COUNT:kotlin.String`

### setRepeating

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRepeating(
    type: Int, 
    triggerAtMillis: Long, 
    intervalMillis: Long, 
    operation: PendingIntent
): Unit
```

Schedule a repeating alarm. **Note: for timing operations (ticks, timeouts, etc) it is easier and much more efficient to use `https://developer.android.com/reference/kotlin/android/os/Handler.html#`.** If there is already an alarm scheduled for the same IntentSender, it will first be canceled.

Like #set, except you can also supply a period at which the alarm will automatically repeat. This alarm continues repeating until explicitly removed with #cancel. If the stated trigger time is in the past, the alarm will be triggered immediately, with an alarm count depending on how far in the past the trigger time is relative to the repeat interval.

If an alarm is delayed (by system sleep, for example, for non _WAKEUP alarm types), a skipped repeat will be delivered as soon as possible. After that, future alarms will be delivered according to the original schedule; they do not drift over time. For example, if you have set a recurring alarm for the top of every hour but the phone was asleep from 7:45 until 8:45, an alarm will be sent as soon as the phone awakens, then the next alarm will be sent at 9:00.

If your application wants to allow the delivery times to drift in order to guarantee that at least a certain time interval always elapses between alarms, then the approach to take is to use one-time alarms, scheduling the next one yourself when handling each alarm delivery.

**Note:** as of API 19, all repeating alarms are inexact. If your application needs precise delivery times then it must use one-time exact alarms, rescheduling each time as described above. Legacy applications whose `targetSdkVersion` is earlier than API 19 will continue to have all of their alarms, including repeating alarms, treated as exact.

Apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` will need to set the flag `https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_MUTABLE:kotlin.Int` on the PendingIntent being used to set this alarm, if they want the alarm count to be supplied with the key `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ALARM_COUNT:kotlin.String`.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): type of alarm. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME:kotlin.Int` |
| `triggerAtMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): time in milliseconds that the alarm should first go off, using the appropriate clock (depending on the alarm type). |
| `intervalMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): interval in milliseconds between subsequent repeats of the alarm. |
| --- | --- |
| `operation` | [PendingIntent](PendingIntent.md): Action to perform when the alarm goes off; typically comes from getBroadcast. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/Handler.html#`
- filterEquals
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME_WAKEUP:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC_WAKEUP:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ALARM_COUNT:kotlin.String`

### setTime

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTime(millis: Long): Unit
```

Set the system wall clock time. Requires the permission android.permission.SET_TIME. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_TIME:kotlin.String`

| Parameters ||
|---|---|
| `millis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): time in milliseconds since the Epoch |

### setTimeZone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTimeZone(timeZone: String!): Unit
```

Sets the system's persistent default time zone. This is the time zone for all apps, even after a reboot. Use setDefault if you just want to change the time zone within your app, and even then prefer to pass an explicit `https://developer.android.com/reference/kotlin/java/util/TimeZone.html#` to APIs that require it rather than changing the time zone for all threads.

On android M and above, it is an error to pass in a non-Olson timezone to this function. Note that this is a bad idea on all Android releases because POSIX and the `TimeZone` class have opposite interpretations of `'+'` and `'-'` in the same non-Olson ID. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_TIME_ZONE:kotlin.String`

| Parameters ||
|---|---|
| `timeZone` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: one of the Olson ids from the list returned by java.util.TimeZone#getAvailableIDs |

### setWindow

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWindow(
    type: Int, 
    windowStartMillis: Long, 
    windowLengthMillis: Long, 
    operation: PendingIntent
): Unit
```

Schedule an alarm to be delivered within a given window of time. This method is similar to set, but allows the application to precisely control the degree to which its delivery might be adjusted by the OS. This method allows an application to take advantage of the battery optimizations that arise from delivery batching even when it has modest timeliness requirements for its alarms.

Note: Starting with API `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps should not pass in a window of less than 10 minutes. The system will try its best to accommodate smaller windows if the alarm is supposed to fire in the near future, but there are no guarantees and the app should expect any window smaller than 10 minutes to get elongated to 10 minutes.

This method can also be used to achieve strict ordering guarantees among multiple alarms by ensuring that the windows requested for each alarm do not intersect.

When precise delivery is not required, applications should use the standard set method. This will give the OS the most flexibility to minimize wakeups and battery use. For alarms that must be delivered at precisely-specified times with no acceptable variation, applications can use setExact.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): type of alarm. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME:kotlin.Int` |
| `windowStartMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The earliest time, in milliseconds, that the alarm should be delivered, expressed in the appropriate clock's units (depending on the alarm type). |
| `windowLengthMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The length of the requested delivery window, in milliseconds. The alarm will be delivered no later than this many milliseconds after `windowStartMillis`. Note that this parameter is a *duration,* not the timestamp of the end of the window. |
| --- | --- |
| `operation` | [PendingIntent](PendingIntent.md): Action to perform when the alarm goes off; typically comes from getBroadcast. This value cannot be `null`. |

**See Also**

- setRepeating
- filterEquals
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME_WAKEUP:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC_WAKEUP:kotlin.Int`

### setWindow

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWindow(
    type: Int, 
    windowStartMillis: Long, 
    windowLengthMillis: Long, 
    tag: String?, 
    listener: AlarmManager.OnAlarmListener, 
    targetHandler: Handler?
): Unit
```

Direct callback version of setWindow. Rather than supplying a PendingIntent to be sent when the alarm time is reached, this variant supplies an `https://developer.android.com/reference/kotlin/android/app/AlarmManager.OnAlarmListener` instance that will be invoked at that time.

Listener based alarms may be canceled by the Android system whenever the calling process no longer has any components running, such as Activity, Service, or `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#`, so only use these APIs when you do not need to receive alarms after the current component finishes, and also make sure to [cancel(OnAlarmListener)](AlarmManager.md)) them when it does. For example, if you use these APIs from an Activity, make sure to cancel the respective alarms when the activity finishes. If you need to receive the alarm even after that, use the PendingIntent based APIs.

The OnAlarmListener onAlarm method will be invoked via the specified target Handler, or on the application's main looper if `null` is passed as the `targetHandler` parameter.

Note: Starting with API `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps should not pass in a window of less than 10 minutes. The system will try its best to accommodate smaller windows if the alarm is supposed to fire in the near future, but there are no guarantees and the app should expect any window smaller than 10 minutes to get elongated to 10 minutes.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME:kotlin.Int` |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `listener` | [AlarmManager.OnAlarmListener](../android/app/AlarmManager.OnAlarmListener.md): This value cannot be `null`. |
| --- | --- |
| `targetHandler` | [Handler](../android.os/Handler.md)?: This value may be `null`. |

**See Also**

- setWindow

### setWindow

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWindow(
    type: Int, 
    windowStartMillis: Long, 
    windowLengthMillis: Long, 
    tag: String?, 
    executor: Executor, 
    listener: AlarmManager.OnAlarmListener
): Unit
```

Direct callback version of setWindow. Rather than supplying a PendingIntent to be sent when the alarm time is reached, this variant supplies an `https://developer.android.com/reference/kotlin/android/app/AlarmManager.OnAlarmListener` instance that will be invoked at that time.

Listener based alarms may be canceled by the Android system whenever the calling process no longer has any components running, such as Activity, Service, or `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#`, so only use these APIs when you do not need to receive alarms after the current component finishes, and also make sure to [cancel(OnAlarmListener)](AlarmManager.md)) them when it does. For example, if you use these APIs from an Activity, make sure to cancel the respective alarms when the activity finishes. If you need to receive the alarm even after that, use the PendingIntent based APIs.

The OnAlarmListener onAlarm method will be invoked via the specified target Executor.

Note: Starting with API `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps should not pass in a window of less than 10 minutes. The system will try its best to accommodate smaller windows if the alarm is supposed to fire in the near future, but there are no guarantees and the app should expect any window smaller than 10 minutes to get elongated to 10 minutes.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#RTC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME_WAKEUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AlarmManager#ELAPSED_REALTIME:kotlin.Int` |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): This value cannot be `null`. |
| --- | --- |
| `listener` | [AlarmManager.OnAlarmListener](../android/app/AlarmManager.OnAlarmListener.md): This value cannot be `null`. |

**See Also**

- setWindow

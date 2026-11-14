# AlarmManager.OnAlarmListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnAlarmListener

Kotlin| [Java](https://developer.android.com/reference/android/app/AlarmManager.OnAlarmListener "View this page in Java") 

```
interface OnAlarmListener
```

| [android.app.AlarmManager.OnAlarmListener](https://developer.android.com/reference/kotlin/android/app/AlarmManager.OnAlarmListener#) |

Direct-notification alarms: the requester must be running continuously from the time the alarm is set to the time it is delivered, or delivery will fail. Only one-shot alarms can be set using this mechanism, not repeating alarms.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAlarm](https://developer.android.com/reference/kotlin/android/app/AlarmManager.OnAlarmListener#onAlarm())`()` Callback method that is invoked by the system when the alarm time is reached. |

## Public methods

### onAlarm

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAlarm(): Unit
```

Callback method that is invoked by the system when the alarm time is reached.

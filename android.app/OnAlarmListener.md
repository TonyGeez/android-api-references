# AlarmManager.OnAlarmListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnAlarmListener

Kotlin| [Java](../android/app/AlarmManager.OnAlarmListener.md) 
| --- | --- |

```
interface OnAlarmListener
```

| [android.app.AlarmManager.OnAlarmListener](../android/app/AlarmManager.OnAlarmListener.md) |

Direct-notification alarms: the requester must be running continuously from the time the alarm is set to the time it is delivered, or delivery will fail. Only one-shot alarms can be set using this mechanism, not repeating alarms.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAlarm](../android/app/AlarmManager.OnAlarmListener.md))`()` Callback method that is invoked by the system when the alarm time is reached. |

## Public methods

### onAlarm

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAlarm(): Unit
```

Callback method that is invoked by the system when the alarm time is reached.

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AlarmClock

```
class AlarmClock
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.provider.AlarmClock](https://developer.android.com/reference/kotlin/android/provider/AlarmClock#) |

The AlarmClock provider contains an Intent action and extras that can be used to start an Activity to set a new alarm or timer in an alarm clock application. Applications that wish to receive the ACTION_SET_ALARM, ACTION_SET_TIMER, ACTION_DISMISS_ALARM, ACTION_DISMISS_TIMER, and ACTION_SNOOZE_ALARM Intents should create an activity to handle the Intent that requires the permission, com.android.alarm.permission.SET_ALARM. Applications that wish to create a new alarm or timer should use android.content.Context#startActivity so that the user has the option of choosing which alarm clock application to use. Android TV devices may not support the alarm intents.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_DISMISS_ALARM:kotlin.String` Activity Action: Dismiss an alarm. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_DISMISS_TIMER:kotlin.String` Activity Action: Dismiss a timer. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_ALARM:kotlin.String` Activity Action: Set an alarm. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_TIMER:kotlin.String` Activity Action: Set a timer. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SHOW_ALARMS:kotlin.String` Activity Action: Show the alarms. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SHOW_TIMERS:kotlin.String` Activity Action: Show the timers. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SNOOZE_ALARM:kotlin.String` Activity Action: Snooze a currently ringing alarm. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ALARM_SEARCH_MODE_ALL:kotlin.String` Selects all alarms. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ALARM_SEARCH_MODE_LABEL:kotlin.String` Search by alarm label. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ALARM_SEARCH_MODE_NEXT:kotlin.String` Selects the alarm that will ring next, or the alarm that is currently ringing, if any. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ALARM_SEARCH_MODE_TIME:kotlin.String` Search for the alarm that is most closely matched by the search parameters `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_HOUR:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_MINUTES:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_IS_PM:kotlin.String`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_ALARM_SEARCH_MODE:kotlin.String` Bundle extra: Specify the type of search mode to look up an alarm. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_ALARM_SNOOZE_DURATION:kotlin.String` Bundle extra: The snooze duration of the alarm in minutes. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_DAYS:kotlin.String` Bundle extra: Weekdays for repeating alarm. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_HOUR:kotlin.String` Bundle extra: The hour of the alarm. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_IS_PM:kotlin.String` Bundle extra: The AM/PM of the alarm. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_LENGTH:kotlin.String` Bundle extra: The length of the timer in seconds. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_MESSAGE:kotlin.String` Bundle extra: A custom message for the alarm or timer. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_MINUTES:kotlin.String` Bundle extra: The minutes of the alarm. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_RINGTONE:kotlin.String` Bundle extra: A ringtone to be played with this alarm. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_SKIP_UI:kotlin.String` Bundle extra: Whether or not to display an activity after performing the action. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_VIBRATE:kotlin.String` Bundle extra: Whether or not to activate the device vibrator. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#VALUE_RINGTONE_SILENT:kotlin.String` Bundle extra value: Indicates no ringtone should be played. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#AlarmClock()()` <br /> |

## Constants

### ACTION_DISMISS_ALARM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DISMISS_ALARM: String
```

Activity Action: Dismiss an alarm.

The alarm to dismiss can be specified or searched for in one of the following ways:

1. The Intent's data URI, which represents a deeplink to the alarm.
2. The extra `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_ALARM_SEARCH_MODE:kotlin.String` to determine how to search for the alarm.

<br />

If neither of the above are given then:

- If exactly one active alarm exists, it is dismissed.
- If more than one active alarm exists, the user is prompted to choose the alarm to dismiss.

<br />

If the extra `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_ALARM_SEARCH_MODE:kotlin.String` is used, and the search results contain two or more matching alarms, then the implementation should show an UI with the results and allow the user to select the alarm to dismiss. If the implementation supports `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_VOICE:kotlin.String` and the activity is started in Voice Interaction mode (i.e. check `https://developer.android.com/reference/kotlin/android/app/Activity.html#isVoiceInteraction()`), then the implementation should additionally use `https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.PickOptionRequest.html#` to start a voice interaction follow-on flow to help the user disambiguate the alarm by voice.

If the specified alarm is a single occurrence alarm, then dismissing it effectively disables the alarm; it will never ring again unless explicitly re-enabled.

If the specified alarm is a repeating alarm, then dismissing it only prevents the upcoming instance from ringing. The alarm remains enabled so that it will still ring on the date and time of the next instance (i.e. the instance after the upcoming one).

 Value: "android.intent.action.DISMISS_ALARM"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_ALARM_SEARCH_MODE:kotlin.String`

### ACTION_DISMISS_TIMER

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DISMISS_TIMER: String
```

Activity Action: Dismiss a timer.

The timer to dismiss should be specified using the Intent's data URI, which represents a deeplink to the timer.

If no data URI is provided, dismiss all expired timers.

This intent requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_ALARM:kotlin.String` permission.

 Value: "android.intent.action.DISMISS_TIMER"

### ACTION_SET_ALARM

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SET_ALARM: String
```

Activity Action: Set an alarm.

Activates an existing alarm or creates a new one.

This action requests an alarm to be set for a given time of day. If no time of day is specified, an implementation should start an activity that is capable of setting an alarm (`https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_SKIP_UI:kotlin.String` is ignored in this case). If a time of day is specified, and `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_SKIP_UI:kotlin.String` is `true`, and the alarm is not repeating, the implementation should remove this alarm after it has been dismissed. If an identical alarm exists matching all parameters, the implementation may re-use it instead of creating a new one (in this case, the alarm should not be removed after dismissal).

This action always enables the alarm.

This activity could also be started in Voice Interaction mode. The activity should check `https://developer.android.com/reference/kotlin/android/app/Activity.html#isVoiceInteraction()`, and if true, the implementation should report a deeplink of the created/enabled alarm using `https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.CompleteVoiceRequest.html#`. This allows follow-on voice actions such as `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_DISMISS_ALARM:kotlin.String` to dismiss the alarm that was just enabled.

### Request parameters

- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_HOUR:kotlin.String` *(optional)*: The hour of the alarm being set.
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_MINUTES:kotlin.String` *(optional)*: The minutes of the alarm being set.
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_DAYS:kotlin.String` *(optional)*: Weekdays for repeating alarm.
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_MESSAGE:kotlin.String` *(optional)*: A custom message for the alarm.
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_RINGTONE:kotlin.String` *(optional)*: A ringtone to play with this alarm.
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_VIBRATE:kotlin.String` *(optional)*: Whether or not to activate the device vibrator for this alarm.
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_SKIP_UI:kotlin.String` *(optional)*: Whether or not to display an activity for setting this alarm.

 Value: "android.intent.action.SET_ALARM"

### ACTION_SET_TIMER

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SET_TIMER: String
```

Activity Action: Set a timer.

Activates an existing timer or creates a new one.

This action requests a timer to be started for a specific `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_LENGTH:kotlin.String` of time. If no `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_LENGTH:kotlin.String` is specified, the implementation should start an activity that is capable of setting a timer (`https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_SKIP_UI:kotlin.String` is ignored in this case). If a `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_LENGTH:kotlin.String` is specified, and `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_SKIP_UI:kotlin.String` is `true`, the implementation should remove this timer after it has been dismissed. If an identical, unused timer exists matching both parameters, an implementation may re-use it instead of creating a new one (in this case, the timer should not be removed after dismissal). This action always starts the timer.

### Request parameters

- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_LENGTH:kotlin.String` *(optional)*: The length of the timer being set.
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_MESSAGE:kotlin.String` *(optional)*: A custom message for the timer.
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_SKIP_UI:kotlin.String` *(optional)*: Whether or not to display an activity for setting this timer.

This intent requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_ALARM:kotlin.String` permission.

 Value: "android.intent.action.SET_TIMER"

### ACTION_SHOW_ALARMS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SHOW_ALARMS: String
```

Activity Action: Show the alarms.

This action opens the alarms page.

 Value: "android.intent.action.SHOW_ALARMS"

### ACTION_SHOW_TIMERS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SHOW_TIMERS: String
```

Activity Action: Show the timers.

This action opens the timers page.

 Value: "android.intent.action.SHOW_TIMERS"

### ACTION_SNOOZE_ALARM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SNOOZE_ALARM: String
```

Activity Action: Snooze a currently ringing alarm.

Snoozes the currently ringing alarm. The extra `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_ALARM_SNOOZE_DURATION:kotlin.String` can be optionally set to specify the snooze duration; if unset, the implementation should use a reasonable default, for example 10 minutes. The alarm should ring again after the snooze duration.

Any application that wants to use this action should also be granted the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_ALARM:kotlin.String` permission.

Note: setting the extra `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_ALARM_SNOOZE_DURATION:kotlin.String` does not change the default snooze duration; it's only applied to the currently ringing alarm.

If there is no currently ringing alarm, then this is a no-op.

 Value: "android.intent.action.SNOOZE_ALARM"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_ALARM_SNOOZE_DURATION:kotlin.String`

### ALARM_SEARCH_MODE_ALL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALARM_SEARCH_MODE_ALL: String
```

Selects all alarms.

 Value: "android.all"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_ALARM_SEARCH_MODE:kotlin.String`

### ALARM_SEARCH_MODE_LABEL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALARM_SEARCH_MODE_LABEL: String
```

Search by alarm label. Should return alarms that contain the word or phrase in given label.

 Value: "android.label"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_ALARM_SEARCH_MODE:kotlin.String`

### ALARM_SEARCH_MODE_NEXT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALARM_SEARCH_MODE_NEXT: String
```

Selects the alarm that will ring next, or the alarm that is currently ringing, if any.

 Value: "android.next"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_ALARM_SEARCH_MODE:kotlin.String`

### ALARM_SEARCH_MODE_TIME

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALARM_SEARCH_MODE_TIME: String
```

Search for the alarm that is most closely matched by the search parameters `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_HOUR:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_MINUTES:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_IS_PM:kotlin.String`. In this search mode, at least one of these additional extras are required.

- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_HOUR:kotlin.String` - The hour to search for the alarm.
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_MINUTES:kotlin.String` - The minute to search for the alarm.
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_IS_PM:kotlin.String` - Whether the hour is AM or PM.

<br />

 Value: "android.time"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_ALARM_SEARCH_MODE:kotlin.String`

### EXTRA_ALARM_SEARCH_MODE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ALARM_SEARCH_MODE: String
```

Bundle extra: Specify the type of search mode to look up an alarm.

For example, used by `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_DISMISS_ALARM:kotlin.String` to identify the alarm to dismiss.

This extra is only used when the alarm is not already identified by a deeplink as specified in the Intent's data URI.

The value of this extra is a `https://developer.android.com/reference/kotlin/java/lang/String.html#`, restricted to the following set of supported search modes:

- *Time* - `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ALARM_SEARCH_MODE_TIME:kotlin.String`: Selects the alarm that is most closely matched by the search parameters `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_HOUR:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_MINUTES:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_IS_PM:kotlin.String`.
- *Next alarm* - `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ALARM_SEARCH_MODE_NEXT:kotlin.String`: Selects the alarm that will ring next, or the alarm that is currently ringing, if any.
- *All alarms* - `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ALARM_SEARCH_MODE_ALL:kotlin.String`: Selects all alarms.
- *Label* - `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ALARM_SEARCH_MODE_LABEL:kotlin.String`: Search by alarm label. Should return alarms that contain the word or phrase in given label.

<br />

 Value: "android.intent.extra.alarm.SEARCH_MODE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ALARM_SEARCH_MODE_TIME:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ALARM_SEARCH_MODE_NEXT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ALARM_SEARCH_MODE_ALL:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ALARM_SEARCH_MODE_LABEL:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_DISMISS_ALARM:kotlin.String`

### EXTRA_ALARM_SNOOZE_DURATION

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ALARM_SNOOZE_DURATION: String
```

Bundle extra: The snooze duration of the alarm in minutes.

Used by `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SNOOZE_ALARM:kotlin.String`. This extra is optional and the value is an `https://developer.android.com/reference/kotlin/java/lang/Integer.html#` that specifies the duration in minutes for which to snooze the alarm.

 Value: "android.intent.extra.alarm.SNOOZE_DURATION"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SNOOZE_ALARM:kotlin.String`

### EXTRA_DAYS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DAYS: String
```

Bundle extra: Weekdays for repeating alarm.

Used by `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_ALARM:kotlin.String`.

The value is an `ArrayList<Integer>`. Each item can be:

- `https://developer.android.com/reference/kotlin/java/util/Calendar.html#SUNDAY:kotlin.Int`,
- `https://developer.android.com/reference/kotlin/java/util/Calendar.html#MONDAY:kotlin.Int`,
- `https://developer.android.com/reference/kotlin/java/util/Calendar.html#TUESDAY:kotlin.Int`,
- `https://developer.android.com/reference/kotlin/java/util/Calendar.html#WEDNESDAY:kotlin.Int`,
- `https://developer.android.com/reference/kotlin/java/util/Calendar.html#THURSDAY:kotlin.Int`,
- `https://developer.android.com/reference/kotlin/java/util/Calendar.html#FRIDAY:kotlin.Int`,
- `https://developer.android.com/reference/kotlin/java/util/Calendar.html#SATURDAY:kotlin.Int`

 Value: "android.intent.extra.alarm.DAYS"

### EXTRA_HOUR

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_HOUR: String
```

Bundle extra: The hour of the alarm.

Used by `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_ALARM:kotlin.String`.

This extra is optional. If not provided, an implementation should open an activity that allows a user to set an alarm with user provided time.

The value is an `https://developer.android.com/reference/kotlin/java/lang/Integer.html#` and ranges from 0 to 23.

 Value: "android.intent.extra.alarm.HOUR"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_ALARM:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_MINUTES:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_DAYS:kotlin.String`

### EXTRA_IS_PM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_IS_PM: String
```

Bundle extra: The AM/PM of the alarm.

Used by `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_DISMISS_ALARM:kotlin.String`.

This extra is optional and only used when `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_ALARM_SEARCH_MODE:kotlin.String` is set to `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ALARM_SEARCH_MODE_TIME:kotlin.String`. In this search mode, the `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_IS_PM:kotlin.String` is used together with `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_HOUR:kotlin.String` and `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_MINUTES:kotlin.String`. The implementation should look up the alarm that is most closely matched by these search parameters. If `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_IS_PM:kotlin.String` is missing, then the AM/PM of the specified `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_HOUR:kotlin.String` is ambiguous and the implementation should ask for clarification from the user.

The value is a `https://developer.android.com/reference/kotlin/java/lang/Boolean.html#`, where false=AM and true=PM.

 Value: "android.intent.extra.alarm.IS_PM"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_DISMISS_ALARM:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_HOUR:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_MINUTES:kotlin.String`

### EXTRA_LENGTH

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_LENGTH: String
```

Bundle extra: The length of the timer in seconds.

Used by `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_TIMER:kotlin.String`.

This extra is optional. If not provided, an implementation should open an activity that allows a user to set a timer with user provided length.

The value is an `https://developer.android.com/reference/kotlin/java/lang/Integer.html#` and ranges from 1 to 86400 (24 hours).

 Value: "android.intent.extra.alarm.LENGTH"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_TIMER:kotlin.String`

### EXTRA_MESSAGE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MESSAGE: String
```

Bundle extra: A custom message for the alarm or timer.

Used by `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_ALARM:kotlin.String` and `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_TIMER:kotlin.String`.

The value is a `https://developer.android.com/reference/kotlin/java/lang/String.html#`.

 Value: "android.intent.extra.alarm.MESSAGE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_ALARM:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_TIMER:kotlin.String`

### EXTRA_MINUTES

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MINUTES: String
```

Bundle extra: The minutes of the alarm.

Used by `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_ALARM:kotlin.String`.

The value is an `https://developer.android.com/reference/kotlin/java/lang/Integer.html#` and ranges from 0 to 59. If not provided, it defaults to 0.

 Value: "android.intent.extra.alarm.MINUTES"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_ALARM:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_HOUR:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_DAYS:kotlin.String`

### EXTRA_RINGTONE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_RINGTONE: String
```

Bundle extra: A ringtone to be played with this alarm.

Used by `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_ALARM:kotlin.String`.

This value is a `https://developer.android.com/reference/kotlin/java/lang/String.html#` and can either be set to `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#VALUE_RINGTONE_SILENT:kotlin.String` or to a content URI of the media to be played. If not specified or the URI doesn't exist, `"content://settings/system/alarm_alert` will be used.

 Value: "android.intent.extra.alarm.RINGTONE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_ALARM:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#VALUE_RINGTONE_SILENT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_VIBRATE:kotlin.String`

### EXTRA_SKIP_UI

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SKIP_UI: String
```

Bundle extra: Whether or not to display an activity after performing the action.

Used by `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_ALARM:kotlin.String` and `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_TIMER:kotlin.String`.

If true, the application is asked to bypass any intermediate UI. If false, the application may display intermediate UI like a confirmation dialog or settings.

The value is a `https://developer.android.com/reference/kotlin/java/lang/Boolean.html#`. The default is `false`.

 Value: "android.intent.extra.alarm.SKIP_UI"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_ALARM:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_TIMER:kotlin.String`

### EXTRA_VIBRATE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_VIBRATE: String
```

Bundle extra: Whether or not to activate the device vibrator.

Used by `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_ALARM:kotlin.String`.

The value is a `https://developer.android.com/reference/kotlin/java/lang/Boolean.html#`. The default is `true`.

 Value: "android.intent.extra.alarm.VIBRATE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_ALARM:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_RINGTONE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#VALUE_RINGTONE_SILENT:kotlin.String`

### VALUE_RINGTONE_SILENT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VALUE_RINGTONE_SILENT: String
```

Bundle extra value: Indicates no ringtone should be played.

Used by `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_ALARM:kotlin.String`, passed in through `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_RINGTONE:kotlin.String`.

 Value: "silent"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#ACTION_SET_ALARM:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_RINGTONE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/AlarmClock#EXTRA_VIBRATE:kotlin.String`

## Public constructors

### AlarmClock

```
AlarmClock()
```

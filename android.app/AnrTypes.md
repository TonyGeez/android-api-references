Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnrTypes

```
class AnrTypes
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.AnrTypes](https://developer.android.com/reference/kotlin/android/app/AnrTypes#) |

Defines the types of Application Not Responding (ANR) errors.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AnrTypes#ANR_TYPE_APPLICATION_START:kotlin.Int` The app took too long to start up. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AnrTypes#ANR_TYPE_APP_TRIGGERED:kotlin.Int` The app itself due to its own internal logic or behavior has triggered an ANR. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AnrTypes#ANR_TYPE_BROADCAST_OF_INTENT:kotlin.Int` The app's broadcast receiver took too long to process the message. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AnrTypes#ANR_TYPE_CONTENT_PROVIDER_NOT_RESPONDING:kotlin.Int` The app's content provider took too long to respond. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AnrTypes#ANR_TYPE_EXECUTE_SERVICE:kotlin.Int` The app's service took too long to finish `https://developer.android.com/reference/kotlin/android/app/Service#onCreate()` and `https://developer.android.com/reference/kotlin/android/app/Service#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` / `https://developer.android.com/reference/kotlin/android/app/Service#onBind(android.content.Intent)` |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AnrTypes#ANR_TYPE_FOREGROUND_SHORT_SERVICE_TIMEOUT:kotlin.Int` A foreground short service took too long to respond to android. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AnrTypes#ANR_TYPE_INPUT_DISPATCH:kotlin.Int` The app took too long to respond to an input event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AnrTypes#ANR_TYPE_INPUT_DISPATCH_NO_FOCUSED_WINDOW:kotlin.Int` The app took too long to respond to an input event because no window was focused. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AnrTypes#ANR_TYPE_JOB_SERVICE_START:kotlin.Int` The job service took too long to start. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AnrTypes#ANR_TYPE_OTHER:kotlin.Int` The ANR type is not one of the other defined types. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AnrTypes#ANR_TYPE_START_FOREGROUND_SERVICE:kotlin.Int` The foreground service took too long to start. |

## Constants

### ANR_TYPE_APPLICATION_START

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ANR_TYPE_APPLICATION_START: Int
```

The app took too long to start up.

 Value: 10

### ANR_TYPE_APP_TRIGGERED

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ANR_TYPE_APP_TRIGGERED: Int
```

The app itself due to its own internal logic or behavior has triggered an ANR.

 Value: 7

### ANR_TYPE_BROADCAST_OF_INTENT

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ANR_TYPE_BROADCAST_OF_INTENT: Int
```

The app's broadcast receiver took too long to process the message.

 Value: 3

### ANR_TYPE_CONTENT_PROVIDER_NOT_RESPONDING

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ANR_TYPE_CONTENT_PROVIDER_NOT_RESPONDING: Int
```

The app's content provider took too long to respond.

 Value: 6

### ANR_TYPE_EXECUTE_SERVICE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ANR_TYPE_EXECUTE_SERVICE: Int
```

The app's service took too long to finish `https://developer.android.com/reference/kotlin/android/app/Service#onCreate()` and `https://developer.android.com/reference/kotlin/android/app/Service#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` / `https://developer.android.com/reference/kotlin/android/app/Service#onBind(android.content.Intent)`

 Value: 5

### ANR_TYPE_FOREGROUND_SHORT_SERVICE_TIMEOUT

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ANR_TYPE_FOREGROUND_SHORT_SERVICE_TIMEOUT: Int
```

A foreground short service took too long to respond to android.app.Service#onTimeout.

 Value: 8

### ANR_TYPE_INPUT_DISPATCH

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ANR_TYPE_INPUT_DISPATCH: Int
```

The app took too long to respond to an input event.

 Value: 2

### ANR_TYPE_INPUT_DISPATCH_NO_FOCUSED_WINDOW

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ANR_TYPE_INPUT_DISPATCH_NO_FOCUSED_WINDOW: Int
```

The app took too long to respond to an input event because no window was focused.

 Value: 1

### ANR_TYPE_JOB_SERVICE_START

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ANR_TYPE_JOB_SERVICE_START: Int
```

The job service took too long to start.

 Value: 9

### ANR_TYPE_OTHER

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ANR_TYPE_OTHER: Int
```

The ANR type is not one of the other defined types.

This is used as a default when the specific cause of the ANR is not known or does not fit into a more specific category

 Value: 0

### ANR_TYPE_START_FOREGROUND_SERVICE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ANR_TYPE_START_FOREGROUND_SERVICE: Int
```

The foreground service took too long to start.

 Value: 4

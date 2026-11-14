Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppInteractionDeniedException

```
open class AppInteractionDeniedException : AppInteractionException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [android.app.AppInteractionException](https://developer.android.com/reference/kotlin/android/app/AppInteractionException) ||
| | | | ↳ | [android.app.AppInteractionDeniedException](https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException#) |

Exception thrown when an app interaction is denied.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException#REASON_AUTO_DENIED:kotlin.Int` Auto denied the interaction. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException#REASON_UNKNOWN:kotlin.Int` Unknown reason for denied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException#REASON_USER_DENIED:kotlin.Int` User denied the interaction. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException#AppInteractionDeniedException(kotlin.String,%20kotlin.Int)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, reason: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructor for `https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException#`. |
| `https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException#AppInteractionDeniedException(kotlin.String,%20kotlin.Int,%20android.os.Bundle)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, reason: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#)` Constructor for `https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException#`. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException#getReason()()` Returns the reason for interaction denied. |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/app/AppInteractionException` `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` `https://developer.android.com/reference/kotlin/android/app/AppInteractionException#getExtras()()`

Returns the additional metadata for this exception.

<br />

## Constants

### REASON_AUTO_DENIED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_AUTO_DENIED: Int
```

Auto denied the interaction.

This means that the user was not shown a dialog and the interaction was denied by the system automatically. This could happen because the user has previously denied the interaction already.

 Value: 2

### REASON_UNKNOWN

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_UNKNOWN: Int
```

Unknown reason for denied.

 Value: 0

### REASON_USER_DENIED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_USER_DENIED: Int
```

User denied the interaction.

This means that the user was shown a dialog and explicitly denied the access.

 Value: 1

## Public constructors

### AppInteractionDeniedException

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AppInteractionDeniedException(
    message: String?, 
    reason: Int)
```

Constructor for `https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException#`.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The error message. This value may be `null`. |
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The reason for interaction denied. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException#REASON_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException#REASON_USER_DENIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException#REASON_AUTO_DENIED:kotlin.Int` |

### AppInteractionDeniedException

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AppInteractionDeniedException(
    message: String?, 
    reason: Int, 
    extras: Bundle)
```

Constructor for `https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException#`.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The error message. This value may be `null`. |
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The reason for interaction denied. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException#REASON_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException#REASON_USER_DENIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException#REASON_AUTO_DENIED:kotlin.Int` |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): Additional metadata. This value cannot be `null`. |

## Public methods

### getReason

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getReason(): Int
```

Returns the reason for interaction denied.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The reason for interaction denied. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException#REASON_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException#REASON_USER_DENIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException#REASON_AUTO_DENIED:kotlin.Int` |

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppInteractionException

```
open class AppInteractionException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [android.app.AppInteractionException](https://developer.android.com/reference/kotlin/android/app/AppInteractionException#) |

Known Direct Subclasses [AppInteractionDeniedException](https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException) [AppInteractionDeniedException](https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException) Exception thrown when an app interaction is denied.

Exception thrown when an app interaction operation fails.

## Summary

| Public methods ||
|---|---|
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | `https://developer.android.com/reference/kotlin/android/app/AppInteractionException#getExtras()()` Returns the additional metadata for this exception. |

## Public methods

### getExtras

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getExtras(): Bundle
```

Returns the additional metadata for this exception.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` | The additional metadata. This value cannot be `null`. |

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppInteractionException

```
open class AppInteractionException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [android.app.AppInteractionException](../android/app/AppInteractionException.md) |
| --- | --- | --- | --- |

Known Direct Subclasses [AppInteractionDeniedException](../android/app/AppInteractionDeniedException.md) [AppInteractionDeniedException](../android/app/AppInteractionDeniedException.md) Exception thrown when an app interaction is denied.

Exception thrown when an app interaction operation fails.

## Summary

| Public methods ||
|---|---|
| open [Bundle](../android/os/Bundle.md) | `https://developer.android.com/reference/kotlin/android/app/AppInteractionException#getExtras()()` Returns the additional metadata for this exception. |

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

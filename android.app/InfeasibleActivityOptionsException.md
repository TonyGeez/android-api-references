Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InfeasibleActivityOptionsException

```
open class InfeasibleActivityOptionsException : AndroidRuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.util.AndroidRuntimeException](https://developer.android.com/reference/kotlin/android/util/AndroidRuntimeException.html#) ||
| | | | | ↳ | [android.app.InfeasibleActivityOptionsException](https://developer.android.com/reference/kotlin/android/app/InfeasibleActivityOptionsException#) |

This exception is thrown when a call to android.content.Context#startActivity or one of its variants fails because it is not possible to satisfy requirements specified in the `https://developer.android.com/reference/kotlin/android/app/ActivityOptions` passed in the android.content.Context#startActivity call.

## Summary

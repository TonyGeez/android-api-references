Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InfeasibleActivityOptionsException

```
open class InfeasibleActivityOptionsException : AndroidRuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.util.AndroidRuntimeException](../android.util/AndroidRuntimeException.md) ||
| | | | | ↳ | [android.app.InfeasibleActivityOptionsException](InfeasibleActivityOptionsException.md) |

This exception is thrown when a call to android.content.Context#startActivity or one of its variants fails because it is not possible to satisfy requirements specified in the `https://developer.android.com/reference/kotlin/android/app/ActivityOptions` passed in the android.content.Context#startActivity call.

## Summary

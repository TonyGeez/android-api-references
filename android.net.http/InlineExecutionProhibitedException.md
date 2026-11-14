# InlineExecutionProhibitedException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# InlineExecutionProhibitedException

Kotlin| [Java](InlineExecutionProhibitedException.md) 
| --- | --- |

```
class InlineExecutionProhibitedException : RejectedExecutionException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.util.concurrent.RejectedExecutionException](../java.util.concurrent/RejectedExecutionException.md) ||
| | | | | ↳ | [android.net.http.InlineExecutionProhibitedException](InlineExecutionProhibitedException.md) |

Thrown when an executor runs a submitted runnable inline in [java.util.concurrent.Executor#execute(Runnable)](../java.util.concurrent/Executor.md))and [android.net.http.UrlRequest.Builder#setDirectExecutorAllowed](../android/net/http/UrlRequest.Builder.md))was not called.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InlineExecutionProhibitedException](InlineExecutionProhibitedException.md))`()` <br /> |

## Public constructors

### InlineExecutionProhibitedException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
InlineExecutionProhibitedException()
```

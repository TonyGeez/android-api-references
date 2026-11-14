# InlineExecutionProhibitedException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# InlineExecutionProhibitedException

Kotlin| [Java](https://developer.android.com/reference/android/net/http/InlineExecutionProhibitedException "View this page in Java") 

```
class InlineExecutionProhibitedException : RejectedExecutionException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| | | | ↳ | [java.util.concurrent.RejectedExecutionException](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionException.html#) ||
| | | | | ↳ | [android.net.http.InlineExecutionProhibitedException](https://developer.android.com/reference/kotlin/android/net/http/InlineExecutionProhibitedException#) |

Thrown when an executor runs a submitted runnable inline in [java.util.concurrent.Executor#execute(Runnable)](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#execute(java.lang.Runnable))and [android.net.http.UrlRequest.Builder#setDirectExecutorAllowed](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setDirectExecutorAllowed(kotlin.Boolean))was not called.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InlineExecutionProhibitedException](https://developer.android.com/reference/kotlin/android/net/http/InlineExecutionProhibitedException#InlineExecutionProhibitedException())`()` <br /> |

## Public constructors

### InlineExecutionProhibitedException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
InlineExecutionProhibitedException()
```

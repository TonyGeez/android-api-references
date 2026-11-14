# NetworkOnMainThreadException

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NetworkOnMainThreadException

Kotlin| [Java](https://developer.android.com/reference/android/os/NetworkOnMainThreadException "View this page in Java") 
| --- | --- |

```
open class NetworkOnMainThreadException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.os.NetworkOnMainThreadException](https://developer.android.com/reference/kotlin/android/os/NetworkOnMainThreadException#) |

The exception that is thrown when an application attempts to perform a networking operation on its main thread.

This is only thrown for applications targeting the Honeycomb SDK or higher. Applications targeting earlier SDK versions are allowed to do networking on their main event loop threads, but it's heavily discouraged. See the document [Designing for Responsiveness](https://developer.android.com/guide/practices/design/responsiveness.html).

Also see [StrictMode](https://developer.android.com/reference/kotlin/android/os/StrictMode).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NetworkOnMainThreadException](https://developer.android.com/reference/kotlin/android/os/NetworkOnMainThreadException#NetworkOnMainThreadException())`()` <br /> |

## Public constructors

### NetworkOnMainThreadException

```
NetworkOnMainThreadException()
```

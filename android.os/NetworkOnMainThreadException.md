# NetworkOnMainThreadException

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NetworkOnMainThreadException

Kotlin| [Java](NetworkOnMainThreadException.md) 
| --- | --- |

```
open class NetworkOnMainThreadException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.os.NetworkOnMainThreadException](NetworkOnMainThreadException.md) |

The exception that is thrown when an application attempts to perform a networking operation on its main thread.

This is only thrown for applications targeting the Honeycomb SDK or higher. Applications targeting earlier SDK versions are allowed to do networking on their main event loop threads, but it's heavily discouraged. See the document [Designing for Responsiveness](https://developer.android.com/guide/practices/design/responsiveness.html).

Also see [StrictMode](StrictMode.md).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NetworkOnMainThreadException](NetworkOnMainThreadException.md))`()` <br /> |

## Public constructors

### NetworkOnMainThreadException

```
NetworkOnMainThreadException()
```

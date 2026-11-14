# IkeNonProtocolException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeNonProtocolException

Kotlin| [Java](https://developer.android.com/reference/android/net/ipsec/ike/exceptions/IkeNonProtocolException "View this page in Java") 

```
abstract class IkeNonProtocolException : IkeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [android.net.ipsec.ike.exceptions.IkeException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeException) ||
| | | | ↳ | [android.net.ipsec.ike.exceptions.IkeNonProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeNonProtocolException#) |

| Known Direct Subclasses [IkeIOException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeIOException), [IkeInternalException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeInternalException), [IkeNetworkLostException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeNetworkLostException) |------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [IkeIOException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeIOException) | Wrapper for I/O exceptions encountered during IKE operations. | | [IkeInternalException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeInternalException) | IkeInternalException encapsulates all local implementation or resource related exceptions. | | [IkeNetworkLostException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeNetworkLostException) | IkeNetworkLostException is returned to the caller via [android.net.ipsec.ike.IkeSessionCallback#onError(android.net.ipsec.ike.exceptions.IkeException)](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback.html#onError(android.net.ipsec.ike.exceptions.IkeException))if the underlying Network for the was lost with no alternatives. | |

IkeNonProtocolException encapsulates all implementation-specific non-protocol IKE errors.

## Summary

# IkeException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeException

Kotlin| [Java](https://developer.android.com/reference/android/net/ipsec/ike/exceptions/IkeException "View this page in Java") 

```
abstract class IkeException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [android.net.ipsec.ike.exceptions.IkeException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeException#) |

| Known Direct Subclasses [IkeNonProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeNonProtocolException), [IkeProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException) |------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------| | [IkeNonProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeNonProtocolException) | IkeNonProtocolException encapsulates all implementation-specific non-protocol IKE errors. | | [IkeProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException) | IkeProtocolException is an abstract class that represents the common information for all IKE protocol errors. | |

| Known Indirect Subclasses [IkeIOException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeIOException), [IkeInternalException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeInternalException), [IkeNetworkLostException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeNetworkLostException), [InvalidKeException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/InvalidKeException), [InvalidMajorVersionException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/InvalidMajorVersionException), [InvalidSelectorsException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/InvalidSelectorsException) |----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [IkeIOException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeIOException) | Wrapper for I/O exceptions encountered during IKE operations. | | [IkeInternalException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeInternalException) | IkeInternalException encapsulates all local implementation or resource related exceptions. | | [IkeNetworkLostException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeNetworkLostException) | IkeNetworkLostException is returned to the caller via [android.net.ipsec.ike.IkeSessionCallback#onError(android.net.ipsec.ike.exceptions.IkeException)](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback.html#onError(android.net.ipsec.ike.exceptions.IkeException))if the underlying Network for the was lost with no alternatives. | | [InvalidKeException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/InvalidKeException) | This exception is thrown when the remote server expected a different Diffie-Hellman group. | | [InvalidMajorVersionException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/InvalidMajorVersionException) | This exception is thrown when major version of an inbound message is higher than 2. | | [InvalidSelectorsException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/InvalidSelectorsException) | This exception is thrown if the remote server received an IPsec packet with mismatched selectors. | |

IkeException represents a generic exception that includes internal and protocol exceptions.

## Summary

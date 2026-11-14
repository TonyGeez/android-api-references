# IkeException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeException

Kotlin| [Java](../android/net/ipsec/ike/exceptions/IkeException.md) 
| --- | --- |

```
abstract class IkeException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [android.net.ipsec.ike.exceptions.IkeException](../android/net/ipsec/ike/exceptions/IkeException.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [IkeNonProtocolException](../android/net/ipsec/ike/exceptions/IkeNonProtocolException.md), [IkeProtocolException](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) |------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------| | [IkeNonProtocolException](../android/net/ipsec/ike/exceptions/IkeNonProtocolException.md) | IkeNonProtocolException encapsulates all implementation-specific non-protocol IKE errors. | | [IkeProtocolException](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) | IkeProtocolException is an abstract class that represents the common information for all IKE protocol errors. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [IkeIOException](../android/net/ipsec/ike/exceptions/IkeIOException.md), [IkeInternalException](../android/net/ipsec/ike/exceptions/IkeInternalException.md), [IkeNetworkLostException](../android/net/ipsec/ike/exceptions/IkeNetworkLostException.md), [InvalidKeException](../android/net/ipsec/ike/exceptions/InvalidKeException.md), [InvalidMajorVersionException](../android/net/ipsec/ike/exceptions/InvalidMajorVersionException.md), [InvalidSelectorsException](../android/net/ipsec/ike/exceptions/InvalidSelectorsException.md) |----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [IkeIOException](../android/net/ipsec/ike/exceptions/IkeIOException.md) | Wrapper for I/O exceptions encountered during IKE operations. | | [IkeInternalException](../android/net/ipsec/ike/exceptions/IkeInternalException.md) | IkeInternalException encapsulates all local implementation or resource related exceptions. | | [IkeNetworkLostException](../android/net/ipsec/ike/exceptions/IkeNetworkLostException.md) | IkeNetworkLostException is returned to the caller via [android.net.ipsec.ike.IkeSessionCallback#onError(android.net.ipsec.ike.exceptions.IkeException)](../android/net/ipsec/ike/IkeSessionCallback.md))if the underlying Network for the was lost with no alternatives. | | [InvalidKeException](../android/net/ipsec/ike/exceptions/InvalidKeException.md) | This exception is thrown when the remote server expected a different Diffie-Hellman group. | | [InvalidMajorVersionException](../android/net/ipsec/ike/exceptions/InvalidMajorVersionException.md) | This exception is thrown when major version of an inbound message is higher than 2. | | [InvalidSelectorsException](../android/net/ipsec/ike/exceptions/InvalidSelectorsException.md) | This exception is thrown if the remote server received an IPsec packet with mismatched selectors. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

IkeException represents a generic exception that includes internal and protocol exceptions.

## Summary

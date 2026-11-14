# IkeException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeException

Kotlin| [Java](IkeException.md) 
| --- | --- |

```
abstract class IkeException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [android.net.ipsec.ike.exceptions.IkeException](IkeException.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [IkeNonProtocolException](IkeNonProtocolException.md), [IkeProtocolException](IkeProtocolException.md) |------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------| | [IkeNonProtocolException](IkeNonProtocolException.md) | IkeNonProtocolException encapsulates all implementation-specific non-protocol IKE errors. | | [IkeProtocolException](IkeProtocolException.md) | IkeProtocolException is an abstract class that represents the common information for all IKE protocol errors. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [IkeIOException](IkeIOException.md), [IkeInternalException](IkeInternalException.md), [IkeNetworkLostException](IkeNetworkLostException.md), [InvalidKeException](InvalidKeException.md), [InvalidMajorVersionException](InvalidMajorVersionException.md), [InvalidSelectorsException](InvalidSelectorsException.md) |----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [IkeIOException](IkeIOException.md) | Wrapper for I/O exceptions encountered during IKE operations. | | [IkeInternalException](IkeInternalException.md) | IkeInternalException encapsulates all local implementation or resource related exceptions. | | [IkeNetworkLostException](IkeNetworkLostException.md) | IkeNetworkLostException is returned to the caller via [android.net.ipsec.ike.IkeSessionCallback#onError(android.net.ipsec.ike.exceptions.IkeException)](../android.net.ipsec.ike/IkeSessionCallback.md))if the underlying Network for the was lost with no alternatives. | | [InvalidKeException](InvalidKeException.md) | This exception is thrown when the remote server expected a different Diffie-Hellman group. | | [InvalidMajorVersionException](InvalidMajorVersionException.md) | This exception is thrown when major version of an inbound message is higher than 2. | | [InvalidSelectorsException](InvalidSelectorsException.md) | This exception is thrown if the remote server received an IPsec packet with mismatched selectors. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

IkeException represents a generic exception that includes internal and protocol exceptions.

## Summary

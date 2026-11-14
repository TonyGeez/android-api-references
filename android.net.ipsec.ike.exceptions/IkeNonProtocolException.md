# IkeNonProtocolException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeNonProtocolException

Kotlin| [Java](IkeNonProtocolException.md) 
| --- | --- |

```
abstract class IkeNonProtocolException : IkeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [android.net.ipsec.ike.exceptions.IkeException](IkeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.net.ipsec.ike.exceptions.IkeNonProtocolException](IkeNonProtocolException.md) |

| Known Direct Subclasses [IkeIOException](IkeIOException.md), [IkeInternalException](IkeInternalException.md), [IkeNetworkLostException](IkeNetworkLostException.md) |------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [IkeIOException](IkeIOException.md) | Wrapper for I/O exceptions encountered during IKE operations. | | [IkeInternalException](IkeInternalException.md) | IkeInternalException encapsulates all local implementation or resource related exceptions. | | [IkeNetworkLostException](IkeNetworkLostException.md) | IkeNetworkLostException is returned to the caller via [android.net.ipsec.ike.IkeSessionCallback#onError(android.net.ipsec.ike.exceptions.IkeException)](../android.net.ipsec.ike/IkeSessionCallback.md))if the underlying Network for the was lost with no alternatives. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

IkeNonProtocolException encapsulates all implementation-specific non-protocol IKE errors.

## Summary

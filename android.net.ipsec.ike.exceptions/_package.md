# android.net.ipsec.ike.exceptions

# android.net.ipsec.ike.exceptions

Kotlin| [Java](../android/net/ipsec/ike/exceptions/_package.md)
| --- | --- |

## Exceptions

| [IkeException](../android/net/ipsec/ike/exceptions/IkeException.md) | IkeException represents a generic exception that includes internal and protocol exceptions. |
| --- | --- |
| [IkeInternalException](../android/net/ipsec/ike/exceptions/IkeInternalException.md) | IkeInternalException encapsulates all local implementation or resource related exceptions. |
| [IkeIOException](../android/net/ipsec/ike/exceptions/IkeIOException.md) | Wrapper for I/O exceptions encountered during IKE operations. |
| [IkeNetworkLostException](../android/net/ipsec/ike/exceptions/IkeNetworkLostException.md) | IkeNetworkLostException is returned to the caller via [android.net.ipsec.ike.IkeSessionCallback#onError(android.net.ipsec.ike.exceptions.IkeException)](../android/net/ipsec/ike/IkeSessionCallback.md))if the underlying Network for the was lost with no alternatives. |
| --- | --- |
| [IkeNonProtocolException](../android/net/ipsec/ike/exceptions/IkeNonProtocolException.md) | IkeNonProtocolException encapsulates all implementation-specific non-protocol IKE errors. |
| [IkeProtocolException](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) | IkeProtocolException is an abstract class that represents the common information for all IKE protocol errors. |
| [IkeTimeoutException](../android/net/ipsec/ike/exceptions/IkeTimeoutException.md) | This exception is thrown when there is an IKE retransmission timeout. |
| --- | --- |
| [InvalidKeException](../android/net/ipsec/ike/exceptions/InvalidKeException.md) | This exception is thrown when the remote server expected a different Diffie-Hellman group. |
| [InvalidMajorVersionException](../android/net/ipsec/ike/exceptions/InvalidMajorVersionException.md) | This exception is thrown when major version of an inbound message is higher than 2. |
| [InvalidSelectorsException](../android/net/ipsec/ike/exceptions/InvalidSelectorsException.md) | This exception is thrown if the remote server received an IPsec packet with mismatched selectors. |
| --- | --- |

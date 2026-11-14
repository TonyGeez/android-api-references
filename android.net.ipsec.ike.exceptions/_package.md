# android.net.ipsec.ike.exceptions

# android.net.ipsec.ike.exceptions

Kotlin| [Java](https://developer.android.com/reference/android/net/ipsec/ike/exceptions/package-summary "View this page in Java")
| --- | --- |

## Exceptions

| [IkeException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeException) | IkeException represents a generic exception that includes internal and protocol exceptions. |
| --- | --- |
| [IkeInternalException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeInternalException) | IkeInternalException encapsulates all local implementation or resource related exceptions. |
| [IkeIOException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeIOException) | Wrapper for I/O exceptions encountered during IKE operations. |
| [IkeNetworkLostException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeNetworkLostException) | IkeNetworkLostException is returned to the caller via [android.net.ipsec.ike.IkeSessionCallback#onError(android.net.ipsec.ike.exceptions.IkeException)](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback.html#onError(android.net.ipsec.ike.exceptions.IkeException))if the underlying Network for the was lost with no alternatives. |
| --- | --- |
| [IkeNonProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeNonProtocolException) | IkeNonProtocolException encapsulates all implementation-specific non-protocol IKE errors. |
| [IkeProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException) | IkeProtocolException is an abstract class that represents the common information for all IKE protocol errors. |
| [IkeTimeoutException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeTimeoutException) | This exception is thrown when there is an IKE retransmission timeout. |
| --- | --- |
| [InvalidKeException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/InvalidKeException) | This exception is thrown when the remote server expected a different Diffie-Hellman group. |
| [InvalidMajorVersionException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/InvalidMajorVersionException) | This exception is thrown when major version of an inbound message is higher than 2. |
| [InvalidSelectorsException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/InvalidSelectorsException) | This exception is thrown if the remote server received an IPsec packet with mismatched selectors. |
| --- | --- |

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InvalidSelectorsException

Kotlin | [Java](../android/net/ipsec/ike/exceptions/InvalidSelectorsException.md)
| --- | --- |

```
class InvalidSelectorsException : IkeProtocolException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [android.net.ipsec.ike.exceptions.IkeException](../android/net/ipsec/ike/exceptions/IkeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.net.ipsec.ike.exceptions.IkeProtocolException](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) ||
| | | | | ↳ | [android.net.ipsec.ike.exceptions.InvalidSelectorsException](../android/net/ipsec/ike/exceptions/InvalidSelectorsException.md) |

This exception is thrown if the remote server received an IPsec packet with mismatched selectors.

This exception indicates that the remote server received an IPsec packet whose selectors do not match those of the IPsec SA on which it was delivered. The error data contains the start of the offending packet (as in ICMP messages), which is the IP header plus the first 64 bits of the original datagram's data.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_AUTHENTICATION_FAILED:kotlin.Int` IKE authentication failed <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_CHILD_SA_NOT_FOUND:kotlin.Int` Child SA in the received packet does not exist <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_FAILED_CP_REQUIRED:kotlin.Int` Configuration Payload required but not found in IKE setup <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_INTERNAL_ADDRESS_FAILURE:kotlin.Int` No internal addresses can be assigned <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_INVALID_IKE_SPI:kotlin.Int` Unrecognized destination IKE SPI <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_INVALID_KE_PAYLOAD:kotlin.Int` Invalid Key Exchange Payload <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_INVALID_MAJOR_VERSION:kotlin.Int` Invalid major version <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_INVALID_MESSAGE_ID:kotlin.Int` Invalid message ID <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_INVALID_SELECTORS:kotlin.Int` An IPsec Packet was found to have mismatched Traffic Selectors of the IPsec SA on which it was delivered <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_INVALID_SYNTAX:kotlin.Int` Invalid syntax <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_NO_ADDITIONAL_SAS:kotlin.Int` No additional SAa are acceptable <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_NO_PROPOSAL_CHOSEN:kotlin.Int` No SA Proposal Chosen is acceptable <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_SINGLE_PAIR_REQUIRED:kotlin.Int` Only Traffic Selectors specifying a single pair of addresses are acceptable <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_TEMPORARY_FAILURE:kotlin.Int` Temporary failure <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_TS_UNACCEPTABLE:kotlin.Int` No Traffic Selectors are acceptable <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_UNSUPPORTED_CRITICAL_PAYLOAD:kotlin.Int` Unsupported critical payload <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/InvalidSelectorsException#InvalidSelectorsException(kotlin.Int,%20kotlin.ByteArray)(spi: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, packetInfo: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)` Construct an instance of InvalidSelectorsException. |

| Public methods ||
|---|---|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/InvalidSelectorsException#getIpSecPacketInfo()()` Returns the IP header plus the first 64 bits of the packet that has mismtached selectors. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/InvalidSelectorsException#getIpSecSpi()()` Returns the SPI of the IPsec SA that delivered the packet with mismtached selectors. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#getErrorType()()` Returns the IKE protocol error type of this `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException` instance. <br /> | ||

## Public constructors

### InvalidSelectorsException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
InvalidSelectorsException(
    spi: Int, 
    packetInfo: ByteArray)
```

Construct an instance of InvalidSelectorsException.

Except for testing, IKE library users normally do not instantiate this object themselves but instead get a reference via `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback.html#` or `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback.html#`

| Parameters ||
|---|---|
| `spi` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the SPI of the IPsec SA that delivered the packet with mismtached selectors. |
| `packetInfo` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the IP header plus the first 64 bits of the packet that has mismtached selectors. This value cannot be `null`. |

## Public methods

### getIpSecPacketInfo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIpSecPacketInfo(): ByteArray
```

Returns the IP header plus the first 64 bits of the packet that has mismtached selectors.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | This value cannot be `null`. |

### getIpSecSpi

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIpSecSpi(): Int
```

Returns the SPI of the IPsec SA that delivered the packet with mismtached selectors.

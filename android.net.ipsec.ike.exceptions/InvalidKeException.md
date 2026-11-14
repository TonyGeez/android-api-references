# InvalidKeException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InvalidKeException

Kotlin| [Java](../android/net/ipsec/ike/exceptions/InvalidKeException.md) 
| --- | --- |

```
class InvalidKeException : IkeProtocolException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [android.net.ipsec.ike.exceptions.IkeException](../android/net/ipsec/ike/exceptions/IkeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.net.ipsec.ike.exceptions.IkeProtocolException](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) ||
| | | | | ↳ | [android.net.ipsec.ike.exceptions.InvalidKeException](../android/net/ipsec/ike/exceptions/InvalidKeException.md) |

This exception is thrown when the remote server expected a different Diffie-Hellman group.

This exception indicates that the remote server received a different KE payload in the Child creation request from accepted Diffie-Hellman group. Callers can retry Child creation by proposing the expected DH group included in this exception.

## Summary

| Inherited constants ||
|---|---|
| From class [IkeProtocolException](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_AUTHENTICATION_FAILED](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) <br /> IKE authentication failed <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_CHILD_SA_NOT_FOUND](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) <br /> Child SA in the received packet does not exist <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_FAILED_CP_REQUIRED](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) <br /> Configuration Payload required but not found in IKE setup <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INTERNAL_ADDRESS_FAILURE](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) <br /> No internal addresses can be assigned <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_IKE_SPI](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) <br /> Unrecognized destination IKE SPI <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_KE_PAYLOAD](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) <br /> Invalid Key Exchange Payload <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_MAJOR_VERSION](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) <br /> Invalid major version <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_MESSAGE_ID](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) <br /> Invalid message ID <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_SELECTORS](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) <br /> An IPsec Packet was found to have mismatched Traffic Selectors of the IPsec SA on which it was delivered <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_SYNTAX](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) <br /> Invalid syntax <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_NO_ADDITIONAL_SAS](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) <br /> No additional SAa are acceptable <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_NO_PROPOSAL_CHOSEN](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) <br /> No SA Proposal Chosen is acceptable <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_SINGLE_PAIR_REQUIRED](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) <br /> Only Traffic Selectors specifying a single pair of addresses are acceptable <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_TEMPORARY_FAILURE](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) <br /> Temporary failure <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_TS_UNACCEPTABLE](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) <br /> No Traffic Selectors are acceptable <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_UNSUPPORTED_CRITICAL_PAYLOAD](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) <br /> Unsupported critical payload <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InvalidKeException](../android/net/ipsec/ike/exceptions/InvalidKeException.md))`(`dhGroup:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Construct an instance of InvalidKeException. |

| Public methods ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDhGroup](../android/net/ipsec/ike/exceptions/InvalidKeException.md))`()` Return the expected DH Group included in this exception. |

| Inherited functions ||
|---|---|
| From class [IkeProtocolException](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorType](../android/net/ipsec/ike/exceptions/IkeProtocolException.md))`()` <br /> Returns the IKE protocol error type of this [IkeProtocolException](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) instance. <br /> | ||

## Public constructors

### InvalidKeException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidKeException(dhGroup: Int)
```

Construct an instance of InvalidKeException.

Except for testing, IKE library users normally do not instantiate this object themselves but instead get a reference via [IkeSessionCallback](../android/net/ipsec/ike/IkeSessionCallback.md) or [ChildSessionCallback](../android/net/ipsec/ike/ChildSessionCallback.md).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------|
| `dhGroup` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected DH group |

## Public methods

### getDhGroup

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDhGroup(): Int
```

Return the expected DH Group included in this exception.

| Return ||
|----------------------------------------------------------------------------|------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the expected DH Group. |

# InvalidKeException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InvalidKeException

Kotlin| [Java](https://developer.android.com/reference/android/net/ipsec/ike/exceptions/InvalidKeException "View this page in Java") 
| --- | --- |

```
class InvalidKeException : IkeProtocolException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [android.net.ipsec.ike.exceptions.IkeException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeException) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.net.ipsec.ike.exceptions.IkeProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException) ||
| | | | | ↳ | [android.net.ipsec.ike.exceptions.InvalidKeException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/InvalidKeException#) |

This exception is thrown when the remote server expected a different Diffie-Hellman group.

This exception indicates that the remote server received a different KE payload in the Child creation request from accepted Diffie-Hellman group. Callers can retry Child creation by proposing the expected DH group included in this exception.

## Summary

| Inherited constants ||
|---|---|
| From class [IkeProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_AUTHENTICATION_FAILED](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_AUTHENTICATION_FAILED:kotlin.Int) <br /> IKE authentication failed <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_CHILD_SA_NOT_FOUND](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_CHILD_SA_NOT_FOUND:kotlin.Int) <br /> Child SA in the received packet does not exist <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_FAILED_CP_REQUIRED](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_FAILED_CP_REQUIRED:kotlin.Int) <br /> Configuration Payload required but not found in IKE setup <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INTERNAL_ADDRESS_FAILURE](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_INTERNAL_ADDRESS_FAILURE:kotlin.Int) <br /> No internal addresses can be assigned <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_IKE_SPI](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_INVALID_IKE_SPI:kotlin.Int) <br /> Unrecognized destination IKE SPI <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_KE_PAYLOAD](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_INVALID_KE_PAYLOAD:kotlin.Int) <br /> Invalid Key Exchange Payload <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_MAJOR_VERSION](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_INVALID_MAJOR_VERSION:kotlin.Int) <br /> Invalid major version <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_MESSAGE_ID](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_INVALID_MESSAGE_ID:kotlin.Int) <br /> Invalid message ID <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_SELECTORS](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_INVALID_SELECTORS:kotlin.Int) <br /> An IPsec Packet was found to have mismatched Traffic Selectors of the IPsec SA on which it was delivered <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_SYNTAX](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_INVALID_SYNTAX:kotlin.Int) <br /> Invalid syntax <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_NO_ADDITIONAL_SAS](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_NO_ADDITIONAL_SAS:kotlin.Int) <br /> No additional SAa are acceptable <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_NO_PROPOSAL_CHOSEN](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_NO_PROPOSAL_CHOSEN:kotlin.Int) <br /> No SA Proposal Chosen is acceptable <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_SINGLE_PAIR_REQUIRED](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_SINGLE_PAIR_REQUIRED:kotlin.Int) <br /> Only Traffic Selectors specifying a single pair of addresses are acceptable <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_TEMPORARY_FAILURE](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_TEMPORARY_FAILURE:kotlin.Int) <br /> Temporary failure <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_TS_UNACCEPTABLE](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_TS_UNACCEPTABLE:kotlin.Int) <br /> No Traffic Selectors are acceptable <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_UNSUPPORTED_CRITICAL_PAYLOAD](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_UNSUPPORTED_CRITICAL_PAYLOAD:kotlin.Int) <br /> Unsupported critical payload <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InvalidKeException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/InvalidKeException#InvalidKeException(kotlin.Int))`(`dhGroup:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Construct an instance of InvalidKeException. |

| Public methods ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDhGroup](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/InvalidKeException#getDhGroup())`()` Return the expected DH Group included in this exception. |

| Inherited functions ||
|---|---|
| From class [IkeProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorType](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#getErrorType())`()` <br /> Returns the IKE protocol error type of this [IkeProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException) instance. <br /> | ||

## Public constructors

### InvalidKeException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidKeException(dhGroup: Int)
```

Construct an instance of InvalidKeException.

Except for testing, IKE library users normally do not instantiate this object themselves but instead get a reference via [IkeSessionCallback](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback.html#) or [ChildSessionCallback](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback.html#).

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

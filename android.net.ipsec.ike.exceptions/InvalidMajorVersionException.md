# InvalidMajorVersionException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InvalidMajorVersionException

Kotlin| [Java](https://developer.android.com/reference/android/net/ipsec/ike/exceptions/InvalidMajorVersionException "View this page in Java") 
| --- | --- |

```
class InvalidMajorVersionException : IkeProtocolException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [android.net.ipsec.ike.exceptions.IkeException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeException) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.net.ipsec.ike.exceptions.IkeProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException) ||
| | | | | ↳ | [android.net.ipsec.ike.exceptions.InvalidMajorVersionException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/InvalidMajorVersionException#) |

This exception is thrown when major version of an inbound message is higher than 2.

## Summary

| Inherited constants ||
|---|---|
| From class [IkeProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_AUTHENTICATION_FAILED](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_AUTHENTICATION_FAILED:kotlin.Int) <br /> IKE authentication failed <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_CHILD_SA_NOT_FOUND](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_CHILD_SA_NOT_FOUND:kotlin.Int) <br /> Child SA in the received packet does not exist <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_FAILED_CP_REQUIRED](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_FAILED_CP_REQUIRED:kotlin.Int) <br /> Configuration Payload required but not found in IKE setup <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INTERNAL_ADDRESS_FAILURE](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_INTERNAL_ADDRESS_FAILURE:kotlin.Int) <br /> No internal addresses can be assigned <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_IKE_SPI](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_INVALID_IKE_SPI:kotlin.Int) <br /> Unrecognized destination IKE SPI <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_KE_PAYLOAD](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_INVALID_KE_PAYLOAD:kotlin.Int) <br /> Invalid Key Exchange Payload <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_MAJOR_VERSION](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_INVALID_MAJOR_VERSION:kotlin.Int) <br /> Invalid major version <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_MESSAGE_ID](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_INVALID_MESSAGE_ID:kotlin.Int) <br /> Invalid message ID <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_SELECTORS](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_INVALID_SELECTORS:kotlin.Int) <br /> An IPsec Packet was found to have mismatched Traffic Selectors of the IPsec SA on which it was delivered <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_SYNTAX](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_INVALID_SYNTAX:kotlin.Int) <br /> Invalid syntax <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_NO_ADDITIONAL_SAS](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_NO_ADDITIONAL_SAS:kotlin.Int) <br /> No additional SAa are acceptable <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_NO_PROPOSAL_CHOSEN](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_NO_PROPOSAL_CHOSEN:kotlin.Int) <br /> No SA Proposal Chosen is acceptable <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_SINGLE_PAIR_REQUIRED](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_SINGLE_PAIR_REQUIRED:kotlin.Int) <br /> Only Traffic Selectors specifying a single pair of addresses are acceptable <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_TEMPORARY_FAILURE](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_TEMPORARY_FAILURE:kotlin.Int) <br /> Temporary failure <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_TS_UNACCEPTABLE](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_TS_UNACCEPTABLE:kotlin.Int) <br /> No Traffic Selectors are acceptable <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_UNSUPPORTED_CRITICAL_PAYLOAD](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#ERROR_TYPE_UNSUPPORTED_CRITICAL_PAYLOAD:kotlin.Int) <br /> Unsupported critical payload <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InvalidMajorVersionException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/InvalidMajorVersionException#InvalidMajorVersionException(kotlin.Byte))`(`version:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Construct a instance of InvalidMajorVersionException |

| Public methods ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [getMajorVersion](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/InvalidMajorVersionException#getMajorVersion())`()` Return the major version included in this exception. |

| Inherited functions ||
|---|---|
| From class [IkeProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorType](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException#getErrorType())`()` <br /> Returns the IKE protocol error type of this [IkeProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException) instance. <br /> | ||

## Public constructors

### InvalidMajorVersionException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidMajorVersionException(version: Byte)
```

Construct a instance of InvalidMajorVersionException

Except for testing, IKE library users normally do not instantiate this object themselves but instead get a reference via [IkeSessionCallback](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback.html#) or [ChildSessionCallback](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback.html#).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------|
| `version` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the major version in received packet |

## Public methods

### getMajorVersion

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMajorVersion(): Byte
```

Return the major version included in this exception.

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | the major version |

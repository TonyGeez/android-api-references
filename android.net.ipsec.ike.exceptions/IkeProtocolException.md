# IkeProtocolException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeProtocolException

Kotlin| [Java](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) 
| --- | --- |

```
abstract class IkeProtocolException : IkeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [android.net.ipsec.ike.exceptions.IkeException](../android/net/ipsec/ike/exceptions/IkeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.net.ipsec.ike.exceptions.IkeProtocolException](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) |

| Known Direct Subclasses [InvalidKeException](../android/net/ipsec/ike/exceptions/InvalidKeException.md), [InvalidMajorVersionException](../android/net/ipsec/ike/exceptions/InvalidMajorVersionException.md), [InvalidSelectorsException](../android/net/ipsec/ike/exceptions/InvalidSelectorsException.md) |----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------| | [InvalidKeException](../android/net/ipsec/ike/exceptions/InvalidKeException.md) | This exception is thrown when the remote server expected a different Diffie-Hellman group. | | [InvalidMajorVersionException](../android/net/ipsec/ike/exceptions/InvalidMajorVersionException.md) | This exception is thrown when major version of an inbound message is higher than 2. | | [InvalidSelectorsException](../android/net/ipsec/ike/exceptions/InvalidSelectorsException.md) | This exception is thrown if the remote server received an IPsec packet with mismatched selectors. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

IkeProtocolException is an abstract class that represents the common information for all IKE protocol errors.

Error types are as defined by RFC 7296.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_AUTHENTICATION_FAILED](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) IKE authentication failed |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_CHILD_SA_NOT_FOUND](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) Child SA in the received packet does not exist |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_FAILED_CP_REQUIRED](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) Configuration Payload required but not found in IKE setup |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INTERNAL_ADDRESS_FAILURE](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) No internal addresses can be assigned |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_IKE_SPI](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) Unrecognized destination IKE SPI |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_KE_PAYLOAD](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) Invalid Key Exchange Payload |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_MAJOR_VERSION](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) Invalid major version |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_MESSAGE_ID](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) Invalid message ID |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_SELECTORS](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) An IPsec Packet was found to have mismatched Traffic Selectors of the IPsec SA on which it was delivered |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_INVALID_SYNTAX](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) Invalid syntax |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_NO_ADDITIONAL_SAS](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) No additional SAa are acceptable |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_NO_PROPOSAL_CHOSEN](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) No SA Proposal Chosen is acceptable |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_SINGLE_PAIR_REQUIRED](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) Only Traffic Selectors specifying a single pair of addresses are acceptable |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_TEMPORARY_FAILURE](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) Temporary failure |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_TS_UNACCEPTABLE](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) No Traffic Selectors are acceptable |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_UNSUPPORTED_CRITICAL_PAYLOAD](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) Unsupported critical payload |

| Public methods ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorType](../android/net/ipsec/ike/exceptions/IkeProtocolException.md))`()` Returns the IKE protocol error type of this [IkeProtocolException](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) instance. |

## Constants

### ERROR_TYPE_AUTHENTICATION_FAILED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TYPE_AUTHENTICATION_FAILED: Int
```

IKE authentication failed 

 Value: 24

### ERROR_TYPE_CHILD_SA_NOT_FOUND

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TYPE_CHILD_SA_NOT_FOUND: Int
```

Child SA in the received packet does not exist 

 Value: 44

### ERROR_TYPE_FAILED_CP_REQUIRED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TYPE_FAILED_CP_REQUIRED: Int
```

Configuration Payload required but not found in IKE setup 

 Value: 37

### ERROR_TYPE_INTERNAL_ADDRESS_FAILURE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TYPE_INTERNAL_ADDRESS_FAILURE: Int
```

No internal addresses can be assigned 

 Value: 36

### ERROR_TYPE_INVALID_IKE_SPI

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TYPE_INVALID_IKE_SPI: Int
```

Unrecognized destination IKE SPI 

 Value: 4

### ERROR_TYPE_INVALID_KE_PAYLOAD

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TYPE_INVALID_KE_PAYLOAD: Int
```

Invalid Key Exchange Payload 

 Value: 17

### ERROR_TYPE_INVALID_MAJOR_VERSION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TYPE_INVALID_MAJOR_VERSION: Int
```

Invalid major version 

 Value: 5

### ERROR_TYPE_INVALID_MESSAGE_ID

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TYPE_INVALID_MESSAGE_ID: Int
```

Invalid message ID 

 Value: 9

### ERROR_TYPE_INVALID_SELECTORS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TYPE_INVALID_SELECTORS: Int
```

An IPsec Packet was found to have mismatched Traffic Selectors of the IPsec SA on which it was delivered 

 Value: 39

### ERROR_TYPE_INVALID_SYNTAX

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TYPE_INVALID_SYNTAX: Int
```

Invalid syntax 

 Value: 7

### ERROR_TYPE_NO_ADDITIONAL_SAS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TYPE_NO_ADDITIONAL_SAS: Int
```

No additional SAa are acceptable 

 Value: 35

### ERROR_TYPE_NO_PROPOSAL_CHOSEN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TYPE_NO_PROPOSAL_CHOSEN: Int
```

No SA Proposal Chosen is acceptable 

 Value: 14

### ERROR_TYPE_SINGLE_PAIR_REQUIRED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TYPE_SINGLE_PAIR_REQUIRED: Int
```

Only Traffic Selectors specifying a single pair of addresses are acceptable 

 Value: 34

### ERROR_TYPE_TEMPORARY_FAILURE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TYPE_TEMPORARY_FAILURE: Int
```

Temporary failure 

 Value: 43

### ERROR_TYPE_TS_UNACCEPTABLE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TYPE_TS_UNACCEPTABLE: Int
```

No Traffic Selectors are acceptable 

 Value: 38

### ERROR_TYPE_UNSUPPORTED_CRITICAL_PAYLOAD

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TYPE_UNSUPPORTED_CRITICAL_PAYLOAD: Int
```

Unsupported critical payload 

 Value: 1

## Public methods

### getErrorType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getErrorType(): Int
```

Returns the IKE protocol error type of this [IkeProtocolException](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) instance.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the IKE standard protocol error type defined in [IkeProtocolException](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) or the error code for an unrecognized error type. Value is [android.net.ipsec.ike.exceptions.IkeProtocolException#ERROR_TYPE_UNSUPPORTED_CRITICAL_PAYLOAD](../android/net/ipsec/ike/exceptions/IkeProtocolException.md), [android.net.ipsec.ike.exceptions.IkeProtocolException#ERROR_TYPE_INVALID_IKE_SPI](../android/net/ipsec/ike/exceptions/IkeProtocolException.md), [android.net.ipsec.ike.exceptions.IkeProtocolException#ERROR_TYPE_INVALID_MAJOR_VERSION](../android/net/ipsec/ike/exceptions/IkeProtocolException.md), [android.net.ipsec.ike.exceptions.IkeProtocolException#ERROR_TYPE_INVALID_SYNTAX](../android/net/ipsec/ike/exceptions/IkeProtocolException.md), [android.net.ipsec.ike.exceptions.IkeProtocolException#ERROR_TYPE_INVALID_MESSAGE_ID](../android/net/ipsec/ike/exceptions/IkeProtocolException.md), [android.net.ipsec.ike.exceptions.IkeProtocolException#ERROR_TYPE_NO_PROPOSAL_CHOSEN](../android/net/ipsec/ike/exceptions/IkeProtocolException.md), [android.net.ipsec.ike.exceptions.IkeProtocolException#ERROR_TYPE_INVALID_KE_PAYLOAD](../android/net/ipsec/ike/exceptions/IkeProtocolException.md), [android.net.ipsec.ike.exceptions.IkeProtocolException#ERROR_TYPE_AUTHENTICATION_FAILED](../android/net/ipsec/ike/exceptions/IkeProtocolException.md), [android.net.ipsec.ike.exceptions.IkeProtocolException#ERROR_TYPE_SINGLE_PAIR_REQUIRED](../android/net/ipsec/ike/exceptions/IkeProtocolException.md), [android.net.ipsec.ike.exceptions.IkeProtocolException#ERROR_TYPE_NO_ADDITIONAL_SAS](../android/net/ipsec/ike/exceptions/IkeProtocolException.md), [android.net.ipsec.ike.exceptions.IkeProtocolException#ERROR_TYPE_INTERNAL_ADDRESS_FAILURE](../android/net/ipsec/ike/exceptions/IkeProtocolException.md), [android.net.ipsec.ike.exceptions.IkeProtocolException#ERROR_TYPE_FAILED_CP_REQUIRED](../android/net/ipsec/ike/exceptions/IkeProtocolException.md), [android.net.ipsec.ike.exceptions.IkeProtocolException#ERROR_TYPE_TS_UNACCEPTABLE](../android/net/ipsec/ike/exceptions/IkeProtocolException.md), [android.net.ipsec.ike.exceptions.IkeProtocolException#ERROR_TYPE_INVALID_SELECTORS](../android/net/ipsec/ike/exceptions/IkeProtocolException.md), [android.net.ipsec.ike.exceptions.IkeProtocolException#ERROR_TYPE_TEMPORARY_FAILURE](../android/net/ipsec/ike/exceptions/IkeProtocolException.md), or [android.net.ipsec.ike.exceptions.IkeProtocolException#ERROR_TYPE_CHILD_SA_NOT_FOUND](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) |

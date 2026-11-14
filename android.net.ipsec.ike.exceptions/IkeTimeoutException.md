# IkeTimeoutException

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeTimeoutException

Kotlin| [Java](IkeTimeoutException.md) 
| --- | --- |

```
class IkeTimeoutException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.io.IOException](../java.io/IOException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.net.ipsec.ike.exceptions.IkeTimeoutException](IkeTimeoutException.md) |

This exception is thrown when there is an IKE retransmission timeout.

This exception indicates that the IKE Session failed to receive an IKE response before hitting the maximum number of retransmission attempts configured in[android.net.ipsec.ike.IkeSessionParams.Builder#setRetransmissionTimeoutsMillis(int[])](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams.Builder.html#setRetransmissionTimeoutsMillis(kotlin.IntArray)).

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IkeTimeoutException](IkeTimeoutException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Constructs an`IkeTimeoutException`with the specified detail message. |

## Public constructors

### IkeTimeoutException

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IkeTimeoutException(message: String)
```

Constructs an`IkeTimeoutException`with the specified detail message.

Callers are not generally expected to instantiate this object themselves, except for testing. A reference is passed via [IkeSessionCallback](../android.net.ipsec.ike/IkeSessionCallback.md) or [ChildSessionCallback](../android.net.ipsec.ike/ChildSessionCallback.md).

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The detail message (which is saved for later retrieval by the [getMessage()](../java.lang/Throwable.md))method) This value cannot be`null`. |

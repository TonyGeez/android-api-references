# IkeTimeoutException

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeTimeoutException

Kotlin| [Java](https://developer.android.com/reference/android/net/ipsec/ike/exceptions/IkeTimeoutException "View this page in Java") 
| --- | --- |

```
class IkeTimeoutException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.net.ipsec.ike.exceptions.IkeTimeoutException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeTimeoutException#) |

This exception is thrown when there is an IKE retransmission timeout.

This exception indicates that the IKE Session failed to receive an IKE response before hitting the maximum number of retransmission attempts configured in[android.net.ipsec.ike.IkeSessionParams.Builder#setRetransmissionTimeoutsMillis(int[])](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams.Builder.html#setRetransmissionTimeoutsMillis(kotlin.IntArray)).

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IkeTimeoutException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeTimeoutException#IkeTimeoutException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Constructs an`IkeTimeoutException`with the specified detail message. |

## Public constructors

### IkeTimeoutException

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IkeTimeoutException(message: String)
```

Constructs an`IkeTimeoutException`with the specified detail message.

Callers are not generally expected to instantiate this object themselves, except for testing. A reference is passed via [IkeSessionCallback](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback.html#) or [ChildSessionCallback](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback.html#).

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The detail message (which is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getMessage())method) This value cannot be`null`. |

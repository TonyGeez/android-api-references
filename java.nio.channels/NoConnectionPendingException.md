# NoConnectionPendingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NoConnectionPendingException

```
open class NoConnectionPendingException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) ||
| | | | | ↳ | [java.nio.channels.NoConnectionPendingException](https://developer.android.com/reference/kotlin/java/nio/channels/NoConnectionPendingException#) |

Unchecked exception thrown when the [finishConnect](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel#finishConnect()) method of a [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel) is invoked without first successfully invoking its [connect](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel#connect(java.net.SocketAddress)) method.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NoConnectionPendingException](https://developer.android.com/reference/kotlin/java/nio/channels/NoConnectionPendingException#NoConnectionPendingException())`()` Constructs an instance of this class. |

## Public constructors

### NoConnectionPendingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoConnectionPendingException()
```

Constructs an instance of this class.

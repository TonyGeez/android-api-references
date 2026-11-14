# NoConnectionPendingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NoConnectionPendingException

```
open class NoConnectionPendingException : IllegalStateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalStateException](../java/lang/IllegalStateException.md) ||
| | | | | ↳ | [java.nio.channels.NoConnectionPendingException](../java/nio/channels/NoConnectionPendingException.md) |

Unchecked exception thrown when the [finishConnect](../java/nio/channels/SocketChannel.md)) method of a [SocketChannel](../java/nio/channels/SocketChannel.md) is invoked without first successfully invoking its [connect](../java/nio/channels/SocketChannel.md)) method.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NoConnectionPendingException](../java/nio/channels/NoConnectionPendingException.md))`()` Constructs an instance of this class. |

## Public constructors

### NoConnectionPendingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoConnectionPendingException()
```

Constructs an instance of this class.

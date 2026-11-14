# HandshakeCompletedListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HandshakeCompletedListener

```
interface HandshakeCompletedListener : EventListener
```

| [javax.net.ssl.HandshakeCompletedListener](HandshakeCompletedListener.md) |

This interface is implemented by any class which wants to receive notifications about the completion of an SSL protocol handshake on a given SSL connection.

When an SSL handshake completes, new security parameters will have been established. Those parameters always include the security keys used to protect messages. They may also include parameters associated with a new*session*such as authenticated peer identity and a new SSL cipher suite.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [handshakeCompleted](HandshakeCompletedListener.md))`(`event:` ` [HandshakeCompletedEvent](HandshakeCompletedEvent.md)!`)` This method is invoked on registered objects when a SSL handshake is completed. |

## Public methods

### handshakeCompleted

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun handshakeCompleted(event: HandshakeCompletedEvent!): Unit
```

This method is invoked on registered objects when a SSL handshake is completed.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [HandshakeCompletedEvent](HandshakeCompletedEvent.md)!:the event identifying when the SSL Handshake completed on a given SSL connection |

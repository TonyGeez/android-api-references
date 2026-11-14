# SSLSessionBindingListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLSessionBindingListener

```
interface SSLSessionBindingListener : EventListener
```

| [javax.net.ssl.SSLSessionBindingListener](../javax/net/ssl/SSLSessionBindingListener.md) |

This interface is implemented by objects which want to know when they are being bound or unbound from a SSLSession. When either event occurs via [SSLSession.putValue(String, Object)](../javax/net/ssl/SSLSession.md))or [SSLSession.removeValue(String)](../javax/net/ssl/SSLSession.md)), the event is communicated through a SSLSessionBindingEvent identifying the session.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [valueBound](../javax/net/ssl/SSLSessionBindingListener.md))`(`event:` ` [SSLSessionBindingEvent](../javax/net/ssl/SSLSessionBindingEvent.md)!`)` This is called to notify the listener that it is being bound into an SSLSession. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [valueUnbound](../javax/net/ssl/SSLSessionBindingListener.md))`(`event:` ` [SSLSessionBindingEvent](../javax/net/ssl/SSLSessionBindingEvent.md)!`)` This is called to notify the listener that it is being unbound from a SSLSession. |

## Public methods

### valueBound

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun valueBound(event: SSLSessionBindingEvent!): Unit
```

This is called to notify the listener that it is being bound into an SSLSession.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [SSLSessionBindingEvent](../javax/net/ssl/SSLSessionBindingEvent.md)!:the event identifying the SSLSession into which the listener is being bound. |

### valueUnbound

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun valueUnbound(event: SSLSessionBindingEvent!): Unit
```

This is called to notify the listener that it is being unbound from a SSLSession.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [SSLSessionBindingEvent](../javax/net/ssl/SSLSessionBindingEvent.md)!:the event identifying the SSLSession from which the listener is being unbound. |

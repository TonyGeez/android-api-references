# SSLSessionBindingListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLSessionBindingListener

```
interface SSLSessionBindingListener : EventListener
```

| [javax.net.ssl.SSLSessionBindingListener](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionBindingListener#) |

This interface is implemented by objects which want to know when they are being bound or unbound from a SSLSession. When either event occurs via [SSLSession.putValue(String, Object)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#putValue(kotlin.String,%20kotlin.Any))or [SSLSession.removeValue(String)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#removeValue(kotlin.String)), the event is communicated through a SSLSessionBindingEvent identifying the session.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [valueBound](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionBindingListener#valueBound(javax.net.ssl.SSLSessionBindingEvent))`(`event:` ` [SSLSessionBindingEvent](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionBindingEvent)!`)` This is called to notify the listener that it is being bound into an SSLSession. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [valueUnbound](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionBindingListener#valueUnbound(javax.net.ssl.SSLSessionBindingEvent))`(`event:` ` [SSLSessionBindingEvent](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionBindingEvent)!`)` This is called to notify the listener that it is being unbound from a SSLSession. |

## Public methods

### valueBound

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun valueBound(event: SSLSessionBindingEvent!): Unit
```

This is called to notify the listener that it is being bound into an SSLSession.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [SSLSessionBindingEvent](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionBindingEvent)!:the event identifying the SSLSession into which the listener is being bound. |

### valueUnbound

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun valueUnbound(event: SSLSessionBindingEvent!): Unit
```

This is called to notify the listener that it is being unbound from a SSLSession.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [SSLSessionBindingEvent](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionBindingEvent)!:the event identifying the SSLSession from which the listener is being unbound. |

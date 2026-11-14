# SSLSessionBindingEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLSessionBindingEvent

```
open class SSLSessionBindingEvent : EventObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) ||
| | ↳ | [javax.net.ssl.SSLSessionBindingEvent](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionBindingEvent#) |

This event is propagated to a SSLSessionBindingListener. When a listener object is bound or unbound to an SSLSession by [SSLSession.putValue(String, Object)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#putValue(kotlin.String,%20kotlin.Any)) or [SSLSession.removeValue(String)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#removeValue(kotlin.String)), objects which implement the SSLSessionBindingListener will be receive an event of this type. The event's `name` field is the key in which the listener is being bound or unbound.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SSLSessionBindingEvent](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionBindingEvent#SSLSessionBindingEvent(javax.net.ssl.SSLSession,%20kotlin.String))`(`session:` ` [SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession)!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new SSLSessionBindingEvent. |

| Public methods ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionBindingEvent#getName())`()` Returns the name to which the object is being bound, or the name from which the object is being unbound. |
| open [SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession)! | [getSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionBindingEvent#getSession())`()` Returns the SSLSession into which the listener is being bound or from which the listener is being unbound. |

| Inherited functions ||
|---|---|
| From class [EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) |----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getSource](https://developer.android.com/reference/kotlin/java/util/EventObject.html#getSource())`()` The object on which the Event initially occurred. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/EventObject.html#toString())`()` Returns a String representation of this EventObject. <br /> | ||

| Inherited properties ||
|---|---|
| From class [EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) |-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [source](https://developer.android.com/reference/kotlin/java/util/EventObject.html#source:kotlin.Any) The object on which the Event initially occurred. <br /> | ||

## Public constructors

### SSLSessionBindingEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLSessionBindingEvent(
    session: SSLSession!, 
    name: String!)
```

Constructs a new SSLSessionBindingEvent.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `session` | [SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession)!: the SSLSession acting as the source of the event |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name to which the object is being bound or unbound |

| Exceptions ||
|--------------------------------------|-----------------------|
| `java.lang.IllegalArgumentException` | if `session` is null. |

## Public methods

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getName(): String!
```

Returns the name to which the object is being bound, or the name from which the object is being unbound.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name to which the object is being bound or unbound |

### getSession

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSession(): SSLSession!
```

Returns the SSLSession into which the listener is being bound or from which the listener is being unbound.

| Return ||
|----------------------------------------------------------------------------------------|------------------|
| [SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession)! | the `SSLSession` |

# SSLSessionBindingEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLSessionBindingEvent

```
open class SSLSessionBindingEvent : EventObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.EventObject](../java.util/EventObject.md) ||
| | ↳ | [javax.net.ssl.SSLSessionBindingEvent](SSLSessionBindingEvent.md) |

This event is propagated to a SSLSessionBindingListener. When a listener object is bound or unbound to an SSLSession by [SSLSession.putValue(String, Object)](SSLSession.md)) or [SSLSession.removeValue(String)](SSLSession.md)), objects which implement the SSLSessionBindingListener will be receive an event of this type. The event's `name` field is the key in which the listener is being bound or unbound.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SSLSessionBindingEvent](SSLSessionBindingEvent.md))`(`session:` ` [SSLSession](SSLSession.md)!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new SSLSessionBindingEvent. |

| Public methods ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](SSLSessionBindingEvent.md))`()` Returns the name to which the object is being bound, or the name from which the object is being unbound. |
| open [SSLSession](SSLSession.md)! | [getSession](SSLSessionBindingEvent.md))`()` Returns the SSLSession into which the listener is being bound or from which the listener is being unbound. |

| Inherited functions ||
|---|---|
| From class [EventObject](../java.util/EventObject.md) |----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getSource](../java.util/EventObject.md))`()` The object on which the Event initially occurred. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java.util/EventObject.md))`()` Returns a String representation of this EventObject. <br /> | ||

| Inherited properties ||
|---|---|
| From class [EventObject](../java.util/EventObject.md) |-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [source](../java.util/EventObject.md) The object on which the Event initially occurred. <br /> | ||

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
| `session` | [SSLSession](SSLSession.md)!: the SSLSession acting as the source of the event |
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
| [SSLSession](SSLSession.md)! | the `SSLSession` |

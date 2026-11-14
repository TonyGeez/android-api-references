# WebMessage

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WebMessage

Kotlin| [Java](../android/webkit/WebMessage.md) 
| --- | --- |

```
open class WebMessage
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.WebMessage](../android/webkit/WebMessage.md) |

The Java representation of the HTML5 PostMessage event. See https://html.spec.whatwg.org/multipage/comms.html#the-messageevent-interfaces for definition of a MessageEvent in HTML5.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WebMessage](../android/webkit/WebMessage.md))`(`data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a WebMessage. |
| [WebMessage](../android/webkit/WebMessage.md))`(`data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `ports:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [WebMessagePort](../android/webkit/WebMessagePort.md)!>!`)` Creates a WebMessage. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getData](../android/webkit/WebMessage.md))`()` Returns the data of the message. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [WebMessagePort](../android/webkit/WebMessagePort.md)!\>? | [getPorts](../android/webkit/WebMessage.md))`()` Returns the ports that are sent with the message, or`null`if no port is sent. |

## Public constructors

### WebMessage

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WebMessage(data: String!)
```

Creates a WebMessage.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the data of the message. |

### WebMessage

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WebMessage(
    data: String!, 
    ports: Array<WebMessagePort!>!)
```

Creates a WebMessage.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the data of the message. |
| `ports` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [WebMessagePort](../android/webkit/WebMessagePort.md)!\>!:the ports that are sent with the message. |

## Public methods

### getData

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getData(): String!
```

Returns the data of the message. 

### getPorts

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPorts(): Array<WebMessagePort!>?
```

Returns the ports that are sent with the message, or`null`if no port is sent.

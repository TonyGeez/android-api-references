# WebMessagePort

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WebMessagePort

Kotlin | [Java](WebMessagePort.md) 
| --- | --- |

```
abstract class WebMessagePort
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.WebMessagePort](WebMessagePort.md) |

The Java representation of the [HTML5 message ports.](https://html.spec.whatwg.org/multipage/comms.html#messageport)

A Message port represents one endpoint of a Message Channel. In Android webview, there is no separate Message Channel object. When a message channel is created, both ports are tangled to each other and started, and then returned in a MessagePort array, see [WebView.createWebMessageChannel](WebView.md)) for creating a message channel.

When a message port is first created or received via transfer, it does not have a WebMessageCallback to receive web messages. The messages are queued until a WebMessageCallback is set.

A message port should be closed when it is not used by the embedder application anymore. A closed port cannot be transferred or cannot be reopened to send messages. Close can be called multiple times.

When a port is transferred to JS, it cannot be used to send or receive messages at the Java side anymore. Different from HTML5 Spec, a port cannot be transferred if one of these has ever happened: i. a message callback was set, ii. a message was posted on it. A transferred port cannot be closed by the application, since the ownership is also transferred.

It is possible to transfer both ports of a channel to JS, for example for communication between subframes.

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [WebMessageCallback](../android/webkit/WebMessagePort.WebMessageCallback.md) The listener for handling MessagePort events. |

| Public methods ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](WebMessagePort.md))`()` Close the message port and free any resources associated with it. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [postMessage](WebMessagePort.md))`(`message:` ` [WebMessage](WebMessage.md)!`)` Post a WebMessage to the entangled port. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWebMessageCallback](WebMessagePort.md))`(`callback:` ` [WebMessagePort.WebMessageCallback](../android/webkit/WebMessagePort.WebMessageCallback.md)!`)` Sets a callback to receive message events on the main thread. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWebMessageCallback](WebMessagePort.md))`(`callback:` ` [WebMessagePort.WebMessageCallback](../android/webkit/WebMessagePort.WebMessageCallback.md)!`, `handler:` ` [Handler](../android.os/Handler.md)!`)` Sets a callback to receive message events on the handler that is provided by the application. |

## Public methods

### close

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Close the message port and free any resources associated with it. 

### postMessage

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun postMessage(message: WebMessage!): Unit
```

Post a WebMessage to the entangled port.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `message` | [WebMessage](WebMessage.md)!: the message from Java to JS. |

| Exceptions ||
|-----------------------------------|---------------------------------------------------|
| `java.lang.IllegalStateException` | If message port is already transferred or closed. |

### setWebMessageCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setWebMessageCallback(callback: WebMessagePort.WebMessageCallback!): Unit
```

Sets a callback to receive message events on the main thread.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [WebMessagePort.WebMessageCallback](../android/webkit/WebMessagePort.WebMessageCallback.md)!: the message callback. |

### setWebMessageCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setWebMessageCallback(
    callback: WebMessagePort.WebMessageCallback!, 
    handler: Handler!
): Unit
```

Sets a callback to receive message events on the handler that is provided by the application.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [WebMessagePort.WebMessageCallback](../android/webkit/WebMessagePort.WebMessageCallback.md)!: the message callback. |
| `handler` | [Handler](../android.os/Handler.md)!: the handler to receive the message messages. |

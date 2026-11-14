# ReceiverCallNotAllowedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReceiverCallNotAllowedException

Kotlin| [Java](ReceiverCallNotAllowedException.md) 
| --- | --- |

```
open class ReceiverCallNotAllowedException : AndroidRuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.util.AndroidRuntimeException](../android.util/AndroidRuntimeException.md) ||
| | | | | ↳ | [android.content.ReceiverCallNotAllowedException](ReceiverCallNotAllowedException.md) |

This exception is thrown from android.content.Context#registerReceiver and android.content.Context#bindService when these methods are being used from an [BroadcastReceiver](BroadcastReceiver.md) component. In this case, the component will no longer be active upon returning from receiving the Intent, so it is not valid to use asynchronous APIs.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ReceiverCallNotAllowedException](ReceiverCallNotAllowedException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### ReceiverCallNotAllowedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReceiverCallNotAllowedException(msg: String!)
```

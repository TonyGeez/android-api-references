# ReceiverCallNotAllowedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReceiverCallNotAllowedException

Kotlin| [Java](https://developer.android.com/reference/android/content/ReceiverCallNotAllowedException "View this page in Java") 

```
open class ReceiverCallNotAllowedException : AndroidRuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| | | | ↳ | [android.util.AndroidRuntimeException](https://developer.android.com/reference/kotlin/android/util/AndroidRuntimeException.html#) ||
| | | | | ↳ | [android.content.ReceiverCallNotAllowedException](https://developer.android.com/reference/kotlin/android/content/ReceiverCallNotAllowedException#) |

This exception is thrown from android.content.Context#registerReceiver and android.content.Context#bindService when these methods are being used from an [BroadcastReceiver](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver) component. In this case, the component will no longer be active upon returning from receiving the Intent, so it is not valid to use asynchronous APIs.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ReceiverCallNotAllowedException](https://developer.android.com/reference/kotlin/android/content/ReceiverCallNotAllowedException#ReceiverCallNotAllowedException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### ReceiverCallNotAllowedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReceiverCallNotAllowedException(msg: String!)
```

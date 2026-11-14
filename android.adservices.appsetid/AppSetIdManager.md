Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# AppSetIdManager

Kotlin | [Java](AppSetIdManager.md)
| --- | --- |

```
open class AppSetIdManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.appsetid.AppSetIdManager](AppSetIdManager.md) |

AppSetIdManager provides APIs for app and ad-SDKs to access appSetId for non-monetizing purpose.

## Summary

| Public methods ||
|---|---|
| open static [AppSetIdManager](AppSetIdManager.md) | get Factory method for creating an instance of AppSetIdManager. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getAppSetId Retrieve the AppSetId. |

## Public methods

### get

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 6](https://developer.android.com/sdkExtensions)

```
open static fun get(context: Context): AppSetIdManager
```

Factory method for creating an instance of AppSetIdManager.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The `https://developer.android.com/reference/kotlin/android/content/Context.html#` to use. This value cannot be `null`. |

| Return ||
|---|---|
| AppSetIdManager | A AppSetIdManager instance. This value cannot be `null`. |

### getAppSetId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

```
open fun getAppSetId(
    executor: Executor, 
    callback: OutcomeReceiver<AppSetId!, Exception!>
): Unit
```

Retrieve the AppSetId.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor to run callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [AppSetId](AppSetId.md)!, [Exception](../java.lang/Exception.md)!\>: The callback that's called after appsetid are available or an error occurs. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | This value cannot be `null`. |

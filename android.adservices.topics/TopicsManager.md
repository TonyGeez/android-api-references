Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TopicsManager

```
class TopicsManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.adservices.topics.TopicsManager](https://developer.android.com/reference/kotlin/android/adservices/topics/TopicsManager#) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The Rubidium (Rb) Relevance APIs, including those in android.adservices.topics, are being deprecated. Relevance APIs have no direct replacement. Developers should stop using them, as calls will be rejected in future Android releases. Please refer to official Privacy Sandbox documentation for deprecation and roadmap details: https://privacysandbox.com/news/update-on-plans-for-privacy-sandbox-technologies/

TopicsManager provides APIs for App and Ad-Sdks to get the user interest topics in a privacy preserving way.

The instance of the `https://developer.android.com/reference/kotlin/android/adservices/topics/TopicsManager#` can be obtained using android.content.Context#getSystemService and `https://developer.android.com/reference/kotlin/android/adservices/topics/TopicsManager#` class.

## Summary

| Public methods ||
|---|---|
| static [TopicsManager](https://developer.android.com/reference/kotlin/android/adservices/topics/TopicsManager#) | `https://developer.android.com/reference/kotlin/android/adservices/topics/TopicsManager#get(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#)` Factory method for creating an instance of TopicsManager. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/topics/TopicsManager#getTopics(android.adservices.topics.GetTopicsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(getTopicsRequest: https://developer.android.com/reference/kotlin/android/adservices/topics/GetTopicsRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/adservices/topics/GetTopicsResponse!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>)` Return the topics. |

## Public methods

### get

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 6](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun get(context: Context): TopicsManager
```

**Deprecated:** *Deprecated in Java.*

Factory method for creating an instance of TopicsManager.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): The `https://developer.android.com/reference/kotlin/android/content/Context.html#` to use. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/topics/TopicsManager#` | A `https://developer.android.com/reference/kotlin/android/adservices/topics/TopicsManager#` instance. This value cannot be `null`. |

### getTopics

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTopics(
    getTopicsRequest: GetTopicsRequest, 
    executor: Executor, 
    callback: OutcomeReceiver<GetTopicsResponse!, Exception!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Return the topics. 
Requires `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_TOPICS:kotlin.String`

| Parameters ||
|---|---|
| `getTopicsRequest` | [GetTopicsRequest](https://developer.android.com/reference/kotlin/android/adservices/topics/GetTopicsRequest): The request for obtaining Topics. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor to run callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [GetTopicsResponse](https://developer.android.com/reference/kotlin/android/adservices/topics/GetTopicsResponse)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>: The callback that's called after topics are available or an error occurs. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this API is not available. |

# CustomAudienceManager

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# CustomAudienceManager

Kotlin| [Java](../android/adservices/customaudience/CustomAudienceManager.md) 
| --- | --- |

```
open class CustomAudienceManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.customaudience.CustomAudienceManager](../android/adservices/customaudience/CustomAudienceManager.md) |

CustomAudienceManager provides APIs for app and ad-SDKs to join / leave custom audiences.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fetchAndJoinCustomAudience](../android/adservices/customaudience/CustomAudienceManager.md))`(`fetchAndJoinCustomAudienceRequest:` ` [FetchAndJoinCustomAudienceRequest](../android/adservices/customaudience/FetchAndJoinCustomAudienceRequest.md)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `receiver:` ` [OutcomeReceiver](../android/os/OutcomeReceiver.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](../java/lang/Exception.md)!>`)` Adds the user to the [CustomAudience](../android/adservices/customaudience/CustomAudience.md) fetched from a`fetchUri`. |
| openstatic [CustomAudienceManager](../android/adservices/customaudience/CustomAudienceManager.md) | [get](../android/adservices/customaudience/CustomAudienceManager.md))`(`context:` ` [Context](../android/content/Context.md)`)` Factory method for creating an instance of CustomAudienceManager. |
| open [TestCustomAudienceManager](../android/adservices/customaudience/TestCustomAudienceManager.md) | [getTestCustomAudienceManager](../android/adservices/customaudience/CustomAudienceManager.md))`()` Create a service with test-enabling APIs |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [joinCustomAudience](../android/adservices/customaudience/CustomAudienceManager.md))`(`joinCustomAudienceRequest:` ` [JoinCustomAudienceRequest](../android/adservices/customaudience/JoinCustomAudienceRequest.md)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `receiver:` ` [OutcomeReceiver](../android/os/OutcomeReceiver.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](../java/lang/Exception.md)!>`)` Adds the user to the given [CustomAudience](../android/adservices/customaudience/CustomAudience.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [leaveCustomAudience](../android/adservices/customaudience/CustomAudienceManager.md))`(`leaveCustomAudienceRequest:` ` [LeaveCustomAudienceRequest](../android/adservices/customaudience/LeaveCustomAudienceRequest.md)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `receiver:` ` [OutcomeReceiver](../android/os/OutcomeReceiver.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](../java/lang/Exception.md)!>`)` Attempts to remove a user from a custom audience by deleting any existing [CustomAudience](../android/adservices/customaudience/CustomAudience.md) data, identified by`ownerPackageName`,`buyer`, and`name`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scheduleCustomAudienceUpdate](../android/adservices/customaudience/CustomAudienceManager.md))`(`request:` ` [ScheduleCustomAudienceUpdateRequest](../android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest.md)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `receiver:` ` [AdServicesOutcomeReceiver](../android/adservices/common/AdServicesOutcomeReceiver.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](../java/lang/Exception.md)!>`)` Allows the API caller to schedule a deferred Custom Audience update. |
| --- | --- |

## Public methods

### fetchAndJoinCustomAudience

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
open fun fetchAndJoinCustomAudience(
    fetchAndJoinCustomAudienceRequest: FetchAndJoinCustomAudienceRequest, 
    executor: Executor, 
    receiver: OutcomeReceiver<Any!, Exception!>
): Unit
```

Adds the user to the [CustomAudience](../android/adservices/customaudience/CustomAudience.md) fetched from a`fetchUri`.

An attempt to register the user for a custom audience with the same combination of`ownerPackageName`,`buyer`, and`name`will cause the existing custom audience's information to be overwritten, including the list of ads data.

Note that the ads list can be completely overwritten by the daily background fetch job.

This call fails with an [SecurityException](../java/lang/SecurityException.md) if

1. the`ownerPackageName`is not calling app's package name and/or
2. the buyer is not authorized to use the API.

This call fails with an [IllegalArgumentException](../java/lang/IllegalArgumentException.md) if

1. the storage limit has been exceeded by the calling application and/or
2. any URI parameters in the [CustomAudience](../android/adservices/customaudience/CustomAudience.md) given are not authenticated with the [CustomAudience](../android/adservices/customaudience/CustomAudience.md) buyer.

This call fails with [LimitExceededException](../android/os/LimitExceededException.md) if the calling package exceeds the allowed rate limits and is throttled.

This call fails with an [IllegalStateException](../java/lang/IllegalStateException.md) if an internal service error is encountered. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](../android/adservices/common/AdServicesPermissions.md)

| Parameters ||
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fetchAndJoinCustomAudienceRequest` | [FetchAndJoinCustomAudienceRequest](../android/adservices/customaudience/FetchAndJoinCustomAudienceRequest.md):This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>:This value cannot be`null`. |
| --- | --- |

### get

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 6](https://developer.android.com/sdkExtensions) 

```
open static fun get(context: Context): CustomAudienceManager
```

Factory method for creating an instance of CustomAudienceManager.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):The [Context](../android/content/Context.md) to use This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CustomAudienceManager](../android/adservices/customaudience/CustomAudienceManager.md) | A [CustomAudienceManager](../android/adservices/customaudience/CustomAudienceManager.md) instance This value cannot be`null`. |

### getTestCustomAudienceManager

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
open fun getTestCustomAudienceManager(): TestCustomAudienceManager
```

Create a service with test-enabling APIs

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [TestCustomAudienceManager](../android/adservices/customaudience/TestCustomAudienceManager.md) | This value cannot be`null`. |

### joinCustomAudience

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
open fun joinCustomAudience(
    joinCustomAudienceRequest: JoinCustomAudienceRequest, 
    executor: Executor, 
    receiver: OutcomeReceiver<Any!, Exception!>
): Unit
```

Adds the user to the given [CustomAudience](../android/adservices/customaudience/CustomAudience.md).

An attempt to register the user for a custom audience with the same combination of`ownerPackageName`,`buyer`, and`name`will cause the existing custom audience's information to be overwritten, including the list of ads data.

Note that the ads list can be completely overwritten by the daily background fetch job.

This call fails with an [SecurityException](../java/lang/SecurityException.md) if

1. the`ownerPackageName`is not calling app's package name and/or
2. the buyer is not authorized to use the API.

This call fails with an [IllegalArgumentException](../java/lang/IllegalArgumentException.md) if

1. the storage limit has been exceeded by the calling application and/or
2. any URI parameters in the [CustomAudience](../android/adservices/customaudience/CustomAudience.md) given are not authenticated with the [CustomAudience](../android/adservices/customaudience/CustomAudience.md) buyer.

This call fails with [LimitExceededException](../android/os/LimitExceededException.md) if the calling package exceeds the allowed rate limits and is throttled.

This call fails with an [IllegalStateException](../java/lang/IllegalStateException.md) if an internal service error is encountered. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](../android/adservices/common/AdServicesPermissions.md)

| Parameters ||
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `joinCustomAudienceRequest` | [JoinCustomAudienceRequest](../android/adservices/customaudience/JoinCustomAudienceRequest.md):This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>:This value cannot be`null`. |
| --- | --- |

### leaveCustomAudience

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
open fun leaveCustomAudience(
    leaveCustomAudienceRequest: LeaveCustomAudienceRequest, 
    executor: Executor, 
    receiver: OutcomeReceiver<Any!, Exception!>
): Unit
```

Attempts to remove a user from a custom audience by deleting any existing [CustomAudience](../android/adservices/customaudience/CustomAudience.md) data, identified by`ownerPackageName`,`buyer`, and`name`.

This call fails with an [SecurityException](../java/lang/SecurityException.md) if

1. the`ownerPackageName`is not calling app's package name; and/or
2. the buyer is not authorized to use the API.

This call fails with [LimitExceededException](../android/os/LimitExceededException.md) if the calling package exceeds the allowed rate limits and is throttled.

This call does not inform the caller whether the custom audience specified existed in on-device storage. In other words, it will fail silently when a buyer attempts to leave a custom audience that was not joined. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](../android/adservices/common/AdServicesPermissions.md)

| Parameters ||
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `leaveCustomAudienceRequest` | [LeaveCustomAudienceRequest](../android/adservices/customaudience/LeaveCustomAudienceRequest.md):This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>:This value cannot be`null`. |
| --- | --- |

### scheduleCustomAudienceUpdate

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 

```
open fun scheduleCustomAudienceUpdate(
    request: ScheduleCustomAudienceUpdateRequest, 
    executor: Executor, 
    receiver: AdServicesOutcomeReceiver<Any!, Exception!>
): Unit
```

Allows the API caller to schedule a deferred Custom Audience update. For each update the user will be able to join or leave a set of CustomAudiences.

This API only guarantees minimum delay to make the update, and does not guarantee a maximum deadline within which the update request would be made. Scheduled updates could be batched and queued together to preserve system resources, thus exact delay time is not guaranteed.

If the provided`shouldReplacePendingUpdates`is true, all the currently scheduled pending updates matching the`owner`i.e. calling app and`buyer`inferred from Update Uri will be deleted.

In order to conserve system resources the API will make and update request only if the following constraints are satisfied

1. The device is using an un-metered internet connection
2. The device battery is not low
3. The device storage is not low

When the deferred update is triggered the API makes a POST request to the provided updateUri with the request body containing a JSON of Partial Custom Audience list.

An example of request body containing list of Partial Custom Audiences would look like: 

```kotlin
<code>{
      "partial_custom_audience_data": [
          {
              "name": "running_shoes",
              "activation_time": 1644375856883,
              "expiration_time": 1644375908397
          },
          {
              "name": "casual_shirt",
              "user_bidding_signals": {
                  "signal1": "value1"
              }
          }
      ]
  }
  </code>
```

In response the API expects a JSON in return with following keys:

1. "join" : Should contain list containing full data for a [CustomAudience](../android/adservices/customaudience/CustomAudience.md) object
2. "leave" : List of [CustomAudience](../android/adservices/customaudience/CustomAudience.md) names that user is intended to be removed from

An example of JSON in response would look like: 

```kotlin
<code>{
      "join": [
          {
              "name": "running-shoes",
              "activation_time": 1680603133,
              "expiration_time": 1680803133,
              "user_bidding_signals": {
                  "signal1": "value"
              },
              "trusted_bidding_data": {
                  "trusted_bidding_uri": "https://example-dsp.com/",
                  "trusted_bidding_keys": [
                      "k1",
                      "k2"
                  ]
              },
              "bidding_logic_uri": "https://example-dsp.com/...",
              "ads": [
                  {
                      "render_uri": "https://example-dsp.com/...",
                      "metadata": {},
                      "ad_filters": {
                          "frequency_cap": {
                              "win": [
                                  {
                                      "ad_counter_key": "key1",
                                      "max_count": 2,
                                      "interval_in_seconds": 60
                                  }
                              ],
                              "view": [
                                  {
                                      "ad_counter_key": "key2",
                                      "max_count": 10,
                                      "interval_in_seconds": 3600
                                  }
                              ]
                          },
                          "app_install": {
                              "package_names": [
                                  "package.name.one"
                              ]
                          }
                      }
                  }
              ]
          },
          {}
      ],
      "leave": [
          "tennis_shoes",
          "formal_shirt"
      ]
  }
  </code>
```

An attempt to register the user for a custom audience from the same application with the same combination of`buyer`inferred from Update Uri, and`name`will cause the existing custom audience's information to be overwritten, including the list of ads data.

In case information related to any of the CustomAudience to be joined is malformed, the deferred update would silently ignore that single Custom Audience

When removing this API attempts to remove a user from a custom audience by deleting any existing [CustomAudience](../android/adservices/customaudience/CustomAudience.md) identified by owner i.e. calling app,`buyer`inferred from Update Uri, and`name`

Any partial custom audience field set by the caller cannot be overridden by the custom audience fetched from the`updateUri`. Given multiple Custom Audiences could be returned by a buyer ad tech we will match the override restriction based on the names of the Custom Audiences. A buyer may skip returning a full Custom Audience for any Partial Custom Audience in request.

In case the API encounters transient errors while making the network call for update, like 5xx, connection timeout, rate limit exceeded it would employ retries, with backoff up to a 'retry limit' number of times. The API would also honor 'retry-after' header specifying the min amount of seconds by which the next request should be delayed.

In a scenario where server responds with a '429 status code', signifying 'Too many requests', API would place the deferred update and other updates for the same requester i.e. caller package and buyer combination, in a quarantine. The quarantine records would be referred before making any calls for requesters, and request will only be made once the quarantine period has expired. The applications can leverage the \`retry-after\` header to self-quarantine for traffic management to their servers and prevent being overwhelmed with requests. The default quarantine value will be set to 30 minutes.

This call fails with an [SecurityException](../java/lang/SecurityException.md) if

1. the`ownerPackageName`is not calling app's package name; and/or
2. the buyer, inferred from`updateUri`, is not authorized to use the API.

This call fails with an [IllegalArgumentException](../java/lang/IllegalArgumentException.md) if

1. the provided`updateUri`is invalid or malformed.
2. the provided`delayTime`is not within permissible bounds
3. the combined size of`partialCustomAudience`list is larger than allowed limits

This call fails with [LimitExceededException](../android/os/LimitExceededException.md) if the calling package exceeds the allowed rate limits and is throttled.

This call fails with [IllegalStateException](../java/lang/IllegalStateException.md) if the provided`shouldReplacePendingUpdates`is false, and there exists a pending update in the queue. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](../android/adservices/common/AdServicesPermissions.md)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [ScheduleCustomAudienceUpdateRequest](../android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest.md):This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `receiver` | [AdServicesOutcomeReceiver](../android/adservices/common/AdServicesOutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>:This value cannot be`null`. |
| --- | --- |

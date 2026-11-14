# ScheduleCustomAudienceUpdateRequest

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions)

# ScheduleCustomAudienceUpdateRequest

Kotlin| [Java](../android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest.md) 
| --- | --- |

```
class ScheduleCustomAudienceUpdateRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.customaudience.ScheduleCustomAudienceUpdateRequest](../android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest.md) |

The request object wrapping the required and optional parameters to schedule a deferred update for a buyer ad tech's custom audiences.

The on-device caller can specify information in a series of [PartialCustomAudience](../android/adservices/customaudience/PartialCustomAudience.md) objects that will be sent to the buyer ad tech's server after a designated minimum delay.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest.Builder.md) Builder for [ScheduleCustomAudienceUpdateRequest](../android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest.md) objects. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Duration](../java/time/Duration.md) | [getMinDelay](../android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest.md))`()` Returns the minimum [Duration](../java/time/Duration.md) that the update will be deferred before the service fetches updates for the buyer ad tech's custom audiences. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PartialCustomAudience](../android/adservices/customaudience/PartialCustomAudience.md)!\> | [getPartialCustomAudienceList](../android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest.md))`()` Returns the list of [PartialCustomAudience](../android/adservices/customaudience/PartialCustomAudience.md) objects which are sent along with the request to download the updates for the buyer ad tech's custom audiences. |
| --- | --- |
| [Uri](../android/net/Uri.md) | [getUpdateUri](../android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest.md))`()` Returns the [Uri](../android/net/Uri.md) from which the update for the buyer's custom audiences will be fetched. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest.md))`()` Returns the hash of [ScheduleCustomAudienceUpdateRequest](../android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest.md) object's data. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldReplacePendingUpdates](../android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest.md))`()` Returns`true`if any pending scheduled updates should be canceled and replaced with the update detailed in the current [ScheduleCustomAudienceUpdateRequest](../android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest.md). |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest.md))`()` <br /> |

## Public methods

### equals

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`only if two [ScheduleCustomAudienceUpdateRequest](../android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest.md) objects contain the same information. |

### getMinDelay

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 

```
fun getMinDelay(): Duration
```

Returns the minimum [Duration](../java/time/Duration.md) that the update will be deferred before the service fetches updates for the buyer ad tech's custom audiences.

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------|
| [Duration](../java/time/Duration.md) | This value cannot be`null`. |

### getPartialCustomAudienceList

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 

```
fun getPartialCustomAudienceList(): MutableList<PartialCustomAudience!>
```

Returns the list of [PartialCustomAudience](../android/adservices/customaudience/PartialCustomAudience.md) objects which are sent along with the request to download the updates for the buyer ad tech's custom audiences.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PartialCustomAudience](../android/adservices/customaudience/PartialCustomAudience.md)!> | This value cannot be`null`. |

### getUpdateUri

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 

```
fun getUpdateUri(): Uri
```

Returns the [Uri](../android/net/Uri.md) from which the update for the buyer's custom audiences will be fetched.

The [Uri](../android/net/Uri.md) must use the same HTTPS site as the buyer ad tech's enrolled server.

| Return ||
|-----------------------------------------------------------------------------|-----------------------------|
| [Uri](../android/net/Uri.md) | This value cannot be`null`. |

### hashCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns the hash of [ScheduleCustomAudienceUpdateRequest](../android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest.md) object's data.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### shouldReplacePendingUpdates

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 

```
fun shouldReplacePendingUpdates(): Boolean
```

Returns`true`if any pending scheduled updates should be canceled and replaced with the update detailed in the current [ScheduleCustomAudienceUpdateRequest](../android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest.md).

If this method returns`false`and there are previously requested updates still pending for the same buyer in the same app, a call to [android.adservices.customaudience.CustomAudienceManager#scheduleCustomAudienceUpdate(android.adservices.customaudience.ScheduleCustomAudienceUpdateRequest,java.util.concurrent.Executor,android.adservices.common.AdServicesOutcomeReceiver)](../android/adservices/customaudience/CustomAudienceManager.md))with this [ScheduleCustomAudienceUpdateRequest](../android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest.md) will fail. 

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a human-readable representation of [ScheduleCustomAudienceUpdateRequest](../android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest.md). |

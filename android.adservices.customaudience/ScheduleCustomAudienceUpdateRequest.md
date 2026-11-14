# ScheduleCustomAudienceUpdateRequest

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions)

# ScheduleCustomAudienceUpdateRequest

Kotlin| [Java](https://developer.android.com/reference/android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest "View this page in Java") 
| --- | --- |

```
class ScheduleCustomAudienceUpdateRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.customaudience.ScheduleCustomAudienceUpdateRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest#) |

The request object wrapping the required and optional parameters to schedule a deferred update for a buyer ad tech's custom audiences.

The on-device caller can specify information in a series of [PartialCustomAudience](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience) objects that will be sent to the buyer ad tech's server after a designated minimum delay.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest.Builder) Builder for [ScheduleCustomAudienceUpdateRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest#) objects. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#) | [getMinDelay](https://developer.android.com/reference/kotlin/android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest#getMinDelay())`()` Returns the minimum [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#) that the update will be deferred before the service fetches updates for the buyer ad tech's custom audiences. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PartialCustomAudience](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience)!\> | [getPartialCustomAudienceList](https://developer.android.com/reference/kotlin/android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest#getPartialCustomAudienceList())`()` Returns the list of [PartialCustomAudience](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience) objects which are sent along with the request to download the updates for the buyer ad tech's custom audiences. |
| --- | --- |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | [getUpdateUri](https://developer.android.com/reference/kotlin/android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest#getUpdateUri())`()` Returns the [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) from which the update for the buyer's custom audiences will be fetched. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest#hashCode())`()` Returns the hash of [ScheduleCustomAudienceUpdateRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest#) object's data. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldReplacePendingUpdates](https://developer.android.com/reference/kotlin/android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest#shouldReplacePendingUpdates())`()` Returns`true`if any pending scheduled updates should be canceled and replaced with the update detailed in the current [ScheduleCustomAudienceUpdateRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest#). |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest#toString())`()` <br /> |

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
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`only if two [ScheduleCustomAudienceUpdateRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest#) objects contain the same information. |

### getMinDelay

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 

```
fun getMinDelay(): Duration
```

Returns the minimum [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#) that the update will be deferred before the service fetches updates for the buyer ad tech's custom audiences.

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------|
| [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#) | This value cannot be`null`. |

### getPartialCustomAudienceList

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 

```
fun getPartialCustomAudienceList(): MutableList<PartialCustomAudience!>
```

Returns the list of [PartialCustomAudience](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience) objects which are sent along with the request to download the updates for the buyer ad tech's custom audiences.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PartialCustomAudience](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience)!> | This value cannot be`null`. |

### getUpdateUri

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 

```
fun getUpdateUri(): Uri
```

Returns the [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) from which the update for the buyer's custom audiences will be fetched.

The [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) must use the same HTTPS site as the buyer ad tech's enrolled server.

| Return ||
|-----------------------------------------------------------------------------|-----------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | This value cannot be`null`. |

### hashCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns the hash of [ScheduleCustomAudienceUpdateRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest#) object's data.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### shouldReplacePendingUpdates

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 

```
fun shouldReplacePendingUpdates(): Boolean
```

Returns`true`if any pending scheduled updates should be canceled and replaced with the update detailed in the current [ScheduleCustomAudienceUpdateRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest#).

If this method returns`false`and there are previously requested updates still pending for the same buyer in the same app, a call to [android.adservices.customaudience.CustomAudienceManager#scheduleCustomAudienceUpdate(android.adservices.customaudience.ScheduleCustomAudienceUpdateRequest,java.util.concurrent.Executor,android.adservices.common.AdServicesOutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudienceManager#scheduleCustomAudienceUpdate(android.adservices.customaudience.ScheduleCustomAudienceUpdateRequest,%20java.util.concurrent.Executor,%20android.adservices.common.AdServicesOutcomeReceiver))with this [ScheduleCustomAudienceUpdateRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest#) will fail. 

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a human-readable representation of [ScheduleCustomAudienceUpdateRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/ScheduleCustomAudienceUpdateRequest#). |

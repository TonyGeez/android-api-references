# GroupCall

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GroupCall

Kotlin| [Java](GroupCall.md) 
| --- | --- |

```
open class GroupCall : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.mbms.GroupCall](GroupCall.md) |

Class used to represent a single MBMS group call. After a call has been started with [MbmsGroupCallSession.startGroupCall](../android.telephony/MbmsGroupCallSession.md)), this class is used to hold information about the call and control it.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_BY_USER_REQUEST](GroupCall.md) State changed due to a call to [close()](GroupCall.md))or [MbmsGroupCallSession.startGroupCall](../android.telephony/MbmsGroupCallSession.md)) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_FREQUENCY_CONFLICT](GroupCall.md) State changed due to a frequency conflict with another requested call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_LEFT_MBMS_BROADCAST_AREA](GroupCall.md) State changed due to the device leaving the area where this call is being broadcast. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_NONE](GroupCall.md) Indicates that the middleware does not have a reason to provide for the state change. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_NOT_CONNECTED_TO_HOMECARRIER_LTE](GroupCall.md) State changed due to the device leaving the home carrier's LTE network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_OUT_OF_MEMORY](GroupCall.md) State changed due to the middleware running out of memory |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_STALLED](GroupCall.md) Indicates that the group call is stalled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_STARTED](GroupCall.md) Indicates that the group call is started. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_STOPPED](GroupCall.md) Indicates that the group call is in a stopped state This can be reported after network action or after calling [close](GroupCall.md)). |
| --- | --- |

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](GroupCall.md))`()` Stop this group call. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTmgi](GroupCall.md))`()` Retrieve the TMGI (Temporary Mobile Group Identity) corresponding to this call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateGroupCall](GroupCall.md))`(`saiList:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>`, `frequencyList:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>`)` Send an update to the middleware when the SAI (Service Area Identifier) list and frequency information of the group call has \* changed. |
| --- | --- |

## Constants

### REASON_BY_USER_REQUEST

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_BY_USER_REQUEST: Int
```

State changed due to a call to [close()](GroupCall.md))or [MbmsGroupCallSession.startGroupCall](../android.telephony/MbmsGroupCallSession.md)) 

 Value: 1

### REASON_FREQUENCY_CONFLICT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_FREQUENCY_CONFLICT: Int
```

State changed due to a frequency conflict with another requested call. 

 Value: 3

### REASON_LEFT_MBMS_BROADCAST_AREA

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_LEFT_MBMS_BROADCAST_AREA: Int
```

State changed due to the device leaving the area where this call is being broadcast. 

 Value: 6

### REASON_NONE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_NONE: Int
```

Indicates that the middleware does not have a reason to provide for the state change. 

 Value: 0

### REASON_NOT_CONNECTED_TO_HOMECARRIER_LTE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_NOT_CONNECTED_TO_HOMECARRIER_LTE: Int
```

State changed due to the device leaving the home carrier's LTE network. 

 Value: 5

### REASON_OUT_OF_MEMORY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_OUT_OF_MEMORY: Int
```

State changed due to the middleware running out of memory 

 Value: 4

### STATE_STALLED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_STALLED: Int
```

Indicates that the group call is stalled. This may be due to a network issue or the device being temporarily out of range. 

 Value: 3

### STATE_STARTED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_STARTED: Int
```

Indicates that the group call is started. Data can be transmitted and received in this state. 

 Value: 2

### STATE_STOPPED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_STOPPED: Int
```

Indicates that the group call is in a stopped state This can be reported after network action or after calling [close](GroupCall.md)). 

 Value: 1

## Public methods

### close

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Stop this group call. Further operations on this object will fail with an [IllegalStateException](../java.lang/IllegalStateException.md). May throw an [IllegalStateException](../java.lang/IllegalStateException.md)

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### getTmgi

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTmgi(): Long
```

Retrieve the TMGI (Temporary Mobile Group Identity) corresponding to this call. 

### updateGroupCall

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun updateGroupCall(
    saiList: MutableList<Int!>, 
    frequencyList: MutableList<Int!>
): Unit
```

Send an update to the middleware when the SAI (Service Area Identifier) list and frequency information of the group call has \* changed. Callers must obtain this information from the wireless carrier independently.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `saiList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>:New list of SAIs that the call is available on. This value cannot be`null`. |
| `frequencyList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>:New list of frequencies that the call is available on. This value cannot be`null`. |

# EventStats

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EventStats

Kotlin| [Java](https://developer.android.com/reference/android/app/usage/EventStats "View this page in Java") 
| --- | --- |

```
class EventStats : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.usage.EventStats](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#) |

Contains usage statistics for an event type for a specific time range.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EventStats](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#EventStats(android.app.usage.EventStats))`(`stats:` ` [EventStats](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#)!`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [add](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#add(android.app.usage.EventStats))`(`right:` ` [EventStats](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#)!`)` Add the statistics from the right [EventStats](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#) to the left. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#describeContents())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#getCount())`()` Return the number of times that this event occurred over the interval. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEventType](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#getEventType())`()` Return the type of event this is usage for. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFirstTimeStamp](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#getFirstTimeStamp())`()` Get the beginning of the time range this [android.app.usage.EventStats](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#) represents, measured in milliseconds since the epoch. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLastEventTime](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#getLastEventTime())`()` Get the last time this event triggered, measured in milliseconds since the epoch. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLastTimeStamp](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#getLastTimeStamp())`()` Get the end of the time range this [android.app.usage.EventStats](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#) represents, measured in milliseconds since the epoch. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTotalTime](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#getTotalTime())`()` Get the total time this event was active, measured in milliseconds. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [EventStats](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### EventStats

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EventStats(stats: EventStats!)
```

## Public methods

### add

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun add(right: EventStats!): Unit
```

Add the statistics from the right [EventStats](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#) to the left. The event type for both [UsageStats](https://developer.android.com/reference/kotlin/android/app/usage/UsageStats) objects must be the same.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `right` | [EventStats](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#)!:The [EventStats](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#) object to merge into this one. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the event types of the two [UsageStats](https://developer.android.com/reference/kotlin/android/app/usage/UsageStats) objects are different. |

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getCount

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCount(): Int
```

Return the number of times that this event occurred over the interval. 

### getEventType

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEventType(): Int
```

Return the type of event this is usage for. May be one of the event constants in [UsageEvents.Event](https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event). 

### getFirstTimeStamp

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFirstTimeStamp(): Long
```

Get the beginning of the time range this [android.app.usage.EventStats](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#) represents, measured in milliseconds since the epoch.

<br />

See [System.currentTimeMillis()](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()). 

### getLastEventTime

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLastEventTime(): Long
```

Get the last time this event triggered, measured in milliseconds since the epoch.

<br />

See [System.currentTimeMillis()](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()). 

### getLastTimeStamp

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLastTimeStamp(): Long
```

Get the end of the time range this [android.app.usage.EventStats](https://developer.android.com/reference/kotlin/android/app/usage/EventStats#) represents, measured in milliseconds since the epoch.

<br />

See [System.currentTimeMillis()](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()). 

### getTotalTime

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTotalTime(): Long
```

Get the total time this event was active, measured in milliseconds. 

### writeToParcel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<EventStats!>
```

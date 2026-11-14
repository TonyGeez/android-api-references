# UsageEventsQuery

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UsageEventsQuery

Kotlin| [Java](https://developer.android.com/reference/android/app/usage/UsageEventsQuery "View this page in Java") 
| --- | --- |

```
class UsageEventsQuery : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.usage.UsageEventsQuery](https://developer.android.com/reference/kotlin/android/app/usage/UsageEventsQuery#) |

An Object-Oriented representation for a [UsageEvents](https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents) query. Used by [UsageStatsManager.queryEvents(UsageEventsQuery)](https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryEvents(android.app.usage.UsageEventsQuery))call.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/app/usage/UsageEventsQuery.Builder) Builder for UsageEventsQuery. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/usage/UsageEventsQuery#describeContents())`()` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getBeginTimeMillis](https://developer.android.com/reference/kotlin/android/app/usage/UsageEventsQuery#getBeginTimeMillis())`()` Returns the inclusive timestamp to indicate the beginning of the range of events. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getEndTimeMillis](https://developer.android.com/reference/kotlin/android/app/usage/UsageEventsQuery#getEndTimeMillis())`()` Returns the exclusive timestamp to indicate the end of the range of events. |
| --- | --- |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getEventTypes](https://developer.android.com/reference/kotlin/android/app/usage/UsageEventsQuery#getEventTypes())`()` Retrieves the usage event types for the query. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getPackageNames](https://developer.android.com/reference/kotlin/android/app/usage/UsageEventsQuery#getPackageNames())`()` Retrieves a`Set`of package names for the query. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/usage/UsageEventsQuery#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [UsageEventsQuery](https://developer.android.com/reference/kotlin/android/app/usage/UsageEventsQuery#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/usage/UsageEventsQuery#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getBeginTimeMillis

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBeginTimeMillis(): Long
```

Returns the inclusive timestamp to indicate the beginning of the range of events. Defined in terms of "Unix time", see [java.lang.System#currentTimeMillis](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()). 
Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z. |

### getEndTimeMillis

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEndTimeMillis(): Long
```

Returns the exclusive timestamp to indicate the end of the range of events. Defined in terms of "Unix time", see [java.lang.System#currentTimeMillis](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()). 
Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z. |

### getEventTypes

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEventTypes(): IntArray
```

Retrieves the usage event types for the query.

Note that an empty array indicates querying all usage event types, and it may cause additional system overhead when calling [UsageStatsManager.queryEvents(UsageEventsQuery)](https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryEvents(android.app.usage.UsageEventsQuery)). Apps are encouraged to provide a list of event types via [Builder.setEventTypes(int...)](https://developer.android.com/reference/kotlin/android/app/usage/UsageEventsQuery.Builder#setEventTypes(kotlin.Int))

| Return ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | an array contains the usage event types that was previously set using [Builder.setEventTypes(int...)](https://developer.android.com/reference/kotlin/android/app/usage/UsageEventsQuery.Builder#setEventTypes(kotlin.Int))or an empty array if no value has been set. This value cannot be`null`. Value is [android.app.usage.UsageEvents.Event#NONE](https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#NONE:kotlin.Int), [android.app.usage.UsageEvents.Event#ACTIVITY_RESUMED](https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#ACTIVITY_RESUMED:kotlin.Int), [android.app.usage.UsageEvents.Event#ACTIVITY_PAUSED](https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#ACTIVITY_PAUSED:kotlin.Int), android.app.usage.UsageEvents.Event.END_OF_DAY, android.app.usage.UsageEvents.Event.CONTINUE_PREVIOUS_DAY, [android.app.usage.UsageEvents.Event#CONFIGURATION_CHANGE](https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#CONFIGURATION_CHANGE:kotlin.Int), android.app.usage.UsageEvents.Event.SYSTEM_INTERACTION, [android.app.usage.UsageEvents.Event#USER_INTERACTION](https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#USER_INTERACTION:kotlin.Int), [android.app.usage.UsageEvents.Event#SHORTCUT_INVOCATION](https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#SHORTCUT_INVOCATION:kotlin.Int), android.app.usage.UsageEvents.Event.CHOOSER_ACTION, android.app.usage.UsageEvents.Event.NOTIFICATION_SEEN, [android.app.usage.UsageEvents.Event#STANDBY_BUCKET_CHANGED](https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#STANDBY_BUCKET_CHANGED:kotlin.Int), android.app.usage.UsageEvents.Event.NOTIFICATION_INTERRUPTION, android.app.usage.UsageEvents.Event.SLICE_PINNED_PRIV, android.app.usage.UsageEvents.Event.SLICE_PINNED, [android.app.usage.UsageEvents.Event#SCREEN_INTERACTIVE](https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#SCREEN_INTERACTIVE:kotlin.Int), [android.app.usage.UsageEvents.Event#SCREEN_NON_INTERACTIVE](https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#SCREEN_NON_INTERACTIVE:kotlin.Int), [android.app.usage.UsageEvents.Event#KEYGUARD_SHOWN](https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#KEYGUARD_SHOWN:kotlin.Int), [android.app.usage.UsageEvents.Event#KEYGUARD_HIDDEN](https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#KEYGUARD_HIDDEN:kotlin.Int), [android.app.usage.UsageEvents.Event#FOREGROUND_SERVICE_START](https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#FOREGROUND_SERVICE_START:kotlin.Int), [android.app.usage.UsageEvents.Event#FOREGROUND_SERVICE_STOP](https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#FOREGROUND_SERVICE_STOP:kotlin.Int), android.app.usage.UsageEvents.Event.CONTINUING_FOREGROUND_SERVICE, android.app.usage.UsageEvents.Event.ROLLOVER_FOREGROUND_SERVICE, [android.app.usage.UsageEvents.Event#ACTIVITY_STOPPED](https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#ACTIVITY_STOPPED:kotlin.Int), android.app.usage.UsageEvents.Event.ACTIVITY_DESTROYED, android.app.usage.UsageEvents.Event.FLUSH_TO_DISK, [android.app.usage.UsageEvents.Event#DEVICE_SHUTDOWN](https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#DEVICE_SHUTDOWN:kotlin.Int), [android.app.usage.UsageEvents.Event#DEVICE_STARTUP](https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#DEVICE_STARTUP:kotlin.Int), android.app.usage.UsageEvents.Event.USER_UNLOCKED, android.app.usage.UsageEvents.Event.USER_STOPPED, android.app.usage.UsageEvents.Event.LOCUS_ID_SET, or android.app.usage.UsageEvents.Event.APP_COMPONENT_USED |

### getPackageNames

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPackageNames(): MutableSet<String!>
```

Retrieves a`Set`of package names for the query.

Note that an empty set indicates querying usage events for all packages, and it may cause additional system overhead when calling [UsageStatsManager.queryEvents(UsageEventsQuery)](https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryEvents(android.app.usage.UsageEventsQuery)). Apps are encouraged to provide a list of package names via [Builder.setPackageNames(String...)](https://developer.android.com/reference/kotlin/android/app/usage/UsageEventsQuery.Builder#setPackageNames(kotlin.String))

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | a`Set`contains the package names that was previously set through [Builder.setPackageNames(String...)](https://developer.android.com/reference/kotlin/android/app/usage/UsageEventsQuery.Builder#setPackageNames(kotlin.String))or an empty set if no value has been set. This value cannot be`null`. |

### writeToParcel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<UsageEventsQuery!>
```

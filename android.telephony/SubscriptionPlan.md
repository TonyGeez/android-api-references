# SubscriptionPlan

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SubscriptionPlan

Kotlin| [Java](https://developer.android.com/reference/android/telephony/SubscriptionPlan "View this page in Java") 
| --- | --- |

```
class SubscriptionPlan : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.SubscriptionPlan](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#) |

Description of a billing relationship plan between a carrier and a specific subscriber. This information is used to present more useful UI to users, such as explaining how much mobile data they have remaining, and what will happen when they run out. If specifying network types, the developer must supply at least one plan that applies to all network types (default), and all additional plans may not include a particular network type more than once. This is enforced by [SubscriptionManager](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager) when setting the plans. Plan selection will prefer plans that have specific network types defined over plans that apply to all network types.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan.Builder) Builder for a [SubscriptionPlan](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#). |

| Constants ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [BYTES_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#BYTES_UNKNOWN:kotlin.Long) Value indicating a number of bytes is unknown. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [BYTES_UNLIMITED](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#BYTES_UNLIMITED:kotlin.Long) Value indicating a number of bytes is unlimited. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LIMIT_BEHAVIOR_BILLED](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#LIMIT_BEHAVIOR_BILLED:kotlin.Int) When a resource limit is hit, the user is billed automatically. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LIMIT_BEHAVIOR_DISABLED](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#LIMIT_BEHAVIOR_DISABLED:kotlin.Int) When a resource limit is hit, access is disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LIMIT_BEHAVIOR_THROTTLED](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#LIMIT_BEHAVIOR_THROTTLED:kotlin.Int) When a resource limit is hit, access is throttled to a slower rate. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LIMIT_BEHAVIOR_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#LIMIT_BEHAVIOR_UNKNOWN:kotlin.Int) When a resource limit is hit, the behavior is unknown. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUBSCRIPTION_STATUS_ACTIVE](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#SUBSCRIPTION_STATUS_ACTIVE:kotlin.Int) Subscription is active. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUBSCRIPTION_STATUS_INACTIVE](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#SUBSCRIPTION_STATUS_INACTIVE:kotlin.Int) Subscription is inactive. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUBSCRIPTION_STATUS_SUSPENDED](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#SUBSCRIPTION_STATUS_SUSPENDED:kotlin.Int) Subscription is suspended. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUBSCRIPTION_STATUS_TRIAL](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#SUBSCRIPTION_STATUS_TRIAL:kotlin.Int) Subscription is in a trial period. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUBSCRIPTION_STATUS_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#SUBSCRIPTION_STATUS_UNKNOWN:kotlin.Int) Subscription status is unknown. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [TIME_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#TIME_UNKNOWN:kotlin.Long) Value indicating a timestamp is unknown. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [Range](https://developer.android.com/reference/kotlin/android/util/Range.html#)\< [ZonedDateTime](https://developer.android.com/reference/kotlin/java/time/ZonedDateTime.html#)!\>!\>! | [cycleIterator](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#cycleIterator())`()` Return an iterator that will return all valid data usage cycles based on any recurrence rules. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDataLimitBehavior](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#getDataLimitBehavior())`()` Return the behavior of data access when usage reaches [getDataLimitBytes()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#getDataLimitBytes()). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDataLimitBytes](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#getDataLimitBytes())`()` Return the usage threshold at which data access changes according to [getDataLimitBehavior()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#getDataLimitBehavior()). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDataUsageBytes](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#getDataUsageBytes())`()` Return a snapshot of currently known mobile data usage at [getDataUsageTime()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#getDataUsageTime()). |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDataUsageTime](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#getDataUsageTime())`()` Return the time at which [getDataUsageBytes()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#getDataUsageBytes())was valid. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getNetworkTypes](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#getNetworkTypes())`()` Return an array containing all network types this SubscriptionPlan applies to. |
| [ZonedDateTime](https://developer.android.com/reference/kotlin/java/time/ZonedDateTime.html#)? | [getPlanEndDate](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#getPlanEndDate())`()` Return the end date of this plan, or null if no end date exists. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSubscriptionStatus](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#getSubscriptionStatus())`()` Returns the status of the subscription plan. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getSummary](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#getSummary())`()` Return the short summary of this plan. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getTitle](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#getTitle())`()` Return the short title of this plan. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [SubscriptionPlan](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### BYTES_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BYTES_UNKNOWN: Long
```

Value indicating a number of bytes is unknown. 

 Value: -1L

### BYTES_UNLIMITED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BYTES_UNLIMITED: Long
```

Value indicating a number of bytes is unlimited. 

 Value: 9223372036854775807L

### LIMIT_BEHAVIOR_BILLED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIMIT_BEHAVIOR_BILLED: Int
```

When a resource limit is hit, the user is billed automatically. 

 Value: 1

### LIMIT_BEHAVIOR_DISABLED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIMIT_BEHAVIOR_DISABLED: Int
```

When a resource limit is hit, access is disabled. 

 Value: 0

### LIMIT_BEHAVIOR_THROTTLED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIMIT_BEHAVIOR_THROTTLED: Int
```

When a resource limit is hit, access is throttled to a slower rate. 

 Value: 2

### LIMIT_BEHAVIOR_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIMIT_BEHAVIOR_UNKNOWN: Int
```

When a resource limit is hit, the behavior is unknown. 

 Value: -1

### SUBSCRIPTION_STATUS_ACTIVE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBSCRIPTION_STATUS_ACTIVE: Int
```

Subscription is active. 

 Value: 1

### SUBSCRIPTION_STATUS_INACTIVE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBSCRIPTION_STATUS_INACTIVE: Int
```

Subscription is inactive. 

 Value: 2

### SUBSCRIPTION_STATUS_SUSPENDED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBSCRIPTION_STATUS_SUSPENDED: Int
```

Subscription is suspended. 

 Value: 4

### SUBSCRIPTION_STATUS_TRIAL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBSCRIPTION_STATUS_TRIAL: Int
```

Subscription is in a trial period. 

 Value: 3

### SUBSCRIPTION_STATUS_UNKNOWN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBSCRIPTION_STATUS_UNKNOWN: Int
```

Subscription status is unknown. 

 Value: 0

### TIME_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIME_UNKNOWN: Long
```

Value indicating a timestamp is unknown. 

 Value: -1L

## Public methods

### cycleIterator

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun cycleIterator(): MutableIterator<Range<ZonedDateTime!>!>!
```

Return an iterator that will return all valid data usage cycles based on any recurrence rules. The iterator starts from the currently active cycle and walks backwards through time. 

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|--------------------------|
| `obj` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getDataLimitBehavior

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDataLimitBehavior(): Int
```

Return the behavior of data access when usage reaches [getDataLimitBytes()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#getDataLimitBytes()).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.telephony.SubscriptionPlan#LIMIT_BEHAVIOR_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#LIMIT_BEHAVIOR_UNKNOWN:kotlin.Int), [android.telephony.SubscriptionPlan#LIMIT_BEHAVIOR_DISABLED](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#LIMIT_BEHAVIOR_DISABLED:kotlin.Int), [android.telephony.SubscriptionPlan#LIMIT_BEHAVIOR_BILLED](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#LIMIT_BEHAVIOR_BILLED:kotlin.Int), or [android.telephony.SubscriptionPlan#LIMIT_BEHAVIOR_THROTTLED](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#LIMIT_BEHAVIOR_THROTTLED:kotlin.Int) |

### getDataLimitBytes

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDataLimitBytes(): Long
```

Return the usage threshold at which data access changes according to [getDataLimitBehavior()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#getDataLimitBehavior()). 
Value is a non-negative number of bytes.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative number of bytes. |

### getDataUsageBytes

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDataUsageBytes(): Long
```

Return a snapshot of currently known mobile data usage at [getDataUsageTime()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#getDataUsageTime()). 
Value is a non-negative number of bytes.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative number of bytes. |

### getDataUsageTime

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDataUsageTime(): Long
```

Return the time at which [getDataUsageBytes()](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#getDataUsageBytes())was valid. 
Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z. |

### getNetworkTypes

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNetworkTypes(): IntArray
```

Return an array containing all network types this SubscriptionPlan applies to.

| Return ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | This value cannot be`null`. Value is [android.telephony.TelephonyManager#NETWORK_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UNKNOWN:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_GPRS](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GPRS:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_EDGE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EDGE:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_UMTS](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UMTS:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_CDMA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_CDMA:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_EVDO_0](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_0:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_EVDO_A](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_A:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_1xRTT](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_1xRTT:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_HSDPA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSDPA:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_HSUPA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSUPA:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_HSPA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPA:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_IDEN](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_IDEN:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_EVDO_B](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_B:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_LTE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_LTE:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_EHRPD](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EHRPD:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_HSPAP](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPAP:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_GSM](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GSM:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_TD_SCDMA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_TD_SCDMA:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_IWLAN](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_IWLAN:kotlin.Int), or [android.telephony.TelephonyManager#NETWORK_TYPE_NR](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_NR:kotlin.Int) |

**See Also**

- [android.telephony.TelephonyManager](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager) 

### getPlanEndDate

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPlanEndDate(): ZonedDateTime?
```

Return the end date of this plan, or null if no end date exists. 

### getSubscriptionStatus

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSubscriptionStatus(): Int
```

Returns the status of the subscription plan.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The subscription status, or [SUBSCRIPTION_STATUS_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#SUBSCRIPTION_STATUS_UNKNOWN:kotlin.Int) if not available. Value is [android.telephony.SubscriptionPlan#SUBSCRIPTION_STATUS_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#SUBSCRIPTION_STATUS_UNKNOWN:kotlin.Int), [android.telephony.SubscriptionPlan#SUBSCRIPTION_STATUS_ACTIVE](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#SUBSCRIPTION_STATUS_ACTIVE:kotlin.Int), [android.telephony.SubscriptionPlan#SUBSCRIPTION_STATUS_INACTIVE](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#SUBSCRIPTION_STATUS_INACTIVE:kotlin.Int), [android.telephony.SubscriptionPlan#SUBSCRIPTION_STATUS_TRIAL](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#SUBSCRIPTION_STATUS_TRIAL:kotlin.Int), or [android.telephony.SubscriptionPlan#SUBSCRIPTION_STATUS_SUSPENDED](https://developer.android.com/reference/kotlin/android/telephony/SubscriptionPlan#SUBSCRIPTION_STATUS_SUSPENDED:kotlin.Int) |

### getSummary

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSummary(): CharSequence?
```

Return the short summary of this plan.

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | This value may be`null`. |

### getTitle

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTitle(): CharSequence?
```

Return the short title of this plan.

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | This value may be`null`. |

### hashCode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

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
static val CREATOR: Parcelable.Creator<SubscriptionPlan!>
```
